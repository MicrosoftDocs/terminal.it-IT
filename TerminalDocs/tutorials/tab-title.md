---
title: Terminale Windows - Configurazione del titolo delle schede
description: Questa esercitazione illustra come configurare il titolo delle schede in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: 94c0d9afc8ccd3d95a3f52f5f9f6bdd0cb05bc12
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416466"
---
# <a name="tutorial-configure-tab-titles-in-windows-terminal"></a><span data-ttu-id="8ae68-103">Esercitazione: Configurare i titoli delle schede in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="8ae68-103">Tutorial: Configure tab titles in Windows Terminal</span></span>

<span data-ttu-id="8ae68-104">Per impostazione predefinita, il titolo della scheda è impostato sul titolo della shell.</span><span class="sxs-lookup"><span data-stu-id="8ae68-104">By default, the tab title is set to the shell's title.</span></span> <span data-ttu-id="8ae68-105">Se una scheda è composta da più riquadri, il titolo della scheda viene impostato su quello del riquadro attualmente attivo.</span><span class="sxs-lookup"><span data-stu-id="8ae68-105">If a tab is composed of multiple panes, the tab's title is set to that of the currently focused pane.</span></span> <span data-ttu-id="8ae68-106">Se vuoi personalizzare il titolo della scheda, segui questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="8ae68-106">If you want to customize what is set as the tab title, follow this tutorial.</span></span>

<span data-ttu-id="8ae68-107">In questa esercitazione verranno illustrate le procedure per:</span><span class="sxs-lookup"><span data-stu-id="8ae68-107">In this tutorial, you learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="8ae68-108">Usare l'impostazione `tabTitle`</span><span class="sxs-lookup"><span data-stu-id="8ae68-108">Use the `tabTitle` setting</span></span>
> * <span data-ttu-id="8ae68-109">Impostare il titolo della shell</span><span class="sxs-lookup"><span data-stu-id="8ae68-109">Set the shell's title</span></span>
> * <span data-ttu-id="8ae68-110">Uso dell'impostazione `suppressApplicationTitle`</span><span class="sxs-lookup"><span data-stu-id="8ae68-110">Using the `suppressApplicationTitle` setting</span></span>

## <a name="use-the-tabtitle-setting"></a><span data-ttu-id="8ae68-111">Usare l'impostazione `tabTitle`</span><span class="sxs-lookup"><span data-stu-id="8ae68-111">Use the `tabTitle` setting</span></span>

<span data-ttu-id="8ae68-112">L'impostazione `tabTitle` consente di definire il titolo iniziale di una nuova istanza di una shell.</span><span class="sxs-lookup"><span data-stu-id="8ae68-112">The `tabTitle` setting allows you to define the starting title for a new instance of a shell.</span></span> <span data-ttu-id="8ae68-113">Se non è impostata, viene usata l'impostazione `name` del profilo.</span><span class="sxs-lookup"><span data-stu-id="8ae68-113">If it is not set, the profile `name` is used instead.</span></span> <span data-ttu-id="8ae68-114">Ogni shell risponde a questa impostazione in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="8ae68-114">Each shell responds to this setting differently.</span></span>

| <span data-ttu-id="8ae68-115">Shell</span><span class="sxs-lookup"><span data-stu-id="8ae68-115">Shell</span></span> | <span data-ttu-id="8ae68-116">Comportamento</span><span class="sxs-lookup"><span data-stu-id="8ae68-116">Behavior</span></span> |
| ----- | -------- |
| <span data-ttu-id="8ae68-117">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ae68-117">PowerShell</span></span> | <span data-ttu-id="8ae68-118">Il titolo viene impostato.</span><span class="sxs-lookup"><span data-stu-id="8ae68-118">The title is set.</span></span> |
| <span data-ttu-id="8ae68-119">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="8ae68-119">Command Prompt</span></span> | <span data-ttu-id="8ae68-120">Il titolo viene impostato.</span><span class="sxs-lookup"><span data-stu-id="8ae68-120">The title is set.</span></span> <span data-ttu-id="8ae68-121">Un eventuale comando in esecuzione viene aggiunto temporaneamente alla fine del titolo.</span><span class="sxs-lookup"><span data-stu-id="8ae68-121">If a command is running, it is temporarily appended to the end of the title.</span></span> |
| <span data-ttu-id="8ae68-122">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="8ae68-122">Ubuntu</span></span> | <span data-ttu-id="8ae68-123">Il titolo viene ignorato e viene invece impostato su `user@machine:path`</span><span class="sxs-lookup"><span data-stu-id="8ae68-123">The title is ignored, and instead set to `user@machine:path`</span></span> |
| <span data-ttu-id="8ae68-124">Debian</span><span class="sxs-lookup"><span data-stu-id="8ae68-124">Debian</span></span> | <span data-ttu-id="8ae68-125">Il titolo viene impostato.</span><span class="sxs-lookup"><span data-stu-id="8ae68-125">The title is set.</span></span> |

> [!NOTE]
> <span data-ttu-id="8ae68-126">Anche se Ubuntu e Debian eseguono entrambi bash, hanno comportamenti diversi.</span><span class="sxs-lookup"><span data-stu-id="8ae68-126">Though Ubuntu and Debian both run bash, they have different behaviors.</span></span> <span data-ttu-id="8ae68-127">Questo consente di illustrare che i comportamenti variano a seconda delle distribuzioni.</span><span class="sxs-lookup"><span data-stu-id="8ae68-127">This is to show that different distributions may have different behaviors.</span></span>

