---
title: Impostazioni del profilo avanzato di Windows Terminal
description: Informazioni su come personalizzare le impostazioni avanzate del profilo nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 0019a96f80e73740d980c9c6e156cf50134f0945
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041971"
---
# <a name="advanced-profile-settings-in-windows-terminal"></a>Impostazioni avanzate del profilo nel terminale di Windows

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

## <a name="suppress-title-changes"></a>Non visualizzare modifiche al titolo

Quando è impostata su `true`, `tabTitle` sostituisce il titolo predefinito della scheda. Tutti i messaggi di modifica del titolo dall'applicazione verranno eliminati. Se `tabTitle` non è impostata, verrà usata `name`. Quando è impostata su `false`, `tabTitle` si comporta normalmente.

**Nome della proprietà:** `suppressApplicationTitle`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

<br />

___

## <a name="text-antialiasing"></a>Anti-aliasing del testo

Controlla la modalità di anti-aliasing del testo nel renderer. La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.

![Terminale Windows - Anti-aliasing del testo](./../images/antialiasing-mode.gif)

**Nome della proprietà:** `antialiasingMode`

**Obbligatoria:** Facoltativo

**Accetta:** `"grayscale"`, `"cleartype"`, `"aliased"`

**Valore predefinito:** `"grayscale"`

<br />

___

## <a name="altgr-aliasing"></a>Aliasing AltGr

Questa proprietà consente di controllare se Terminale Windows considererà <kbd>CTRL+ALT</kbd> come alias di <kbd>ALTGR</kbd>.

**Nome della proprietà:** `altGrAliasing`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

<br />

___

## <a name="scroll-to-input-when-typing"></a>Scorri fino all'input durante la digitazione

Quando è impostata su `true`, la finestra scorre fino alla riga di input del comando durante la digitazione. Quando è impostata su `false`, lo scorrimento della finestra non è attivato quando inizi a digitare.

**Nome della proprietà:** `snapOnInput`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `true`

<br />

___

## <a name="history-size"></a>Dimensioni della cronologia

Consente di impostare il numero di righe a cui è possibile passare scorrendo che precedono quelle visualizzate nella finestra.

**Nome della proprietà:** `historySize`

**Obbligatoria:** Facoltativo

**Accetta:** Intero

**Valore predefinito:** `9001`

<br />

___

## <a name="profile-termination-behavior"></a>Comportamento di terminazione del profilo

Consente di impostare la reazione del profilo alla chiusura o a un errore all'avvio. Con `"graceful"`, il profilo verrà chiuso quando viene digitato `exit` o quando il processo viene chiuso normalmente. Con `"always"` il profilo verrà sempre chiuso, mentre con `"never"` non verrà mai chiuso. `true` e `false` vengono accettati come sinonimi rispettivamente per `"graceful"` e `"never"`.

**Nome della proprietà:** `closeOnExit`

**Obbligatoria:** Facoltativo

**Accetta:** `"graceful"`, `"always"`, `"never"`, `true`, `false`

**Valore predefinito:** `"graceful"`

<br />

___

## <a name="bell-notification-style"></a>Stile notifica campanello

Controlla cosa accade quando l'applicazione emette un carattere BEL. Quando è impostato su `"all"` , il terminale riprodurrà un suono e lampeggerà l'icona della barra delle applicazioni.

**Nome della proprietà:** `bellStyle`

**Obbligatoria:** Facoltativo

**Accetta:** `"all"`, `"audible"`, `"visual"`, `"none"`

**Valore predefinito:** `"audible"`

> [!IMPORTANT]
> Gli `"all"` `"visual"` stili di notifica e Bell sono disponibili solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).

<br />

___

## <a name="unique-identifier"></a>Identificatore univoco

I profili possono usare un GUID come identificatore univoco. Per impostare un profilo come predefinito, è necessario un GUID per l'impostazione globale `defaultProfile`.

**Nome della proprietà:** `guid`

**Obbligatoria:** Obbligatoria

**Accetta:** GUID in formato stringa del Registro di sistema: `"{00000000-0000-0000-0000-000000000000}"`

<br />

___

## <a name="source"></a>Origine

Archivia il nome del generatore di profili che ha originato il profilo. _Non esistono valori individuabili per questo campo._ Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).

**Nome della proprietà:** `source`

**Obbligatoria:** Facoltativo

**Accetta:** String

> [!NOTE]
> Questo campo deve essere omesso quando si dichiara un profilo personalizzato. Viene usato dal terminale per connettere i profili generati automaticamente al file di impostazioni.
