---
title: validation-timeout
description: Docs derleme sorunu validation-timeout için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 00461768491c25b9bafaff6b117a356d9e291e22
ms.sourcegitcommit: 412ce4ab23e758d41947043f1463e96595ba3bfe
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67033305"
---
# <a name="validation-timeout"></a><span data-ttu-id="d1b66-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="d1b66-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="d1b66-104">Uyarı</span><span class="sxs-lookup"><span data-stu-id="d1b66-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or  If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="d1b66-105">Doğrulama hizmetinde bulunan hatalı durumdaki bir sunucu gibi geçici sorunlar Docs Derlemesinin hizmeti başarılı bir şekilde çağırmasını engelliyor.</span><span class="sxs-lookup"><span data-stu-id="d1b66-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="d1b66-106">Birkaç denemenin ardından çağrı zaman aşımına uğrar ve derleme gecikmeleri ile derleme işlem hattının tıka basa dolmasını engellemek için doğrulama işlemi iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="d1b66-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="d1b66-107">Çözüm</span><span class="sxs-lookup"><span data-stu-id="d1b66-107">Resolution</span></span>

<span data-ttu-id="d1b66-108">PR’ınızı kapatıp yeniden açmayı deneyin veya Docs Portal’dan bir derlemeyi el ile yeniden çalıştırmayı deneyin (yalnızca depo yöneticileri).</span><span class="sxs-lookup"><span data-stu-id="d1b66-108">Try closing and re-opening your PR, or re-running a manual build via Docs Portal (repo admins only).</span></span> <span data-ttu-id="d1b66-109">Sık karşılaşılan hizmet sorunları ilk yeniden denemenin ardından kendilerini temizler.</span><span class="sxs-lookup"><span data-stu-id="d1b66-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="d1b66-110">Bir yöneticinin yardımına ihtiyaç duyarsanız, [https://SiteHelp](https://SiteHelp) üzerinden bir ileti almaya veya sorun bildirmeye devam ederseniz, Microsoft çalışanıysanız veya yardım için PR’ınızdaki bir makalenin yazarından @ bahsederseniz veya bir dış katkıda bulunansanız.</span><span class="sxs-lookup"><span data-stu-id="d1b66-110">If you need help from an admin or if you continue to get this message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
