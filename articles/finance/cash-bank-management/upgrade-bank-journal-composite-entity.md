---
title: تحديث الكيان المركب لدفتر يومية البنك
description: تُعد الخطوات التالية مطلوبة لإضافة الحقل BankTransactionType الإضافي إلى BankJournalEntity المركب.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6c990208f26dde26b7adc306198f7cd16e0e69b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978904"
---
# <a name="update-the-bank-journal-composite-entity"></a>تحديث الكيان المركب لدفتر يومية البنك

[!include [banner](../includes/banner.md)]

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






[!INCLUDE[footer-include](../../includes/footer-banner.md)]