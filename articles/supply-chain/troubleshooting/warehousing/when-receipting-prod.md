---
title: تتم طباعة تسمية واحدة فقط لرؤوس العمل المتعددة في إيصال واحد
description: تتم طباعة تسمية واحدة فقط لرؤوس العمل المتعددة في إيصال واحد.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026234"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>تتم طباعة تسمية واحدة فقط لرؤوس العمل المتعددة في إيصال واحد

رقم KB: 4614667

## <a name="symptoms"></a>العلامات

يتم إنشاء العديد من رؤوس العمل لنفس لوحة الترخيص الهدف كجزء من حدث استلام تطبيق مستودع واحد. ومع ذلك، تتم طباعة تسمية واحدة فقط من لوحات التراخيص عند استلام المنتج.

## <a name="resolution"></a>الدقة

يعمل النظام كما هو مصمم.

في التصميم الحالي، يتم دائمًا إنشاء تسمية لوحة ترخيص واحدة، بغض النظر عن عدد مجموعات أسطر العمل ورأس العمل الموجودة. تتضمن التسمية التي تم إنشاؤها المعلومات الخاصة بمجموعة واحدة فقط.

لحل هذه المشكلة، تأكد من تعيين رأس العمل دائمًا إلى لوحة ترخيص هدف واحد فقط.
