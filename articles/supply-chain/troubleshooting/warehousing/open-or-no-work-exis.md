---
title: لا يمكنك تاكيد الشحنة بسبب العمل غير المكتمل أو المفقود
description: لا يمكنك تاكيد الشحنة بسبب العمل غير المكتمل أو المفقود
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
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938414"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="aaa21-103">لا يمكنك تاكيد الشحنة بسبب العمل غير المكتمل أو المفقود</span><span class="sxs-lookup"><span data-stu-id="aaa21-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="aaa21-104">رمز الخطأ: WAX515</span><span class="sxs-lookup"><span data-stu-id="aaa21-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="aaa21-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="aaa21-105">Symptoms</span></span>

<span data-ttu-id="aaa21-106">عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:</span><span class="sxs-lookup"><span data-stu-id="aaa21-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="aaa21-107">تعذر تأكيد شحن الحمولة %1 لأنه يجب إكمال جميع أعمال الحمولة.</span><span class="sxs-lookup"><span data-stu-id="aaa21-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="aaa21-108">وبالتالي، لا يمكنك تاكيد الشحن للتحميل.</span><span class="sxs-lookup"><span data-stu-id="aaa21-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="aaa21-109">السبب</span><span class="sxs-lookup"><span data-stu-id="aaa21-109">Cause</span></span>

<span data-ttu-id="aaa21-110">الحمولة أو الشحنة في حالة فشل فيها تأكيد الشحنة.</span><span class="sxs-lookup"><span data-stu-id="aaa21-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="aaa21-111">قبل أن تتمكن من تأكيد الشحنة، يجب توفر بعض الأعمال على الأقل للحمل، ويجب أن يكون لكل هذا العمل حالة *مقفل* أو *ملغى*.</span><span class="sxs-lookup"><span data-stu-id="aaa21-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="aaa21-112">الدقة</span><span class="sxs-lookup"><span data-stu-id="aaa21-112">Resolution</span></span>

<span data-ttu-id="aaa21-113">تحقق من أوامر المبيعات أو أوامر التحويل ذات الصلة الخاصة بالحمل أو الشحن، وتاكد من اكتمال كافة الاعمال ذات الصلة أو إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="aaa21-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="aaa21-114">ويمكنك التعامل مع الشحنات والأحمال في العديد من الصفحات.</span><span class="sxs-lookup"><span data-stu-id="aaa21-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="aaa21-115">توفر الأقسام الفرعية التالية أمثله قليله.</span><span class="sxs-lookup"><span data-stu-id="aaa21-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="aaa21-116">صفحة كل الأحمال</span><span class="sxs-lookup"><span data-stu-id="aaa21-116">All loads page</span></span>

1. <span data-ttu-id="aaa21-117">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="aaa21-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="aaa21-118">حدد الحمل الذي لا يمكن تأكيد الشحنة له.</span><span class="sxs-lookup"><span data-stu-id="aaa21-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="aaa21-119">في جزء الإجراءات، في علامة التبويب **الأحمال**، في مجموعة **المعلومات ذات الصلة**، حدد **العمل**.</span><span class="sxs-lookup"><span data-stu-id="aaa21-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="aaa21-120">افحص حالة كل معرف عمل.</span><span class="sxs-lookup"><span data-stu-id="aaa21-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="aaa21-121">تابع كل معرف عمل ليس له حالة *مقفل* أو *ملغي*.</span><span class="sxs-lookup"><span data-stu-id="aaa21-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="aaa21-122">عندما تكون حاله كل معرف عمل هي *مقفل* أو *ملغى*، حاول مرة أخرى لتاكيد الشحنة.</span><span class="sxs-lookup"><span data-stu-id="aaa21-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="aaa21-123">صفحة كل الشحنات</span><span class="sxs-lookup"><span data-stu-id="aaa21-123">All shipments page</span></span>

1. <span data-ttu-id="aaa21-124">انتقل إلى **إدارة المستودعات \> الشحنات \> جميع الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="aaa21-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="aaa21-125">حدد الشحنة التي لا يمكن تأكيدها.</span><span class="sxs-lookup"><span data-stu-id="aaa21-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="aaa21-126">في جزء الإجراءات، ضمن علامة التبويب **الشحنات**، في مجموعة **العمل**، حدد **تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="aaa21-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="aaa21-127">افحص حالة كل معرف عمل.</span><span class="sxs-lookup"><span data-stu-id="aaa21-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="aaa21-128">تابع كل معرف عمل ليس له حالة *مقفل* أو *ملغي*.</span><span class="sxs-lookup"><span data-stu-id="aaa21-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="aaa21-129">عندما تكون حاله كل معرف عمل هي *مقفل* أو *ملغى*، حاول مرة أخرى لتاكيد الشحنة.</span><span class="sxs-lookup"><span data-stu-id="aaa21-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="aaa21-130">صفحة كل العمل</span><span class="sxs-lookup"><span data-stu-id="aaa21-130">All work page</span></span>

1. <span data-ttu-id="aaa21-131">انتقل إلى **إدارة المستودعات \> العمل\> كل العمل**.</span><span class="sxs-lookup"><span data-stu-id="aaa21-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="aaa21-132">حدد العمل لرقم الأمر الذي لا يمكن تأكيد الشحنة له.</span><span class="sxs-lookup"><span data-stu-id="aaa21-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="aaa21-133">في "جزء الإجراءات"، في علامة التبويب **الشحن**، في مجموعة **الشحن**، حدد **تأكيد الشحن**.</span><span class="sxs-lookup"><span data-stu-id="aaa21-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="aaa21-134">افحص حالة كل معرف عمل.</span><span class="sxs-lookup"><span data-stu-id="aaa21-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="aaa21-135">تابع كل معرف عمل ليس له حالة *مقفل* أو *ملغي*.</span><span class="sxs-lookup"><span data-stu-id="aaa21-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="aaa21-136">عندما تكون حاله كل معرف عمل هي *مقفل* أو *ملغى*، حاول مرة أخرى لتاكيد الشحنة.</span><span class="sxs-lookup"><span data-stu-id="aaa21-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
