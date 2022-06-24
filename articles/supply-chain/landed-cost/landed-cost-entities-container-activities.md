---
title: كيان أنشطة الحاوية
description: يوفر هذا المقال معلومات حول أنشطة الحاويات، والتي تُستخدم لتتبع تقدم حاويات الشحن.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: b69d26ee8abaa403f6a0ef3b03d9015fe507dd5b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873945"
---
# <a name="container-activities-entity"></a>كيان أنشطة الحاويات

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

تُستخدم أنشطة الحاويات لتتبع تقدم حاويات الشحن. يتم إنشاء سجل لكل جزء تم تعيينه لقالب الرحلة الذي تم تحديده في وقت إنشاء حاوية الشحن. يتم أيضًا إنشاء السجلات عند إنشاء حاوية الشحن عبر كيان بيانات.

غالبًا ما يتم تلقي معلومات حول تقدم حاوية الشحن العابر من مصدر خارجي. يمكّن كيان أنشطة الحاوية مصدرًا خارجيًا مثل وكيل الشحن لتحديث السجل مباشرةً. لذلك، لا يلزم إجراء تحديث يدوي للبيانات.

## <a name="container-activities-itmcontaineractivityentity"></a>أنشطة الحاويات (ITMContainerActivityEntity)

يمكنك استخدام كيان أنشطة الحاوية (`ITMContainerActivityEntity`) لإنشاء سجلات نشاط إضافية. وبدلاً من ذلك، يمكن لوكيل الشحن تمرير التحديثات لقيمة **تاريخ انتهاء فعلي** مؤكدة.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| تاريخ الانتهاء الفعلي | ITMContainerActivityTable.ActualEndDate | التاريخ والوقت | لا | لا |
| وضع التسليم | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | لا | لا |
| تاريخ النهاية المقدر | ITMContainerActivityTable.EsimatedDate | التاريخ والوقت | لا | لا |
| رقم البند | ITMContainerActivityTable.LineNum | Numeric(32, 16) | **نعم** | لا |
| الإشعارات | ITMContainerActivityTable.Notes | nvarchar(MAX) | لا | لا |
| نشاط | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | لا | **نعم** |
| حاوية الشحن | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **نعم** | **نعم** |
| الرحلة البحرية | ITMContainerActivityTable.ShipId | Nvarchar(20) | **نعم** | **نعم** |
| الشُعبة | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | لا | **نعم** |
| موفر الخدمة | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | لا | لا |
| درجة الحرارة | ITMContainerActivityTable.ShipTemperature | Numeric(32, 6) | لا | لا |
| الباخرة | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | لا | لا |
| تاريخ البدء | ITMContainerActivityTable.StartDate | التاريخ والوقت | لا | لا |

## <a name="tracking-control"></a>مراقبة التعقب

يتيح مركز مراقبة التعقب تحديث حقل مصدر محدد ليتم تشغيله عن طريق تحديث حقل هدف محدد. إذا تم تحديث كل من قيمة الحقل المصدر وقيمة الحقل الهدف باستخدام كيان أنشطة الحاوية، فسيعرض الحقل الهدف قيمة الكيان. يرتبط هذا السلوك بتتبع سجلات التحكم التي لها قيمة **نوع الإنشاء** الخاص بـ *وقت المهلة*.

بالنسبة لمناطق التكلفة التي تحتوي على قيمة **نوع الإنشاء** الخاص بـ *تحديث الحالة* أو *فارغ* (وهي قيمة محددة من قبل المستخدم)، النظام سيقوم بتحديث حالة الرحلة أو الحقل المستهدف وفقًا لتكوين التحكم في التتبع.

## <a name="calculated-fields"></a>الحقول المحسوبة

يتم حساب قيم الحقول التالية في سجل نشاط الحاوية بناءً على قيم الحقول الأخرى. على الرغم من عدم تضمين هذه الحقول المحسوبة في كيان البيانات، إلا أنه سيتم تعيينها إذا تم توفير الحقول التي تستند إليها العمليات الحسابية.

- **الأيام المقدرة** = **تاريخ الانتهاء المقدر** – **تاريخ البدء**
- **الأيام الفعلية** = **تاريخ الانتهاء الفعلي** – **تاريخ البدء**
