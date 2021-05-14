---
title: أقل من فئات حمولة الشاحنات (LTL)
description: يشرح هذا الموضوع ما هي فئات أقل من حمولة الشاحنة (LTL) ويصف كيفية إعدادها في Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941800"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="dd6dd-103">أقل من فئات حمولة الشاحنات (LTL)</span><span class="sxs-lookup"><span data-stu-id="dd6dd-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd6dd-104">فئة أقل من حمولة الشاحنة (LTL) هي فئة شحن تُستخدم لتصنيف العناصر التي يمكن شحنها.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="dd6dd-105">بشكل عام، يحتوي كل نوع من أنواع المنتجات أو السلع على رمز تصنيف وطني لشحن السيارات (NMFC) يتوافق مع رقم فئة شحن محدد لشحنات LTL.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="dd6dd-106">تمثل فئات الشحن LTL فئات من العناصر، في حين ترتبط رموز NMFC بسلع محددة في كل فئة من فئات الشحن الثمانية عشر.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="dd6dd-107">تتيح لك هذه الميزة استخدام نظامك لأداء المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="dd6dd-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="dd6dd-108">حدد فئات الشحن LTL المستخدمة في شركتك.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="dd6dd-109">قم بتعيين كل فئة LTL إلى رمز NMFC الموجود على صحة **رموز NMFC**.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="dd6dd-110">لمزيد من المعلومات، راجع [رموز التصنيف الوطني لشحن السيارات (NMFC)](nmfc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dd6dd-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="dd6dd-111">قم بتعيين رمز NMFC (وبالتالي رمز LTL المرتبط به) لكل منتج في صفحة **المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="dd6dd-112">قم بتقييم فئة LTL بدقة لكل منتج تم تعيين رمز NMFC له.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="dd6dd-113">حدد متطلبات التعبئة لكل فئة LTL عن طريق التحقق من معايير LTL الدولية.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="dd6dd-114">بهذه الطريقة، فإنك تضمن حماية منتجاتك جيدًا وشحنها بأمان.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="dd6dd-115">احصل على تقديرات شحن دقيقة، بناءً على فئة الشحن LTL لكل منتج.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="dd6dd-116">يصف هذا الموضوع كيفية إنشاء فئات LTL في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="dd6dd-117">إنشاء فئة LTL</span><span class="sxs-lookup"><span data-stu-id="dd6dd-117">Create an LTL class</span></span>

<span data-ttu-id="dd6dd-118">لإنشاء فئة LTL، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="dd6dd-119">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="dd6dd-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="dd6dd-120">انتقل إلى **إدارة المستودعات \> الإعداد \> المخزون \> فئات LTL**.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="dd6dd-121">انتقل إلى **إدارة النقل \> الإعداد \> معايير النقل \> فئات LTL**.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="dd6dd-122">في جزء الإجراءات، حدد **جديد** لإنشاء فئة LTL.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="dd6dd-123">قم بعد ذلك بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="dd6dd-123">Then set the following fields:</span></span>

    - <span data-ttu-id="dd6dd-124">**فئة LTL** – أدخل معرف فئة LTL الداخلي لشركتك لنوع السلعة.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="dd6dd-125">تستخدم معظم الشركات المعيار الدولي.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-125">Most companies use the international standard.</span></span> <span data-ttu-id="dd6dd-126">في هذه الحالة، ستطابق قيمة هذا الحقل قيمة حقل **الفئة**.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="dd6dd-127">ومع ذلك، إذا كانت شركتك تستخدم معيارها الخاص، فأدخل رمزًا يتوافق مع هذا المعيار.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="dd6dd-128">**الاسم** – أدخل اسمًا وصفيًا يساعدك أنت والمستخدمين الآخرين في تحديد فئة LTL الصحيحة لكل رمز NMFC.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="dd6dd-129">**الفئة** – أدخل معرّف فئة LTL القياسي الدولي لنوع السلعة.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="dd6dd-130">يجب أن يتوافق الرمز الذي تدخله هنا مع المعيار الرسمي.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="dd6dd-131">مثال: إعداد فئات LTL</span><span class="sxs-lookup"><span data-stu-id="dd6dd-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="dd6dd-132">يوضح المثال التالي كيفية إعداد فئتي LTL مختلفتين يمكنك استخدامهما مع أنواع مختلفة من المنتجات.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="dd6dd-133">انتقل إلى **إدارة المستودعات \> الإعداد \> المخزون \> فئات LTL**.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="dd6dd-134">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd6dd-135">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="dd6dd-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dd6dd-136">**فئة LTL:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="dd6dd-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="dd6dd-137">**الاسم:** *أجهزة الكمبيوتر، أجهزة العرض، الثلاجات*</span><span class="sxs-lookup"><span data-stu-id="dd6dd-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="dd6dd-138">**الفئة:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="dd6dd-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="dd6dd-139">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="dd6dd-140">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd6dd-141">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="dd6dd-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dd6dd-142">**فئة LTL:** *125*</span><span class="sxs-lookup"><span data-stu-id="dd6dd-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="dd6dd-143">**الاسم:** *الأجهزة المنزلية الصغيرة*</span><span class="sxs-lookup"><span data-stu-id="dd6dd-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="dd6dd-144">**الفئة:** *125*</span><span class="sxs-lookup"><span data-stu-id="dd6dd-144">**Class:** *125*</span></span>

1. <span data-ttu-id="dd6dd-145">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd6dd-146">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="dd6dd-146">Additional resources</span></span>

- [<span data-ttu-id="dd6dd-147">رموز التصنيف الوطني لشحن السيارات (NMFC)</span><span class="sxs-lookup"><span data-stu-id="dd6dd-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="dd6dd-148">إنشاء بوليصة شحن</span><span class="sxs-lookup"><span data-stu-id="dd6dd-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
