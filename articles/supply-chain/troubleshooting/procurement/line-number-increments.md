---
title: تعرض أوامر الشراء المستوردة أرقام الأسطر غير الصحيحة
description: عند استيراد أوامر الشراء من خلال إدارة البيانات، لن تتبع بنود أمر الشراء الزيادة التي تم تحديدها في معلمات النظام
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475427"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>تعرض أوامر الشراء المستوردة أرقام الأسطر غير الصحيحة

## <a name="symptoms"></a>العلامات

بشكل افتراضي، لا تستخدم أرقام البنود المُنشأة بشكل تلقائي لبنود أوامر الشراء المستوردة عبر كيان البيانات *بنود أمر الشراء V2* زيادة رقم بند النظام المحددة في معلمات النظام. إذا أنشأت أمر شراء بشكل يدوي وأضفت البنود عبر واجهة المستخدم (UI)، يتم زيادة أرقام البنود بشكل صحيح. ومع ذلك، إذا كنت تستخدم إطار عمل إدارة البيانات (DMF)، فإنها لن تزداد بشكل صحيح.

تحدث هذه المشكلة لأن النظام يستخدم أسلوب إطار عمل إدارة البيانات (DMF) لتعيين أرقام البنود إذا لم تكن أرقام البنود معينة في الكيان المستورد، وذلك عند استيراد البنود عبر DMF. تقوم هذه الطريقة دائمًا بزيادة أرقام البنود بمقدار رقم واحد.

## <a name="workaround"></a>حل بديل

تأكد من أن أرقام البنود المطلوبة معطاة بالفعل في حقول أرقام بنود كيان البيانات عندما تستورد بنود أمر الشراء. في هذه الحالة، لن يستبدل DMF أرقام البنود.
