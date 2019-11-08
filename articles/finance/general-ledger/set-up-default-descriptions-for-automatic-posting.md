---
title: إعداد أوصاف افتراضية للترحيل التلقائي
description: يشرح هذا الموضوع كيفية إعداد نص افتراضي يُستخدم لملء القيود المحاسبية التي تم ترحيلها تلقائيًا لدفتر الأستاذ العام. يمكنك إعداد نص وصف افتراضي باستخدام نص نموذج حر أو عن طريق تحديد متغيرات ثابتة.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb89f50a3d227cad80226ce30f71c4f210129245
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622679"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="0a4b5-104">إعداد أوصاف افتراضية للترحيل التلقائي</span><span class="sxs-lookup"><span data-stu-id="0a4b5-104">Set up default descriptions for automatic posting</span></span>

<span data-ttu-id="0a4b5-105">يشرح هذا الموضوع كيفية إعداد نص افتراضي يُستخدم لملء القيود المحاسبية التي تم ترحيلها تلقائيًا لدفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="0a4b5-106">يمكنك إعداد نص وصف افتراضي باستخدام نص نموذج حر أو عن طريق تحديد متغيرات ثابتة.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="0a4b5-107">بالنسبة لبعض أنواع حركات معيَّنة في بعض البلدان أو المناطق، يمكنك أيضًا تضمين نصوص من الحقول الموجودة في قاعدة البيانات Microsoft DynamicsAX المرتبطة بأنواع الحركات تلك.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="0a4b5-108">للحصول علي قائمة بأنواع الحركات والبلدان والمناطق، راجع قسم [‏‫اختياري: إضافة نص آخر إلى الأوصاف الافتراضية‬](#optional-add-other-text-to-default-descriptions) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="0a4b5-109">إعداد الأوصاف الافتراضية</span><span class="sxs-lookup"><span data-stu-id="0a4b5-109">Set up default descriptions</span></span>

1. <span data-ttu-id="0a4b5-110">انتقل إلى **إدارة المؤسسة** \> **إعداد** \> **الأوصاف الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="0a4b5-111">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="0a4b5-112">في الحقل **الوصف**، حدد نوع الحركة لإنشاء وصف افتراضي لها.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="0a4b5-113">في الحقل **اللغة**، حدد اللغة التي ينطبق عليها هذا الوصف.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="0a4b5-114">في الحقل **النص**، أدخل الوصف الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="0a4b5-115">يمكنك كتابة نص في الحقل، أو يمكنك استخدام واحد أو أكثر من متغيرات النص الحر التالية:</span><span class="sxs-lookup"><span data-stu-id="0a4b5-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="0a4b5-116">**%1** -يقوم بإضافة تاريخ الحركة.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="0a4b5-117">**%2**- يقوم بإضافة معرف يتوافق مع نوع المستند الذي يتم ترحيله إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="0a4b5-118">على سبيل المثال، بالنسبة لأنواع الحركات المرتبطة بالفواتير، يقوم المتغير **%2** بإضافة رقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="0a4b5-119">**%3**- يقوم بإضافة معرف يتوافق مع نوع المستند الذي يتم ترحيله إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="0a4b5-120">على سبيل المثال، بالنسبة لأنواع الحركات المرتبطة بالفواتير، يقوم المتغير **%3** بإضافة رقم حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="0a4b5-121">اختياري: إضافة نص آخر إلى الأوصاف الافتراضية</span><span class="sxs-lookup"><span data-stu-id="0a4b5-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="0a4b5-122">بالنسبة لبعض أنواع حركات معيَّنة في بعض البلدان أو المناطق، يمكن أن تتضمن الأوصاف الافتراضية نصًا مستمدًا من الحقول بالبيانات المرتبطة بأنواع الحركات تلك.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="0a4b5-123">تُظهر القوائم التالية أنواع الحركات والبلدان والمناطق التي يتوفر بها هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="0a4b5-124">**أنواع الحركات**</span><span class="sxs-lookup"><span data-stu-id="0a4b5-124">**Transaction types**</span></span>

<span data-ttu-id="0a4b5-125">يمكنك إضافة نص آخر للأوصاف الافتراضية لأنواع الحركات المرتبطة بأنواع المستندات التالية:</span><span class="sxs-lookup"><span data-stu-id="0a4b5-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="0a4b5-126">فواتير العميل</span><span class="sxs-lookup"><span data-stu-id="0a4b5-126">Customer invoices</span></span>
- <span data-ttu-id="0a4b5-127">اشعارات ائتمان العميل</span><span class="sxs-lookup"><span data-stu-id="0a4b5-127">Customer credit notes</span></span>
- <span data-ttu-id="0a4b5-128">المدفوعات النقدية الخاصة بالعميل</span><span class="sxs-lookup"><span data-stu-id="0a4b5-128">Customer cash payments</span></span>
- <span data-ttu-id="0a4b5-129">مدفوعات المورد</span><span class="sxs-lookup"><span data-stu-id="0a4b5-129">Vendor payments</span></span>
- <span data-ttu-id="0a4b5-130">أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="0a4b5-130">Sales orders</span></span>
- <span data-ttu-id="0a4b5-131">أوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="0a4b5-131">Purchase orders</span></span>
- <span data-ttu-id="0a4b5-132">دفاتر يومية المخزون</span><span class="sxs-lookup"><span data-stu-id="0a4b5-132">Inventory journals</span></span>
- <span data-ttu-id="0a4b5-133">التخطيط الرئيسي (MRP)</span><span class="sxs-lookup"><span data-stu-id="0a4b5-133">Master planning (MRP)</span></span>
- <span data-ttu-id="0a4b5-134">الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="0a4b5-134">Fixed assets</span></span>

<span data-ttu-id="0a4b5-135">**البلدان والمناطق**</span><span class="sxs-lookup"><span data-stu-id="0a4b5-135">**Countries and regions**</span></span>

<span data-ttu-id="0a4b5-136">يتوفر هذا الخيار للبلدان والمناطق التالية:</span><span class="sxs-lookup"><span data-stu-id="0a4b5-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="0a4b5-137">البرازيل</span><span class="sxs-lookup"><span data-stu-id="0a4b5-137">Brazil</span></span>
- <span data-ttu-id="0a4b5-138">الصين</span><span class="sxs-lookup"><span data-stu-id="0a4b5-138">China</span></span>
- <span data-ttu-id="0a4b5-139">جمهورية التشيك</span><span class="sxs-lookup"><span data-stu-id="0a4b5-139">Czech Republic</span></span>
- <span data-ttu-id="0a4b5-140">أوروبا الشرقية</span><span class="sxs-lookup"><span data-stu-id="0a4b5-140">Eastern Europe</span></span>
- <span data-ttu-id="0a4b5-141">المجر</span><span class="sxs-lookup"><span data-stu-id="0a4b5-141">Hungary</span></span>
- <span data-ttu-id="0a4b5-142">الهند</span><span class="sxs-lookup"><span data-stu-id="0a4b5-142">India</span></span>
- <span data-ttu-id="0a4b5-143">اليابان</span><span class="sxs-lookup"><span data-stu-id="0a4b5-143">Japan</span></span>
- <span data-ttu-id="0a4b5-144">لتوانيا</span><span class="sxs-lookup"><span data-stu-id="0a4b5-144">Lithuania</span></span>
- <span data-ttu-id="0a4b5-145">لاتفيا</span><span class="sxs-lookup"><span data-stu-id="0a4b5-145">Latvia</span></span>
- <span data-ttu-id="0a4b5-146">بولندا</span><span class="sxs-lookup"><span data-stu-id="0a4b5-146">Poland</span></span>
- <span data-ttu-id="0a4b5-147">روسيا</span><span class="sxs-lookup"><span data-stu-id="0a4b5-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="0a4b5-148">إضافة نص آخر إلى الأوصاف الافتراضية</span><span class="sxs-lookup"><span data-stu-id="0a4b5-148">Add text to default descriptions</span></span>

<span data-ttu-id="0a4b5-149">بعد إكمال الخطوات المذكورة في [‏‫إعداد الأوصاف الافتراضية‬](#set-up-default-descriptions) سابقًا في هذا الموضوع، اتبع هذه الخطوات لإضافة نص آخر إلى الأوصاف الافتراضية:</span><span class="sxs-lookup"><span data-stu-id="0a4b5-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="0a4b5-150">على علامة التبويب السريعة **المحددات** ، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="0a4b5-151">في الحقل **‏‫جدول المراجع‬**، حدد جدول قاعدة البيانات الذي ستقوم بإضافة بيانات المعلمة منه إلى الوصف.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="0a4b5-152">في الحقل **‏‫حقل المراجع‬**، حدد الحقل الذي ستقوم بإضافة بيانات المعلمة منه إلى الوصف.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="0a4b5-153">كرر الخطوات من 1 إلى 3 لإضافة مزيد من المعلمات.</span><span class="sxs-lookup"><span data-stu-id="0a4b5-153">Repeat steps 1 through 3 to add more parameters.</span></span>
