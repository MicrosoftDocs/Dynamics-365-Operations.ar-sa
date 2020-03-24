---
title: إضافة توصيات إلى شاشة الحركة
description: يوضح هذا الموضوع كيفية إضافة عنصر تحكم في التوصيات لشاشة الحركة على جهاز نقطة البيع باستخدام مصمم تخطيط الشاشة في Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/12/20
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
ms.openlocfilehash: 9117f398ee1d9edbd3aee9bed366eea225964184
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127665"
---
# <a name="add-recommendations-to-the-transaction-screen"></a><span data-ttu-id="a005d-103">إضافة توصيات إلى شاشة الحركة</span><span class="sxs-lookup"><span data-stu-id="a005d-103">Add recommendations to the transaction screen</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="a005d-104">يوضح هذا الموضوع كيفية إضافة عنصر تحكم في التوصيات لشاشة الحركة على جهاز نقطة البيع باستخدام مصمم تخطيط الشاشة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a005d-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="a005d-105">لمزيد من المعلومات حول توصيات المنتجات، اقرأ [توصيات المنتجات على وثائق نقطة البيع](product.md).</span><span class="sxs-lookup"><span data-stu-id="a005d-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="a005d-106">يمكنك عرض توصيات المنتجات على جهاز نقطة البيع عندما تستخدم Commerce.</span><span class="sxs-lookup"><span data-stu-id="a005d-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="a005d-107">لعرض توصيات المنتج، تحتاج إلى إضافة عنصر تحكم إلى شاشة الحركة باستخدام مصمم تخطيط الشاشة.</span><span class="sxs-lookup"><span data-stu-id="a005d-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="a005d-108">فتح مصمم التخطيط</span><span class="sxs-lookup"><span data-stu-id="a005d-108">Open Layout designer</span></span>

1. <span data-ttu-id="a005d-109">انتقال إلى **البيع بالتجزئة والتجارة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **نقطة البيع** &gt; **تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="a005d-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="a005d-110">استخدم عامل التصفية السريع للعثور على الشاشة التي ترغب في إضافة عامل التحكم إليها.</span><span class="sxs-lookup"><span data-stu-id="a005d-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="a005d-111">على سبيل المثال، نفّذ التصفية في حقل **معرف تخطيط الشاشة** باستخدام قيمة **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="a005d-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="a005d-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="a005d-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="a005d-113">على سبيل المثال، حدد **الاسم: F2CP16:9M معرف تخطيط الشاشة: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="a005d-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="a005d-114">انقر فوق **مصمم التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="a005d-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="a005d-115">اتبع المطالبات لتشغيل مصمم التخطيط.</span><span class="sxs-lookup"><span data-stu-id="a005d-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="a005d-116">عند مطالبتك ببيانات الاعتماد، أدخل بيانات الاعتماد نفسها التي تم استخدامها عندما تم تشغيل مصمم التخطيط من صفحة **تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="a005d-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="a005d-117">عندما تقوم بتسجيل الدخول، سوف تظهر لك صفحة تشبه الصفحة الموجودة أدناه.</span><span class="sxs-lookup"><span data-stu-id="a005d-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="a005d-118">سوف يكون التخطيط مختلفًا اعتمادًا على التخصيصات التي تم إجراؤها لمتجرك.</span><span class="sxs-lookup"><span data-stu-id="a005d-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="a005d-119">[![مصمم التخطيط](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="a005d-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="a005d-120">تحديد خيار عرض</span><span class="sxs-lookup"><span data-stu-id="a005d-120">Choose a display option</span></span>

<span data-ttu-id="a005d-121">يتوفر خياران للتكوينات.</span><span class="sxs-lookup"><span data-stu-id="a005d-121">There are two configurations options available.</span></span> <span data-ttu-id="a005d-122">قم باختيار الخيار الأفضل لمتجرك، ثم اتبع الإرشادات المتبقية لإنهاء إعداد عنصر التحكم.</span><span class="sxs-lookup"><span data-stu-id="a005d-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="a005d-123">الخياران المتاحان هما:</span><span class="sxs-lookup"><span data-stu-id="a005d-123">The two options are:</span></span>

