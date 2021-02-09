---
title: Installazione di Terminale Windows
description: In questa Guida introduttiva si apprenderà come installare e configurare il terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: quickstart
ms.localizationpriority: high
ms.openlocfilehash: 7fc7029d3905f66be15071ade6c6b3b01ef68ef9
ms.sourcegitcommit: 85519c60d559160a7847cf99971b90eb5cb94b4e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "99974932"
---
# <a name="install-and-set-up-windows-terminal"></a><span data-ttu-id="1fea0-103">Installare e configurare Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="1fea0-103">Install and set up Windows Terminal</span></span>

## <a name="installation"></a><span data-ttu-id="1fea0-104">Installazione</span><span class="sxs-lookup"><span data-stu-id="1fea0-104">Installation</span></span>

<span data-ttu-id="1fea0-105">È possibile installare Terminale Windows da [Microsoft Store](https://aka.ms/terminal).</span><span class="sxs-lookup"><span data-stu-id="1fea0-105">You can install Windows Terminal from the [Microsoft Store](https://aka.ms/terminal).</span></span>

<span data-ttu-id="1fea0-106">Se non hai accesso a Microsoft Store, le build sono pubblicate nella [pagina di versioni in GitHub](https://github.com/microsoft/terminal/releases).</span><span class="sxs-lookup"><span data-stu-id="1fea0-106">If you don't have access to the Microsoft Store, the builds are published on the [GitHub releases page](https://github.com/microsoft/terminal/releases).</span></span> <span data-ttu-id="1fea0-107">Se esegui l'installazione da GitHub, il terminale non verrà aggiornato automaticamente alle nuove versioni.</span><span class="sxs-lookup"><span data-stu-id="1fea0-107">If you install from GitHub, the terminal will not automatically update with new versions.</span></span>

## <a name="first-run"></a><span data-ttu-id="1fea0-108">Prima esecuzione</span><span class="sxs-lookup"><span data-stu-id="1fea0-108">First run</span></span>

<span data-ttu-id="1fea0-109">Dopo l'installazione, quando apri il terminale, verrà avviato con PowerShell come profilo predefinito nella scheda aperta.</span><span class="sxs-lookup"><span data-stu-id="1fea0-109">After installation, when you open the terminal, it will start with PowerShell as the default profile in the open tab.</span></span>

![Prima esecuzione di Terminale Windows](./images/first-run.png)

### <a name="dynamic-profiles"></a><span data-ttu-id="1fea0-111">Profili dinamici</span><span class="sxs-lookup"><span data-stu-id="1fea0-111">Dynamic profiles</span></span>

<span data-ttu-id="1fea0-112">Il terminale creerà automaticamente i profili se sono installate distribuzioni WSL o più versioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1fea0-112">The terminal will automatically create profiles for you if you have WSL distros or multiple versions of PowerShell installed.</span></span> <span data-ttu-id="1fea0-113">Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="1fea0-113">Learn more about dynamic profiles on the [Dynamic profiles page](./dynamic-profiles.md).</span></span>

## <a name="open-a-new-tab"></a><span data-ttu-id="1fea0-114">Aprire una nuova scheda</span><span class="sxs-lookup"><span data-stu-id="1fea0-114">Open a new tab</span></span>

<span data-ttu-id="1fea0-115">È possibile aprire una nuova scheda del profilo predefinito premendo <kbd>CTRL</kbd> + <kbd>MAIUSC</kbd> + <kbd>T</kbd> o facendo clic sul pulsante + (segno più).</span><span class="sxs-lookup"><span data-stu-id="1fea0-115">You can open a new tab of the default profile by pressing <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>T</kbd> or by selecting the + (plus) button.</span></span> <span data-ttu-id="1fea0-116">Per aprire un profilo diverso, seleziona la freccia (˅) accanto a + per visualizzare il menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="1fea0-116">To open a different profile, select the ˅ (arrow) next to the + button to open the dropdown menu.</span></span> <span data-ttu-id="1fea0-117">Da qui puoi selezionare il profilo da aprire.</span><span class="sxs-lookup"><span data-stu-id="1fea0-117">From there, you can select which profile to open.</span></span>

## <a name="invoke-the-command-palette"></a><span data-ttu-id="1fea0-118">Richiamare il riquadro comandi</span><span class="sxs-lookup"><span data-stu-id="1fea0-118">Invoke the command palette</span></span>

<span data-ttu-id="1fea0-119">È possibile richiamare la maggior parte delle funzionalità del terminale Windows tramite il [riquadro comandi](./command-palette.md).</span><span class="sxs-lookup"><span data-stu-id="1fea0-119">You can invoke most features of Windows Terminal through the [command palette](./command-palette.md).</span></span> <span data-ttu-id="1fea0-120">La combinazione di tasti predefinita per richiamarla è <kbd>CTRL</kbd> + <kbd>MAIUSC</kbd> + <kbd>P</kbd>.</span><span class="sxs-lookup"><span data-stu-id="1fea0-120">The default key combination to invoke it is <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>.</span></span>

![Esempio del riquadro comandi in uso](./images/command-palette-iterable-commands.gif)

## <a name="open-a-new-pane"></a><span data-ttu-id="1fea0-122">Aprire un nuovo riquadro</span><span class="sxs-lookup"><span data-stu-id="1fea0-122">Open a new pane</span></span>

<span data-ttu-id="1fea0-123">Puoi eseguire più shell affiancate usando i riquadri.</span><span class="sxs-lookup"><span data-stu-id="1fea0-123">You can run multiple shells side-by-side using panes.</span></span> <span data-ttu-id="1fea0-124">Per aprire un riquadro, è possibile utilizzare <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> + <kbd>+</kbd> per un riquadro verticale o <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> + <kbd>-</kbd> per uno orizzontale.</span><span class="sxs-lookup"><span data-stu-id="1fea0-124">To open a pane, you can use <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>+</kbd> for a vertical pane or <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>-</kbd> for a horizontal one.</span></span> <span data-ttu-id="1fea0-125">È inoltre possibile utilizzare <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> + <kbd>D</kbd> per aprire un riquadro duplicato del profilo con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="1fea0-125">You can also use <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>D</kbd> to open a duplicate pane of your focused profile.</span></span> <span data-ttu-id="1fea0-126">Per altre informazioni sui riquadri, vedi la [pagina Riquadri](./panes.md).</span><span class="sxs-lookup"><span data-stu-id="1fea0-126">Learn more about panes on the [Panes page](./panes.md).</span></span>

## <a name="configuration"></a><span data-ttu-id="1fea0-127">Configurazione</span><span class="sxs-lookup"><span data-stu-id="1fea0-127">Configuration</span></span>

<span data-ttu-id="1fea0-128">Per personalizzare le impostazioni di Terminale Windows, scegli **Impostazioni** dal menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="1fea0-128">To customize the settings of your Windows Terminal, select **Settings** in the dropdown menu.</span></span> <span data-ttu-id="1fea0-129">Verrà aperto il file `settings.json` nell'editor di testo predefinito.</span><span class="sxs-lookup"><span data-stu-id="1fea0-129">This will open the `settings.json` file in your default text editor.</span></span> <span data-ttu-id="1fea0-130">L'editor di testo predefinito viene definito nelle[impostazioni di Windows](ms-settings:defaultapps).</span><span class="sxs-lookup"><span data-stu-id="1fea0-130">(The default text editor is defined in your [Windows settings](ms-settings:defaultapps).)</span></span>

<span data-ttu-id="1fea0-131">Il terminale supporta la personalizzazione delle proprietà globali che interessano l'intera applicazione, le [proprietà del profilo](./customize-settings/profile-general.md) che influiscono sulle impostazioni di ogni profilo e le [azioni](./customize-settings/actions.md) che consentono di interagire con il terminale usando la tastiera o il riquadro comandi.</span><span class="sxs-lookup"><span data-stu-id="1fea0-131">The terminal supports customization of global properties that affect the whole application, [profile properties](./customize-settings/profile-general.md) that affect the settings of each profile, and [actions](./customize-settings/actions.md) that allow you to interact with the terminal using your keyboard or the command palette.</span></span>

> [!TIP]
> <span data-ttu-id="1fea0-132">È anche possibile usare l'interfaccia utente delle impostazioni per configurare le impostazioni se si usa [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="1fea0-132">You can also use the settings UI to configure your settings if you are using [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="1fea0-133">È possibile apprendere come aprire l'interfaccia utente delle impostazioni nella [pagina azioni](./customize-settings/actions.md#application-level-commands).</span><span class="sxs-lookup"><span data-stu-id="1fea0-133">You can learn how to open the settings UI on the [Actions page](./customize-settings/actions.md#application-level-commands).</span></span>

## <a name="command-line-arguments"></a><span data-ttu-id="1fea0-134">Argomenti della riga di comando</span><span class="sxs-lookup"><span data-stu-id="1fea0-134">Command line arguments</span></span>

<span data-ttu-id="1fea0-135">Per avviare Terminale Windows in una specifica configurazione, puoi usare gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="1fea0-135">You can launch the terminal in a specific configuration using command line arguments.</span></span> <span data-ttu-id="1fea0-136">Questi argomenti ti consentono di aprire il terminale con schede e riquadri specifici con impostazioni personalizzate del profilo.</span><span class="sxs-lookup"><span data-stu-id="1fea0-136">These arguments let you open the terminal with specific tabs and panes with custom profile settings.</span></span> <span data-ttu-id="1fea0-137">Per altre informazioni sugli argomenti della riga di comando, vedi la [pagina Argomenti della riga di comando](./command-line-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="1fea0-137">Learn more about command line arguments on the [Command line arguments page](./command-line-arguments.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="1fea0-138">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="1fea0-138">Troubleshooting</span></span>

<span data-ttu-id="1fea0-139">Se si verificano problemi con il terminale, vedi la [pagina Risoluzione dei problemi](./troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="1fea0-139">If you encounter any difficulties using the terminal, reference the [Troubleshooting page](./troubleshooting.md).</span></span> <span data-ttu-id="1fea0-140">Se trovi bug o vuoi richiedere una funzionalità, seleziona il collegamento al feedback nel menu **Informazioni** del terminale per accedere alla [pagina di GitHub](https://github.com/microsoft/terminal) in cui puoi segnalare problemi o suggerimenti.</span><span class="sxs-lookup"><span data-stu-id="1fea0-140">If you find any bugs or have a feature request, you can select the feedback link in the **About** menu of the terminal to go to the [GitHub page](https://github.com/microsoft/terminal) where you can file a new issue.</span></span>
