---
title: التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 1 - إعداد نموذج البيانات)
description: تصف هذه المقالة كيفية تكوين تنسيق التقارير الإلكترونية (ER) لاستخدام ملفات إداره المستندات (المرفقات) في إخراج التقارير الإلكتروني (ER). (جزء 1)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
- ERSolutionTable, ERSolutionCreateDropDialog
ms.openlocfilehash: f407555eca4c4bd08d09047e9d8f8512cb99d254
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291013"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a>التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 1 - إعداد نموذج البيانات)

[!include [banner](../../includes/banner.md)]

تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية. يمكن تنفيذ هذه الخطوات في أي شركة.

لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".

يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>الوصول إلى قائمة التكوينات التي توفرها Microsoft
1. انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.

    تأكد من أن موفر 'Litware, Inc.' متوفر ومن وضع علامة عليه كنشط.  

2. حدد الموفر 'Litware, Inc.' .
3. انقر فوق "المستودعات".

    إذا كان مخزن من نوع "موارد العمليات" موجودًا بالفعل، فيمكنك تجاوز الخطوات المتبقية في المهمة الفرعية الحالية.  

4. انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.
5. في الحقل "نوع مستودع التكوين"، أدخل "موارد العمليات".
6. انقر فوق إنشاء مستودع.
7. انقر فوق "موافق".

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>الحصول على تكوينات نموذج فاتورة العميل التي توفرها Microsoft
1. انقر فوق "إظهار عوامل التصفية".
2. طبّق عوامل التصفية التالية: أدخل قيمة عامل التصفية "موارد العمليات" في حقل "الاسم" باستخدام عامل التصفية "يبدأ بـ"‬‏‫؛ أدخل قيمة عامل التصفية "" في حقل "الوصف" باستخدام عامل التصفية "يبدأ بـ".
3. انقر فوق "إظهار عوامل التصفية".
4. انقر فوق "فتح".
5. في الشجرة، حدد "نموذج فاتورة العميل".

    حدد تكوين النموذج "نموذج فاتورة العميل" لاستيراده.  

6. انقر فوق "استيراد".

    انقر فوق "استيراد" للإصدار 1 من التكوين المحدد.  

7. انقر فوق نعم.
8. قم بإغلاق الصفحة.
9. قم بإغلاق الصفحة.
10. انقر فوق "تكوينات إعداد التقارير‬".
11. في الشجرة، حدد "نموذج فاتورة العميل".

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>أنشئ النموذج المشتق لدعم الوصول إلى ملفات "إدارة المستندات".
ستقوم بإنشاء تكوين خاص بك لنموذج فاتورة العميل يكون مشتقًا من التكوين الذي توفره Microsoft. سوف تستخدم هذا التكوين لتطبيق الوصول إلى ملفات "إدارة المستندات" وجعله متوفرًا للمستندات الإلكترونية التي ستقوم بإنشائها استنادًا إلى هذا النموذج.  
1. انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.
2. في الحقل "جديد"، أدخل "مشتق من اسم: نموذج فاتورة العميل، Microsoft".
3. في الحقل "الاسم، اكتب "نموذج فاتورة العميل (مخصص)".
4. وانقر فوق إنشاء تكوين.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
