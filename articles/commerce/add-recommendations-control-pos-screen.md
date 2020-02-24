---
title: إضافة عنصر تحكم في التوصيات إلى شاشة الحركة على أجهزة نقطة البيع (POS)
description: يوضح هذا الموضوع كيفية إضافة عنصر تحكم في التوصيات لشاشة الحركة على جهاز نقطة البيع باستخدام مصمم تخطيط الشاشة في Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6d6f48197a36f633e3cd63cbad4518f53946fc7f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021433"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="86817-103">إضافة عنصر تحكم في التوصيات إلى شاشة الحركة على أجهزة نقطة البيع (POS)</span><span class="sxs-lookup"><span data-stu-id="86817-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="86817-104">يوضح هذا الموضوع كيفية إضافة عنصر تحكم في التوصيات لشاشة الحركة على جهاز نقطة البيع باستخدام مصمم تخطيط الشاشة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86817-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="86817-105">لمزيد من المعلومات حول توصيات المنتجات، اقرأ [توصيات المنتجات على وثائق نقطة البيع](product.md).</span><span class="sxs-lookup"><span data-stu-id="86817-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="86817-106">يمكنك عرض توصيات المنتجات على جهاز نقطة البيع عندما تستخدم Commerce.</span><span class="sxs-lookup"><span data-stu-id="86817-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="86817-107">لعرض توصيات المنتج، تحتاج إلى إضافة عنصر تحكم إلى شاشة الحركة باستخدام مصمم تخطيط الشاشة.</span><span class="sxs-lookup"><span data-stu-id="86817-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="86817-108">فتح مصمم التخطيط</span><span class="sxs-lookup"><span data-stu-id="86817-108">Open Layout designer</span></span>

1. <span data-ttu-id="86817-109">انتقال إلى **البيع بالتجزئة والتجارة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **نقطة البيع** &gt; **تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="86817-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="86817-110">استخدم عامل التصفية السريع للعثور على الشاشة التي ترغب في إضافة عامل التحكم إليها.</span><span class="sxs-lookup"><span data-stu-id="86817-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="86817-111">على سبيل المثال، نفّذ التصفية في حقل **معرف تخطيط الشاشة** باستخدام قيمة **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="86817-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="86817-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="86817-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="86817-113">على سبيل المثال، حدد **الاسم: F2CP16:9M معرف تخطيط الشاشة: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="86817-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="86817-114">انقر فوق **مصمم التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="86817-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="86817-115">اتبع المطالبات لتشغيل مصمم التخطيط.</span><span class="sxs-lookup"><span data-stu-id="86817-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="86817-116">عند مطالبتك ببيانات الاعتماد، أدخل بيانات الاعتماد نفسها التي تم استخدامها عندما تم تشغيل مصمم التخطيط من صفحة **تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="86817-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="86817-117">عندما تقوم بتسجيل الدخول، سوف تظهر لك صفحة تشبه الصفحة الموجودة أدناه.</span><span class="sxs-lookup"><span data-stu-id="86817-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="86817-118">سوف يكون التخطيط مختلفًا اعتمادًا على التخصيصات التي تم إجراؤها لمتجرك.</span><span class="sxs-lookup"><span data-stu-id="86817-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="86817-119">[![مصمم التخطيط](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="86817-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="86817-120">تحديد خيار عرض</span><span class="sxs-lookup"><span data-stu-id="86817-120">Choose a display option</span></span>

<span data-ttu-id="86817-121">يتوفر خياران للتكوينات.</span><span class="sxs-lookup"><span data-stu-id="86817-121">There are two configurations options available.</span></span> <span data-ttu-id="86817-122">قم باختيار الخيار الأفضل لمتجرك، ثم اتبع الإرشادات المتبقية لإنهاء إعداد عنصر التحكم.</span><span class="sxs-lookup"><span data-stu-id="86817-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="86817-123">الخياران المتاحان هما:</span><span class="sxs-lookup"><span data-stu-id="86817-123">The two options are:</span></span>

