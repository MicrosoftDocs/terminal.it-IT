---
title: Azioni del terminale di Windows
description: Informazioni su come creare azioni personalizzate per il terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 11/11/2020
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 31ba6ab95ffc9c55808cb85ba97651dff19076d2
ms.sourcegitcommit: 9a2f9d152f65cdc8106fb9aad7fa69b01f3d05db
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/11/2020
ms.locfileid: "94520283"
---
# <a name="custom-actions-in-windows-terminal"></a>Azioni personalizzate nel terminale di Windows

> [!IMPORTANT]
> A partire dalla versione 1,4 del terminale di Windows, la `keybindings` matrice è stata rinominata all' `actions` interno del settings.jssu file. Il supporto per la `keybindings` matrice esiste ancora per la compatibilità con le versioni precedenti, ma il terminale non verrà rinominato automaticamente all' `keybindings` interno del `actions` settings.jssu file.

È possibile creare azioni personalizzate all'interno del terminale di Windows che consentono di controllare la modalità di interazione con il terminale. Queste azioni verranno aggiunte automaticamente al riquadro comandi.

## <a name="action-formats"></a>Formati di azione

Le azioni possono essere strutturate nei formati seguenti:

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

## <a name="action-properties"></a>Proprietà delle azioni

Le azioni possono essere costruite usando le proprietà seguenti.

### <a name="command"></a>Comando

Comando eseguito quando vengono premuti i tasti associati.

**Nome della proprietà:** `command`

**Obbligatoria:** Obbligatoria

**Accetta:** String

### <a name="keys"></a>Tasti

