---
title: تتلقى خطأ عند تشغيل محرك التخطيط الرئيسي المضمن
description: عندما تقوم بتشغيل محرك التخطيط الرئيسي المضمن، فإنك تستلم رسالة خطأ.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7c0c674818a21d3ad422661fc427b0b9c4aad52b8d44d08791d2d703be528fe3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751711"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>تتلقى خطأ عند تشغيل محرك التخطيط الرئيسي المضمن

رمز الخطأ: ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>العلامات

عندما تقوم بتشغيل التخطيط الرئيسي باستخدام محرك التخطيط الرئيسي المضمن والمهمل فإنك تستلم رسالة الخطأ التالية:

> تظهر رسالة الخطا هذه بسبب استخدام مشغل التخطيط الرئيسي المضمن للسيناريوهات المعتمدة من قبل تحسين التخطيط. يجب الترحيل إلى التخطيط تحسين الأداء الآن ، حيث سيتم إهمال التخطيط الرئيسي المضمن الحالي. لاحظ ان تشغيل هذا التخطيط الرئيسي قد اكتمل بنجاح. في حاله وجود تبعيات قويه بالميزات المعلقة في الترحيل ، يمكن طلب الاستخدام المستمر لاستخدام محرك التخطيط الرئيسي المضمن. الرجاء إكمال الاستبيان التالي للبدء، وفي حالة استثناء الطلب المناسب من الترحيل إلى تحسين التخطيط. [ترحيل تحسين التخطيط واستبيان الاستثناء](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>السبب

إذا قمت بتشغيل التخطيط ولم تستخدم ميزات التحكم في الإنتاج، فيجب عليك أن تفكر في الترحيل إلى تحسين التخطيط. يتم إهمال محرك التخطيط الرئيسي المضمن. لذلك، إذا كنت تريد متابعة استخدامه دون تلقي رسالة الخطأ، فإنه يجب تطبيق استثناء من Microsoft.

## <a name="resolution"></a>الحل

لمزيد من المعلومات حول كيفية الترحيل إلى تحسين التخطيط، أو كيفية التقدم بطلب للحصول على استثناء بحيث يمكنك الاستمرار في استخدام محرك التخطيط المضمن المهمل بدلاً من ذلك، راجع [الترحيل إلى تحسين التخطيط للتخطيط الرئيسي](/dynamics365/supply-chain/master-planning/new-master-planning-engine).