- <span data-ttu-id="86817-124">دائمًا ما تكون التوصيات مرئية.</span><span class="sxs-lookup"><span data-stu-id="86817-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="86817-125">تظهر علامة تبويب **التوصيات** في الشبكة على الجانب الأيسر من الشاشة.</span><span class="sxs-lookup"><span data-stu-id="86817-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="86817-126">جعل التوصيات مرئية دائمًا</span><span class="sxs-lookup"><span data-stu-id="86817-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="86817-127">قم بتقليل ارتفاع منطقة تفاصيل سطور الحركة بحيث يصبح ارتفاعها مماثلاً للوحة العميل إلى يسارها.</span><span class="sxs-lookup"><span data-stu-id="86817-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="86817-128">[![تقليل ارتفاع منطقة تفاصيل سطور الحركة](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="86817-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="86817-129">من القائمة الموجودة على اليسار، قم بسحب وإفلات عنصر تحكيم التوصيات بين منطقة تفاصيل سطور الحركة وزر الشبكة في منتصف أسفل شاشة الحركة.</span><span class="sxs-lookup"><span data-stu-id="86817-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="86817-130">قم بتغيير حجم عنصر التحكم بحيث تحتويه هذه المساحة.</span><span class="sxs-lookup"><span data-stu-id="86817-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="86817-131">[![إضافة عناصر التحكم في التوصيات إلى التخطيط](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="86817-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="86817-132">انقر فوق **X** للحفظ والخروج من مصمم التخطيط.</span><span class="sxs-lookup"><span data-stu-id="86817-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="86817-133">فب Commerce، انتقل إلى **البيع بالتجزئة والتجارة** &gt; **تكنولوجيا معلومات البيع بالتجزئة والتجارة** &gt; **جداول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="86817-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="86817-134">من القائمة المنسدلة، قم بتحديد **سجلات 1090**.</span><span class="sxs-lookup"><span data-stu-id="86817-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="86817-135">انقر فوق **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="86817-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="86817-136">إضافة علامة تبويب التوصيات إلى شبكة الأزرار على الجانب الأيسر من الشاشة</span><span class="sxs-lookup"><span data-stu-id="86817-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="86817-137">انقر بزر الماوس الأيمن فوق المساحة الفارغة أسفل علامة التبويب الأخيرة على شبكة الأزرار الموجودة على الجانب الأيمن من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="86817-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="86817-138">انقر فوق **تخصيص‏‎**.</span><span class="sxs-lookup"><span data-stu-id="86817-138">Click **Customize**.</span></span>

    <span data-ttu-id="86817-139">[![التخصيص - مربع حوار عنصر التحكم في التبويب](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="86817-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="86817-140">انقر فوق **علامة تبويب جديدة**.</span><span class="sxs-lookup"><span data-stu-id="86817-140">Click **New tab**.</span></span>
4. <span data-ttu-id="86817-141">ابحث عن علامة التبويب الجديدة التي قمت بإضافتها.</span><span class="sxs-lookup"><span data-stu-id="86817-141">Find the new tab that you just added.</span></span> <span data-ttu-id="86817-142">قد تحتاج إلى التمرير لأسفل.</span><span class="sxs-lookup"><span data-stu-id="86817-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="86817-143">من القائمة المنسدلة **محتويات**، قم بتحديد **المنتجات الموصى بها**.</span><span class="sxs-lookup"><span data-stu-id="86817-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="86817-144">[![تحديد المنتجات الموصى بها في حقل المحتويات](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="86817-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="86817-145">في حقل **التسمية** ، اكتب اسمًا لعلامة تبويب التوصيات. على سبيل المثال، اكتب "المنتجات الموصى بها‬".</span><span class="sxs-lookup"><span data-stu-id="86817-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="86817-146">في حقل **صورة**، قم بتحديد الصورة لتظهر على علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="86817-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="86817-147">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="86817-147">Click **OK**.</span></span> <span data-ttu-id="86817-148">سوف تظهر علامة التبويب الجديدة في شبكة الأزرار.</span><span class="sxs-lookup"><span data-stu-id="86817-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="86817-149">انقر فوق **X** للحفظ والخروج من مصمم التخطيط.</span><span class="sxs-lookup"><span data-stu-id="86817-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="86817-150">فب Commerce، انتقل إلى **البيع بالتجزئة والتجارة** &gt; **تكنولوجيا معلومات البيع بالتجزئة والتجارة** &gt; **جداول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="86817-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="86817-151">من القائمة المنسدلة، قم بتحديد **سجلات 1090**.</span><span class="sxs-lookup"><span data-stu-id="86817-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="86817-152">انقر فوق **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="86817-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86817-153">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="86817-153">Additional resources</span></span>

[<span data-ttu-id="86817-154">توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="86817-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="86817-155">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="86817-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)
