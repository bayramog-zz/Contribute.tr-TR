---
ms.date: 03/29/2019
ms.openlocfilehash: 4e07ecf777f1361e21343b7b80f59ad9c5e86b3e
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653425"
---
# <a name="tabbed-conceptual"></a><span data-ttu-id="13bf4-101">Sekmeli kavramsal</span><span class="sxs-lookup"><span data-stu-id="13bf4-101">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13bf4-102">Sekmeli kavramsal söz dizimi kullanım dışıdır ve yeni sekmeler eklenmemelidir.</span><span class="sxs-lookup"><span data-stu-id="13bf4-102">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="13bf4-103">Bu makalede açıklanan doğrulamalar, değişim işlevi kullanılabilir olana kadar sekmeli kavramsal söz dizimi kullanması onaylanan içerik kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="13bf4-103">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="13bf4-104">Sekme söz dizimi</span><span class="sxs-lookup"><span data-stu-id="13bf4-104">Tab syntax</span></span>

<span data-ttu-id="13bf4-105">Sekmeler için söz dizimi aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="13bf4-105">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="13bf4-106">Tek düzeyli sekme:</span><span class="sxs-lookup"><span data-stu-id="13bf4-106">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="13bf4-107">İsteğe bağlı bağımlı sekme:</span><span class="sxs-lookup"><span data-stu-id="13bf4-107">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="13bf4-108">İki sekmesi ve sekme grubu ayırıcısı (---) olan tek düzeyli sekme seçimi örneği:</span><span class="sxs-lookup"><span data-stu-id="13bf4-108">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="13bf4-109">Sekmeler isteğe bağlı olarak ikincil sekmeler veya bağımlılık sekmeleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="13bf4-109">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="13bf4-110">Böylece sekmeler, başka sekme kümelerindeki seçime bağımlı hale gelir.</span><span class="sxs-lookup"><span data-stu-id="13bf4-110">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="13bf4-111">Bunun bir örneği aşağıda verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="13bf4-111">Here's an example:</span></span>

```markdown
# [Azure CLI](#tab/azure-cli/linux)

Azure CLI content for Linux...

# [Azure CLI](#tab/azure-cli/windows)

Azure CLI content for Windows...

# [PowerShell](#tab/azure-powershell/linux)

PowerShell content for Linux...

# [PowerShell](#tab/azure-powershell/windows)

PowerShell content for Windows...

---
```

<span data-ttu-id="13bf4-112">Aşağıdaki doğrulamalar, sekme söz dizimi için geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="13bf4-112">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="13bf4-113">Sekme söz dizimi doğru olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="13bf4-113">Tab syntax must be correct.</span></span>
- <span data-ttu-id="13bf4-114">Bağımlı sekmeler, önceki sekme grubunda tanımlanmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="13bf4-114">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="13bf4-115">Yalnızca bir bağımlılık düzeyine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="13bf4-115">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="13bf4-116">İkiden az sekmeye izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="13bf4-116">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="13bf4-117">Dörtten fazla sekmeye izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="13bf4-117">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="13bf4-118">Sekmeler onaylanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="13bf4-118">Tabs must be approved.</span></span>
- <span data-ttu-id="13bf4-119">Sekme/Kimlik çiftleri geçerli olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="13bf4-119">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="13bf4-120">Bir sekme grubunda aynı sekme kimliği birden fazla kez kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="13bf4-120">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="approved-tabs"></a><span data-ttu-id="13bf4-121">Onaylanan sekmeler</span><span class="sxs-lookup"><span data-stu-id="13bf4-121">Approved tabs</span></span>

<span data-ttu-id="13bf4-122">Aşağıdaki sekme adı/sekme kimliği çiftleri onaylanır.</span><span class="sxs-lookup"><span data-stu-id="13bf4-122">The following tab name/tab ID pairs are approved.</span></span> <span data-ttu-id="13bf4-123">Bağımlı sekme kimlikleri, Sekme Kimliği sütunuyla eşleştirilmez ancak bu sütuna göre geçerli olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="13bf4-123">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="13bf4-124">Değerler büyük/küçük harfe duyarlıdır</span><span class="sxs-lookup"><span data-stu-id="13bf4-124">The values are case-sensitive</span></span>

