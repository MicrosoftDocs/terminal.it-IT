---
title: Cascadia Code in Terminale Windows
description: Informazioni sui diversi tipi di carattere Cascadia Code e sul relativo funzionamento con Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: overview
ms.service: terminal
ms.openlocfilehash: e9af1ea8445514534c64410fe494d35186d028b5
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415856"
---
# <a name="cascadia-code"></a><span data-ttu-id="8ea14-103">Cascadia Code</span><span class="sxs-lookup"><span data-stu-id="8ea14-103">Cascadia Code</span></span>

<span data-ttu-id="8ea14-104">Cascadia Code è un nuovo tipo di carattere Microsoft con spaziatura fissa che offre una nuova esperienza con le applicazioni da riga di comando e gli editor di testo.</span><span class="sxs-lookup"><span data-stu-id="8ea14-104">Cascadia Code is a new monospaced font from Microsoft that provides a fresh experience for command line applications and text editors.</span></span> <span data-ttu-id="8ea14-105">Cascadia Code è stato sviluppato insieme a Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="8ea14-105">Cascadia Code was developed alongside Windows Terminal.</span></span> <span data-ttu-id="8ea14-106">L'uso di questo tipo di carattere è particolarmente consigliato con applicazioni di terminale e editor di testo come Visual Studio e Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="8ea14-106">This font is most recommended to be used with terminal applications and text editors such as Visual Studio and Visual Studio Code.</span></span>

## <a name="cascadia-code-versions"></a><span data-ttu-id="8ea14-107">Versioni di Cascadia Code</span><span class="sxs-lookup"><span data-stu-id="8ea14-107">Cascadia Code versions</span></span>

