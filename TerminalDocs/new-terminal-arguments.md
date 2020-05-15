---
title: Nuovi argomenti del terminale in Terminale Windows
description: Nuovi argomenti del terminale in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: include
ms.service: terminal
ms.openlocfilehash: 4430124e3f9319e79cbf7b097d8743543c1d52a6
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416316"
---
# <a name="new-terminal-arguments-in-the-windows-terminal"></a>Nuovi argomenti del terminale in Terminale Windows

Quando apri un nuovo riquadro o una nuova scheda con una combinazione di tasti, puoi specificare quale profilo usare includendo il relativo nome, il GUID o l'indice. Se non lo specifichi, verrà usato il profilo predefinito. A questo scopo, aggiungi `profile` o `index` come argomento a una combinazione di tasti `splitPane` o `newTab`. Tieni presente che l'indicizzazione inizia da 0.

```json
{ "command": { "action": "splitPane", "split": "vertical", "profile": "profile1" }, "keys": "ctrl+a" },
{ "command": { "action": "splitPane", "split": "vertical", "profile": "{00000000-0000-0000-0000-000000000000}" }, "keys": "ctrl+b" },
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+c" }
```

Inoltre, puoi sostituire determinati aspetti del profilo, ad esempio l'eseguibile della riga di comando, la directory iniziale o il titolo della scheda. A questo scopo, aggiungi `commandline`, `startingDirectory` e/o `tabTitle` a una combinazione di tasti `splitPane` o `newTab`.

```json
{ "command": { "action": "splitPane", "split": "auto", "profile": "profile1", "commandline": "foo.exe" }, "keys": "ctrl+a" },
{ "command": { "action": "newTab", "profile": "{00000000-0000-0000-0000-000000000000}", "startingDirectory": "C:\\foo" }, "keys": "ctrl+b" },
{ "command": { "action": "newTab", "index": 0, "tabTitle": "bar", "startingDirectory": "C:\\foo", "commandline": "foo.exe" }, "keys": "ctrl+c" }
```
