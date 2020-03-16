---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (18 فبراير 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 96e66c86e98cc1cfee82221da06f9c57a17d170b
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077451"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources (18 فبراير 2020)

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.2903. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.

## <a name="platform-update-32"></a>update 32 للنظام الأساسي 

التحديث الخاص بالنظام الأساسي 32 متوفر الآن. لمزيد من المعلومات، راجع [المزايا الجديدة أو المتغيرة في تحديث النظام الأساسي 32 لتطبيقات Finance and Operations (فبراير 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>يتم تذكر قيم البحث عند تغيير خيارات العرض في نموذج موظف المبسط (383833)

يحتفظ الآن نموذج **العامل** بقيم البحث عند تغيير خيارات العرض وتطبيق التغييرات.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>إطارات ملخص إدارة التعويض في إعادة توجيه ميزة المعاينة إلى نموذج خاطئ (401861)

تعرض الآن تجانبات إدارة التعويض الثابتة والمتغيرة السجلات الصحيحة في نموذج **العامل** الجديد. ينطبق فقط على ميزة معاينة نموذج الموظف المبسط. يمكنك تمكين ميزة المعاينة هذه في **إدارة الميزات**. لمزيد من المعلومات، راجع [إدارة الميزات](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a>حقل الحالة فارغ لبعض سجلات طلب الإجازة في Common Data Service (414915)

يعمل هذا التغيير على تصحيح مشكلة في Common Data Service عندما يتم تعيين حقل **الحالة** في طلب إجازة إلى **المراجعة**. Common Data Service يعكس الآن الحالة.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>يكون تحليل فروق المهارات ممكنًا للوظيفة المعينة (411390) فقط

يمكنك الآن القيام بتحليل فروق المهارات في أي وظيفة محددة في Human Resources.

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a>لا تتم مزامنة عملة النظام من Common Data Service إلى Human Resources في البيئات الجديدة (418011)

الآن، يمكن أن تتزامن عملة النظام في Common Data Service إلى Human Resources.

## <a name="in-preview"></a>قيد المعاينة

- [ميزات مُعاينة الإجازة والغياب](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [ميزة معاينة إدارة المزايا](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>قريبًا

### <a name="updated-common-data-service-solution"></a>حل Common Data Service المحدث

سيتوفر حل Common Data Service قريبًا بالتغييرات التالية:

| ‏‏الوصف | التغيير |
| ----------------------------------------- | --- |
| تغييرات كيان **الوظيفة/المنصب** | تم إضافة **منطقة التعويض**</br>تمت إضافة **الأبعاد المالية** |
| تغييرات كيان **العامل** | تمت إضافة **تسلسل الاسم**</br>تم إضافة **الأعمال من الصفحة الرئيسية**</br>تمت إضافة **اللغة**</br>تمت إضافة **تاريخ الأقدمية**</br>تمت إضاف **تاريخ التفعيل السنوي**</br>تمت إضافة **تاريخ التوظيف الأصلي** |
| تغييرات كيان **التوظيف** | تمت إضافة **الأبعاد المالية**</br>تمت إضافة **سبب الإنهاء**</br>تمت إعادة تسمية **تاريخ الإنهاء** من **تاريخ الانتقال**</br>تمت إضافة **تاريخ فترة الاختبار** |
| تغييرات كيان **عنوان العامل** | تمت إضافة **عنوان الشارع**</br>**سطر العنوان 1**، و**سطر العنوان 2**، و**سطر العنوان 3** المميز للإهلاك |
| كيانات إعداد التعويض المتغيرة الجديدة | **نوع خطة التعويض المتغير**</br>**خطة التعويض المتغيرة**</br>**قواعد الاستحقاق**</br>**مستوى خطة التعويض المتغير** |
| كيان **توظيف تقويم العامل** الجديد | تمت إضافة **كيان تقويم العمل** |
| كيان **تفاصيل المنصب في كشف الرواتب** الجديد | تمت إضافة **تفاصيل المنصب في كشف الرواتب** |
| كيان **العنوان** الجديد | تمت إضافة **العنوان**. سيتم تضمين كيان **العنوان** الجديد في عملية المزامنة بين Human Resources وCommon Data Service. ولن تتم الإشارة إليه من كيانات **منصب الوظيفة** أو **الوظيفة**. |

## <a name="see-also"></a>راجع أيضًا

[المزايا الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)
