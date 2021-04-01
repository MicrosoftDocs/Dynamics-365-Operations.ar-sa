---
title: " تحديد نقاط مكافآت الولاء"
description: يتناول هذا الإجراء تحديد نقاط مكافآت الولاء.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bb190e720e5040d446d75a2e8c39cb360019d42
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256867"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="7e2f3-103"> تحديد نقاط مكافآت الولاء</span><span class="sxs-lookup"><span data-stu-id="7e2f3-103">Define loyalty reward points</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e2f3-104">يتناول هذا الإجراء تحديد نقاط مكافآت الولاء.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="7e2f3-105">ينبغي إعداد نقاط مكافآت الولاء قبل إعداد برنامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="7e2f3-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="7e2f3-107">انتقل إلى البيع بالتجزئة والتجارة > العملاء > الولاء > نقاط مكافآت الولاء.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="7e2f3-108">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-108">Click New.</span></span>
3. <span data-ttu-id="7e2f3-109">في حقل "‏‫معرف نقطة المكافأة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="7e2f3-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7e2f3-111">في حقل "نوع نقطة المكافأة"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="7e2f3-112">حدد الكمية إذا أردت تقريب نقاط المكافآت إلى أقرب عدد صحيح.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="7e2f3-113">حدد المبلغ إذا أردت تقريب نقاط المكافآت وفقًا لقواعد تقريب العملة.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="7e2f3-114">وإذا قمت بتحديد الكمية، فقم بتخطي الخطوة التالية من هذا الإجراء..</span><span class="sxs-lookup"><span data-stu-id="7e2f3-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="7e2f3-115">في الحقل "العملة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="7e2f3-116">للحصول على نقاط مكافآت نوع المبلغ، ستكون كافة النقاط التي تم إصدارها بالعملة المحددة.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="7e2f3-117">للحصول على نقاط مكافآت نوع الكمية، لا ينطبق هذا الحقل، يمكنك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="7e2f3-118">حدد خانة الاختيار "‏‫قابل للاسترجاع" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="7e2f3-119">في حقل "‏‫استرجاع التقييم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="7e2f3-120">يُستخدم ‏‫استرجاع التقييم عندما يمكن استخدام نقطتين أو أكثر من نقاط المكافآت القابلة للاسترجاع لدفع ثمن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="7e2f3-121">إذا كان لنقطتي المكافآت نفس استرجاع التقييم، فسيتم استخدام النقطة التي تحتاج إلى عدد أقل من النقاط.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="7e2f3-122">في حقل "‏‫قيمة وقت انتهاء الصلاحية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="7e2f3-123">ستنتهي مدة صلاحية نقاط المكافآت بعدما يتم إصدار النقاط بعدد محدد من الأيام أو الشهور أو السنوات.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="7e2f3-124">وتعني قيمة "0" أن نقاط مكافآت الولاء لن تنتهي صلاحيتها أبدًا.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-124">A value of '0' means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="7e2f3-125">في حقل "‏‫‏‫وحدة وقت انتهاء الصلاحية‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="7e2f3-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="7e2f3-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7e2f3-126">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]