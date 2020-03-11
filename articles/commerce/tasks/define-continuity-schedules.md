---
title: " تحديد جداول الاستمرارية"
description: يتناول هذا الموضوع إعداد برنامج استمرارية (المعروف بالأوامر المتكررة الحدوث).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a438656730863f345080bc99fef24cfff724f528
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021472"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="ffefd-103"> تحديد جداول الاستمرارية</span><span class="sxs-lookup"><span data-stu-id="ffefd-103">Define continuity schedules</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ffefd-104">يتناول هذا الموضوع إعداد برنامج استمرارية (المعروف بالأوامر المتكررة الحدوث).</span><span class="sxs-lookup"><span data-stu-id="ffefd-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="ffefd-105">يستخدم هذا الموضوع شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="ffefd-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="ffefd-106">إنشاء برنامج استمرارية</span><span class="sxs-lookup"><span data-stu-id="ffefd-106">Create continuity program</span></span>
1. <span data-ttu-id="ffefd-107">انتقل إلى البيع بالتجزئة والتجارة > الاستمرارية > برامج الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="ffefd-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="ffefd-108">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="ffefd-108">Click New.</span></span>
3. <span data-ttu-id="ffefd-109">في الحقل "معرف الجدول‬"، اكتب معرف جدول الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="ffefd-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="ffefd-110">في حقل "بدء الأمر‬"، حدد "الحدث الأول".</span><span class="sxs-lookup"><span data-stu-id="ffefd-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="ffefd-111">إذا قام عميل بوضع أمر جديد لبرنامج الاستمرارية، هناك خياران لشحن المنتج: 1.</span><span class="sxs-lookup"><span data-stu-id="ffefd-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="ffefd-112">الحدث الأول: سيتم شحن المنتج الأول في برنامج الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="ffefd-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="ffefd-113">2</span><span class="sxs-lookup"><span data-stu-id="ffefd-113">2.</span></span> <span data-ttu-id="ffefd-114">الحدث الحالي: سيتم شحن المنتج الحالي.</span><span class="sxs-lookup"><span data-stu-id="ffefd-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="ffefd-115">على سبيل المثال،</span><span class="sxs-lookup"><span data-stu-id="ffefd-115">For example.</span></span> <span data-ttu-id="ffefd-116">بعد ثلاثة أشهر من البرنامج، سيتلقى العميل الحدث الثالث في البرنامج.</span><span class="sxs-lookup"><span data-stu-id="ffefd-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="ffefd-117">حدد "نعم" للمطالبة بتاريخ بدء الأمر.</span><span class="sxs-lookup"><span data-stu-id="ffefd-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="ffefd-118">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="ffefd-118">Click Add line.</span></span>
7. <span data-ttu-id="ffefd-119">في حقل "رقم الصنف"، اكتب رقم الصنف للمنتج الأول ("0013").</span><span class="sxs-lookup"><span data-stu-id="ffefd-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="ffefd-120">اكتب "CP".</span><span class="sxs-lookup"><span data-stu-id="ffefd-120">Type 'CP'.</span></span>
9. <span data-ttu-id="ffefd-121">أدخل التاريخ الذي سيكون فيه المنتج الأول متاحًا للطلب.</span><span class="sxs-lookup"><span data-stu-id="ffefd-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="ffefd-122">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="ffefd-122">Click Add line.</span></span>
11. <span data-ttu-id="ffefd-123">في حقل "رقم الصنف"، اكتب "0014".</span><span class="sxs-lookup"><span data-stu-id="ffefd-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="ffefd-124">في حقل "كود الفاصل الزمني‬"، امسح القيمة لكي يكون الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="ffefd-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="ffefd-125">لتنفيذ هذا الإجراء، قم بإلغاء تحديد فترة التاريخ.</span><span class="sxs-lookup"><span data-stu-id="ffefd-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="ffefd-126">ستقوم بتعيين التاريخ كتاريخ تزايدي من تاريخ البدء للصنف الأول.</span><span class="sxs-lookup"><span data-stu-id="ffefd-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="ffefd-127">هنا سوف تدخل الفاصل الزمني الذي سيتم عنده شحن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ffefd-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="ffefd-128">اكتب "30".</span><span class="sxs-lookup"><span data-stu-id="ffefd-128">Type '30'.</span></span>
    * <span data-ttu-id="ffefd-129">فيما يتعلق ببرنامج شهري، سوف تقوم بإدخال 30 يومًا للفاصل الزمني.</span><span class="sxs-lookup"><span data-stu-id="ffefd-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="ffefd-130">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="ffefd-130">Click Add line.</span></span>
15. <span data-ttu-id="ffefd-131">في حقل "رقم الصنف"، اكتب "0015".</span><span class="sxs-lookup"><span data-stu-id="ffefd-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="ffefd-132">اكتب "إنهاء‬".</span><span class="sxs-lookup"><span data-stu-id="ffefd-132">Type 'End'.</span></span>
17. <span data-ttu-id="ffefd-133">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ffefd-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="ffefd-134">تعيين إلى صنف الاستمرارية</span><span class="sxs-lookup"><span data-stu-id="ffefd-134">Assign to continuity item</span></span>
1. <span data-ttu-id="ffefd-135">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="ffefd-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ffefd-136">حدد الصنف "0016".</span><span class="sxs-lookup"><span data-stu-id="ffefd-136">Select item '0016'.</span></span>
    * <span data-ttu-id="ffefd-137">لتنفيذ هذا الإجراء، ستحدد رقم الصنف 0016.</span><span class="sxs-lookup"><span data-stu-id="ffefd-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="ffefd-138">عادة، كنت ستقوم بإنشاء منتج تم إصداره تم تطبيق عليه منطق إضافي لاستمرارية العمل عند وضعه في أمر مبيعات في مركز اتصال.</span><span class="sxs-lookup"><span data-stu-id="ffefd-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="ffefd-139">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ffefd-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ffefd-140">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="ffefd-140">Click Edit.</span></span>
5. <span data-ttu-id="ffefd-141">قم بتوسيع أو طي القسم البيع.</span><span class="sxs-lookup"><span data-stu-id="ffefd-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="ffefd-142">هنا سوف تقوم بإدخال برنامج الاستمرارية الذي يمثله هذا الصنف.</span><span class="sxs-lookup"><span data-stu-id="ffefd-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="ffefd-143">اكتب "معرف الجدول" الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="ffefd-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="ffefd-144">عندما يتم بيع هذا الصنف في مركز الاتصال، يتم تطبيق منطق عمل إضافي من برنامج الاستمرارية المحدد.</span><span class="sxs-lookup"><span data-stu-id="ffefd-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="ffefd-145">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ffefd-145">Click Save.</span></span>
