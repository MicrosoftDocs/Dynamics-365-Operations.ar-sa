---
title: "تقليل الأيام على رسوم الاشتراك"
description: "لتخفيض عدد الأيام في رسم اشتراك موجود، يمكنك إنشاء حركة جديدة تقوم فيها بإزالة الفترة الزمنية التي لم تعد جزءًا من فترة رسم الاشتراك."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 04b183d8fc8083c630bcb4e0e69fb755f8a50f95
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---


# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="e91fe-103">تقليل الأيام على رسوم الاشتراك</span><span class="sxs-lookup"><span data-stu-id="e91fe-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e91fe-104">لتخفيض عدد الأيام في رسم اشتراك موجود، يمكنك إنشاء حركة جديدة تقوم فيها بإزالة الفترة الزمنية التي لم تعد جزءًا من فترة رسم الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="e91fe-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="e91fe-105">تخفيض الأيام ف رسم اشتراك</span><span class="sxs-lookup"><span data-stu-id="e91fe-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="e91fe-106">انقر فوق **إدارة الخدمة** \> **عام** \> **اشتراكات الخدمة** \> **جميع اشتراكات الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="e91fe-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="e91fe-107">حدد اشتراك الخدمة، ثم في جزء الإجراءات، انقر فوق **رسوم الاشتراك**</span><span class="sxs-lookup"><span data-stu-id="e91fe-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="e91fe-108">في حقل **نوع الاشتراك**، حدد **أيام التخفيض**.</span><span class="sxs-lookup"><span data-stu-id="e91fe-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="e91fe-109">استخدم حقل **تاريخ من** وحقل **تاريخ إلى** لتحديد فترة التاريخ الخاصة برسوم الاشتراك التي تريد إزالتها من فترة رسوم الاشتراك، ثم انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e91fe-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="e91fe-110">لعرض الحركة التي تم إنشاؤها، في النموذج **الاشتراك**، انقر فوق **حركات الرسوم**.</span><span class="sxs-lookup"><span data-stu-id="e91fe-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="e91fe-111">مثال</span><span class="sxs-lookup"><span data-stu-id="e91fe-111">Example</span></span>

<span data-ttu-id="e91fe-112">إذا كانت فترة حركة الاشتراك تبدأ من 1 يناير إلى 31 يناير، وأنت ترغب في تخفيض المدة 15 يومًا، فقم بإنشاء حركة جديدة تبدأ فيها فترة التخفيض من 1 يناير إلى 10 يناير.</span><span class="sxs-lookup"><span data-stu-id="e91fe-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="e91fe-113">(يُمكن أيضًا أن تكون فترة التخفيض من 5 يناير إلى 15 يناير، أو أي فترة عشرة أيام أخرى).</span><span class="sxs-lookup"><span data-stu-id="e91fe-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="e91fe-114">أيضًا إذا كان **من تاريخ** في فترة التخفيض هو 21 يناير (بطرح 10 من 31)، فيُمكنك تعيين **إلى تاريخ** على أي تاريخ بعد 31 يناير، ومع ذلك ستتم إزالة 10 أيام من فترة حركة الرسوم.</span><span class="sxs-lookup"><span data-stu-id="e91fe-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="e91fe-115">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="e91fe-115">See also</span></span>

[<span data-ttu-id="e91fe-116">مثال أيام التخفيض</span><span class="sxs-lookup"><span data-stu-id="e91fe-116">Reduction days example</span></span>](reduction-days-example.md)

  



