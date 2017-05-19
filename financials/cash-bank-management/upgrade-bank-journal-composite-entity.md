---
title: "تحديث الكيان المركب لدفتر يومية البنك"
description: "تُعد الخطوات التالية مطلوبة لإضافة الحقل BankTransactionType الإضافي إلى BankJournalEntity المركب."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 364bdff8f8d825cc50760631bb533b531f8b2121
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="update-the-bank-journal-composite-entity"></a>تحديث الكيان المركب لدفتر يومية البنك

[!include[banner](../includes/banner.md)]


تُعد الخطوات التالية مطلوبة لإضافة الحقل BankTransactionType الإضافي إلى BankJournalEntity المركب.

استخدم الخطوات التالية لإضافة الحقل الإضافي BankTransactionType إلى BankJournalEntity المركب.

1.  تجميع ومزامنة الكيانات المركبة التالية لدفتر يومية البنك والكيانات وجداول التشغيل المرحلي:
    -   الكيان المركب‬\\BankJournalEntity
    -   الكيان\\BankJournalHeaderEntity
    -   الكيان\\BankJournalLineEntity
    -   الجدول\\BankJournalHeaderStaging
    -   الجدول\\BankJournalLineStaging

2.  إدارة البيانات\\مشاريع البيانات
    -   عرض نوع **الحركة البنكية** على تخطيط **المصدر المصدر**.
        -   تنسيق بيانات المصدر = عنصر XML
        -   اسم الكيان = دفتر يومية البنك
        -   تحميل ملف البيانات = إصدار SampleBankJournalCompositeEntity.xml الجديد
        -   انقر فوق **نعم** للكتابة فوق الملف الموجود.
        -   انقر فوق **نعم** لإنشاء التعيين منذ البداية.
        -   تأكد من تعيين "نوع الحركة البنكية".
            -   انقر فوق **عرض الخريطة** على كيان البند.
            -   تأكد من تعيين نوع الحركة البنكية من المصدر إلى التشغيل المرحلي‬.

3.  استيراد كشف الحساب الجديد.





