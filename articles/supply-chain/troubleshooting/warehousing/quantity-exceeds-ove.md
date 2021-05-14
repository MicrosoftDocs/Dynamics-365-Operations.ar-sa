---
title: لا يمكنك تاكيد الشحنة نظرا لان الكمية تتجاوز النسبة المئوية للتسليم الزائد.
description: لا يمكنك تاكيد الشحنة نظرا لان الكمية تتجاوز النسبة المئوية للتسليم الزائد.
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938416"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a><span data-ttu-id="68d54-103">لا يمكنك تاكيد الشحنة نظرا لان الكمية تتجاوز النسبة المئوية للتسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="68d54-103">You can't confirm a shipment because the quantity exceeds the overdelivery percentage</span></span>

<span data-ttu-id="68d54-104">رمز الخطأ: WAX1687</span><span class="sxs-lookup"><span data-stu-id="68d54-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="68d54-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="68d54-105">Symptoms</span></span>

<span data-ttu-id="68d54-106">عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:</span><span class="sxs-lookup"><span data-stu-id="68d54-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="68d54-107">تعذر تأكيد الشحنة للحمل %1 لأن كميه الصنف %2 تتجاوز النسبة المئوية التي تم تحديدها للتسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="68d54-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for overdelivery.</span></span>

<span data-ttu-id="68d54-108">وبالتالي، لا يمكنك تاكيد الشحن للتحميل.</span><span class="sxs-lookup"><span data-stu-id="68d54-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="68d54-109">السبب</span><span class="sxs-lookup"><span data-stu-id="68d54-109">Cause</span></span>

<span data-ttu-id="68d54-110">تم انتقاء كميه التحميل أو الشحن جزئيا فقط.</span><span class="sxs-lookup"><span data-stu-id="68d54-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="68d54-111">تتجاوز الكمية حاليًا الكمية المنتقاة بنسبة مئوية خارج النسبة المئوية للتسليم الزائد المسموح بها.</span><span class="sxs-lookup"><span data-stu-id="68d54-111">The quantity currently exceeds the picked quantity by a percentage that is outside the allowed overdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="68d54-112">الدقة</span><span class="sxs-lookup"><span data-stu-id="68d54-112">Resolution</span></span>

<span data-ttu-id="68d54-113">لإصلاح هذه المشكلة، أكمل إحدى المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="68d54-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="68d54-114">يستخدم في تعيين كميه بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="68d54-114">Set the load line quantity.</span></span>
- <span data-ttu-id="68d54-115">قم بتعيين النسبة المئوية للتسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="68d54-115">Set the overdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="68d54-116">يستخدم في تعيين كميه بند التحميل</span><span class="sxs-lookup"><span data-stu-id="68d54-116">Set the load line quantity</span></span>

<span data-ttu-id="68d54-117">لتعيين كمية بند الحمل، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="68d54-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="68d54-118">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="68d54-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="68d54-119">حدد الحمل الذي لا يمكن تأكيد الشحنة له.</span><span class="sxs-lookup"><span data-stu-id="68d54-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="68d54-120">في علامة التبويب السريعة، **بنود الحمل**، حدد بند الحمل للعنصر الذي يتجاوز النسبة المئوية للتسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="68d54-120">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="68d54-121">في علامة التبويب السريعة **تفاصيل البنود**، حدد **أمر**.</span><span class="sxs-lookup"><span data-stu-id="68d54-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="68d54-122">في حقل **الكمية**، عيّن القيمة إلى الكمية المنتقاة (أي إلى قيمة **كمية العمل الذي تم إنشاؤه**)، بحيث يمكن أن يحدث تأكيد الشحنة.</span><span class="sxs-lookup"><span data-stu-id="68d54-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-overdelivery-percentage"></a><span data-ttu-id="68d54-123">تعيين النسبة المئوية للتسليم الزائد</span><span class="sxs-lookup"><span data-stu-id="68d54-123">Set the overdelivery percentage</span></span>

<span data-ttu-id="68d54-124">لتعيين النسبة المئوية للتسليم الناقص، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="68d54-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="68d54-125">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="68d54-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="68d54-126">حدد الحمل الذي لا يمكن تأكيد الشحنة له.</span><span class="sxs-lookup"><span data-stu-id="68d54-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="68d54-127">في علامة التبويب السريعة، **بنود الحمل**، حدد بند الحمل للعنصر الذي يتجاوز النسبة المئوية للتسليم الزائد.</span><span class="sxs-lookup"><span data-stu-id="68d54-127">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="68d54-128">في علامة التبويب السريعة **تفاصيل البنود**، حدد **عام**.</span><span class="sxs-lookup"><span data-stu-id="68d54-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="68d54-129">في حقل **التسليم الزائد**، عيّن القيمة إلى نسبة مئوية أكبر تستوعب الكمية التي تم انتقاؤها مقابل كمية التحميل، بحيث يمكن تأكيد الشحنة.</span><span class="sxs-lookup"><span data-stu-id="68d54-129">In the **Overdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
