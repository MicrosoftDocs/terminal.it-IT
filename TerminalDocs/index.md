---
title: Panoramica di Terminale Windows
description: Informazioni su Terminale Windows e su come può migliorare il flusso di lavoro della riga di comando.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: overview
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: abc0397c3f26da92980377aac2df466fe1bf190e
ms.sourcegitcommit: d8e23557224bc50a82a36dc80ac68b9d11dfdde9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "84720117"
---
# <a name="what-is-windows-terminal"></a>Che cos'è Terminale Windows?

Terminale Windows è un'applicazione di terminale moderna destinata agli utenti di strumenti da riga di comando, come il prompt dei comandi, PowerShell e il sottosistema Windows per Linux (WSL, Windows Subsystem for Linux). Le principali funzionalità includono più schede e riquadri, il supporto per i caratteri Unicode e UTF-8, un motore di rendering del testo con accelerazione della GPU e la possibilità di personalizzare temi, testo, colori, sfondo e combinazioni di tasti di scelta rapida.

![Screenshot di Terminale Windows](./images/overview.png)

> [!NOTE]
> [Qual è la differenza tra una console, un terminale e una shell?](https://www.hanselman.com/blog/WhatsTheDifferenceBetweenAConsoleATerminalAndAShell.aspx) Spiegazione di Scott Hanselman.

## <a name="multiple-profiles-supporting-a-variety-of-command-line-applications"></a>Più profili che supportano un'ampia gamma di applicazioni da riga di comando

All'interno di Terminale Windows puoi eseguire qualsiasi applicazione dotata di un'interfaccia della riga di comando. Queste applicazioni includono PowerShell, il prompt dei comandi, Azure Cloud Shell e qualsiasi distribuzione WSL, come Ubuntu o Oh-My-Zsh.

## <a name="customized-schemes-and-configurations"></a>Configurazioni e schemi personalizzati

Puoi configurare Terminale Windows con un'ampia varietà di combinazioni di colori e impostazioni. Per informazioni su come creare una combinazione di colori personalizzati, vedi la [pagina Combinazioni di colori](./customize-settings/color-schemes.md). Puoi anche trovare configurazioni personalizzate del terminale nella [raccolta di terminali personalizzati](./custom-terminal-gallery/powerline-in-powershell.md).

## <a name="custom-key-bindings"></a>Combinazioni di tasti personalizzate

In Terminale Windows puoi usare un'ampia varietà di combinazioni di tasti personalizzate in base alle tue preferenze. Se una specifica scelta rapida da tastiera non soddisfa le tue esigenze, puoi cambiarla come preferisci.

Ad esempio, la combinazione predefinita di tasti di scelta rapida per la copia di testo dalla riga di comando è <kbd>CTRL+MAIUSC+C</kbd>. Puoi sostituirla con <kbd>CTRL+1</kbd> o con qualsiasi altra combinazione a scelta. Per aprire una nuova scheda, la combinazione predefinita di tasti di scelta rapida è <kbd>CTRL+MAIUSC+T</kbd>, ma puoi scegliere di sostituirla con <kbd>CTRL+2</kbd>. La combinazione predefinita di tasti di scelta rapida per passare tra le schede aperte è <kbd>CTRL+TAB</kbd>, ma puoi sostituirla con <kbd>CTRL+-</kbd> e usarla per creare invece una nuova scheda.

Per informazioni sulla personalizzazione delle combinazioni di tasti, vedi la [pagina Combinazioni di tasti](./customize-settings/key-bindings.md).

## <a name="unicode-and-utf-8-character-support"></a>Supporto di caratteri Unicode e UTF-8

Terminale Windows può visualizzare caratteri Unicode e UTF-8, ad esempio emoji e i caratteri di un'ampia varietà di lingue.

## <a name="gpu-accelerated-text-rendering"></a>Rendering del testo con accelerazione della GPU

Terminale Windows usa la GPU per il rendering del testo, assicurando prestazioni più elevate rispetto all'esperienza predefinita della riga di comando Windows.

## <a name="background-image-support"></a>Supporto per immagini di sfondo

Nella finestra di Terminale Windows puoi aggiungere immagini e GIF di sfondo. Per informazioni su come aggiungere immagini di sfondo al tuo profilo, vedi la [pagina Impostazioni del profilo](./customize-settings/profile-settings.md#background-image-settings).

## <a name="command-line-arguments"></a>Argomenti della riga di comando

Per avviare Terminale Windows in una specifica configurazione, puoi usare gli argomenti della riga di comando. Puoi specificare quale profilo aprire in una nuova scheda e quale cartella dovrà essere selezionata, puoi aprire il terminale con riquadri della finestra divisi e scegliere quale scheda dovrà avere lo stato attivo.

Ad esempio, per aprire Terminale Windows da PowerShell con tre riquadri, di cui quello a sinistra esegue un profilo del prompt dei comandi e quello a destra è diviso tra PowerShell e il profilo predefinito che esegue WSL, immetti:

```bash
wt -p "Command Prompt" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

Per informazioni su come configurare gli argomenti della riga di comando, vedi la [pagina Argomenti della riga di comando](./command-line-arguments.md).
