---
title: مراقبة مخزون الشحن باستخدام تعاون المورّد
description: يوضح هذا الإجراء كيفية استخدام تعاون المورّد لعرض معلومات حول مستوى مخزون المنتج الذي قمت بوضعها في الشحن مع عميل.
author: sherry-zheng
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e397c12b9f605d1c864ce053477090ed8c1700
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839261"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="0c4c7-103">مراقبة مخزون الشحن باستخدام تعاون المورّد</span><span class="sxs-lookup"><span data-stu-id="0c4c7-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c4c7-104">يوضح هذا الإجراء كيفية استخدام تعاون المورّد لعرض معلومات حول مستوى مخزون المنتج الذي قمت بوضعها في الشحن مع عميل.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="0c4c7-105">يمكنك أيضًا مراقبة استهلاك المخزون عند يأخذ العميل ملكية المخزون.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="0c4c7-106">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="0c4c7-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="0c4c7-108">عرض المخزون المستهلك</span><span class="sxs-lookup"><span data-stu-id="0c4c7-108">View consumed inventory</span></span>
1. <span data-ttu-id="0c4c7-109">انتقل إلى تعاون المورد‬ > مخزون الشحن‬ > المنتجات التي تم استلامها من مخزون الشحن‬.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="0c4c7-110">تعرض القائمة بنود إيصال استلام المنتجات‬ التي تم إنشاؤها عندما تغيرت ملكية مخزون الشحن من المورّد إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="0c4c7-111">قد تحتاج إلى التمرير إلى اليمين لعرض الكميات ومعلومات أخرى.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="0c4c7-112">ويمكنك استخدام المعلومات الموجودة في هذه القائمة لإنشاء فواتير للعميل.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="0c4c7-113">يمكنك أيضًا تصدير البيانات إلى Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="0c4c7-114">انقر فوق "عرض أمر الشراء‬".</span><span class="sxs-lookup"><span data-stu-id="0c4c7-114">Click View purchase order.</span></span>
3. <span data-ttu-id="0c4c7-115">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="0c4c7-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="0c4c7-116">يتم وضع علامة "الشحن" على البند، ويوضح مقطع الرأس أن حالة أمر الشراء هي "مستلم".</span><span class="sxs-lookup"><span data-stu-id="0c4c7-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="0c4c7-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="0c4c7-118">عرض المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="0c4c7-118">View on-hand inventory</span></span>
1. <span data-ttu-id="0c4c7-119">انتقل إلى تعاون المورد‬ > مخزون الشحن‬ > مخزون الشحن الفعلي‬‬.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="0c4c7-120">تظهر الصفحة "مخزون الشحن الفعلي‬" المخزون الذي تملكه في مستودع العميل.</span><span class="sxs-lookup"><span data-stu-id="0c4c7-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="0c4c7-121">يمكنك إظهار أبعاد إضافية، مثل الموقع والمستودع، بالنقر فوق علامة التبويب "عرض الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="0c4c7-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]