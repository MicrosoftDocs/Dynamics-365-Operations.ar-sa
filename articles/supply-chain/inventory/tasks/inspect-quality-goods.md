---
title: فحص جودة البضائع
description: يوضح هذا الإجراء كيفية معالجة أمر جودة.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e9d750f116db62519ac7148f19bf62050430e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "315419"
---
# <a name="inspect-the-quality-of-goods"></a>فحص جودة البضائع

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية معالجة أمر جودة. يمكنك تنفيذ هذا الدليل في شركة بيانات العرض التوضيحي USMF. قبل بدء هذا الإجراء المستخدم كمثال، تحتاج إلى تأكيد أمر الشراء "000016" وترحيل إيصال استلام منتجات. سيؤدي ذلك إلى إنشاء أمر جودة بشكل تلقائي. عادة ما يتم تنفيذ عمليات فحص الجودة من قِبل موظف التحكم في الجودة‬.


## <a name="select-a-quality-order"></a>تحديد أمر جودة
1. انتقل إلى‬ ‏‫إدارة المخزون > المهام الدورية‬ > إدارة الجودة > أوامر الجودة.
2. في القائمة، قم بوضع علامة للصف المحدد.
    * حدد أمر الجودة الذي تم إنشاؤه قبل بدء هذا الإجراء.  

## <a name="record-test-results"></a>تسجيل نتائج الاختبار
1. انقر فوق "النتائج".
2. انقر فوق "تحرير".
3. في الحقل "كمية النتائج‬"، أدخل رقمًا.
4. في القائمة، قم بوضع علامة للصف المحدد.
5. في الحقل "الناتج"، انقر فوق زر القائمة المنسدلة لفتح البحث.
6. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * في هذا المثال، تستند النتيجة إلى ناتج محدد مسبقًا. يمكنك عادة تسجيل نتيجة اختبار أكثر تحديدًا، على سبيل المثال، حجم أو أبعاد أخرى.  
7. في القائمة، انقر فوق الارتباط في الصف المحدد.
8. انقر فوق "حفظ".
9. قم بإغلاق الصفحة.

## <a name="validate-the-quality-order"></a>التحقق من صحة أمر الجودة
1. انقر فوق "التحقق من الصحة‬".
2. في الحقل "تم التحقق بواسطة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
    * حدد المستخدم الذي يجري عملية الفحص.  
3. في القائمة، انقر فوق الارتباط في الصف المحدد.
4. انقر فوق تحديد.
5. انقر فوق "موافق".
6. قم بإغلاق الصفحة.

