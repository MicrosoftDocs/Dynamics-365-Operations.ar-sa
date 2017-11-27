---
title: "إضافة عنصر التحكم في التوصيات لصفحة الحركة على جهاز نقطة البيع"
description: "يوضح هذا الموضوع كيفية إضافة عنصر تحكم في التوصيات لشاشة الحركة على جهاز نقطة البيع باستخدام مصمم تخطيط الشاشة في Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47ad5dc8fd698f6f543c6a48e2c7eb01d4e148e6
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="5ba91-103">إضافة عنصر التحكم في التوصيات لصفحة الحركة على جهاز نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="5ba91-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="5ba91-104">يوضح هذا الموضوع كيفية إضافة عنصر تحكم في التوصيات لشاشة الحركة على جهاز نقطة البيع باستخدام مصمم تخطيط الشاشة في Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="5ba91-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="5ba91-105">يمكنك عرض توصيات المنتج على جهاز نقطة البيع الخاص بك عندما تستخدم Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="5ba91-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="5ba91-106">وتُعد *التوصيات* هي الأصناف التي قد يكون عميلك مهتم بها بناءً على محفوظات الشراء الخاصة بهم، والأصناف الموجودة في قائمة الأمنيات الخاصة بهم، والأصناف التي قام العملاء الآخرين بشرائها عبر الإنترنت والمتاجر التقليدية.</span><span class="sxs-lookup"><span data-stu-id="5ba91-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="5ba91-107">لعرض توصيات المنتج، تحتاج إلى إضافة عنصر تحكم إلى شاشة الحركة باستخدام مصمم تخطيط الشاشة.</span><span class="sxs-lookup"><span data-stu-id="5ba91-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="5ba91-108">فتح مصمم التخطيط</span><span class="sxs-lookup"><span data-stu-id="5ba91-108">Open Layout designer</span></span>
1.  <span data-ttu-id="5ba91-109">انتقل إلى **البيع بالتجزئة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **نقطة البيع** &gt; **تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="5ba91-110">استخدم عامل التصفية السريع للعثور على الشاشة التي ترغب في إضافة عامل التحكم إليها.</span><span class="sxs-lookup"><span data-stu-id="5ba91-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="5ba91-111">على سبيل المثال، إضافة عامل التصفية على حقل **معرف تخطيط الشاشة** باستخدام قيمة 'F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="5ba91-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="5ba91-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5ba91-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="5ba91-113">على سبيل المثال، حدد ‘الاسم: F2CP16:9M معرف تخطيط الشاشة: F2CP16:9M’.</span><span class="sxs-lookup"><span data-stu-id="5ba91-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="5ba91-114">انقر فوق **مصمم التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="5ba91-115">اتبع المطالبات لتشغيل مصمم التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5ba91-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="5ba91-116">عند مطالبتك ببيانات الاعتماد، أدخل نفس بيانات الاعتماد التي تم استخدامها عندما تم تشغيل مصمم التخطيط من صفحة **تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="5ba91-117">عندما تقوم بتسجيل الدخول، سوف تظهر لك صفحة تشبه الصفحة الموجودة أدناه.</span><span class="sxs-lookup"><span data-stu-id="5ba91-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="5ba91-118">سوف يكون التخطيط مختلفًا اعتمادًا على التخصيصات التي تم إجراؤها لمتجرك.</span><span class="sxs-lookup"><span data-stu-id="5ba91-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="5ba91-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) اختر خيار عرض</span><span class="sxs-lookup"><span data-stu-id="5ba91-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="5ba91-120">يتوفر خياران للتكوينات.</span><span class="sxs-lookup"><span data-stu-id="5ba91-120">There are two configurations options available.</span></span> <span data-ttu-id="5ba91-121">قم باختيار الخيار الأفضل لمتجرك، ثم اتبع الإرشادات المتبقية لإنهاء إعداد عنصر التحكم.</span><span class="sxs-lookup"><span data-stu-id="5ba91-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="5ba91-122">الخياران المتاحان هما:</span><span class="sxs-lookup"><span data-stu-id="5ba91-122">The two options are:</span></span>
-   <span data-ttu-id="5ba91-123">دائمًا ما تكون التوصيات مرئية.</span><span class="sxs-lookup"><span data-stu-id="5ba91-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="5ba91-124">تظهر علامة تبويب **توصيات** في الشبكة على الجانب الأيمن من الشاشة.</span><span class="sxs-lookup"><span data-stu-id="5ba91-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="5ba91-125">لجعل التوصيات مرئية دائمًا.</span><span class="sxs-lookup"><span data-stu-id="5ba91-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="5ba91-126">قم بتقليل ارتفاع منطقة تفاصيل سطور الحركة لتكون في نفس ارتفاع جزء العميل الموجود إلى يسارها.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="5ba91-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="5ba91-127">من القائمة الموجودة على اليسار، قم بسحب وإفلات عنصر تحكيم التوصيات بين منطقة تفاصيل سطور الحركة وزر الشبكة في منتصف أسفل شاشة الحركة.</span><span class="sxs-lookup"><span data-stu-id="5ba91-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="5ba91-128">قم بتغيير حجم عنصر التحكم بحيث تتلائم في هذه المساحة.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="5ba91-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="5ba91-129">انقر فوق **X** للحفظ والخروج من مصمم التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5ba91-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="5ba91-130">في Dynamics 365 for Retail، انتقل إلى **البيع بالتجزئة** &gt; **تكنولوجيا معلومات البيع بالتجزئة** &gt; **جداول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="5ba91-131">من القائمة المنسدلة، قم بتحديد **سجلات 1090**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="5ba91-132">انقر فوق **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="5ba91-133">لإضافة علامة تبويب توصيات إلى شبكة الأزرار على الجانب الأيمن من الشاشة</span><span class="sxs-lookup"><span data-stu-id="5ba91-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="5ba91-134">انقر بزر الماوس الأيمن فوق المساحة الفارغة أسفل علامة التبويب الأخيرة على شبكة الأزرار الموجودة على الجانب الأيمن من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5ba91-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="5ba91-135">انقر فوق **تخصيص**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="5ba91-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="5ba91-136">انقر فوق **علامة تبويب جديدة**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="5ba91-137">ابحث عن علامة التبويب الجديدة التي قمت بإضافتها.</span><span class="sxs-lookup"><span data-stu-id="5ba91-137">Find the new tab that you just added.</span></span> <span data-ttu-id="5ba91-138">قد تحتاج إلى التمرير لأسفل.</span><span class="sxs-lookup"><span data-stu-id="5ba91-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="5ba91-139">من القائمة المنسدلة **محتويات**، قم بتحديد **المنتجات الموصى بها**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="5ba91-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="5ba91-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="5ba91-141">في حقل **التسمية** ، اكتب اسمًا لعلامة تبويب التوصيلات. على سبيل المثال، اكتب "المنتجات الموصى بها‬".</span><span class="sxs-lookup"><span data-stu-id="5ba91-141">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="5ba91-142">في حقل **صورة**، قم بتحديد الصورة لتظهر على علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="5ba91-142">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="5ba91-143">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-143">Click **OK**.</span></span> <span data-ttu-id="5ba91-144">سوف تظهر علامة التبويب الجديدة في شبكة الأزرار.</span><span class="sxs-lookup"><span data-stu-id="5ba91-144">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="5ba91-145">انقر فوق **X** للحفظ والخروج من مصمم التخطيط.</span><span class="sxs-lookup"><span data-stu-id="5ba91-145">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="5ba91-146">في Dynamics 365 for Retail، انتقل إلى **البيع بالتجزئة** &gt; **تكنولوجيا معلومات البيع بالتجزئة** &gt; **جداول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-146">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="5ba91-147">من القائمة المنسدلة، قم بتحديد **سجلات 1090**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-147">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="5ba91-148">انقر فوق **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="5ba91-148">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="5ba91-149">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="5ba91-149">See also</span></span>
--------

[<span data-ttu-id="5ba91-150">نظرة عامة حول توصيات المنتج المخصصة</span><span class="sxs-lookup"><span data-stu-id="5ba91-150">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




