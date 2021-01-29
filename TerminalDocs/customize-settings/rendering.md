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
# <a name="rendering-settings-in-windows-terminal"></a>Impostazioni di rendering nel terminale di Windows

Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo. Queste proprietà devono essere inserite nella radice del file settings.json.

Per cambiare le impostazioni di rendering, vedere le informazioni aggiuntive disponibili nella [pagina sulla risoluzione dei problemi](./../troubleshooting.md#the-text-is-blurry) per assistenza.

> [!IMPORTANT]
> L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview). Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).

## <a name="redraw-entire-screen-when-display-updates"></a>Ricreare lo schermo intero durante la visualizzazione degli aggiornamenti

Se questa proprietà è impostata su `true`, il terminale ridisegnerà ogni frame dello schermo. Se è impostata su `false`, verrà eseguito solo il rendering degli aggiornamenti dello schermo tra frame.

**Nome della proprietà:** `experimental.rendering.forceFullRepaint`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

<br />

___

## <a name="use-software-rendering"></a>Usa rendering software

Se questa proprietà è impostata su `true`, il terminale userà il renderer software, ossia WARP, invece di quello hardware.

**Nome della proprietà:** `experimental.rendering.software`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`
