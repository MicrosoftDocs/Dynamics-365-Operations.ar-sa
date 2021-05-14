---
title: رموز التصنيف الوطني لشحن السيارات (NMFC)
description: يصف هذا الموضوع كيفية التعامل مع أكواد التصنيف الوطني لشحن السيارات (NMFC) في Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941872"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="dbecb-103">رموز التصنيف الوطني لشحن السيارات (NMFC)</span><span class="sxs-lookup"><span data-stu-id="dbecb-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbecb-104">تساعدك رموز التصنيف الوطني لشحن السيارات (NMFC) على تصنيف العناصر التي يمكن شحنها.</span><span class="sxs-lookup"><span data-stu-id="dbecb-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="dbecb-105">رمز NMFC هو تسمية تُستخدم لتجميع السلع.</span><span class="sxs-lookup"><span data-stu-id="dbecb-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="dbecb-106">إنه يمكّن شركات النقل من تقييم البضائع للشحن عن طريق تصنيف العناصر بناءً على اعتبارات مثل ملاءمة الشاحنة، ومشكلات التحميل، ومسائل المناولة، وقابلية التلف.</span><span class="sxs-lookup"><span data-stu-id="dbecb-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="dbecb-107">يتم تجميع السلع في واحدة من 18 فئة شحن باستخدام مجموعة من الأرقام من 50 إلى 500.</span><span class="sxs-lookup"><span data-stu-id="dbecb-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="dbecb-108">تعتمد الفئة التي يتم تجميع السلع فيها على تقييم أربع خصائص للنقل: الكثافة، والتخزين، والمناولة، والمسؤولية.</span><span class="sxs-lookup"><span data-stu-id="dbecb-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="dbecb-109">ومعًا، تحدد هذه الخصائص قابلية نقل السلعة.</span><span class="sxs-lookup"><span data-stu-id="dbecb-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="dbecb-110">يرتبط رمز NMFC بكل عنصر شحن أقل من حمولة الشاحنة (LTL).</span><span class="sxs-lookup"><span data-stu-id="dbecb-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="dbecb-111">على سبيل المثال، قد يتم تعيين NMFC لجهاز كمبيوتر محمول مصنّف في 2.5، بينما قد يتم تعيين NMFC المصنف في 65 للأسلاك الكهربائية.</span><span class="sxs-lookup"><span data-stu-id="dbecb-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="dbecb-112">يمكن أن تساعد هذه الميزة العمال على استخدام أكواد NMFC لتصنيف عناصر الشحن LTL.</span><span class="sxs-lookup"><span data-stu-id="dbecb-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="dbecb-113">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="dbecb-113">Here are some examples:</span></span>

- <span data-ttu-id="dbecb-114">إذا أدرجت شركتك وصفًا للشحن في بوليصة الشحن (BOL)، فسيكون لدى شركة النقل فكرة ما عن ماهية الشحن.</span><span class="sxs-lookup"><span data-stu-id="dbecb-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="dbecb-115">يعتبر الشحن تصنيفًا مهمًا لأن العديد من شركات النقل تبني نموذج أعمالها بالكامل على أنواع الشحن التي يشحنونها.</span><span class="sxs-lookup"><span data-stu-id="dbecb-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="dbecb-116">قد يكون هذا التصنيف ضروريًا لشركتك لأنه يُستخدم لتحديد تكلفة حمولة معينة.</span><span class="sxs-lookup"><span data-stu-id="dbecb-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="dbecb-117">يمكن لشركتك تحديد ربحية شركة النقل والخدمات اللوجستية لـ LTL.</span><span class="sxs-lookup"><span data-stu-id="dbecb-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="dbecb-118">يصف هذا الموضوع كيفية العمل مع رموز NMFC في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dbecb-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dbecb-119">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="dbecb-119">Prerequisites</span></span>

