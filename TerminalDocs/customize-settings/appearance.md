---
title: Impostazioni aspetto terminale Windows
description: Informazioni su come personalizzare le impostazioni di aspetto nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 0393cecf59a9b0dd1dce4aecf7fe11df1b5a4a63
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041978"
---
# <a name="appearance-settings-in-windows-terminal"></a>Impostazioni aspetto nel terminale Windows

Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo. Queste proprietà devono essere inserite nella radice del file settings.json.

> [!IMPORTANT]
> L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview). Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).

## <a name="theme"></a>Tema

:::row:::
:::column span="":::
Consente di impostare il tema dell'applicazione. Con `"system"` viene usato lo stesso tema di Windows.

**Nome della proprietà:** `theme`

**Obbligatoria:** Facoltativo

**Accetta:** `"system"`, `"dark"`, `"light"`

**Valore predefinito:** `"system"`

:::column-end:::
:::column span="":::
![Terminale Windows - Tema scuro](./../images/requested-themes.gif)
_Configurazione: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_

:::column-end:::
:::row-end:::

<br />

___

## <a name="always-show-tabs"></a>Mostra sempre le schede

:::row:::
:::column span="":::
Quando è impostata su `true`, le schede vengono sempre visualizzate. Quando è impostata su `false` e `showTabsInTitlebar` è impostata su `true`, le schede vengono sempre visualizzate sotto la barra del titolo. Quando è impostata su `false` e `showTabsInTitlebar` è impostata su `false`, le schede vengono visualizzate solo se sono presenti più schede digitando <kbd>ctrl+shift+t</kbd> oppure digitando il tasto di scelta rapida assegnato a `newTab`. La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.

**Nome della proprietà:** `alwaysShowTabs`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

:::column-end:::
:::column span="":::
![Terminale Windows - Visualizza sempre le schede](./../images/always-show-tabs.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="hide-the-title-bar"></a>Nascondi la barra del titolo

:::row:::
:::column span="":::
Quando è impostata su `true`, le schede vengono spostate nella barra del titolo e la barra del titolo scompare. Quando è impostata su `false`, la barra del titolo si trova sopra le schede. La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.

**Nome della proprietà:** `showTabsInTitlebar`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

:::column-end:::
:::column span="":::
![Terminale Windows - Mostra le schede nella barra del titolo](./../images/show-tabs-in-title-bar.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="use-active-terminal-title-as-application-title"></a>USA titolo del terminale attivo come titolo dell'applicazione

Quando è impostata su `true`, la barra del titolo visualizza il titolo della scheda selezionata. Quando è impostata su `false`, la barra del titolo visualizza "Terminale Windows". La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.

**Nome della proprietà:** `showTerminalTitleInTitlebar`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

<br />

___

## <a name="always-on-top-mode"></a>Modalità sempre in primo piano

Quando è impostato su true, Windows Terminal viene avviato in tutte le altre finestre sul desktop. Questo stato può anche essere attivato o disattivato con l' `toggleAlwaysOnTop` associazione di tasti.

**Nome della proprietà:** `alwaysOnTop`

**Obbligatoria:** Facoltativo

**Accetta:**`true, false`

**Valore predefinito:** `false`

<br />

___

## <a name="tab-width-mode"></a>Modalità larghezza schede

:::row:::
:::column span="":::
Consente di impostare la larghezza delle schede. Con `"equal"` tutte le schede hanno la stessa larghezza. Con `"titleLength"` ogni scheda viene adattata alla lunghezza del titolo. `"compact"` comprime tutte le schede inattive fino alla larghezza dell'icona, lasciando alla scheda attiva più spazio per visualizzare il titolo completo.

**Nome della proprietà:** `tabWidthMode`

**Obbligatoria:** Facoltativo

**Accetta:** `"equal"`, `"titleLength"`, `"compact"`

**Valore predefinito:** `"equal"`

:::column-end:::
:::column span="":::
![Terminale Windows - Modalità larghezza schede](./../images/tab-width-mode.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="disable-pane-animations"></a>Disabilita animazioni del riquadro

In questo modo vengono disabilitate le animazioni visive nell'applicazione quando è impostato su `true` .

**Nome della proprietà:** `disableAnimations`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

<br />

___

## <a name="show-close-all-tabs-popup"></a>Mostra finestra di chiusura di tutte le schede popup

:::row:::
:::column span="":::
Quando è impostata su `true`, alla chiusura di una finestra con più schede aperte _verrà_ richiesta una conferma. Quando è impostata su `false`, alla chiusura di una finestra con più schede aperte _non verrà_ richiesta alcuna conferma.

**Nome della proprietà:** `confirmCloseAllTabs`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

:::column-end:::
:::column span="":::
![Terminale Windows - Conferma chiusura di tutte le schede](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::
