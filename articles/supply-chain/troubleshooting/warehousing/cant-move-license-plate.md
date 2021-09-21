---
title: يتعذر نقل لوحة الترخيص في حالة السماح بإصدار فارغ وإيصال فارغ
description: لا يمكنك نقل لوحة الترخيص إذا كان الرقم التسلسلي يشتمل على إصدار فارغ ويسمح بالإيصال الفارغ. سيتم إصلاح ذلك من خلال جعل حقل الرقم التسلسلي اختيارياً.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475464"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>يتعذر نقل لوحة الترخيص إذا كان الرقم التسلسلي يشتمل على إصدار فارغ ويسمح بإيصال فارغ

## <a name="symptoms"></a>العلامات

لا يمكنك نقل لوحة ترخيص باستخدام عنصر قائمه **الحركة** إذا كان الرقم المسلسل يحتوي على إعدادات *لإصدار فارغ مسموح به* و *تم السماح بإيصال فارغ* في مجموعة بعد التعقب، وإذا كان هناك عده لوحات ترخيص في نفس الموقع ، يكون لبعضها الأرقام التسلسلية وبعضها لا تملكها.

## <a name="resolution"></a>الحل

سيتم حل هذه المشكلة من خلال التغييرات التي يتم نشرها في [قاعدة المعارف 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). ستؤدي هذه التغييرات إلى جعل حقل **الرقم التسلسلي** اختيارياً عند السماح بالاستلام الفارغ والإصدار الفارغ.
