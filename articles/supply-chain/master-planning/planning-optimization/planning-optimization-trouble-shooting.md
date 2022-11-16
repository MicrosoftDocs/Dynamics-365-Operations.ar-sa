---
title: استكشاف أخطاء تحسين التخطيط وإصلاحها
description: يوضح هذا المقال كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع تحسين التخطيط.
author: t-benebo
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 37c38ab9cec8ae3c9d4decf8043b43ea2251083e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739719"
---
# <a name="troubleshoot-planning-optimization"></a>استكشاف أخطاء تحسين التخطيط وإصلاحها 

[!include [banner](../../includes/banner.md)]

يوضح هذا المقال كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع تحسين التخطيط.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>عدم إكمال تثبيت الوظيفة الإضافية لتحسين أداء التخطيط

يتطلب تحسين التخطيط توافر بيئة ذات توفر عالي الطبقة 2 أو أعلى مع تمكين Lifecycle Services (LCS) (ليست بيئة OneBox)، مع الإصدار Dynamics 365 Supply Chain Management 10.0.7 أو أحدث. إذا حاولت تثبيت الوظيفة الإضافية في بيئة OneBox، فلن يكتمل التثبيت.

**الإصلاح**: قم بإلغاء التثبيت واستخدم بيئة عالية التوافر، من الطبقة 2 أو أعلى (ليس بيئة OneBox).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>فشل تخطيط الوظائف الدفعية عند تمكين تحسين أداء التخطيط

عند تمكين تحسين التخطيط، يتم تعطيل محرك التخطيط الرئيسي المهمل تلقائيًا. تفشل الوظائف الدفعية للتخطيط الرئيسي التي تم إنشاؤها لمحرك التخطيط الرئيسي المهمل إذا تم تشغيلها أثناء تمكين تحسين التخطيط. قد تتلقي رسالة خطأ مثل *هذه العملية أطلقت عملية تخطيط رئيسي غير مدعومة عند تمكين تحسين التخطيط*.

**الإصلاح**: قم بإلغاء كافة الوظائف الدفعية للتخطيط الرئيسي التي تم إنشاؤها لمحرك التخطيط الرئيسي المهمل.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>تختلف نتائج تحسين التخطيط عن النتائج السابقة

يختلف تحسين التخطيط عن تصميم محرك التخطيط الرئيسي المهمل في بعض المناطق. ويمكن أيضًا أن يحدث ذلك بسبب الميزات المعلقة.

**الإصلاح** : قم بتشغيل تحليل ملاءمة تحسين التخطيط ، ثم قم بتحليل النتائج في حين الرجوع إلى الوثائق ذات الصلة لفهم التأثير. لمزيد من المعلومات، راجع [تحليل ملائمة تحسين التخطيط](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>لا يمكن تمكين تحسين التخطيط

يجب أن تكون **حالة الاتصال** **متصل** قبل أن تتمكن من تعيين **استخدام تحسين التخطيط** إلى **نعم**. لمزيد من المعلومات، راجع [الشروع في العمل مع تحسين التخطيط](get-started.md).

**الإصلاح**: تأكد من تثبيت الوظيفة الإضافية لتحسين أداء التخطيط بنجاح.

## <a name="error-message-is-shown-during-ctp"></a>ظهور رسالة خطأ أثناء CTP

إذا حاولت تشغيل المتاح للتعهد (CTP) من أمر مبيعات عند تمكين تحسين التخطيط، ستتلقى رسالة الخطأ التالية: *هذه العملية أطلقت التخطيط الرئيسي غير المدعوم عند تمكين تحسين أداء التخطيط*.

يرتبط هذا الأمر بميزة معلقة تم تخطيطها كجزء من دعم أوامر الإنتاج.

**الإصلاح:** تجنب حسابات CTP عند تمكين تحسين أداء التخطيط حتى يتوفر دعم CTP.

## <a name="additional-resources"></a>الموارد الإضافية

- [الشروع في العمل مع التخطيط الرئيسي](get-started.md)
- [تحليل ملاءمة تحسين التخطيط](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]