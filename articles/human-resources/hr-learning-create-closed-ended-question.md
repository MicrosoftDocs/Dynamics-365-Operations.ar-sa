---
title: إنشاء سؤال ذي نهاية مغلقة
description: تسمح لك الأسئلة ذات الإجابات المغلقة بتوفير خيارات للمستجيب يمكنه الاختيار منها.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41e12e6f35237ea125756b502d5cebed58c6bf55
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790634"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="da736-103">إنشاء سؤال ذي نهاية مغلقة</span><span class="sxs-lookup"><span data-stu-id="da736-103">Create a closed ended question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="da736-104">تسمح لك الأسئلة ذات الإجابات المغلقة بتوفير خيارات للمستجيب يمكنه الاختيار منها.</span><span class="sxs-lookup"><span data-stu-id="da736-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="da736-105">أولاً، تحتاج إلى إنشاء مجموعة الإجابات بواسطة الإجابات، ثم إنشاء السؤال الذي سيستخدم مجموعة الإجابات.</span><span class="sxs-lookup"><span data-stu-id="da736-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="da736-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="da736-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="da736-107">إنشاء مجموعة إجابات</span><span class="sxs-lookup"><span data-stu-id="da736-107">Create an answer group</span></span>
1. <span data-ttu-id="da736-108">انتقل إلى الاستبيان > تصميم > مجموعات الإجابات.</span><span class="sxs-lookup"><span data-stu-id="da736-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="da736-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="da736-109">Click New.</span></span>
3. <span data-ttu-id="da736-110">في الحقل "مجموعة الإجابات"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da736-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="da736-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da736-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="da736-112">استخدام وظيفة "الترتيب عشوائيًا‬" لوضع الإجابات بترتيب مختلف وبطريقة عشوائية في كل مرة يتم فيها استخدام مجموعة الإجابات لسؤال ما.</span><span class="sxs-lookup"><span data-stu-id="da736-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="da736-113">انقر فوق "إجابة".</span><span class="sxs-lookup"><span data-stu-id="da736-113">Click Answer.</span></span>
6. <span data-ttu-id="da736-114">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="da736-114">Click New.</span></span>
    * <span data-ttu-id="da736-115">يتحكم الرقم التسلسلي بالترتيب الذي يتم فيه عرض الإجابات، ما لم يتم تحديد الخيار "ترتيب عشوائيًا" لمجموعة الإجابات.</span><span class="sxs-lookup"><span data-stu-id="da736-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="da736-116">يمكن منح نقاط للإجابات لاستخدامها في تسجيل نقاط الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="da736-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="da736-117">في الحقل "النقاط‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="da736-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="da736-118">يمكن وضع علامة على الإجابة الصحيحة للإشارة إلى أن الإجابة المحددة هي الإجابة الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="da736-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="da736-119">ويمكن استخدام هذا لتسجيل نقاط الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="da736-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="da736-120">في الحقل "الإجابة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da736-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="da736-121">تابع إنشاء خيارات تحديد الإجابات لمجموعة الإجابات.</span><span class="sxs-lookup"><span data-stu-id="da736-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="da736-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="da736-122">Click New.</span></span>
10. <span data-ttu-id="da736-123">في الحقل "النقاط‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="da736-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="da736-124">في الحقل "الإجابة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da736-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="da736-125">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="da736-125">Click New.</span></span>
13. <span data-ttu-id="da736-126">في الحقل "النقاط‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="da736-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="da736-127">في الحقل "الإجابة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da736-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="da736-128">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="da736-128">Click New.</span></span>
16. <span data-ttu-id="da736-129">في الحقل "النقاط‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="da736-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="da736-130">في الحقل "الإجابة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da736-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="da736-131">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="da736-131">Click New.</span></span>
19. <span data-ttu-id="da736-132">في الحقل "النقاط‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="da736-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="da736-133">في الحقل "الإجابة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da736-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="da736-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da736-134">Close the page.</span></span>
22. <span data-ttu-id="da736-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da736-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="da736-136">إنشاء السؤال</span><span class="sxs-lookup"><span data-stu-id="da736-136">Create the question</span></span>
1. <span data-ttu-id="da736-137">انتقل إلى الاستبيان > تصميم > الأسئلة.</span><span class="sxs-lookup"><span data-stu-id="da736-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="da736-138">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="da736-138">Click New.</span></span>
3. <span data-ttu-id="da736-139">استخدم حقل "النوع" لتجميع الأسئلة ذات الصلة معًا.</span><span class="sxs-lookup"><span data-stu-id="da736-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="da736-140">يمكنك استخدام أنواع الإدخال "خانة اختيار" أو "زر بديل" أو "مربع تحرير وسرد‬" للأسئلة ذات الإجابات المغلقة.</span><span class="sxs-lookup"><span data-stu-id="da736-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="da736-141">في الحقل "نوع الإدخال"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="da736-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="da736-142">في الحقل "مجموعة الإجابات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="da736-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="da736-143">في الحقل "نص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da736-143">In the Text field, type a value.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]