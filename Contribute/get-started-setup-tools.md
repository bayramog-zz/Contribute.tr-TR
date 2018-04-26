---
title: İçerik yazma araçlarını yükleme
description: Bu makale, Git ve markdown dosyalarını düzenlemek için ihtiyacınız olacak istemci araçları indirip yüklemenize yardımcı olur.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 62c4b234f23b470ffea33cacdfc469fbd7e526bd
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2018
---
# <a name="install-content-authoring-tools"></a>İçerik yazma araçlarını yükleme

Bu makalede Git istemci araçlarını ve Visual Studio Code'u etkileşimli olarak yükleme adımları açıklanır.
> [!div class="checklist"]
> * [Windows için Git](https://git-scm.com/download/win)'i yükleme
> * [Visual Studio Code](https://code.visualstudio.com/)'u yükleme

>[!IMPORTANT]
> Bir makalede yalnızca küçük değişiklikler yapıyorsanız bu makaledeki adımları tamamlamanız gerekli *değildir* ve doğrudan [küçük/seyrek görülen değişiklikler iş akışı](light-workflow.md) kısmına gidebilirsiniz.
>
> Büyük katkılarda bulunanların bu adımı tamamlaması önerilir, bu adımdan sonra [büyük/uzun ömürlü değişiklikler iş akışı](full-workflow.md) kısmına geçebilirler. Ana depoda yazma izinleriniz olsa bile, önerdiğiniz değişiklikleri çatalınızda depolamak üzere okuma/yazma izinlerinizin olacağı *depo çatalını oluşturmanız ve kopyalamanız kesinlikle önerilir (ve bu makalede öyle yaptığınız varsayılır)*.

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

## <a name="next-steps"></a>Sonraki adımlar

Artık [yerel Git deposunu ayarlamaya](get-started-setup-local.md) hazırsınız.
