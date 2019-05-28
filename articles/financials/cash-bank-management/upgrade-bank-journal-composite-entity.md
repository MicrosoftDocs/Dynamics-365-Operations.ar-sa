---
title: تحديث الكيان المركب لدفتر يومية البنك
description: تُعد الخطوات التالية مطلوبة لإضافة الحقل BankTransactionType الإضافي إلى BankJournalEntity المركب.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 70db65dca4cfadd1ed8769386b4b437cecc217a2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565898"
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