<span data-ttu-id="8ea14-108">Sono disponibili più versioni di Cascadia Code che includono legature e glifi.</span><span class="sxs-lookup"><span data-stu-id="8ea14-108">There are multiple versions of Cascadia Code available that include ligatures and glyphs.</span></span> <span data-ttu-id="8ea14-109">Tutte le versioni di Cascadia Code possono essere scaricate dalla [pagina di versioni di Cascadia Code in GitHub](https://github.com/microsoft/cascadia-code/releases).</span><span class="sxs-lookup"><span data-stu-id="8ea14-109">All versions of Cascadia Code can be downloaded from the [Cascadia Code GitHub releases page](https://github.com/microsoft/cascadia-code/releases).</span></span> <span data-ttu-id="8ea14-110">Il pacchetto di Terminale Windows include Cascadia Code e Cascadia Mono, quest'ultimo usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8ea14-110">Windows Terminal ships Cascadia Code and Cascadia Mono in its package and uses Cascadia Mono by default.</span></span>

| <span data-ttu-id="8ea14-111">Nome del tipo carattere</span><span class="sxs-lookup"><span data-stu-id="8ea14-111">Font Name</span></span> | <span data-ttu-id="8ea14-112">Include legature</span><span class="sxs-lookup"><span data-stu-id="8ea14-112">Includes Ligatures</span></span> | <span data-ttu-id="8ea14-113">Include glifi di Powerline</span><span class="sxs-lookup"><span data-stu-id="8ea14-113">Includes Powerline Glyphs</span></span> |
| --------- | ------------------ | ------------------------- |
| <span data-ttu-id="8ea14-114">Cascadia Code</span><span class="sxs-lookup"><span data-stu-id="8ea14-114">Cascadia Code</span></span> | <span data-ttu-id="8ea14-115">Sì</span><span class="sxs-lookup"><span data-stu-id="8ea14-115">Yes</span></span> | <span data-ttu-id="8ea14-116">No</span><span class="sxs-lookup"><span data-stu-id="8ea14-116">No</span></span> |
| <span data-ttu-id="8ea14-117">Cascadia Mono</span><span class="sxs-lookup"><span data-stu-id="8ea14-117">Cascadia Mono</span></span> | <span data-ttu-id="8ea14-118">No</span><span class="sxs-lookup"><span data-stu-id="8ea14-118">No</span></span>  | <span data-ttu-id="8ea14-119">No</span><span class="sxs-lookup"><span data-stu-id="8ea14-119">No</span></span> |
| <span data-ttu-id="8ea14-120">Cascadia Code PL</span><span class="sxs-lookup"><span data-stu-id="8ea14-120">Cascadia Code PL</span></span> | <span data-ttu-id="8ea14-121">Sì</span><span class="sxs-lookup"><span data-stu-id="8ea14-121">Yes</span></span> | <span data-ttu-id="8ea14-122">Sì</span><span class="sxs-lookup"><span data-stu-id="8ea14-122">Yes</span></span> |
| <span data-ttu-id="8ea14-123">Cascadia Mono PL</span><span class="sxs-lookup"><span data-stu-id="8ea14-123">Cascadia Mono PL</span></span> | <span data-ttu-id="8ea14-124">No</span><span class="sxs-lookup"><span data-stu-id="8ea14-124">No</span></span> | <span data-ttu-id="8ea14-125">Sì</span><span class="sxs-lookup"><span data-stu-id="8ea14-125">Yes</span></span> |

## <a name="powerline-and-programming-ligatures"></a><span data-ttu-id="8ea14-126">Legature di Powerline di programmazione</span><span class="sxs-lookup"><span data-stu-id="8ea14-126">Powerline and programming ligatures</span></span>

<span data-ttu-id="8ea14-127">Powerline è un plug-in comune della riga di comando che ti consente di visualizzare altre informazioni nel prompt.</span><span class="sxs-lookup"><span data-stu-id="8ea14-127">Powerline is a common command line plugin that allows you to display additional information in your prompt.</span></span> <span data-ttu-id="8ea14-128">Per la corretta visualizzazione di queste informazioni, usa alcuni glifi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="8ea14-128">It uses a few additional glyphs to display this information properly.</span></span> <span data-ttu-id="8ea14-129">Per altre informazioni sulla configurazione di Powerline nel prompt dei comandi, vedi la pagina [Powerline in Terminale Windows](./tutorials/powerline-setup.md).</span><span class="sxs-lookup"><span data-stu-id="8ea14-129">To learn more about setting up Powerline in your command prompt, visit the [Powerline in Windows Terminal](./tutorials/powerline-setup.md) page.</span></span>

<span data-ttu-id="8ea14-130">Le legature di programmazione sono glifi creati combinando caratteri.</span><span class="sxs-lookup"><span data-stu-id="8ea14-130">Programming ligatures are glyphs that are created by combining characters.</span></span> <span data-ttu-id="8ea14-131">Sono particolarmente utili per la scrittura di codice.</span><span class="sxs-lookup"><span data-stu-id="8ea14-131">They are must useful when writing code.</span></span> <span data-ttu-id="8ea14-132">Le varianti "Code" includono legature, mentre le varianti "Mono" no.</span><span class="sxs-lookup"><span data-stu-id="8ea14-132">The "Code" variants include ligatures, whereas the "Mono" variants exclude them.</span></span>

![Legature di programmazione di Cascadia Code](./images/programming-ligatures.gif)

## <a name="contributing-to-cascadia-code"></a><span data-ttu-id="8ea14-134">Aggiunta di contributi a Cascadia Code</span><span class="sxs-lookup"><span data-stu-id="8ea14-134">Contributing to Cascadia Code</span></span>

<span data-ttu-id="8ea14-135">Cascadia Code è concesso in licenza [SIL Open Font](https://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL) in [GitHub](https://github.com/microsoft/cascadia-code).</span><span class="sxs-lookup"><span data-stu-id="8ea14-135">Cascadia Code is licensed under the [SIL Open Font license](https://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL) on [GitHub](https://github.com/microsoft/cascadia-code).</span></span>