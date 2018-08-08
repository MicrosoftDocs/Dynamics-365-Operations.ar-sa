--- 
title: "تسوية الشحن يدويًا"
description: "يوضح هذا الإجراء كيفية تسوية الشحن يدويًا."
author: ShylaThompson
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: eb6f53de5013e8d5ee50c606bac15599bc960da4
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="0d599-103">تسوية الشحن يدويًا</span><span class="sxs-lookup"><span data-stu-id="0d599-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d599-104">يوضح هذا الإجراء كيفية تسوية الشحن يدويًا.</span><span class="sxs-lookup"><span data-stu-id="0d599-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="0d599-105">عادة ما يتم ذلك عن طريق منسق نقل.</span><span class="sxs-lookup"><span data-stu-id="0d599-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="0d599-106">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="0d599-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="0d599-107">تحديد حمل عمل للتسوية</span><span class="sxs-lookup"><span data-stu-id="0d599-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="0d599-108">انتقل إلى إدارة النقل > التخطيط > منضدة عمل تخطيط الحِمل‬.</span><span class="sxs-lookup"><span data-stu-id="0d599-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="0d599-109">قم بإلغاء تحديد خانة الاختيار "إخفاء ما تم شحنه‬ وما تم استلامه‬".</span><span class="sxs-lookup"><span data-stu-id="0d599-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="0d599-110">في القائمة، حدد الحمولة ذات معرف الحمل 00006.</span><span class="sxs-lookup"><span data-stu-id="0d599-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="0d599-111">إنشاء فاتورة شركة نقل</span><span class="sxs-lookup"><span data-stu-id="0d599-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="0d599-112">إذا قمت بتسوية الشحن يدويًا ولم تستلم فواتير الشركة تلقائيًا، فيمكنك إنشاء فاتورة استنادًا إلى فاتورة الشحن.</span><span class="sxs-lookup"><span data-stu-id="0d599-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="0d599-113">انقر فوق "معلومات ذات صلة".</span><span class="sxs-lookup"><span data-stu-id="0d599-113">Click Related information.</span></span>
2. <span data-ttu-id="0d599-114">انقر فوق "تفاصيل فاتورة الشحن".</span><span class="sxs-lookup"><span data-stu-id="0d599-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="0d599-115">انقر فوق "إنشاء كمبيالة/فاتورة الشحن".</span><span class="sxs-lookup"><span data-stu-id="0d599-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="0d599-116">في الحقل "الفاتورة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0d599-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="0d599-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0d599-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="0d599-118">تسوية الفاتورة</span><span class="sxs-lookup"><span data-stu-id="0d599-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="0d599-119">عند تسوية فاتورة الشركة وفاتورة الشحن، يتم ذلك كل بند بعد الآخر.</span><span class="sxs-lookup"><span data-stu-id="0d599-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="0d599-120">انقر فوق "مطابقة فواتير الشحن والفواتير".</span><span class="sxs-lookup"><span data-stu-id="0d599-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="0d599-121">قم بتوسيع المقطع "تفاصيل الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="0d599-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="0d599-122">قم بتوسيع المقطع "تفاصيل فاتورة الشحن غير المطابقة‬".</span><span class="sxs-lookup"><span data-stu-id="0d599-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="0d599-123">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0d599-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="0d599-124">انقر فوق "مطابقة".</span><span class="sxs-lookup"><span data-stu-id="0d599-124">Click Match.</span></span>
6. <span data-ttu-id="0d599-125">قم بتوسيع المقطع "تفاصيل فاتورة الشحن المطابقة‬".</span><span class="sxs-lookup"><span data-stu-id="0d599-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="0d599-126">تقديم الفاتورة للاعتماد</span><span class="sxs-lookup"><span data-stu-id="0d599-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="0d599-127">انقر فوق "إرسال" للموافقة.</span><span class="sxs-lookup"><span data-stu-id="0d599-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="0d599-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0d599-128">Close the page.</span></span>
3. <span data-ttu-id="0d599-129">امسح تحديد خانة الاختيار "إخفاء الموافقة‬".</span><span class="sxs-lookup"><span data-stu-id="0d599-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="0d599-130">انقر فوق "دفاتر يومية فاتورة المورّد".</span><span class="sxs-lookup"><span data-stu-id="0d599-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="0d599-131">انقر لمتابعة الارتباط الوارد في الحقل "رقم دفتر يومية المرجع‬".</span><span class="sxs-lookup"><span data-stu-id="0d599-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="0d599-132">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="0d599-132">Click Lines.</span></span>


