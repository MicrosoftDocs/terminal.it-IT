---
title: Terminale Windows - Impostazioni globali
description: Informazioni su come personalizzare le impostazioni globali in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 11/11/2020
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 2724cc52c5a612184a7a5fc3a09be4d3d2d6d232
ms.sourcegitcommit: 9a2f9d152f65cdc8106fb9aad7fa69b01f3d05db
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/11/2020
ms.locfileid: "94520266"
---
# <a name="global-settings-in-windows-terminal"></a>Impostazioni globali di Terminale Windows

Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo. Queste proprietà devono essere inserite nella radice del file settings.json.

## <a name="default-profile"></a>Profilo predefinito

Imposta il profilo predefinito che viene aperto quando si digita <kbd>ctrl+shift+t</kbd>, si digita il tasto di scelta rapida assegnato a `newTab`, si esegue `wt new-tab` senza specificare un profilo o si fa clic sull'icona '+'.

**Nome della proprietà:** `defaultProfile`

**Obbligatoria:** Obbligatoria

**Accetta:** GUID o nome del profilo in formato stringa

**Valore predefinito:** GUID di PowerShell

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

### <a name="use-tab-switcher-experience-preview"></a>Usare l'esperienza di selezione scheda ([Anteprima](https://aka.ms/terminal-preview))

:::row:::
:::column span="":::
Quando è impostato su `true` o `"mru"` , i `nextTab` comandi e utilizzeranno `prevTab` l'interfaccia utente di selezione scheda, con l'ordine di utilizzo più recente. Quando è impostato su `"inOrder"` , queste azioni cambieranno le schede nell'ordine corrente sulla barra della scheda. L'interfaccia utente mostrerà tutte le schede attualmente aperte in un elenco verticale, navigable con la tastiera o il mouse.

Il selettore di schede verrà aperto sulla pressione iniziale delle azioni per `nextTab` e `prevTab` e resterà aperto finché il tasto di modifica verrà mantenuto premuto. Quando vengono rilasciati tutti i tasti di modifica, lo switcher si chiude e la scheda evidenziata verrà messa a fuoco. <kbd>scheda</kbd> / <kbd>MAIUSC + TAB</kbd>, i tasti freccia <kbd>su</kbd> e <kbd>giù</kbd> e le `nextTab` / `prevTab` azioni possono essere usate per scorrere l'interfaccia utente di selezione.

Per disabilitare lo switcher di tabulazione, è possibile impostare questa impostazione su `false` o su `"disabled"` .

