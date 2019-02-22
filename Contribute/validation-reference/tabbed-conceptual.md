# <a name="tabbed-conceptual"></a>Sekmeli kavramsal

> [!IMPORTANT]
> Sekmeli kavramsal söz dizimi kullanım dışıdır ve yeni sekmeler eklenmemelidir. Bu makalede açıklanan doğrulamalar, değişim işlevi kullanılabilir olana kadar sekmeli kavramsal söz dizimi kullanması onaylanan içerik kümeleri için geçerlidir.

## <a name="tab-syntax"></a>Sekme söz dizimi

Sekmeler için söz dizimi aşağıdaki gibidir:

Tek düzeyli sekme:

`# [Tab Display Name](#tab/tab-id)`

İsteğe bağlı bağımlı sekme:

`# [Tab Display Name](#tab/tab-id/tab-condition)`

İki sekmesi ve sekme grubu ayırıcısı (---) olan tek düzeyli sekme seçimi örneği:

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

Sekmeler isteğe bağlı olarak ikincil sekmeler veya bağımlılık sekmeleri içerebilir. Böylece sekmeler, başka sekme kümelerindeki seçime bağımlı hale gelir. Bunun bir örneği aşağıda verilmiştir:

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

Aşağıdaki doğrulamalar, sekme söz dizimi için geçerlidir:

- Sekme söz dizimi doğru olmalıdır.
- Bağımlı sekmeler, önceki sekme grubunda tanımlanmış olmalıdır.
- Yalnızca bir bağımlılık düzeyine izin verilir.
- İkiden az sekmeye izin verilmez.
- Dörtten fazla sekmeye izin verilmez.
- Sekmeler güvenilir listeye alınmalıdır.
- Sekme/Kimlik çiftleri geçerli olmalıdır.
- Bir sekme grubunda aynı sekme kimliği birden fazla kez kullanılamaz.

## <a name="tab-whitelist"></a>Güvenilir sekme listesi

Aşağıdaki sekme adı/sekme kimliği çiftleri güvenilir listeye alınmıştır. Bağımlı sekme kimlikleri, Sekme Kimliği sütunuyla eşleştirilmez ancak bu sütuna göre geçerli olmalıdır. Değerler büyük/küçük harfe duyarlıdır

|Sekme adı              |Sekme kimliği            |
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