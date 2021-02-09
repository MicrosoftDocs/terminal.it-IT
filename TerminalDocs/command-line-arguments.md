---
title: Argomenti della riga di comando di Terminale Windows
description: Informazioni su come creare argomenti della riga di comando per Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 1/28/2021
ms.topic: how-to
ms.openlocfilehash: efb5711b2569571e65f5c157b96fde68a61b292c
ms.sourcegitcommit: 85519c60d559160a7847cf99971b90eb5cb94b4e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "99974922"
---
# <a name="using-command-line-arguments-for-windows-terminal"></a><span data-ttu-id="b84e9-103">Uso degli argomenti della riga di comando per Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="b84e9-103">Using command-line arguments for Windows Terminal</span></span>

<span data-ttu-id="b84e9-104">Per aprire una nuova istanza di Terminale Windows dalla riga di comando, puoi usare `wt.exe`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-104">You can use `wt.exe` to open a new instance of Windows Terminal from the command line.</span></span> <span data-ttu-id="b84e9-105">In alternativa, puoi anche usare l'alias di esecuzione `wt`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-105">You can also use the execution alias `wt` instead.</span></span>

> [!NOTE]
> <span data-ttu-id="b84e9-106">Se Terminale Windows è stato creato dal codice sorgente disponibile in [GitHub](https://github.com/microsoft/terminal), è possibile aprire tale build usando `wtd.exe` o `wtd`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-106">If you built Windows Terminal from the source code on [GitHub](https://github.com/microsoft/terminal), you can open that build using `wtd.exe` or `wtd`.</span></span>

![Argomento della riga di comando di Terminale Windows per i riquadri divisi](./images/terminal-command-args.gif)

## <a name="command-line-syntax"></a><span data-ttu-id="b84e9-108">Sintassi della riga di comando</span><span class="sxs-lookup"><span data-stu-id="b84e9-108">Command line syntax</span></span>

<span data-ttu-id="b84e9-109">La riga di comando `wt` accetta due tipi di valori, ovvero **opzioni** e **comandi**.</span><span class="sxs-lookup"><span data-stu-id="b84e9-109">The `wt` command line accepts two types of values: **options** and **commands**.</span></span> <span data-ttu-id="b84e9-110">Le **opzioni** sono un elenco di flag e di altri parametri che controllano il comportamento della riga di comando `wt` nel complesso.</span><span class="sxs-lookup"><span data-stu-id="b84e9-110">**Options** are a list of flags and other parameters that can control the behavior of the `wt` command line as a whole.</span></span> <span data-ttu-id="b84e9-111">I **comandi** forniscono l'azione, o l'elenco di azioni delimitate da punti e virgola, che è necessario implementare.</span><span class="sxs-lookup"><span data-stu-id="b84e9-111">**Commands** provide the action, or list of actions separated by semicolons, that should be implemented.</span></span> <span data-ttu-id="b84e9-112">Se non specifichi un comando, per impostazione predefinita viene usato `new-tab`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-112">If no command is specified, then the command is assumed to be `new-tab` by default.</span></span>

```cmd
wt [options] [command ; ]
```

<span data-ttu-id="b84e9-113">Per visualizzare un messaggio della Guida con l'elenco degli argomenti della riga di comando disponibili, immettere `wt -h`, `wt --help`, `wt -?` o `wt /?`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-113">To display a help message listing the available command-line arguments, enter: `wt -h`, `wt --help`, `wt -?`, or `wt /?`.</span></span>

## <a name="options-and-commands"></a><span data-ttu-id="b84e9-114">Opzioni e comandi</span><span class="sxs-lookup"><span data-stu-id="b84e9-114">Options and commands</span></span>

<span data-ttu-id="b84e9-115">Di seguito è riportato l'elenco completo di opzioni e comandi supportati per la riga di comando `wt`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-115">Below is the full list of supported commands and options for the `wt` command line.</span></span>

| <span data-ttu-id="b84e9-116">Opzione</span><span class="sxs-lookup"><span data-stu-id="b84e9-116">Option</span></span> | <span data-ttu-id="b84e9-117">Description</span><span class="sxs-lookup"><span data-stu-id="b84e9-117">Description</span></span> |
| ------ | ----------- |
| <span data-ttu-id="b84e9-118">`--help`, `-h`, `-?`, `/?`</span><span class="sxs-lookup"><span data-stu-id="b84e9-118">`--help`, `-h`, `-?`, `/?`</span></span> | <span data-ttu-id="b84e9-119">Visualizza il messaggio della Guida.</span><span class="sxs-lookup"><span data-stu-id="b84e9-119">Displays the help message.</span></span> |
| <span data-ttu-id="b84e9-120">`--maximized`, `-M`</span><span class="sxs-lookup"><span data-stu-id="b84e9-120">`--maximized`, `-M`</span></span> | <span data-ttu-id="b84e9-121">Avvia il terminale ingrandito.</span><span class="sxs-lookup"><span data-stu-id="b84e9-121">Launches the terminal maximized.</span></span> |
| <span data-ttu-id="b84e9-122">`--fullscreen`, `-F`</span><span class="sxs-lookup"><span data-stu-id="b84e9-122">`--fullscreen`, `-F`</span></span> | <span data-ttu-id="b84e9-123">Avvia il terminale a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="b84e9-123">Launches the terminal as full screen.</span></span> |
| <span data-ttu-id="b84e9-124">`--focus`, `-f`</span><span class="sxs-lookup"><span data-stu-id="b84e9-124">`--focus`, `-f`</span></span> | <span data-ttu-id="b84e9-125">Avvia il terminale in modalità messa a fuoco.</span><span class="sxs-lookup"><span data-stu-id="b84e9-125">Launches the terminal in the focus mode.</span></span> <span data-ttu-id="b84e9-126">Può essere combinato con `maximized` .</span><span class="sxs-lookup"><span data-stu-id="b84e9-126">Can be combined with `maximized`.</span></span> |

| <span data-ttu-id="b84e9-127">Comando</span><span class="sxs-lookup"><span data-stu-id="b84e9-127">Command</span></span> | <span data-ttu-id="b84e9-128">Parametri</span><span class="sxs-lookup"><span data-stu-id="b84e9-128">Parameters</span></span> | <span data-ttu-id="b84e9-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b84e9-129">Description</span></span> |
| ------- | ---------- | ----------- |
| <span data-ttu-id="b84e9-130">`new-tab`, `nt`</span><span class="sxs-lookup"><span data-stu-id="b84e9-130">`new-tab`, `nt`</span></span> | <span data-ttu-id="b84e9-131">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`, `--tabColor`</span><span class="sxs-lookup"><span data-stu-id="b84e9-131">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`, `--tabColor`</span></span> | <span data-ttu-id="b84e9-132">Crea una nuova scheda.</span><span class="sxs-lookup"><span data-stu-id="b84e9-132">Creates a new tab.</span></span> |
| <span data-ttu-id="b84e9-133">`split-pane`, `sp`</span><span class="sxs-lookup"><span data-stu-id="b84e9-133">`split-pane`, `sp`</span></span> | <span data-ttu-id="b84e9-134">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `--title`, `--tabColor`, `--size, -s size`, `commandline`</span><span class="sxs-lookup"><span data-stu-id="b84e9-134">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `--title`, `--tabColor`, `--size, -s size`, `commandline`</span></span> | <span data-ttu-id="b84e9-135">Divide un nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="b84e9-135">Splits a new pane.</span></span> |
| <span data-ttu-id="b84e9-136">`focus-tab`, `ft`</span><span class="sxs-lookup"><span data-stu-id="b84e9-136">`focus-tab`, `ft`</span></span> | `--target, -t tab-index` | <span data-ttu-id="b84e9-137">Imposta lo stato attivo su una specifica scheda.</span><span class="sxs-lookup"><span data-stu-id="b84e9-137">Focuses on a specific tab.</span></span> |
| <span data-ttu-id="b84e9-138">`move-focus`, `mf`</span><span class="sxs-lookup"><span data-stu-id="b84e9-138">`move-focus`, `mf`</span></span> | `direction` | <span data-ttu-id="b84e9-139">Sposta lo stato attivo tra i riquadri nella direzione specificata.</span><span class="sxs-lookup"><span data-stu-id="b84e9-139">Move focus between panes in the given direction.</span></span> <span data-ttu-id="b84e9-140">Accetta uno tra `up` , `down` , `left` , `right` .</span><span class="sxs-lookup"><span data-stu-id="b84e9-140">Accepts one of `up`, `down`, `left`, `right`.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="b84e9-141">Il `--tabColor` parametro del `new-tab` sottocomando, i `--tabColor` `--size,-s size` parametri del sottocomando `split-pane` e il `move-focus` sottocomando sono disponibili solo in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="b84e9-141">The `--tabColor` parameter of the `new-tab` subcommand, `--tabColor` and `--size,-s size` parameters of the `split-pane` subcommand, and the `move-focus` subcommand are only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

> [!NOTE]
> <span data-ttu-id="b84e9-142">Quando si apre il terminale di Windows da cmd (prompt dei comandi), se si vogliono usare le impostazioni del profilo "cmd" personalizzate, sarà necessario usare il comando `wt -p cmd` .</span><span class="sxs-lookup"><span data-stu-id="b84e9-142">When opening Windows Terminal from cmd (Command Prompt), if you want to use your custom "cmd" profile settings, you will need to use the command `wt -p cmd`.</span></span> <span data-ttu-id="b84e9-143">In caso contrario, per eseguire le impostazioni *predefinite* del profilo, è sufficiente usare `wt cmd` .</span><span class="sxs-lookup"><span data-stu-id="b84e9-143">Otherwise, to run your *default* profile settings, just use `wt cmd`.</span></span>

## <a name="command-line-argument-examples"></a><span data-ttu-id="b84e9-144">Esempi di argomenti della riga di comando</span><span class="sxs-lookup"><span data-stu-id="b84e9-144">Command line argument examples</span></span>

<span data-ttu-id="b84e9-145">I comandi possono variare leggermente a seconda della riga di comando che usi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-145">Commands may vary slightly depending on which command line you're using.</span></span>

### <a name="open-a-new-profile-instance"></a><span data-ttu-id="b84e9-146">Aprire una nuova istanza del profilo</span><span class="sxs-lookup"><span data-stu-id="b84e9-146">Open a new profile instance</span></span>

<span data-ttu-id="b84e9-147">Per aprire una nuova istanza del terminale, in questo caso il comando aprirà il profilo denominato "Ubuntu-18.04", immetti:</span><span class="sxs-lookup"><span data-stu-id="b84e9-147">To open a new terminal instance, in this case the command will open the profile named "Ubuntu-18.04", enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="b84e9-148">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="b84e9-148">Command Prompt</span></span>](#tab/windows)

```cmd
wt -p "Ubuntu-18.04"
```

#### <a name="powershell"></a>[<span data-ttu-id="b84e9-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b84e9-149">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Ubuntu-18.04"
```

#### <a name="linux"></a>[<span data-ttu-id="b84e9-150">Linux</span><span class="sxs-lookup"><span data-stu-id="b84e9-150">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Ubuntu-18.04"
```

<span data-ttu-id="b84e9-151">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="b84e9-151">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="b84e9-152">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-152">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="b84e9-153">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b84e9-153">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

 <span data-ttu-id="b84e9-154">Il flag `-p` si usa per specificare il profilo di Terminale Windows da aprire.</span><span class="sxs-lookup"><span data-stu-id="b84e9-154">The `-p` flag is used to specify the Windows Terminal profile that should be opened.</span></span> <span data-ttu-id="b84e9-155">Sostituisci "Ubuntu-18.04" con il nome di un profilo di terminale installato.</span><span class="sxs-lookup"><span data-stu-id="b84e9-155">Substitute "Ubuntu-18.04" with the name of any terminal profile that you have installed.</span></span> <span data-ttu-id="b84e9-156">Verrà sempre aperta una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="b84e9-156">This will always open a new window.</span></span> <span data-ttu-id="b84e9-157">Terminale Windows non è ancora in grado di aprire nuove schede o riquadri in un'istanza esistente.</span><span class="sxs-lookup"><span data-stu-id="b84e9-157">Windows Terminal is not yet capable of opening new tabs or panes in an existing instance.</span></span>

### <a name="target-a-directory"></a><span data-ttu-id="b84e9-158">Directory di destinazione</span><span class="sxs-lookup"><span data-stu-id="b84e9-158">Target a directory</span></span>

<span data-ttu-id="b84e9-159">Per specificare la cartella da usare come directory iniziale della console, in questo caso la directory d:\, immetti:</span><span class="sxs-lookup"><span data-stu-id="b84e9-159">To specify the folder that should be used as the starting directory for the console, in this case the d:\ directory, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="b84e9-160">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="b84e9-160">Command Prompt</span></span>](#tab/windows)

```cmd
wt -d d:\
```

#### <a name="powershell"></a>[<span data-ttu-id="b84e9-161">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b84e9-161">PowerShell</span></span>](#tab/powershell)

```powershell
wt -d d:\
```

#### <a name="linux"></a>[<span data-ttu-id="b84e9-162">Linux</span><span class="sxs-lookup"><span data-stu-id="b84e9-162">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -d d:\
```

<span data-ttu-id="b84e9-163">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="b84e9-163">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="b84e9-164">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-164">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="b84e9-165">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b84e9-165">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-tabs"></a><span data-ttu-id="b84e9-166">Più schede</span><span class="sxs-lookup"><span data-stu-id="b84e9-166">Multiple tabs</span></span>

<span data-ttu-id="b84e9-167">Per aprire una nuova istanza del terminale con più schede, immetti:</span><span class="sxs-lookup"><span data-stu-id="b84e9-167">To open a new terminal instance with multiple tabs, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="b84e9-168">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="b84e9-168">Command Prompt</span></span>](#tab/windows)

```cmd
wt ; ;
```

#### <a name="powershell"></a>[<span data-ttu-id="b84e9-169">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b84e9-169">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; `;
```

<span data-ttu-id="b84e9-170">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="b84e9-170">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="b84e9-171">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-171">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="b84e9-172">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="b84e9-172">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="b84e9-173">Linux</span><span class="sxs-lookup"><span data-stu-id="b84e9-173">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; \;
```

<span data-ttu-id="b84e9-174">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="b84e9-174">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="b84e9-175">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-175">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="b84e9-176">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b84e9-176">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="b84e9-177">Per aprire una nuova istanza del terminale con più schede, in questo caso un profilo del prompt dei comandi e un profilo di PowerShell, immetti:</span><span class="sxs-lookup"><span data-stu-id="b84e9-177">To open a new terminal instance with multiple tabs, in this case a Command Prompt profile and a PowerShell profile, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="b84e9-178">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="b84e9-178">Command Prompt</span></span>](#tab/windows)

```cmd
wt -p "Command Prompt" ; new-tab -p "Windows PowerShell"
```

#### <a name="powershell"></a>[<span data-ttu-id="b84e9-179">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b84e9-179">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; new-tab -p "Windows PowerShell"
```

<span data-ttu-id="b84e9-180">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="b84e9-180">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="b84e9-181">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-181">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="b84e9-182">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="b84e9-182">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="b84e9-183">Linux</span><span class="sxs-lookup"><span data-stu-id="b84e9-183">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; new-tab -p "Windows PowerShell"
```

<span data-ttu-id="b84e9-184">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="b84e9-184">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="b84e9-185">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-185">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="b84e9-186">L' `/c` opzione indica a cmd di terminare dopo l'esecuzione e la `\;` barra rovesciata + punto e virgola separa i comandi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-186">The `/c` option tells CMD to terminate after running and the `\;` backslash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-panes"></a><span data-ttu-id="b84e9-187">Più riquadri</span><span class="sxs-lookup"><span data-stu-id="b84e9-187">Multiple panes</span></span>

<span data-ttu-id="b84e9-188">Per aprire una nuova istanza del terminale con una scheda contenente tre riquadri eseguendo un profilo del prompt dei comandi, un profilo di PowerShell e il profilo predefinito che esegue una riga di comando WSL, immetti:</span><span class="sxs-lookup"><span data-stu-id="b84e9-188">To open a new terminal instance with one tab containing three panes running a Command Prompt profile, a PowerShell profile, and your default profile running a WSL command line, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="b84e9-189">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="b84e9-189">Command Prompt</span></span>](#tab/windows)

```cmd
wt -p "Command Prompt" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

#### <a name="powershell"></a>[<span data-ttu-id="b84e9-190">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b84e9-190">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

<span data-ttu-id="b84e9-191">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="b84e9-191">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="b84e9-192">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-192">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="b84e9-193">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="b84e9-193">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="b84e9-194">Linux</span><span class="sxs-lookup"><span data-stu-id="b84e9-194">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; split-pane -p "Windows PowerShell" \; split-pane -H wsl.exe
```

<span data-ttu-id="b84e9-195">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="b84e9-195">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="b84e9-196">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-196">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="b84e9-197">L' `/c` opzione indica a cmd di terminare dopo l'esecuzione e la `\;` barra rovesciata + punto e virgola separa i comandi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-197">The `/c` option tells CMD to terminate after running and the `\;` backslash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="b84e9-198">Il flag `-H` (o `--horizontal`) indica che i riquadri devono essere divisi orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="b84e9-198">The `-H` flag (or `--horizontal`) indicates that you would like the panes to be split horizontally.</span></span> <span data-ttu-id="b84e9-199">Il flag `-V` (o `--vertical`) indica che i riquadri devono essere divisi verticalmente.</span><span class="sxs-lookup"><span data-stu-id="b84e9-199">The `-V` flag (or `--vertical`) indicates that you would like the panes split vertically.</span></span>

### <a name="multiple-tabs-and-panes"></a><span data-ttu-id="b84e9-200">Più schede e riquadri</span><span class="sxs-lookup"><span data-stu-id="b84e9-200">Multiple tabs and panes</span></span>

<span data-ttu-id="b84e9-201">I `new-tab` `split-pane` comandi e possono essere sequenziati per ottenere più schede, ognuna con riquadri suddivisi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-201">The `new-tab` and `split-pane` commands can be sequenced to get multiple tabs, each with split panes.</span></span> <span data-ttu-id="b84e9-202">Per aprire una nuova istanza di Terminal con due schede, ognuna con due riquadri che eseguono un prompt dei comandi e una riga di comando di WSL, con ogni scheda in una directory diversa, immettere:</span><span class="sxs-lookup"><span data-stu-id="b84e9-202">To open a new terminal instance with two tabs, each with two panes running a Command Prompt and a WSL command line, with each tab in a different directory, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="b84e9-203">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="b84e9-203">Command Prompt</span></span>](#tab/windows)

```cmd
wt -p "Command Prompt" ; split-pane -V wsl.exe ; new-tab -d c:\ ; split-pane -H -d c:\ wsl.exe
```

#### <a name="powershell"></a>[<span data-ttu-id="b84e9-204">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b84e9-204">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; split-pane -V wsl.exe `; new-tab -d c:\ `; split-pane -H -d c:\ wsl.exe
```

<span data-ttu-id="b84e9-205">PowerShell usa un punto e virgola (;) per delimitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="b84e9-205">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="b84e9-206">Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-206">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="b84e9-207">PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.</span><span class="sxs-lookup"><span data-stu-id="b84e9-207">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="b84e9-208">Linux</span><span class="sxs-lookup"><span data-stu-id="b84e9-208">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; split-pane -V wsl.exe \; new-tab -d c:\\ \; split-pane -H -d c:\\ wsl.exe
```

<span data-ttu-id="b84e9-209">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="b84e9-209">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="b84e9-210">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-210">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="b84e9-211">L' `/c` opzione indica a cmd di terminare dopo l'esecuzione e la `\;` barra rovesciata + punto e virgola separa i comandi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-211">The `/c` option tells CMD to terminate after running and the `\;` backslash + semicolon separates commands.</span></span>  <span data-ttu-id="b84e9-212">Si noti che per specificare una directory di Windows come directory iniziale per il `wsl.exe` quale sono necessarie due barre rovesciate `\\` .</span><span class="sxs-lookup"><span data-stu-id="b84e9-212">Note to specify a Windows directory as the starting directory for `wsl.exe` that two backslashes `\\` are required.</span></span>

---
<!-- End tab selectors.  -->

### <a name="tab-title"></a><span data-ttu-id="b84e9-213">Titolo scheda</span><span class="sxs-lookup"><span data-stu-id="b84e9-213">Tab title</span></span>

<span data-ttu-id="b84e9-214">Per aprire una nuova istanza del terminale con titoli di schede personalizzati, usare l'argomento `--title`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-214">To open a new terminal instance with custom tab titles, use the `--title` argument.</span></span> <span data-ttu-id="b84e9-215">Per impostare il titolo di ogni scheda all'apertura di due schede, immettere:</span><span class="sxs-lookup"><span data-stu-id="b84e9-215">To set the title of each tab when opening two tabs, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="b84e9-216">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="b84e9-216">Command Prompt</span></span>](#tab/windows)

```cmd
wt --title tabname1 ; new-tab -p "Ubuntu-18.04" --title tabname2
```

#### <a name="powershell"></a>[<span data-ttu-id="b84e9-217">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b84e9-217">PowerShell</span></span>](#tab/powershell)

```powershell
wt --title tabname1 `; new-tab -p "Ubuntu-18.04" --title tabname2
```

#### <a name="linux"></a>[<span data-ttu-id="b84e9-218">Linux</span><span class="sxs-lookup"><span data-stu-id="b84e9-218">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" --title tabname1 \; new-tab -p "Ubuntu-18.04" --title tabname2
```

<span data-ttu-id="b84e9-219">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="b84e9-219">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="b84e9-220">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-220">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="b84e9-221">L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-221">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

### <a name="tab-color-preview"></a><span data-ttu-id="b84e9-222">Colore scheda ([Anteprima](https://aka.ms/terminal-preview))</span><span class="sxs-lookup"><span data-stu-id="b84e9-222">Tab color ([Preview](https://aka.ms/terminal-preview))</span></span>

<span data-ttu-id="b84e9-223">Per aprire una nuova istanza di Terminal con i colori di tabulazione personalizzati, utilizzare l' `--tabColor` argomento.</span><span class="sxs-lookup"><span data-stu-id="b84e9-223">To open a new terminal instance with custom tab colors, use the `--tabColor` argument.</span></span> <span data-ttu-id="b84e9-224">Questo argomento sostituisce il valore definito nel profilo, ma è possibile eseguirne l'override anche usando la selezione dei colori della scheda.</span><span class="sxs-lookup"><span data-stu-id="b84e9-224">This argument overrides the value defined in the profile, but can be overridden as well using the tab color picker.</span></span> <span data-ttu-id="b84e9-225">Nell'esempio seguente viene creato un nuovo terminale con due schede di colori diversi:</span><span class="sxs-lookup"><span data-stu-id="b84e9-225">In the following example, a new terminal is created with two tabs of different colors:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="b84e9-226">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="b84e9-226">Command Prompt</span></span>](#tab/windows)

```cmd
wt --tabColor #009999 ; new-tab --tabColor #f59218
```

#### <a name="powershell"></a>[<span data-ttu-id="b84e9-227">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b84e9-227">PowerShell</span></span>](#tab/powershell)

```powershell
wt --tabColor #009999 ; new-tab --tabColor #f59218
```

#### <a name="linux"></a>[<span data-ttu-id="b84e9-228">Linux</span><span class="sxs-lookup"><span data-stu-id="b84e9-228">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" --tabColor #009999 \; new-tab --tabColor #f59218
```

<span data-ttu-id="b84e9-229">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="b84e9-229">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="b84e9-230">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-230">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="b84e9-231">L' `/c` opzione indica a cmd di terminare dopo l'esecuzione e `\;` separa i comandi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-231">The `/c` option tells CMD to terminate after running and `\;` separates commands.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="b84e9-232">Quando `--tabColor` è impostato per una scheda, è associato al primo riquadro di questa scheda. Pertanto, in una scheda con più riquadri, il colore verrà applicato solo se il primo riquadro è nello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="b84e9-232">When `--tabColor` is set for a tab, it is associated with the first pane of this tab. Hence in a tab with multiple panes, the color will be applied only if the first pane is in focus.</span></span> <span data-ttu-id="b84e9-233">Per impostare il colore della scheda per i riquadri aggiuntivi, è necessario aggiungere `--tabColor` anche il parametro al `split-pane` sottocomando.</span><span class="sxs-lookup"><span data-stu-id="b84e9-233">To set the tab color for additional panes, you will need to add the `--tabColor` parameter to the `split-pane` subcommand as well.</span></span> <span data-ttu-id="b84e9-234">Nell'esempio seguente viene creata una scheda con due riquadri con i colori di tabulazione specificati per ogni riquadro:</span><span class="sxs-lookup"><span data-stu-id="b84e9-234">In the example below, a tab with two panes is created with tab colors specified for each pane:</span></span>

```powershell
wt new-tab --tabColor #009999 ; split-pane --tabColor #f59218
```

> [!IMPORTANT]
> <span data-ttu-id="b84e9-235">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="b84e9-235">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="tab-focus"></a><span data-ttu-id="b84e9-236">Stato attivo della scheda</span><span class="sxs-lookup"><span data-stu-id="b84e9-236">Tab focus</span></span>

<span data-ttu-id="b84e9-237">Per aprire una nuova istanza del terminale con lo stato attivo su una specifica scheda, usa il flag `-t` (o `--target`), insieme al numero dell'indice di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="b84e9-237">To open a new terminal instance with a specific tab in focus, use the `-t` flag (or `--target`), along with the tab-index number.</span></span> <span data-ttu-id="b84e9-238">Per aprire il profilo predefinito nella prima scheda e il profilo "Ubuntu-18.04" con lo stato attivo nella seconda scheda (`-t 1`), immetti:</span><span class="sxs-lookup"><span data-stu-id="b84e9-238">To open your default profile in the first tab and the "Ubuntu-18.04" profile focused in the second tab (`-t 1`), enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="b84e9-239">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="b84e9-239">Command Prompt</span></span>](#tab/windows)

```cmd
wt ; new-tab -p "Ubuntu-18.04" ; focus-tab -t 1
```

#### <a name="powershell"></a>[<span data-ttu-id="b84e9-240">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b84e9-240">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; new-tab -p "Ubuntu-18.04" `; focus-tab -t 1
```

#### <a name="linux"></a>[<span data-ttu-id="b84e9-241">Linux</span><span class="sxs-lookup"><span data-stu-id="b84e9-241">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; new-tab -p "Ubuntu-18.04" \; focus-tab -t 1
```

<span data-ttu-id="b84e9-242">Gli alias di esecuzione non funzionano nelle distribuzioni WSL.</span><span class="sxs-lookup"><span data-stu-id="b84e9-242">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="b84e9-243">Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-243">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="b84e9-244">L' `/c` opzione indica a cmd di terminare dopo l'esecuzione e la `\;` barra rovesciata + punto e virgola separa i comandi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-244">The `/c` option tells CMD to terminate after running and the `\;` backslash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

## <a name="examples-of-multiple-commands-from-powershell"></a><span data-ttu-id="b84e9-245">Esempi di più comandi immessi da PowerShell</span><span class="sxs-lookup"><span data-stu-id="b84e9-245">Examples of multiple commands from PowerShell</span></span>

<span data-ttu-id="b84e9-246">Terminale Windows usa il carattere punto e virgola `;` come delimitatore per separare i comandi nella riga di comando `wt`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-246">Windows Terminal uses the semicolon character `;` as a delimiter for separating commands in the `wt` command line.</span></span> <span data-ttu-id="b84e9-247">Però anche PowerShell usa `;` come separatore di comandi.</span><span class="sxs-lookup"><span data-stu-id="b84e9-247">Unfortunately, PowerShell also uses `;` as a command separator.</span></span> <span data-ttu-id="b84e9-248">Per ovviare a questo problema, puoi usare i suggerimenti seguenti per eseguire più comandi `wt` da PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b84e9-248">To work around this, you can use the following tricks to run multiple `wt` commands from PowerShell.</span></span> <span data-ttu-id="b84e9-249">In tutti gli esempi seguenti viene creata una nuova finestra del terminale con tre riquadri, uno che esegue il prompt dei comandi, uno PowerShell e l'ultimo WSL.</span><span class="sxs-lookup"><span data-stu-id="b84e9-249">In all the following examples, a new terminal window is created with three panes - one running Command Prompt, one with PowerShell, and the last one running WSL.</span></span>

<span data-ttu-id="b84e9-250">Gli esempi seguenti usano il comando `Start-Process` per eseguire `wt`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-250">The following examples use the `Start-Process` command to run `wt`.</span></span> <span data-ttu-id="b84e9-251">Per altre informazioni sui motivi per cui il terminale usa `Start-Process`, vedi [Uso di start](#using-start) di seguito.</span><span class="sxs-lookup"><span data-stu-id="b84e9-251">For more information on why the terminal uses `Start-Process`, see [Using start](#using-start) below.</span></span>

### <a name="single-quoted-parameters"></a><span data-ttu-id="b84e9-252">Parametri tra virgolette singole</span><span class="sxs-lookup"><span data-stu-id="b84e9-252">Single quoted parameters</span></span>

<span data-ttu-id="b84e9-253">In questo esempio i parametri di `wt` sono racchiusi tra virgolette singole (`'`).</span><span class="sxs-lookup"><span data-stu-id="b84e9-253">In this example, the `wt` parameters are wrapped in single quotes (`'`).</span></span> <span data-ttu-id="b84e9-254">Questa sintassi è utile se non viene calcolato nulla.</span><span class="sxs-lookup"><span data-stu-id="b84e9-254">This syntax is useful if nothing is being calculated.</span></span>

```powershell
start wt 'new-tab "cmd" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe'
```

### <a name="escaped-quotes"></a><span data-ttu-id="b84e9-255">Escape delle virgolette</span><span class="sxs-lookup"><span data-stu-id="b84e9-255">Escaped quotes</span></span>

<span data-ttu-id="b84e9-256">Per passare un valore contenuto in una variabile nella riga di comando `wt`, usa la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="b84e9-256">When passing a value contained in a variable to the `wt` command line, use the following syntax:</span></span>

```powershell
$ThirdPane = "wsl.exe"
start wt "new-tab cmd ; split-pane -p `"Windows PowerShell`" ; split-pane -H $ThirdPane"
```

<span data-ttu-id="b84e9-257">Nota l'utilizzo di `` ` `` per eseguire l'escape delle virgolette doppie (`"`) intorno a "Windows PowerShell" tra il parametro `-p` e il parametro `split-pane`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-257">Note the usage of  `` ` `` to escape the double-quotes (`"`) around "Windows PowerShell" in the `-p` parameter to the `split-pane` parameter.</span></span>

### <a name="using-start"></a><span data-ttu-id="b84e9-258">Uso di `start`</span><span class="sxs-lookup"><span data-stu-id="b84e9-258">Using `start`</span></span>

<span data-ttu-id="b84e9-259">Tutti gli esempi precedenti usano in modo esplicito `start` per avviare il terminale.</span><span class="sxs-lookup"><span data-stu-id="b84e9-259">All the above examples explicitly used `start` to launch the terminal.</span></span>

<span data-ttu-id="b84e9-260">Gli esempi seguenti non usano `start` per eseguire la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b84e9-260">The following examples do not use `start` to run the command line.</span></span> <span data-ttu-id="b84e9-261">Esistono invece altri due metodi per l'escape della riga di comando:</span><span class="sxs-lookup"><span data-stu-id="b84e9-261">Instead, there are two other methods of escaping the command line:</span></span>

* <span data-ttu-id="b84e9-262">Esegui l'escape solo dei punti e virgola in modo che `PowerShell` li ignorerà e li passerà direttamente a `wt`.</span><span class="sxs-lookup"><span data-stu-id="b84e9-262">Only escaping the semicolons so that `PowerShell` will ignore them and pass them straight to `wt`.</span></span>
* <span data-ttu-id="b84e9-263">Usa `--%`, in modo che PowerShell consideri il resto della riga di comando come argomenti per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b84e9-263">Using `--%`, so PowerShell will treat the rest of the command line as arguments to the application.</span></span>

```powershell
wt new-tab "cmd" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

```powershell
wt --% new-tab cmd ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

<span data-ttu-id="b84e9-264">In entrambi questi esempi la finestra di Terminale Windows verrà creata con l'analisi corretta di tutti gli argomenti della riga di comando specificati.</span><span class="sxs-lookup"><span data-stu-id="b84e9-264">In both of these examples, the newly created Windows Terminal window will create the window by correctly parsing all the provided command-line arguments.</span></span>

<span data-ttu-id="b84e9-265">Tuttavia, questi metodi _non_ sono attualmente consigliati, perché PowerShell aspetterà che la finestra del terminale appena creata venga chiusa prima di restituire il controllo a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b84e9-265">However, these methods are _not_ recommended currently, as PowerShell will wait for the newly-created terminal window to be closed before returning control to PowerShell.</span></span> <span data-ttu-id="b84e9-266">Per impostazione predefinita, PowerShell aspetterà che le applicazioni di Windows Store, come Terminale Windows, vengano chiuse prima di tornare al prompt.</span><span class="sxs-lookup"><span data-stu-id="b84e9-266">By default, PowerShell will always wait for Windows Store applications (like Windows Terminal) to close before returning to the prompt.</span></span> <span data-ttu-id="b84e9-267">Nota che questo comportamento è diverso da quello del prompt dei comandi, che tornerà immediatamente al prompt.</span><span class="sxs-lookup"><span data-stu-id="b84e9-267">Note that this is different than the behavior of Command Prompt, which will return to the prompt immediately.</span></span>
