---
title: تسوية الشحن يدويًا
description: يوضح هذا الإجراء كيفية تسوية الشحن يدويًا.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb9c850aa045b72137b8a1d3c8cdae51cf2fd7b6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843231"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="39527-103">تسوية الشحن يدويًا</span><span class="sxs-lookup"><span data-stu-id="39527-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39527-104">يوضح هذا الإجراء كيفية تسوية الشحن يدويًا.</span><span class="sxs-lookup"><span data-stu-id="39527-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="39527-105">عادة ما يتم ذلك عن طريق منسق نقل.</span><span class="sxs-lookup"><span data-stu-id="39527-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="39527-106">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="39527-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="39527-107">تحديد حمل عمل للتسوية</span><span class="sxs-lookup"><span data-stu-id="39527-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="39527-108">انتقل إلى إدارة النقل > التخطيط > منضدة عمل تخطيط الحِمل‬.</span><span class="sxs-lookup"><span data-stu-id="39527-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="39527-109">قم بإلغاء تحديد خانة الاختيار "إخفاء ما تم شحنه‬ وما تم استلامه‬".</span><span class="sxs-lookup"><span data-stu-id="39527-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="39527-110">في القائمة، حدد الحمولة ذات معرف الحمل 00006.</span><span class="sxs-lookup"><span data-stu-id="39527-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="39527-111">إنشاء فاتورة شركة نقل</span><span class="sxs-lookup"><span data-stu-id="39527-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="39527-112">إذا قمت بتسوية الشحن يدويًا ولم تستلم فواتير الشركة تلقائيًا، فيمكنك إنشاء فاتورة استنادًا إلى فاتورة الشحن.</span><span class="sxs-lookup"><span data-stu-id="39527-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="39527-113">انقر فوق "معلومات ذات صلة".</span><span class="sxs-lookup"><span data-stu-id="39527-113">Click Related information.</span></span>
2. <span data-ttu-id="39527-114">انقر فوق "تفاصيل فاتورة الشحن".</span><span class="sxs-lookup"><span data-stu-id="39527-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="39527-115">انقر فوق "إنشاء كمبيالة/فاتورة الشحن".</span><span class="sxs-lookup"><span data-stu-id="39527-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="39527-116">في الحقل "الفاتورة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="39527-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="39527-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="39527-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="39527-118">تسوية الفاتورة</span><span class="sxs-lookup"><span data-stu-id="39527-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="39527-119">عند تسوية فاتورة الشركة وفاتورة الشحن، يتم ذلك كل بند بعد الآخر.</span><span class="sxs-lookup"><span data-stu-id="39527-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="39527-120">انقر فوق "مطابقة فواتير الشحن والفواتير".</span><span class="sxs-lookup"><span data-stu-id="39527-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="39527-121">قم بتوسيع المقطع "تفاصيل الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="39527-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="39527-122">قم بتوسيع المقطع "تفاصيل فاتورة الشحن غير المطابقة‬".</span><span class="sxs-lookup"><span data-stu-id="39527-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="39527-123">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="39527-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="39527-124">انقر فوق "مطابقة".</span><span class="sxs-lookup"><span data-stu-id="39527-124">Click Match.</span></span>
6. <span data-ttu-id="39527-125">قم بتوسيع المقطع "تفاصيل فاتورة الشحن المطابقة‬".</span><span class="sxs-lookup"><span data-stu-id="39527-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="39527-126">تقديم الفاتورة للاعتماد</span><span class="sxs-lookup"><span data-stu-id="39527-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="39527-127">انقر فوق "إرسال" للموافقة.</span><span class="sxs-lookup"><span data-stu-id="39527-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="39527-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="39527-128">Close the page.</span></span>
3. <span data-ttu-id="39527-129">امسح تحديد خانة الاختيار "إخفاء الموافقة‬".</span><span class="sxs-lookup"><span data-stu-id="39527-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="39527-130">انقر فوق "دفاتر يومية فاتورة المورّد".</span><span class="sxs-lookup"><span data-stu-id="39527-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="39527-131">انقر لمتابعة الارتباط الوارد في الحقل "رقم دفتر يومية المرجع‬".</span><span class="sxs-lookup"><span data-stu-id="39527-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="39527-132">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="39527-132">Click Lines.</span></span>

