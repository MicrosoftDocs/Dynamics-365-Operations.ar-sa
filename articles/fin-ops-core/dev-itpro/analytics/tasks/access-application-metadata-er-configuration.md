---
title: الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER
description: تصف المقالة كيف يمكن لمستخدمRegulatory configuration service ‎ تصميم تعيين جديد لنموذج التقارير الإلكترونية (ER) باستخدام بيانات التعريف.
author: kfend
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 7a0947ec255a8d51f236c6c2f397378f44af1b96
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267891"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER

[!include [banner](../../includes/banner.md)]

تشرح الخطوات التالية كيف يمكن لمستخدم Regulatory configuration service (RCS) يؤدي دور مسؤول النظام أو مطور التقارير الإلكترونية تصميم تعيين جديد لنموذج التقارير الإلكترونية (ER) باستخدام بيانات تعريف التطبيق. سيتم الوصول إلى بيانات تعريف التطبيق باستخدام تكوين بيانات تعريف ER الذي يحتوي على عينة من مجموعة بيانات التعريف للوصول إلى حركات التجارة الخارجية. لإكمال هذه الخطوات، في RCS يجب أولاً استكمال الخطوات في المقال، [إنشاء موفري التكوين وتعليمهم كنشطين](er-configuration-provider-mark-it-active-2016-11.md) إجراء. بعد ذلك، أكمل الخطوات في المقال، [إعداد بيانات تعريف التطبيق لاستخدامها في RCS](prepare-application-metadata-rcs.md).

