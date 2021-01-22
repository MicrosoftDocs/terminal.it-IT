---
title: Profili dinamici di Terminale Windows
description: Informazioni sui profili dinamici in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: concept
ms.openlocfilehash: 8b6ea176a834517b8d57777bf2f39129151a9351
ms.sourcegitcommit: 8e0901b83a8cc437f090fe58688b86acb73f3cb3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "90988710"
---
# <a name="dynamic-profiles-in-windows-terminal"></a><span data-ttu-id="68338-103">Profili dinamici in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="68338-103">Dynamic profiles in Windows Terminal</span></span>

<span data-ttu-id="68338-104">Terminale Windows creerà automaticamente il sottosistema Windows per Linux (WSL) e i profili di PowerShell se queste shell sono installate nel computer.</span><span class="sxs-lookup"><span data-stu-id="68338-104">Windows Terminal will automatically create Windows Subsystem for Linux (WSL) and PowerShell profiles for you if you have these shells installed on your machine.</span></span> <span data-ttu-id="68338-105">In questo modo è più facile avere tutte le shell incluse nel terminale senza dover individuare i relativi file eseguibili.</span><span class="sxs-lookup"><span data-stu-id="68338-105">This makes it easier for you to have all of your shells included in the terminal without having to locate their executable files.</span></span> <span data-ttu-id="68338-106">Questi profili vengono generati con la proprietà `source`, che indica al terminale dove trovare il file eseguibile appropriato.</span><span class="sxs-lookup"><span data-stu-id="68338-106">These profiles are generated with the `source` property, which tells the terminal where to locate the proper executable.</span></span>

<span data-ttu-id="68338-107">Dopo l'installazione, il terminale imposterà PowerShell come profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="68338-107">Upon installing the terminal, it will set PowerShell as your default profile.</span></span> <span data-ttu-id="68338-108">Per informazioni su come cambiare il profilo predefinito, vedi la [pagina delle impostazioni globali](./customize-settings/global-settings.md).</span><span class="sxs-lookup"><span data-stu-id="68338-108">To learn how to change your default profile, visit the [Global settings page](./customize-settings/global-settings.md).</span></span>

<span data-ttu-id="68338-109">![Profili dinamici di Terminale Windows](./images/dynamic-profiles.png)
_Configurazione: [tema chiaro](./custom-terminal-gallery/frosted-glass-theme.md)_</span><span class="sxs-lookup"><span data-stu-id="68338-109">![Windows Terminal dynamic profiles](./images/dynamic-profiles.png)
_Configuration: [Light Theme](./custom-terminal-gallery/frosted-glass-theme.md)_</span></span>

## <a name="installing-a-new-shell-after-installing-windows-terminal"></a><span data-ttu-id="68338-110">Installazione di una nuova shell dopo l'installazione di Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="68338-110">Installing a new shell after installing Windows Terminal</span></span>

<span data-ttu-id="68338-111">Dopo l'installazione di una nuova shell, indipendentemente dal fatto che venga eseguita prima o dopo l'installazione del terminale, verrà creato un nuovo profilo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="68338-111">Regardless of whether a new shell is installed before or after your terminal installation, the terminal will create a new profile for the newly installed shell.</span></span>

## <a name="hide-a-profile"></a><span data-ttu-id="68338-112">Nascondere un profilo</span><span class="sxs-lookup"><span data-stu-id="68338-112">Hide a profile</span></span>

<span data-ttu-id="68338-113">Per nascondere un profilo nel menu a discesa del terminale, aggiungi la proprietà `hidden` all'oggetto profilo nel file settings.json e impostala su `true`.</span><span class="sxs-lookup"><span data-stu-id="68338-113">To hide a profile from your terminal dropdown menu, add the `hidden` property to the profile object in your settings.json file and set it to `true`.</span></span>

```json
"hidden": true
```

<span data-ttu-id="68338-114">Se elimini un profilo creato dinamicamente, il terminale lo rigenererà automaticamente e lo sostituirà nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="68338-114">If you delete a dynamically-created profile, the terminal will automatically regenerate the profile and replace it in your settings.json file.</span></span>

## <a name="prevent-a-profile-from-being-generated"></a><span data-ttu-id="68338-115">Impedire la generazione di un profilo</span><span class="sxs-lookup"><span data-stu-id="68338-115">Prevent a profile from being generated</span></span>

<span data-ttu-id="68338-116">Per impedire la generazione di un profilo dinamico, puoi aggiungere il generatore di profili alla matrice `disabledProfileSources` nelle impostazioni globali.</span><span class="sxs-lookup"><span data-stu-id="68338-116">To prevent a dynamic profile from being generated, you can add the profile generator to the `disabledProfileSources` array in your global settings.</span></span> <span data-ttu-id="68338-117">Per altre informazioni su questa impostazione, vedi la [pagina delle impostazioni globali](./customize-settings/global-settings.md#disable-dynamic-profiles).</span><span class="sxs-lookup"><span data-stu-id="68338-117">More information on this setting can be found on the [Global settings page](./customize-settings/global-settings.md#disable-dynamic-profiles).</span></span>

```json
"disabledProfileSources": ["Windows.Terminal.Wsl", "Windows.Terminal.Azure", "Windows.Terminal.PowershellCore"]
```
