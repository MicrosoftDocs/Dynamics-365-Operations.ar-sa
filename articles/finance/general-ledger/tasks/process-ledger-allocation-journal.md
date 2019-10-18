---
title: ‏‫معالجة دفتر يومية توزيع دفتر الأستاذ‬
description: يشرح هذا الموضوع كيفية معالجة طلب تخصيص في Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 882362a03e4fc4e249b092caea374640813eef88
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186062"
---
# <a name="process-ledger-allocation-journal"></a>‏‫معالجة دفتر يومية توزيع دفتر الأستاذ‬

[!include [task guide banner](../../includes/task-guide-banner.md)]

يشرح هذا الموضوع كيفية معالجة طلب تخصيص. استخدم صفحة طلب تخصيص العملية لإنشاء دفتر يومية تخصيص يمكن مراجعته واعتماده قبل الترحيل إلى دفتر الأستاذ العام أو ترحيله مباشرةً إلى دفتر الأستاذ العام. قبل أن تتمكن من إنشاء دفتر يومية التخصيصات، يجب أن تتوفر قاعدة واحدة نشطة على الأقل لتخصيص دفتر الأستاذ. تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية > دفتر الأستاذ العام > تخصيصات > طلب تخصيص العملية**.
2. في حقل **القاعدة**، حدد السجل المطلوب في القائمة المنسدلة.
3. أدخل تاريخاً في الحقل **اعتبارًا من تاريخ**.

    - يُعد **اعتبارًا من تاريخ** مهمًا جداً عندما يكون دفتر الأستاذ هو مصدر البيانات للقاعدة. يتحكم هذا التاريخ في دفتر الأستاذ المطلوب تضمينه للتخصيص.  
    - في الحقل **قيمة المصدر صفر** حدد **إيقاف**. يؤدي هذا إلى إيقاف عملية التخصيص وعرض رسالة توضح أنه تم تحديد مبلغ بقيمة المصدر صفر.  

4. في الحقل **خيارات المقترح**، حدد **مقترح فقط**. حدد **مقترح فقط** لمراجعة النتيجة الواردة في دفاتر يومية التخصيص واعتمادها قبل ترحيل التخصيص إلى دفتر الأستاذ العام.  
5. في الحقل "ترحيل دفتر الأستاذ العام"، أدخل تاريخًا.
6. حدد **موافق**.
7. في جزء التنقل، انتقل إلى **الوحدات النمطية > دفتر الأستاذ العام > تخصيصات > دفاتر يومية التخصيص**.
8. حدد **البنود**.
9. حدد **ترحيل**.
10. حدد **ترحيل**.
