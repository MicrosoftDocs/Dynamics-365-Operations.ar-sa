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
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294003"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="3ffa4-103">تتلقى خطأ عند تشغيل محرك التخطيط الرئيسي المضمن</span><span class="sxs-lookup"><span data-stu-id="3ffa4-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="3ffa4-104">رمز الخطأ: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="3ffa4-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="3ffa4-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="3ffa4-105">Symptoms</span></span>

<span data-ttu-id="3ffa4-106">عندما تقوم بتشغيل التخطيط الرئيسي باستخدام محرك التخطيط الرئيسي المضمن والمهمل فإنك تستلم رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="3ffa4-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="3ffa4-107">تظهر رسالة الخطا هذه بسبب استخدام مشغل التخطيط الرئيسي المضمن للسيناريوهات المعتمدة من قبل تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="3ffa4-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="3ffa4-108">يجب الترحيل إلى التخطيط تحسين الأداء الآن ، حيث سيتم إهمال التخطيط الرئيسي المضمن الحالي.</span><span class="sxs-lookup"><span data-stu-id="3ffa4-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="3ffa4-109">لاحظ ان تشغيل هذا التخطيط الرئيسي قد اكتمل بنجاح.</span><span class="sxs-lookup"><span data-stu-id="3ffa4-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="3ffa4-110">في حاله وجود تبعيات قويه بالميزات المعلقة في الترحيل ، يمكن طلب الاستخدام المستمر لاستخدام محرك التخطيط الرئيسي المضمن.</span><span class="sxs-lookup"><span data-stu-id="3ffa4-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="3ffa4-111">الرجاء إكمال الاستبيان التالي للبدء، وفي حالة استثناء الطلب المناسب من الترحيل إلى تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="3ffa4-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="3ffa4-112">ترحيل تحسين التخطيط واستبيان الاستثناء</span><span class="sxs-lookup"><span data-stu-id="3ffa4-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="3ffa4-113">السبب</span><span class="sxs-lookup"><span data-stu-id="3ffa4-113">Cause</span></span>

<span data-ttu-id="3ffa4-114">إذا قمت بتشغيل التخطيط ولم تستخدم ميزات التحكم في الإنتاج، فيجب عليك أن تفكر في الترحيل إلى تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="3ffa4-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="3ffa4-115">يتم إهمال محرك التخطيط الرئيسي المضمن.</span><span class="sxs-lookup"><span data-stu-id="3ffa4-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="3ffa4-116">لذلك، إذا كنت تريد متابعة استخدامه دون تلقي رسالة الخطأ، فإنه يجب تطبيق استثناء من Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3ffa4-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="3ffa4-117">الحل</span><span class="sxs-lookup"><span data-stu-id="3ffa4-117">Resolution</span></span>

<span data-ttu-id="3ffa4-118">لمزيد من المعلومات حول كيفية الترحيل إلى تحسين التخطيط، أو كيفية التقدم بطلب للحصول على استثناء بحيث يمكنك الاستمرار في استخدام محرك التخطيط المضمن المهمل بدلاً من ذلك، راجع [الترحيل إلى تحسين التخطيط للتخطيط الرئيسي](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span><span class="sxs-lookup"><span data-stu-id="3ffa4-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
