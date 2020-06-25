---
title: Installazione di Terminale Windows
description: Questo argomento di avvio rapido illustra come installare ed eseguire Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: quickstart
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: e804f94643835b2286e1d7aa11c84334c4223889
ms.sourcegitcommit: d8e23557224bc50a82a36dc80ac68b9d11dfdde9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "84720107"
---
# <a name="install-and-set-up-windows-terminal"></a>Installare e configurare Terminale Windows

## <a name="installation"></a>Installazione

È possibile installare Terminale Windows da [Microsoft Store](https://aka.ms/terminal).

Se non hai accesso a Microsoft Store, le build sono pubblicate nella [pagina di versioni in GitHub](https://github.com/microsoft/terminal/releases). Se esegui l'installazione da GitHub, il terminale non verrà aggiornato automaticamente alle nuove versioni.

## <a name="first-run"></a>Prima esecuzione

Dopo l'installazione, quando apri il terminale, verrà avviato con PowerShell come profilo predefinito nella scheda aperta.

![Prima esecuzione di Terminale Windows](./images/first-run.png)

### <a name="dynamic-profiles"></a>Profili dinamici

Il terminale creerà automaticamente i profili se sono installate distribuzioni WSL o più versioni di PowerShell. Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./dynamic-profiles.md).

## <a name="open-a-new-tab"></a>Aprire una nuova scheda

Per aprire una nuova scheda del profilo predefinito, premi <kbd>CTRL+MAIUSC+T</kbd> oppure il segno più (+). Per aprire un profilo diverso, seleziona la freccia (˅) accanto a + per visualizzare il menu a discesa. Da qui puoi selezionare il profilo da aprire.

## <a name="open-a-new-pane"></a>Aprire un nuovo riquadro

Puoi eseguire più shell affiancate usando i riquadri. Per aprire un riquadro, premi <kbd>ALT+MAIUSC+D</kbd>. Questa combinazione di tasti aprirà un riquadro duplicato del profilo con lo stato attivo. Per altre informazioni sui riquadri, vedi la [pagina Riquadri](./panes.md).

## <a name="configuration"></a>Configurazione

Per personalizzare le impostazioni di Terminale Windows, scegli **Impostazioni** dal menu a discesa. Verrà aperto il file `settings.json` nell'editor di testo predefinito. L'editor di testo predefinito viene definito nelle[impostazioni di Windows](ms-settings:defaultapps).

Il terminale supporta la personalizzazione di [proprietà globali](./customize-settings/global-settings.md) che influiscono sull'intera applicazione, di [proprietà del profilo](./customize-settings/profile-settings.md) che influiscono sulle impostazioni di ogni profilo e delle [combinazioni d tasti](./customize-settings/key-bindings.md) che ti consentono di interagire con il terminale tramite tastiera.

## <a name="command-line-arguments"></a>Argomenti della riga di comando

Per avviare Terminale Windows in una specifica configurazione, è possibile usare gli argomenti della riga di comando. Questi argomenti ti consentono di aprire il terminale con schede e riquadri specifici con impostazioni personalizzate del profilo. Per altre informazioni, vedere la [pagina Argomenti della riga di comando](./command-line-arguments.md).

## <a name="troubleshooting"></a>Risoluzione dei problemi

Se si verificano problemi con il terminale, vedi la [pagina Risoluzione dei problemi](./troubleshooting.md). Se trovi bug o vuoi richiedere una funzionalità, seleziona il collegamento al feedback nel menu **Informazioni** del terminale per accedere alla [pagina di GitHub](https://github.com/microsoft/terminal) in cui puoi segnalare problemi o suggerimenti.
