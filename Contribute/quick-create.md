---
title: "Hızlı başlangıç: Azure Key Vault'tan gizli dizi ayarlama ve alma | Microsoft Docs"
description: "Hızlı başlangıç: Azure Key Vault'tan gizli dizi ayarlama ve alma"
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages, keyvault-platforms
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 8b758274203748bb6e04c03dec5de38fb77947b4
ms.sourcegitcommit: b0105f322f91bb4dbde47f6da35b3c12271d5b03
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43239576"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a>Hızlı başlangıç: Azure Key Vault'tan gizli dizi ayarlama ve alma

Bu hızlı başlangıçta Anahtar Kasasında gizli dizi depolama ve bunu Web uygulaması kullanarak alma adımları gösterilmektedir. Gizli dizi değerini görmek için bunu Azure'da çalıştırmanız gerekir. Bu hızlı başlangıçta Node.js ve Yönetilen Hizmet Kimlikleri (MSI) kullanılmaktadır.

> [!div class="checklist"]
> * Anahtar Kasası oluşturun.
> * Anahtar Kasasında bir gizli dizi depolayın.
> * Anahtar Kasasındaki bir gizli diziyi alın.
> * Azure Web Uygulaması oluşturun.
> * [Yönetilen hizmet kimliklerini etkinleştirin](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).
> * Web uygulamasının Anahtar Kasasından verileri okuması için gereken izinleri verin.

Devam etmeden önce [temel kavramlar](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts) hakkında bilgi sahibi olduğunuzdan emin olun.

>[!NOTE]
Aşağıdaki öğreticinin neden en iyi yöntem olduğunu anlamak için bilmeniz gereken birkaç kavram vardır. Key Vault, gizli dizilerin program aracılığıyla depolandığı merkezi bir depodur. Bunu yapmak için uygulamaların/kullanıcıların gizli dizi sunarak Key Vault kimlik doğrulamasından geçmesi gerekir. Güvenlikle ilgili en iyi yöntemlerin uygulanması için bu ilk gizli dizinin de düzenli olarak döndürülmesi gerekir. Ancak [Yönetilen Hizmet Kimliği](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) sayesinde Azure'da çalışan uygulamalara Azure tarafından otomatik olarak yönetilen bir kimlik verilir. Bu da **Gizli Dizi Belirleme Sorununu** çözerek kullanıcıların/uygulamaların en iyi yöntemleri uygulamasına ve ilk gizli diziyi döndürme konusunda endişelenmemesine yardımcı olur.

## <a name="prerequisites"></a>Önkoşullar

