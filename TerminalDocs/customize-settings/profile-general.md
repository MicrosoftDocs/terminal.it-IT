---
title: Impostazioni del profilo generale di Windows Terminal
description: Informazioni su come personalizzare le impostazioni generali del profilo nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: e8eb635075e5ea87c35713762f95cc0a375fe4b4
ms.sourcegitcommit: 85519c60d559160a7847cf99971b90eb5cb94b4e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "99974872"
---
# <a name="general-profile-settings-in-windows-terminal"></a>Impostazioni generali del profilo nel terminale di Windows

Le impostazioni elencate di seguito sono specifiche dei singoli profili univoci. Se vuoi applicare un'impostazione a tutti i profili, puoi aggiungerla alla sezione `defaults` prima dell'elenco dei profili nel file settings.json.

```json
"defaults":
{
    // SETTINGS TO APPLY TO ALL PROFILES
},
"list":
[
    // PROFILE OBJECTS
]
```

> [!IMPORTANT]
> L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview). Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).

## <a name="name"></a>Nome

Nome del profilo che verrà visualizzato nel menu a discesa. Questo valore viene usato anche come titolo da passare alla shell all'avvio. Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione. Per eseguire l'override di questo comportamento del titolo, usa `tabTitle`.

**Nome della proprietà:** `name`

**Obbligatoria:** Obbligatoria

**Accetta:** String

<br />

___

## <a name="command-line"></a>Riga di comando

File eseguibile usato nel profilo.

**Nome della proprietà:** `commandline`

**Obbligatoria:** Facoltativo

**Accetta:** nome del file eseguibile in formato stringa

**Valore predefinito:** `"cmd.exe"`

<br />

___

## <a name="starting-directory"></a>Directory iniziale

Directory in cui viene avviata la shell quando viene caricata.

**Nome della proprietà:** `startingDirectory`

**Obbligatoria:** Facoltativo

**Accetta:** percorso della cartella in formato stringa

**Valore predefinito:** `"%USERPROFILE%"`

**Esempio:** Avviare il profilo di PowerShell nella cartella *GitHubRepos* della directory dei *documenti* individuando il profilo di powershell.exe e aggiungendo `"startingDirectory": "%USERPROFILE%/Documents/GitHubRepos",`

**Esempio con WSL:** Quando si imposta la directory iniziale per una [distribuzione Linux installata tramite WSL](https://docs.microsoft.com/windows/wsl/install-win10), usare il formato: `"startingDirectory": "\\\\wsl$\\DISTRO NAME\\home\\USERNAME"` , sostituendo con i segnaposto con i nomi appropriati della distribuzione. Ad esempio: `"startingDirectory": "\\\\wsl$\\Ubuntu-20.04\\home\\user1"`.

**Comportamento predefinito:** Se il valore startingDirectory non è specificato, si otterranno risultati diversi a seconda della posizione in cui si avvia il terminale:
- Se si esegue il terminale di Windows dal menu Start: C:\Windows\System32
- Se si esegue wt.exe dal menu Start: C:\Windows\System32
- Se si esegue wt.exe da Win + R:% USERPROFILE%
- Se si esegue wt.exe dalla barra degli indirizzi di Explorer, ovvero qualunque sia la cartella esaminata.

> [!NOTE]
> Le barre rovesciate devono essere precedute da un carattere di escape. Ad esempio, `C:\Users\USERNAME\Documents` deve essere immesso come `C:\\Users\\USERNAME\\Documents` .

___

## <a name="icon"></a>Icona

Questa operazione consente di impostare l'icona visualizzata all'interno della scheda, del menu a discesa, di JumpList e dello switcher di tabulazione.

**Nome della proprietà:** `icon`

**Obbligatoria:** Facoltativo

**Accetta:** Percorso del file sotto forma di stringa o emoji

**Esempio:**  Inserendo l'immagine dell'icona `ubuntu.ico` nella cartella `%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\RoamingState` che si trova in, è possibile visualizzare l'icona aggiungendo questa riga al profilo nel settings.jsin: `"icon": "ms-appdata:///roaming/ubuntu.ico"` .

<br>
___

## <a name="tab-title"></a>Titolo scheda

Se è impostata, sostituirà `name` come titolo da passare alla shell all'avvio. Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione. Per informazioni su come impostare la shell come titolo, vedi l'[esercitazione relativa al titolo della scheda](./../tutorials/tab-title.md).

**Nome della proprietà:** `tabTitle`

**Obbligatoria:** Facoltativo

**Accetta:** String

<br />

___

## <a name="hide-profile-from-dropdown"></a>Nascondi profilo dall'elenco a discesa

Se `hidden` è impostato su `true`, il profilo non verrà visualizzato nell'elenco dei profili. Può essere usata per nascondere i profili predefiniti e quelli generati dinamicamente, lasciandoli nel file settings. Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).

**Nome della proprietà:** `hidden`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`