## <a name="prerequisites"></a>المتطلبات الأساسية
1. انتقل إلى **كل مساحات العمل‬** > **إعداد التقارير الإلكترونية**. 
2. تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**. في حالة عدم رؤية موفر التكوين هذا، أكمل الخطوات المذكورة في الإجراء [إنشاء موفرات تكوين وتحديدها بالحالة نشط‬](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="import-metadata-configuration"></a>استيراد ‏‫بيانات التعريف‬ 
1. انقر فوق **تكوينات بيانات التعريف**. 
2. استورد تكوين بيانات تعريف التقارير الإلكترونية التي تحتوي على بيانات التعريف التي تم تكوينها لإنشاء مستندات إلكترونية لشركة التجارة الخارجية. تم تصدير تكوين بيانات تعريف ER هذه كملف XML في حين تم استكمال الخطوات في [تجهيز بيانات تعريف التطبيق المراد استخدامها في RCS](prepare-application-metadata-rcs.md). 
3. انقر فوق **تبادل**. 
4. انقر فوق **تحميل من ملف XML**. 
5. انقر فوق **استعراض** وحدد ملف 'Foreign trade metadata.xml'. 
6. انقر فوق **موافق**. 
7. قم بإغلاق الصفحة. 

## <a name="create-data-model-configuration"></a>إنشاء تكوين نموذج البيانات
1. انقر فوق **تكوينات إعداد التقارير‬**. 
2. انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬. 
3. في حقل **الاسم**، اكتب 'نموذج تجارة خارجية'. 
4. وانقر فوق **إنشاء تكوين**. 
5. انقر فوق **المصمم**. 
6. انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬. 
7. في حقل **الاسم**، اكتب "الجذر"‬. 
8. انقر فوق **إضافة**. 
9. انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬. 
10.    في حقل **الاسم**، اكتب 'حركة'. 
11.    في حقل **نوع الصنف**، حدد **قائمة سجلات**. 
12.    انقر فوق **إضافة**. 
13.    انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬. 
14.    في حقل **الاسم**، اكتب 'كود السلعة'. 
15.    في الحقل **نوع الصنف**، حدد **سلسلة**. 
16.    انقر فوق **إضافة**. 
17.    انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬. 
18.    في حقل **الاسم**، اكتب 'المبلغ المفوتر'. 
19.    في الحقل **نوع الصنف**، حدد **حقيقي**. 
20.    انقر فوق **إضافة**. 
21.    انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬. 
22.    في حقل **الاسم**، اكتب 'التاريخ'. 
23.    في الحقل **نوع الصنف**، حدد **تاريخ**. 
24.    انقر فوق **إضافة**. 
25.    انقر فوق **المرجع الجذر**. 
26.    انقر فوق **موافق**. 
27.    انقر فوق **حفظ**. 
28.    قم بإغلاق الصفحة. 
29.    انقر فوق **تغيير الحالة**. 
30.    انقر فوق **إكمال**. 
31.    انقر فوق **موافق**. 

## <a name="create-model-mapping-configuration"></a>إنشاء تكوين لتعيين نموذج 
1. انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬. 
2. في الحقل **جديد**، أدخل 'تعيين نموذج استنادًا إلى نموذج بيانات التجارة الخارجية'. 
3. في حقل **الاسم**، اكتب 'تعيين تجارة خارجية'. 
4. وانقر فوق **إنشاء تكوين**. 
5. قم بتوسيع قسم **المتطلبات الأساسية‬**. 
6. انقر فوق **تحرير**. 
7. انقر فوق **جديد**. 
8. في القائمة، قم بوضع علامة للصف المحدد. 
9. في حقل **نوع مكون المتطلبات الأساسية**، حدد **التكوين.** 
10.    حدد تكوين **بيانات تعريف التجارة الخارجية**. 
11.    انقر فوق **حفظ**. 
12.    أضفنا المرجع إلى الإصدار 1 من تكوين "بيانات تعريف التجارة الخارجية". سيتم توفير بيانات تعريف التطبيق من هذا التكوين بينما سيتم تصميم تعيين النموذج هذا. 
13.    قم بإغلاق الصفحة. 
14.    انقر فوق **المصمم**. 
15.    انقر فوق **المصمم**. 
16.    في الشجرة، حدد **Dynamics 365 for Operations\سجلات الجداول**. 
17.    انقر فوق **إضافة جذر**. 
18.    في حقل **الاسم**، اكتب '‏‫نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي'. 
19.    حدد سجلات جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**. 
20.    انقر فوق **موافق**. 

> [!NOTE]
> تم عرض الجدولين الوحيدين باعتبارها الجدولين الوحيدين الذين تمت إضافتهما إلى مجموعة بيانات التعريف المستخدمة حاليًا. 

21.    انقر فوق **ربط**. 
22.    في الشجرة، قم بتوسيع **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬**. 
23.    في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي/AmountMST**. 
24.    في الشجرة، قم بتوسيع **الحركة = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬**. 
25.    في الشجرة، حدد **الحركات = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي/مبلغ الفاتورة**. 
26.    انقر فوق **ربط**. 
27.    في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي/TransDate**. 
28.    في الشجرة، حدد **الحركة = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\التاريخ**. 
29.    انقر فوق **ربط**. 
30.    في الشجرة، قم بتوسيع **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\>العلاقات**. 
31.    في الشجرة، قم بتوسيع **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\>Relations\IntrastatCommodity**. 
32.    في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\>Relations\IntrastatCommodity\Code**. 
33.    في الشجرة، حدد **الحركات = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي/كود السلعة**. 
34.    انقر فوق **ربط**. 
35.    انقر فوق **التحقق من الصحة**. 

> [!NOTE]
> لقد نجحنا في ربط عناصر نموذج البيانات مع عناصر مصادر البيانات التي تم وصفها باستخدام تفاصيل بيانات تعريف التطبيق من تكوين بيانات تعريف ER المشار إليها. 
36.    انقر فوق **حفظ**. 
37.    قم بإغلاق الصفحة. 
38.    قم بإغلاق الصفحة. 
39.    عند الحاجة، يمكنك توسيع مجموعة بيانات التعريف الموجودة ثم تصدير الإصدار الجديد المكتمل من تكوين بيانات تعريف التقارير الإلكترونية. ثم يمكنك استيرادها إلى RCS، وتحديث المتطلبات الأساسية لتكوين تعيين النموذج المكوّن الذي يشير إلى إصدار جديد من تكوين بيانات التعريف المستوردة. 

> [!NOTE]
> تعتبر هذه الطريقة للحصول على معلومات حول بيانات تعريف التطبيق الطريقة الوحيدة المتوفرة للتطبيقات المنشورة محليًا (عند استخدام نموذج نشر بيانات العمل المحلية (LBD) أو في الموقع المحلي).
        


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
