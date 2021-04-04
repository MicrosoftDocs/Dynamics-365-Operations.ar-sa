---
title: تسوية الشحن يدويًا
description: يوضح هذا الإجراء كيفية تسوية الشحن يدويًا.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: becda50b5d176ceb350c471b154aed1842c31a3b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247180"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="7d973-103">تسوية الشحن يدويًا</span><span class="sxs-lookup"><span data-stu-id="7d973-103">Reconcile freight manually</span></span>

<span data-ttu-id="7d973-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="7d973-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="7d973-105">يوضح هذا الإجراء كيفية تسوية الشحن يدويًا.</span><span class="sxs-lookup"><span data-stu-id="7d973-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="7d973-106">عادة ما يتم ذلك عن طريق منسق نقل.</span><span class="sxs-lookup"><span data-stu-id="7d973-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="7d973-107">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="7d973-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="7d973-108">تحديد حمل عمل للتسوية</span><span class="sxs-lookup"><span data-stu-id="7d973-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="7d973-109">انتقل إلى إدارة النقل > التخطيط > منضدة عمل تخطيط الحِمل‬.</span><span class="sxs-lookup"><span data-stu-id="7d973-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="7d973-110">قم بإلغاء تحديد خانة الاختيار "إخفاء ما تم شحنه‬ وما تم استلامه‬".</span><span class="sxs-lookup"><span data-stu-id="7d973-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="7d973-111">في القائمة، حدد الحمولة ذات معرف الحمل 00006.</span><span class="sxs-lookup"><span data-stu-id="7d973-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="7d973-112">إنشاء فاتورة شركة نقل</span><span class="sxs-lookup"><span data-stu-id="7d973-112">Create a carrier invoice</span></span>
<span data-ttu-id="7d973-113">إذا قمت بتسوية الشحن يدويًا ولم تستلم فواتير الشركة تلقائيًا، فيمكنك إنشاء فاتورة استنادًا إلى فاتورة الشحن.</span><span class="sxs-lookup"><span data-stu-id="7d973-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="7d973-114">انقر فوق "معلومات ذات صلة".</span><span class="sxs-lookup"><span data-stu-id="7d973-114">Click Related information.</span></span>
2. <span data-ttu-id="7d973-115">انقر فوق "تفاصيل فاتورة الشحن".</span><span class="sxs-lookup"><span data-stu-id="7d973-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="7d973-116">انقر فوق "إنشاء كمبيالة/فاتورة الشحن".</span><span class="sxs-lookup"><span data-stu-id="7d973-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="7d973-117">في الحقل "الفاتورة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7d973-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="7d973-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7d973-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="7d973-119">تسوية الفاتورة</span><span class="sxs-lookup"><span data-stu-id="7d973-119">Reconcile the invoice</span></span>
<span data-ttu-id="7d973-120">عند تسوية فاتورة الشركة وفاتورة الشحن، يتم ذلك كل بند بعد الآخر.</span><span class="sxs-lookup"><span data-stu-id="7d973-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="7d973-121">انقر فوق "مطابقة فواتير الشحن والفواتير".</span><span class="sxs-lookup"><span data-stu-id="7d973-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="7d973-122">قم بتوسيع المقطع "تفاصيل الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="7d973-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="7d973-123">قم بتوسيع المقطع "تفاصيل فاتورة الشحن غير المطابقة‬".</span><span class="sxs-lookup"><span data-stu-id="7d973-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="7d973-124">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7d973-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="7d973-125">انقر فوق "مطابقة".</span><span class="sxs-lookup"><span data-stu-id="7d973-125">Click Match.</span></span>
6. <span data-ttu-id="7d973-126">قم بتوسيع المقطع "تفاصيل فاتورة الشحن المطابقة‬".</span><span class="sxs-lookup"><span data-stu-id="7d973-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="7d973-127">تقديم الفاتورة للاعتماد</span><span class="sxs-lookup"><span data-stu-id="7d973-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="7d973-128">انقر فوق "إرسال" للموافقة.</span><span class="sxs-lookup"><span data-stu-id="7d973-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="7d973-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7d973-129">Close the page.</span></span>
3. <span data-ttu-id="7d973-130">امسح تحديد خانة الاختيار "إخفاء الموافقة‬".</span><span class="sxs-lookup"><span data-stu-id="7d973-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="7d973-131">انقر فوق "دفاتر يومية فاتورة المورّد".</span><span class="sxs-lookup"><span data-stu-id="7d973-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="7d973-132">انقر لمتابعة الارتباط الوارد في الحقل "رقم دفتر يومية المرجع‬".</span><span class="sxs-lookup"><span data-stu-id="7d973-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="7d973-133">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="7d973-133">Click Lines.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]