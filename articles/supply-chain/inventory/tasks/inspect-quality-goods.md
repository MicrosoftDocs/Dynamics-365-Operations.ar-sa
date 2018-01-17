---
title: "فحص جودة البضائع"
description: "يوضح هذا الإجراء كيفية معالجة أمر جودة."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 3a4ace658b8a3a20d613b7a251eb85c32c7f1c09
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="74864-103">فحص جودة البضائع</span><span class="sxs-lookup"><span data-stu-id="74864-103">Inspect the quality of goods</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74864-104">يوضح هذا الإجراء كيفية معالجة أمر جودة.</span><span class="sxs-lookup"><span data-stu-id="74864-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="74864-105">يمكنك تنفيذ هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="74864-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="74864-106">قبل بدء هذا الإجراء المستخدم كمثال، تحتاج إلى تأكيد أمر الشراء "000016" وترحيل إيصال استلام منتجات.</span><span class="sxs-lookup"><span data-stu-id="74864-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="74864-107">سيؤدي ذلك إلى إنشاء أمر جودة بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="74864-107">This will automatically create a quality order.</span></span> <span data-ttu-id="74864-108">عادة ما يتم تنفيذ عمليات فحص الجودة من قِبل موظف التحكم في الجودة‬.</span><span class="sxs-lookup"><span data-stu-id="74864-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="74864-109">تحديد أمر جودة</span><span class="sxs-lookup"><span data-stu-id="74864-109">Select a quality order</span></span>
1. <span data-ttu-id="74864-110">انتقل إلى‬ ‏‫إدارة المخزون > المهام الدورية‬ > إدارة الجودة > أوامر الجودة.</span><span class="sxs-lookup"><span data-stu-id="74864-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="74864-111">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="74864-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="74864-112">حدد أمر الجودة الذي تم إنشاؤه قبل بدء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="74864-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="74864-113">تسجيل نتائج الاختبار</span><span class="sxs-lookup"><span data-stu-id="74864-113">Record test results</span></span>
1. <span data-ttu-id="74864-114">انقر فوق "النتائج".</span><span class="sxs-lookup"><span data-stu-id="74864-114">Click Results.</span></span>
2. <span data-ttu-id="74864-115">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="74864-115">Click Edit.</span></span>
3. <span data-ttu-id="74864-116">في الحقل "كمية النتائج‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="74864-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="74864-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="74864-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="74864-118">في الحقل "الناتج"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="74864-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="74864-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="74864-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="74864-120">في هذا المثال، تستند النتيجة إلى ناتج محدد مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="74864-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="74864-121">يمكنك عادة تسجيل نتيجة اختبار أكثر تحديدًا، على سبيل المثال، حجم أو أبعاد أخرى.</span><span class="sxs-lookup"><span data-stu-id="74864-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="74864-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="74864-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="74864-123">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="74864-123">Click Save.</span></span>
9. <span data-ttu-id="74864-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="74864-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="74864-125">التحقق من صحة أمر الجودة</span><span class="sxs-lookup"><span data-stu-id="74864-125">Validate the quality order</span></span>
1. <span data-ttu-id="74864-126">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="74864-126">Click Validate.</span></span>
2. <span data-ttu-id="74864-127">في الحقل "تم التحقق بواسطة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="74864-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="74864-128">حدد المستخدم الذي يجري عملية الفحص.</span><span class="sxs-lookup"><span data-stu-id="74864-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="74864-129">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="74864-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="74864-130">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="74864-130">Click Select.</span></span>
5. <span data-ttu-id="74864-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="74864-131">Click OK.</span></span>
6. <span data-ttu-id="74864-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="74864-132">Close the page.</span></span>

