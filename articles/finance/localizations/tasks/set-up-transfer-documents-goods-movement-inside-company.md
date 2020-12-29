---
title: إعداد مستندات التحويل لحركة البضائع داخل شركة
description: يوضح هذا الإجراء كيفية إنشاء مستندات التحويل لحركة البضائع داخل شركة.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e85bd359ce1053629ad4217cf623e57b2976463a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439990"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="d8669-103">إعداد مستندات التحويل لحركة البضائع داخل شركة</span><span class="sxs-lookup"><span data-stu-id="d8669-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8669-104">يوضح هذا الإجراء كيفية إنشاء مستندات التحويل لحركة البضائع داخل شركة.</span><span class="sxs-lookup"><span data-stu-id="d8669-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="d8669-105">يتوفر هذا الإجراء فقط للكيانات القانونية التي يقع عنوانها الرئيسي في ليتوانيا.</span><span class="sxs-lookup"><span data-stu-id="d8669-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="d8669-106">تم إنشاء الإجراء باستخدام شركة بيانات العرض التوضيحي DEMF مع عنوان رئيسي في ليتوانيا.</span><span class="sxs-lookup"><span data-stu-id="d8669-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="d8669-107">قبل إتمام هذا الإجراء، يجب إكمال الإجراء "إعداد مستندات التحويل لحركة البضائع داخل شركة".</span><span class="sxs-lookup"><span data-stu-id="d8669-107">Before you can complete this procedure, you must complete the "Set up transfer documents for goods movement inside a company" procedure.</span></span> <span data-ttu-id="d8669-108">هذا الإجراء مخصص لمحاسبي المخزون‬.</span><span class="sxs-lookup"><span data-stu-id="d8669-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="d8669-109">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="d8669-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="d8669-110">إنشاء أمر التحويل</span><span class="sxs-lookup"><span data-stu-id="d8669-110">Create a transfer order</span></span>
1. <span data-ttu-id="d8669-111">انتقل إلى إدارة المخزون > الأوامر الواردة > أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="d8669-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="d8669-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d8669-112">Click New.</span></span>
3. <span data-ttu-id="d8669-113">في الحقل "من المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d8669-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="d8669-114">في الحقل "إلى المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d8669-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="d8669-115">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="d8669-115">Click Add.</span></span>
6. <span data-ttu-id="d8669-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d8669-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="d8669-117">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d8669-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="d8669-118">إدخال تفاصيل التحويل لأمر التحويل</span><span class="sxs-lookup"><span data-stu-id="d8669-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="d8669-119">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d8669-119">Click Save.</span></span>
2. <span data-ttu-id="d8669-120">في جزء الإجراءات، انقر فوق "شحن".</span><span class="sxs-lookup"><span data-stu-id="d8669-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="d8669-121">انقر فوق "تفاصيل النقل".</span><span class="sxs-lookup"><span data-stu-id="d8669-121">Click Transportation details.</span></span>
4. <span data-ttu-id="d8669-122">حدد "نعم" في الحقل "تفاصيل نقل الطباعة".</span><span class="sxs-lookup"><span data-stu-id="d8669-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="d8669-123">في الحقل "صرف البضائع بتاريخ"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d8669-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="d8669-124">في الحقل "الحزمة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d8669-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="d8669-125">في الحقل "مستوى المخاطرة للحمولة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d8669-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="d8669-126">في حقل "شركة النقل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d8669-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="d8669-127">في الحقل "النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d8669-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="d8669-128">في الحقل "رقم التسجيل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d8669-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="d8669-129">في الحقل "رقم تسجيل العربة الملحقة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d8669-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="d8669-130">في حقل "السائق"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d8669-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="d8669-131">في الحقل "اسم السائق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d8669-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="d8669-132">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d8669-132">Click Save.</span></span>
15. <span data-ttu-id="d8669-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d8669-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="d8669-134">عرض إيصال التعبئة الخاص بأمر التحويل غير المرحّل</span><span class="sxs-lookup"><span data-stu-id="d8669-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="d8669-135">انقر فوق "إيصال التعبئة".</span><span class="sxs-lookup"><span data-stu-id="d8669-135">Click Packing slip.</span></span>
2. <span data-ttu-id="d8669-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d8669-136">Click OK.</span></span>
3. <span data-ttu-id="d8669-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d8669-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="d8669-138">عرض إيصال التعبئة الخاص بأمر التحويل المرحّل</span><span class="sxs-lookup"><span data-stu-id="d8669-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="d8669-139">في جزء الإجراءات، انقر فوق "أمر التحويل".</span><span class="sxs-lookup"><span data-stu-id="d8669-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="d8669-140">في جزء الإجراءات، انقر فوق "شحن".</span><span class="sxs-lookup"><span data-stu-id="d8669-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="d8669-141">انقر فوق "أمر تحويل الشحنة‬".</span><span class="sxs-lookup"><span data-stu-id="d8669-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="d8669-142">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="d8669-142">Click the General tab.</span></span>
5. <span data-ttu-id="d8669-143">في الحقل "تحديث"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="d8669-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="d8669-144">انقر فوق علامة التبويب نظرة عامة.</span><span class="sxs-lookup"><span data-stu-id="d8669-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="d8669-145">في الحقل "إيصال التعبئة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d8669-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="d8669-146">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d8669-146">Click OK.</span></span>
9. <span data-ttu-id="d8669-147">في جزء الإجراءات، انقر فوق "شحن".</span><span class="sxs-lookup"><span data-stu-id="d8669-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="d8669-148">انقر فوق "إيصال التعبئة".</span><span class="sxs-lookup"><span data-stu-id="d8669-148">Click Packing slip.</span></span>
11. <span data-ttu-id="d8669-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d8669-149">Click OK.</span></span>

