--- 
title: "إنشاء كود شريطي لمنتج"
description: "يظهر هذا الإجراء كيفية إنشاء كود شريطي يدويًا باستخدام رقم الصنف M0001 كمثال."
author: YuyuScheller
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6a55e25205bc7e996b6ab8c6915e2e86b758ee7a
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="79a3b-103">إنشاء كود شريطي لمنتج</span><span class="sxs-lookup"><span data-stu-id="79a3b-103">Create a bar code for a product</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79a3b-104">يظهر هذا الإجراء كيفية إنشاء كود شريطي يدويًا باستخدام رقم الصنف M0001 كمثال.</span><span class="sxs-lookup"><span data-stu-id="79a3b-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="79a3b-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="79a3b-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="79a3b-106">انقر فوق "صيانة المنتج الذي تم إصداره".</span><span class="sxs-lookup"><span data-stu-id="79a3b-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="79a3b-107">انقر فوق "المنتجات التي تم إصدارها".</span><span class="sxs-lookup"><span data-stu-id="79a3b-107">Click Released products.</span></span>
3. <span data-ttu-id="79a3b-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79a3b-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="79a3b-109">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="79a3b-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="79a3b-110">انقر فوق "الأكواد الشريطية‬".</span><span class="sxs-lookup"><span data-stu-id="79a3b-110">Click Bar codes.</span></span>
6. <span data-ttu-id="79a3b-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="79a3b-111">Click New.</span></span>
7. <span data-ttu-id="79a3b-112">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79a3b-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="79a3b-113">في الحقل "إعداد الكود الشريطي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="79a3b-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="79a3b-114">في حقل "الكود الشريطي‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="79a3b-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="79a3b-115">في حقل "الكود الشريطي‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="79a3b-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="79a3b-116">اضغط على المفتاح Tab.</span><span class="sxs-lookup"><span data-stu-id="79a3b-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="79a3b-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="79a3b-117">Close the page.</span></span>
12. <span data-ttu-id="79a3b-118">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="79a3b-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="79a3b-119">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="79a3b-119">Click Save.</span></span>
    * <span data-ttu-id="79a3b-120">عندما تنقر فوق "حفظ"، يتم تشغيل فحص الكود الشريطي، وفي هذه الحالة سيعرض خطأ يفيد بأن رقم الفحص المتوقع هو 8، إلا أنه تم العثور على 3.</span><span class="sxs-lookup"><span data-stu-id="79a3b-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="79a3b-121">حدّث رقم الكود الشريطي يدويًا بحيث يكون الرقم 8 في النهاية.</span><span class="sxs-lookup"><span data-stu-id="79a3b-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="79a3b-122">في حقل "الكود الشريطي‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="79a3b-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="79a3b-123">في حقل "الكود الشريطي‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="79a3b-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="79a3b-124">اضغط على المفتاح Tab.</span><span class="sxs-lookup"><span data-stu-id="79a3b-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="79a3b-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="79a3b-125">Close the page.</span></span>
17. <span data-ttu-id="79a3b-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="79a3b-126">Click Save.</span></span>
18. <span data-ttu-id="79a3b-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="79a3b-127">Close the page.</span></span>


