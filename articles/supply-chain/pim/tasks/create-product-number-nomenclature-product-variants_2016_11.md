---
title: إنشاء nomenclature لرقم منتج لمتغيرات المنتج المعرفة مسبقًا‬‏‫
description: يوضح هذا الإجراء كيفية إعداد كود nomenclature لرقم المنتج لمتغيرات المنتج المكوّنة، وكيف يمكن إرفاقه بأصل منتج قابل للتكوين.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921001"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="bbaac-103">إنشاء nomenclature لرقم منتج لمتغيرات المنتج المعرفة مسبقًا‬‏‫</span><span class="sxs-lookup"><span data-stu-id="bbaac-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bbaac-104">يوضح هذا الإجراء كيفية إعداد كود nomenclature لرقم المنتج لمتغيرات المنتج المكوّنة، وكيف يمكن إرفاقه بأصل منتج قابل للتكوين.</span><span class="sxs-lookup"><span data-stu-id="bbaac-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="bbaac-105">يوضح هذا الإجراء أيضًا كيف يمكنك بناء nomenclature تكوين لمكون نموذج تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="bbaac-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="bbaac-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="bbaac-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bbaac-107">يتم تعيين nomenclature رقم المنتج الجديد إلى أصل المنتج D0004.</span><span class="sxs-lookup"><span data-stu-id="bbaac-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="bbaac-108">وعادة ما تُنفذ هذه المهمة عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="bbaac-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="bbaac-109">إنشاء nomenclature لرقم المنتج</span><span class="sxs-lookup"><span data-stu-id="bbaac-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="bbaac-110">انتقل إلى **إدارة معلومات المنتج \> إعداد \> ‏‫كود nomenclature للمنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="bbaac-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-111">Select **New**.</span></span>
1. <span data-ttu-id="bbaac-112">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="bbaac-113">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="bbaac-114">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-114">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-115">حدد **رقم أصل المنتج**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="bbaac-116">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-116">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-117">حدد **الثابت النصي**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="bbaac-118">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bbaac-119">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="bbaac-120">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-120">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-121">حدد **تكوين**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="bbaac-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="bbaac-123">تعيين nomenclature رقم المنتج إلى أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="bbaac-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="bbaac-124">‏‫انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> أصول المنتجات‬‬**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="bbaac-125">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="bbaac-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bbaac-126">على سبيل المثال، قم بإجراء التصفية على حقل **رقم المنتج** باستخدام قيمة "D".</span><span class="sxs-lookup"><span data-stu-id="bbaac-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="bbaac-127">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="bbaac-128">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-128">Select **Edit**.</span></span>
1. <span data-ttu-id="bbaac-129">حدد *نعم* في الحقل **استخدام كود nomenclature**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="bbaac-130">أدخل قيمة أو حددها في حقل **كود nomenclature لرقم متغير المنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="bbaac-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-131">Close the page.</span></span>
1. <span data-ttu-id="bbaac-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="bbaac-133">إنشاء nomenclature لمكون نموذج تكوين منتج</span><span class="sxs-lookup"><span data-stu-id="bbaac-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="bbaac-134">انتقل إلى **إدارة معلومات المنتج \> المنتجات \> نماذج تكوين المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="bbaac-135">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bbaac-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="bbaac-136">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="bbaac-137">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-137">Select **Edit**.</span></span>
1. <span data-ttu-id="bbaac-138">حدد *نعم* في حقل **استخدام كود nomenclature للتكوين**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="bbaac-139">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-139">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-140">حدد **قيمة السمة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="bbaac-141">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bbaac-142">في حقل **التسمية**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bbaac-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="bbaac-143">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-143">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-144">حدد **الثابت النصي**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="bbaac-145">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bbaac-146">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="bbaac-147">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-147">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-148">حدد **قيمة السمة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="bbaac-149">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bbaac-150">في حقل **التسمية**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bbaac-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="bbaac-151">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-151">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-152">حدد **الثابت النصي**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="bbaac-153">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bbaac-154">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="bbaac-155">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-155">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-156">حدد **قيمة السمة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="bbaac-157">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bbaac-158">في حقل **التسمية**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bbaac-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="bbaac-159">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-159">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-160">حدد **الثابت النصي**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="bbaac-161">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bbaac-162">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="bbaac-163">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-163">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-164">حدد **قيمة السمة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="bbaac-165">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bbaac-166">في حقل **التسمية**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bbaac-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="bbaac-167">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-167">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-168">حدد **الثابت النصي**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="bbaac-169">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bbaac-170">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="bbaac-171">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-171">Select **Add**.</span></span>
1. <span data-ttu-id="bbaac-172">حدد **قيمة التسلسل الرقمي**.</span><span class="sxs-lookup"><span data-stu-id="bbaac-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="bbaac-173">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bbaac-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bbaac-174">في حقل **التسلسل الرقمي**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bbaac-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="bbaac-175">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-175">Close the page.</span></span>
1. <span data-ttu-id="bbaac-176">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-176">Close the page.</span></span>
1. <span data-ttu-id="bbaac-177">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bbaac-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]