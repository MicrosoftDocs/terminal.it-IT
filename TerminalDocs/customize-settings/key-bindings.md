---
title: Terminale Windows - Tasti di scelta rapida
description: Informazioni su come creare tasti di scelta rapida personalizzati per Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 06/18/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 2716e3bfbbc290eb3f2bdce58d0de5c12ee3225d
ms.sourcegitcommit: 91a802863cd0730d2e364377ffe44f819a66ff2a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2020
ms.locfileid: "84994294"
---
# <a name="custom-key-bindings-in-windows-terminal"></a>Tasti di scelta rapida personalizzati in Terminale Windows

In Terminale Windows è possibile creare tasti di scelta rapida personalizzati per controllare l'interazione con il terminale tramite la tastiera.

## <a name="key-binding-formats"></a>Formati di tasti di scelta rapida

I tasti di scelta rapida possono essere strutturati nei formati seguenti:

### <a name="commands-without-arguments"></a>Comandi senza argomenti

```json
{ "command": "commandName", "keys": "modifiers+key" }
```

Questa impostazione predefinita, ad esempio, usa il tasto di scelta rapida <kbd>alt+f4</kbd> per chiudere la finestra del terminale:

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

### <a name="commands-with-arguments"></a>Comandi con argomenti

```json
{ "command": { "action": "commandName", "argument": "value" }, "keys": "modifiers+key" }
```

Questa impostazione predefinita, ad esempio, usa il tasto di scelta rapida <kbd>ctrl+maiusc+1</kbd> per aprire una nuova scheda nel terminale in base al profilo elencato per primo nel menu a discesa (in genere verrà aperto il profilo PowerShell):

```json
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+shift+1" }
```

<br />

___

## <a name="key-binding-properties"></a>Proprietà dei tasti di scelta rapida

È possibile creare tasti di scelta rapida usando le proprietà seguenti.

### <a name="command"></a>Comando

Comando eseguito quando vengono premuti i tasti associati.

**Nome della proprietà:** `command`

**Obbligatoria:** Obbligatoria

**Accetta:** String

### <a name="keys"></a>Tasti

