---
title: Argomenti della riga di comando di Terminale Windows
description: Informazioni su come creare argomenti della riga di comando per Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 11/11/2020
ms.topic: how-to
ms.openlocfilehash: 04eefd4f62b71987ce785f03f005ae7025e8949b
ms.sourcegitcommit: 9a2f9d152f65cdc8106fb9aad7fa69b01f3d05db
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/11/2020
ms.locfileid: "94520316"
---
# <a name="using-command-line-arguments-for-windows-terminal"></a><span data-ttu-id="649a3-103">Uso degli argomenti della riga di comando per Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="649a3-103">Using command-line arguments for Windows Terminal</span></span>

<span data-ttu-id="649a3-104">Per aprire una nuova istanza di Terminale Windows dalla riga di comando, puoi usare `wt.exe`.</span><span class="sxs-lookup"><span data-stu-id="649a3-104">You can use `wt.exe` to open a new instance of Windows Terminal from the command line.</span></span> <span data-ttu-id="649a3-105">In alternativa, puoi anche usare l'alias di esecuzione `wt`.</span><span class="sxs-lookup"><span data-stu-id="649a3-105">You can also use the execution alias `wt` instead.</span></span>

> [!NOTE]
> <span data-ttu-id="649a3-106">Se Terminale Windows è stato creato dal codice sorgente disponibile in [GitHub](https://github.com/microsoft/terminal), è possibile aprire tale build usando `wtd.exe` o `wtd`.</span><span class="sxs-lookup"><span data-stu-id="649a3-106">If you built Windows Terminal from the source code on [GitHub](https://github.com/microsoft/terminal), you can open that build using `wtd.exe` or `wtd`.</span></span>

![Argomento della riga di comando di Terminale Windows per i riquadri divisi](./images/terminal-command-args.gif)

## <a name="command-line-syntax"></a><span data-ttu-id="649a3-108">Sintassi della riga di comando</span><span class="sxs-lookup"><span data-stu-id="649a3-108">Command line syntax</span></span>

<span data-ttu-id="649a3-109">La riga di comando `wt` accetta due tipi di valori, ovvero **opzioni** e **comandi**.</span><span class="sxs-lookup"><span data-stu-id="649a3-109">The `wt` command line accepts two types of values: **options** and **commands**.</span></span> <span data-ttu-id="649a3-110">Le **opzioni** sono un elenco di flag e di altri parametri che controllano il comportamento della riga di comando `wt` nel complesso.</span><span class="sxs-lookup"><span data-stu-id="649a3-110">**Options** are a list of flags and other parameters that can control the behavior of the `wt` command line as a whole.</span></span> <span data-ttu-id="649a3-111">I **comandi** forniscono l'azione, o l'elenco di azioni delimitate da punti e virgola, che è necessario implementare.</span><span class="sxs-lookup"><span data-stu-id="649a3-111">**Commands** provide the action, or list of actions separated by semicolons, that should be implemented.</span></span> <span data-ttu-id="649a3-112">Se non specifichi un comando, per impostazione predefinita viene usato `new-tab`.</span><span class="sxs-lookup"><span data-stu-id="649a3-112">If no command is specified, then the command is assumed to be `new-tab` by default.</span></span>

```bash
wt [options] [command ; ]
```

<span data-ttu-id="649a3-113">Per visualizzare un messaggio della Guida con l'elenco degli argomenti della riga di comando disponibili, immettere `wt -h`, `wt --help`, `wt -?` o `wt /?`.</span><span class="sxs-lookup"><span data-stu-id="649a3-113">To display a help message listing the available command-line arguments, enter: `wt -h`, `wt --help`, `wt -?`, or `wt /?`.</span></span>

## <a name="options-and-commands"></a><span data-ttu-id="649a3-114">Opzioni e comandi</span><span class="sxs-lookup"><span data-stu-id="649a3-114">Options and commands</span></span>

<span data-ttu-id="649a3-115">Di seguito è riportato l'elenco completo di opzioni e comandi supportati per la riga di comando `wt`.</span><span class="sxs-lookup"><span data-stu-id="649a3-115">Below is the full list of supported commands and options for the `wt` command line.</span></span>

| <span data-ttu-id="649a3-116">Opzione</span><span class="sxs-lookup"><span data-stu-id="649a3-116">Option</span></span> | <span data-ttu-id="649a3-117">Description</span><span class="sxs-lookup"><span data-stu-id="649a3-117">Description</span></span> |
| ------ | ----------- |
| <span data-ttu-id="649a3-118">`--help`, `-h`, `-?`, `/?`</span><span class="sxs-lookup"><span data-stu-id="649a3-118">`--help`, `-h`, `-?`, `/?`</span></span> | <span data-ttu-id="649a3-119">Visualizza il messaggio della Guida.</span><span class="sxs-lookup"><span data-stu-id="649a3-119">Displays the help message.</span></span> |
| <span data-ttu-id="649a3-120">`--maximized`, `-M`</span><span class="sxs-lookup"><span data-stu-id="649a3-120">`--maximized`, `-M`</span></span> | <span data-ttu-id="649a3-121">Avvia il terminale ingrandito.</span><span class="sxs-lookup"><span data-stu-id="649a3-121">Launches the terminal maximized.</span></span> |
| <span data-ttu-id="649a3-122">`--fullscreen`, `-F`</span><span class="sxs-lookup"><span data-stu-id="649a3-122">`--fullscreen`, `-F`</span></span> | <span data-ttu-id="649a3-123">Avvia il terminale a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="649a3-123">Launches the terminal as full screen.</span></span> |
| <span data-ttu-id="649a3-124">`--focus`, `-f`</span><span class="sxs-lookup"><span data-stu-id="649a3-124">`--focus`, `-f`</span></span> | <span data-ttu-id="649a3-125">Avvia il terminale in modalità messa a fuoco.</span><span class="sxs-lookup"><span data-stu-id="649a3-125">Launches the terminal in the focus mode.</span></span> <span data-ttu-id="649a3-126">Può essere combinato con `maximized` .</span><span class="sxs-lookup"><span data-stu-id="649a3-126">Can be combined with `maximized`.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="649a3-127">I `--focus` `-f` flag e sono disponibili solo in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="649a3-127">The `--focus` and `-f` flags are only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

| <span data-ttu-id="649a3-128">Comando</span><span class="sxs-lookup"><span data-stu-id="649a3-128">Command</span></span> | <span data-ttu-id="649a3-129">Parametri</span><span class="sxs-lookup"><span data-stu-id="649a3-129">Parameters</span></span> | <span data-ttu-id="649a3-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="649a3-130">Description</span></span> |
| ------- | ---------- | ----------- |
| <span data-ttu-id="649a3-131">`new-tab`, `nt`</span><span class="sxs-lookup"><span data-stu-id="649a3-131">`new-tab`, `nt`</span></span> | <span data-ttu-id="649a3-132">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span><span class="sxs-lookup"><span data-stu-id="649a3-132">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span></span> | <span data-ttu-id="649a3-133">Crea una nuova scheda.</span><span class="sxs-lookup"><span data-stu-id="649a3-133">Creates a new tab.</span></span> |
| <span data-ttu-id="649a3-134">`split-pane`, `sp`</span><span class="sxs-lookup"><span data-stu-id="649a3-134">`split-pane`, `sp`</span></span> | <span data-ttu-id="649a3-135">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span><span class="sxs-lookup"><span data-stu-id="649a3-135">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span></span> | <span data-ttu-id="649a3-136">Divide un nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="649a3-136">Splits a new pane.</span></span> |
| <span data-ttu-id="649a3-137">`focus-tab`, `ft`</span><span class="sxs-lookup"><span data-stu-id="649a3-137">`focus-tab`, `ft`</span></span> | `--target, -t tab-index` | <span data-ttu-id="649a3-138">Imposta lo stato attivo su una specifica scheda.</span><span class="sxs-lookup"><span data-stu-id="649a3-138">Focuses on a specific tab.</span></span> |

> [!NOTE]
> <span data-ttu-id="649a3-139">Quando si apre il terminale di Windows da cmd (prompt dei comandi), se si vogliono usare le impostazioni del profilo "cmd" personalizzate, sarà necessario usare il comando `wt -p cmd` .</span><span class="sxs-lookup"><span data-stu-id="649a3-139">When opening Windows Terminal from cmd (Command Prompt), if you want to use your custom "cmd" profile settings, you will need to use the command `wt -p cmd`.</span></span> <span data-ttu-id="649a3-140">In caso contrario, per eseguire le impostazioni *predefinite* del profilo, è sufficiente usare `wt cmd` .</span><span class="sxs-lookup"><span data-stu-id="649a3-140">Otherwise, to run your *default* profile settings, just use `wt cmd`.</span></span>

## <a name="command-line-argument-examples"></a><span data-ttu-id="649a3-141">Esempi di argomenti della riga di comando</span><span class="sxs-lookup"><span data-stu-id="649a3-141">Command line argument examples</span></span>

<span data-ttu-id="649a3-142">I comandi possono variare leggermente a seconda della riga di comando che usi.</span><span class="sxs-lookup"><span data-stu-id="649a3-142">Commands may vary slightly depending on which command line you're using.</span></span>

### <a name="open-a-new-profile-instance"></a><span data-ttu-id="649a3-143">Aprire una nuova istanza del profilo</span><span class="sxs-lookup"><span data-stu-id="649a3-143">Open a new profile instance</span></span>

<span data-ttu-id="649a3-144">Per aprire una nuova istanza del terminale, in questo caso il comando aprirà il profilo denominato "Ubuntu-18.04", immetti:</span><span class="sxs-lookup"><span data-stu-id="649a3-144">To open a new terminal instance, in this case the command will open the profile named "Ubuntu-18.04", enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="649a3-145">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="649a3-145">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Ubuntu-18.04"
```

#### <a name="powershell"></a>[<span data-ttu-id="649a3-146">PowerShell</span><span class="sxs-lookup"><span data-stu-id="649a3-146">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Ubuntu-18.04"
```

#### <a name="linux"></a>[<span data-ttu-id="649a3-147">Linux</span><span class="sxs-lookup"><span data-stu-id="649a3-147">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Ubuntu-18.04"
```

<span data-ttu-id="649a3-148">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="649a3-148">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="649a3-149">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="649a3-149">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="649a3-150">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="649a3-150">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

 <span data-ttu-id="649a3-151">Il flag `-p` si usa per specificare il profilo di Terminale Windows da aprire.</span><span class="sxs-lookup"><span data-stu-id="649a3-151">The `-p` flag is used to specify the Windows Terminal profile that should be opened.</span></span> <span data-ttu-id="649a3-152">Sostituisci "Ubuntu-18.04" con il nome di un profilo di terminale installato.</span><span class="sxs-lookup"><span data-stu-id="649a3-152">Substitute "Ubuntu-18.04" with the name of any terminal profile that you have installed.</span></span> <span data-ttu-id="649a3-153">Verrà sempre aperta una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="649a3-153">This will always open a new window.</span></span> <span data-ttu-id="649a3-154">Terminale Windows non è ancora in grado di aprire nuove schede o riquadri in un'istanza esistente.</span><span class="sxs-lookup"><span data-stu-id="649a3-154">Windows Terminal is not yet capable of opening new tabs or panes in an existing instance.</span></span>

### <a name="target-a-directory"></a><span data-ttu-id="649a3-155">Directory di destinazione</span><span class="sxs-lookup"><span data-stu-id="649a3-155">Target a directory</span></span>

<span data-ttu-id="649a3-156">Per specificare la cartella da usare come directory iniziale della console, in questo caso la directory d:\, immetti:</span><span class="sxs-lookup"><span data-stu-id="649a3-156">To specify the folder that should be used as the starting directory for the console, in this case the d:\ directory, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="649a3-157">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="649a3-157">Command Prompt</span></span>](#tab/windows)

```bash
wt -d d:\
```

#### <a name="powershell"></a>[<span data-ttu-id="649a3-158">PowerShell</span><span class="sxs-lookup"><span data-stu-id="649a3-158">PowerShell</span></span>](#tab/powershell)

```powershell
wt -d d:\
```

#### <a name="linux"></a>[<span data-ttu-id="649a3-159">Linux</span><span class="sxs-lookup"><span data-stu-id="649a3-159">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -d d:\
```

<span data-ttu-id="649a3-160">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="649a3-160">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="649a3-161">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="649a3-161">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="649a3-162">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="649a3-162">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-tabs"></a><span data-ttu-id="649a3-163">Più schede</span><span class="sxs-lookup"><span data-stu-id="649a3-163">Multiple tabs</span></span>

<span data-ttu-id="649a3-164">Per aprire una nuova istanza del terminale con più schede, immetti:</span><span class="sxs-lookup"><span data-stu-id="649a3-164">To open a new terminal instance with multiple tabs, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="649a3-165">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="649a3-165">Command Prompt</span></span>](#tab/windows)

```bash
wt ; ;
```

#### <a name="powershell"></a>[<span data-ttu-id="649a3-166">PowerShell</span><span class="sxs-lookup"><span data-stu-id="649a3-166">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; `;
```

<span data-ttu-id="649a3-167">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="649a3-167">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="649a3-168">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="649a3-168">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="649a3-169">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="649a3-169">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="649a3-170">Linux</span><span class="sxs-lookup"><span data-stu-id="649a3-170">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; \;
```

<span data-ttu-id="649a3-171">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="649a3-171">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="649a3-172">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="649a3-172">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="649a3-173">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="649a3-173">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="649a3-174">Per aprire una nuova istanza del terminale con più schede, in questo caso un profilo del prompt dei comandi e un profilo di PowerShell, immetti:</span><span class="sxs-lookup"><span data-stu-id="649a3-174">To open a new terminal instance with multiple tabs, in this case a Command Prompt profile and a PowerShell profile, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="649a3-175">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="649a3-175">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Command Prompt" ; new-tab -p "Windows PowerShell"
```

#### <a name="powershell"></a>[<span data-ttu-id="649a3-176">PowerShell</span><span class="sxs-lookup"><span data-stu-id="649a3-176">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; new-tab -p "Windows PowerShell"
```

<span data-ttu-id="649a3-177">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="649a3-177">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="649a3-178">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="649a3-178">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="649a3-179">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="649a3-179">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="649a3-180">Linux</span><span class="sxs-lookup"><span data-stu-id="649a3-180">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; new-tab -p "Windows PowerShell"
```

<span data-ttu-id="649a3-181">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="649a3-181">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="649a3-182">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="649a3-182">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="649a3-183">L' `/c` opzione indica a cmd di terminare dopo l'esecuzione e la `\;` barra rovesciata + punto e virgola separa i comandi.</span><span class="sxs-lookup"><span data-stu-id="649a3-183">The `/c` option tells CMD to terminate after running and the `\;` backslash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-panes"></a><span data-ttu-id="649a3-184">Più riquadri</span><span class="sxs-lookup"><span data-stu-id="649a3-184">Multiple panes</span></span>

<span data-ttu-id="649a3-185">Per aprire una nuova istanza del terminale con una scheda contenente tre riquadri eseguendo un profilo del prompt dei comandi, un profilo di PowerShell e il profilo predefinito che esegue una riga di comando WSL, immetti:</span><span class="sxs-lookup"><span data-stu-id="649a3-185">To open a new terminal instance with one tab containing three panes running a Command Prompt profile, a PowerShell profile, and your default profile running a WSL command line, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="649a3-186">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="649a3-186">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Command Prompt" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

#### <a name="powershell"></a>[<span data-ttu-id="649a3-187">PowerShell</span><span class="sxs-lookup"><span data-stu-id="649a3-187">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

<span data-ttu-id="649a3-188">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="649a3-188">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="649a3-189">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="649a3-189">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="649a3-190">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="649a3-190">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="649a3-191">Linux</span><span class="sxs-lookup"><span data-stu-id="649a3-191">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; split-pane -p "Windows PowerShell" \; split-pane -H wsl.exe
```

<span data-ttu-id="649a3-192">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="649a3-192">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="649a3-193">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="649a3-193">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="649a3-194">L' `/c` opzione indica a cmd di terminare dopo l'esecuzione e la `\;` barra rovesciata + punto e virgola separa i comandi.</span><span class="sxs-lookup"><span data-stu-id="649a3-194">The `/c` option tells CMD to terminate after running and the `\;` backslash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="649a3-195">Il flag `-H` (o `--horizontal`) indica che i riquadri devono essere divisi orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="649a3-195">The `-H` flag (or `--horizontal`) indicates that you would like the panes to be split horizontally.</span></span> <span data-ttu-id="649a3-196">Il flag `-V` (o `--vertical`) indica che i riquadri devono essere divisi verticalmente.</span><span class="sxs-lookup"><span data-stu-id="649a3-196">The `-V` flag (or `--vertical`) indicates that you would like the panes split vertically.</span></span>

### <a name="multiple-tabs-and-panes"></a><span data-ttu-id="649a3-197">Più schede e riquadri</span><span class="sxs-lookup"><span data-stu-id="649a3-197">Multiple tabs and panes</span></span>

<span data-ttu-id="649a3-198">I `new-tab` `split-pane` comandi e possono essere sequenziati per ottenere più schede, ognuna con riquadri suddivisi.</span><span class="sxs-lookup"><span data-stu-id="649a3-198">The `new-tab` and `split-pane` commands can be sequenced to get multiple tabs, each with split panes.</span></span> <span data-ttu-id="649a3-199">Per aprire una nuova istanza di Terminal con due schede, ognuna con due riquadri che eseguono un prompt dei comandi e una riga di comando di WSL, con ogni scheda in una directory diversa, immettere:</span><span class="sxs-lookup"><span data-stu-id="649a3-199">To open a new terminal instance with two tabs, each with two panes running a Command Prompt and a WSL command line, with each tab in a different directory, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="649a3-200">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="649a3-200">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Command Prompt" ; split-pane -V wsl.exe ; new-tab -d c:\ ; split-pane -H -d c:\ wsl.exe
```

#### <a name="powershell"></a>[<span data-ttu-id="649a3-201">PowerShell</span><span class="sxs-lookup"><span data-stu-id="649a3-201">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; split-pane -V wsl.exe `; new-tab -d c:\ `; split-pane -H -d c:\ wsl.exe
```

<span data-ttu-id="649a3-202">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="649a3-202">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="649a3-203">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="649a3-203">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="649a3-204">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="649a3-204">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="649a3-205">Linux</span><span class="sxs-lookup"><span data-stu-id="649a3-205">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; split-pane -V wsl.exe \; new-tab -d c:\\ \; split-pane -H -d c:\\ wsl.exe
```

<span data-ttu-id="649a3-206">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="649a3-206">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="649a3-207">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="649a3-207">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="649a3-208">L' `/c` opzione indica a cmd di terminare dopo l'esecuzione e la `\;` barra rovesciata + punto e virgola separa i comandi.</span><span class="sxs-lookup"><span data-stu-id="649a3-208">The `/c` option tells CMD to terminate after running and the `\;` backslash + semicolon separates commands.</span></span>  <span data-ttu-id="649a3-209">Si noti che per specificare una directory di Windows come directory iniziale per il `wsl.exe` quale sono necessarie due barre rovesciate `\\` .</span><span class="sxs-lookup"><span data-stu-id="649a3-209">Note to specify a Windows directory as the starting directory for `wsl.exe` that two backslashes `\\` are required.</span></span>

---
<!-- End tab selectors.  -->

### <a name="tab-title"></a><span data-ttu-id="649a3-210">Titolo scheda</span><span class="sxs-lookup"><span data-stu-id="649a3-210">Tab title</span></span>

<span data-ttu-id="649a3-211">Per aprire una nuova istanza del terminale con titoli di schede personalizzati, usare l'argomento `--title`.</span><span class="sxs-lookup"><span data-stu-id="649a3-211">To open a new terminal instance with custom tab titles, use the `--title` argument.</span></span> <span data-ttu-id="649a3-212">Per impostare il titolo di ogni scheda all'apertura di due schede, immettere:</span><span class="sxs-lookup"><span data-stu-id="649a3-212">To set the title of each tab when opening two tabs, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="649a3-213">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="649a3-213">Command Prompt</span></span>](#tab/windows)

```bash
wt --title tabname1 ; new-tab -p "Ubuntu-18.04" --title tabname2
```

#### <a name="powershell"></a>[<span data-ttu-id="649a3-214">PowerShell</span><span class="sxs-lookup"><span data-stu-id="649a3-214">PowerShell</span></span>](#tab/powershell)

```powershell
wt --title tabname1 `; new-tab -p "Ubuntu-18.04" --title tabname2
```

#### <a name="linux"></a>[<span data-ttu-id="649a3-215">Linux</span><span class="sxs-lookup"><span data-stu-id="649a3-215">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" --title tabname1 \; new-tab -p "Ubuntu-18.04" --title tabname2
```

<span data-ttu-id="649a3-216">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="649a3-216">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="649a3-217">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="649a3-217">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="649a3-218">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.</span><span class="sxs-lookup"><span data-stu-id="649a3-218">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

### <a name="tab-focus"></a><span data-ttu-id="649a3-219">Stato attivo della scheda</span><span class="sxs-lookup"><span data-stu-id="649a3-219">Tab focus</span></span>

<span data-ttu-id="649a3-220">Per aprire una nuova istanza del terminale con lo stato attivo su una specifica scheda, usa il flag `-t` (o `--target`), insieme al numero dell'indice di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="649a3-220">To open a new terminal instance with a specific tab in focus, use the `-t` flag (or `--target`), along with the tab-index number.</span></span> <span data-ttu-id="649a3-221">Per aprire il profilo predefinito nella prima scheda e il profilo "Ubuntu-18.04" con lo stato attivo nella seconda scheda (`-t 1`), immetti:</span><span class="sxs-lookup"><span data-stu-id="649a3-221">To open your default profile in the first tab and the "Ubuntu-18.04" profile focused in the second tab (`-t 1`), enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="649a3-222">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="649a3-222">Command Prompt</span></span>](#tab/windows)

```bash
wt ; new-tab -p "Ubuntu-18.04" ; focus-tab -t 1
```

#### <a name="powershell"></a>[<span data-ttu-id="649a3-223">PowerShell</span><span class="sxs-lookup"><span data-stu-id="649a3-223">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; new-tab -p "Ubuntu-18.04" `; focus-tab -t 1
```

#### <a name="linux"></a>[<span data-ttu-id="649a3-224">Linux</span><span class="sxs-lookup"><span data-stu-id="649a3-224">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; new-tab -p "Ubuntu-18.04" \; focus-tab -t 1
```

<span data-ttu-id="649a3-225">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="649a3-225">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="649a3-226">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="649a3-226">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="649a3-227">L' `/c` opzione indica a cmd di terminare dopo l'esecuzione e la `\;` barra rovesciata + punto e virgola separa i comandi.</span><span class="sxs-lookup"><span data-stu-id="649a3-227">The `/c` option tells CMD to terminate after running and the `\;` backslash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

## <a name="examples-of-multiple-commands-from-powershell"></a><span data-ttu-id="649a3-228">Esempi di più comandi immessi da PowerShell</span><span class="sxs-lookup"><span data-stu-id="649a3-228">Examples of multiple commands from PowerShell</span></span>

<span data-ttu-id="649a3-229">Terminale Windows usa il carattere punto e virgola `;` come delimitatore per separare i comandi nella riga di comando `wt`.</span><span class="sxs-lookup"><span data-stu-id="649a3-229">Windows Terminal uses the semicolon character `;` as a delimiter for separating commands in the `wt` command line.</span></span> <span data-ttu-id="649a3-230">Però anche PowerShell usa `;` come separatore di comandi.</span><span class="sxs-lookup"><span data-stu-id="649a3-230">Unfortunately, PowerShell also uses `;` as a command separator.</span></span> <span data-ttu-id="649a3-231">Per ovviare a questo problema, puoi usare i suggerimenti seguenti per eseguire più comandi `wt` da PowerShell.</span><span class="sxs-lookup"><span data-stu-id="649a3-231">To work around this, you can use the following tricks to run multiple `wt` commands from PowerShell.</span></span> <span data-ttu-id="649a3-232">In tutti gli esempi seguenti viene creata una nuova finestra del terminale con tre riquadri, uno che esegue il prompt dei comandi, uno PowerShell e l'ultimo WSL.</span><span class="sxs-lookup"><span data-stu-id="649a3-232">In all the following examples, a new terminal window is created with three panes - one running Command Prompt, one with PowerShell, and the last one running WSL.</span></span>

<span data-ttu-id="649a3-233">Gli esempi seguenti usano il comando `Start-Process` per eseguire `wt`.</span><span class="sxs-lookup"><span data-stu-id="649a3-233">The following examples use the `Start-Process` command to run `wt`.</span></span> <span data-ttu-id="649a3-234">Per altre informazioni sui motivi per cui il terminale usa `Start-Process`, vedi [Uso di start](#using-start) di seguito.</span><span class="sxs-lookup"><span data-stu-id="649a3-234">For more information on why the terminal uses `Start-Process`, see [Using start](#using-start) below.</span></span>

### <a name="single-quoted-parameters"></a><span data-ttu-id="649a3-235">Parametri tra virgolette singole</span><span class="sxs-lookup"><span data-stu-id="649a3-235">Single quoted parameters</span></span>

<span data-ttu-id="649a3-236">In questo esempio i parametri di `wt` sono racchiusi tra virgolette singole (`'`).</span><span class="sxs-lookup"><span data-stu-id="649a3-236">In this example, the `wt` parameters are wrapped in single quotes (`'`).</span></span> <span data-ttu-id="649a3-237">Questa sintassi è utile se non viene calcolato nulla.</span><span class="sxs-lookup"><span data-stu-id="649a3-237">This syntax is useful if nothing is being calculated.</span></span>

```powershell
start wt 'new-tab "cmd" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe'
```

### <a name="escaped-quotes"></a><span data-ttu-id="649a3-238">Escape delle virgolette</span><span class="sxs-lookup"><span data-stu-id="649a3-238">Escaped quotes</span></span>

<span data-ttu-id="649a3-239">Per passare un valore contenuto in una variabile nella riga di comando `wt`, usa la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="649a3-239">When passing a value contained in a variable to the `wt` command line, use the following syntax:</span></span>

```powershell
$ThirdPane = "wsl.exe"
start wt "new-tab cmd ; split-pane -p `"Windows PowerShell`" ; split-pane -H $ThirdPane"
```

<span data-ttu-id="649a3-240">Nota l'utilizzo di `` ` `` per eseguire l'escape delle virgolette doppie (`"`) intorno a "Windows PowerShell" tra il parametro `-p` e il parametro `split-pane`.</span><span class="sxs-lookup"><span data-stu-id="649a3-240">Note the usage of  `` ` `` to escape the double-quotes (`"`) around "Windows PowerShell" in the `-p` parameter to the `split-pane` parameter.</span></span>

### <a name="using-start"></a><span data-ttu-id="649a3-241">Uso di `start`</span><span class="sxs-lookup"><span data-stu-id="649a3-241">Using `start`</span></span>

<span data-ttu-id="649a3-242">Tutti gli esempi precedenti usano in modo esplicito `start` per avviare il terminale.</span><span class="sxs-lookup"><span data-stu-id="649a3-242">All the above examples explicitly used `start` to launch the terminal.</span></span>

<span data-ttu-id="649a3-243">Gli esempi seguenti non usano `start` per eseguire la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="649a3-243">The following examples do not use `start` to run the command line.</span></span> <span data-ttu-id="649a3-244">Esistono invece altri due metodi per l'escape della riga di comando:</span><span class="sxs-lookup"><span data-stu-id="649a3-244">Instead, there are two other methods of escaping the command line:</span></span>

* <span data-ttu-id="649a3-245">Esegui l'escape solo dei punti e virgola in modo che `PowerShell` li ignorerà e li passerà direttamente a `wt`.</span><span class="sxs-lookup"><span data-stu-id="649a3-245">Only escaping the semicolons so that `PowerShell` will ignore them and pass them straight to `wt`.</span></span>
* <span data-ttu-id="649a3-246">Usa `--%`, in modo che PowerShell consideri il resto della riga di comando come argomenti per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="649a3-246">Using `--%`, so PowerShell will treat the rest of the command line as arguments to the application.</span></span>

```powershell
wt new-tab "cmd" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

```powershell
wt --% new-tab cmd ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

<span data-ttu-id="649a3-247">In entrambi questi esempi la finestra di Terminale Windows verrà creata con l'analisi corretta di tutti gli argomenti della riga di comando specificati.</span><span class="sxs-lookup"><span data-stu-id="649a3-247">In both of these examples, the newly created Windows Terminal window will create the window by correctly parsing all the provided command-line arguments.</span></span>

<span data-ttu-id="649a3-248">Tuttavia, questi metodi _non_ sono attualmente consigliati, perché PowerShell aspetterà che la finestra del terminale appena creata venga chiusa prima di restituire il controllo a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="649a3-248">However, these methods are _not_ recommended currently, as PowerShell will wait for the newly-created terminal window to be closed before returning control to PowerShell.</span></span> <span data-ttu-id="649a3-249">Per impostazione predefinita, PowerShell aspetterà che le applicazioni di Windows Store, come Terminale Windows, vengano chiuse prima di tornare al prompt.</span><span class="sxs-lookup"><span data-stu-id="649a3-249">By default, PowerShell will always wait for Windows Store applications (like Windows Terminal) to close before returning to the prompt.</span></span> <span data-ttu-id="649a3-250">Nota che questo comportamento è diverso da quello del prompt dei comandi, che tornerà immediatamente al prompt.</span><span class="sxs-lookup"><span data-stu-id="649a3-250">Note that this is different than the behavior of Command Prompt, which will return to the prompt immediately.</span></span>
