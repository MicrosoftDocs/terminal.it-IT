---
title: Argomenti della riga di comando di Terminale Windows
description: Informazioni su come creare argomenti della riga di comando per Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.openlocfilehash: e30fd547052a87c88b72d015e132e32b1889af05
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415896"
---
# <a name="using-command-line-arguments-for-windows-terminal"></a><span data-ttu-id="31467-103">Uso degli argomenti della riga di comando per Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="31467-103">Using command line arguments for Windows Terminal</span></span>

<span data-ttu-id="31467-104">Per aprire una nuova istanza di Terminale Windows dalla riga di comando, puoi usare `wt.exe`.</span><span class="sxs-lookup"><span data-stu-id="31467-104">You can use `wt.exe` to open a new instance of Windows Terminal from the command line.</span></span> <span data-ttu-id="31467-105">In alternativa, puoi anche usare l'alias di esecuzione `wt`.</span><span class="sxs-lookup"><span data-stu-id="31467-105">You can also use the execution alias `wt` instead.</span></span>

> [!NOTE]
> <span data-ttu-id="31467-106">Se hai creato Terminale Windows dal codice sorgente disponibile in [GitHub](https://github.com/microsoft/terminal), puoi aprire tale build usando `wtd.exe` o `wtd`.</span><span class="sxs-lookup"><span data-stu-id="31467-106">If you built the Windows Terminal from the source code on [GitHub](https://github.com/microsoft/terminal), you can open that build using `wtd.exe` or `wtd`.</span></span>

![Argomenti della riga di comando di Terminale Windows per riquadri divisi](./images/terminal-command-args.gif)

## <a name="command-line-syntax"></a><span data-ttu-id="31467-108">Sintassi della riga di comando</span><span class="sxs-lookup"><span data-stu-id="31467-108">Command line syntax</span></span>

<span data-ttu-id="31467-109">La riga di comando `wt` accetta due tipi di valori, ovvero **opzioni** e **comandi**.</span><span class="sxs-lookup"><span data-stu-id="31467-109">The `wt` command line accepts two types of values: **options** and **commands**.</span></span> <span data-ttu-id="31467-110">Le **opzioni** sono un elenco di flag e di altri parametri che controllano il comportamento della riga di comando `wt` nel complesso.</span><span class="sxs-lookup"><span data-stu-id="31467-110">**Options** are a list of flags and other parameters that can control the behavior of the `wt` command line as a whole.</span></span> <span data-ttu-id="31467-111">I **comandi** forniscono l'azione, o l'elenco di azioni delimitate da punti e virgola, che è necessario implementare.</span><span class="sxs-lookup"><span data-stu-id="31467-111">**Commands** provide the action, or list of actions separated by semicolons, that should be implemented.</span></span> <span data-ttu-id="31467-112">Se non specifichi un comando, per impostazione predefinita viene usato `new-tab`.</span><span class="sxs-lookup"><span data-stu-id="31467-112">If no command is specified, then the command is assumed to be `new-tab` by default.</span></span>

```bash
wt [options] [command ; ]
```

<span data-ttu-id="31467-113">Per visualizzare un messaggio della Guida con l'elenco degli argomenti della riga di comando, immetti `wt -h`, `wt --help`, `wt -?` o `wt /?`.</span><span class="sxs-lookup"><span data-stu-id="31467-113">To display a help message listing the available command line arguments, enter: `wt -h`, `wt --help`, `wt -?`, or `wt /?`.</span></span>

## <a name="options-and-commands"></a><span data-ttu-id="31467-114">Opzioni e comandi</span><span class="sxs-lookup"><span data-stu-id="31467-114">Options and commands</span></span>

<span data-ttu-id="31467-115">Di seguito è riportato l'elenco completo di opzioni e comandi supportati per la riga di comando `wt`.</span><span class="sxs-lookup"><span data-stu-id="31467-115">Below is the full list of supported commands and options for the `wt` command line.</span></span>

| <span data-ttu-id="31467-116">Opzione</span><span class="sxs-lookup"><span data-stu-id="31467-116">Option</span></span> | <span data-ttu-id="31467-117">Description</span><span class="sxs-lookup"><span data-stu-id="31467-117">Description</span></span> |
| ------ | ----------- |
| <span data-ttu-id="31467-118">`--help`, `-h`, `-?`, `/?`</span><span class="sxs-lookup"><span data-stu-id="31467-118">`--help`, `-h`, `-?`, `/?`</span></span> | <span data-ttu-id="31467-119">Visualizza il messaggio della Guida.</span><span class="sxs-lookup"><span data-stu-id="31467-119">Displays the help message.</span></span> |

| <span data-ttu-id="31467-120">Comando</span><span class="sxs-lookup"><span data-stu-id="31467-120">Command</span></span> | <span data-ttu-id="31467-121">Parametri</span><span class="sxs-lookup"><span data-stu-id="31467-121">Parameters</span></span> | <span data-ttu-id="31467-122">Description</span><span class="sxs-lookup"><span data-stu-id="31467-122">Description</span></span> |
| ------- | ---------- | ----------- |
| `new-tab` | <span data-ttu-id="31467-123">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`</span><span class="sxs-lookup"><span data-stu-id="31467-123">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`</span></span> | <span data-ttu-id="31467-124">Crea una nuova scheda.</span><span class="sxs-lookup"><span data-stu-id="31467-124">Creates a new tab.</span></span> |
| `split-pane` | <span data-ttu-id="31467-125">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`</span><span class="sxs-lookup"><span data-stu-id="31467-125">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`</span></span> | <span data-ttu-id="31467-126">Divide un nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="31467-126">Splits a new pane.</span></span> |
| `focus-tab` | `--target, -t tab-index` | <span data-ttu-id="31467-127">Imposta lo stato attivo su una specifica scheda.</span><span class="sxs-lookup"><span data-stu-id="31467-127">Focuses on a specific tab.</span></span> |

## <a name="command-line-argument-examples"></a><span data-ttu-id="31467-128">Esempi di argomenti della riga di comando</span><span class="sxs-lookup"><span data-stu-id="31467-128">Command line argument examples</span></span>

<span data-ttu-id="31467-129">I comandi possono variare leggermente a seconda della riga di comando che usi.</span><span class="sxs-lookup"><span data-stu-id="31467-129">Commands may vary slightly depending on which command line you're using.</span></span>

### <a name="open-a-new-profile-instance"></a><span data-ttu-id="31467-130">Aprire una nuova istanza del profilo</span><span class="sxs-lookup"><span data-stu-id="31467-130">Open a new profile instance</span></span>

<span data-ttu-id="31467-131">Per aprire una nuova istanza del terminale, in questo caso il comando aprirà il profilo denominato "Ubuntu-18.04", immetti:</span><span class="sxs-lookup"><span data-stu-id="31467-131">To open a new terminal instance, in this case the command will open the profile named "Ubuntu-18.04", enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="31467-132">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="31467-132">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Ubuntu-18.04"
```

#### <a name="powershell"></a>[<span data-ttu-id="31467-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="31467-133">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Ubuntu-18.04"
```

#### <a name="linux"></a>[<span data-ttu-id="31467-134">Linux</span><span class="sxs-lookup"><span data-stu-id="31467-134">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Ubuntu-18.04"
```

<span data-ttu-id="31467-135">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="31467-135">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="31467-136">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="31467-136">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="31467-137">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="31467-137">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

 <span data-ttu-id="31467-138">Il flag `-p` si usa per specificare il profilo di Terminale Windows da aprire.</span><span class="sxs-lookup"><span data-stu-id="31467-138">The `-p` flag is used to specify the Windows Terminal profile that should be opened.</span></span> <span data-ttu-id="31467-139">Sostituisci "Ubuntu-18.04" con il nome di un profilo di terminale installato.</span><span class="sxs-lookup"><span data-stu-id="31467-139">Substitute "Ubuntu-18.04" with the name of any terminal profile that you have installed.</span></span> <span data-ttu-id="31467-140">Verrà sempre aperta una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="31467-140">This will always open a new window.</span></span> <span data-ttu-id="31467-141">Terminale Windows non è ancora in grado di aprire nuove schede o riquadri in un'istanza esistente.</span><span class="sxs-lookup"><span data-stu-id="31467-141">Windows Terminal is not yet capable of opening new tabs or panes in an existing instance.</span></span>

### <a name="target-a-directory"></a><span data-ttu-id="31467-142">Directory di destinazione</span><span class="sxs-lookup"><span data-stu-id="31467-142">Target a directory</span></span>

<span data-ttu-id="31467-143">Per specificare la cartella da usare come directory iniziale della console, in questo caso la directory d:\, immetti:</span><span class="sxs-lookup"><span data-stu-id="31467-143">To specify the folder that should be used as the starting directory for the console, in this case the d:\ directory, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="31467-144">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="31467-144">Command Prompt</span></span>](#tab/windows)

```bash
wt -d d:\
```

#### <a name="powershell"></a>[<span data-ttu-id="31467-145">PowerShell</span><span class="sxs-lookup"><span data-stu-id="31467-145">PowerShell</span></span>](#tab/powershell)

```powershell
wt -d d:\
```

#### <a name="linux"></a>[<span data-ttu-id="31467-146">Linux</span><span class="sxs-lookup"><span data-stu-id="31467-146">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -d d:\
```

<span data-ttu-id="31467-147">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="31467-147">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="31467-148">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="31467-148">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="31467-149">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="31467-149">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-tabs"></a><span data-ttu-id="31467-150">Più schede</span><span class="sxs-lookup"><span data-stu-id="31467-150">Multiple tabs</span></span>

<span data-ttu-id="31467-151">Per aprire una nuova istanza del terminale con più schede, immetti:</span><span class="sxs-lookup"><span data-stu-id="31467-151">To open a new terminal instance with multiple tabs, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="31467-152">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="31467-152">Command Prompt</span></span>](#tab/windows)

```bash
wt ; ;
```

#### <a name="powershell"></a>[<span data-ttu-id="31467-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="31467-153">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; `;
```

<span data-ttu-id="31467-154">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="31467-154">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="31467-155">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, devi usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="31467-155">To interpret a semicolon ; as a command delimiter for wt command line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="31467-156">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="31467-156">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="31467-157">Linux</span><span class="sxs-lookup"><span data-stu-id="31467-157">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; \;
```

<span data-ttu-id="31467-158">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="31467-158">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="31467-159">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="31467-159">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="31467-160">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="31467-160">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="31467-161">Per aprire una nuova istanza del terminale con più schede, in questo caso un profilo del prompt dei comandi e un profilo di PowerShell, immetti:</span><span class="sxs-lookup"><span data-stu-id="31467-161">To open a new terminal instance with multiple tabs, in this case a Command Prompt profile and a PowerShell profile, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="31467-162">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="31467-162">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Command Prompt" ; new-tab -p "Windows PowerShell"
```

#### <a name="powershell"></a>[<span data-ttu-id="31467-163">PowerShell</span><span class="sxs-lookup"><span data-stu-id="31467-163">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; new-tab -p "Windows PowerShell"
```

<span data-ttu-id="31467-164">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="31467-164">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="31467-165">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, devi usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="31467-165">To interpret a semicolon ; as a command delimiter for wt command line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="31467-166">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="31467-166">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="31467-167">Linux</span><span class="sxs-lookup"><span data-stu-id="31467-167">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; new-tab -p "Windows Powershell"
```

<span data-ttu-id="31467-168">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="31467-168">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="31467-169">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="31467-169">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="31467-170">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.</span><span class="sxs-lookup"><span data-stu-id="31467-170">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-panes"></a><span data-ttu-id="31467-171">Più riquadri</span><span class="sxs-lookup"><span data-stu-id="31467-171">Multiple panes</span></span>

<span data-ttu-id="31467-172">Per aprire una nuova istanza del terminale con una scheda contenente tre riquadri eseguendo un profilo del prompt dei comandi, un profilo di PowerShell e il profilo predefinito che esegue una riga di comando WSL, immetti:</span><span class="sxs-lookup"><span data-stu-id="31467-172">To open a new terminal instance with one tab containing three panes running a Command Prompt profile, a PowerShell profile, and your default profile running a WSL command line, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="31467-173">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="31467-173">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Command Prompt" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

#### <a name="powershell"></a>[<span data-ttu-id="31467-174">PowerShell</span><span class="sxs-lookup"><span data-stu-id="31467-174">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

<span data-ttu-id="31467-175">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="31467-175">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="31467-176">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, devi usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="31467-176">To interpret a semicolon ; as a command delimiter for wt command line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="31467-177">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="31467-177">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="31467-178">Linux</span><span class="sxs-lookup"><span data-stu-id="31467-178">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; split-pane -p "Windows PowerShell" \; split-pane -H wsl.exe
```

<span data-ttu-id="31467-179">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="31467-179">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="31467-180">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="31467-180">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="31467-181">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.</span><span class="sxs-lookup"><span data-stu-id="31467-181">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="31467-182">Il flag `-H` (o `--horizontal`) indica che i riquadri devono essere divisi orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="31467-182">The `-H` flag (or `--horizontal`) indicates that you would like the panes to be split horizontally.</span></span> <span data-ttu-id="31467-183">Il flag `-V` (o `--vertical`) indica che i riquadri devono essere divisi verticalmente.</span><span class="sxs-lookup"><span data-stu-id="31467-183">The `-V` flag (or `--vertical`) indicates that you would like the panes split vertically.</span></span>

### <a name="tab-focus"></a><span data-ttu-id="31467-184">Stato attivo della scheda</span><span class="sxs-lookup"><span data-stu-id="31467-184">Tab focus</span></span>

<span data-ttu-id="31467-185">Per aprire una nuova istanza del terminale con lo stato attivo su una specifica scheda, usa il flag `-t` (o `--target`), insieme al numero dell'indice di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="31467-185">To open a new terminal instance with a specific tab in focus, use the `-t` flag (or `--target`), along with the tab-index number.</span></span> <span data-ttu-id="31467-186">Per aprire il profilo predefinito nella prima scheda e il profilo "Ubuntu-18.04" con lo stato attivo nella seconda scheda (`-t 1`), immetti:</span><span class="sxs-lookup"><span data-stu-id="31467-186">To open your default profile in the first tab and the "Ubuntu-18.04" profile focused in the second tab (`-t 1`), enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="31467-187">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="31467-187">Command Prompt</span></span>](#tab/windows)

```bash
wt ; new-tab -p "Ubuntu-18.04" ; focus-tab -t 1
```

#### <a name="powershell"></a>[<span data-ttu-id="31467-188">PowerShell</span><span class="sxs-lookup"><span data-stu-id="31467-188">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; new-tab -p "Ubuntu-18.04" `; focus-tab -t 1
```

#### <a name="linux"></a>[<span data-ttu-id="31467-189">Linux</span><span class="sxs-lookup"><span data-stu-id="31467-189">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; new-tab -p "Ubuntu-18.04" \; focus-tab -t 1
```

<span data-ttu-id="31467-190">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="31467-190">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="31467-191">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="31467-191">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="31467-192">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.</span><span class="sxs-lookup"><span data-stu-id="31467-192">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

## <a name="examples-of-multiple-commands-from-powershell"></a><span data-ttu-id="31467-193">Esempi di più comandi immessi da PowerShell</span><span class="sxs-lookup"><span data-stu-id="31467-193">Examples of multiple commands from PowerShell</span></span>

<span data-ttu-id="31467-194">Terminale Windows usa il carattere punto e virgola `;` come delimitatore per separare i comandi nella riga di comando `wt`.</span><span class="sxs-lookup"><span data-stu-id="31467-194">The Windows Terminal uses the semicolon character `;` as a delimiter for separating commands in the `wt` command line.</span></span> <span data-ttu-id="31467-195">Però anche PowerShell usa `;` come separatore di comandi.</span><span class="sxs-lookup"><span data-stu-id="31467-195">Unfortunately, PowerShell also uses `;` as a command separator.</span></span> <span data-ttu-id="31467-196">Per ovviare a questo problema, puoi usare i suggerimenti seguenti per eseguire più comandi `wt` da PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31467-196">To work around this, you can use the following tricks to run multiple `wt` commands from PowerShell.</span></span> <span data-ttu-id="31467-197">In tutti gli esempi seguenti viene creata una nuova finestra del terminale con tre riquadri, uno che esegue il prompt dei comandi, uno PowerShell e l'ultimo WSL.</span><span class="sxs-lookup"><span data-stu-id="31467-197">In all the following examples, a new terminal window is created with three panes - one running Command Prompt, one with PowerShell, and the last one running WSL.</span></span>

<span data-ttu-id="31467-198">Gli esempi seguenti usano il comando `Start-Process` per eseguire `wt`.</span><span class="sxs-lookup"><span data-stu-id="31467-198">The following examples use the `Start-Process` command to run `wt`.</span></span> <span data-ttu-id="31467-199">Per altre informazioni sui motivi per cui il terminale usa `Start-Process`, vedi [Uso di start](#using-start) di seguito.</span><span class="sxs-lookup"><span data-stu-id="31467-199">For more information on why the terminal uses `Start-Process`, see [Using start](#using-start) below.</span></span>

### <a name="single-quoted-parameters"></a><span data-ttu-id="31467-200">Parametri tra virgolette singole</span><span class="sxs-lookup"><span data-stu-id="31467-200">Single quoted parameters</span></span>

<span data-ttu-id="31467-201">In questo esempio i parametri di `wt` sono racchiusi tra virgolette singole (`'`).</span><span class="sxs-lookup"><span data-stu-id="31467-201">In this example, the `wt` parameters are wrapped in single quotes (`'`).</span></span> <span data-ttu-id="31467-202">Questa sintassi è utile se non viene calcolato nulla.</span><span class="sxs-lookup"><span data-stu-id="31467-202">This syntax is useful if nothing is being calculated.</span></span>

```powershell
start wt 'new-tab "cmd" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe'
```

### <a name="escaped-quotes"></a><span data-ttu-id="31467-203">Escape delle virgolette</span><span class="sxs-lookup"><span data-stu-id="31467-203">Escaped quotes</span></span>

<span data-ttu-id="31467-204">Per passare un valore contenuto in una variabile nella riga di comando `wt`, usa la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="31467-204">When passing a value contained in a variable to the `wt` command line, use the following syntax:</span></span>

```powershell
$ThirdPane = "wsl.exe"
start wt "new-tab cmd ; split-pane -p `"Windows PowerShell`" ; split-pane -H $ThirdPane"
```

<span data-ttu-id="31467-205">Nota l'utilizzo di `` ` `` per eseguire l'escape delle virgolette doppie (`"`) intorno a "Windows PowerShell" tra il parametro `-p` e il parametro `split-pane`.</span><span class="sxs-lookup"><span data-stu-id="31467-205">Note the usage of  `` ` `` to escape the double-quotes (`"`) around "Windows PowerShell" in the `-p` parameter to the `split-pane` parameter.</span></span>

### <a name="using-start"></a><span data-ttu-id="31467-206">Uso di `start`</span><span class="sxs-lookup"><span data-stu-id="31467-206">Using `start`</span></span>

<span data-ttu-id="31467-207">Tutti gli esempi precedenti usano in modo esplicito `start` per avviare il terminale.</span><span class="sxs-lookup"><span data-stu-id="31467-207">All the above examples explicitly used `start` to launch the terminal.</span></span>

<span data-ttu-id="31467-208">Gli esempi seguenti non usano `start` per eseguire la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="31467-208">The following examples do not use `start` to run the command line.</span></span> <span data-ttu-id="31467-209">Esistono invece altri due metodi per l'escape della riga di comando:</span><span class="sxs-lookup"><span data-stu-id="31467-209">Instead, there are two other methods of escaping the command line:</span></span>

* <span data-ttu-id="31467-210">Esegui l'escape solo dei punti e virgola in modo che `PowerShell` li ignorerà e li passerà direttamente a `wt`.</span><span class="sxs-lookup"><span data-stu-id="31467-210">Only escaping the semicolons so that `PowerShell` will ignore them and pass them straight to `wt`.</span></span>
* <span data-ttu-id="31467-211">Usa `--%`, in modo che PowerShell consideri il resto della riga di comando come argomenti per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="31467-211">Using `--%`, so PowerShell will treat the rest of the command line as arguments to the application.</span></span>

```powershell
wt new-tab "cmd" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

```powershell
wt --% new-tab cmd ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

<span data-ttu-id="31467-212">In entrambi questi esempi la finestra di Terminale Windows verrà creata con l'analisi corretta di tutti gli argomenti della riga di comando specificati.</span><span class="sxs-lookup"><span data-stu-id="31467-212">In both of these examples, the newly created Windows Terminal window will create the window by correctly parsing all the provided command line arguments.</span></span>

<span data-ttu-id="31467-213">Tuttavia, questi metodi _non_ sono attualmente consigliati, perché PowerShell aspetterà che la finestra del terminale appena creata venga chiusa prima di restituire il controllo a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31467-213">However, these methods are _not_ recommended currently, as PowerShell will wait for the newly-created terminal window to be closed before returning control to PowerShell.</span></span> <span data-ttu-id="31467-214">Per impostazione predefinita, PowerShell aspetterà che le applicazioni di Windows Store, come Terminale Windows, vengano chiuse prima di tornare al prompt.</span><span class="sxs-lookup"><span data-stu-id="31467-214">By default, PowerShell will always wait for Windows Store applications (like the Windows Terminal) to close before returning to the prompt.</span></span> <span data-ttu-id="31467-215">Nota che questo comportamento è diverso da quello del prompt dei comandi, che tornerà immediatamente al prompt.</span><span class="sxs-lookup"><span data-stu-id="31467-215">Note that this is different than the behavior of Command Prompt, which will return to the prompt immediately.</span></span>
