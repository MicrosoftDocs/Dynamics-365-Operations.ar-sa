---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (25 فبراير 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 25 فبراير 2020.
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1302686aeba52de484ad520efe292fafefc39ebf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526800"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources (25 فبراير 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.2927. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>تمكين التنقل في إدارة الحالات‬ وكيان إطار عمل إدارة البيانات (DMF) ‏(414754)

تقوم ميزة المعاينة هذه بتمكين التنقل الإضافي إلى حالات إدارة الحالات. يمكنك تمكين ميزة المعاينة هذه في مساحة عمل **إدارة الميزات**. تظهر عناصر القائمة هذه في مساحة عمل **التوافق** Dynamics 365 Human Resources. ومع هذا التغيير، بإمكان Human Resources الوصول إلى:

- كل الحالات
- الحالات الخاصة بي
- الحالات المفتوحة  
- حالات التأخر
- الحالات المعيَّنة لي خلال سير العمل

إلى جانب طرق العرض الجديدة هذه، يتوفر أيضًا كيان DMF **تفاصيل الحالة**

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>تمكين تعريفات العلاقة في دفتر العناوين العمومي (414762)

تم الآن تمكين العلاقات في دفتر العناوين العمومي. قبل إصدار هذا الأسبوع، عرض مربع الحقائق **العلاقة** أي علاقات معرفة من قبل النظام. يمكنك الآن تعريف هذه العلاقات داخل صفحة دفتر العناوين العمومي.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>يمكن إزالة منصب عند وجود سجلات تعويضات نشطة للمنصب (414568)

مع هذا التغيير، يظهر تحذير عندما تحاول حذف منصب وهناك سجل تعويض نشط لدى العامل لهذا المنصب نفسه. وعند حدوث ذلك، يجب تحديث سجل التعويض الثابت للموظف قبل إزالة المنصب.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>يقوم سير عمل مراجعة الأداء في بعض الأحيان بإضافة عمليات الاعتماد من أشخاص لا يشكلون جزءًا من العملية (414171)

يعمل هذا التغيير على تصحيح مشكلة حيث تتم فيها إضافة مشاركين إضافيين إلى عمليات الاعتماد إلى مراجعة الأداء.

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a>لم يتم إنشاء تعيين منصب العامل في Common Data Service عند تحديده في مربع الحوار "عامل جديد" (413479)

يعمل هذا التغيير على تصحيح مشكل عند توظيف عامل جديد وتعيين الموظف الجديد إلى منصب في مربع حوار **عامل جديد**. يظهر الآن تعيين المنصب في Common Data Service.

## <a name="coming-soon"></a>قريبًا

### <a name="updated-common-data-service-solution"></a>حل Common Data Service المحدث

سيتوفر حل Common Data Service قريبًا بالتغييرات التالية:

| ‏‏الوصف | التغيير |
| ----------------------------------------- | --- |
| تغييرات كيان **الوظيفة/المنصب** | تم إضافة **منطقة التعويض**</br>تمت إضافة **الأبعاد المالية** |
| تغييرات كيان **العامل** | تمت إضافة **تسلسل الاسم**</br>تم إضافة **الأعمال من الصفحة الرئيسية**</br>تمت إضافة **اللغة**</br>تمت إضافة **تاريخ الأقدمية**</br>تمت إضاف **تاريخ التفعيل السنوي**</br>تمت إضافة **تاريخ التوظيف الأصلي** |
| تغييرات كيان **التوظيف** | تمت إضافة **الأبعاد المالية**</br>تمت إضافة **سبب الإنهاء**</br>تمت إعادة تسمية **تاريخ الإنهاء** من **تاريخ الانتقال**</br>تمت إضافة **تاريخ فترة الاختبار** |
| تغييرات كيان **عنوان العامل** | تمت إضافة **عنوان الشارع**</br>**سطر العنوان 1**، و **سطر العنوان 2**، و **سطر العنوان 3** المميز للإهلاك |
| كيانات إعداد التعويض المتغيرة الجديدة | **نوع خطة التعويض المتغير**</br>**خطة التعويض المتغيرة**</br>**قواعد الاستحقاق**</br>**مستوى خطة التعويض المتغير** |
| كيان **توظيف تقويم العامل** الجديد | تمت إضافة **كيان تقويم العمل** |
| كيان **تفاصيل المنصب في كشف الرواتب** الجديد | تمت إضافة **تفاصيل المنصب في كشف الرواتب** |
| كيان **العنوان** الجديد | تمت إضافة **العنوان**. سيتم تضمين كيان **العنوان** الجديد في عملية المزامنة بين Human Resources وCommon Data Service. ولن تتم الإشارة إليه من كيانات **منصب الوظيفة** أو **الوظيفة**. |

خلال الأسابيع القليلة التالية، ستتوفر هذه التغييرات الخاصة بالكيانات في كافة البيئات. لتثبيت حل Common Data Service الأحدث لـ Human Resources:

1.  انتقل إلى [مركز إدارة Power Platform](https://admin.powerplatform.microsoft.com).

2.  حدد **بيئات**.

3.  ابحث عن البيئة التي تريد ترقيتها. يجب أن تتطابق مع **اسم البيئة** في قسم **Common Data Service المعلومات** في النموذج **حول** في Human Resources.

4.  حدد البيئة لعرض تفاصيل البيئة.

5.  حدد **إدارة الحلول** في شريط الإجراءات في الجزء العلوي. ستفتح نافذة مستعرض جديدة وتنتقل إلى **مركز إدارة Dynamics 365** في سياق بيئتك.

6.  في قائمة **الحل**، حدد **ارتساء Dynamics 365 Human Resources**.

7.  حدد **ترقية** لتطبيق الحل الأخير.

## <a name="in-preview"></a>قيد المعاينة

أصبحت ميزات المعاينة التالية متوفرة في 3 فبراير 2020:

- **ميزات معاينة الغياب والإجازات** - لمزيد من المعلومات، راجع [ميزات معاينة الإجازات والغياب](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **ميزة معاينة إدارة الميزات** - لمزيد من المعلومات، بما في ذلك المشكلات المعروفة، راجع [نظرة عامة على إدارة الميزات](hr-benefits-management-overview.md).

## <a name="see-also"></a>راجع أيضًا

[المزايا الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)