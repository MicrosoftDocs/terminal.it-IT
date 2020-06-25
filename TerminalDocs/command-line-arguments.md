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
# <a name="using-command-line-arguments-for-windows-terminal"></a>Uso degli argomenti della riga di comando per Terminale Windows

Per aprire una nuova istanza di Terminale Windows dalla riga di comando, puoi usare `wt.exe`. In alternativa, puoi anche usare l'alias di esecuzione `wt`.

> [!NOTE]
> Se Terminale Windows è stato creato dal codice sorgente disponibile in [GitHub](https://github.com/microsoft/terminal), è possibile aprire tale build usando `wtd.exe` o `wtd`.

![Argomento della riga di comando di Terminale Windows per i riquadri divisi](./images/terminal-command-args.gif)

## <a name="command-line-syntax"></a>Sintassi della riga di comando

La riga di comando `wt` accetta due tipi di valori, ovvero **opzioni** e **comandi**. Le **opzioni** sono un elenco di flag e di altri parametri che controllano il comportamento della riga di comando `wt` nel complesso. I **comandi** forniscono l'azione, o l'elenco di azioni delimitate da punti e virgola, che è necessario implementare. Se non specifichi un comando, per impostazione predefinita viene usato `new-tab`.

```bash
wt [options] [command ; ]
```

Per visualizzare un messaggio della Guida con l'elenco degli argomenti della riga di comando disponibili, immettere `wt -h`, `wt --help`, `wt -?` o `wt /?`.

## <a name="options-and-commands"></a>Opzioni e comandi

Di seguito è riportato l'elenco completo di opzioni e comandi supportati per la riga di comando `wt`.

| Opzione | Description |
| ------ | ----------- |
| `--help`, `-h`, `-?`, `/?` | Visualizza il messaggio della Guida. |
| `--maximized`, `-M` | Avvia il terminale ingrandito. |
| `--fullscreen`, `-F` | Avvia il terminale a schermo intero. |

> [!IMPORTANT]
> `--maximized`, `-M` e `--fullscreen`, `-F` sono disponibili solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).

| Comando | Parametri | Description |
| ------- | ---------- | ----------- |
| `new-tab` | `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title` | Crea una nuova scheda. |
| `split-pane` | `-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title` | Divide un nuovo riquadro. |
| `focus-tab` | `--target, -t tab-index` | Imposta lo stato attivo su una specifica scheda. |

> [!IMPORTANT]
> `--title` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).

## <a name="command-line-argument-examples"></a>Esempi di argomenti della riga di comando

I comandi possono variare leggermente a seconda della riga di comando che usi.

### <a name="open-a-new-profile-instance"></a>Aprire una nuova istanza del profilo

Per aprire una nuova istanza del terminale, in questo caso il comando aprirà il profilo denominato "Ubuntu-18.04", immetti:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Prompt dei comandi](#tab/windows)

```bash
wt -p "Ubuntu-18.04"
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt -p "Ubuntu-18.04"
```

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Ubuntu-18.04"
```

Gli alias di esecuzione non funzionano nelle distribuzioni WSL. Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`. L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.

---
<!-- End tab selectors.  -->

 Il flag `-p` si usa per specificare il profilo di Terminale Windows da aprire. Sostituisci "Ubuntu-18.04" con il nome di un profilo di terminale installato. Verrà sempre aperta una nuova finestra. Terminale Windows non è ancora in grado di aprire nuove schede o riquadri in un'istanza esistente.

### <a name="target-a-directory"></a>Directory di destinazione

Per specificare la cartella da usare come directory iniziale della console, in questo caso la directory d:\, immetti:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Prompt dei comandi](#tab/windows)

```bash
wt -d d:\
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt -d d:\
```

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" -d d:\
```

Gli alias di esecuzione non funzionano nelle distribuzioni WSL. Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`. L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.

---
<!-- End tab selectors.  -->

### <a name="multiple-tabs"></a>Più schede

Per aprire una nuova istanza del terminale con più schede, immetti:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Prompt dei comandi](#tab/windows)

```bash
wt ; ;
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt `; `;
```

PowerShell usa un punto e virgola (;) per delimitare le istruzioni. Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi. PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; \;
```

Gli alias di esecuzione non funzionano nelle distribuzioni WSL. Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`. L'opzione `/c` indica a CMD di terminare dopo l'esecuzione.

---
<!-- End tab selectors.  -->

Per aprire una nuova istanza del terminale con più schede, in questo caso un profilo del prompt dei comandi e un profilo di PowerShell, immetti:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Prompt dei comandi](#tab/windows)

```bash
wt -p "Command Prompt" ; new-tab -p "Windows PowerShell"
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt -p "Command Prompt" `; new-tab -p "Windows PowerShell"
```

PowerShell usa un punto e virgola (;) per delimitare le istruzioni. Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi. PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; new-tab -p "Windows Powershell"
```

Gli alias di esecuzione non funzionano nelle distribuzioni WSL. Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`. L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.

---
<!-- End tab selectors.  -->

### <a name="multiple-panes"></a>Più riquadri

Per aprire una nuova istanza del terminale con una scheda contenente tre riquadri eseguendo un profilo del prompt dei comandi, un profilo di PowerShell e il profilo predefinito che esegue una riga di comando WSL, immetti:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Prompt dei comandi](#tab/windows)

```bash
wt -p "Command Prompt" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt -p "Command Prompt" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

PowerShell usa un punto e virgola (;) per delimitare le istruzioni. Per interpretare un punto e virgola ; come delimitatore di comandi per gli argomenti della riga di comando wt, è necessario usare i caratteri di escape del punto e virgola con accenti gravi. PowerShell include anche l'operatore di interruzione analisi (--%), che indica di arrestare l'interpretazione di qualsiasi stringa dopo tale operatore e di passarla esattamente così come è.

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; split-pane -p "Windows PowerShell" \; split-pane -H wsl.exe
```

Gli alias di esecuzione non funzionano nelle distribuzioni WSL. Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`. L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.

---
<!-- End tab selectors.  -->

Il flag `-H` (o `--horizontal`) indica che i riquadri devono essere divisi orizzontalmente. Il flag `-V` (o `--vertical`) indica che i riquadri devono essere divisi verticalmente.

### <a name="tab-title-preview"></a>Titolo della scheda ([anteprima](https://aka.ms/terminal-preview/))

Per aprire una nuova istanza del terminale con titoli di schede personalizzati, usare l'argomento `--title`. Per impostare il titolo di ogni scheda all'apertura di due schede, immettere:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Prompt dei comandi](#tab/windows)

```bash
wt --title tabname1 ; new-tab -p "Ubuntu-18.04" --title tabname2
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt --title tabname1 `; new-tab -p "Ubuntu-18.04" --title tabname2
```

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" --title tabname1 \; new-tab -p "Ubuntu-18.04" --title tabname2
```

Gli alias di esecuzione non funzionano nelle distribuzioni WSL. Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`. L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.

---
<!-- End tab selectors.  -->

> [!IMPORTANT]
> Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).