Definisce le combinazioni di tasti usate per chiamare il comando. Con la proprietà keys è possibile associare più modificatori a un unico tasto. I tasti e i modificatori accettati sono elencati [di seguito](#accepted-modifiers-and-keys).

**Nome della proprietà:** `keys`

**Obbligatoria:** Obbligatoria

**Accetta:** stringa o matrice[stringa]

### <a name="action"></a>Azione

Aggiunge funzionalità aggiuntive a determinati comandi.

**Nome della proprietà:** `action`

**Obbligatoria:** Facoltativo

**Accetta:** String

<br />

___

## <a name="accepted-modifiers-and-keys"></a>Tasti e modificatori accettati

### <a name="modifiers"></a>Modificatori

`ctrl+`, `shift+`, `alt+`

### <a name="modifier-keys"></a>Tasti di modifica

| Type | Tasti |
| ---- | ---- |
| Tasti funzione e alfanumerici | `f1-f24`, `a-z`, `0-9` |
| Simboli | ``` ` ```, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/` |
| Tasti di direzione | `down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`, `plus` |
| Tasti di azione | `tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert` |
| Tasti del tastierino numerico | `numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply` |

<br />

___

## <a name="application-level-commands"></a>Comandi a livello di applicazione

### <a name="close-window"></a>Chiudi finestra

:::row:::
:::column span="":::
Chiude la finestra corrente e tutte le relative schede. Se `confirmCloseAllTabs` è impostato su `true`, verrà visualizzata una finestra di dialogo per confermare la chiusura di tutte le schede. Per altre informazioni su questa impostazione, vedi la [pagina delle impostazioni globali](./global-settings.md#hide-close-all-tabs-popup).

**Nome del comando:** `closeWindow`

**Associazione predefinita:**

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

:::column-end:::
:::column span="":::
![Terminale Windows - Conferma chiusura di tutte le schede](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

### <a name="find"></a>Trova

Apre la finestra di dialogo di ricerca. Per altre informazioni sulla ricerca, vedi la [pagina relativa alla ricerca](./../search.md).

**Nome del comando:** `find`

**Associazione predefinita:**

```json
{ "command": "find", "keys": "ctrl+shift+f" }
```

### <a name="open-the-dropdown"></a>Apri menu a discesa

Apre il menu a discesa.

**Nome del comando:** `openNewTabDropdown`

**Associazione predefinita:**

```json
{ "command": "openNewTabDropdown", "keys": "ctrl+shift+space" }
```

### <a name="open-settings-files"></a>Apri file di impostazioni

Apre i file di impostazioni predefiniti o personalizzati. Senza il campo `target` verrà aperto il file settings.json.

**Nome del comando:** `openSettings`

**Associazione predefinita:**

```json
{ "command": "openSettings", "keys": "ctrl+," },
{ "command": { "action": "openSettings", "target": "defaultsFile" }, "keys": "ctrl+alt+," },
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `target` | Facoltativo | `"settingsFile"`, `"defaultsFile"`, `"allFiles"` | Il file di impostazioni da aprire. |

> [!IMPORTANT]
> Il campo `target` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).

### <a name="toggle-full-screen"></a>Attiva/Disattiva schermo intero

Consente di passare dalla finestra a schermo intero a quella con dimensioni predefinite e viceversa.

**Nome del comando:** `toggleFullscreen`

**Associazioni predefinite:**

```json
{ "command": "toggleFullscreen", "keys": "alt+enter" },
{ "command": "toggleFullscreen", "keys": "f11" }
```

<br />

___

## <a name="tab-management-commands"></a>Comandi per la gestione delle schede

### <a name="close-tab"></a>Chiudi scheda

Chiude la scheda corrente.

**Nome del comando:** `closeTab`

### <a name="duplicate-tab"></a>Duplica scheda

Crea una copia della scheda corrente e la apre.

**Nome del comando:** `duplicateTab`

**Associazione predefinita:**

```json
{ "command": "duplicateTab", "keys": "ctrl+shift+d" }
```

### <a name="new-tab"></a>Nuova scheda

Crea una nuova scheda. Se viene specificato senza argomenti, il profilo predefinito verrà aperto in una nuova scheda. Se non viene specificata un'azione, verrà usata l'impostazione equivalente del profilo predefinito.

**Nome del comando:** `newTab`

**Associazioni predefinite:**

```json
{ "command": "newTab", "keys": "ctrl+shift+t" },
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+shift+1" },
{ "command": { "action": "newTab", "index": 1 }, "keys": "ctrl+shift+2" },
{ "command": { "action": "newTab", "index": 2 }, "keys": "ctrl+shift+3" },
{ "command": { "action": "newTab", "index": 3 }, "keys": "ctrl+shift+4" },
{ "command": { "action": "newTab", "index": 4 }, "keys": "ctrl+shift+5" },
{ "command": { "action": "newTab", "index": 5 }, "keys": "ctrl+shift+6" },
{ "command": { "action": "newTab", "index": 6 }, "keys": "ctrl+shift+7" },
{ "command": { "action": "newTab", "index": 7 }, "keys": "ctrl+shift+8" },
{ "command": { "action": "newTab", "index": 8 }, "keys": "ctrl+shift+9" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `commandLine` | Facoltativo | Nome del file eseguibile in formato stringa | Esegue l'eseguibile all'interno della scheda. |
| `startingDirectory` | Facoltativo | Percorso della cartella in formato stringa | Directory in cui verrà aperta la scheda. |
| `tabTitle` | Facoltativo | String | Titolo della nuova scheda. |
| `index` | Facoltativo | Intero | Profilo che verrà aperto in base alla relativa posizione nel menu a discesa (a partire da 0). |
| `profile` | Facoltativo | Nome o GUID del profilo in formato stringa | Profilo che verrà aperto in base al relativo nome o GUID. |

### <a name="open-next-tab"></a>Apri scheda successiva

Apre la scheda a destra di quella corrente.

**Nome del comando:** `nextTab`

**Associazione predefinita:**

```json
{ "command": "nextTab", "keys": "ctrl+tab" }
```

### <a name="open-previous-tab"></a>Apri scheda precedente

Apre la scheda a sinistra di quella corrente.

**Nome del comando:** `prevTab`

**Associazione predefinita:**

```json
{ "command": "prevTab", "keys": "ctrl+shift+tab" }
```

### <a name="open-a-specific-tab"></a>Apri una scheda specifica

Apre una scheda specifica a seconda dell'indice.

**Nome del comando:** `switchToTab`

**Associazioni predefinite:**

```json
{ "command": { "action": "switchToTab", "index": 0 }, "keys": "ctrl+alt+1" },
{ "command": { "action": "switchToTab", "index": 1 }, "keys": "ctrl+alt+2" },
{ "command": { "action": "switchToTab", "index": 2 }, "keys": "ctrl+alt+3" },
{ "command": { "action": "switchToTab", "index": 3 }, "keys": "ctrl+alt+4" },
{ "command": { "action": "switchToTab", "index": 4 }, "keys": "ctrl+alt+5" },
{ "command": { "action": "switchToTab", "index": 5 }, "keys": "ctrl+alt+6" },
{ "command": { "action": "switchToTab", "index": 6 }, "keys": "ctrl+alt+7" },
{ "command": { "action": "switchToTab", "index": 7 }, "keys": "ctrl+alt+8" },
{ "command": { "action": "switchToTab", "index": 8 }, "keys": "ctrl+alt+9" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `index` | Obbligatoria | Intero | Scheda che verrà aperta in base alla relativa posizione nella barra delle schede (a partire da 0). |

<br />

___

## <a name="pane-management-commands"></a>Comandi di gestione dei riquadri

### <a name="close-pane"></a>Chiudi riquadro

Chiude il riquadro attivo. Se non sono presenti riquadri divisi, chiude la scheda corrente. Se è aperta una sola scheda, chiude la finestra.

**Nome del comando:** `closePane`

**Associazione predefinita:**

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

### <a name="move-pane-focus"></a>Sposta stato attivo nel riquadro

Consente di spostare lo stato attivo in un altro riquadro a seconda della direzione.

**Nome del comando:** `moveFocus`

**Associazioni predefinite:**

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `direction` | Obbligatoria | `"left"`, `"right"`, `"up"`, `"down"` | Direzione in cui viene spostato lo stato attivo. |

### <a name="resize-a-pane"></a>Ridimensiona un riquadro

Modifica le dimensioni del riquadro attivo.

**Nome del comando:** `resizePane`

**Associazioni predefinite:**

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `direction` | Obbligatoria | `"left"`, `"right"`, `"up"`, `"down"` | Direzione in cui verranno modificate le dimensioni del riquadro. |

### <a name="split-a-pane"></a>Dividi un riquadro

Divide a metà il riquadro attivo e ne apre un altro. Se viene specificato senza argomenti, il profilo predefinito verrà aperto nel nuovo riquadro. Se non viene specificata un'azione, verrà usata l'impostazione equivalente del profilo predefinito.

**Nome del comando:** `splitPane`

**Associazioni predefinite:**

```json
// In settings.json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" },

// In defaults.json
{ "command": { "action": "splitPane", "split": "horizontal"}, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "vertical"}, "keys": "alt+shift+plus" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `split` | Obbligatoria | `"vertical"`, `"horizontal"`, `"auto"` | Modalità di divisione del riquadro. Con `"auto"` il riquadro verrà diviso nella direzione che offre l'area con la superficie più estesa. |
| `commandLine` | Facoltativo | Nome del file eseguibile in formato stringa | Esegue l'eseguibile all'interno del riquadro. |
| `startingDirectory` | Facoltativo | Percorso della cartella in formato stringa | Directory in cui verrà aperto il riquadro. |
| `tabTitle` | Facoltativo | String | Titolo della scheda quando lo stato attivo si trova nel nuovo riquadro. |
| `index` | Facoltativo | Intero | Profilo che verrà aperto in base alla relativa posizione nel menu a discesa (a partire da 0). |
| `profile` | Facoltativo | Nome o GUID del profilo in formato stringa | Profilo che verrà aperto in base al relativo nome o GUID. |
| `splitMode` | Facoltativo | `"duplicate"` | Controlla la modalità di divisione del riquadro. Accetta solo `"duplicate"`, con cui il profilo del riquadro con lo stato attivo viene duplicato in un nuovo riquadro. |

<br />

___

## <a name="clipboard-integration-commands"></a>Comandi di integrazione degli Appunti

### <a name="copy"></a>Copia

Copia il contenuto del terminale selezionato negli Appunti.

**Nome del comando:** `copy`

**Associazioni predefinite:**

```json
// In settings.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+c" },

// In defaults.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+shift+c" },
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+insert" }
```

#### <a name="clipboard-actions"></a>Azioni degli Appunti

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `singleLine` | Facoltativo | `true`, `false` | Quando è `true`, il contenuto copiato verrà copiato come una riga singola. Quando è `false`, i caratteri di nuova riga del testo selezionato vengono mantenuti. |

### <a name="paste"></a>Incolla

Inserisce il contenuto copiato negli Appunti.

**Nome del comando:** `paste`

**Associazioni predefinite:**

```json
// In settings.json
{ "command": "paste", "keys": "ctrl+v" },

// In defaults.json
{ "command": "paste", "keys": "ctrl+shift+v" },
{ "command": "paste", "keys": "shift+insert" }
```

<br />

___

## <a name="scrollback-commands"></a>Comandi di scorrimento

### <a name="scroll-up"></a>Scorri verso l'alto

Scorre lo schermo verso l'alto.

**Nome del comando:** `scrollUp`

**Associazione predefinita:**

```json
{ "command": "scrollUp", "keys": "ctrl+shift+up" }
```

### <a name="scroll-down"></a>Scorri verso il basso

Scorre lo schermo verso il basso.

**Nome del comando:** `scrollDown`

**Associazione predefinita:**

```json
{ "command": "scrollDown", "keys": "ctrl+shift+down" }
```

### <a name="scroll-up-a-whole-page"></a>Scorri verso l'alto di una pagina intera

Scorre lo schermo verso l'alto di una pagina intera, che corrisponde all'altezza della finestra.

**Nome del comando:** `scrollUpPage`

**Associazione predefinita:**

```json
{ "command": "scrollUpPage", "keys": "ctrl+shift+pgup" }
```

### <a name="scroll-down-a-whole-page"></a>Scorri verso il basso di una pagina intera

Scorre lo schermo verso il basso di una pagina intera, che corrisponde all'altezza della finestra.

**Nome del comando:** `scrollDownPage`

**Associazione predefinita:**

```json
{ "command": "scrollDownPage", "keys": "ctrl+shift+pgdn" }
```

<br />

___

## <a name="visual-adjustment-commands"></a>Comandi di regolazione della visualizzazione

### <a name="adjust-font-size"></a>Regola dimensioni caratteri

Modifica le dimensioni del testo in base al numero di punti specificato.

**Nome del comando:** `adjustFontSize`

**Associazioni predefinite:**

```json
{ "command": { "action": "adjustFontSize", "delta": 1 }, "keys": "ctrl+=" },
{ "command": { "action": "adjustFontSize", "delta": -1 }, "keys": "ctrl+-" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `delta` | Obbligatoria | Intero | Modifiche applicate alle dimensioni per ogni chiamata del comando. |

### <a name="reset-font-size"></a>Reimposta dimensioni del carattere

Reimposta le dimensioni del testo in base al valore predefinito.

**Nome del comando:** `resetFontSize`

**Associazione predefinita:**

```json
{ "command": "resetFontSize", "keys": "ctrl+0" }
```

<br />

___

## <a name="unbind-keys"></a>Disassocia tasti

Annulla l'associazione dei tasti per tutti i comandi.

**Nome del comando:** `unbound`
