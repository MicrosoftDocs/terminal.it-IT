---
title: Impostazioni del profilo generale di Windows Terminal
description: Informazioni su come personalizzare le impostazioni generali del profilo nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: ce5b495df7048b2bff549b75f260df8e50b7ce74
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041969"
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

<br />

> [!NOTE]
> Quando si imposta la directory iniziale a cui si aprono le distribuzioni WSL installate, è necessario usare il formato seguente: `"startingDirectory": "\\\\wsl$\\DISTRO NAME\\home\\USERNAME"` , sostituendo con il nome della distribuzione. Ad esempio: `"startingDirectory": "\\\\wsl$\\Ubuntu-20.04\\home\\user1"`.

> [!NOTE]
> L'omissione del valore startingDirectory in un profilo comporta...
</br>
.. Se si esegue il terminale di Windows dal menu Start: C:\Windows\System32
</br>
.. Se si esegue wt.exe dal menu Start: C:\Windows\System32
</br>
.. Se si esegue wt.exe da Win + R:% USERPROFILE%
</br>
.. Se si esegue wt.exe dalla barra degli indirizzi di Explorer, ovvero qualunque sia la cartella esaminata.
___

## <a name="icon"></a>Icona

Questa operazione consente di impostare l'icona visualizzata all'interno della scheda, del menu a discesa, di JumpList e dello switcher di tabulazione.

**Nome della proprietà:** `icon`

**Obbligatoria:** Facoltativo

**Accetta:** Percorso del file sotto forma di stringa o emoji

<br />

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
