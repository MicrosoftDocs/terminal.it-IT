---
title: Terminale Windows - Impostazioni del profilo
description: Informazioni su come personalizzare i singoli profili in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 309fb40736718df7d1670a7376806b70ef0e35fe
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416086"
---
# <a name="profile-settings-in-the-windows-terminal"></a>Impostazioni del profilo in Terminale Windows

Le impostazioni elencate di seguito sono specifiche dei singoli profili univoci. Se vuoi applicare un'impostazione a tutti i profili, puoi aggiungerla alla sezione `defaults` prima dell'elenco dei profili nel file settings.json.

```json
"defaults":
{
    // SETTINGS TO APPLY TO ALL PROFILES
},
"list":
[
    // PROFILE OBJECTS
]
```

## <a name="unique-identifier"></a>Identificatore univoco

I profili possono usare un GUID come identificatore univoco. Per impostare un profilo come predefinito, è necessario un GUID per l'impostazione globale `defaultProfile`.

**Nome della proprietà:** `guid`

**Obbligatoria:** Obbligatoria

**Accetta:** GUID in formato stringa del Registro di sistema: `"{00000000-0000-0000-0000-000000000000}"`

<br />

___

## <a name="executable-settings"></a>Impostazioni per file eseguibili

### <a name="command-line"></a>Riga di comando

File eseguibile usato nel profilo.

**Nome della proprietà:** `commandline`

**Obbligatoria:** Facoltativo

**Accetta:** nome del file eseguibile in formato stringa

**Valore predefinito:** `"cmd.exe"`

### <a name="source"></a>Origine

Archivia il nome del generatore di profili che ha originato il profilo. _Non esistono valori individuabili per questo campo._ Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).

**Nome della proprietà:** `source`

**Obbligatoria:** Facoltativo

**Accetta:** String

### <a name="starting-directory"></a>Directory iniziale

Directory in cui viene avviata la shell quando viene caricata.

**Nome della proprietà:** `startingDirectory`

**Obbligatoria:** Facoltativo

**Accetta:** percorso della cartella in formato stringa

**Valore predefinito:** `"%USERPROFILE%"`

<br />

___

## <a name="dropdown-settings"></a>Impostazioni per il menu a discesa

![Terminale Windows - Menu a discesa](./../images/dropdown.png)
_Configurazione: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_

### <a name="name"></a>Nome

Nome del profilo che verrà visualizzato nel menu a discesa. Questo valore viene usato anche come titolo da passare alla shell all'avvio. Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione. Per eseguire l'override di questo comportamento del titolo, usa `tabTitle`.

**Nome della proprietà:** `name`

**Obbligatoria:** Obbligatoria

**Accetta:** String

### <a name="icon"></a>Icona

Consente di impostare l'icona visualizzata all'interno della scheda e nel menu a discesa.

**Nome della proprietà:** `icon`

**Obbligatoria:** Facoltativo

**Accetta:** percorso del file in formato stringa

### <a name="hide-a-profile-from-the-dropdown"></a>Nascondi un profilo nell'elenco a discesa

Se `hidden` è impostato su `true`, il profilo non verrà visualizzato nell'elenco dei profili. Può essere usata per nascondere i profili predefiniti e quelli generati dinamicamente, lasciandoli nel file settings. Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).

**Nome della proprietà:** `hidden`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

<br />

___

## <a name="tab-title-settings"></a>Impostazioni per i titoli delle schede

### <a name="custom-tab-title"></a>Titolo scheda personalizzato

Se è impostata, sostituirà `name` come titolo da passare alla shell all'avvio. Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione. Per informazioni su come impostare la shell come titolo, vedi l'[esercitazione relativa al titolo della scheda](./../tutorials/tab-title.md).

**Nome della proprietà:** `tabTitle`

**Obbligatoria:** Facoltativo

**Accetta:** String

### <a name="suppress-title-changes-from-the-shell"></a>Non visualizzare le modifiche apportate al titolo dalla shell

Quando è impostata su `true`, `tabTitle` sostituisce il titolo predefinito della scheda. Tutti i messaggi di modifica del titolo dall'applicazione verranno eliminati. Se `tabTitle` non è impostata, verrà usata `name`. Quando è impostata su `false`, `tabTitle` si comporta normalmente.

**Nome della proprietà:** `suppressApplicationTitle`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

<br />

___

## <a name="text-settings"></a>Impostazioni per il testo

### <a name="font-face"></a>Tipo di carattere

Nome del tipo di carattere usato nel profilo. Il terminale proverà ad eseguire il fallback a Consolas se non riesce a trovarlo o non è valido. Per informazioni sulle altre varianti del tipo di carattere predefinito, Cascadia Mono, vedi la [tabella codici di Cascadia](./../cascadia-code.md).

**Nome della proprietà:** `fontFace`

**Obbligatoria:** Facoltativo

**Accetta:** nome del tipo di carattere in formato stringa

**Valore predefinito:** `"Cascadia Mono"`

### <a name="font-size"></a>Dimensioni del carattere

Consente di impostare le dimensioni del carattere del profilo in punti.

