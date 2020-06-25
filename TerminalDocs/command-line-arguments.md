---
title: Argomenti della riga di comando di Terminale Windows
description: Informazioni su come creare argomenti della riga di comando per Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 06/18/2020
ms.topic: how-to
ms.service: terminal
ms.openlocfilehash: d40b0527bab94289457cf8c8a88931f4df943496
ms.sourcegitcommit: 91a802863cd0730d2e364377ffe44f819a66ff2a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2020
ms.locfileid: "84994378"
---
# <a name="using-command-line-arguments-for-windows-terminal"></a><span data-ttu-id="e7112-103">Uso degli argomenti della riga di comando per Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="e7112-103">Using command-line arguments for Windows Terminal</span></span>

<span data-ttu-id="e7112-104">Per aprire una nuova istanza di Terminale Windows dalla riga di comando, puoi usare `wt.exe`.</span><span class="sxs-lookup"><span data-stu-id="e7112-104">You can use `wt.exe` to open a new instance of Windows Terminal from the command line.</span></span> <span data-ttu-id="e7112-105">In alternativa, puoi anche usare l'alias di esecuzione `wt`.</span><span class="sxs-lookup"><span data-stu-id="e7112-105">You can also use the execution alias `wt` instead.</span></span>

> [!NOTE]
> <span data-ttu-id="e7112-106">Se Terminale Windows è stato creato dal codice sorgente disponibile in [GitHub](https://github.com/microsoft/terminal), è possibile aprire tale build usando `wtd.exe` o `wtd`.</span><span class="sxs-lookup"><span data-stu-id="e7112-106">If you built Windows Terminal from the source code on [GitHub](https://github.com/microsoft/terminal), you can open that build using `wtd.exe` or `wtd`.</span></span>

![Argomento della riga di comando di Terminale Windows per i riquadri divisi](./images/terminal-command-args.gif)

## <a name="command-line-syntax"></a><span data-ttu-id="e7112-108">Sintassi della riga di comando</span><span class="sxs-lookup"><span data-stu-id="e7112-108">Command line syntax</span></span>

<span data-ttu-id="e7112-109">La riga di comando `wt` accetta due tipi di valori, ovvero **opzioni** e **comandi**.</span><span class="sxs-lookup"><span data-stu-id="e7112-109">The `wt` command line accepts two types of values: **options** and **commands**.</span></span> <span data-ttu-id="e7112-110">Le **opzioni** sono un elenco di flag e di altri parametri che controllano il comportamento della riga di comando `wt` nel complesso.</span><span class="sxs-lookup"><span data-stu-id="e7112-110">**Options** are a list of flags and other parameters that can control the behavior of the `wt` command line as a whole.</span></span> <span data-ttu-id="e7112-111">I **comandi** forniscono l'azione, o l'elenco di azioni delimitate da punti e virgola, che è necessario implementare.</span><span class="sxs-lookup"><span data-stu-id="e7112-111">**Commands** provide the action, or list of actions separated by semicolons, that should be implemented.</span></span> <span data-ttu-id="e7112-112">Se non specifichi un comando, per impostazione predefinita viene usato `new-tab`.</span><span class="sxs-lookup"><span data-stu-id="e7112-112">If no command is specified, then the command is assumed to be `new-tab` by default.</span></span>

```bash
wt [options] [command ; ]
```

<span data-ttu-id="e7112-113">Per visualizzare un messaggio della Guida con l'elenco degli argomenti della riga di comando disponibili, immettere `wt -h`, `wt --help`, `wt -?` o `wt /?`.</span><span class="sxs-lookup"><span data-stu-id="e7112-113">To display a help message listing the available command-line arguments, enter: `wt -h`, `wt --help`, `wt -?`, or `wt /?`.</span></span>

## <a name="options-and-commands"></a><span data-ttu-id="e7112-114">Opzioni e comandi</span><span class="sxs-lookup"><span data-stu-id="e7112-114">Options and commands</span></span>

<span data-ttu-id="e7112-115">Di seguito è riportato l'elenco completo di opzioni e comandi supportati per la riga di comando `wt`.</span><span class="sxs-lookup"><span data-stu-id="e7112-115">Below is the full list of supported commands and options for the `wt` command line.</span></span>

| <span data-ttu-id="e7112-116">Opzione</span><span class="sxs-lookup"><span data-stu-id="e7112-116">Option</span></span> | <span data-ttu-id="e7112-117">Description</span><span class="sxs-lookup"><span data-stu-id="e7112-117">Description</span></span> |
| ------ | ----------- |
| <span data-ttu-id="e7112-118">`--help`, `-h`, `-?`, `/?`</span><span class="sxs-lookup"><span data-stu-id="e7112-118">`--help`, `-h`, `-?`, `/?`</span></span> | <span data-ttu-id="e7112-119">Visualizza il messaggio della Guida.</span><span class="sxs-lookup"><span data-stu-id="e7112-119">Displays the help message.</span></span> |
| <span data-ttu-id="e7112-120">`--maximized`, `-M`</span><span class="sxs-lookup"><span data-stu-id="e7112-120">`--maximized`, `-M`</span></span> | <span data-ttu-id="e7112-121">Avvia il terminale ingrandito.</span><span class="sxs-lookup"><span data-stu-id="e7112-121">Launches the terminal maximized.</span></span> |
| <span data-ttu-id="e7112-122">`--fullscreen`, `-F`</span><span class="sxs-lookup"><span data-stu-id="e7112-122">`--fullscreen`, `-F`</span></span> | <span data-ttu-id="e7112-123">Avvia il terminale a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="e7112-123">Launches the terminal as full screen.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="e7112-124">`--maximized`, `-M` e `--fullscreen`, `-F` sono disponibili solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="e7112-124">`--maximized`, `-M` and `--fullscreen`, `-F` are only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

| <span data-ttu-id="e7112-125">Comando</span><span class="sxs-lookup"><span data-stu-id="e7112-125">Command</span></span> | <span data-ttu-id="e7112-126">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7112-126">Parameters</span></span> | <span data-ttu-id="e7112-127">Description</span><span class="sxs-lookup"><span data-stu-id="e7112-127">Description</span></span> |
| ------- | ---------- | ----------- |
| `new-tab` | <span data-ttu-id="e7112-128">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span><span class="sxs-lookup"><span data-stu-id="e7112-128">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span></span> | <span data-ttu-id="e7112-129">Crea una nuova scheda.</span><span class="sxs-lookup"><span data-stu-id="e7112-129">Creates a new tab.</span></span> |
| `split-pane` | <span data-ttu-id="e7112-130">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span><span class="sxs-lookup"><span data-stu-id="e7112-130">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span></span> | <span data-ttu-id="e7112-131">Divide un nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="e7112-131">Splits a new pane.</span></span> |
| `focus-tab` | `--target, -t tab-index` | <span data-ttu-id="e7112-132">Imposta lo stato attivo su una specifica scheda.</span><span class="sxs-lookup"><span data-stu-id="e7112-132">Focuses on a specific tab.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="e7112-133">`--title` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="e7112-133">`--title` is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

## <a name="command-line-argument-examples"></a><span data-ttu-id="e7112-134">Esempi di argomenti della riga di comando</span><span class="sxs-lookup"><span data-stu-id="e7112-134">Command line argument examples</span></span>

<span data-ttu-id="e7112-135">I comandi possono variare leggermente a seconda della riga di comando che usi.</span><span class="sxs-lookup"><span data-stu-id="e7112-135">Commands may vary slightly depending on which command line you're using.</span></span>

### <a name="open-a-new-profile-instance"></a><span data-ttu-id="e7112-136">Aprire una nuova istanza del profilo</span><span class="sxs-lookup"><span data-stu-id="e7112-136">Open a new profile instance</span></span>

<span data-ttu-id="e7112-137">Per aprire una nuova istanza del terminale, in questo caso il comando aprirà il profilo denominato "Ubuntu-18.04", immetti:</span><span class="sxs-lookup"><span data-stu-id="e7112-137">To open a new terminal instance, in this case the command will open the profile named "Ubuntu-18.04", enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="e7112-138">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="e7112-138">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Ubuntu-18.04"
```

#### <a name="powershell"></a>[<span data-ttu-id="e7112-139">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7112-139">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Ubuntu-18.04"
```

#### <a name="linux"></a>[<span data-ttu-id="e7112-140">Linux</span><span class="sxs-lookup"><span data-stu-id="e7112-140">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Ubuntu-18.04"
```

<span data-ttu-id="e7112-141">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="e7112-141">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="e7112-142">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="e7112-142">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="e7112-143">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e7112-143">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

 <span data-ttu-id="e7112-144">Il flag `-p` si usa per specificare il profilo di Terminale Windows da aprire.</span><span class="sxs-lookup"><span data-stu-id="e7112-144">The `-p` flag is used to specify the Windows Terminal profile that should be opened.</span></span> <span data-ttu-id="e7112-145">Sostituisci "Ubuntu-18.04" con il nome di un profilo di terminale installato.</span><span class="sxs-lookup"><span data-stu-id="e7112-145">Substitute "Ubuntu-18.04" with the name of any terminal profile that you have installed.</span></span> <span data-ttu-id="e7112-146">Verrà sempre aperta una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="e7112-146">This will always open a new window.</span></span> <span data-ttu-id="e7112-147">Terminale Windows non è ancora in grado di aprire nuove schede o riquadri in un'istanza esistente.</span><span class="sxs-lookup"><span data-stu-id="e7112-147">Windows Terminal is not yet capable of opening new tabs or panes in an existing instance.</span></span>

### <a name="target-a-directory"></a><span data-ttu-id="e7112-148">Directory di destinazione</span><span class="sxs-lookup"><span data-stu-id="e7112-148">Target a directory</span></span>

<span data-ttu-id="e7112-149">Per specificare la cartella da usare come directory iniziale della console, in questo caso la directory d:\, immetti:</span><span class="sxs-lookup"><span data-stu-id="e7112-149">To specify the folder that should be used as the starting directory for the console, in this case the d:\ directory, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="e7112-150">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="e7112-150">Command Prompt</span></span>](#tab/windows)

```bash
wt -d d:\
```

#### <a name="powershell"></a>[<span data-ttu-id="e7112-151">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7112-151">PowerShell</span></span>](#tab/powershell)

```powershell
wt -d d:\
```

#### <a name="linux"></a>[<span data-ttu-id="e7112-152">Linux</span><span class="sxs-lookup"><span data-stu-id="e7112-152">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -d d:\
```

<span data-ttu-id="e7112-153">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="e7112-153">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="e7112-154">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="e7112-154">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="e7112-155">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e7112-155">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-tabs"></a><span data-ttu-id="e7112-156">Più schede</span><span class="sxs-lookup"><span data-stu-id="e7112-156">Multiple tabs</span></span>

<span data-ttu-id="e7112-157">Per aprire una nuova istanza del terminale con più schede, immetti:</span><span class="sxs-lookup"><span data-stu-id="e7112-157">To open a new terminal instance with multiple tabs, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="e7112-158">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="e7112-158">Command Prompt</span></span>](#tab/windows)

```bash
wt ; ;
```

#### <a name="powershell"></a>[<span data-ttu-id="e7112-159">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7112-159">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; `;
```

<span data-ttu-id="e7112-160">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="e7112-160">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="e7112-161">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="e7112-161">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="e7112-162">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="e7112-162">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="e7112-163">Linux</span><span class="sxs-lookup"><span data-stu-id="e7112-163">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; \;
```

<span data-ttu-id="e7112-164">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="e7112-164">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="e7112-165">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="e7112-165">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="e7112-166">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e7112-166">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="e7112-167">Per aprire una nuova istanza del terminale con più schede, in questo caso un profilo del prompt dei comandi e un profilo di PowerShell, immetti:</span><span class="sxs-lookup"><span data-stu-id="e7112-167">To open a new terminal instance with multiple tabs, in this case a Command Prompt profile and a PowerShell profile, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="e7112-168">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="e7112-168">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Command Prompt" ; new-tab -p "Windows PowerShell"
```

#### <a name="powershell"></a>[<span data-ttu-id="e7112-169">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7112-169">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; new-tab -p "Windows PowerShell"
```

<span data-ttu-id="e7112-170">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="e7112-170">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="e7112-171">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="e7112-171">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="e7112-172">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="e7112-172">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="e7112-173">Linux</span><span class="sxs-lookup"><span data-stu-id="e7112-173">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; new-tab -p "Windows Powershell"
```

<span data-ttu-id="e7112-174">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="e7112-174">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="e7112-175">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="e7112-175">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="e7112-176">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.</span><span class="sxs-lookup"><span data-stu-id="e7112-176">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-panes"></a><span data-ttu-id="e7112-177">Più riquadri</span><span class="sxs-lookup"><span data-stu-id="e7112-177">Multiple panes</span></span>

<span data-ttu-id="e7112-178">Per aprire una nuova istanza del terminale con una scheda contenente tre riquadri eseguendo un profilo del prompt dei comandi, un profilo di PowerShell e il profilo predefinito che esegue una riga di comando WSL, immetti:</span><span class="sxs-lookup"><span data-stu-id="e7112-178">To open a new terminal instance with one tab containing three panes running a Command Prompt profile, a PowerShell profile, and your default profile running a WSL command line, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="e7112-179">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="e7112-179">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Command Prompt" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

#### <a name="powershell"></a>[<span data-ttu-id="e7112-180">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7112-180">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

<span data-ttu-id="e7112-181">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="e7112-181">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="e7112-182">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="e7112-182">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="e7112-183">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="e7112-183">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="e7112-184">Linux</span><span class="sxs-lookup"><span data-stu-id="e7112-184">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; split-pane -p "Windows PowerShell" \; split-pane -H wsl.exe
```

<span data-ttu-id="e7112-185">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="e7112-185">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="e7112-186">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="e7112-186">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="e7112-187">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.</span><span class="sxs-lookup"><span data-stu-id="e7112-187">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="e7112-188">Il flag `-H` (o `--horizontal`) indica che i riquadri devono essere divisi orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="e7112-188">The `-H` flag (or `--horizontal`) indicates that you would like the panes to be split horizontally.</span></span> <span data-ttu-id="e7112-189">Il flag `-V` (o `--vertical`) indica che i riquadri devono essere divisi verticalmente.</span><span class="sxs-lookup"><span data-stu-id="e7112-189">The `-V` flag (or `--vertical`) indicates that you would like the panes split vertically.</span></span>

### <a name="tab-title-preview"></a><span data-ttu-id="e7112-190">Titolo della scheda ([anteprima](https://aka.ms/terminal-preview/))</span><span class="sxs-lookup"><span data-stu-id="e7112-190">Tab title ([Preview](https://aka.ms/terminal-preview/))</span></span>

<span data-ttu-id="e7112-191">Per aprire una nuova istanza del terminale con titoli di schede personalizzati, usare l'argomento `--title`.</span><span class="sxs-lookup"><span data-stu-id="e7112-191">To open a new terminal instance with custom tab titles, use the `--title` argument.</span></span> <span data-ttu-id="e7112-192">Per impostare il titolo di ogni scheda all'apertura di due schede, immettere:</span><span class="sxs-lookup"><span data-stu-id="e7112-192">To set the title of each tab when opening two tabs, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="e7112-193">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="e7112-193">Command Prompt</span></span>](#tab/windows)

```bash
wt --title tabname1 ; new-tab -p "Ubuntu-18.04" --title tabname2
```

#### <a name="powershell"></a>[<span data-ttu-id="e7112-194">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7112-194">PowerShell</span></span>](#tab/powershell)

```powershell
wt --title tabname1 `; new-tab -p "Ubuntu-18.04" --title tabname2
```

#### <a name="linux"></a>[<span data-ttu-id="e7112-195">Linux</span><span class="sxs-lookup"><span data-stu-id="e7112-195">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" --title tabname1 \; new-tab -p "Ubuntu-18.04" --title tabname2
```

<span data-ttu-id="e7112-196">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="e7112-196">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="e7112-197">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="e7112-197">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="e7112-198">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.</span><span class="sxs-lookup"><span data-stu-id="e7112-198">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

> [!IMPORTANT]
> <span data-ttu-id="e7112-199">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="e7112-199">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="tab-focus"></a><span data-ttu-id="e7112-200">Stato attivo della scheda</span><span class="sxs-lookup"><span data-stu-id="e7112-200">Tab focus</span></span>

<span data-ttu-id="e7112-201">Per aprire una nuova istanza del terminale con lo stato attivo su una specifica scheda, usa il flag `-t` (o `--target`), insieme al numero dell'indice di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="e7112-201">To open a new terminal instance with a specific tab in focus, use the `-t` flag (or `--target`), along with the tab-index number.</span></span> <span data-ttu-id="e7112-202">Per aprire il profilo predefinito nella prima scheda e il profilo "Ubuntu-18.04" con lo stato attivo nella seconda scheda (`-t 1`), immetti:</span><span class="sxs-lookup"><span data-stu-id="e7112-202">To open your default profile in the first tab and the "Ubuntu-18.04" profile focused in the second tab (`-t 1`), enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="e7112-203">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="e7112-203">Command Prompt</span></span>](#tab/windows)

```bash
wt ; new-tab -p "Ubuntu-18.04" ; focus-tab -t 1
```

#### <a name="powershell"></a>[<span data-ttu-id="e7112-204">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7112-204">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; new-tab -p "Ubuntu-18.04" `; focus-tab -t 1
```

#### <a name="linux"></a>[<span data-ttu-id="e7112-205">Linux</span><span class="sxs-lookup"><span data-stu-id="e7112-205">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; new-tab -p "Ubuntu-18.04" \; focus-tab -t 1
```

<span data-ttu-id="e7112-206">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="e7112-206">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="e7112-207">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="e7112-207">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="e7112-208">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.</span><span class="sxs-lookup"><span data-stu-id="e7112-208">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

## <a name="examples-of-multiple-commands-from-powershell"></a><span data-ttu-id="e7112-209">Esempi di più comandi immessi da PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7112-209">Examples of multiple commands from PowerShell</span></span>

<span data-ttu-id="e7112-210">Terminale Windows usa il carattere punto e virgola `;` come delimitatore per separare i comandi nella riga di comando `wt`.</span><span class="sxs-lookup"><span data-stu-id="e7112-210">Windows Terminal uses the semicolon character `;` as a delimiter for separating commands in the `wt` command line.</span></span> <span data-ttu-id="e7112-211">Però anche PowerShell usa `;` come separatore di comandi.</span><span class="sxs-lookup"><span data-stu-id="e7112-211">Unfortunately, PowerShell also uses `;` as a command separator.</span></span> <span data-ttu-id="e7112-212">Per ovviare a questo problema, puoi usare i suggerimenti seguenti per eseguire più comandi `wt` da PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7112-212">To work around this, you can use the following tricks to run multiple `wt` commands from PowerShell.</span></span> <span data-ttu-id="e7112-213">In tutti gli esempi seguenti viene creata una nuova finestra del terminale con tre riquadri, uno che esegue il prompt dei comandi, uno PowerShell e l'ultimo WSL.</span><span class="sxs-lookup"><span data-stu-id="e7112-213">In all the following examples, a new terminal window is created with three panes - one running Command Prompt, one with PowerShell, and the last one running WSL.</span></span>

<span data-ttu-id="e7112-214">Gli esempi seguenti usano il comando `Start-Process` per eseguire `wt`.</span><span class="sxs-lookup"><span data-stu-id="e7112-214">The following examples use the `Start-Process` command to run `wt`.</span></span> <span data-ttu-id="e7112-215">Per altre informazioni sui motivi per cui il terminale usa `Start-Process`, vedi [Uso di start](#using-start) di seguito.</span><span class="sxs-lookup"><span data-stu-id="e7112-215">For more information on why the terminal uses `Start-Process`, see [Using start](#using-start) below.</span></span>

### <a name="single-quoted-parameters"></a><span data-ttu-id="e7112-216">Parametri tra virgolette singole</span><span class="sxs-lookup"><span data-stu-id="e7112-216">Single quoted parameters</span></span>

<span data-ttu-id="e7112-217">In questo esempio i parametri di `wt` sono racchiusi tra virgolette singole (`'`).</span><span class="sxs-lookup"><span data-stu-id="e7112-217">In this example, the `wt` parameters are wrapped in single quotes (`'`).</span></span> <span data-ttu-id="e7112-218">Questa sintassi è utile se non viene calcolato nulla.</span><span class="sxs-lookup"><span data-stu-id="e7112-218">This syntax is useful if nothing is being calculated.</span></span>

```powershell
start wt 'new-tab "cmd" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe'
```

### <a name="escaped-quotes"></a><span data-ttu-id="e7112-219">Escape delle virgolette</span><span class="sxs-lookup"><span data-stu-id="e7112-219">Escaped quotes</span></span>

<span data-ttu-id="e7112-220">Per passare un valore contenuto in una variabile nella riga di comando `wt`, usa la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="e7112-220">When passing a value contained in a variable to the `wt` command line, use the following syntax:</span></span>

```powershell
$ThirdPane = "wsl.exe"
start wt "new-tab cmd ; split-pane -p `"Windows PowerShell`" ; split-pane -H $ThirdPane"
```

<span data-ttu-id="e7112-221">Nota l'utilizzo di `` ` `` per eseguire l'escape delle virgolette doppie (`"`) intorno a "Windows PowerShell" tra il parametro `-p` e il parametro `split-pane`.</span><span class="sxs-lookup"><span data-stu-id="e7112-221">Note the usage of  `` ` `` to escape the double-quotes (`"`) around "Windows PowerShell" in the `-p` parameter to the `split-pane` parameter.</span></span>

### <a name="using-start"></a><span data-ttu-id="e7112-222">Uso di `start`</span><span class="sxs-lookup"><span data-stu-id="e7112-222">Using `start`</span></span>

<span data-ttu-id="e7112-223">Tutti gli esempi precedenti usano in modo esplicito `start` per avviare il terminale.</span><span class="sxs-lookup"><span data-stu-id="e7112-223">All the above examples explicitly used `start` to launch the terminal.</span></span>

<span data-ttu-id="e7112-224">Gli esempi seguenti non usano `start` per eseguire la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e7112-224">The following examples do not use `start` to run the command line.</span></span> <span data-ttu-id="e7112-225">Esistono invece altri due metodi per l'escape della riga di comando:</span><span class="sxs-lookup"><span data-stu-id="e7112-225">Instead, there are two other methods of escaping the command line:</span></span>

* <span data-ttu-id="e7112-226">Esegui l'escape solo dei punti e virgola in modo che `PowerShell` li ignorerà e li passerà direttamente a `wt`.</span><span class="sxs-lookup"><span data-stu-id="e7112-226">Only escaping the semicolons so that `PowerShell` will ignore them and pass them straight to `wt`.</span></span>
* <span data-ttu-id="e7112-227">Usa `--%`, in modo che PowerShell consideri il resto della riga di comando come argomenti per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7112-227">Using `--%`, so PowerShell will treat the rest of the command line as arguments to the application.</span></span>

```powershell
wt new-tab "cmd" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

```powershell
wt --% new-tab cmd ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

<span data-ttu-id="e7112-228">In entrambi questi esempi la finestra di Terminale Windows verrà creata con l'analisi corretta di tutti gli argomenti della riga di comando specificati.</span><span class="sxs-lookup"><span data-stu-id="e7112-228">In both of these examples, the newly created Windows Terminal window will create the window by correctly parsing all the provided command-line arguments.</span></span>

<span data-ttu-id="e7112-229">Tuttavia, questi metodi _non_ sono attualmente consigliati, perché PowerShell aspetterà che la finestra del terminale appena creata venga chiusa prima di restituire il controllo a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7112-229">However, these methods are _not_ recommended currently, as PowerShell will wait for the newly-created terminal window to be closed before returning control to PowerShell.</span></span> <span data-ttu-id="e7112-230">Per impostazione predefinita, PowerShell aspetterà che le applicazioni di Windows Store, come Terminale Windows, vengano chiuse prima di tornare al prompt.</span><span class="sxs-lookup"><span data-stu-id="e7112-230">By default, PowerShell will always wait for Windows Store applications (like Windows Terminal) to close before returning to the prompt.</span></span> <span data-ttu-id="e7112-231">Nota che questo comportamento è diverso da quello del prompt dei comandi, che tornerà immediatamente al prompt.</span><span class="sxs-lookup"><span data-stu-id="e7112-231">Note that this is different than the behavior of Command Prompt, which will return to the prompt immediately.</span></span>
