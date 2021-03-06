---
title: استكشاف أخطاء تحسين التخطيط وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع تحسين التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8e67a6faf52b51264555b06f56b289d19ca580d6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992485"
---
# <a name="troubleshoot-planning-optimization"></a>استكشاف أخطاء تحسين التخطيط وإصلاحها 

[!include [banner](../../includes/banner.md)]

يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع تحسين التخطيط.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>عدم إكمال تثبيت الوظيفة الإضافية لتحسين أداء التخطيط

يتطلب تحسين التخطيط توافر بيئة ذات توفر عالي الطبقة 2 أو أعلى مع تمكين Lifecycle Services (LCS) (ليست بيئة OneBox)، مع الإصدار Dynamics 365 Supply Chain Management 10.0.7 أو أحدث. إذا حاولت تثبيت الوظيفة الإضافية في بيئة OneBox، فلن يكتمل التثبيت.

**الإصلاح**: قم بإلغاء التثبيت واستخدم بيئة عالية التوافر، من الطبقة 2 أو أعلى (ليس بيئة OneBox).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>فشل تخطيط الوظائف الدفعية عند تمكين تحسين أداء التخطيط

عند تمكين تحسين التخطيط، يتم تعطيل مشغل التخطيط الرئيسي المضمن تلقائيًا. تفشل الوظائف الدفعة للتخطيط الرئيسي التي تم إنشاؤها لمحرك تخطيط Supply Chain Management المضمن إذا تم تشغيلها أثناء تكمين تحسين أداء التخطيط. قد تتلقي رسالة خطأ مثل *هذه العملية أطلقت عملية تخطيط رئيسي غير مدعومة عند تمكين تحسين التخطيط*.

**الإصلاح**: قم بإلغاء كافة الوظائف الدفعية للتخطيط الرئيسي التي تم إنشاؤها لمحرك تخطيط Supply Chain Management المضمن.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>تختلف نتائج تحسين التخطيط عن النتائج السابقة

تختلف نتائج تحسين التخطيط عن تصميم التخطيط الرئيسي المضمن في بعض المناطق. ويمكن أيضًا أن يحدث ذلك بسبب الميزات المعلقة.

**الإصلاح** : قم بتشغيل تحليل ملاءمة تحسين التخطيط ، ثم قم بتحليل النتائج في حين الرجوع إلى الوثائق ذات الصلة لفهم التأثير. لمزيد من المعلومات، راجع [تحليل ملائمة تحسين التخطيط](planning-optimization-fit-analysis.md).

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a>التخطيط الرئيسي لا يحترم الحد الزمني للتغطية

يحدث ذلك بسبب وجود ميزة معلقة لتحسين التخطيط.

**الإصلاح**: حتى تتوفر الميزة المعلقة، قم بتصفية الأوامر المخططة أو حذفها الإزالة اقتراحات التوريد خارج الحد الزمني للتغطية.

## <a name="cant-enable-planning-optimization"></a>لا يمكن تمكين تحسين التخطيط

يجب أن تكون **حالة الاتصال** **متصل** قبل أن تتمكن من تعيين **استخدام تحسين التخطيط** إلى **نعم**. لمزيد من المعلومات، راجع [الشروع في العمل مع تحسين التخطيط](get-started.md).

**الإصلاح**: تأكد من تثبيت الوظيفة الإضافية لتحسين أداء التخطيط بنجاح.

## <a name="error-message-is-shown-during-ctp"></a>ظهور رسالة خطأ أثناء CTP

إذا حاولت تشغيل المتاح للتعهد (CTP) من أمر مبيعات عند تمكين تحسين التخطيط، ستتلقى رسالة الخطأ التالية: *هذه العملية أطلقت التخطيط الرئيسي غير المدعوم عند تمكين تحسين أداء التخطيط*.

يرتبط هذا الأمر بميزة معلقة تم تخطيطها كجزء من دعم أوامر الإنتاج.

**الإصلاح:** تجنب حسابات CTP عند تمكين تحسين أداء التخطيط حتى يتوفر دعم CTP.

## <a name="additional-resources"></a>الموارد الإضافية

[بدء تحسين التخطيط](get-started.md)

[تحليل ملاءمة تحسين التخطيط](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]