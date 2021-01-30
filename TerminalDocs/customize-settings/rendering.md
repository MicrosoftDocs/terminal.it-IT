---
title: Impostazioni per il rendering del terminale Windows
description: Informazioni su come personalizzare le impostazioni di rendering nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: b32ae538292b111bde5d8f6b218fb3eb55818587
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041967"
---
# <a name="rendering-settings-in-windows-terminal"></a><span data-ttu-id="6713f-103">Impostazioni di rendering nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="6713f-103">Rendering settings in Windows Terminal</span></span>

<span data-ttu-id="6713f-104">Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo.</span><span class="sxs-lookup"><span data-stu-id="6713f-104">The properties listed below affect the entire terminal window, regardless of the profile settings.</span></span> <span data-ttu-id="6713f-105">Queste proprietà devono essere inserite nella radice del file settings.json.</span><span class="sxs-lookup"><span data-stu-id="6713f-105">These should be placed at the root of your settings.json file.</span></span>

<span data-ttu-id="6713f-106">Per cambiare le impostazioni di rendering, vedere le informazioni aggiuntive disponibili nella [pagina sulla risoluzione dei problemi](./../troubleshooting.md#the-text-is-blurry) per assistenza.</span><span class="sxs-lookup"><span data-stu-id="6713f-106">If you are thinking about changing the rendering settings, additional information is provided on the [Troubleshooting page](./../troubleshooting.md#the-text-is-blurry) to help guide you.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6713f-107">L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="6713f-107">The settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="6713f-108">Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).</span><span class="sxs-lookup"><span data-stu-id="6713f-108">Detailed instructions on how to enable the settings UI can be found on the [Troubleshooting page](./../troubleshooting.md#open-the-settings-ui).</span></span>

## <a name="redraw-entire-screen-when-display-updates"></a><span data-ttu-id="6713f-109">Ricreare lo schermo intero durante la visualizzazione degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="6713f-109">Redraw entire screen when display updates</span></span>

<span data-ttu-id="6713f-110">Se questa proprietà è impostata su `true`, il terminale ridisegnerà ogni frame dello schermo.</span><span class="sxs-lookup"><span data-stu-id="6713f-110">When this set to `true`, the terminal will redraw the entire screen each frame.</span></span> <span data-ttu-id="6713f-111">Se è impostata su `false`, verrà eseguito solo il rendering degli aggiornamenti dello schermo tra frame.</span><span class="sxs-lookup"><span data-stu-id="6713f-111">When set to `false`, it will render only the updates to the screen between frames.</span></span>

<span data-ttu-id="6713f-112">**Nome della proprietà:** `experimental.rendering.forceFullRepaint`</span><span class="sxs-lookup"><span data-stu-id="6713f-112">**Property name:** `experimental.rendering.forceFullRepaint`</span></span>

<span data-ttu-id="6713f-113">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6713f-113">**Necessity:** Optional</span></span>

<span data-ttu-id="6713f-114">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="6713f-114">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="6713f-115">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="6713f-115">**Default value:** `false`</span></span>

<br />

___

## <a name="use-software-rendering"></a><span data-ttu-id="6713f-116">Usa rendering software</span><span class="sxs-lookup"><span data-stu-id="6713f-116">Use software rendering</span></span>

<span data-ttu-id="6713f-117">Se questa proprietà è impostata su `true`, il terminale userà il renderer software, ossia</span><span class="sxs-lookup"><span data-stu-id="6713f-117">When this is set to `true`, the terminal will use the software renderer (a.k.a.</span></span> <span data-ttu-id="6713f-118">WARP, invece di quello hardware.</span><span class="sxs-lookup"><span data-stu-id="6713f-118">WARP) instead of the hardware one.</span></span>

<span data-ttu-id="6713f-119">**Nome della proprietà:** `experimental.rendering.software`</span><span class="sxs-lookup"><span data-stu-id="6713f-119">**Property name:** `experimental.rendering.software`</span></span>

<span data-ttu-id="6713f-120">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6713f-120">**Necessity:** Optional</span></span>

<span data-ttu-id="6713f-121">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="6713f-121">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="6713f-122">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="6713f-122">**Default value:** `false`</span></span>
