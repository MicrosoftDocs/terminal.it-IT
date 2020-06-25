---
title: Terminale Windows - Impostazioni globali
description: Informazioni su come personalizzare le impostazioni globali in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 06/18/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: ba3197bb8b9466d37c01432b60314a7a00227898
ms.sourcegitcommit: 91a802863cd0730d2e364377ffe44f819a66ff2a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2020
ms.locfileid: "84994310"
---
# <a name="global-settings-in-windows-terminal"></a>Impostazioni globali di Terminale Windows

Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo. Queste proprietà devono essere inserite nella radice del file settings.json.

## <a name="default-profile"></a>Profilo predefinito

Imposta il profilo predefinito che viene aperto quando si digita <kbd>ctrl+shift+t</kbd>, si digita il tasto di scelta rapida assegnato a `newTab`, si esegue `wt new-tab` senza specificare un profilo o si fa clic sull'icona '+'.

**Nome della proprietà:** `defaultProfile`

**Obbligatoria:** Obbligatoria

**Accetta:** GUID o nome del profilo in formato stringa

**Valore predefinito:** GUID di PowerShell

> [!IMPORTANT]
> L'uso del nome del profilo per `defaultProfile` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).

<br />

___

## <a name="disable-dynamic-profiles"></a>Disabilita i profili dinamici

Consente di impostare i generatori di profili dinamici da disabilitare, per evitare che aggiungano profili all'elenco di profili all'avvio. Per informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).

**Nome della proprietà:** `disabledProfileSources`

**Obbligatoria:** Facoltativo

**Accetta:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"` e/o `"Windows.Terminal.PowershellCore"` all'interno di una matrice

**Valore predefinito:** `[]`

<br />

___

## <a name="darklight-theme"></a>Tema chiaro/scuro

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

## <a name="tab-settings"></a>Impostazioni per le schede

### <a name="always-show-tabs"></a>Mostra sempre le schede

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

### <a name="tab-width-mode"></a>Modalità larghezza schede

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

> [!IMPORTANT]
> L'impostazione `"compact"` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).

### <a name="hide-close-all-tabs-popup"></a>Nascondi il popup di chiusura di tutte le schede

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

<br />

___

## <a name="launch-settings"></a>Impostazioni per l'avvio

### <a name="launch-on-startup-preview"></a>Avvio all'avvio del sistema ([anteprima](https://aka.ms/terminal-preview/))

Se questa proprietà è impostata su `true`, abilita l'avvio di Terminale Windows all'avvio del sistema. L'impostazione su `false` disabiliterà la voce dell'attività di avvio del sistema. Nota: se la voce dell'attività di avvio del sistema di Terminale Windows viene disabilitata da criteri dell'organizzazione o da un'azione dell'utente, questa impostazione non avrà effetto.

**Nome della proprietà:** `startOnUserLogin`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

> [!IMPORTANT]
> Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).

### <a name="launch-size"></a>Dimensioni all'avvio

Definisce se il terminale verrà avviato con dimensioni ingrandite, a schermo intero o in una finestra.

**Nome della proprietà:** `launchMode`

**Obbligatoria:** Facoltativo

**Accetta:** `"default"`, `"maximized"`, `"fullscreen"`

**Valore predefinito:** `"default"`

> [!IMPORTANT]
> L'impostazione `"fullscreen"` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).

### <a name="launch-position"></a>Posizione di avvio

Consente di impostare la posizione in pixel dell'angolo superiore sinistro della finestra al primo caricamento. In un sistema con più schermi queste coordinate si riferiscono all'angolo superiore sinistro dello schermo principale. Se non viene specificata una coordinata X o Y, il terminale userà l'impostazione predefinita del sistema per tale valore. Se `launchMode` è impostata su `"maximized"`, la finestra aperta a schermo intero nel monitor specificato da tali coordinate.

**Nome della proprietà:** `initialPosition`

**Obbligatoria:** Facoltativo

**Accetta:** coordinate nei formati stringa seguenti: `","`, `"#,#"`, `"#,"`, `",#"`

**Valore predefinito:** `","`

### <a name="columns-on-first-launch"></a>Colonne al primo avvio

Numero di colonne di tipo carattere visualizzate nella finestra al primo caricamento. Se `launchMode` è impostata su `"maximized"`, questa proprietà viene ignorata.