**Nome della proprietà:** `fontSize`

**Obbligatoria:** Facoltativo

**Accetta:** Intero

**Valore predefinito:** `12`

### <a name="padding"></a>Spaziatura interna

:::row:::
:::column span="":::
Consente di impostare la spaziatura intorno al testo all'interno della finestra. Vengono accettati tre diversi formati: `"#"` imposta la stessa spaziatura interna su tutti i lati, `"#, #"` imposta la stessa spaziatura interna per left-right e top-bottom, mentre `"#, #, #, #"` imposta la spaziatura interna singolarmente per left, top, right e bottom.

**Nome della proprietà:** `padding`

**Obbligatoria:** Facoltativo

**Accetta:** valori nei formati stringa seguenti: `"#"`, `"#, #"`, `"#, #, #, #"`

**Valore predefinito:** `"8, 8, 8, 8"`

:::column-end:::
:::column span="":::
![Terminale Windows - Spaziatura interna](./../images/padding.gif)

:::column-end:::
:::row-end:::

### <a name="antialiasing-text"></a>Anti-aliasing del testo

Controlla la modalità di anti-aliasing del testo nel renderer. La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.

![Terminale Windows - Anti-aliasing del testo](./../images/antialiasing-mode.gif)

**Nome della proprietà:** `antialiasingMode`

**Obbligatoria:** Facoltativo

**Accetta:** `"grayscale"`, `"cleartype"`, `"aliased"`

**Valore predefinito:** `"grayscale"`

<br />

___

## <a name="cursor-settings"></a>Impostazioni per il cursore

### <a name="cursor-shape"></a>Forma del cursore

