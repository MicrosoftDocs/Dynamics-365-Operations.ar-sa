---
title: "تحديث الكيان المركب لدفتر يومية البنك"
description: "تُعد الخطوات التالية مطلوبة لإضافة الحقل BankTransactionType الإضافي إلى BankJournalEntity المركب."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 43413aad9d537e518f7276ccab11ce01d23cf13f
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2017

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





