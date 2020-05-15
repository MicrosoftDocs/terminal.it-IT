---
title: Riquadri di Terminale Windows
description: Informazioni su come dividere i riquadri in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.openlocfilehash: 5d13d48d8e9317c229720937f916f57769da7261
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416306"
---
# <a name="panes-in-windows-terminal"></a>Riquadri in Terminale Windows

I riquadri offrono la possibilità di eseguire più applicazioni da riga di comando una accanto all'altra all'interno della stessa scheda. Questa opzione riduce la necessità di spostarsi tra schede e ti consente di vedere più prompt contemporaneamente.

## <a name="creating-a-new-pane"></a>Creazione di un nuovo riquadro

In Terminale Windows puoi creare un nuovo riquadro verticale o orizzontale. La divisione in verticale apre un nuovo riquadro a destra di quello con lo stato attivo, mentre la divisione in orizzontale ne apre uno nuovo sotto quello con lo stato attivo. Per creare un nuovo riquadro verticale del profilo predefinito, premi <kbd>ALT+MAIUSC++</kbd>. Per creare un riquadro orizzontale del profilo predefinito, premi <kbd>ALT+MAIUSC+-</kbd>.

![Creazione di riquadri di Terminale Windows](./images/open-panes.gif)
_Configurazione: [Raspberry Ubuntu](./custom-terminal-gallery/raspberry-ubuntu.md)_

Per cambiare queste combinazioni di tasti, puoi crearne altre usando l'azione `splitPane` e i valori `vertical` o `horizontal` per la proprietà `split` nel file profiles.json. Per avere un unico riquadro con la quantità massima di area disponibile, imposta `split` su `auto`. Per altre informazioni, vedi la [pagina sulle combinazioni di tasti](./customize-settings/key-bindings.md).

```json
{ "command": { "action": "splitPane", "split": "vertical" }, "keys": "alt+shift+plus" },
{ "command": { "action": "splitPane", "split": "horizontal" }, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "auto" }, "keys": "alt+shift+|" }
```

## <a name="switching-between-panes"></a>Passaggio tra riquadri

Il terminale ti consente di spostarti tra i riquadri usando la tastiera. Se tieni premuto <kbd>ALT</kbd>, puoi usare i tasti di direzione per spostare lo stato attivo tra i riquadri. Il riquadro con lo stato attivo è identificabile dal colore in risalto del bordo che lo circonda. Questo colore è configurato nelle impostazioni dei colori di Windows.

![Passaggio tra i riquadri di Terminale Windows](./images/navigate-panes.gif)

Puoi personalizzare questa impostazione aggiungendo combinazioni di tasti per il comando `moveFocus` e impostando `direction` su `down`, `left`, `right` o `up`.

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

## <a name="resizing-a-pane"></a>Ridimensionamento di un riquadro

Per modificare le dimensioni dei riquadri, tieni premuto <kbd>ALT+MAIUSC</kbd> e usa i tasti di direzione per ridimensionare il riquadro con lo stato attivo.

![Creazione di riquadri di Terminale Windows](./images/resize-panes.gif)

Per personalizzare questa combinazione di tasti, puoi aggiungerne altre usando l'azione `resizePane` e impostando `direction` su `down`, `left`, `right` o `up`.

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

## <a name="closing-a-pane"></a>Chiusura di un riquadro

Per chiudere il riquadro con lo stato attivo, premi <kbd>CTRL+MAIUSC+W</kbd>. Se è aperto un solo riquadro, <kbd>CTRL+MAIUSC+W</kbd> chiuderà la scheda. Come sempre, chiudendo l'ultima scheda si chiuderà la finestra.

![Chiusura dei riquadri di Terminale Windows](./images/close-panes.gif)

Puoi cambiare i tasti di chiusura del riquadro aggiungendo una combinazione che usa il comando `closePane`.

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

## <a name="customizing-panes-using-key-bindings"></a>Personalizzazione dei riquadri con le combinazioni di tasti

Puoi personalizzare cosa aprire all'interno di un nuovo riquadro a seconda delle combinazioni di tasti personalizzate.

### <a name="duplicating-a-pane"></a>Duplicazione di un riquadro

Il terminale ti consente di duplicare il profilo del riquadro con lo stato attivo in un altro riquadro.

![Riquadri duplicati in Terminale di Windows](./images/duplicate-panes.gif)

A questo scopo, aggiungi la proprietà `splitMode` con `duplicate` come valore a una combinazione di tasti `splitPane`.

```json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" }
```

### <a name="new-terminal-arguments"></a>Nuovi argomenti del terminale

[!INCLUDE [new-terminal-arguments](./new-terminal-arguments.md)]
