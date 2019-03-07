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
ms.openlocfilehash: dd70780927bb9aaa19c196705d6e8fa1c247ea66
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "330507"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="ffb1b-103"> تحديد جداول الاستمرارية</span><span class="sxs-lookup"><span data-stu-id="ffb1b-103">Define continuity schedules</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ffb1b-104">يتناول هذا الموضوع إعداد برنامج استمرارية (المعروف بالأوامر المتكررة الحدوث).</span><span class="sxs-lookup"><span data-stu-id="ffb1b-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="ffb1b-105">يستخدم هذا الموضوع شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="ffb1b-106">إنشاء برنامج استمرارية</span><span class="sxs-lookup"><span data-stu-id="ffb1b-106">Create continuity program</span></span>
1. <span data-ttu-id="ffb1b-107">انتقل إلى البيع بالتجزئة والتجارة > الاستمرارية > برامج الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-107">Go to Retail and commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="ffb1b-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-108">Click New.</span></span>
3. <span data-ttu-id="ffb1b-109">في الحقل "معرف الجدول‬"، اكتب معرف جدول الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="ffb1b-110">في حقل "بدء الأمر‬"، حدد "الحدث الأول".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="ffb1b-111">إذا قام عميل بوضع أمر جديد لبرنامج الاستمرارية، هناك خياران لشحن المنتج: 1.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="ffb1b-112">الحدث الأول: سيتم شحن المنتج الأول في برنامج الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="ffb1b-113">2</span><span class="sxs-lookup"><span data-stu-id="ffb1b-113">2.</span></span> <span data-ttu-id="ffb1b-114">الحدث الحالي: سيتم شحن المنتج الحالي.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="ffb1b-115">على سبيل المثال،</span><span class="sxs-lookup"><span data-stu-id="ffb1b-115">For example.</span></span> <span data-ttu-id="ffb1b-116">بعد ثلاثة أشهر من البرنامج، سيتلقى العميل الحدث الثالث في البرنامج.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="ffb1b-117">حدد "نعم" للمطالبة بتاريخ بدء الأمر.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="ffb1b-118">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-118">Click Add line.</span></span>
7. <span data-ttu-id="ffb1b-119">في حقل "رقم الصنف"، اكتب رقم الصنف للمنتج الأول ("0013").</span><span class="sxs-lookup"><span data-stu-id="ffb1b-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="ffb1b-120">اكتب "CP".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-120">Type 'CP'.</span></span>
9. <span data-ttu-id="ffb1b-121">أدخل التاريخ الذي سيكون فيه المنتج الأول متاحًا للطلب.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="ffb1b-122">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-122">Click Add line.</span></span>
11. <span data-ttu-id="ffb1b-123">في حقل "رقم الصنف"، اكتب "0014".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="ffb1b-124">في حقل "كود الفاصل الزمني‬"، امسح القيمة لكي يكون الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="ffb1b-125">لتنفيذ هذا الإجراء، قم بإلغاء تحديد فترة التاريخ.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="ffb1b-126">ستقوم بتعيين التاريخ كتاريخ تزايدي من تاريخ البدء للصنف الأول.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="ffb1b-127">هنا سوف تدخل الفاصل الزمني الذي سيتم عنده شحن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="ffb1b-128">اكتب "30".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-128">Type '30'.</span></span>
    * <span data-ttu-id="ffb1b-129">فيما يتعلق ببرنامج شهري، سوف تقوم بإدخال 30 يومًا للفاصل الزمني.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="ffb1b-130">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-130">Click Add line.</span></span>
15. <span data-ttu-id="ffb1b-131">في حقل "رقم الصنف"، اكتب "0015".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="ffb1b-132">اكتب "إنهاء‬".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-132">Type 'End'.</span></span>
17. <span data-ttu-id="ffb1b-133">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="ffb1b-134">تعيين إلى صنف الاستمرارية</span><span class="sxs-lookup"><span data-stu-id="ffb1b-134">Assign to continuity item</span></span>
1. <span data-ttu-id="ffb1b-135">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ffb1b-136">حدد الصنف "0016".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-136">Select item '0016'.</span></span>
    * <span data-ttu-id="ffb1b-137">لتنفيذ هذا الإجراء، ستحدد رقم الصنف 0016.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="ffb1b-138">عادة، كنت ستقوم بإنشاء منتج تم إصداره تم تطبيق عليه منطق إضافي لاستمرارية العمل عند وضعه في أمر مبيعات في مركز اتصال.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="ffb1b-139">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ffb1b-140">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-140">Click Edit.</span></span>
5. <span data-ttu-id="ffb1b-141">قم بتوسيع أو طي القسم البيع.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="ffb1b-142">هنا سوف تقوم بإدخال برنامج الاستمرارية الذي يمثله هذا الصنف.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="ffb1b-143">اكتب "معرف الجدول" الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="ffb1b-144">عندما يتم بيع هذا الصنف في مركز الاتصال، يتم تطبيق منطق عمل إضافي من برنامج الاستمرارية المحدد.</span><span class="sxs-lookup"><span data-stu-id="ffb1b-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="ffb1b-145">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ffb1b-145">Click Save.</span></span>

