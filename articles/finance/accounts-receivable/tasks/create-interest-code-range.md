---
title: إنشاء رمز فائدة مع نطاق
description: يمكن إعداد رموز الفائدة لحساب مبالغ الفائدة المختلفة استنادًا إلى نطاق القيم.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44b98436d6e0c40f0458dc4744b8b1d96baa8b54
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216559"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="0ae8c-103">إنشاء رمز فائدة مع نطاق</span><span class="sxs-lookup"><span data-stu-id="0ae8c-103">Create an interest code with a range</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="0ae8c-104">يمكن إعداد رموز الفائدة لحساب مبالغ الفائدة المختلفة استنادًا إلى نطاق القيم.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="0ae8c-105">يوضح لك هذا الإجراء كيفية إضافة رمز فائدة وإضافة نطاق إليه.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="0ae8c-106">الانتقال إلى الائتمان والتحصيلات > الفائدة > إعداد رموز الفائدة.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="0ae8c-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0ae8c-107">Click New.</span></span>
3. <span data-ttu-id="0ae8c-108">في حقل "رمز الفائدة"، أدخل اسم رمز الفائدة.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="0ae8c-109">في حقل "الوصف"، أدخل وصفًا لرمز الفائدة.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="0ae8c-110">حدد الشهر.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-110">Select Month.</span></span>
6. <span data-ttu-id="0ae8c-111">قم بتوسيع مقطع "الأرباح‬".</span><span class="sxs-lookup"><span data-stu-id="0ae8c-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="0ae8c-112">قم بتوسيع مقطع "الأرباح حسب العملة‬".</span><span class="sxs-lookup"><span data-stu-id="0ae8c-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="0ae8c-113">في حقل "‏‫حساب ترحيل دفتر الأستاذ‬"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="0ae8c-114">في حقل "الفائدة حسب النطاق"، حدد "الأشهر".</span><span class="sxs-lookup"><span data-stu-id="0ae8c-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="0ae8c-115">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-115">Click Add.</span></span>
11. <span data-ttu-id="0ae8c-116">في حقل "الوصف"، أدخل وصفًا لهذه العملة والنطاق.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="0ae8c-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="0ae8c-117">Click Save.</span></span>
13. <span data-ttu-id="0ae8c-118">انقر فوق "النطاقات".</span><span class="sxs-lookup"><span data-stu-id="0ae8c-118">Click Ranges.</span></span>
14. <span data-ttu-id="0ae8c-119">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0ae8c-119">Click New.</span></span>
15. <span data-ttu-id="0ae8c-120">أدخل "من القيمة" بقيمة 0، ثم أدخل النسبة المئوية للفائدة في الشهر والتي سيتم استخدامها لحساب الفائدة.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="0ae8c-121">على سبيل المثال، ستكون 1.5.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="0ae8c-122">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-122">Click New.</span></span>
17. <span data-ttu-id="0ae8c-123">أدخل "التالي من القيمة" بقيمة 4، وهو الشهر الأول الذي ستقوم بحساب مبلغ فائدة جديد له.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="0ae8c-124">أدخل النسبة المئوية للفائدة في الشهر والتي سيتم استخدامها لحساب الفائدة بدءًا من الشهر 4.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="0ae8c-125">بالنسبة لهذا المثال، ستكون 2.0.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="0ae8c-126">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-126">Click New.</span></span>
20. <span data-ttu-id="0ae8c-127">أدخل "التالي من القيمة" بقيمة 7، وهو الشهر التالي الذي ستقوم بحساب مبلغ فائدة جديد له.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="0ae8c-128">أدخل النسبة المئوية للفائدة في الشهر والتي سيتم استخدامها لحساب الفائدة بدءًا من الشهر 7.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="0ae8c-129">بالنسبة لهذا المثال، ستكون 2.5.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="0ae8c-130">انقر فوق "إغلاق" لإكمال الإعداد.</span><span class="sxs-lookup"><span data-stu-id="0ae8c-130">Click Close to complete the setup.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]