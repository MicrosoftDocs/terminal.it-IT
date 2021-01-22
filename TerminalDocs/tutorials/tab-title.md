---
title: Terminale Windows - Configurazione del titolo delle schede
description: Questa esercitazione illustra come configurare il titolo delle schede in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.openlocfilehash: a127b1be1dc3592568db9abd1027555bf38f349c
ms.sourcegitcommit: 8e0901b83a8cc437f090fe58688b86acb73f3cb3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "90988756"
---
# <a name="tutorial-configure-tab-titles-in-windows-terminal"></a>Esercitazione: Configurare i titoli delle schede in Terminale Windows

Per impostazione predefinita, il titolo della scheda è impostato sul titolo della shell. Se una scheda è composta da più riquadri, il titolo della scheda viene impostato su quello del riquadro attualmente attivo. Se vuoi personalizzare il titolo della scheda, segui questa esercitazione.

In questa esercitazione verranno illustrate le procedure per:

> [!div class="checklist"]
> * Usare l'impostazione `tabTitle`
> * Impostare il titolo della shell
> * Uso dell'impostazione `suppressApplicationTitle`

## <a name="use-the-tabtitle-setting"></a>Usare l'impostazione `tabTitle`

L'impostazione `tabTitle` consente di definire il titolo iniziale di una nuova istanza di una shell. Se non è impostata, viene usata l'impostazione `name` del profilo. Ogni shell risponde a questa impostazione in modo diverso.

| Shell | Comportamento |
| ----- | -------- |
| PowerShell | Il titolo viene impostato. |
| Prompt dei comandi | Il titolo viene impostato. Un eventuale comando in esecuzione viene aggiunto temporaneamente alla fine del titolo. |
| Ubuntu | Il titolo viene ignorato e viene invece impostato su `user@machine:path` |
| Debian | Il titolo viene impostato. |

> [!NOTE]
> Anche se Ubuntu e Debian eseguono entrambi bash, hanno comportamenti diversi. Questo consente di illustrare che i comportamenti variano a seconda delle distribuzioni.

## <a name="set-the-shells-title"></a>Impostare il titolo della shell

Una shell ha controllo completo sul proprio titolo, ma ogni shell imposta il titolo in modo diverso.

| Shell | Comando |
| ----- | ------- |
| PowerShell | `$Host.UI.RawUI.WindowTitle = "New Title"` |
| Prompt dei comandi | `TITLE "New Title"` |
| bash* | `echo -ne "\033]0;New Title\a"` |

Tieni presente che alcune distribuzioni di Linux, ad esempio Ubuntu, impostano automaticamente il titolo mentre interagisci con la shell. Se il comando precedente non funziona, esegui il comando seguente:

```bash
PS1=$
PROMPT_COMMAND=
echo -ne "\033]0;New Title\a"
```

Il titolo verrà modificato in 'New Title' e il prompt verrà impostato su '$'.

## <a name="use-the-suppressapplicationtitle-setting"></a>Usare l'impostazione `suppressApplicationTitle`

Dal momento che una shell può controllare il proprio titolo, può scegliere di sovrascrivere il titolo della scheda in qualsiasi momento. Il modulo `posh-git` per PowerShell, ad esempio, aggiunge al titolo informazioni sul repository GIT.

In Terminale Windows puoi disattivare le modifiche apportate al titolo impostando `suppressApplicationTitle` su `true` nel profilo. In questo modo le nuove istanze del profilo impostano il titolo visibile su `tabTitle`. Se `tabTitle` non è impostata, il titolo visibile viene impostato sul valore di `name` del profilo.

Questo comportamento consente di scollegare il titolo della shell dal titolo visibile indicato sulla scheda. Se esamini la variabile della shell in cui è impostato il titolo, noterai che potrebbe essere diversa dal titolo della scheda.

## <a name="resources"></a>Risorse

* [Impostazione del titolo della console come directory di lavoro corrente](https://devblogs.microsoft.com/powershell/setting-the-console-title-to-be-your-current-working-directory/)
* [Modificare il titolo di un terminale in Ubuntu 16.04](https://www.zachpfeffer.com/single-post/Change-the-title-of-a-terminal-on-Ubuntu-1604)