- <span data-ttu-id="a005d-124">دائمًا ما تكون التوصيات مرئية.</span><span class="sxs-lookup"><span data-stu-id="a005d-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="a005d-125">تظهر علامة تبويب **التوصيات** في الشبكة على الجانب الأيسر من الشاشة.</span><span class="sxs-lookup"><span data-stu-id="a005d-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="a005d-126">جعل التوصيات مرئية دائمًا</span><span class="sxs-lookup"><span data-stu-id="a005d-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="a005d-127">قم بتقليل ارتفاع منطقة تفاصيل سطور الحركة بحيث يصبح ارتفاعها مماثلاً للوحة العميل إلى يسارها.</span><span class="sxs-lookup"><span data-stu-id="a005d-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="a005d-128">[![تقليل ارتفاع منطقة تفاصيل سطور الحركة](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="a005d-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="a005d-129">من القائمة الموجودة على اليسار، قم بسحب وإفلات عنصر تحكيم التوصيات بين منطقة تفاصيل سطور الحركة وزر الشبكة في منتصف أسفل شاشة الحركة.</span><span class="sxs-lookup"><span data-stu-id="a005d-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="a005d-130">قم بتغيير حجم عنصر التحكم بحيث تحتويه هذه المساحة.</span><span class="sxs-lookup"><span data-stu-id="a005d-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="a005d-131">[![إضافة عناصر التحكم في التوصيات إلى التخطيط](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="a005d-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="a005d-132">انقر فوق **X** للحفظ والخروج من مصمم التخطيط.</span><span class="sxs-lookup"><span data-stu-id="a005d-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="a005d-133">فب Commerce، انتقل إلى **البيع بالتجزئة والتجارة** &gt; **تكنولوجيا معلومات البيع بالتجزئة والتجارة** &gt; **جداول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="a005d-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="a005d-134">من القائمة المنسدلة، قم بتحديد **سجلات 1090**.</span><span class="sxs-lookup"><span data-stu-id="a005d-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="a005d-135">انقر فوق **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="a005d-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="a005d-136">إضافة علامة تبويب التوصيات إلى شبكة الأزرار على الجانب الأيسر من الشاشة</span><span class="sxs-lookup"><span data-stu-id="a005d-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="a005d-137">انقر بزر الماوس الأيمن فوق المساحة الفارغة أسفل علامة التبويب الأخيرة على شبكة الأزرار الموجودة على الجانب الأيمن من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a005d-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="a005d-138">انقر فوق **تخصيص‏‎**.</span><span class="sxs-lookup"><span data-stu-id="a005d-138">Click **Customize**.</span></span>

    <span data-ttu-id="a005d-139">[![التخصيص - مربع حوار عنصر التحكم في التبويب](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="a005d-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="a005d-140">انقر فوق **علامة تبويب جديدة**.</span><span class="sxs-lookup"><span data-stu-id="a005d-140">Click **New tab**.</span></span>
4. <span data-ttu-id="a005d-141">ابحث عن علامة التبويب الجديدة التي قمت بإضافتها.</span><span class="sxs-lookup"><span data-stu-id="a005d-141">Find the new tab that you just added.</span></span> <span data-ttu-id="a005d-142">قد تحتاج إلى التمرير لأسفل.</span><span class="sxs-lookup"><span data-stu-id="a005d-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="a005d-143">من القائمة المنسدلة **محتويات**، قم بتحديد **المنتجات الموصى بها**.</span><span class="sxs-lookup"><span data-stu-id="a005d-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="a005d-144">[![تحديد المنتجات الموصى بها في حقل المحتويات](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="a005d-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="a005d-145">في حقل **التسمية** ، اكتب اسمًا لعلامة تبويب التوصيات. على سبيل المثال، اكتب "المنتجات الموصى بها‬".</span><span class="sxs-lookup"><span data-stu-id="a005d-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="a005d-146">في حقل **صورة**، قم بتحديد الصورة لتظهر على علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="a005d-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="a005d-147">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a005d-147">Click **OK**.</span></span> <span data-ttu-id="a005d-148">سوف تظهر علامة التبويب الجديدة في شبكة الأزرار.</span><span class="sxs-lookup"><span data-stu-id="a005d-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="a005d-149">انقر فوق **X** للحفظ والخروج من مصمم التخطيط.</span><span class="sxs-lookup"><span data-stu-id="a005d-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="a005d-150">فب Commerce، انتقل إلى **البيع بالتجزئة والتجارة** &gt; **تكنولوجيا معلومات البيع بالتجزئة والتجارة** &gt; **جداول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="a005d-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="a005d-151">من القائمة المنسدلة، قم بتحديد **سجلات 1090**.</span><span class="sxs-lookup"><span data-stu-id="a005d-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="a005d-152">انقر فوق **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="a005d-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a005d-153">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a005d-153">Additional resources</span></span>

[<span data-ttu-id="a005d-154">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="a005d-154">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a005d-155">تمكين ADLS في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a005d-155">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="a005d-156">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="a005d-156">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a005d-157">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="a005d-157">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="a005d-158">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="a005d-158">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="a005d-159">إضافة قوائم توصيات المنتجات إلى موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="a005d-159">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="a005d-160">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="a005d-160">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="a005d-161">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="a005d-161">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="a005d-162">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="a005d-162">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a005d-163">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="a005d-163">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a005d-164">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="a005d-164">Product recommendations FAQ</span></span>](faq-recommendations.md)
