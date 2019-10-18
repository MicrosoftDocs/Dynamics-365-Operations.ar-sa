---
title: إعداد نماذج القيم
description: يوضح هذا الإجراء كيفية إنشاء دفتر أصول ثابتة جديد وإقرانه بمجموعة أصول ثابتة.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a528bd12552d5ce100027c9a789f6e1bdc597b66
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186844"
---
# <a name="set-up-value-models"></a><span data-ttu-id="ebd33-103">إعداد نماذج القيم</span><span class="sxs-lookup"><span data-stu-id="ebd33-103">Set up value models</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ebd33-104">يوضح هذا الإجراء كيفية إنشاء دفتر أصول ثابتة جديد وإقرانه بمجموعة أصول ثابتة.</span><span class="sxs-lookup"><span data-stu-id="ebd33-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="ebd33-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="ebd33-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="ebd33-106">إنشاء دفتر</span><span class="sxs-lookup"><span data-stu-id="ebd33-106">Create a book</span></span>
1. <span data-ttu-id="ebd33-107">انتقل إلى الأصول الثابتة > إعداد > الدفاتر.</span><span class="sxs-lookup"><span data-stu-id="ebd33-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="ebd33-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ebd33-108">Click New.</span></span>
3. <span data-ttu-id="ebd33-109">في الحقل "الدفتر"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ebd33-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="ebd33-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ebd33-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ebd33-111">إذا تم تحديد "حساب الإهلاك‬"، فسيتم تضمين دفتر الأصول المقترن في مقترحات الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="ebd33-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="ebd33-112">أما إذا لم يتم تحديده، فلن يتم إهلاك دفتر الأصول بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="ebd33-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="ebd33-113">حدد "نعم" في الحقل "حساب الإهلاك".</span><span class="sxs-lookup"><span data-stu-id="ebd33-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="ebd33-114">في الحقل "ملف تعريف الإهلاك"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ebd33-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="ebd33-115">يُعرف أيضًا ملف تعريف الإهلاك البديل بأسلوب تحويل الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="ebd33-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="ebd33-116">سيتحوّل مقترح الإهلاك إلى ملف التعريف هذا عندما يحسب ملف التعريف البديل مبلغ إهلاك يساوي ملف تعريف الإهلاك الافتراضي أو أكبر منه.</span><span class="sxs-lookup"><span data-stu-id="ebd33-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="ebd33-117">حدد ملف تعريف الإهلاك الاستثنائي‬ لاستخدامه في إهلاك إضافي لأصل ما في ظروف غير عادية.</span><span class="sxs-lookup"><span data-stu-id="ebd33-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="ebd33-118">على سبيل المثال، قد تستخدم هذا الملف لتسجيل الإهلاك الناتج عن كارثة طبيعية.</span><span class="sxs-lookup"><span data-stu-id="ebd33-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="ebd33-119">إذا تم تحديد "إنشاء تسويات الإهلاك التي لها تسويات أساسية‬"، فسيتم إنشاء تسويات الإهلاك تلقائيًا عند تحديث قيمة الأصل.</span><span class="sxs-lookup"><span data-stu-id="ebd33-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="ebd33-120">إذا لم يتم تحديد هذا الخيار، فإن قيمة الأصول المحدثة ستؤثر فقط على حسابات الإهلاك المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="ebd33-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="ebd33-121">حدد "نعم" في الحقل "إنشاء تسويات الإهلاك التي لها تسويات أساسية‬".</span><span class="sxs-lookup"><span data-stu-id="ebd33-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="ebd33-122">بشكل افتراضي، سيتم ترحيل حركات دفتر الأصول الثابتة إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="ebd33-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="ebd33-123">يمكنك تعطيل ترحيل الدفتر إلى دفتر الأستاذ العام عبر تعيين الحقل "الترحيل إلى دفتر الأستاذ العام‬" إلى "لا"</span><span class="sxs-lookup"><span data-stu-id="ebd33-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="ebd33-124">تستخدم عادة الدفاتر التي لا يتم ترحيلها إلى دفتر الأستاذ العام لأغراض إعداد تقارير الضرائب.</span><span class="sxs-lookup"><span data-stu-id="ebd33-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="ebd33-125">يمنحك هذا الأمر مرونة إضافية لحذف الحركات السابقة الخاصة بدفتر الأصول نظرًا لعدم ربطها بدفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="ebd33-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="ebd33-126">يكون الإعداد الافتراضي لطبقة الترحيل "الطبقة الحالية" إذا تم ترحيل الدفتر إلى دفتر الأستاذ العام، و"بلا" في حال عدم ترحيل إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="ebd33-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="ebd33-127">حدّث طبقة الترحيل إذا كنت تريد ترحيل حركات هذا الدفتر هذا إلى طبقة أخرى.</span><span class="sxs-lookup"><span data-stu-id="ebd33-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="ebd33-128">في حقل "التقويم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ebd33-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="ebd33-129">ستقوم الدفاتر المشتقة بترحيل الحركات إلى دفاتر مختلفة في الوقت نفسه.</span><span class="sxs-lookup"><span data-stu-id="ebd33-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="ebd33-130">ستقوم بإنشاء الحركات بواسطة الدفتر الأساسي وأثناء عملية الترحيل، يتم ترحيل نسخة طبق الأصل من الحركة إلى الدفتر المشتق.</span><span class="sxs-lookup"><span data-stu-id="ebd33-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="ebd33-131">لا توجد أية عملية إعادة الحساب مع حركات الكتب المشتقة، وبالتالي يجب عدم استخدامها لحركات الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="ebd33-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="ebd33-132">إقران الدفتر بمجموعة أصول ثابتة</span><span class="sxs-lookup"><span data-stu-id="ebd33-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="ebd33-133">انقر فوق "مجموعات الأصول الثابتة".</span><span class="sxs-lookup"><span data-stu-id="ebd33-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="ebd33-134">في حقل "مجموعة الأصول الثابتة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ebd33-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="ebd33-135">في الحقل "مدة الخدمة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="ebd33-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="ebd33-136">لاحظ أنه يتم حساب "فترات الإهلاك" بعد تعيين مدة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="ebd33-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="ebd33-137">يمكنك تعيين قواعد الإهلاك كما تقتضيه الأغراض الضريبية.</span><span class="sxs-lookup"><span data-stu-id="ebd33-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  

