---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (3 مارس 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 3 مارس 2020.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 793f47526ef828a281750c34da9d763c94971943
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790442"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources (3 مارس 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.2955. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>يتوفر حل Dataverse الآن مع التغييرات التالية:

سيتوفر حل Dataverse قريبًا بالتغييرات التالية:

| ‏‏الوصف | التغيير |
| ----------------------------------------- | --- |
| تغييرات كيان **الوظيفة/المنصب** | تم إضافة **منطقة التعويض**</br>تمت إضافة **الأبعاد المالية** |
| تغييرات كيان **العامل** | تمت إضافة **تسلسل الاسم**</br>تم إضافة **الأعمال من الصفحة الرئيسية**</br>تمت إضافة **اللغة**</br>تمت إضافة **تاريخ الأقدمية**</br>تمت إضاف **تاريخ التفعيل السنوي**</br>تمت إضافة **تاريخ التوظيف الأصلي** |
| تغييرات كيان **التوظيف** | تمت إضافة **الأبعاد المالية**</br>تمت إضافة **سبب الإنهاء**</br>تمت إعادة تسمية **تاريخ الإنهاء** من **تاريخ الانتقال**</br>تمت إضافة **تاريخ فترة الاختبار** |
| تغييرات كيان **عنوان العامل** | تمت إضافة **عنوان الشارع**</br>**سطر العنوان 1**، و **سطر العنوان 2**، و **سطر العنوان 3** المميز للإهلاك |
| كيانات إعداد التعويض المتغيرة الجديدة | **نوع خطة التعويض المتغير**</br>**خطة التعويض المتغيرة**</br>**قواعد الاستحقاق**</br>**مستوى خطة التعويض المتغير** |
| كيان **توظيف تقويم العامل** الجديد | تمت إضافة **كيان تقويم العمل** |
| كيان **تفاصيل المنصب في كشف الرواتب** الجديد | تمت إضافة **تفاصيل المنصب في كشف الرواتب** |
| كيان **العنوان** الجديد | تمت إضافة **العنوان**. سيتم تضمين كيان **العنوان** الجديد في عملية المزامنة بين Human Resources وDataverse. ولن تتم الإشارة إليه من كيانات **منصب الوظيفة** أو **الوظيفة**. |

خلال الأسابيع القليلة التالية، ستتوفر هذه التغييرات الخاصة بالكيانات في كافة البيئات. لتثبيت حل Dataverse الأحدث لـ Human Resources:

1.  انتقل إلى [مركز إدارة Power Platform](https://admin.powerplatform.microsoft.com).

2.  حدد **بيئات**.

3.  ابحث عن البيئة التي تريد ترقيتها. يجب أن تتطابق البيئة مع **اسم البيئة** في قسم **Common Data Service المعلومات** في النموذج **حول** في Human Resources.

4.  حدد البيئة لعرض تفاصيل البيئة.

5.  حدد **إدارة الحلول** في شريط الإجراءات في الجزء العلوي. ستفتح نافذة مستعرض جديدة وتنتقل إلى **مركز إدارة Dynamics 365** في سياق بيئتك.

6.  في قائمة **الحل**، حدد **ارتساء Dynamics 365 Human Resources**.

7.  حدد **ترقية** لتطبيق الحل الأخير.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>مشاكل الاستيراد مع كيان بيانات تسجيل الإجازات (406082)

يمكنك الآن تسجيل موظف في خطة الإجازة الجديدة من النوع نفسه، طالما كان تاريخ التسجيل الجديد يقع بعد تاريخ التسجيل المنتهي الصلاحية للخطة السابقة.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>مشكلة في تصدير أسعار المساهمة في الكيان 401k payrollWorkerEnrolledBenefitDetail في DMF (420700)

يعمل هذا التغيير على تصحيح وظيفة التصدير للكيان **payrollWorkerEnrolledBenefitDetail** لعكس القيم الحالية لمساهمة رب العمل.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>يؤدي البحث في نموذج العامل المبسط إلى ظهور رسالة تشير إلى ضرورة ملف حقل الشخص (402525)

عند البحث عن موظف، ستتوقف عن تلقي رسالة تفيد بأنه يجب عليك ملء حقل **الشخص**.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>عدم عرض قيمة حقل الملاحظة في النموذج إضافة مهارات إضافية (380134)

يعمل هذا التغيير على تصحيح مشكلة عند تخصيص النموذج **إضافة مهارات إضافية** في خدمة الموظف الذاتية‬.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>عدم انتهاء صلاحية خطط التعويض الثابت المتعددة عند نقل الموظفين (389466)

مع هذا التغيير، ستنتهي مدة صلاحية كافة سجلات التعويض الثابت النشطة للمنصب القديم في تاريخ الانتقال.

## <a name="in-preview"></a>قيد المعاينة

أصبحت ميزات المعاينة التالية متوفرة في 3 فبراير 2020:

- **ميزات معاينة الغياب والإجازات** - لمزيد من المعلومات، راجع [ميزات معاينة الإجازات والغياب](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **ميزة معاينة إدارة الميزات** - لمزيد من المعلومات، بما في ذلك المشكلات المعروفة، راجع [نظرة عامة على إدارة الميزات](hr-benefits-management-overview.md).

## <a name="see-also"></a>راجع أيضًا

[المزايا الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]