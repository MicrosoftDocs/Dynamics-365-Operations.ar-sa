---
title: فحص جودة البضائع
description: يشرح هذا الموضوع كيفية معالجة أمر جودة.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbfb3733cc52f0f8f54ab4388764429387358ee7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011512"
---
# <a name="inspect-the-quality-of-goods"></a>فحص جودة البضائع

[!include [banner](../../includes/banner.md)]

يشرح هذا الموضوع كيفية معالجة أمر جودة. يمكنك تنفيذ هذا الدليل في شركة بيانات العرض التوضيحي USMF. قبل بدء هذا الإجراء المستخدم كمثال، تحتاج إلى تأكيد أمر الشراء "000016" وترحيل إيصال استلام منتجات. سيؤدي ذلك إلى إنشاء أمر جودة بشكل تلقائي. عادة ما يتم تنفيذ عمليات فحص الجودة من قِبل موظف التحكم في الجودة‬.


## <a name="select-a-quality-order"></a>تحديد أمر جودة
1. في جزء التنقل، انتقل إلى **الوحدات النمطية >‬ ‏‫إدارة المخزون > المهام الدورية‬ > إدارة الجودة > أوامر الجودة**.
2. حدد أمر الجودة الذي تم إنشاؤه قبل بدء هذا الإجراء.  

## <a name="record-test-results"></a>تسجيل نتائج الاختبار
1. حدد **النتائج**.
2. حدد **تحرير**.
3. في الحقل **كمية النتائج‬**، أدخل رقمًا.
4. في حقل **النتيجة**، حدد السجل المطلوب في القائمة المنسدلة.  
- في هذا المثال، تستند النتيجة إلى ناتج محدد مسبقًا. يمكنك عادة تسجيل نتيجة اختبار أكثر تحديدًا، على سبيل المثال، حجم أو أبعاد أخرى.  
5. حدد **حفظ**.
6. قم بإغلاق الصفحة.

## <a name="validate-the-quality-order"></a>التحقق من صحة أمر الجودة
1. حدد **التحقق من الصحة**.
2. في الحقل **تم التحقق من الصحة بواسطة‬**، حدد المستخدم الذي يقوم بإجراء الفحص من القائمة المنسدلة.  
3. انقر فوق **تحديد**.
4. حدد **موافق**.
5. قم بإغلاق الصفحة.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]