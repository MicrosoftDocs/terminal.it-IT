---
title: Impostazioni del profilo aspetto terminale Windows
description: Informazioni su come personalizzare le impostazioni del profilo aspetto nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 0257f6698e0a497e98b77f4b574560adea00b7e1
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041970"
---
# <a name="appearance-profile-settings-in-windows-terminal"></a>Impostazioni del profilo aspetto nel terminale di Windows

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

> [!IMPORTANT]
> L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview). Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).

## <a name="text"></a>Testo

### <a name="color-scheme"></a>Combinazione colori

Nome della combinazione colori usata nel profilo. Le combinazioni colori sono definite nell'oggetto `schemes`. Per informazioni più dettagliate, vedi la [pagina Combinazioni colori](./color-schemes.md).

**Nome della proprietà:** `colorScheme`

**Obbligatoria:** Facoltativo

**Accetta:** nome della combinazione colori in formato stringa

**Valore predefinito:** `"Campbell"`

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

### <a name="font-weight"></a>Peso carattere

Questa proprietà imposta lo spessore (tratti sottili o spessi) per il tipo di carattere del profilo.

**Nome della proprietà:** `fontWeight`

**Obbligatoria:** Facoltativo

**Accetta**  `"normal"`, `"thin"`, `"extra-light"`, `"light"`, `"semi-light"`, `"medium"`, `"semi-bold"`, `"bold"`, `"extra-bold"`, `"black"`, `"extra-black"` oppure un intero che corrisponde alla rappresentazione numerica dello spesso del tipo di carattere OpenType

**Valore predefinito:** `"normal"`

## <a name="retro-terminal-effects"></a>Effetti per terminale retro

:::row:::
:::column span="":::
Quando è impostata su `true`, il terminale emulerà un monitor CRT classico con linee di scansione e bordi di testo sfocati. Si tratta di una funzionalità sperimentale che potrebbe non essere mantenuta.

Se `experimental.pixelShaderPath` è impostato, eseguirà l'override di questa impostazione.

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

<br />

___

## <a name="cursor"></a>Cursore

### <a name="cursor-shape"></a>Forma del cursore

Consente di impostare la forma del cursore per il profilo. I possibili cursori sono i seguenti: `"bar"` (&#x2503;), `"vintage"` (&#x2583;), `"underscore"` (&#x2581;), `"filledBox"` (&#x2588;), `"emptyBox"` (&#x25AF;), `"doubleUnderscore"` (&#x2017;)

**Nome della proprietà:** `cursorShape`

**Obbligatoria:** Facoltativo

**Accetta:** `"bar"` , `"vintage"` , `"underscore"` , `"filledBox"` , `"emptyBox"` , `"doubleUnderscore"`

**Valore predefinito:** `"bar"`

> [!IMPORTANT]
> La `"doubleUnderscore"` forma del cursore è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).

### <a name="cursor-height"></a>Altezza del cursore

Consente di impostare l'altezza percentuale del cursore a partire dalla parte inferiore. Funziona solo se `cursorShape` è impostata su `"vintage"`.

**Nome della proprietà:** `cursorHeight`

**Obbligatoria:** Facoltativo

**Accetta:** intero compreso tra 25-100

<br />

___

## <a name="background-image"></a>Immagine di sfondo

### <a name="background-image-path"></a>Percorso dell'immagine di sfondo

Consente di impostare il percorso del file dell'immagine da tracciare sullo sfondo della finestra. L'immagine di sfondo può essere un file con estensione jpg, png o gif. `"desktopWallpaper"` imposta l'immagine di sfondo sullo sfondo del desktop.

**Nome della proprietà:** `backgroundImage`

**Obbligatoria:** Facoltativo

**Accetta:** Percorso del file sotto forma di stringa o `"desktopWallpaper"`

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

## <a name="acrylic"></a>Acrilico

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

## <a name="window"></a>Finestra

### <a name="padding"></a>Spaziatura interna

:::row:::
:::column span="":::
Consente di impostare la spaziatura intorno al testo all'interno della finestra. Questo accetta tre formati diversi: `"#"` e imposta `#` la stessa spaziatura interna per tutti i lati, `"#, #"` imposta la stessa spaziatura interna per Left-Right e top-bottom e `"#, #, #, #"` imposta la spaziatura interna singolarmente per left, top, Right e Bottom.

**Nome della proprietà:** `padding`

**Obbligatoria:** Facoltativo

**Accetta:** Valori come stringa nei formati seguenti: `"#"` , `"#, #"` `"#, #, #, #"` o valore come Integer: `#`

**Valore predefinito:** `"8, 8, 8, 8"`

:::column-end:::
:::column span="":::
![Terminale Windows - Spaziatura interna](./../images/padding.gif)

:::column-end:::
:::row-end:::

### <a name="scrollbar-visibility"></a>Visibilità della barra di scorrimento

Consente di impostare la visibilità della barra di scorrimento.

**Nome della proprietà:** `scrollbarState`

**Obbligatoria:** Facoltativo

**Accetta:** `"visible"`, `"hidden"`

<br />

___

## <a name="color-settings"></a>Impostazioni per il colore

### <a name="tab-color"></a>Colore delle schede

Viene impostato il colore della scheda del profilo. Se si utilizza la selezione colori scheda, questo colore verrà ignorato.

**Nome della proprietà:** `tabColor`

**Obbligatoria:** Facoltativo

**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`

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

### <a name="cursor-color"></a>Colore del cursore

Consente di impostare il colore del cursore per il profilo. Sostituisce il valore di `cursorColor` impostato nella combinazione colori se è impostata `colorScheme`.

**Nome della proprietà:** `cursorColor`

**Obbligatoria:** Facoltativo

**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`

<br />

___

## <a name="pixel-shader-effects-preview"></a>Effetti pixel shader ([Anteprima](https://aka.ms/terminal-preview))

Questa impostazione consente a un utente di specificare il percorso di un pixel shader personalizzato da usare con il contenuto del terminale. Si tratta di una funzionalità sperimentale che potrebbe non essere mantenuta. Per altri dettagli sulla creazione di pixel shader personalizzati per il terminale, vedere [questa documentazione](https://github.com/microsoft/terminal/blob/main/samples/PixelShaders/README.md).

Se impostato, l'impostazione verrà sostituita `experimental.retroTerminalEffect` .

**Nome della proprietà:** `experimental.pixelShaderPath`

**Obbligatoria:** Facoltativo

**Accetta:** Percorso di un `.hlsl` file shader sotto forma di stringa

> [!IMPORTANT]
> Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).
