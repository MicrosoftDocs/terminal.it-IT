---
title: Installazione di Terminale Windows
description: Questo argomento di avvio rapido illustra come installare ed eseguire Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 09/22/2020
ms.topic: quickstart
ms.localizationpriority: high
ms.openlocfilehash: f8900c62bf973860c5ae9dc6600a99c18336949a
ms.sourcegitcommit: 8e0901b83a8cc437f090fe58688b86acb73f3cb3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "90988593"
---
# <a name="install-and-set-up-windows-terminal"></a><span data-ttu-id="c3a01-103">Installare e configurare Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="c3a01-103">Install and set up Windows Terminal</span></span>

## <a name="installation"></a><span data-ttu-id="c3a01-104">Installazione</span><span class="sxs-lookup"><span data-stu-id="c3a01-104">Installation</span></span>

<span data-ttu-id="c3a01-105">È possibile installare Terminale Windows da [Microsoft Store](https://aka.ms/terminal).</span><span class="sxs-lookup"><span data-stu-id="c3a01-105">You can install Windows Terminal from the [Microsoft Store](https://aka.ms/terminal).</span></span>

<span data-ttu-id="c3a01-106">Se non hai accesso a Microsoft Store, le build sono pubblicate nella [pagina di versioni in GitHub](https://github.com/microsoft/terminal/releases).</span><span class="sxs-lookup"><span data-stu-id="c3a01-106">If you don't have access to the Microsoft Store, the builds are published on the [GitHub releases page](https://github.com/microsoft/terminal/releases).</span></span> <span data-ttu-id="c3a01-107">Se esegui l'installazione da GitHub, il terminale non verrà aggiornato automaticamente alle nuove versioni.</span><span class="sxs-lookup"><span data-stu-id="c3a01-107">If you install from GitHub, the terminal will not automatically update with new versions.</span></span>

## <a name="first-run"></a><span data-ttu-id="c3a01-108">Prima esecuzione</span><span class="sxs-lookup"><span data-stu-id="c3a01-108">First run</span></span>

<span data-ttu-id="c3a01-109">Dopo l'installazione, quando apri il terminale, verrà avviato con PowerShell come profilo predefinito nella scheda aperta.</span><span class="sxs-lookup"><span data-stu-id="c3a01-109">After installation, when you open the terminal, it will start with PowerShell as the default profile in the open tab.</span></span>

![Prima esecuzione di Terminale Windows](./images/first-run.png)

### <a name="dynamic-profiles"></a><span data-ttu-id="c3a01-111">Profili dinamici</span><span class="sxs-lookup"><span data-stu-id="c3a01-111">Dynamic profiles</span></span>

<span data-ttu-id="c3a01-112">Il terminale creerà automaticamente i profili se sono installate distribuzioni WSL o più versioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c3a01-112">The terminal will automatically create profiles for you if you have WSL distros or multiple versions of PowerShell installed.</span></span> <span data-ttu-id="c3a01-113">Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="c3a01-113">Learn more about dynamic profiles on the [Dynamic profiles page](./dynamic-profiles.md).</span></span>

## <a name="open-a-new-tab"></a><span data-ttu-id="c3a01-114">Aprire una nuova scheda</span><span class="sxs-lookup"><span data-stu-id="c3a01-114">Open a new tab</span></span>

<span data-ttu-id="c3a01-115">Per aprire una nuova scheda del profilo predefinito, premi <kbd>CTRL+MAIUSC+T</kbd> oppure il segno più (+).</span><span class="sxs-lookup"><span data-stu-id="c3a01-115">You can open a new tab of the default profile by pressing <kbd>ctrl+shift+t</kbd> or by selecting the + (plus) button.</span></span> <span data-ttu-id="c3a01-116">Per aprire un profilo diverso, seleziona la freccia (˅) accanto a + per visualizzare il menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="c3a01-116">To open a different profile, select the ˅ (arrow) next to the + button to open the dropdown menu.</span></span> <span data-ttu-id="c3a01-117">Da qui puoi selezionare il profilo da aprire.</span><span class="sxs-lookup"><span data-stu-id="c3a01-117">From there, you can select which profile to open.</span></span>

## <a name="open-a-new-pane"></a><span data-ttu-id="c3a01-118">Aprire un nuovo riquadro</span><span class="sxs-lookup"><span data-stu-id="c3a01-118">Open a new pane</span></span>

<span data-ttu-id="c3a01-119">Puoi eseguire più shell affiancate usando i riquadri.</span><span class="sxs-lookup"><span data-stu-id="c3a01-119">You can run multiple shells side-by-side using panes.</span></span> <span data-ttu-id="c3a01-120">Per aprire un riquadro, è possibile utilizzare <kbd>ALT + MAIUSC + più</kbd> per un riquadro verticale o <kbd>ALT + MAIUSC + meno</kbd> per uno orizzontale.</span><span class="sxs-lookup"><span data-stu-id="c3a01-120">To open a pane, you can use <kbd>alt+shift+plus</kbd> for a vertical pane or <kbd>alt+shift+minus</kbd> for a horizontal one.</span></span> <span data-ttu-id="c3a01-121">È inoltre possibile utilizzare <kbd>ALT + MAIUSC + d</kbd> per aprire un riquadro duplicato del profilo con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="c3a01-121">You can also use <kbd>alt+shift+d</kbd> to open a duplicate pane of your focused profile.</span></span> <span data-ttu-id="c3a01-122">Per altre informazioni sui riquadri, vedi la [pagina Riquadri](./panes.md).</span><span class="sxs-lookup"><span data-stu-id="c3a01-122">Learn more about panes on the [Panes page](./panes.md).</span></span>

## <a name="configuration"></a><span data-ttu-id="c3a01-123">Configurazione</span><span class="sxs-lookup"><span data-stu-id="c3a01-123">Configuration</span></span>

<span data-ttu-id="c3a01-124">Per personalizzare le impostazioni di Terminale Windows, scegli **Impostazioni** dal menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="c3a01-124">To customize the settings of your Windows Terminal, select **Settings** in the dropdown menu.</span></span> <span data-ttu-id="c3a01-125">Verrà aperto il file `settings.json` nell'editor di testo predefinito.</span><span class="sxs-lookup"><span data-stu-id="c3a01-125">This will open the `settings.json` file in your default text editor.</span></span> <span data-ttu-id="c3a01-126">L'editor di testo predefinito viene definito nelle[impostazioni di Windows](ms-settings:defaultapps).</span><span class="sxs-lookup"><span data-stu-id="c3a01-126">(The default text editor is defined in your [Windows settings](ms-settings:defaultapps).)</span></span>

<span data-ttu-id="c3a01-127">Il terminale supporta la personalizzazione delle [proprietà globali](./customize-settings/global-settings.md) che interessano l'intera applicazione, le [proprietà del profilo](./customize-settings/profile-settings.md) che influiscono sulle impostazioni di ogni profilo e le [azioni](./customize-settings/actions.md) che consentono di interagire con il terminale usando la tastiera o il riquadro comandi.</span><span class="sxs-lookup"><span data-stu-id="c3a01-127">The terminal supports customization of [global properties](./customize-settings/global-settings.md) that affect the whole application, [profile properties](./customize-settings/profile-settings.md) that affect the settings of each profile, and [actions](./customize-settings/actions.md) that allow you to interact with the terminal using your keyboard or the command palette.</span></span>

## <a name="command-line-arguments"></a><span data-ttu-id="c3a01-128">Argomenti della riga di comando</span><span class="sxs-lookup"><span data-stu-id="c3a01-128">Command line arguments</span></span>

<span data-ttu-id="c3a01-129">Per avviare Terminale Windows in una specifica configurazione, puoi usare gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c3a01-129">You can launch the terminal in a specific configuration using command line arguments.</span></span> <span data-ttu-id="c3a01-130">Questi argomenti ti consentono di aprire il terminale con schede e riquadri specifici con impostazioni personalizzate del profilo.</span><span class="sxs-lookup"><span data-stu-id="c3a01-130">These arguments let you open the terminal with specific tabs and panes with custom profile settings.</span></span> <span data-ttu-id="c3a01-131">Per altre informazioni sugli argomenti della riga di comando, vedi la [pagina Argomenti della riga di comando](./command-line-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="c3a01-131">Learn more about command line arguments on the [Command line arguments page](./command-line-arguments.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c3a01-132">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="c3a01-132">Troubleshooting</span></span>

<span data-ttu-id="c3a01-133">Se si verificano problemi con il terminale, vedi la [pagina Risoluzione dei problemi](./troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="c3a01-133">If you encounter any difficulties using the terminal, reference the [Troubleshooting page](./troubleshooting.md).</span></span> <span data-ttu-id="c3a01-134">Se trovi bug o vuoi richiedere una funzionalità, seleziona il collegamento al feedback nel menu **Informazioni** del terminale per accedere alla [pagina di GitHub](https://github.com/microsoft/terminal) in cui puoi segnalare problemi o suggerimenti.</span><span class="sxs-lookup"><span data-stu-id="c3a01-134">If you find any bugs or have a feature request, you can select the feedback link in the **About** menu of the terminal to go to the [GitHub page](https://github.com/microsoft/terminal) where you can file a new issue.</span></span>