Definisce le combinazioni di tasti usate per chiamare il comando. Con la proprietà keys è possibile associare più modificatori a un unico tasto. I tasti e i modificatori accettati sono elencati [di seguito](#accepted-modifiers-and-keys).

Se l'azione non dispone di chiavi, verrà visualizzata nel riquadro comandi, ma non potrà essere richiamata con la tastiera.

**Nome della proprietà:** `keys`

**Obbligatoria:** Facoltativo

**Accetta:** stringa o matrice[stringa]

### <a name="action"></a>Azione

Aggiunge funzionalità aggiuntive a determinati comandi.

**Nome della proprietà:** `action`

**Obbligatoria:** Facoltativo

**Accetta:** String

### <a name="name"></a>Nome

Questo consente di impostare il nome che verrà visualizzato nel riquadro comandi. Se non ne viene specificato uno, il terminale tenterà di generare automaticamente un nome.

**Nome della proprietà:** `name`

**Necessità**: facoltativo

**Accetta:** String

### <a name="icon"></a>Icona

Questa operazione consente di impostare l'icona visualizzata all'interno del riquadro comandi.

**Nome della proprietà:** `icon`

**Obbligatoria:** Facoltativo

**Accetta:** Percorso del file sotto forma di stringa o emoji

<br />

___

## <a name="accepted-modifiers-and-keys"></a>Tasti e modificatori accettati

### <a name="modifiers"></a>Modificatori

`ctrl+`, `shift+`, `alt+`

> [!NOTE]
> La `Windows` chiave non è supportata come modificatore. 

### <a name="modifier-keys"></a>Tasti di modifica

| Type | Tasti |
| ---- | ---- |
| Tasti funzione e alfanumerici | `f1-f24`, `a-z`, `0-9` |
| Simboli | ``` ` ```, `plus`, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/` |
| Tasti di direzione | `down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home` |
| Tasti di azione | `tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`, `app`, `menu`  |
| Tasti del tastierino numerico | `numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply` |

**Nota:** `=` e `plus` sono equivalenti. Il secondo non deve essere confuso con `numpad_plus` .

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

### <a name="toggle-full-screen"></a>Attiva/Disattiva schermo intero

Consente di passare dalla finestra a schermo intero a quella con dimensioni predefinite e viceversa.

**Nome del comando:** `toggleFullscreen`

**Associazioni predefinite:**

```json
{ "command": "toggleFullscreen", "keys": "alt+enter" },
{ "command": "toggleFullscreen", "keys": "f11" }
```

### <a name="toggle-focus-mode"></a>Attiva/Nascondi modalità messa a fuoco

Questo consente di attivare la modalità messa a fuoco, che nasconde le schede e la barra del titolo.

**Nome del comando:** `toggleFocusMode`

**Associazioni predefinite:**

```json
{ "command": "toggleFocusMode" }
```

### <a name="toggle-always-on-top-mode"></a>Attiva/Nascondi sempre in modalità principale

In questo modo è possibile impostare lo stato "always on top" della finestra. Quando si usa la modalità "always on top", la finestra verrà visualizzata nella parte superiore di tutte le altre finestre non in primo piano.

**Nome del comando:** `toggleAlwaysOnTop`

**Associazioni predefinite:**

```json
{ "command": "toggleAlwaysOnTop" }
```

### <a name="send-input"></a>Invia input

Inviare input di testo arbitrario alla Shell.
Ad esempio, l'input `"text\n"` scriverà "testo" seguito da una nuova riga nella shell.

È possibile usare le sequenze di escape ANSI, ma i codici `\x1b` di escape come devono essere scritti come `\u001b` .
Ad esempio `"\u001b[A"` , si comporterà come se fosse stato premuto il pulsante freccia su.

**Nome del comando:** `sendInput`

**Associazioni predefinite:**

_Questo comando non è attualmente associato alle impostazioni predefinite_.

```json
{ "command": { "action": "sendInput", "input": "\u001b[A" }, "keys": "" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `input` | Obbligatoria | string | Input di testo da inserire nella shell. |

<br />

___

## <a name="tab-management-commands"></a>Comandi per la gestione delle schede

### <a name="close-tab"></a>Chiudi scheda

Chiude la scheda corrente.

**Nome del comando:** `closeTab`

### <a name="close-all-other-tabs"></a>Chiudi tutte le altre schede

In questo modo vengono chiuse tutte le schede ad eccezione di quella in corrispondenza di un indice. Se non viene specificato alcun indice, usare l'indice della scheda con lo stato attivo.

**Nome del comando:** `closeOtherTabs`

**Associazione predefinita:**

```json
{ "command": "closeOtherTabs" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `index` | Facoltativo | Intero | Posizione della scheda da mantenere aperta. |

### <a name="close-tabs-after-index"></a>Chiudi tabulazioni dopo l'indice

Questa operazione chiude le schede che seguono la scheda in corrispondenza di un indice. Se non viene specificato alcun indice, usare l'indice della scheda con lo stato attivo.

**Nome del comando:** `closeTabsAfter`

**Associazione predefinita:**

```json
{ "command": "closeTabsAfter" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `index` | Facoltativo | Intero | Posizione dell'ultima scheda da mantenere aperta. |

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
| `commandline` | Facoltativo | Nome del file eseguibile in formato stringa | Esegue l'eseguibile all'interno della scheda. |
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

### <a name="tab-search"></a>Ricerca nella scheda

:::row:::
:::column span="":::
Verrà visualizzata la casella di ricerca della scheda.

**Nome del comando:** `tabSearch`

**Associazione predefinita:**

_Questo comando non è attualmente associato alle impostazioni predefinite_.

```json
{"command": "tabSearch", "keys": ""}
```

:::column-end:::
:::column span="":::
![Ricerca nella scheda terminale di Windows](./../images/tab-search.gif)

:::column-end:::
:::row-end:::

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

### <a name="rename-tab"></a>Rinomina scheda

Questo comando può essere usato per rinominare una scheda in una stringa specifica.

**Nome del comando:** `renameTab`

**Associazione predefinita:**

_Questo comando non è attualmente associato alle impostazioni predefinite_.

```json
// Rename a tab to "Foo"
{ "command": { "action": "renameTab", "title": "Foo" }, "keys": "" }

// Reset the tab's name
{ "command": { "action": "renameTab", "title": null }, "keys": "" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `title` | Facoltativo | String | Nuovo titolo da utilizzare per questa scheda. Se omesso, il comando ripristinerà nuovamente il titolo della scheda al valore originale. |

### <a name="open-tab-rename-text-box-preview"></a>Apri ridenominazione tabulazione casella di testo ([Anteprima](https://aka.ms/terminal-preview))

Questo comando modifica il titolo della scheda in un campo di testo che consente di modificare il titolo per la scheda corrente. Se si deseleziona il campo di testo, il titolo della scheda viene reimpostato sul valore predefinito per l'istanza corrente della shell.

**Nome del comando:** `openTabRenamer`

**Associazione predefinita:**

_Questo comando non è attualmente associato alle impostazioni predefinite_.

```json
{ "command": "openTabRenamer", "keys": "ctrl+alt+a" }
```

> [!IMPORTANT]
> Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).

### <a name="change-tab-color"></a>Cambia colore scheda

Questo comando può essere usato per modificare il colore di una scheda in un valore specifico.

**Nome del comando:** `setTabColor`

**Associazione predefinita:**

_Questo comando non è attualmente associato alle impostazioni predefinite_.

```json
// Change the tab's color to a bright magenta
{ "command": { "action": "setTabColor", "color": "#ff00ff" }, "keys": "" }

// Reset the tab's color
{ "command": { "action": "setTabColor", "color": null }, "keys": "" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `color` | Facoltativo | Stringa, in formato esadecimale: `"#rgb"` o `"#rrggbb"` | Nuovo colore da usare per questa scheda. Se omesso, il comando ripristinerà il colore della scheda al valore originale. |

### <a name="open-tab-color-picker"></a>Apri selezione colori scheda

Questo comando può essere usato per aprire la selezione colori per la scheda attiva. La selezione colori può essere usata per impostare un colore per la scheda in fase di esecuzione.

**Nome del comando:** `openTabColorPicker`

**Associazione predefinita:**

```json
{ "command": "openTabColorPicker" }
```

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

### <a name="zoom-a-pane-preview"></a>Zoom di un riquadro ([Anteprima](https://aka.ms/terminal-preview))

:::row:::
:::column span="":::
In questo modo si espande il riquadro con lo stato attivo per riempire l'intero contenuto della finestra.

**Nome del comando:** `togglePaneZoom`

**Associazione predefinita:**

```json
{ "command": "togglePaneZoom" }
```

:::column-end:::
:::column span="":::
![Zoom del riquadro di attivazione/disconnessione del terminale di Windows](./../images/toggle-pane-zoom.gif)

:::column-end:::
:::row-end:::

> [!IMPORTANT]
> Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).

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
| `commandline` | Facoltativo | Nome del file eseguibile in formato stringa | Esegue l'eseguibile all'interno del riquadro. |
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

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `singleLine` | Facoltativo | `true`, `false` | Quando è `true`, il contenuto copiato verrà copiato come una riga singola. Quando è `false`, i caratteri di nuova riga del testo selezionato vengono mantenuti. |
| `copyFormatting` | Facoltativo | `true`, `false`, `"all"`, `"none"`, `"html"`, `"rtf"` | Quando `true` , anche il colore e la formattazione dei caratteri del testo selezionato vengono copiati negli Appunti. Quando `false` , solo il testo normale viene copiato negli Appunti. È inoltre possibile specificare i formati che si desidera copiare. Se `null` , il `"copyFormatting"` comportamento globale viene ereditato. |

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

Scorre lo schermo verso l'alto in base al numero di righe definito da `"rowsToScroll"` . Se `"rowsToScroll"` non viene specificato, scorrerà verso l'alto la quantità definita dall'impostazione predefinita del sistema, ovvero la stessa quantità di scorrimento del mouse.

**Nome del comando:** `scrollUp`

**Associazione predefinita:**

```json
{ "command": "scrollUp", "keys": "ctrl+shift+up" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `rowsToScroll` | Facoltativo | Intero | Numero di righe da scorrere. |

> [!IMPORTANT]
> L' `"rowsToScroll"` azione è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).

### <a name="scroll-down"></a>Scorri verso il basso

Scorre lo schermo verso il basso in base al numero di righe definito da `"rowsToScroll"` . Se `"rowsToScroll"` non viene specificato, scorre verso il basso la quantità definita dall'impostazione predefinita del sistema, che corrisponde allo scorrimento del mouse.

**Nome del comando:** `scrollDown`

**Associazione predefinita:**

```json
{ "command": "scrollDown", "keys": "ctrl+shift+down" }
```

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `rowsToScroll` | Facoltativo | Intero | Numero di righe da scorrere. |

> [!IMPORTANT]
> L' `"rowsToScroll"` azione è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).

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

### <a name="toggle-retro-terminal-effects"></a>Imposta/Rimuovi effetti terminali retro

Questo consente di attivare o disabilitare il "effetto terminale retrò", che è abilitato con l'impostazione del profilo `experimental.retroTerminalEffect` .

**Nome del comando:** `toggleRetroEffect`

**Associazione predefinita:**

```json
{ "command": "toggleRetroEffect" }
```

### <a name="set-the-color-scheme"></a>Imposta la combinazione di colori

Modifica la combinazione di colori attiva.

**Nome del comando:** `setColorScheme`

#### <a name="actions"></a>Azioni

| Nome | Obbligatoria | Tipo accettato | Description |
| ---- | --------- | ------- | ----------- |
| `colorScheme` | Obbligatoria | string | Oggetto `name` della combinazione di colori da applicare. |

**Associazione di esempio:**

```json
{ "command": { "action": "setColorScheme", "colorScheme": "Campbell" }, "keys": "" }
```

<br />

___

## <a name="unbind-keys"></a>Disassocia tasti

Annulla l'associazione dei tasti per tutti i comandi.

**Nome del comando:** `unbound`
