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

È possibile aprire una nuova scheda del profilo predefinito premendo <kbd>CTRL</kbd> + <kbd>MAIUSC</kbd> + <kbd>T</kbd> o facendo clic sul pulsante + (segno più). Per aprire un profilo diverso, seleziona la freccia (˅) accanto a + per visualizzare il menu a discesa. Da qui puoi selezionare il profilo da aprire.

## <a name="invoke-the-command-palette"></a>Richiamare il riquadro comandi

È possibile richiamare la maggior parte delle funzionalità del terminale Windows tramite il [riquadro comandi](./command-palette.md). La combinazione di tasti predefinita per richiamarla è <kbd>CTRL</kbd> + <kbd>MAIUSC</kbd> + <kbd>P</kbd>.

![Esempio del riquadro comandi in uso](./images/command-palette-iterable-commands.gif)

## <a name="open-a-new-pane"></a>Aprire un nuovo riquadro

Puoi eseguire più shell affiancate usando i riquadri. Per aprire un riquadro, è possibile utilizzare <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> + <kbd>+</kbd> per un riquadro verticale o <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> + <kbd>-</kbd> per uno orizzontale. È inoltre possibile utilizzare <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> + <kbd>D</kbd> per aprire un riquadro duplicato del profilo con lo stato attivo. Per altre informazioni sui riquadri, vedi la [pagina Riquadri](./panes.md).

## <a name="configuration"></a>Configurazione

Per personalizzare le impostazioni di Terminale Windows, scegli **Impostazioni** dal menu a discesa. Verrà aperto il file `settings.json` nell'editor di testo predefinito. L'editor di testo predefinito viene definito nelle[impostazioni di Windows](ms-settings:defaultapps).

Il terminale supporta la personalizzazione delle proprietà globali che interessano l'intera applicazione, le [proprietà del profilo](./customize-settings/profile-general.md) che influiscono sulle impostazioni di ogni profilo e le [azioni](./customize-settings/actions.md) che consentono di interagire con il terminale usando la tastiera o il riquadro comandi.

> [!TIP]
> È anche possibile usare l'interfaccia utente delle impostazioni per configurare le impostazioni se si usa [Windows Terminal Preview](https://aka.ms/terminal-preview). È possibile apprendere come aprire l'interfaccia utente delle impostazioni nella [pagina azioni](./customize-settings/actions.md#application-level-commands).

## <a name="command-line-arguments"></a>Argomenti della riga di comando

Per avviare Terminale Windows in una specifica configurazione, puoi usare gli argomenti della riga di comando. Questi argomenti ti consentono di aprire il terminale con schede e riquadri specifici con impostazioni personalizzate del profilo. Per altre informazioni sugli argomenti della riga di comando, vedi la [pagina Argomenti della riga di comando](./command-line-arguments.md).

## <a name="troubleshooting"></a>Risoluzione dei problemi

Se si verificano problemi con il terminale, vedi la [pagina Risoluzione dei problemi](./troubleshooting.md). Se trovi bug o vuoi richiedere una funzionalità, seleziona il collegamento al feedback nel menu **Informazioni** del terminale per accedere alla [pagina di GitHub](https://github.com/microsoft/terminal) in cui puoi segnalare problemi o suggerimenti.
