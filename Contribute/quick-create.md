---
title: "Hızlı başlangıç: Azure Key Vault'tan gizli dizi ayarlama ve alma | Microsoft Docs"
description: "Hızlı başlangıç: Azure Key Vault'tan gizli dizi ayarlama ve alma"
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 497631fe46ac4e2c9c495a609547753a84d662bf
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805758"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="665af-103">Hızlı başlangıç: Azure Key Vault'tan gizli dizi ayarlama ve alma</span><span class="sxs-lookup"><span data-stu-id="665af-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="665af-104">Bu hızlı başlangıçta Anahtar Kasasında gizli dizi depolama ve bunu Web uygulaması kullanarak alma adımları gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="665af-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="665af-105">Gizli dizi değerini görmek için bunu Azure'da çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="665af-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="665af-106">Bu hızlı başlangıçta Node.js ve Yönetilen Hizmet Kimlikleri (MSI) kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="665af-106">The quickstart uses Node.js and Managed service identities (MSIs).</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="665af-107">Anahtar Kasası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="665af-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="665af-108">Anahtar kasasında bir gizli dizi depolayın.</span><span class="sxs-lookup"><span data-stu-id="665af-108">Store a secret in the Key Vault.</span></span>
> * <span data-ttu-id="665af-109">Anahtar Kasasındaki bir gizli diziyi alın.</span><span class="sxs-lookup"><span data-stu-id="665af-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="665af-110">Azure Web Uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="665af-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="665af-111">[Yönetilen hizmet kimliklerini etkinleştirin](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span><span class="sxs-lookup"><span data-stu-id="665af-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="665af-112">Web uygulamasının Anahtar Kasasından verileri okuması için gereken izinleri verin.</span><span class="sxs-lookup"><span data-stu-id="665af-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="665af-113">Devam etmeden önce [temel kavramlar](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts) hakkında bilgi sahibi olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="665af-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

> [!NOTE]
> <span data-ttu-id="665af-114">Aşağıdaki öğreticinin neden en iyi yöntem olduğunu anlamak için bilmeniz gereken birkaç kavram vardır.</span><span class="sxs-lookup"><span data-stu-id="665af-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="665af-115">Key Vault, gizli dizilerin program aracılığıyla depolandığı merkezi bir depodur.</span><span class="sxs-lookup"><span data-stu-id="665af-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="665af-116">Bunu yapmak için uygulamaların/kullanıcıların gizli dizi sunarak Key Vault kimlik doğrulamasından geçmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="665af-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="665af-117">Güvenlikle ilgili en iyi yöntemlerin uygulanması için bu ilk gizli dizinin de düzenli olarak döndürülmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="665af-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="665af-118">Ancak [Yönetilen Hizmet Kimliği](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) sayesinde Azure’da çalışan uygulamalara Azure tarafından otomatik olarak yönetilen bir kimlik verilir.</span><span class="sxs-lookup"><span data-stu-id="665af-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview), applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="665af-119">Bu da **Gizli Dizi Belirleme Sorununu** çözerek kullanıcıların/uygulamaların en iyi yöntemleri uygulamasına ve ilk gizli diziyi döndürme konusunda endişelenmemesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="665af-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="665af-120">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="665af-120">Prerequisites</span></span>

::: zone pivot="nodejs"
* [<span data-ttu-id="665af-121">Node JS</span><span class="sxs-lookup"><span data-stu-id="665af-121">Node JS</span></span>](https://nodejs.org/en/)
::: zone-end
::: zone pivot="dotnet"
* <span data-ttu-id="665af-122">[Visual Studio 2017 sürüm 15.7.3 veya üzeri](https://www.microsoft.com/net/download/windows), aşağıdaki iş yükleriyle birlikte:</span><span class="sxs-lookup"><span data-stu-id="665af-122">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="665af-123">ASP.NET ve web geliştirme</span><span class="sxs-lookup"><span data-stu-id="665af-123">ASP.NET and web development</span></span>
  * <span data-ttu-id="665af-124">.NET Core çoklu platform geliştirme</span><span class="sxs-lookup"><span data-stu-id="665af-124">.NET Core cross-platform development</span></span>
* [<span data-ttu-id="665af-125">.NET Core 2.1 SDK’sı veya üzeri</span><span class="sxs-lookup"><span data-stu-id="665af-125">.NET Core 2.1 SDK or later</span></span>](https://www.microsoft.com/net/download/windows)
::: zone-end
* <span data-ttu-id="665af-126">Git ([indir](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="665af-126">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="665af-127">Azure aboneliği.</span><span class="sxs-lookup"><span data-stu-id="665af-127">An Azure subscription.</span></span> <span data-ttu-id="665af-128">Azure aboneliğiniz yoksa başlamadan önce [ücretsiz bir hesap](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="665af-128">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="665af-129">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) 2.0.4 veya sonraki sürümü.</span><span class="sxs-lookup"><span data-stu-id="665af-129">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="665af-130">Bu uygulama Windows, Mac ve Linux’ta kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="665af-130">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="665af-131">Azure'da oturum açma</span><span class="sxs-lookup"><span data-stu-id="665af-131">Login to Azure</span></span>

<span data-ttu-id="665af-132">CLI kullanarak Azure'da oturum açmak için şunu yazabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="665af-132">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="665af-133">Kaynak grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="665af-133">Create resource group</span></span>

<span data-ttu-id="665af-134">[az group create](/cli/azure/group#az-group-create) komutuyla bir kaynak grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="665af-134">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="665af-135">Azure kaynak grubu, Azure kaynaklarının dağıtıldığı ve yönetildiği mantıksal bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="665af-135">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="665af-136">Lütfen bir Kaynak Grubu adı seçin ve yer tutucunun yerine yazın.</span><span class="sxs-lookup"><span data-stu-id="665af-136">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="665af-137">Aşağıdaki örnekte, *eastus* konumunda *<YourResourceGroupName>* adlı bir kaynak grubu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="665af-137">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="665af-138">Az önce oluşturduğunuz kaynak grubu bu öğretici boyunca kullanılır.</span><span class="sxs-lookup"><span data-stu-id="665af-138">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="665af-139">Azure Key Vault oluşturma</span><span class="sxs-lookup"><span data-stu-id="665af-139">Create an Azure Key Vault</span></span>

<span data-ttu-id="665af-140">Daha sonra, önceki adımda oluşturulan kaynak grubunda bir Anahtar Kasası oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="665af-140">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="665af-141">Bu makale boyunca Anahtar Kasası için “ContosoKeyVault” adı kullanılıyor olsa da, sizin benzersiz bir ad kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="665af-141">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="665af-142">Şu bilgileri belirtin:</span><span class="sxs-lookup"><span data-stu-id="665af-142">Provide the following information:</span></span>

* <span data-ttu-id="665af-143">Kasa adı: **Buradan bir Anahtar Kasası adı seçin**.</span><span class="sxs-lookup"><span data-stu-id="665af-143">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="665af-144">Kaynak grubu adı: **Buradan bir Kaynak Grubu Adı seçin**.</span><span class="sxs-lookup"><span data-stu-id="665af-144">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="665af-145">Konum: **Doğu ABD**.</span><span class="sxs-lookup"><span data-stu-id="665af-145">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="665af-146">Bu noktada Azure hesabınız, bu yeni anahtar kasasında herhangi bir işlemi gerçekleştirmeye yetkili olan tek hesaptır.</span><span class="sxs-lookup"><span data-stu-id="665af-146">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="665af-147">Anahtar kasasına gizli dizi ekleme</span><span class="sxs-lookup"><span data-stu-id="665af-147">Add a secret to key vault</span></span>

<span data-ttu-id="665af-148">Bunun nasıl çalıştığını göstermemize yardımcı olması için bir gizli dizi ekliyoruz.</span><span class="sxs-lookup"><span data-stu-id="665af-148">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="665af-149">Güvenle korumanız ama uygulamanıza da sağlamanız gereken bir SQL bağlantı dizesini veya başka bir bilgiyi depoluyor olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="665af-149">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="665af-150">Bu öğreticide, parola **AppSecret** olarak adlandırılır ve içinde **MySecret** değeri depolanır.</span><span class="sxs-lookup"><span data-stu-id="665af-150">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="665af-151">Anahtar Kasasında **MySecret** değerini depolayacak **AppSecret** adlı gizli dizi oluşturmak için aşağıdaki komutları yazın:</span><span class="sxs-lookup"><span data-stu-id="665af-151">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="665af-152">Gizli dizi içindeki değeri düz metin olarak görüntülemek için:</span><span class="sxs-lookup"><span data-stu-id="665af-152">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="665af-153">Bu komut, URI de dahil olmak üzere gizli bilgiyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="665af-153">This command shows the secret information including the URI.</span></span> <span data-ttu-id="665af-154">Bu adımları tamamladıktan sonra, Azure Key Vault'ta bu gizli dizinin URI'sine sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="665af-154">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="665af-155">Bu bilgileri bir yere yazın.</span><span class="sxs-lookup"><span data-stu-id="665af-155">Write this information down.</span></span> <span data-ttu-id="665af-156">Sonraki adımlardan birinde gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="665af-156">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="665af-157">Depoyu kopyalama</span><span class="sxs-lookup"><span data-stu-id="665af-157">Clone the Repo</span></span>

<span data-ttu-id="665af-158">Aşağıdaki komutu kullanarak kaynağı düzenleyebilmeniz için yerel kopyasını oluşturmak üzere depoyu kopyalayın:</span><span class="sxs-lookup"><span data-stu-id="665af-158">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a><span data-ttu-id="665af-159">Bağımlılıkları yükleme</span><span class="sxs-lookup"><span data-stu-id="665af-159">Install dependencies</span></span>

<span data-ttu-id="665af-160">Bu adımda bağımlılıkları yükleyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="665af-160">Here we install the dependencies.</span></span> <span data-ttu-id="665af-161">Aşağıdaki komutları çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="665af-161">Run the following commands:</span></span>

    cd key-vault-node-quickstart
    npm install

<span data-ttu-id="665af-162">Bu projede 2 düğüm modülü kullanılmaktadır:</span><span class="sxs-lookup"><span data-stu-id="665af-162">This project used 2 node modules:</span></span>

* [<span data-ttu-id="665af-163">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="665af-163">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="665af-164">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="665af-164">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="665af-165">Web uygulamasını Azure’da yayımlama</span><span class="sxs-lookup"><span data-stu-id="665af-165">Publish the web application to Azure</span></span>

<span data-ttu-id="665af-166">Uygulamayı Azure’da yayımlamak için tamamlamamız gereken birkaç adım, aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="665af-166">Below are the few steps we need to do to publish the application to Azure.</span></span>

* <span data-ttu-id="665af-167">1. adım, [Azure App Service](https://azure.microsoft.com/services/app-service/) Planı oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="665af-167">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="665af-168">Bu planda birden fazla web uygulaması depolayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="665af-168">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="665af-169">Sonraki adımda bir web uygulaması oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="665af-169">Next we create a web app.</span></span> <span data-ttu-id="665af-170">Aşağıdaki örnekte <app_name> kısmını genel olarak benzersiz bir uygulama adıyla değiştirin (geçerli karakterler a-z, 0-9 ve - şeklindedir).</span><span class="sxs-lookup"><span data-stu-id="665af-170">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="665af-171">Çalışma zamanı NODE|6.9 olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="665af-171">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="665af-172">Desteklenen tüm çalışma zamanlarını görmek için `az webapp list-runtimes` komutunu çalıştırın</span><span class="sxs-lookup"><span data-stu-id="665af-172">To see all supported runtimes, run `az webapp list-runtimes`</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="665af-173">Web uygulaması oluşturulduğunda Azure CLI aşağıda yer alan çıktıdaki gibi bilgiler gösterir:</span><span class="sxs-lookup"><span data-stu-id="665af-173">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

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
    <span data-ttu-id="665af-174">Yeni oluşturduğunuz web uygulamasına göz attığınızda çalışan bir web uygulaması görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="665af-174">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="665af-175"><app_name> değerini benzersiz bir uygulama adıyla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="665af-175">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="665af-176">Yukarıdaki komut ayrıca yerel git ortamınızdan Azure'a dağıtım yapmanızı sağlayan Git özellikli bir uygulama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="665af-176">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="665af-177">Yerel git, şu URL'ye sahiptir: 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span><span class="sxs-lookup"><span data-stu-id="665af-177">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="665af-178">Dağıtım kullanıcısı oluşturma Bir önceki komut tamamlandıktan sonra yerel Git deponuza bir Azure uzak bağlantı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="665af-178">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="665af-179"><url> yerine Uygulamanız için Git'i etkinleştirme adımında aldığınız Git uzak ortamının URL'sini yazın.</span><span class="sxs-lookup"><span data-stu-id="665af-179">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a><span data-ttu-id="665af-180">Çözümü açma ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="665af-180">Open and edit the solution</span></span>

<span data-ttu-id="665af-181">Belirlediğiniz anahtar kasanızın adıyla örneği çalıştırmak için program.cs dosyasını düzenleyin:</span><span class="sxs-lookup"><span data-stu-id="665af-181">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="665af-182">key-vault-dotnet-core-quickstart klasörüne gidin.</span><span class="sxs-lookup"><span data-stu-id="665af-182">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="665af-183">Visual Studio 2017'de key-vault-dotnet-core-quickstart.sln dosyasını açın.</span><span class="sxs-lookup"><span data-stu-id="665af-183">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="665af-184">Program.cs dosyasını açın ve *YourKeyVaultName* yer tutucusunu daha önce oluşturduğunuz anahtar kasanızın adıyla güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="665af-184">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="665af-185">Bu çözümde [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) ve [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet kitaplıkları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="665af-185">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="665af-186">Uygulamayı çalıştırma</span><span class="sxs-lookup"><span data-stu-id="665af-186">Run the app</span></span>

<span data-ttu-id="665af-187">Visual Studio 2017 ana menüsünde **Hata Ayıkla** > **Hata ayıklamadan başlat** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="665af-187">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="665af-188">Tarayıcı görüntülendiğinde **Hakkında** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="665af-188">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="665af-189">**AppSecret** değeri görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="665af-189">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="665af-190">Web uygulamasını Azure’da yayımlama</span><span class="sxs-lookup"><span data-stu-id="665af-190">Publish the web application to Azure</span></span>

<span data-ttu-id="665af-191">Canlı web uygulaması olarak görüntülemek için bu uygulamayı Azure'da yayımlayın ve gizli dizi değerini getirebildiğinizi görmek için:</span><span class="sxs-lookup"><span data-stu-id="665af-191">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="665af-192">Visual Studio'da **key-vault-dotnet-core-quickstart** projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="665af-192">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="665af-193">**Yayımla** > **Başlat** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="665af-193">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="665af-194">Yeni bir **App Service** oluşturun ve ardından **Yayımla** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="665af-194">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="665af-195">Uygulama adını **keyvaultdotnetcorequickstart** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="665af-195">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="665af-196">**Oluştur**’u seçin.</span><span class="sxs-lookup"><span data-stu-id="665af-196">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a><span data-ttu-id="665af-197">Yönetilen hizmet kimliklerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="665af-197">Enable managed service identities</span></span>

<span data-ttu-id="665af-198">Azure Key Vault kimlik bilgilerini ve diğer anahtarlarla gizli dizileri güvenle depolamak için bir yol sağlar, ama bunları alabilmek için kodunuzun Azure Key Vault'ta kimlik doğrulaması yapması gerekir.</span><span class="sxs-lookup"><span data-stu-id="665af-198">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="665af-199">Yönetilen Hizmet Kimliği, Azure Active Directory'de (Azure AD) Azure hizmetlerine otomatik olarak yönetilen bir kimlik vererek bu işlemi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="665af-199">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="665af-200">Bu kimliği kullanarak, Key Vault da dahil olmak üzere Azure AD kimlik doğrulamasını destekleyen tüm hizmetlerde kodunuzda kimlik bilgileri bulunmasına gerek kalmadan kimlik doğrulaması yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="665af-200">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="665af-201">Azure CLI'ye dönün.</span><span class="sxs-lookup"><span data-stu-id="665af-201">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="665af-202">Bu uygulamanın kimliğini oluşturmak için assign-identity komutunu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="665af-202">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="665af-203">Bu yordamdaki komut, portala gidip web uygulaması özelliklerinde **Yönetilen hizmet kimliğini** **Açık** duruma getirmekle eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="665af-203">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="665af-204">Key Vault gizli dizilerini okumak için uygulamanıza izin atama</span><span class="sxs-lookup"><span data-stu-id="665af-204">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="665af-205">Uygulamayı Azure'da yayımladığınızda çıktıyı not edin.</span><span class="sxs-lookup"><span data-stu-id="665af-205">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="665af-206">Şu biçimde olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="665af-206">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="665af-207">Ardından anahtar kasanızın adını ve **PrincipalId** değerini kullanarak şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="665af-207">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="665af-208">Node Uygulamasını Azure'a dağıtma ve gizli diziyi alma</span><span class="sxs-lookup"><span data-stu-id="665af-208">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="665af-209">Tüm ayarları yaptınız.</span><span class="sxs-lookup"><span data-stu-id="665af-209">Now that everything is set.</span></span> <span data-ttu-id="665af-210">Uygulamayı Azure'a dağıtmak için aşağıdaki komutu çalıştırın</span><span class="sxs-lookup"><span data-stu-id="665af-210">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="665af-211">Ardından https://<app_name>.azurewebsites.net adresine gittiğinizde gizli diziyi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="665af-211">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="665af-212"><YourKeyVaultName> adını kasanızın adı ile değiştirdiğinizden emin olun</span><span class="sxs-lookup"><span data-stu-id="665af-212">Make sure that you replaced the name <YourKeyVaultName> with your vault name</span></span>

::: zone-end

::: zone pivot="dotnet"
<span data-ttu-id="665af-213">Uygulamayı çalıştırdığınızda gizli dizi değerinizin alındığını görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="665af-213">Now when you run the application, you should see your secret value retrieved.</span></span>
::: zone-end

## <a name="next-steps"></a><span data-ttu-id="665af-214">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="665af-214">Next steps</span></span>

::: zone pivot="nodejs"
* [<span data-ttu-id="665af-215">Azure Key Vault Ana Sayfası</span><span class="sxs-lookup"><span data-stu-id="665af-215">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="665af-216">Azure Key Vault Belgeleri</span><span class="sxs-lookup"><span data-stu-id="665af-216">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="665af-217">Node için Azure SDK</span><span class="sxs-lookup"><span data-stu-id="665af-217">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [<span data-ttu-id="665af-218">Azure REST API Başvurusu</span><span class="sxs-lookup"><span data-stu-id="665af-218">Azure REST API Reference</span></span>](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end

::: zone pivot="dotnet"
* [<span data-ttu-id="665af-219">Azure Key Vault ana sayfası</span><span class="sxs-lookup"><span data-stu-id="665af-219">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="665af-220">Azure Key Vault belgeleri</span><span class="sxs-lookup"><span data-stu-id="665af-220">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="665af-221">.NET için Azure SDK</span><span class="sxs-lookup"><span data-stu-id="665af-221">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* [<span data-ttu-id="665af-222">Azure REST API başvurusu</span><span class="sxs-lookup"><span data-stu-id="665af-222">Azure REST API reference</span></span>](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end