## <a name="set-the-shells-title"></a><span data-ttu-id="8ae68-128">Impostare il titolo della shell</span><span class="sxs-lookup"><span data-stu-id="8ae68-128">Set the shell's title</span></span>

<span data-ttu-id="8ae68-129">Una shell ha controllo completo sul proprio titolo,</span><span class="sxs-lookup"><span data-stu-id="8ae68-129">A shell has full control over its own title.</span></span> <span data-ttu-id="8ae68-130">ma ogni shell imposta il titolo in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="8ae68-130">However, each shell sets its title differently.</span></span>

| <span data-ttu-id="8ae68-131">Shell</span><span class="sxs-lookup"><span data-stu-id="8ae68-131">Shell</span></span> | <span data-ttu-id="8ae68-132">Comando</span><span class="sxs-lookup"><span data-stu-id="8ae68-132">Command</span></span> |
| ----- | ------- |
| <span data-ttu-id="8ae68-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ae68-133">PowerShell</span></span> | `$Host.UI.RawUI.WindowTitle = "New Title"` |
| <span data-ttu-id="8ae68-134">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="8ae68-134">Command Prompt</span></span> | `TITLE "New Title"` |
| <span data-ttu-id="8ae68-135">bash\*</span><span class="sxs-lookup"><span data-stu-id="8ae68-135">bash\*</span></span> | `echo -ne "\033]0;New Title\a"` |

<span data-ttu-id="8ae68-136">Tieni presente che alcune distribuzioni di Linux, ad esempio Ubuntu, impostano automaticamente il titolo mentre interagisci con la shell.</span><span class="sxs-lookup"><span data-stu-id="8ae68-136">Note that some Linux distributions (i.e. Ubuntu) set their title automatically as you interact with the shell.</span></span> <span data-ttu-id="8ae68-137">Se il comando precedente non funziona, esegui il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="8ae68-137">If the above command doesn't work, run the following command:</span></span>

```bash
PS1=$
PROMPT_COMMAND=
echo -ne "\033]0;New Title\a"
```

<span data-ttu-id="8ae68-138">Il titolo verrà modificato in 'New Title' e il prompt verrà impostato su '$'.</span><span class="sxs-lookup"><span data-stu-id="8ae68-138">This will change the title to 'New Title', and also set the prompt to '$'.</span></span>

## <a name="use-the-suppressapplicationtitle-setting"></a><span data-ttu-id="8ae68-139">Usare l'impostazione `suppressApplicationTitle`</span><span class="sxs-lookup"><span data-stu-id="8ae68-139">Use the `suppressApplicationTitle` setting</span></span>

<span data-ttu-id="8ae68-140">Dal momento che una shell può controllare il proprio titolo, può scegliere di sovrascrivere il titolo della scheda in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="8ae68-140">Since a shell has control over its title, it may choose to overwrite the tab title at any time.</span></span> <span data-ttu-id="8ae68-141">Il modulo `posh-git` per PowerShell, ad esempio, aggiunge al titolo informazioni sul repository GIT.</span><span class="sxs-lookup"><span data-stu-id="8ae68-141">For example, the `posh-git` module for PowerShell adds information about your Git repository to the title.</span></span>

<span data-ttu-id="8ae68-142">In Terminale Windows puoi disattivare le modifiche apportate al titolo impostando `suppressApplicationTitle` su `true` nel profilo.</span><span class="sxs-lookup"><span data-stu-id="8ae68-142">Windows Terminal allows you to suppress changes to the title by setting `suppressApplicationTitle` to `true` in your profile.</span></span> <span data-ttu-id="8ae68-143">In questo modo le nuove istanze del profilo impostano il titolo visibile su `tabTitle`.</span><span class="sxs-lookup"><span data-stu-id="8ae68-143">This makes new instances of the profile set your visible title to `tabTitle`.</span></span> <span data-ttu-id="8ae68-144">Se `tabTitle` non è impostata, il titolo visibile viene impostato sul valore di `name` del profilo.</span><span class="sxs-lookup"><span data-stu-id="8ae68-144">If `tabTitle` is not set, the visible title is set to the profile's `name`.</span></span>

<span data-ttu-id="8ae68-145">Questo comportamento consente di scollegare il titolo della shell dal titolo visibile indicato sulla scheda. Se esamini la variabile della shell in cui è impostato il titolo, noterai che potrebbe essere diversa dal titolo della scheda.</span><span class="sxs-lookup"><span data-stu-id="8ae68-145">Note that this decouples the shell's title from the visible title presented on the tab. If you read the shell's variable where the title is set, it may differ from the tab's title.</span></span>

## <a name="resources"></a><span data-ttu-id="8ae68-146">Risorse</span><span class="sxs-lookup"><span data-stu-id="8ae68-146">Resources</span></span>

* [<span data-ttu-id="8ae68-147">Impostazione del titolo della console come directory di lavoro corrente</span><span class="sxs-lookup"><span data-stu-id="8ae68-147">Setting the console title to be your current working directory</span></span>](https://devblogs.microsoft.com/powershell/setting-the-console-title-to-be-your-current-working-directory/)
* [<span data-ttu-id="8ae68-148">Modificare il titolo di un terminale in Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="8ae68-148">Change the title of a terminal on Ubuntu 16.04</span></span>](https://www.zachpfeffer.com/single-post/Change-the-title-of-a-terminal-on-Ubuntu-1604)