<span data-ttu-id="dbecb-120">قبل أن تتمكن من إنشاء رموز NMFC، يجب عليك إعداد جميع فئات الشحن LTL التي يجب تعيينها لها.</span><span class="sxs-lookup"><span data-stu-id="dbecb-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="dbecb-121">تمثل فئات الشحن LTL فئات من العناصر، في حين ترتبط رموز NMFC بسلع محددة في كل فئة من فئات الشحن الثمانية عشر.</span><span class="sxs-lookup"><span data-stu-id="dbecb-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="dbecb-122">لمزيد من المعلومات حول كيفية العمل مع فئات LTL، راجع [فئات أقل من حمولة الشاحنة (LTL)](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="dbecb-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="dbecb-123">إنشاء رمز NMFC</span><span class="sxs-lookup"><span data-stu-id="dbecb-123">Create an NMFC code</span></span>

<span data-ttu-id="dbecb-124">لإنشاء رمز NMFC، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="dbecb-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="dbecb-125">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="dbecb-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="dbecb-126">انتقل إلى **إدارة المستودعات \> الإعداد \> المخزون \> رمز NMFC**.</span><span class="sxs-lookup"><span data-stu-id="dbecb-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="dbecb-127">انتقل إلى **إدارة النقل \> الإعداد \> معايير النقل \> فئات NMFC**.</span><span class="sxs-lookup"><span data-stu-id="dbecb-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="dbecb-128">حدد **جديد** لإنشاء رمز NMFC.</span><span class="sxs-lookup"><span data-stu-id="dbecb-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="dbecb-129">قم بعد ذلك بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="dbecb-129">Then set the following fields:</span></span>

    - <span data-ttu-id="dbecb-130">**رمز NMFC** – أدخل رمز NMFC لنوع السلعة.</span><span class="sxs-lookup"><span data-stu-id="dbecb-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="dbecb-131">**الاسم** – أدخل اسمًا لرمز NMFC.</span><span class="sxs-lookup"><span data-stu-id="dbecb-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="dbecb-132">**فئة LTL** – حدد فئة LTL المرتبطة برمز NMFC.</span><span class="sxs-lookup"><span data-stu-id="dbecb-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="dbecb-133">**وحدة مناولة BOL** – حدد نوع المناولة الافتراضي للشحنة.</span><span class="sxs-lookup"><span data-stu-id="dbecb-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="dbecb-134">مثال: إعداد رموز NMFC</span><span class="sxs-lookup"><span data-stu-id="dbecb-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="dbecb-135">يوضح المثال التالي كيفية إعداد رمزي NMFC مختلفين يمكن استخدامهما مع منتجات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="dbecb-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="dbecb-136">انتقل إلى **إدارة المستودعات \> الإعداد \> المخزون \> رمز NMFC**.</span><span class="sxs-lookup"><span data-stu-id="dbecb-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="dbecb-137">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="dbecb-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dbecb-138">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="dbecb-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dbecb-139">**رمز NMFC:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="dbecb-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="dbecb-140">**الاسم:** *أجهزة الكمبيوتر*</span><span class="sxs-lookup"><span data-stu-id="dbecb-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="dbecb-141">**فئة LTL:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="dbecb-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="dbecb-142">**وحدة مناولة BOL:** *الوحدة*</span><span class="sxs-lookup"><span data-stu-id="dbecb-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="dbecb-143">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="dbecb-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="dbecb-144">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="dbecb-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dbecb-145">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="dbecb-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dbecb-146">**رمز NMFC:** *125*</span><span class="sxs-lookup"><span data-stu-id="dbecb-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="dbecb-147">**الاسم:** *الهواتف*</span><span class="sxs-lookup"><span data-stu-id="dbecb-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="dbecb-148">**فئة LTL:** *125*</span><span class="sxs-lookup"><span data-stu-id="dbecb-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="dbecb-149">**وحدة مناولة BOL:** *الوحدة*</span><span class="sxs-lookup"><span data-stu-id="dbecb-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="dbecb-150">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="dbecb-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbecb-151">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="dbecb-151">Additional resources</span></span>

- [<span data-ttu-id="dbecb-152">أقل من فئات حمولة الشاحنات (LTL)</span><span class="sxs-lookup"><span data-stu-id="dbecb-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="dbecb-153">إنشاء بوليصة شحن</span><span class="sxs-lookup"><span data-stu-id="dbecb-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
