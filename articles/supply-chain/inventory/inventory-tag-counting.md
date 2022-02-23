---
title: جرد علامات المخزون
description: توفر هذا الموضوع معلومات حول جرد العلامات‬، الذي تستخدمه لمقارنة المحتويات الفعلية للمستودع بالمخزون الفعلي.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb555cdfbcf3fd0c10ec0e2abcdbe7f4a90d82d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421124"
---
# <a name="inventory-tag-counting"></a>جرد علامات المخزون

[!include [banner](../includes/banner.md)]

توفر هذا الموضوع معلومات حول جرد العلامات‬، الذي تستخدمه لمقارنة المحتويات الفعلية للمستودع بالمخزون الفعلي.

‏‫عن طريق إنشاء بنود في صفحة **جرد العلامات**، ضع رقم علامة على كل صنف مخزون، مثل رقم من 1 إلى 500. وأثناء الجرد، يمكنك إدخال رقم الصنف والكمية في علامة مناظرة.‬ ويمكن بعد ذلك استخدام هذه العلامة كأساس للإدخال في دفتر يومية جرد العلامات. وبعد ترحيل دفتر يومية جرد العلامات، يتم إنشاء دفتر يومية جرد جديد في صفحة **الجرد**. ويستند دفتر اليومية الجديد إلى بنود دفتر يومية جرد العلامات الذي قمت بإنشائه. ولجرد الأصناف بالعلامات بواسطة بُعد مخزون محدد، حدد البُعد في صفحة **بُعد العرض** التي يتم عرضها عند إنشاء دفتر يومية جرد العلامات. على سبيل المثال، لحساب عدد الأصناف الموجودة في مستودع معين، حدد خانة الاختيار **مستودع**. إذا تم تحديد شريط التمرير **تأمين الأصناف أثناء الجرد** في صفحة **معلمات إدارة المخزون والمستودعات**، لا يمكن تحديث الأصناف فعلياً أثناء الجرد. ومع ذلك، لا يتم تأمين الأصناف في دفاتر يومية جرد العلامات خلال عملية الجرد. ولا يتم إنشاء حركات المخزون حتى يتم ترحيل ونقل بنود جرد العلامات إلى دفتر يومية جرد. في حالة إدخال العلامات عشوائيًا وكنت ترغب في تحديد العلامات المفقودة، فانقر فوق رأس عمود **العلامة** لفرز البنود حسب العلامة.

## <a name="additional-resources"></a>الموارد الإضافية

[الجرد الدوري](../warehousing/cycle-counting.md)