**Nome della proprietà:** `initialCols`

**Obbligatoria:** Facoltativo

**Accetta:** Intero

**Valore predefinito:** `120`

### <a name="rows-on-first-launch"></a>Righe al primo avvio

Numero di righe visualizzate nella finestra al primo caricamento. Se `launchMode` è impostata su `"maximized"`, questa proprietà viene ignorata.

**Nome della proprietà:** `initialRows`

**Obbligatoria:** Facoltativo

**Accetta:** Intero

**Valore predefinito:** `30`

<br />

___

## <a name="title-bar-settings"></a>Impostazioni per la barra del titolo

### <a name="showhide-the-title-bar"></a>Mostra/Nascondi la barra del titolo

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

### <a name="set-the-text-in-the-title-bar"></a>Imposta il testo nella barra del titolo

Quando è impostata su `true`, la barra del titolo visualizza il titolo della scheda selezionata. Quando è impostata su `false`, la barra del titolo visualizza "Terminale Windows". La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.

**Nome della proprietà:** `showTerminalTitleInTitlebar`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

<br />

___

## <a name="selection-settings"></a>Impostazioni per le selezioni

### <a name="copy-after-selection-is-made"></a>Copia dopo che è stata effettuata la selezione

Quando è impostata su `true`, una selezione viene immediatamente copiata negli Appunti al momento della creazione. In questo caso facendo clic con il pulsante destro del mouse, la selezione verrà sempre incollata. Quando è impostata su `false`, la selezione viene mantenuta in attesa di altre azioni. Facendo clic con il pulsante destro del mouse, la selezione verrà copiata.

**Nome della proprietà:** `copyOnSelect`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

### <a name="copy-formatting"></a>Copia formattazione

Quando è impostata su `true`, negli Appunti vengono copiate anche la formattazione del colore e del carattere del testo selezionato. Quando è impostato su `false`, negli Appunti viene copiato solo il testo normale.

**Nome della proprietà:** `copyFormatting`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

### <a name="word-delimiters"></a>Delimitatori di parola

Determina i delimitatori di parola usati quando si fa doppio clic per selezionare. I delimitatori di parola sono caratteri che specificano la posizione del limite tra due parole. Gli esempi più comuni sono spazi, punti e virgola, virgole e punti.

**Nome della proprietà:** `wordDelimiters`

**Obbligatoria:** Facoltativo

**Accetta:** caratteri in formato stringa

**Valore predefinito:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code><br>_(`│` è `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_

<br />

___

## <a name="scroll-speed"></a>Velocità di scorrimento

Numero di righe da scorrere per volta quando si usa la rotellina del mouse. Sostituisce l'impostazione di sistema se il valore è diverso da zero o `"system"`.

**Nome della proprietà:** `rowsToScroll`

**Obbligatoria:** Facoltativo

**Accetta:** Intero

**Valore predefinito:** `"system"`

<br />

___

## <a name="window-resize-behavior"></a>Comportamento di ridimensionamento delle finestre

:::row:::
:::column span="":::
Quando è impostata su `true`, la finestra verrà allineata al limite del carattere più vicino quando viene ridimensionata. Quando è impostata su `false`, la finestra verrà ridimensionata senza vincoli.

**Nome della proprietà:** `snapToGridOnResize`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

:::column-end:::
:::column span="":::
![Terminale Windows - Blocca sulla griglia al ridimensionamento](./../images/snap-to-grid-on-resize.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="rendering-settings"></a>Impostazioni di rendering

Per cambiare le impostazioni di rendering, vedere le informazioni aggiuntive disponibili nella [pagina sulla risoluzione dei problemi](./../troubleshooting.md#the-text-is-blurry) per assistenza.

### <a name="screen-redrawing"></a>Ridisegno dello schermo

Se questa proprietà è impostata su `true`, il terminale ridisegnerà ogni frame dello schermo. Se è impostata su `false`, verrà eseguito solo il rendering degli aggiornamenti dello schermo tra frame.

**Nome della proprietà:** `experimental.rendering.forceFullRepaint`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

### <a name="software-rendering"></a>Rendering del software

Se questa proprietà è impostata su `true`, il terminale userà il renderer software, ossia WARP, invece di quello hardware.

**Nome della proprietà:** `experimental.rendering.software`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`
