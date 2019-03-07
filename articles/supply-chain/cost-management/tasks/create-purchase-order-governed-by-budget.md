---
title: إنشاء أمر شراء تحكمه الموازنة
description: استخدم هذا الإجراء لإنشاء أمر شراء يتم التحقق منه للموازنة المتوفرة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e82e40d67547f5932a4805f2580e8c9f58def284
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "366525"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="7d651-103">إنشاء أمر شراء تحكمه الموازنة</span><span class="sxs-lookup"><span data-stu-id="7d651-103">Create a purchase order governed by budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d651-104">استخدم هذا الإجراء لإنشاء أمر شراء يتم التحقق منه للموازنة المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="7d651-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="7d651-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="7d651-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="7d651-106">مراجعة تكوين رقابة الموازنة</span><span class="sxs-lookup"><span data-stu-id="7d651-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="7d651-107">انتقل إلى إعداد الموازنة > الإعداد > رقابة الموازنة > تكوين رقابة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="7d651-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="7d651-108">انقر فوق علامة التبويب "أموال الموازنة المتاحة‬".</span><span class="sxs-lookup"><span data-stu-id="7d651-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="7d651-109">انقر فوق علامة التبويب "المستندات ودفاتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="7d651-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="7d651-110">انقر فوق علامة التبويب "تحديد قواعد التحكم في الموازنة‬".</span><span class="sxs-lookup"><span data-stu-id="7d651-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="7d651-111">انقر فوق علامة التبويب "تعريف مجموعات الموازنة‬‬".</span><span class="sxs-lookup"><span data-stu-id="7d651-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="7d651-112">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7d651-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="7d651-113">قم بإنشاء عنوان أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="7d651-113">Create the purchase order header</span></span>
1. <span data-ttu-id="7d651-114">انتقل إلى التدبير وتحديد الموارد > أوامر الشراء > كل أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="7d651-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="7d651-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="7d651-115">Click New.</span></span>
3. <span data-ttu-id="7d651-116">في الحقل "حساب المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7d651-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="7d651-117">قم بتوسيع القسم "عام".</span><span class="sxs-lookup"><span data-stu-id="7d651-117">Expand the General section.</span></span>
5. <span data-ttu-id="7d651-118">في حقل "التاريخ المحاسبي‬"، قم بتعيين التاريخ إلى "2016-01-01".</span><span class="sxs-lookup"><span data-stu-id="7d651-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="7d651-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7d651-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="7d651-120">إضافة بند أمر شراء</span><span class="sxs-lookup"><span data-stu-id="7d651-120">Add a purchase order line</span></span>
1. <span data-ttu-id="7d651-121">في الحقل "فئة التدبير"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7d651-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="7d651-122">قم بتعيين الكمية على "2".</span><span class="sxs-lookup"><span data-stu-id="7d651-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="7d651-123">في الحقل "وحدة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7d651-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="7d651-124">قم بتعيين سعر الوحدة إلى "10000".</span><span class="sxs-lookup"><span data-stu-id="7d651-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="7d651-125">انقر فوق "الماليات‬".</span><span class="sxs-lookup"><span data-stu-id="7d651-125">Click Financials.</span></span>
6. <span data-ttu-id="7d651-126">انقر فوق "توزيع المبالغ".</span><span class="sxs-lookup"><span data-stu-id="7d651-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="7d651-127">في حقل "‏‫حساب دفتر الأستاذ‬"، حدد القيمة "601300-001-023--".</span><span class="sxs-lookup"><span data-stu-id="7d651-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="7d651-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7d651-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="7d651-129">تنفيذ التحقق من الموازنة</span><span class="sxs-lookup"><span data-stu-id="7d651-129">Perform budget checking</span></span>
1. <span data-ttu-id="7d651-130">انقر فوق "الماليات‬".</span><span class="sxs-lookup"><span data-stu-id="7d651-130">Click Financials.</span></span>
2. <span data-ttu-id="7d651-131">انقر فوق "تنفيذ التحقق من الموازنة".</span><span class="sxs-lookup"><span data-stu-id="7d651-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="7d651-132">انقر فوق "الماليات‬".</span><span class="sxs-lookup"><span data-stu-id="7d651-132">Click Financials.</span></span>
4. <span data-ttu-id="7d651-133">انقر فوق "أخطاء فحص الموازنة أو التحذيرات".</span><span class="sxs-lookup"><span data-stu-id="7d651-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="7d651-134">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="7d651-134">Click Close.</span></span>