Consente di impostare la forma del cursore per il profilo. I cursori possibili sono i seguenti: `"bar"` (&#x2503;), `"vintage"` (&#x2583;), `"underscore"` (&#x2581;), `"filledBox"` (&#x2588;), `"emptyBox"` (&#x25AF;)

**Nome della proprietà:** `cursorShape`

**Obbligatoria:** Facoltativo

**Accetta:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`

**Valore predefinito:** `"bar"`

### <a name="cursor-color"></a>Colore del cursore

Consente di impostare il colore del cursore per il profilo. Sostituisce il valore di `cursorColor` impostato nella combinazione colori se è impostata `colorScheme`.

**Nome della proprietà:** `cursorColor`

**Obbligatoria:** Facoltativo

**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`

### <a name="cursor-height"></a>Altezza del cursore

Consente di impostare l'altezza percentuale del cursore a partire dalla parte inferiore. Funziona solo se `cursorShape` è impostata su `"vintage"`.

**Nome della proprietà:** `cursorHeight`

**Obbligatoria:** Facoltativo

**Accetta:** intero compreso tra 25-100

<br />

___

## <a name="color-settings"></a>Impostazioni per il colore

### <a name="color-scheme"></a>Combinazione colori

Nome della combinazione colori usata nel profilo. Le combinazioni colori sono definite nell'oggetto `schemes`. Per informazioni più dettagliate, vedi la [pagina Combinazioni colori](./color-schemes.md).

**Nome della proprietà:** `colorScheme`

**Obbligatoria:** Facoltativo

**Accetta:** nome della combinazione colori in formato stringa

**Valore predefinito:** `"Campbell"`

### <a name="foreground-color"></a>Colore primo piano

Modifica il colore primo piano del profilo. Sostituisce il valore di `foreground` impostato nella combinazione colori se è impostata `colorScheme`.

**Nome della proprietà:** `foreground`

**Obbligatoria:** Facoltativo

**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`

### <a name="background-color"></a>Colore di sfondo

Modifica il colore di sfondo del profilo. Sostituisce il valore di `background` impostato nella combinazione colori se è impostata `colorScheme`.

**Nome della proprietà:** `background`

**Obbligatoria:** Facoltativo

**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`

### <a name="selection-background-color"></a>Colore di sfondo della selezione

Consente di impostare il colore di sfondo di una selezione nel profilo. Sostituisce il valore di `selectionBackground` impostato nella combinazione colori se è impostata `colorScheme`.

**Nome della proprietà:** `selectionBackground`

**Obbligatoria:** Facoltativo

**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`

<br />

___

## <a name="acrylic-settings"></a>Impostazioni per acrilico

### <a name="enable-acrylic"></a>Abilita acrilico

:::row:::
:::column span="":::
Quando è impostata su `true`, la finestra avrà uno sfondo acrilico. Quando è impostato su `false`, la finestra avrà uno sfondo normale e senza trame. A causa delle limitazioni del sistema operativo, la trasparenza si applica solo alle finestre con lo stato attivo.

**Nome della proprietà:** `useAcrylic`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

:::column-end:::
:::column span="":::
![Terminale Windows - Acrilico](./../images/acrylic.gif)

:::column-end:::
:::row-end:::

### <a name="acrylic-opacity"></a>Opacità acrilico

:::row:::
:::column span="":::
Quando `useAcrylic` è impostata su `true`, imposta la trasparenza della finestra per il profilo. Accetta valori a virgola mobile compresi tra 0 e 1.

**Nome della proprietà:** `acrylicOpacity`

**Obbligatoria:** Facoltativo

**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1

**Valore predefinito:** `0.5`

:::column-end:::
:::column span="":::
![Terminale Windows - Opacità acrilico](./../images/acrylic-opacity.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="background-image-settings"></a>Impostazioni per immagine di sfondo

### <a name="setting-the-background-image"></a>Impostazione dell'immagine di sfondo

Consente di impostare il percorso del file dell'immagine da tracciare sullo sfondo della finestra. L'immagine di sfondo può essere un file con estensione jpg, png o gif.

**Nome della proprietà:** `backgroundImage`

**Obbligatoria:** Facoltativo

**Accetta:** percorso del file in formato stringa

### <a name="background-image-stretch-mode"></a>Modalità di estensione dell'immagine di sfondo

:::row:::
:::column span="":::
Consente di impostare la modalità di ridimensionamento dell'immagine di sfondo in modo che occupi tutto lo spazio della finestra.

**Nome della proprietà:** `backgroundImageStretchMode`

**Obbligatoria:** Facoltativo

**Accetta:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`

**Valore predefinito:** `"uniformToFill"`

:::column-end:::
:::column span="":::
![Terminale Windows - Modalità di estensione dell'immagine di sfondo](./../images/background-image-stretch-mode.gif)
 _[Origine dell'immagine di sfondo](https://wallpaperhub.app/wallpapers/6287)_

:::column-end:::
:::row-end:::

### <a name="background-image-alignment"></a>Allineamento dell'immagine di sfondo

:::row:::
:::column span="":::
Consente di impostare la modalità di allineamento dell'immagine di sfondo ai bordi della finestra.

**Nome della proprietà:** `backgroundImageAlignment`

**Obbligatoria:** Facoltativo

**Accetta:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`

**Valore predefinito:** `"center"`

:::column-end:::
:::column span="":::
![Terminale Windows - Allineamento dell'immagine di sfondo](./../images/background-image-alignment.gif)
 _[Origine dell'immagine di sfondo](https://design.ubuntu.com/brand/ubuntu-logo/)_

:::column-end:::
:::row-end:::

### <a name="background-image-opacity"></a>Opacità dell'immagine di sfondo

:::row:::
:::column span="":::
Consente di impostare la trasparenza dell'immagine di sfondo.

:::column-end:::
:::row-end:::

**Nome della proprietà:** `backgroundImageOpacity`

**Obbligatoria:** Facoltativo

**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1

**Valore predefinito:** `1.0`

<br />

___

## <a name="scroll-settings"></a>Impostazioni per lo scorrimento

### <a name="scrollbar-visibility"></a>Visibilità della barra di scorrimento

Consente di impostare la visibilità della barra di scorrimento.

**Nome della proprietà:** `scrollbarState`

**Obbligatoria:** Facoltativo

**Accetta:** `"visible"`, `"hidden"`

### <a name="scroll-to-input-line-when-typing"></a>Scorri fino alla riga di input durante la digitazione

Quando è impostata su `true`, la finestra scorre fino alla riga di input del comando durante la digitazione. Quando è impostata su `false`, lo scorrimento della finestra non è attivato quando inizi a digitare.

**Nome della proprietà:** `snapOnInput`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

### <a name="history-size"></a>Dimensioni della cronologia

Consente di impostare il numero di righe a cui è possibile passare scorrendo che precedono quelle visualizzate nella finestra.

**Nome della proprietà:** `historySize`

**Obbligatoria:** Facoltativo

**Accetta:** Intero

**Valore predefinito:** `9001`

<br />

___

## <a name="how-the-profile-closes-when-exiting"></a>Modalità di chiusura del profilo all'uscita

Consente di impostare la reazione del profilo alla chiusura o a un errore all'avvio. Con `"graceful"`, il profilo verrà chiuso quando viene digitato `exit` o quando il processo viene chiuso normalmente. Con `"always"` il profilo verrà sempre chiuso, mentre con `"never"` non verrà mai chiuso. `true` e `false` vengono accettati come sinonimi rispettivamente per `"graceful"` e `"never"`.

**Nome della proprietà:** `closeOnExit`

**Obbligatoria:** Facoltativo

**Accetta:** `"graceful"`, `"always"`, `"never"`, `true`, `false`

**Valore predefinito:** `"graceful"`

<br />

___

## <a name="retro-terminal-effects"></a>Effetti per terminale retro

:::row:::
:::column span="":::
Quando è impostata su `true`, il terminale emulerà un monitor CRT classico con linee di scansione e bordi di testo sfocati. Si tratta di una funzionalità sperimentale che potrebbe non essere mantenuta.

**Nome della proprietà:** `experimental.retroTerminalEffect`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

:::column-end:::
:::column span="":::
![Terminale Windows - Effetto sperimentale per terminale retro](./../images/experimental-retro-terminal-effect.gif)
_Configurazione: [Prompt dei comandi retro](./../custom-terminal-gallery/retro-command-prompt.md)_

:::column-end:::
:::row-end:::
