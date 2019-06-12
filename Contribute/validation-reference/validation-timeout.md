---
title: validation-timeout
description: Docs derleme sorunu validation-timeout için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 018634b1c5fba0848fb36a70d81c46be9acf2ecd
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67024222"
---
# <a name="validation-timeout"></a><span data-ttu-id="74bf7-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="74bf7-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="74bf7-104">Uyarı</span><span class="sxs-lookup"><span data-stu-id="74bf7-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="74bf7-105">Doğrulama hizmetinde bulunan hatalı durumdaki bir sunucu gibi geçici sorunlar Docs Derlemesinin hizmeti başarılı bir şekilde çağırmasını engelliyor.</span><span class="sxs-lookup"><span data-stu-id="74bf7-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="74bf7-106">Üç denemenin ardından çağrı zaman aşımına uğrar ve derleme gecikmelerini ve derleme işlem hattının tıka basa dolmasını engellemek için doğrulama işlemi iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="74bf7-106">After three tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="74bf7-107">Çözüm</span><span class="sxs-lookup"><span data-stu-id="74bf7-107">Resolution</span></span>

<span data-ttu-id="74bf7-108">PR’ınızı kapatıp yeniden açmayı deneyin veya bir derlemeyi el ile yeniden çalıştırmayı deneyin (yalnızca depo yöneticileri).</span><span class="sxs-lookup"><span data-stu-id="74bf7-108">Try closing and reopening your PR, or re-running a manual build (repo admins only).</span></span> <span data-ttu-id="74bf7-109">Sık karşılaşılan hizmet sorunları ilk yeniden denemenin ardından kendilerini temizler.</span><span class="sxs-lookup"><span data-stu-id="74bf7-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="74bf7-110">[https://SiteHelp](https://SiteHelp) üzerinden bir ileti almaya veya sorun bildirmeye devam ederseniz, Microsoft çalışanıysanız veya yardım için PR’ınızdaki bir makalenin yazarından @ bahsederseniz veya bir dış katkıda bulunansanız.</span><span class="sxs-lookup"><span data-stu-id="74bf7-110">If you continue to get the message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
