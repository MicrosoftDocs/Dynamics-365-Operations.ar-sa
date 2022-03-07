---
title: تحديث بنية قالب مستند الأعمال
description: يشرح هذا الموضوع كيفيه تحديث بنيه قالب مستند العمل باستخدام ميزه أداره مستندات العمل.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 09813115544701ea3fffb6be06114bcdd63c0ba0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570438"
---
# <a name="update-the-structure-of-a-business-document-template"></a>تحديث بنية قالب مستند الأعمال 

[!include[banner](../includes/banner.md)]

في جزء **بنية القالب** الخاص بمحرر قالب [إدارة مستندات الأعمال](er-business-document-management.md)، يمكنك تعديل قالب مستند أعمال عن طريق [إضافة حقول جديدة](er-bdm-add-field-to-excel-template.md) إلى قالب في Microsoft Excel. ويتم بعد ذلك تحديث بنية القالب تلقائيًا في Dynamics 365 Finance، بحيث يعكس التغييرات التي أجريتها في جزء **بنية القالب**.

يمكنك أيضًا تعديل قالب باستخدام وظيفة Office 365 عبر الإنترنت. علي سبيل المثال، يمكنك أضافه عنصر مسمي جديد، مثل صوره أو شكل، إلى ورقه العمل القابلة للتحرير. في هذه الحالة، لا يتم تحديث بنيه القالب تلقائيا في التمويل، ولا يظهر العنصر الذي قمت بإضافته في جزء **بنية القالب**. قم بتحديث بنيه القالب يدويا في المالية من خلال تحديد **تحديث البنية** في صفحة محرر القالب.

للاطلاع على مزيد من المعلومات حول الميزة، أكمل المثال التالي.

## <a name="example-update-the-structure-of-a-business-document-template"></a>مثال: تحديث بنيه قالب مستند الأعمال

يوضح هذا المثال كيفيه قيام مسؤول النظام بتحديث بنيه قالب مستند العمل في التمويل بعد تعديل القالب في Office Online. توضح الأقسام التالية الخطوات المتضمنة.

### <a name="prepare-a-business-document-template-for-editing"></a>إعداد قالب مستند عمل للتحرير

أكمل الإجراءات التالية في [نظرة عامة على إدارة مستندات الأعمال](er-business-document-management.md).

1. [تكوين معلمات التقارير الإلكترونية](er-business-document-management.md#configure-er-parameters)
2. [استيراد حلول التقارير الإلكترونية](er-business-document-management.md#import-er-solutions)
3. [تمكين إدارة مستندات الأعمال](er-business-document-management.md#enable-business-document-management)
4. [تكوين محددات](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>تحرير قالب مستند أعمال

1. في مساحة عمل **إدارة مستندات الأعمال**، حدد **مستند جديد**.
2. في صفحة **إنشاء قالب جديد**، حدد قالب **فاتورة النص الحر (نموذج التقارير الإلكترونية) (Excel)**.
3. حدد **إنشاء مستند**.
4. في حقل **العنوان**، أدخل **FTI sample Litware**.
5. حدد **موافق** لإنشاء القالب الجديد.

    > [!NOTE]
    > إذا لم تقم بتسجيل الدخول بعد إلى Office Online، فسيتم [توجيهك إلى صفحة تسجيل الدخول إلى Office 365](er-business-document-management.md#frequently-asked-questions). للرجوع إلى بيئة Finance، حدد الزر **رجوع** في المستعرض.

    يتم فتح القالب الجديد للتحرير في عنصر تحكم Excel Online المضمن في صفحة محرر القوالب.

[![استخدام مساحة عمل إدارة مستندات الأعمال للبدء في تحرير قالب مستند الأعمال](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>مراجعة البنية الحالية للقالب القابل للتحرير

1. في Excel Online، ضمن الشريط، ضمن علامة التبويب **طريقة العرض**، في مجموعة **الإظهار**، حدد **خطوط الشبكة**.
2. في القالب القابل للتحرير، حدد المستطيل أعلى عنوان القالب. هذا المستطيل هو صورة تسمي **rptHeaderCompLogo**.
3. إذا كان جزء **بنية القالب** مخفيًا، فحدد **إظهار البنية**.
4. في جزء **بنية القالب**، قم بتوسيع **التقرير \> الفاتورة \> rptHeader \> rptHeaderPart1**.
5. لاحظ أنه في بنية القالب في Finance، يتم عرض عنصر **rptHeaderCompLogo** كعنصر تابع لـ **التقرير \> الفاتورة \> rptHeader \> rptHeaderPart1**.

[![استخدام مساحة عمل إدارة مستندات الأعمال لمراجعة الهيكل الحالي لقالب قابل للتحرير](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>تحديث بنية قالب مستند الأعمال عن طريق حذف صورة

1. في Excel Online، في القالب القابل للتحرير، حدد صورة **rptHeaderCompLogo**.
2. اتبع إحدى الخطوات التالية لحذف الصورة المحددة من القالب القابل للتحرير:

    - حدد المفتاح **Delete** في لوحة المفاتيح.
    - حدد ثم اضغط (أو انقر بزر الماوس الأيمن) فوق الصورة، ثم حدد **قص**.

    > [!NOTE]
    > لا يزال عنصر **rptHeaderCompLogo** موجودًا حاليًا في بنية القالب في Finance، على الرغم من أن الصورة لم تعد مضمنة في قالب Excel.

3. حدد **تحديث البنية** لمزامنة بنيه القالب القابل للتحرير في Excel وFinance.
4. في جزء **بنية القالب**، قم بتوسيع **التقرير \> الفاتورة \> rptHeader \> rptHeaderPart1**.
5. لاحظ أن عنصر **rptHeaderCompLogo** لم يعد مضمنًا في بنية القالب في Finance.

[![استخدام مساحة عمل إدارة مستندات الأعمال لحذف صورة من قالب مستند الأعمال](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>تحديث بنية قالب مستند الأعمال عن طريق إضافة صورة

1. في Excel Online، ضمن الشريط، في علامة التبويب **إدراج** في مجموعة **الرسوم التوضيحية**، حدد **صورة**.
2. حدد **اختيار ملف**، واستعرض إلى الصورة التي تريد إضافتها، وحددها، ثم حدد **موافق**.
3. حدد **إدراج**.
4. انقل الصورة الجديدة حتى تصبح في المكان الصحيح. يقوم Excel بتسمية الصورة افتراضيًا. على سبيل المثال، قد يقوم بتسمية الصورة **صورة 2**.
5. حدد **تحديث البنية** لمزامنة بنيه القالب القابل للتحرير في Excel وFinance.
6. في جزء **بنية القالب**، قم بتوسيع **التقرير \> الفاتورة \> rptHeader \> rptHeaderPart1**.
7. لاحظ أن الصورة الجديدة مضمنة الآن كعنصر في بنية القالب في Finance.

[![استخدام مساحة عمل إدارة مستندات الأعمال لإضافة صورة إلى قالب مستند الأعمال](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>الارتباطات‬ ذات الصلة

[نظرة عامة على إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md)

[نظرة عامة على إدارة مستندات الأعمال](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]