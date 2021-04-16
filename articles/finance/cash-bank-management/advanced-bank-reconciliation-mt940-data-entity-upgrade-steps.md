---
title: الاستيراد المتقدم للتسوية البنكية MT940 - ترقية كيان بيانات مركب
description: يجب إضافة رقم تسلسلي إلى كيان استيراد كشف الحساب البنكي لدعم تنسيق MT940.
author: panolte
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d6534cc0835eabe91ab485e1d71412885d12123f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827424"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>الاستيراد المتقدم للتسوية البنكية MT940 - ترقية كيان بيانات مركب

[!include [banner](../includes/banner.md)]

يجب إضافة رقم تسلسلي إلى كيان استيراد كشف الحساب البنكي لدعم تنسيق MT940. 

استخدم الخطوات التالية لإضافة كيان استيراد كشف الحساب البنكي لدعم التنسيق MT940.

1.  تجميع ومزامنة ما يلي:
    -   الكيان المركب\\BankStatementImportEntity
    -   الكيان\\BankStatementBalanceEntity
    -   الكيان\\BankStatementDocumentEntity
    -   الكيان\\BankStatementEntity
    -   الكيان\\BankStatementLineEntity
    -   الجداول\\BankStatementStaging

2.  إدارة البيانات\\مشاريع البيانات.
    1.  تحميل مشروع (مشاريع) استيراد MT940
        1.  تغيير XSLT.
            -   انقر فوق **عرض الخريط**.
            -   انقر فوق **عرض الخريطة** على مستند كشف الحساب البنكي.
            -   انقر فوق **التحويلات**
            -   احذف الملف BankReconiliation-to-Composite.xslt.
            -   أضف إصدار BankReconiliation-to-Composite.xsl الجديد.

        2.  عرض **الرقم التسلسلي‬** على تخطيط **بيانات المصدر‬**.
            1.  تنسيق بيانات المصدر = عنصر XML.
            2.  اسم الكيان = كشوف الحسابات البنكية.
            3.  تحميل ملف البيانات = إصدار SampleBankCompositeEntity.xml الجديد.
            4.  انقر فوق **نعم** للكتابة فوق الملف الموجود.
            5.  انقر فوق **نعم** لإنشاء تعيين جديد.
            6.  تأكد من تعيين **SequenceNumber**.
                -   انقر فوق **عرض الخريطة** على كيان كشف الحساب.
                -   تأكد من تعيين **SequenceNumber** من المصدر إلى التشغيل المرحلي‬.

3.  استيراد كشف الحساب الجديد.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]