::: zone pivot="nodejs"
* [Node JS](https://nodejs.org/en/) ::: zone-end

::: zone pivot="dotnet, windows"
* [Visual Studio 2017 sürüm 15.7.3 veya üzeri](https://www.microsoft.com/net/download/windows), aşağıdaki iş yükleriyle birlikte:
  * ASP.NET ve web geliştirme
  * .NET Core çoklu platform geliştirme
* [.NET Core 2.1 SDK veya üzeri](https://www.microsoft.com/net/download/windows) :::zone-end

::: zone pivot="dotnet, mac"
* Bkz. [Mac için Visual Studio'daki Yenilikler](https://visualstudio.microsoft.com/vs/mac/).
:::zone-end

* Git ([indir](https://git-scm.com/downloads)).
* Azure aboneliği. Azure aboneliğiniz yoksa başlamadan önce [ücretsiz bir hesap](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) oluşturun.
* [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) 2.0.4 veya sonraki sürümü. Bu uygulama Windows, Mac ve Linux’ta kullanılabilir.

## <a name="login-to-azure"></a>Azure'da oturum açma

CLI kullanarak Azure'da oturum açmak için şunu yazabilirsiniz:

```azurecli
az login
```

## <a name="create-resource-group"></a>Kaynak grubu oluşturma

[az group create](/cli/azure/group#az-group-create) komutuyla bir kaynak grubu oluşturun. Azure kaynak grubu, Azure kaynaklarının dağıtıldığı ve yönetildiği mantıksal bir kapsayıcıdır.

Lütfen bir Kaynak Grubu adı seçin ve yer tutucunun yerine yazın.
Aşağıdaki örnekte, *eastus* konumunda *<YourResourceGroupName>* adlı bir kaynak grubu oluşturulur.

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

Az önce oluşturduğunuz kaynak grubu bu öğretici boyunca kullanılır.

## <a name="create-an-azure-key-vault"></a>Azure Key Vault oluşturma

Daha sonra, önceki adımda oluşturulan kaynak grubunda bir Anahtar Kasası oluşturursunuz. Bu makale boyunca Anahtar Kasası için “ContosoKeyVault” adı kullanılıyor olsa da, sizin benzersiz bir ad kullanmanız gerekir. Şu bilgileri belirtin:

* Kasa adı: **Buradan bir Anahtar Kasası adı seçin**.
* Kaynak grubu adı: **Buradan bir Kaynak Grubu Adı seçin**.
* Konum: **Doğu ABD**.

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

Bu noktada Azure hesabınız, bu yeni anahtar kasasında herhangi bir işlemi gerçekleştirmeye yetkili olan tek hesaptır.

## <a name="add-a-secret-to-key-vault"></a>Anahtar kasasına gizli dizi ekleme

Bunun nasıl çalıştığını göstermemize yardımcı olması için bir gizli dizi ekliyoruz. Güvenle korumanız ama uygulamanıza da sağlamanız gereken bir SQL bağlantı dizesini veya başka bir bilgiyi depoluyor olabilirsiniz. Bu öğreticide, parola **AppSecret** olarak adlandırılır ve içinde **MySecret** değeri depolanır.

Anahtar Kasasında **MySecret** değerini depolayacak **AppSecret** adlı gizli dizi oluşturmak için aşağıdaki komutları yazın:

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

Gizli dizi içindeki değeri düz metin olarak görüntülemek için:

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

Bu komut, URI de dahil olmak üzere gizli bilgiyi gösterir. Bu adımları tamamladıktan sonra, Azure Key Vault'ta bu gizli dizinin URI'sine sahip olmalısınız. Bu bilgileri bir yere yazın. Sonraki adımlardan birinde gerekecektir.

## <a name="clone-the-repo"></a>Depoyu kopyalama

Aşağıdaki komutu kullanarak kaynağı düzenleyebilmeniz için yerel kopyasını oluşturmak üzere depoyu kopyalayın:

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a>Bağımlılıkları yükleme

Bu adımda bağımlılıkları yükleyeceksiniz. Şu komutları çalıştırın: cd key-vault-node-quickstart npm install

Bu projede 2 düğüm modülü kullanılmaktadır:

* [ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure) 
* [azure-keyvault](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a>Web uygulamasını Azure’da yayımlama

Yapmanız gereken birkaç adım aşağıda gösterilmiştir

* 1. adım, [Azure App Service](https://azure.microsoft.com/services/app-service/) Planı oluşturmaktır. Bu planda birden fazla web uygulaması depolayabilirsiniz.

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* Sonraki adımda bir web uygulaması oluşturmanız gerekir. Aşağıdaki örnekte <app_name> kısmını genel olarak benzersiz bir uygulama adıyla değiştirin (geçerli karakterler a-z, 0-9 ve - şeklindedir). Çalışma zamanı NODE|6.9 olarak ayarlanmıştır. Desteklenen tüm çalışma zamanlarını görmek için şu komutu çalıştırın: az webapp list-runtimes

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    Web uygulaması oluşturulduğunda Azure CLI aşağıda yer alan çıktıdaki gibi bilgiler gösterir:

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    Yeni oluşturduğunuz web uygulamasına göz attığınızda çalışan bir web uygulaması görmeniz gerekir. <app_name> değerini benzersiz bir uygulama adıyla değiştirin.

    ```text
    http://<app name>.azurewebsites.net
    ```
    Yukarıdaki komut ayrıca yerel git ortamınızdan Azure'a dağıtım yapmanızı sağlayan Git özellikli bir uygulama oluşturur. 
    Yerel git, şu URL'ye sahiptir: 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'

* Dağıtım kullanıcısı oluşturma Bir önceki komut tamamlandıktan sonra yerel Git deponuza bir Azure uzak bağlantı ekleyebilirsiniz. <url> yerine Uygulamanız için Git'i etkinleştirme adımında aldığınız Git uzak ortamının URL'sini yazın.

    ```bash
    git remote add azure <url>
    ```
::: zone-end

::: zone pivot="dotnet"

## <a name="open-and-edit-the-solution"></a>Çözümü açma ve düzenleme

Belirlediğiniz anahtar kasanızın adıyla örneği çalıştırmak için program.cs dosyasını düzenleyin:

1. key-vault-dotnet-core-quickstart klasörüne gidin.
2. Visual Studio 2017'de key-vault-dotnet-core-quickstart.sln dosyasını açın.
3. Program.cs dosyasını açın ve *YourKeyVaultName* yer tutucusunu daha önce oluşturduğunuz anahtar kasanızın adıyla güncelleştirin.

Bu çözümde [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) ve [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet kitaplıkları kullanılır.

## <a name="run-the-app"></a>Uygulamayı çalıştırma

Visual Studio 2017 ana menüsünde **Hata Ayıkla** > **Hata ayıklamadan başlat** seçeneğini belirleyin. Tarayıcı görüntülendiğinde **Hakkında** sayfasına gidin. **AppSecret** değeri görüntülenir.

## <a name="publish-the-web-application-to-azure"></a>Web uygulamasını Azure’da yayımlama

Canlı web uygulaması olarak görüntülemek için bu uygulamayı Azure'da yayımlayın ve gizli dizi değerini getirebildiğinizi görmek için:

1. Visual Studio'da **key-vault-dotnet-core-quickstart** projesini seçin.
2. **Yayımla** > **Başlat** seçeneğini belirleyin.
3. Yeni bir **App Service** oluşturun ve ardından **Yayımla** seçeneğini belirleyin.
4. Uygulama adını **keyvaultdotnetcorequickstart** olarak değiştirin.
5. **Oluştur**’u seçin.

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]

::: zone-end

## <a name="enable-managed-service-identities"></a>Yönetilen hizmet kimliklerini etkinleştirme

Azure Key Vault kimlik bilgilerini ve diğer anahtarlarla gizli dizileri güvenle depolamak için bir yol sağlar, ama bunları alabilmek için kodunuzun Azure Key Vault'ta kimlik doğrulaması yapması gerekir. Yönetilen Hizmet Kimliği, Azure Active Directory'de (Azure AD) Azure hizmetlerine otomatik olarak yönetilen bir kimlik vererek bu işlemi kolaylaştırır. Bu kimliği kullanarak, Key Vault da dahil olmak üzere Azure AD kimlik doğrulamasını destekleyen tüm hizmetlerde kodunuzda kimlik bilgileri bulunmasına gerek kalmadan kimlik doğrulaması yapabilirsiniz.

1. Azure CLI'ye dönün.
2. Bu uygulamanın kimliğini oluşturmak için assign-identity komutunu çalıştırın:

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
>Bu yordamdaki komut, portala gidip web uygulaması özelliklerinde **Yönetilen hizmet kimliğini** **Açık** duruma getirmekle eşdeğerdir.

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a>Key Vault gizli dizilerini okumak için uygulamanıza izin atama

Uygulamayı Azure'da yayımladığınızda çıktıyı not edin. Şu biçimde olmalıdır:

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

Ardından anahtar kasanızın adını ve **PrincipalId** değerini kullanarak şu komutu çalıştırın:

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a>Node Uygulamasını Azure'a dağıtma ve gizli diziyi alma

Tüm ayarları yaptınız. Uygulamayı Azure'a dağıtmak için aşağıdaki komutu çalıştırın

```bash
git push azure master
```

Ardından https://<app_name>.azurewebsites.net adresine gittiğinizde gizli diziyi görebilirsiniz.
<YourKeyVaultName> yerine kasanızın adını yazdığınızdan emin olun ::: zone-end

::: zone pivot="dotnet" Uygulamayı çalıştırdığınızda gizli dizi değerinizin alındığını görürsünüz.
::: zone-end

## <a name="next-steps"></a>Sonraki adımlar

::: zone pivot="nodejs"
* [Azure Key Vault Ana Sayfası](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault Belgeleri](https://docs.microsoft.com/azure/key-vault/)
* [Node için Azure SDK](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [Azure REST API Başvurusu](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end

::: zone pivot="dotnet"
* [Azure Key Vault ana sayfası](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault belgeleri](https://docs.microsoft.com/azure/key-vault/)
* [.NET için Azure SDK](https://github.com/Azure/azure-sdk-for-net)
* [Azure REST API başvurusu](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end