### <a name="tab-focus"></a>Stato attivo della scheda

Per aprire una nuova istanza del terminale con lo stato attivo su una specifica scheda, usa il flag `-t` (o `--target`), insieme al numero dell'indice di tabulazione. Per aprire il profilo predefinito nella prima scheda e il profilo "Ubuntu-18.04" con lo stato attivo nella seconda scheda (`-t 1`), immetti:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Prompt dei comandi](#tab/windows)

```bash
wt ; new-tab -p "Ubuntu-18.04" ; focus-tab -t 1
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt `; new-tab -p "Ubuntu-18.04" `; focus-tab -t 1
```

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; new-tab -p "Ubuntu-18.04" \; focus-tab -t 1
```

Gli alias di esecuzione non funzionano nelle distribuzioni WSL. Se vuoi usare wt.exe dalla riga di comando WSL, puoi generarlo direttamente da CMD eseguendo `cmd.exe`. L'opzione `/c` indica a CMD di terminare dopo l'esecuzione e i caratteri `\;` (barra + punto e virgola) separano i comandi.

---
<!-- End tab selectors.  -->

## <a name="examples-of-multiple-commands-from-powershell"></a>Esempi di più comandi immessi da PowerShell

Terminale Windows usa il carattere punto e virgola `;` come delimitatore per separare i comandi nella riga di comando `wt`. Però anche PowerShell usa `;` come separatore di comandi. Per ovviare a questo problema, puoi usare i suggerimenti seguenti per eseguire più comandi `wt` da PowerShell. In tutti gli esempi seguenti viene creata una nuova finestra del terminale con tre riquadri, uno che esegue il prompt dei comandi, uno PowerShell e l'ultimo WSL.

Gli esempi seguenti usano il comando `Start-Process` per eseguire `wt`. Per altre informazioni sui motivi per cui il terminale usa `Start-Process`, vedi [Uso di start](#using-start) di seguito.

### <a name="single-quoted-parameters"></a>Parametri tra virgolette singole

In questo esempio i parametri di `wt` sono racchiusi tra virgolette singole (`'`). Questa sintassi è utile se non viene calcolato nulla.

```powershell
start wt 'new-tab "cmd" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe'
```

### <a name="escaped-quotes"></a>Escape delle virgolette

Per passare un valore contenuto in una variabile nella riga di comando `wt`, usa la sintassi seguente:

```powershell
$ThirdPane = "wsl.exe"
start wt "new-tab cmd ; split-pane -p `"Windows PowerShell`" ; split-pane -H $ThirdPane"
```

Nota l'utilizzo di `` ` `` per eseguire l'escape delle virgolette doppie (`"`) intorno a "Windows PowerShell" tra il parametro `-p` e il parametro `split-pane`.

### <a name="using-start"></a>Uso di `start`

Tutti gli esempi precedenti usano in modo esplicito `start` per avviare il terminale.

Gli esempi seguenti non usano `start` per eseguire la riga di comando. Esistono invece altri due metodi per l'escape della riga di comando:

* Esegui l'escape solo dei punti e virgola in modo che `PowerShell` li ignorerà e li passerà direttamente a `wt`.
* Usa `--%`, in modo che PowerShell consideri il resto della riga di comando come argomenti per l'applicazione.

```powershell
wt new-tab "cmd" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

```powershell
wt --% new-tab cmd ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

In entrambi questi esempi la finestra di Terminale Windows verrà creata con l'analisi corretta di tutti gli argomenti della riga di comando specificati.

Tuttavia, questi metodi _non_ sono attualmente consigliati, perché PowerShell aspetterà che la finestra del terminale appena creata venga chiusa prima di restituire il controllo a PowerShell. Per impostazione predefinita, PowerShell aspetterà che le applicazioni di Windows Store, come Terminale Windows, vengano chiuse prima di tornare al prompt. Nota che questo comportamento è diverso da quello del prompt dei comandi, che tornerà immediatamente al prompt.
