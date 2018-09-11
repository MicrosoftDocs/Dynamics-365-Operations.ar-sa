--- 
title: "إنشاء مستند تحويل لتحويل مخزون داخلي"
description: "يوضح هذا الإجراء كيفية إنشاء مستندات التحويل لحركة البضائع داخل شركة."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1dc48b3d8761f72bbdf2c611c9280960f7ee119b
ms.contentlocale: ar-sa
ms.lasthandoff: 09/11/2018

---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a><span data-ttu-id="45194-103">إنشاء مستند تحويل لتحويل مخزون داخلي</span><span class="sxs-lookup"><span data-stu-id="45194-103">Generate a transfer document for an internal inventory transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45194-104">يوضح هذا الإجراء كيفية إنشاء مستندات التحويل لحركة البضائع داخل شركة.</span><span class="sxs-lookup"><span data-stu-id="45194-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="45194-105">يتوفر هذا الإجراء فقط للكيانات القانونية التي يقع عنوانها الرئيسي في ليتوانيا.</span><span class="sxs-lookup"><span data-stu-id="45194-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="45194-106">تم إنشاء الإجراء باستخدام شركة بيانات العرض التوضيحي DEMF مع عنوان رئيسي في ليتوانيا.</span><span class="sxs-lookup"><span data-stu-id="45194-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="45194-107">قبل إتمام هذا الإجراء، يجب إكمال الإجراء "إعداد مستندات التحويل لحركة البضائع داخل شركة".</span><span class="sxs-lookup"><span data-stu-id="45194-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="45194-108">هذا الإجراء مخصص لمحاسبي المخزون‬.</span><span class="sxs-lookup"><span data-stu-id="45194-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="45194-109">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="45194-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="45194-110">إنشاء أمر التحويل</span><span class="sxs-lookup"><span data-stu-id="45194-110">Create a transfer order</span></span>
1. <span data-ttu-id="45194-111">انتقل إلى إدارة المخزون > الأوامر الواردة > أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="45194-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="45194-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="45194-112">Click New.</span></span>
3. <span data-ttu-id="45194-113">في الحقل "من المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="45194-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="45194-114">في الحقل "إلى المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="45194-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="45194-115">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="45194-115">Click Add.</span></span>
6. <span data-ttu-id="45194-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="45194-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="45194-117">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="45194-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="45194-118">إدخال تفاصيل التحويل لأمر التحويل</span><span class="sxs-lookup"><span data-stu-id="45194-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="45194-119">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="45194-119">Click Save.</span></span>
2. <span data-ttu-id="45194-120">في جزء الإجراءات، انقر فوق "شحن".</span><span class="sxs-lookup"><span data-stu-id="45194-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="45194-121">انقر فوق "تفاصيل النقل".</span><span class="sxs-lookup"><span data-stu-id="45194-121">Click Transportation details.</span></span>
4. <span data-ttu-id="45194-122">حدد "نعم" في الحقل "تفاصيل نقل الطباعة".</span><span class="sxs-lookup"><span data-stu-id="45194-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="45194-123">في الحقل "صرف البضائع بتاريخ"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="45194-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="45194-124">في الحقل "الحزمة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="45194-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="45194-125">في الحقل "مستوى المخاطرة للحمولة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="45194-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="45194-126">في حقل "شركة النقل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="45194-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="45194-127">في الحقل "النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="45194-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="45194-128">في الحقل "رقم التسجيل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="45194-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="45194-129">في الحقل "رقم تسجيل العربة الملحقة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="45194-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="45194-130">في حقل "السائق"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="45194-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="45194-131">في الحقل "اسم السائق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="45194-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="45194-132">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="45194-132">Click Save.</span></span>
15. <span data-ttu-id="45194-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="45194-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="45194-134">عرض إيصال التعبئة الخاص بأمر التحويل غير المرحّل</span><span class="sxs-lookup"><span data-stu-id="45194-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="45194-135">انقر فوق "إيصال التعبئة".</span><span class="sxs-lookup"><span data-stu-id="45194-135">Click Packing slip.</span></span>
2. <span data-ttu-id="45194-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="45194-136">Click OK.</span></span>
3. <span data-ttu-id="45194-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="45194-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="45194-138">عرض إيصال التعبئة الخاص بأمر التحويل المرحّل</span><span class="sxs-lookup"><span data-stu-id="45194-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="45194-139">في جزء الإجراءات، انقر فوق "أمر التحويل".</span><span class="sxs-lookup"><span data-stu-id="45194-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="45194-140">في جزء الإجراءات، انقر فوق "شحن".</span><span class="sxs-lookup"><span data-stu-id="45194-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="45194-141">انقر فوق "أمر تحويل الشحنة‬".</span><span class="sxs-lookup"><span data-stu-id="45194-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="45194-142">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="45194-142">Click the General tab.</span></span>
5. <span data-ttu-id="45194-143">في الحقل "تحديث"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="45194-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="45194-144">انقر فوق علامة التبويب نظرة عامة.</span><span class="sxs-lookup"><span data-stu-id="45194-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="45194-145">في الحقل "إيصال التعبئة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="45194-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="45194-146">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="45194-146">Click OK.</span></span>
9. <span data-ttu-id="45194-147">في جزء الإجراءات، انقر فوق "شحن".</span><span class="sxs-lookup"><span data-stu-id="45194-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="45194-148">انقر فوق "إيصال التعبئة".</span><span class="sxs-lookup"><span data-stu-id="45194-148">Click Packing slip.</span></span>
11. <span data-ttu-id="45194-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="45194-149">Click OK.</span></span>


