---
title: كود المورد غير معتمد لمنتج وتاريخ محددين
description: عند محاولة تأكيد أمر مخطط أو إضافة بند إلى أمر شراء، فإنك تتلقى رسالة خطأ توضح أن كود المورد غير مخول لأحد المنتجات والتواريخ.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294005"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="a3156-103">كود المورد غير معتمد لمنتج وتاريخ محددين</span><span class="sxs-lookup"><span data-stu-id="a3156-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="a3156-104">رمز الخطأ: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="a3156-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="a3156-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="a3156-105">Symptoms</span></span>

<span data-ttu-id="a3156-106">عند محاولة تأكيد أمر مخطط أو إضافة بند إلى أمر الشراء، تظهر رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="a3156-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="a3156-107">لم يتم اعتماد كود المورّد  %1 لـ %2 على %3.</span><span class="sxs-lookup"><span data-stu-id="a3156-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="a3156-108">السبب</span><span class="sxs-lookup"><span data-stu-id="a3156-108">Cause</span></span>

<span data-ttu-id="a3156-109">يحدث الخطأ نظرًا إلى أنه يتم تعيين **أسلوب التحقق من المورِّد المعتمَد** على *التحذير فقط* أو *غير مسموح* للمنتج المحدد، والمورد غير مخول حاليًا بتقديم ذلك المنتج.</span><span class="sxs-lookup"><span data-stu-id="a3156-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="a3156-110">الحل</span><span class="sxs-lookup"><span data-stu-id="a3156-110">Resolution</span></span>

<span data-ttu-id="a3156-111">لحل هذه المشكلة، قم إما بتعطيل فحص المورد للمنتج ذي الصلة أو الموافقة على المورد.</span><span class="sxs-lookup"><span data-stu-id="a3156-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="a3156-112">لتعطيل فحص المورد لأحد المنتجات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a3156-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="a3156-113">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="a3156-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="a3156-114">افتح المنتج ذا الصلة.</span><span class="sxs-lookup"><span data-stu-id="a3156-114">Open the relevant product.</span></span>
1. <span data-ttu-id="a3156-115">في علامة التبويب السريعة **الشراء**، قم بتعيين الحقل **أسلوب التحقق من المورد المعتمد** إلى قيمة غير *التحذير فقط* أو *غير مسموح*.</span><span class="sxs-lookup"><span data-stu-id="a3156-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="a3156-116">للموافقة على مورد لأحد المنتجات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a3156-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="a3156-117">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="a3156-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="a3156-118">افتح الصنف ذا الصلة.</span><span class="sxs-lookup"><span data-stu-id="a3156-118">Open the relevant item.</span></span>
1. <span data-ttu-id="a3156-119">في جزء الإجراءات، في علامة التبويب **شراء**، في المجموعة **مورّد معتمد**، حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="a3156-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="a3156-120">في صفحة قائمة **مورّد معتمد**، أضف صف إلى الشبكة، وقم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a3156-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="a3156-121">**المورد** – حدد المورد للموافقة على المنتج الحالي.</span><span class="sxs-lookup"><span data-stu-id="a3156-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="a3156-122">**تاريخ السريان** – حدد أول تاريخ قام فيه المورد بالاعتماد.</span><span class="sxs-lookup"><span data-stu-id="a3156-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="a3156-123">**تاريخ انتهاء الصلاحية** – حدد آخر تاريخ قام فيه المورد بالاعتماد.</span><span class="sxs-lookup"><span data-stu-id="a3156-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="a3156-124">لمزيد من المعلومات، راجع [اعتماد الموردين لمنتجات محددة](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="a3156-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
