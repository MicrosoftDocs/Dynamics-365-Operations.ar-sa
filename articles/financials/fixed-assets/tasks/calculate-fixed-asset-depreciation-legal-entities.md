--- 
title: "حساب إهلاك الأصول الثابتة عبر الكيانات القانونية"
description: "يوضح هذا الإجراء كيفية إعداد عملية الإهلاك للعديد من الكيانات القانونية‬ وكيفية تشغيلها."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 4221acf200f41ca39803bcd56c1b05e0d87bd948
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="3a0a1-103">حساب إهلاك الأصول الثابتة عبر الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="3a0a1-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a0a1-104">يمكن تشغيل إهلاك الأصول الثابتة عبر الكيانات القانونية في خطوة واحدة.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="3a0a1-105">يوضح هذا الإجراء كيفية إعداد العملية للعديد من الكيانات القانونية‬ وكيفية تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="3a0a1-106">يستخدم دور المحاسب.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-106">It uses the accountant role.</span></span>  

<span data-ttu-id="3a0a1-107">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="3a0a1-108">مهمة فرعية، الخطوات (16): إعداد دفاتر يومية تشغيل الإهلاك عبر الشركة.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="3a0a1-109">أولاً، يجب إعداد دفاتر اليومية المقرر استخدامها في تشغيل الإهلاك عبر الشركة في كل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="3a0a1-110">انتقل إلى الأصول الثابتة > إعداد > معلمات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="3a0a1-111">قم بتوسيع قسم عروض الأصول الثابتة‬.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="3a0a1-112">أنشئ سجلاً باسم دفتر اليومية المقرر استخدامه لكل طبقة ترحيل في الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="3a0a1-113">إذا لم تكن الدفاتر تقوم بالترحيل إلى دفتر الأستاذ العام، فيجب عندئذ تحديد طبقة الترحيل "بلا" مع دفتر اليومية المقترن.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="3a0a1-114">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-114">Click Add.</span></span> 
4. <span data-ttu-id="3a0a1-115">في الحقل "طبقة الترحيل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="3a0a1-116">في الحقل "اسم دفتر اليومية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="3a0a1-117">قم بتكرار إعداد دفتر اليومية في صفحة معلمات الأصول الثابتة في كل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="3a0a1-118">مهمة فرعية: حساب الإهلاك</span><span class="sxs-lookup"><span data-stu-id="3a0a1-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="3a0a1-119">استخدم صفحة إنشاء عرض إهلاك لبدء تشغيل إهلاك عبر الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="3a0a1-120">انتقل إلى الأصول الثابتة > إدخالات دفتر اليومية‬ > إنشاء مقترح الإهلاك‬‬.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="3a0a1-121">في الحقل "طبقة الترحيل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="3a0a1-122">سيتم تعيين اسم دفتر اليومية افتراضيًا من معلمات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="3a0a1-123">ويمكن تغييره من هنا للكيان القانوني الحالي.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="3a0a1-124">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="3a0a1-125">حدد الكيانات القانونية المقرر تضمينها في تشغيل الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="3a0a1-126">لن يظهر في القائمة غير الكيانات القانونية ذات دفاتر اليومية التي تم إعدادها لعروض الأصول الثابتة في صفحة معلمات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="3a0a1-127">في حالة التمكين، سيقوم خيار ترحيل دفاتر اليومية بترحيل دفاتر يومية الإهلاك تلقائيًا عند إنشائها.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="3a0a1-128">في حالة عدم التحديد، سيتم إنشاء دفاتر اليومية، ولكن لن يتم ترحيلها، بحيث تتمكن من مراجعة التفاصيل قبل الترحيل.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="3a0a1-129">حدد نعم في الحقل ترحيل دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="3a0a1-130">تتضمن حقول التصفية جميع الأصول الثابتة والمجموعات والدفاتر الخاصة بالكيانات القانونية المحددة لتشغيل الإهلاك هذا.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="3a0a1-131">يتم تمكين خيار معالجة الدُفعة بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="3a0a1-132">عند تمكين هذا الخيار، سيتم تشغيل إنشاء دفتر يومية الإهلاك وترحيله في الخلفية.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="3a0a1-133">انقر فوق "إنشاء دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="3a0a1-133">Click Create journal.</span></span> 
10. <span data-ttu-id="3a0a1-134">يمكنك عرض دفاتر يومية الإهلاك التي تم إنشاؤها في الكيانات القانونية الخاصة.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="3a0a1-135">انتقل إلى الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬.</span><span class="sxs-lookup"><span data-stu-id="3a0a1-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

