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
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="77b16-103">Hızlı başlangıç: Azure Key Vault'tan gizli dizi ayarlama ve alma</span><span class="sxs-lookup"><span data-stu-id="77b16-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="77b16-104">Bu hızlı başlangıçta Anahtar Kasasında gizli dizi depolama ve bunu Web uygulaması kullanarak alma adımları gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="77b16-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="77b16-105">Gizli dizi değerini görmek için bunu Azure'da çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="77b16-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="77b16-106">Bu hızlı başlangıçta Node.js ve Yönetilen Hizmet Kimlikleri (MSI) kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="77b16-106">The quickstart uses Node.js and Managed service identities (MSIs)</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="77b16-107">Anahtar Kasası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="77b16-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="77b16-108">Anahtar Kasasında bir gizli dizi depolayın.</span><span class="sxs-lookup"><span data-stu-id="77b16-108">Store a secret in Key Vault.</span></span>
> * <span data-ttu-id="77b16-109">Anahtar Kasasındaki bir gizli diziyi alın.</span><span class="sxs-lookup"><span data-stu-id="77b16-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="77b16-110">Azure Web Uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="77b16-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="77b16-111">[Yönetilen hizmet kimliklerini etkinleştirin](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span><span class="sxs-lookup"><span data-stu-id="77b16-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="77b16-112">Web uygulamasının Anahtar Kasasından verileri okuması için gereken izinleri verin.</span><span class="sxs-lookup"><span data-stu-id="77b16-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="77b16-113">Devam etmeden önce [temel kavramlar](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts) hakkında bilgi sahibi olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="77b16-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

>[!NOTE]
<span data-ttu-id="77b16-114">Aşağıdaki öğreticinin neden en iyi yöntem olduğunu anlamak için bilmeniz gereken birkaç kavram vardır.</span><span class="sxs-lookup"><span data-stu-id="77b16-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="77b16-115">Key Vault, gizli dizilerin program aracılığıyla depolandığı merkezi bir depodur.</span><span class="sxs-lookup"><span data-stu-id="77b16-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="77b16-116">Bunu yapmak için uygulamaların/kullanıcıların gizli dizi sunarak Key Vault kimlik doğrulamasından geçmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="77b16-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="77b16-117">Güvenlikle ilgili en iyi yöntemlerin uygulanması için bu ilk gizli dizinin de düzenli olarak döndürülmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="77b16-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="77b16-118">Ancak [Yönetilen Hizmet Kimliği](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) sayesinde Azure'da çalışan uygulamalara Azure tarafından otomatik olarak yönetilen bir kimlik verilir.</span><span class="sxs-lookup"><span data-stu-id="77b16-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="77b16-119">Bu da **Gizli Dizi Belirleme Sorununu** çözerek kullanıcıların/uygulamaların en iyi yöntemleri uygulamasına ve ilk gizli diziyi döndürme konusunda endişelenmemesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="77b16-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="77b16-120">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="77b16-120">Prerequisites</span></span>

<span data-ttu-id="77b16-121">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="77b16-121">::: zone pivot="nodejs"</span></span>
* <span data-ttu-id="77b16-122">[Node JS](https://nodejs.org/en/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="77b16-122">[Node JS](https://nodejs.org/en/) ::: zone-end</span></span>

<span data-ttu-id="77b16-123">::: zone pivot="dotnet, windows"</span><span class="sxs-lookup"><span data-stu-id="77b16-123">::: zone pivot="dotnet, windows"</span></span>
* <span data-ttu-id="77b16-124">[Visual Studio 2017 sürüm 15.7.3 veya üzeri](https://www.microsoft.com/net/download/windows), aşağıdaki iş yükleriyle birlikte:</span><span class="sxs-lookup"><span data-stu-id="77b16-124">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="77b16-125">ASP.NET ve web geliştirme</span><span class="sxs-lookup"><span data-stu-id="77b16-125">ASP.NET and web development</span></span>
  * <span data-ttu-id="77b16-126">.NET Core çoklu platform geliştirme</span><span class="sxs-lookup"><span data-stu-id="77b16-126">.NET Core cross-platform development</span></span>
* <span data-ttu-id="77b16-127">[.NET Core 2.1 SDK veya üzeri](https://www.microsoft.com/net/download/windows) :::zone-end</span><span class="sxs-lookup"><span data-stu-id="77b16-127">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows) :::zone-end</span></span>

<span data-ttu-id="77b16-128">::: zone pivot="dotnet, mac"</span><span class="sxs-lookup"><span data-stu-id="77b16-128">::: zone pivot="dotnet, mac"</span></span>
* <span data-ttu-id="77b16-129">Bkz. [Mac için Visual Studio'daki Yenilikler](https://visualstudio.microsoft.com/vs/mac/).</span><span class="sxs-lookup"><span data-stu-id="77b16-129">See [What’s New in Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/).</span></span>
<span data-ttu-id="77b16-130">:::zone-end</span><span class="sxs-lookup"><span data-stu-id="77b16-130">:::zone-end</span></span>

* <span data-ttu-id="77b16-131">Git ([indir](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="77b16-131">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="77b16-132">Azure aboneliği.</span><span class="sxs-lookup"><span data-stu-id="77b16-132">An Azure subscription.</span></span> <span data-ttu-id="77b16-133">Azure aboneliğiniz yoksa başlamadan önce [ücretsiz bir hesap](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="77b16-133">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="77b16-134">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) 2.0.4 veya sonraki sürümü.</span><span class="sxs-lookup"><span data-stu-id="77b16-134">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="77b16-135">Bu uygulama Windows, Mac ve Linux’ta kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="77b16-135">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="77b16-136">Azure'da oturum açma</span><span class="sxs-lookup"><span data-stu-id="77b16-136">Login to Azure</span></span>

<span data-ttu-id="77b16-137">CLI kullanarak Azure'da oturum açmak için şunu yazabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="77b16-137">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="77b16-138">Kaynak grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="77b16-138">Create resource group</span></span>

<span data-ttu-id="77b16-139">[az group create](/cli/azure/group#az-group-create) komutuyla bir kaynak grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="77b16-139">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="77b16-140">Azure kaynak grubu, Azure kaynaklarının dağıtıldığı ve yönetildiği mantıksal bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="77b16-140">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="77b16-141">Lütfen bir Kaynak Grubu adı seçin ve yer tutucunun yerine yazın.</span><span class="sxs-lookup"><span data-stu-id="77b16-141">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="77b16-142">Aşağıdaki örnekte, *eastus* konumunda *<YourResourceGroupName>* adlı bir kaynak grubu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="77b16-142">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="77b16-143">Az önce oluşturduğunuz kaynak grubu bu öğretici boyunca kullanılır.</span><span class="sxs-lookup"><span data-stu-id="77b16-143">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="77b16-144">Azure Key Vault oluşturma</span><span class="sxs-lookup"><span data-stu-id="77b16-144">Create an Azure Key Vault</span></span>

<span data-ttu-id="77b16-145">Daha sonra, önceki adımda oluşturulan kaynak grubunda bir Anahtar Kasası oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="77b16-145">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="77b16-146">Bu makale boyunca Anahtar Kasası için “ContosoKeyVault” adı kullanılıyor olsa da, sizin benzersiz bir ad kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="77b16-146">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="77b16-147">Şu bilgileri belirtin:</span><span class="sxs-lookup"><span data-stu-id="77b16-147">Provide the following information:</span></span>

* <span data-ttu-id="77b16-148">Kasa adı: **Buradan bir Anahtar Kasası adı seçin**.</span><span class="sxs-lookup"><span data-stu-id="77b16-148">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="77b16-149">Kaynak grubu adı: **Buradan bir Kaynak Grubu Adı seçin**.</span><span class="sxs-lookup"><span data-stu-id="77b16-149">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="77b16-150">Konum: **Doğu ABD**.</span><span class="sxs-lookup"><span data-stu-id="77b16-150">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="77b16-151">Bu noktada Azure hesabınız, bu yeni anahtar kasasında herhangi bir işlemi gerçekleştirmeye yetkili olan tek hesaptır.</span><span class="sxs-lookup"><span data-stu-id="77b16-151">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="77b16-152">Anahtar kasasına gizli dizi ekleme</span><span class="sxs-lookup"><span data-stu-id="77b16-152">Add a secret to key vault</span></span>

<span data-ttu-id="77b16-153">Bunun nasıl çalıştığını göstermemize yardımcı olması için bir gizli dizi ekliyoruz.</span><span class="sxs-lookup"><span data-stu-id="77b16-153">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="77b16-154">Güvenle korumanız ama uygulamanıza da sağlamanız gereken bir SQL bağlantı dizesini veya başka bir bilgiyi depoluyor olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77b16-154">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="77b16-155">Bu öğreticide, parola **AppSecret** olarak adlandırılır ve içinde **MySecret** değeri depolanır.</span><span class="sxs-lookup"><span data-stu-id="77b16-155">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="77b16-156">Anahtar Kasasında **MySecret** değerini depolayacak **AppSecret** adlı gizli dizi oluşturmak için aşağıdaki komutları yazın:</span><span class="sxs-lookup"><span data-stu-id="77b16-156">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="77b16-157">Gizli dizi içindeki değeri düz metin olarak görüntülemek için:</span><span class="sxs-lookup"><span data-stu-id="77b16-157">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="77b16-158">Bu komut, URI de dahil olmak üzere gizli bilgiyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="77b16-158">This command shows the secret information including the URI.</span></span> <span data-ttu-id="77b16-159">Bu adımları tamamladıktan sonra, Azure Key Vault'ta bu gizli dizinin URI'sine sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="77b16-159">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="77b16-160">Bu bilgileri bir yere yazın.</span><span class="sxs-lookup"><span data-stu-id="77b16-160">Write this information down.</span></span> <span data-ttu-id="77b16-161">Sonraki adımlardan birinde gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="77b16-161">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="77b16-162">Depoyu kopyalama</span><span class="sxs-lookup"><span data-stu-id="77b16-162">Clone the Repo</span></span>

<span data-ttu-id="77b16-163">Aşağıdaki komutu kullanarak kaynağı düzenleyebilmeniz için yerel kopyasını oluşturmak üzere depoyu kopyalayın:</span><span class="sxs-lookup"><span data-stu-id="77b16-163">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

<span data-ttu-id="77b16-164">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="77b16-164">::: zone pivot="nodejs"</span></span>

## <a name="install-dependencies"></a><span data-ttu-id="77b16-165">Bağımlılıkları yükleme</span><span class="sxs-lookup"><span data-stu-id="77b16-165">Install dependencies</span></span>

<span data-ttu-id="77b16-166">Bu adımda bağımlılıkları yükleyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="77b16-166">Here we install the dependencies.</span></span> <span data-ttu-id="77b16-167">Şu komutları çalıştırın: cd key-vault-node-quickstart npm install</span><span class="sxs-lookup"><span data-stu-id="77b16-167">Run the following commands cd key-vault-node-quickstart npm install</span></span>

<span data-ttu-id="77b16-168">Bu projede 2 düğüm modülü kullanılmaktadır:</span><span class="sxs-lookup"><span data-stu-id="77b16-168">This project used 2 node modules:</span></span>

* [<span data-ttu-id="77b16-169">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="77b16-169">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="77b16-170">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="77b16-170">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="77b16-171">Web uygulamasını Azure’da yayımlama</span><span class="sxs-lookup"><span data-stu-id="77b16-171">Publish the web application to Azure</span></span>

<span data-ttu-id="77b16-172">Yapmanız gereken birkaç adım aşağıda gösterilmiştir</span><span class="sxs-lookup"><span data-stu-id="77b16-172">Below are the few steps we need to do</span></span>

* <span data-ttu-id="77b16-173">1. adım, [Azure App Service](https://azure.microsoft.com/services/app-service/) Planı oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="77b16-173">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="77b16-174">Bu planda birden fazla web uygulaması depolayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77b16-174">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="77b16-175">Sonraki adımda bir web uygulaması oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="77b16-175">Next we create a web app.</span></span> <span data-ttu-id="77b16-176">Aşağıdaki örnekte <app_name> kısmını genel olarak benzersiz bir uygulama adıyla değiştirin (geçerli karakterler a-z, 0-9 ve - şeklindedir).</span><span class="sxs-lookup"><span data-stu-id="77b16-176">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="77b16-177">Çalışma zamanı NODE|6.9 olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="77b16-177">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="77b16-178">Desteklenen tüm çalışma zamanlarını görmek için şu komutu çalıştırın: az webapp list-runtimes</span><span class="sxs-lookup"><span data-stu-id="77b16-178">To see all supported runtimes, run az webapp list-runtimes</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="77b16-179">Web uygulaması oluşturulduğunda Azure CLI aşağıda yer alan çıktıdaki gibi bilgiler gösterir:</span><span class="sxs-lookup"><span data-stu-id="77b16-179">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

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
    <span data-ttu-id="77b16-180">Yeni oluşturduğunuz web uygulamasına göz attığınızda çalışan bir web uygulaması görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="77b16-180">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="77b16-181"><app_name> değerini benzersiz bir uygulama adıyla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="77b16-181">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="77b16-182">Yukarıdaki komut ayrıca yerel git ortamınızdan Azure'a dağıtım yapmanızı sağlayan Git özellikli bir uygulama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77b16-182">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="77b16-183">Yerel git, şu URL'ye sahiptir: 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span><span class="sxs-lookup"><span data-stu-id="77b16-183">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="77b16-184">Dağıtım kullanıcısı oluşturma Bir önceki komut tamamlandıktan sonra yerel Git deponuza bir Azure uzak bağlantı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77b16-184">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="77b16-185"><url> yerine Uygulamanız için Git'i etkinleştirme adımında aldığınız Git uzak ortamının URL'sini yazın.</span><span class="sxs-lookup"><span data-stu-id="77b16-185">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
<span data-ttu-id="77b16-186">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="77b16-186">::: zone-end</span></span>

<span data-ttu-id="77b16-187">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="77b16-187">::: zone pivot="dotnet"</span></span>

## <a name="open-and-edit-the-solution"></a><span data-ttu-id="77b16-188">Çözümü açma ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="77b16-188">Open and edit the solution</span></span>

<span data-ttu-id="77b16-189">Belirlediğiniz anahtar kasanızın adıyla örneği çalıştırmak için program.cs dosyasını düzenleyin:</span><span class="sxs-lookup"><span data-stu-id="77b16-189">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="77b16-190">key-vault-dotnet-core-quickstart klasörüne gidin.</span><span class="sxs-lookup"><span data-stu-id="77b16-190">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="77b16-191">Visual Studio 2017'de key-vault-dotnet-core-quickstart.sln dosyasını açın.</span><span class="sxs-lookup"><span data-stu-id="77b16-191">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="77b16-192">Program.cs dosyasını açın ve *YourKeyVaultName* yer tutucusunu daha önce oluşturduğunuz anahtar kasanızın adıyla güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="77b16-192">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="77b16-193">Bu çözümde [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) ve [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet kitaplıkları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="77b16-193">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="77b16-194">Uygulamayı çalıştırma</span><span class="sxs-lookup"><span data-stu-id="77b16-194">Run the app</span></span>

<span data-ttu-id="77b16-195">Visual Studio 2017 ana menüsünde **Hata Ayıkla** > **Hata ayıklamadan başlat** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="77b16-195">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="77b16-196">Tarayıcı görüntülendiğinde **Hakkında** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="77b16-196">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="77b16-197">**AppSecret** değeri görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="77b16-197">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="77b16-198">Web uygulamasını Azure’da yayımlama</span><span class="sxs-lookup"><span data-stu-id="77b16-198">Publish the web application to Azure</span></span>

<span data-ttu-id="77b16-199">Canlı web uygulaması olarak görüntülemek için bu uygulamayı Azure'da yayımlayın ve gizli dizi değerini getirebildiğinizi görmek için:</span><span class="sxs-lookup"><span data-stu-id="77b16-199">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="77b16-200">Visual Studio'da **key-vault-dotnet-core-quickstart** projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="77b16-200">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="77b16-201">**Yayımla** > **Başlat** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="77b16-201">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="77b16-202">Yeni bir **App Service** oluşturun ve ardından **Yayımla** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="77b16-202">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="77b16-203">Uygulama adını **keyvaultdotnetcorequickstart** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="77b16-203">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="77b16-204">**Oluştur**’u seçin.</span><span class="sxs-lookup"><span data-stu-id="77b16-204">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]

<span data-ttu-id="77b16-205">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="77b16-205">::: zone-end</span></span>

## <a name="enable-managed-service-identities"></a><span data-ttu-id="77b16-206">Yönetilen hizmet kimliklerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="77b16-206">Enable managed service identities</span></span>

<span data-ttu-id="77b16-207">Azure Key Vault kimlik bilgilerini ve diğer anahtarlarla gizli dizileri güvenle depolamak için bir yol sağlar, ama bunları alabilmek için kodunuzun Azure Key Vault'ta kimlik doğrulaması yapması gerekir.</span><span class="sxs-lookup"><span data-stu-id="77b16-207">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="77b16-208">Yönetilen Hizmet Kimliği, Azure Active Directory'de (Azure AD) Azure hizmetlerine otomatik olarak yönetilen bir kimlik vererek bu işlemi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="77b16-208">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="77b16-209">Bu kimliği kullanarak, Key Vault da dahil olmak üzere Azure AD kimlik doğrulamasını destekleyen tüm hizmetlerde kodunuzda kimlik bilgileri bulunmasına gerek kalmadan kimlik doğrulaması yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77b16-209">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="77b16-210">Azure CLI'ye dönün.</span><span class="sxs-lookup"><span data-stu-id="77b16-210">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="77b16-211">Bu uygulamanın kimliğini oluşturmak için assign-identity komutunu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="77b16-211">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="77b16-212">Bu yordamdaki komut, portala gidip web uygulaması özelliklerinde **Yönetilen hizmet kimliğini** **Açık** duruma getirmekle eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="77b16-212">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="77b16-213">Key Vault gizli dizilerini okumak için uygulamanıza izin atama</span><span class="sxs-lookup"><span data-stu-id="77b16-213">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="77b16-214">Uygulamayı Azure'da yayımladığınızda çıktıyı not edin.</span><span class="sxs-lookup"><span data-stu-id="77b16-214">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="77b16-215">Şu biçimde olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="77b16-215">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="77b16-216">Ardından anahtar kasanızın adını ve **PrincipalId** değerini kullanarak şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="77b16-216">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

<span data-ttu-id="77b16-217">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="77b16-217">::: zone pivot="nodejs"</span></span>
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="77b16-218">Node Uygulamasını Azure'a dağıtma ve gizli diziyi alma</span><span class="sxs-lookup"><span data-stu-id="77b16-218">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="77b16-219">Tüm ayarları yaptınız.</span><span class="sxs-lookup"><span data-stu-id="77b16-219">Now that everything is set.</span></span> <span data-ttu-id="77b16-220">Uygulamayı Azure'a dağıtmak için aşağıdaki komutu çalıştırın</span><span class="sxs-lookup"><span data-stu-id="77b16-220">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="77b16-221">Ardından https://<app_name>.azurewebsites.net adresine gittiğinizde gizli diziyi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77b16-221">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="77b16-222"><YourKeyVaultName> yerine kasanızın adını yazdığınızdan emin olun ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="77b16-222">Make sure that you replaced the name <YourKeyVaultName> with your vault name ::: zone-end</span></span>

<span data-ttu-id="77b16-223">::: zone pivot="dotnet" Uygulamayı çalıştırdığınızda gizli dizi değerinizin alındığını görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="77b16-223">::: zone pivot="dotnet" Now when you run the application, you should see your secret value retrieved.</span></span>
<span data-ttu-id="77b16-224">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="77b16-224">::: zone-end</span></span>

## <a name="next-steps"></a><span data-ttu-id="77b16-225">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="77b16-225">Next steps</span></span>

<span data-ttu-id="77b16-226">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="77b16-226">::: zone pivot="nodejs"</span></span>
* [<span data-ttu-id="77b16-227">Azure Key Vault Ana Sayfası</span><span class="sxs-lookup"><span data-stu-id="77b16-227">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="77b16-228">Azure Key Vault Belgeleri</span><span class="sxs-lookup"><span data-stu-id="77b16-228">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="77b16-229">Node için Azure SDK</span><span class="sxs-lookup"><span data-stu-id="77b16-229">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* <span data-ttu-id="77b16-230">[Azure REST API Başvurusu](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="77b16-230">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>

<span data-ttu-id="77b16-231">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="77b16-231">::: zone pivot="dotnet"</span></span>
* [<span data-ttu-id="77b16-232">Azure Key Vault ana sayfası</span><span class="sxs-lookup"><span data-stu-id="77b16-232">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="77b16-233">Azure Key Vault belgeleri</span><span class="sxs-lookup"><span data-stu-id="77b16-233">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="77b16-234">.NET için Azure SDK</span><span class="sxs-lookup"><span data-stu-id="77b16-234">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* <span data-ttu-id="77b16-235">[Azure REST API başvurusu](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="77b16-235">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>