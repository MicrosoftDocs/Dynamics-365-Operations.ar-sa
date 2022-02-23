---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (12 فبراير 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 12 فبراير 2020.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2020
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
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b89e022441f69825d9c9c56ecdbca2e09e461b9e
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526867"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources (12 فبراير 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.2867. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>يجب أن تتمتع الكيانات الموجودة CompFixedEmpls وHcmPersonImage بإمكانية الوصول إليها من OData (414178)

باستخدام إصدار الأسبوع هذا، أصبحت الآن كيانات **CompFixedEmpls** و **HcmPersonImage** عامة ومتاحة بواسطة ODAta.

## <a name="delete-employment-from-common-data-service-doesnt-work-when-employment-details-arent-active-403193"></a>حذف التوظيف من Common Data Service لا ينجح عندما تكون تفاصيل التوظيف غير نشطة (403193)

يسمح هذا التغيير الآن بحذف التوظيف عبر Common Data Service في حالة عدم وجود تفاصيل توظيف نشطة.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>يعمل سير عمل تسجيل الدورة التدريبية على تغيير الحالة إلى مكتمل و أخطاء بعد الموافقة الثانية (409749)

تم تحديث سير عمل تسجيل الدورة التدريبية للسماح لمعتمدين متعددين.

## <a name="in-preview"></a>قيد المعاينة

تتوفر ميزات المعاينة التالية في 3 فبراير، 2020:

- **ميزات معاينة الغياب والإجازات** - لمزيد من المعلومات، راجع [ميزات معاينة الإجازات والغياب](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **ميزة معاينة إدارة الميزات** - لمزيد من المعلومات، بما في ذلك المشكلات المعروفة، راجع [نظرة عامة على إدارة الميزات](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>قريبًا

### <a name="platform-update-32"></a>update 32 للنظام الأساسي 

سيتوفر تحديث النظام الأساسي 32 قريبا. [التعرف على مزيد من المعلومات حول تحديث النظام الأساسي 32 هنا](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

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

## <a name="see-also"></a>راجع أيضًا

[المزايا الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)