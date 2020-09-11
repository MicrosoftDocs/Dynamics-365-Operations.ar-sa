---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (7 فبراير 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 7 فبراير 2020.
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
ms.openlocfilehash: 8ca740c9b839a08bdb8b426ff191bea64febcd15
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712076"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources (7 فبراير 2020)

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.2835. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>لا تظهر تحليلات التعليم الدورة التدريبية إذا كانت الفصول الدراسية فارغه (388289)

تعرض الآن صفحه التحليلات التعليمية الدورة التدريبية إذا كانت الفصل الدراسي فارغا.

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>لا ياخذ بحث المنصب المنطقة الزمنيه في الحساب (405344)

ياخذ البحث عن مناصب مفتوحة الآن حساب المنطقة الزمنيه عند التحقق من الصحة إذا كان المنصب مفتوحا.

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>لا يتم تحديث طريقه عرض تحليل الرصيد الحالي برصيد الاجازه الحالي الصحيح بعد إرسال طلبات المهلة (409756)

يشتمل الرصيد الحالي الآن علي طلبات الوقت التي تم إرسالها.

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