**Nome della proprietà:** `tabSwitcherMode`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`, `"mru"`, `"inOrder"`, `"disabled"`

**Valore predefinito:** `true`

:::column-end:::
:::column span="":::
![Switcher Scheda terminale Windows](./../images/tab-switcher.gif)

:::column-end:::
:::row-end:::

> [!IMPORTANT]
> Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).

### <a name="enable-tab-switcher"></a>Abilita Switcher schede

Quando questa impostazione è impostata su `true` , i `nextTab` comandi e utilizzeranno `prevTab` l'interfaccia utente di selezione scheda. L'interfaccia utente mostrerà tutte le schede attualmente aperte in un elenco verticale, navigable con la tastiera o il mouse.

Il selettore di schede verrà aperto sulla pressione iniziale delle azioni per `nextTab` e `prevTab` e resterà aperto finché il tasto di modifica verrà mantenuto premuto. Quando vengono rilasciati tutti i tasti di modifica, lo switcher si chiude e la scheda evidenziata verrà messa a fuoco. <kbd>scheda</kbd> / <kbd>MAIUSC + TAB</kbd>, i tasti freccia <kbd>su</kbd> e <kbd>giù</kbd> e le `nextTab` / `prevTab` azioni possono essere usate per scorrere l'interfaccia utente di selezione.

**Nome della proprietà:** `useTabSwitcher`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

> [!CAUTION]
> L' `"useTabSwitcher"` impostazione non è più disponibile nelle versioni 1,5 e successive. Si consiglia di utilizzare `"tabSwitcherMode"` invece l'impostazione.

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

### <a name="launch-on-startup"></a>Avvia all'avvio

Se questa proprietà è impostata su `true`, abilita l'avvio di Terminale Windows all'avvio del sistema. L'impostazione su `false` disabiliterà la voce dell'attività di avvio del sistema. Nota: se la voce dell'attività di avvio del sistema di Terminale Windows viene disabilitata da criteri dell'organizzazione o da un'azione dell'utente, questa impostazione non avrà effetto.

**Nome della proprietà:** `startOnUserLogin`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

### <a name="launch-mode"></a>Modalità di avvio

Definisce se il terminale verrà avviato come ingrandito, a schermo intero o in una finestra. L'impostazione di questa opzione su `focus` equivale all'avvio del terminale in `default` modalità, ma con la [modalità messa a fuoco](./actions.md#toggle-focus-mode) abilitata. Analogamente, l'impostazione di questa opzione su comporterà `maximizedFocus` l'avvio del terminale in una finestra ingrandita con la modalità messa a fuoco abilitata.

**Nome della proprietà:** `launchMode`

**Obbligatoria:** Facoltativo

**Accetta:** `"default"`, `"maximized"`, `"fullscreen"`, `"focus"`, `"maximizedFocus"`

**Valore predefinito:** `"default"`

> [!IMPORTANT]
> Le `"focus"` `"maximizedFocus"` modalità e sono disponibili solo in [Windows Terminal Preview](https://aka.ms/terminal-preview/).

### <a name="launch-position"></a>Posizione di avvio

Consente di impostare la posizione in pixel dell'angolo superiore sinistro della finestra al primo caricamento. In un sistema con più schermi queste coordinate si riferiscono all'angolo superiore sinistro dello schermo principale. Se non viene specificata una coordinata X o Y, il terminale userà l'impostazione predefinita del sistema per tale valore. Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , la finestra verrà ingrandita sul monitoraggio specificato da tali coordinate.

**Nome della proprietà:** `initialPosition`

**Obbligatoria:** Facoltativo

**Accetta:** coordinate nei formati stringa seguenti: `","`, `"#,#"`, `"#,"`, `",#"`

**Valore predefinito:** `","`

### <a name="columns-on-first-launch"></a>Colonne al primo avvio

Numero di colonne di tipo carattere visualizzate nella finestra al primo caricamento. Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , questa proprietà viene ignorata.

**Nome della proprietà:** `initialCols`

**Obbligatoria:** Facoltativo

**Accetta:** Intero

**Valore predefinito:** `120`

### <a name="rows-on-first-launch"></a>Righe al primo avvio

Numero di righe visualizzate nella finestra al primo caricamento. Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , questa proprietà viene ignorata.

**Nome della proprietà:** `initialRows`

**Obbligatoria:** Facoltativo

**Accetta:** Intero

**Valore predefinito:** `30`

### <a name="always-on-top-mode"></a>Modalità sempre in primo piano

Quando è impostato su true, Windows Terminal viene avviato in tutte le altre finestre sul desktop. Questo stato può anche essere attivato o disattivato con l' `toggleAlwaysOnTop` associazione di tasti.

**Nome della proprietà:** `alwaysOnTop`

**Obbligatoria:** Facoltativo

**Accetta:**`true, false`

**Valore predefinito:** `false`

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

Quando è impostato su `true` , la formattazione del colore e del carattere del testo selezionato viene anche copiata negli Appunti. Quando è impostato su `false`, negli Appunti viene copiato solo il testo normale. È inoltre possibile specificare i formati che si desidera copiare.

**Nome della proprietà:** `copyFormatting`

**Obbligatoria:** Facoltativo

**Accetta:** `true` , `false` , `"all"` , `"none"` , `"html"` , `"rtf"`

**Valore predefinito:** `false`

### <a name="word-delimiters"></a>Delimitatori di parola

Determina i delimitatori di parola usati quando si fa doppio clic per selezionare. I delimitatori di parola sono caratteri che specificano la posizione del limite tra due parole. Gli esempi più comuni sono spazi, punti e virgola, virgole e punti.

**Nome della proprietà:** `wordDelimiters`

**Obbligatoria:** Facoltativo

**Accetta:** caratteri in formato stringa

**Valore predefinito:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code><br>_(`│` è `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_

<br />

___

## <a name="paste-warnings"></a>Avvisi incolla

### <a name="warn-when-the-text-to-paste-is-very-large"></a>Avvisa quando il testo da incollare è molto grande

Quando è impostato su, quando si `true` tenta di incollare testo con più di 5 KiB di caratteri verrà visualizzata una finestra di dialogo in cui viene chiesto se continuare o meno con l'operazione Incolla. Quando è impostato su `false` , la finestra di dialogo non viene visualizzata e invece il testo viene incollato immediatamente. Se spesso si fa clic con il pulsante destro del mouse sul terminale per errore dopo aver selezionato una grande quantità di testo, potrebbe essere utile evitare che il terminale non risponda mentre il programma connesso al terminale riceve il contenuto degli Appunti.

**Nome della proprietà:** `largePasteWarning`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

### <a name="warn-when-the-text-to-paste-contains-multiple-lines"></a>Avvisa quando il testo da incollare contiene più righe

Quando è impostato su, quando si `true` tenta di incollare testo con più righe verrà visualizzata una finestra di dialogo in cui viene chiesto se continuare o meno con l'operazione Incolla. Quando è impostato su `false` , la finestra di dialogo non viene visualizzata e invece il testo viene incollato immediatamente. Nella maggior parte delle shell, una riga corrisponde a un comando, quindi se si incolla il testo che contiene il carattere "nuova riga" in una shell, è possibile che uno o più comandi vengano eseguiti automaticamente al termine della copia, senza che sia necessario convalidare i comandi. Questa operazione può essere utile se si copiano e si incollano spesso comandi da siti Web non attendibili.

**Nome della proprietà:** `multiLinePasteWarning`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

<br />

___

## <a name="disable-animations-preview"></a>Disabilita animazioni ([Anteprima](https://aka.ms/terminal-preview))

In questo modo vengono disabilitate le animazioni visive nell'applicazione quando è impostato su `true` .

**Nome della proprietà:** `disableAnimations`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

> [!IMPORTANT]
> Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).

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
