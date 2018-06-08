---
title: DotNet Aracı kaldırma komutu - .NET Core CLI
description: Dotnet Aracı kaldırma komutu belirtilen .NET Core genel aracı makinenizden kaldırır.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 5cf80d1756dbf4e88bb52a8028d186d44978f440
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34696948"
---
# <a name="dotnet-tool-uninstall"></a><span data-ttu-id="7f066-103">DotNet Aracı kaldırma</span><span class="sxs-lookup"><span data-stu-id="7f066-103">dotnet tool uninstall</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="7f066-104">Ad</span><span class="sxs-lookup"><span data-stu-id="7f066-104">Name</span></span>

<span data-ttu-id="7f066-105">`dotnet tool uninstall` -Kaldırır belirtilen [.NET Core genel aracı](global-tools.md) makinenizden.</span><span class="sxs-lookup"><span data-stu-id="7f066-105">`dotnet tool uninstall` - Uninstalls the specified [.NET Core Global Tool](global-tools.md) from your machine.</span></span>

## <a name="synopsis"></a><span data-ttu-id="7f066-106">Özet</span><span class="sxs-lookup"><span data-stu-id="7f066-106">Synopsis</span></span>

```
dotnet tool uninstall <PACKAGE_NAME> <-g|--global>
dotnet tool uninstall <PACKAGE_NAME> <--tool-path>
dotnet tool uninstall <-h|--help>
```

## <a name="description"></a><span data-ttu-id="7f066-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="7f066-107">Description</span></span>

<span data-ttu-id="7f066-108">`dotnet tool uninstall` Komutu, .NET Core genel araçları, makineden kaldırmak bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="7f066-108">The `dotnet tool uninstall` command provides a way for you to uninstall .NET Core Global Tools from your machine.</span></span> <span data-ttu-id="7f066-109">Komutunu kullanmak için ya da kullanıcı genelinde aracını kullanarak kaldırmak istediğinizi belirtmeniz gerekir `--global` seçeneği veya bir yol yeri belirtin aracı kullanılarak yüklenen `--tool-path` seçeneği.</span><span class="sxs-lookup"><span data-stu-id="7f066-109">To use the command, you either have to specify that you want to remove a user-wide tool using the `--global` option or specify a path to where the tool is installed using the `--tool-path` option.</span></span>

## <a name="arguments"></a><span data-ttu-id="7f066-110">Arguments</span><span class="sxs-lookup"><span data-stu-id="7f066-110">Arguments</span></span>

`PACKAGE_NAME`

<span data-ttu-id="7f066-111">.NET Core genel kaldırmak için Aracı'nı içeren NuGet paketi adı/kimliği.</span><span class="sxs-lookup"><span data-stu-id="7f066-111">Name/ID of the NuGet package that contains the .NET Core Global Tool to uninstall.</span></span> <span data-ttu-id="7f066-112">Paket adı kullanarak bulabilirsiniz [dotnet araç listesi](dotnet-tool-list.md) komutu.</span><span class="sxs-lookup"><span data-stu-id="7f066-112">You can find the package name using the [dotnet tool list](dotnet-tool-list.md) command.</span></span>

## <a name="options"></a><span data-ttu-id="7f066-113">Seçenekler</span><span class="sxs-lookup"><span data-stu-id="7f066-113">Options</span></span>

`-g|--global`

<span data-ttu-id="7f066-114">Kaldırılacak Aracı kullanıcı genelinde yüklemesinden olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f066-114">Specifies that the tool to be removed is from a user-wide installation.</span></span> <span data-ttu-id="7f066-115">Birleştirilemez `--tool-path` seçeneği.</span><span class="sxs-lookup"><span data-stu-id="7f066-115">Can't be combined with the `--tool-path` option.</span></span> <span data-ttu-id="7f066-116">Bu seçeneği belirtmezseniz, belirtmeniz gerekir `--tool-path` seçeneği.</span><span class="sxs-lookup"><span data-stu-id="7f066-116">If you don't specify this option, you must specify the `--tool-path` option.</span></span>

`-h|--help`

<span data-ttu-id="7f066-117">Komutu için kısa bir Yardım yazdırır.</span><span class="sxs-lookup"><span data-stu-id="7f066-117">Prints out a short help for the command.</span></span>

`--tool-path <PATH>`

<span data-ttu-id="7f066-118">Konumun genel Aracı'nı kaldırmak konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f066-118">Specifies the location where to uninstall the Global Tool.</span></span> <span data-ttu-id="7f066-119">YOL, mutlak veya göreli olabilir.</span><span class="sxs-lookup"><span data-stu-id="7f066-119">PATH can be absolute or relative.</span></span> <span data-ttu-id="7f066-120">Birleştirilemez `--global` seçeneği.</span><span class="sxs-lookup"><span data-stu-id="7f066-120">Can't be combined with the `--global` option.</span></span> <span data-ttu-id="7f066-121">Bu seçeneği belirtmezseniz, belirtmeniz gerekir `--global` seçeneği.</span><span class="sxs-lookup"><span data-stu-id="7f066-121">If you don't specify this option, you must specify the `--global` option.</span></span>

## <a name="examples"></a><span data-ttu-id="7f066-122">Örnekler</span><span class="sxs-lookup"><span data-stu-id="7f066-122">Examples</span></span>

<span data-ttu-id="7f066-123">Kaldırır [dotnetsay](https://www.nuget.org/packages/dotnetsay/) genel aracı:</span><span class="sxs-lookup"><span data-stu-id="7f066-123">Uninstalls the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool:</span></span>

`dotnet tool uninstall -g dotnetsay`

<span data-ttu-id="7f066-124">Kaldırır [dotnetsay](https://www.nuget.org/packages/dotnetsay/) belirli bir Windows klasörü genel aracından:</span><span class="sxs-lookup"><span data-stu-id="7f066-124">Uninstalls the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool from a specific Windows folder:</span></span>

`dotnet tool uninstall dotnetsay --tool-path c:\global-tools`

<span data-ttu-id="7f066-125">Kaldırır [dotnetsay](https://www.nuget.org/packages/dotnetsay/) belirli bir Linux/macOS klasörden genel aracı:</span><span class="sxs-lookup"><span data-stu-id="7f066-125">Uninstalls the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool from a specific Linux/macOS folder:</span></span>

`dotnet tool uninstall dotnetsay --tool-path ~/bin`

## <a name="see-also"></a><span data-ttu-id="7f066-126">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="7f066-126">See also</span></span>

[<span data-ttu-id="7f066-127">.NET core genel araçları</span><span class="sxs-lookup"><span data-stu-id="7f066-127">.NET Core Global Tools</span></span>](global-tools.md)