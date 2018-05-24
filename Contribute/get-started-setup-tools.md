---
title: İçerik yazma araçlarını yükleme
description: Bu makale, Git ve markdown dosyalarını düzenlemek için ihtiyacınız olacak istemci araçları indirip yüklemenize yardımcı olur.
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 04/30/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1011c3fc829202a3df134ddc80eb05b8959b7bf6
ms.sourcegitcommit: e046e7aad8ed22bffe5380d63a9d40f0baeecc57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2018
---
# <a name="install-content-authoring-tools"></a>İçerik yazma araçlarını yükleme

Bu makalede Git istemci araçlarını ve Visual Studio Code'u etkileşimli olarak yükleme adımları açıklanır.
> [!div class="checklist"]
> * [Windows için Git](https://git-scm.com/download/win)'i yükleme
> * [Visual Studio Code](https://code.visualstudio.com/)'u yükleme
> * [Docs Yazma Paketi](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)’ni yükleme

>[!IMPORTANT]
> Bir makalede yalnızca küçük değişiklikler yapıyorsanız bu makaledeki adımları tamamlamanız gerekli *değildir* ve doğrudan [hızlı değişiklikler iş akışı](index.md#quick-edits-to-existing-documents) kısmına gidebilirsiniz.
>
> Büyük katkılarda bulunanların bu adımı tamamlaması önerilir, bu adımdan sonra [büyük/uzun ömürlü değişiklikler iş akışı](how-to-write-workflows-major.md) kısmına geçebilirler. Ana depoda yazma izinleriniz olsa bile, önerdiğiniz değişiklikleri çatalınızda depolamak üzere okuma/yazma izinlerinizin olacağı *depo çatalını oluşturmanız ve kopyalamanız kesinlikle önerilir (ve bu makalede öyle yaptığınız varsayılır)*.

## <a name="install-git-client-tools-on-windows"></a>Windows'da Git istemci araçlarını yükleme

 [Software Freedom Conservancy’nin Git istemci araçlarının](https://git-scm.com/download/) son sürümünü yükleyin. Yükleme, Git sürüm denetim sistemini ve yerel Git deponuzla etkileşim için kullandığınız komut satırı uygulaması olan Git Bash'i içerir.

Komut satırı arabirimi (CLI) yerine bir grafik kullanıcı arabirimi (GUI) tercih ederseniz popüler seçenekler için [Software Freedom Conservancy’nin uygun GUI İstemcileri sayfası](https://git-scm.com/downloads/guis), [GitHub’ın GitHub Masaüstü](https://desktop.github.com/) veya [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)’a bakın.

Yükleme ve yapılandırma için seçtiğiniz istemcinin yönergelerini izleyin.

Sonraki makalede, [yerel Git deponuzu ayarlayacaksınız](get-started-setup-local.md).

   Ek Git kaynaklarını burada bulabilirsiniz: [Git terminolojisi](https://help.github.com/articles/github-glossary) | [Git temel bilgileri](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Git ve GitHub'ı öğrenme](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## <a name="understand-markdown-editors"></a>Markdown düzenleyicilerini anlama

Markdown, okuması ve öğrenmesi kolay bir biçimlendirme dilidir. Bu nedenle, bu dil kısa sürede endüstri standardı haline gelmiştir. Markdown’da makale yazmak için önce bir Markdown düzenleyicisi indirip yüklemenizi öneririz.  [Visual Studio Code](https://code.visualstudio.com/), Microsoft'ta Markdown'ı düzenlemek için tercih edilen dildir. Markdown'ı düzenlemeye yönelik bir diğer popüler araç da [Atom](https://atom.io)'dur.

Markdown metinleri, .md uzantılı dosyalara kaydedilir.

Markdown temel bilgileri ve OPS özel Markdown uzantıları tarafından desteklenen özellikler dahil olmak üzere Markdown ile makale yazmaya yönelik ilave ayrıntılar daha sonra [Markdown kullanımı](how-to-write-use-markdown.md) makalesinde ele alınacaktır.

## <a name="visual-studio-code"></a>Visual Studio Code

VS Code olarak da bilinen [Visual Studio Code](https://code.visualstudio.com/), Windows, Linux ve Mac üzerinde çalışan basit bir düzenleyicidir. Git tümleştirmesi ve uzantılar için destek içerir.

[VS Code](https://code.visualstudio.com/)'u indirin ve yükleyin. VS Code giriş sayfasında işletim sisteminiz doğru algılanmalıdır.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> VS Code'u başlatmak ve geçerli klasörü açmak için, komut satırında veya bash kabuğunda `code .` komutunu çalıştırın. Geçerli klasör yerel git deposunun bir parçasıysa, github tümleştirmesi Visual Studio Code'da otomatik olarak gösterilir.

## <a name="docs-authoring-pack"></a>Docs Yazma Paketi
Visual Studio Code için Docs Yazma Paketi’ni yükleyin. Bu uzantı kümesi, Markdown yazarken yardım için temel yazma desteği ve Markdown’ın docs.microsoft.com sitesinde nasıl görüneceğine bakmanız için önizleme özelliği sağlar.

   Bu [market sayfasını](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) ziyaret edin ve **Yükle**’yi seçin veya VS Code penceresindeki uzantılar listenizde `docsmsft.docs-authoring-pack` için arama yapın. 

   Docs Yazma Paketi’ne VS Code’da Alt+M tuşlarına basarak ulaşabilirsiniz. Araç çubuğu varsayılan olarak gizlidir ancak gösterilebilir. Bunun için VS Code ayarlarını düzenleyin (Control+virgül) ve `"markdown.showToolbar": true` kullanıcı ayarını ekleyin.

   Daha fazla bilgi için [Docs Yazma Paketi](how-to-write-docs-auth-pack.md) sayfasına bakın.


## <a name="next-steps"></a>Sonraki adımlar

Artık [yerel Git deposunu ayarlamaya](get-started-setup-local.md) hazırsınız.
