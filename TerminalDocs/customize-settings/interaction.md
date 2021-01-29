---
title: Impostazioni di interazione del terminale di Windows
description: Informazioni su come personalizzare le impostazioni di interazione nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: e16c093ad1a6b7efb058377840bf8d516ef0fb69
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041974"
---
# <a name="interaction-settings-in-windows-terminal"></a>Impostazioni di interazione nel terminale di Windows

Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo. Queste proprietà devono essere inserite nella radice del file settings.json.

> [!IMPORTANT]
> L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview). Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).

## <a name="automatically-copy-selection-to-clipboard"></a>Copia automaticamente selezione negli Appunti

Quando è impostata su `true`, una selezione viene immediatamente copiata negli Appunti al momento della creazione. In questo caso facendo clic con il pulsante destro del mouse, la selezione verrà sempre incollata. Quando è impostata su `false`, la selezione viene mantenuta in attesa di altre azioni. Facendo clic con il pulsante destro del mouse, la selezione verrà copiata.

**Nome della proprietà:** `copyOnSelect`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

<br />

___

## <a name="text-format-when-copying"></a>Formato testo durante la copia

Quando è impostato su `true` , la formattazione del colore e del carattere del testo selezionato viene anche copiata negli Appunti. Quando è impostato su `false`, negli Appunti viene copiato solo il testo normale. È inoltre possibile specificare i formati che si desidera copiare.

**Nome della proprietà:** `copyFormatting`

**Obbligatoria:** Facoltativo

**Accetta:** `true` , `false` , `"all"` , `"none"` , `"html"` , `"rtf"`

**Valore predefinito:** `false`

<br />

___

## <a name="word-delimiters"></a>Delimitatori di parola

Determina i delimitatori di parola usati quando si fa doppio clic per selezionare. I delimitatori di parola sono caratteri che specificano la posizione del limite tra due parole. Gli esempi più comuni sono spazi, punti e virgola, virgole e punti.

**Nome della proprietà:** `wordDelimiters`

**Obbligatoria:** Facoltativo

**Accetta:** caratteri in formato stringa

**Valore predefinito:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code><br>_(`│` è `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_

<br />

___

## <a name="snap-window-resizing-to-character-grid"></a>Blocca la finestra di ridimensionamento in griglia caratteri

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

## <a name="tab-settings"></a>Impostazioni per le schede

### <a name="tab-switcher-interface-style"></a>Stile dell'interfaccia Switcher di tabulazione

:::row:::
:::column span="":::
Quando è impostato su `true` o `"mru"` , i `nextTab` comandi e utilizzeranno `prevTab` l'interfaccia utente di selezione scheda, con l'ordine di utilizzo più recente. Quando è impostato su `"inOrder"` , queste azioni cambieranno le schede nell'ordine corrente sulla barra della scheda. L'interfaccia utente mostrerà tutte le schede attualmente aperte in un elenco verticale, navigable con la tastiera o il mouse.

Il selettore di schede verrà aperto sulla pressione iniziale delle azioni per `nextTab` e `prevTab` e resterà aperto finché il tasto di modifica verrà mantenuto premuto. Quando vengono rilasciati tutti i tasti di modifica, lo switcher si chiude e la scheda evidenziata verrà messa a fuoco. <kbd>scheda</kbd> / <kbd>MAIUSC + TAB</kbd>, i tasti freccia <kbd>su</kbd> e <kbd>giù</kbd> e le `nextTab` / `prevTab` azioni possono essere usate per scorrere l'interfaccia utente di selezione.

Per disabilitare lo switcher di tabulazione, è possibile impostare questa impostazione su `false` o su `"disabled"` .

**Nome della proprietà:** `tabSwitcherMode`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`, `"mru"`, `"inOrder"`, `"disabled"`

**Valore predefinito:** `"inOrder"`

:::column-end:::
:::column span="":::
![Switcher Scheda terminale Windows](./../images/tab-switcher.gif)

:::column-end:::
:::row-end:::

### <a name="enable-tab-switcher"></a>Abilita Switcher schede

Quando questa impostazione è impostata su `true` , i `nextTab` comandi e utilizzeranno `prevTab` l'interfaccia utente di selezione scheda. L'interfaccia utente mostrerà tutte le schede attualmente aperte in un elenco verticale, navigable con la tastiera o il mouse.

Il selettore di schede verrà aperto sulla pressione iniziale delle azioni per `nextTab` e `prevTab` e resterà aperto finché il tasto di modifica verrà mantenuto premuto. Quando vengono rilasciati tutti i tasti di modifica, lo switcher si chiude e la scheda evidenziata verrà messa a fuoco. <kbd>scheda</kbd> / <kbd>MAIUSC + TAB</kbd>, i tasti freccia <kbd>su</kbd> e <kbd>giù</kbd> e le `nextTab` / `prevTab` azioni possono essere usate per scorrere l'interfaccia utente di selezione.

**Nome della proprietà:** `useTabSwitcher`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

> [!CAUTION]
> L' `"useTabSwitcher"` impostazione non è più disponibile nelle versioni 1,5 e successive. Si consiglia di utilizzare `"tabSwitcherMode"` invece l'impostazione.

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
