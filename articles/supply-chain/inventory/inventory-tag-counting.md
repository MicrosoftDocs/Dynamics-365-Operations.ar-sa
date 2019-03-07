---
title: جرد علامات المخزون
description: توفر هذه المقالة معلومات حول جرد العلامات‬، الذي تستخدمه لمقارنة المحتويات الفعلية للمستودع بالمخزون الفعلي.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dff899d0e6d94287c0f1924fe1787189d79c09f4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "328943"
---
# <a name="inventory-tag-counting"></a>جرد علامات المخزون

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

توفر هذه المقالة معلومات حول جرد العلامات‬، الذي تستخدمه لمقارنة المحتويات الفعلية للمستودع بالمخزون الفعلي.

‏‫عن طريق إنشاء بنود في صفحة **جرد العلامات**، ضع رقم علامة على كل صنف مخزون، مثل رقم من 1 إلى 500. وأثناء الجرد، يمكنك إدخال رقم الصنف والكمية في علامة مناظرة.‬ ويمكن بعد ذلك استخدام هذه العلامة كأساس للإدخال في دفتر يومية جرد العلامات. وبعد ترحيل دفتر يومية جرد العلامات، يتم إنشاء دفتر يومية جرد جديد في صفحة **الجرد**. ويستند دفتر اليومية الجديد إلى بنود دفتر يومية جرد العلامات الذي قمت بإنشائه. ولجرد الأصناف بالعلامات بواسطة بُعد مخزون محدد، حدد البُعد في صفحة **بُعد العرض** التي يتم عرضها عند إنشاء دفتر يومية جرد العلامات. على سبيل المثال، لحساب عدد الأصناف الموجودة في مستودع معين، حدد خانة الاختيار **مستودع**. إذا تم تحديد شريط التمرير **تأمين الأصناف أثناء الجرد** في صفحة **معلمات إدارة المخزون والمستودعات**، لا يمكن تحديث الأصناف فعلياً أثناء الجرد. ومع ذلك، لا يتم تأمين الأصناف في دفاتر يومية جرد العلامات خلال عملية الجرد. ولا يتم إنشاء حركات المخزون حتى يتم ترحيل ونقل بنود جرد العلامات إلى دفتر يومية جرد. في حالة إدخال العلامات عشوائيًا وكنت ترغب في تحديد العلامات المفقودة، فانقر فوق رأس عمود **العلامة** لفرز البنود حسب العلامة.

<a name="additional-resources"></a>الموارد الإضافية
--------

[الجرد الدوري](../warehousing/cycle-counting.md)