|<span data-ttu-id="13bf4-125">Sekme adı</span><span class="sxs-lookup"><span data-stu-id="13bf4-125">Tab name</span></span>              |<span data-ttu-id="13bf4-126">Sekme kimliği</span><span class="sxs-lookup"><span data-stu-id="13bf4-126">Tab ID</span></span>            |
|----------------------|------------------|
|`[.NET]`              |`(#tab/dotnet)`   |
|`[.NET Core 1.x]`     |`(#tab/netcore1x)`|
|`[.NET Core 2.x]`     |`(#tab/netcore2x)`|
|`[.NET Core 2.0]`     |`(#tab/netcore20)`|
|`[.NET Core 2.1]`     |`(#tab/netcore21)`|
|`[.NET Core 2.2]`     |`(#tab/netcore22)`|
|`[.NET Core 3.x]`     |`(#tab/netcore3x)`|
|`[.NET Core 3.0]`     |`(#tab/netcore30)`|
|`[.NET Core CLI]`     |`(#tab/netcore-cli)`|
|`[Azure CLI]`         |`(#tab/azure-cli)`|
|`[Android]`           |`(#tab/android)`  |
|`[Browser]`           |`(#tab/browser)`  |
|`[C#]`                |`(#tab/csharp)`   |
|`[C# Script]`         |`(#tab/csharp-script)`|
|`[CentOS]`            |`(#tab/centos)`|
|`[Command Line]`      |`(#tab/command-line)`|
|`[Debian]`            |`(#tab/debian)`|
|`[Docker Hub]`        |`(#tab/docker-hub)`|
|`[F#]`                |`(#tab/fsharp)`|
|`[Fedora]`            |`(#tab/fedora)`|
|`[iOS]`               |`(#tab/ios)`      |
|`[Java]`              |`(#tab/java)`|
|`[JavaScript]`        |`(#tab/javascript)`|
|`[Linux]`             |`(#tab/linux)`    |
|`[macOS]`             |`(#tab/macos)`    |
|`[Managed Kubernetes]`|`(#tab/kubernetes-managed)`|
|`[Maven]`             |`(#tab/maven)`|
|`[Mint]`              |`(#tab/mint)`|
|`[Node.js]`           |`(#tab/nodejs)`|
|`[npm]`               |`(#tab/npm)` |
|`[NuGet]`             |`(#tab/nuget)`|
|`[openSUSE]`          |`(#tab/opensuse)`|
|`[Other]`             |`(#tab/other)` |
|`[Oracle Linux]`      |`(#tab/oracle-linux)`|
|`[Package Manager]`   |`(#tab/package-manager)` |
|`[PEAR]`              |`(#tab/pear)`|
|`[pip]`               |`(#tab/pip)`|
|`[Portal]`            |`(#tab/azure-portal)`    |
|`[PowerShell]`        |`(#tab/azure-powershell)`|
|`[Private Registry]`  |`(#tab/private-registry)`|
|`[Python]`            |`(#tab/python)`|
|`[Resource Manager Template]`|`(#tab/azure-resource-manager)`|
|`[RHEL]`              |`(#tab/rhel)`|
|`[RubyGems]`          |`(#tab/rubygems)`|
|`[SQL Server]`        |`(#tab/sql-server)`|
|`[SQLite]`            |`(#tab/sqlite)`|
|`[TypeScript]`        |`(#tab/typescript)`|
|`[Visual Basic]`      |`(#tab/vb)` |
|`[Visual Studio]`     |`(#tab/visual-studio)`|
|`[Visual Studio 15.6 and earlier]`|`(#tab/vs156)`|
|`[Visual Studio 15.7 and later]`  |`(#tab/vs157)`|
|`[Visual Studio Code]`            |`(#tab/visual-studio-code)`|
|`[Visual Studio for Mac]`         |`(#tab/visual-studio-mac)`|
|`[Ubuntu]`                        |`(#tab/ubuntu)`|
|`[Unmanaged Kubernetes]`          |`(#tab/kubernetes-unmanaged)`|
|`[Windows]`   |`(#tab/windows)`   |