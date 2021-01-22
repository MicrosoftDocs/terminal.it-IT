---
title: Nuovi argomenti del terminale in Terminale Windows
description: Nuovi argomenti del terminale in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 08/26/2020
ms.topic: include
ms.openlocfilehash: e88bb61f2e832f2671ad3a743a3c541e39816bd9
ms.sourcegitcommit: 8e0901b83a8cc437f090fe58688b86acb73f3cb3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "90988530"
---
### <a name="new-terminal-arguments"></a>Nuovi argomenti del terminale

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
