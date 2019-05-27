---
title: استخدام أكواد السبب
description: يمكنك استخدام كود سبب لتوضيح سبب إلغاء اتفاقية مستوى الخدمة (SLA)، أو سبب تجاوز أمر خدمة لحدود الوقت التي قمت بتحديدها في SLA.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33fa7e5f08f09fe109d0507d686315d01e043928
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557746"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="c81a1-103">استخدام أكواد السبب</span><span class="sxs-lookup"><span data-stu-id="c81a1-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c81a1-104">يمكنك استخدام كود سبب لتوضيح سبب إلغاء اتفاقية مستوى الخدمة (SLA)، أو سبب تجاوز أمر خدمة لحدود الوقت التي قمت بتحديدها في SLA.</span><span class="sxs-lookup"><span data-stu-id="c81a1-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="c81a1-105">ويمكنك أيضًا تحديد أن أحد أكواد السبب مطلوب عند إلغاء SLA، أو عندما يتجاوز حد الوقت المدة المحددة في SLA لأمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c81a1-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="c81a1-106">إذا قمت بتحديد أن أحد أكواد السبب مطلوب، فيجب عليك إدخال كود سبب في المواقف التالية:</span><span class="sxs-lookup"><span data-stu-id="c81a1-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="c81a1-107">عندما يتم نقل أمر خدمة إلى مرحلة تقوم بإيقاف تسجيل الوقت في مقابل SLA لأمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c81a1-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="c81a1-108">وقت اعتماد أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c81a1-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="c81a1-109">عندما يتم إيقاف تسجيل الوقت يدويًا.</span><span class="sxs-lookup"><span data-stu-id="c81a1-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="c81a1-110">إعداد أكواد السبب</span><span class="sxs-lookup"><span data-stu-id="c81a1-110">Set up reason codes</span></span>

1.  <span data-ttu-id="c81a1-111">انقر فوق **إدارة الخدمة** \> **الإعداد** \> **أوامر الخدمة** \> **أكواد سبب المرحلة**.</span><span class="sxs-lookup"><span data-stu-id="c81a1-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="c81a1-112">في النموذج **‏‫رموز السبب للمرحلة**، انقر فوق **جديد** لإنشاء رمز سبب جديد.</span><span class="sxs-lookup"><span data-stu-id="c81a1-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="c81a1-113">في الحقل **‏‫رموز السبب للمرحلة**، أدخل رمز سبب فريد خاص بالمرحلة.</span><span class="sxs-lookup"><span data-stu-id="c81a1-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="c81a1-114">في الحقل **الوصف**، أخل وصفًا لرمز السبب الخاص بالمرحلة.</span><span class="sxs-lookup"><span data-stu-id="c81a1-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="c81a1-115">أغلق النموذج لحفظ التغييرات.</span><span class="sxs-lookup"><span data-stu-id="c81a1-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="c81a1-116">طلب أكواد سبب عند إلغاء اتفاقية مستوى الخدمة</span><span class="sxs-lookup"><span data-stu-id="c81a1-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="c81a1-117">انقر فوق **إدارة الخدمة‬** \> **الإعداد** \> **محددات إدارة الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="c81a1-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="c81a1-118">في نموذج **محددات إدارة الخدمة** ، انقر فوق الارتباط **عام** ثم قم بتحديد خانة الاختيار **‏‫رمز سبب الإلغاء‬** .</span><span class="sxs-lookup"><span data-stu-id="c81a1-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="c81a1-119">تقديم أكواد السبب عندما يتجاوز أمر الخدمة حد الوقت المعين بواسطة اتفاقية مستوى الخدمة</span><span class="sxs-lookup"><span data-stu-id="c81a1-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="c81a1-120">انقر فوق **إدارة الخدمة‬** \> **الإعداد** \> **محددات إدارة الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="c81a1-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="c81a1-121">في نموذج **محددات إدارة الخدمة** ، انقر فوق الارتباط **عام** ثم قم بتحديد خانة الاختيار **‏‫رمز سبب ‏‫تجاوز الوقت‬** .</span><span class="sxs-lookup"><span data-stu-id="c81a1-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="c81a1-122">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="c81a1-122">See also</span></span>

[<span data-ttu-id="c81a1-123">تسجيل وقت البدء والتوقف على أمر خدمة</span><span class="sxs-lookup"><span data-stu-id="c81a1-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  


