---
title: Cascadia Code in Terminale Windows
description: Informazioni sui diversi tipi di carattere Cascadia Code e sul relativo funzionamento con Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: overview
ms.service: terminal
ms.openlocfilehash: c2d9b8461c168639f1453050e18f0650afb738fb
ms.sourcegitcommit: d8e23557224bc50a82a36dc80ac68b9d11dfdde9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "84720097"
---
# <a name="cascadia-code"></a>Cascadia Code

Cascadia Code è un nuovo tipo di carattere Microsoft con spaziatura fissa che offre una nuova esperienza con le applicazioni da riga di comando e gli editor di testo. Cascadia Code è stato sviluppato insieme a Terminale Windows. L'uso di questo tipo di carattere è particolarmente consigliato con applicazioni di terminale e editor di testo come Visual Studio e Visual Studio Code.

## <a name="cascadia-code-versions"></a>Versioni di Cascadia Code

Sono disponibili più versioni di Cascadia Code che includono legature e glifi. Tutte le versioni di Cascadia Code possono essere scaricate dalla [pagina di versioni di Cascadia Code in GitHub](https://github.com/microsoft/cascadia-code/releases). Il pacchetto di Terminale Windows include Cascadia Code e Cascadia Mono, quest'ultimo usato per impostazione predefinita.

| Nome del tipo carattere | Include legature | Include glifi di Powerline |
| --------- | ------------------ | ------------------------- |
| Cascadia Code | Sì | No |
| Cascadia Mono | No  | No |
| Cascadia Code PL | Sì | Sì |
| Cascadia Mono PL | No | Sì |

## <a name="powerline-and-programming-ligatures"></a>Legature di Powerline di programmazione

Powerline è un plug-in comune della riga di comando che consente di visualizzare altre informazioni nel prompt. Per la corretta visualizzazione di queste informazioni, usa alcuni glifi aggiuntivi. Per altre informazioni sulla configurazione di Powerline nel prompt dei comandi, vedi la pagina [Powerline in Terminale Windows](./tutorials/powerline-setup.md).

Le legature di programmazione sono glifi creati combinando caratteri. Sono particolarmente utili per la scrittura di codice. Le varianti "Code" includono legature, mentre le varianti "Mono" no.

![Legature di programmazione di Cascadia Code](./images/programming-ligatures.gif)

## <a name="contributing-to-cascadia-code"></a>Aggiunta di contributi a Cascadia Code

Cascadia Code è concesso in licenza [SIL Open Font](https://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL) in [GitHub](https://github.com/microsoft/cascadia-code).
