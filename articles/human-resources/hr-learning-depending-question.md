---
title: طرح سؤال يعتمد على إجابة السؤال السابق
description: تسمح لك الأسئلة المشروطة بتحديد سؤال المتابعة الذي سيتم تقديمه للمستجيب، استنادًا إلى الإجابة على السؤال السابق.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6e49814212b69a618fc3d855b7e290e6b6ff303
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008035"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="55418-103">طرح سؤال يعتمد على إجابة السؤال السابق</span><span class="sxs-lookup"><span data-stu-id="55418-103">Make a question dependent on the answer of the previous question</span></span>



<span data-ttu-id="55418-104">تسمح لك الأسئلة المشروطة بتحديد سؤال المتابعة الذي سيتم تقديمه للمستجيب، استنادًا إلى الإجابة على السؤال السابق.</span><span class="sxs-lookup"><span data-stu-id="55418-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="55418-105">على سبيل المثال، إذا طرحت السؤال "هل تفضل الشاي أو القهوة"، فيمكن تحديد سؤال متابعة منطقي وفقًا لاختيار المستجيب الشاي أو القهوة كجواب على السؤال.</span><span class="sxs-lookup"><span data-stu-id="55418-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="55418-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="55418-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="55418-107">البحث عن الاستبيان الموجود</span><span class="sxs-lookup"><span data-stu-id="55418-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="55418-108">انتقل إلى الاستبيان > تصميم > استبيانات‬.</span><span class="sxs-lookup"><span data-stu-id="55418-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="55418-109">في القائمة، حدد الاستبيان WorkFH.</span><span class="sxs-lookup"><span data-stu-id="55418-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="55418-110">إضافة كافة الأسئلة والأسئلة الفرعية إلى الاستبيان</span><span class="sxs-lookup"><span data-stu-id="55418-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="55418-111">انقر فوق "الأسئلة".</span><span class="sxs-lookup"><span data-stu-id="55418-111">Click Questions.</span></span>
2. <span data-ttu-id="55418-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="55418-112">Click New.</span></span>
3. <span data-ttu-id="55418-113">في الحقل "السؤال‬"، حدد رقم السؤال 00016.</span><span class="sxs-lookup"><span data-stu-id="55418-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="55418-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="55418-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="55418-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="55418-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="55418-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="55418-116">Click Save.</span></span>
7. <span data-ttu-id="55418-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="55418-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="55418-118">تعيين "تسلسل الاستبيان" إلى "مشروط" وطرح سؤال يعتمد على السؤال المناسب</span><span class="sxs-lookup"><span data-stu-id="55418-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="55418-119">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="55418-119">Click Edit.</span></span>
2. <span data-ttu-id="55418-120">قم بتوسيع قسم "الإعداد".</span><span class="sxs-lookup"><span data-stu-id="55418-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="55418-121">في الحقل "ترتيب الأسئلة‬"، حدد "مشروط‬".</span><span class="sxs-lookup"><span data-stu-id="55418-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="55418-122">انقر فوق "سؤال مشروط".</span><span class="sxs-lookup"><span data-stu-id="55418-122">Click Conditional question.</span></span>
5. <span data-ttu-id="55418-123">في الشجرة، حدد "الأسئلة/اشرح سبب إجابتك على السؤال السابق كما فعلت؟".</span><span class="sxs-lookup"><span data-stu-id="55418-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="55418-124">في الحقل "سؤال أساسي‬"، حدد السؤال 00009.</span><span class="sxs-lookup"><span data-stu-id="55418-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="55418-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="55418-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="55418-126">في حقل "الإجابة"، أدخل معرف تسلسل الإجابات لخيار الإجابة الذي تريد جعل السؤال يعتمد عليه.</span><span class="sxs-lookup"><span data-stu-id="55418-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="55418-127">على سبيل المثال، أدخل 1 لخيار الإجابة الأولى.</span><span class="sxs-lookup"><span data-stu-id="55418-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="55418-128">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="55418-128">Click Save.</span></span>
10. <span data-ttu-id="55418-129">في الشجرة، حدد "الأسئلة‬\أتلقى مبلغًا عادلاً نوعًا ما مقابل العمل الذي أقوم به".</span><span class="sxs-lookup"><span data-stu-id="55418-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="55418-130">لاحظ أنه تم تحديث شجرة الأسئلة لإظهار التبعية.</span><span class="sxs-lookup"><span data-stu-id="55418-130">Note that the question tree updated to show the dependency.</span></span>  
