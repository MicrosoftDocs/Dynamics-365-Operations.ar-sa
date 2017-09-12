---
title: "نظرة عامة على توصيات المنتجات المخصصة"
description: "في Dynamics 365 for Retail، يمكن عرض توصيات المنتج على جهاز نقطة البيع. وتُعد التوصيات هي الأصناف التي قد يكون عميلك مهتم بها بناءً على محفوظات الشراء الخاصة بهم، والأصناف الموجودة في قائمة الأمنيات الخاصة بهم، والأصناف التي قام العملاء الآخرين بشرائها عبر الإنترنت والمتاجر التقليدية. لتجار التجزئة مع الكتالوجات الكبيرة، تساعد التوصيات العميل في اكتشاف المنتج. من خلال عرض منتجات تستهدف اهتمامات العملاء والعادات الشرائية، يمكن لتوصيات المنتج مساعدة تجار التجزئة في عمليات البيع الإضافي والبيع التكميلي، ويمكنها تحسين آلية الاحتفاظ بالعملاء. في Dynamics 365 for Retail، يتم تشغيل توصيات المنتج من خلال الخدمات الإدراكية والتعلم الآلي من Microsoft Azure."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: a3a3b5e87a797c29c13b180c248d1782805c4c31
ms.contentlocale: ar-sa
ms.lasthandoff: 06/29/2017


---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="9be8b-107">نظرة عامة على توصيات المنتجات المخصصة</span><span class="sxs-lookup"><span data-stu-id="9be8b-107">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="9be8b-108">في Dynamics 365 for Retail، يمكن عرض توصيات المنتج على جهاز نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="9be8b-108">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="9be8b-109">وتُعد التوصيات هي الأصناف التي قد يكون عميلك مهتم بها بناءً على محفوظات الشراء الخاصة بهم، والأصناف الموجودة في قائمة الأمنيات الخاصة بهم، والأصناف التي قام العملاء الآخرين بشرائها عبر الإنترنت والمتاجر التقليدية.</span><span class="sxs-lookup"><span data-stu-id="9be8b-109">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="9be8b-110">لتجار التجزئة مع الكتالوجات الكبيرة، تساعد التوصيات العميل في اكتشاف المنتج.</span><span class="sxs-lookup"><span data-stu-id="9be8b-110">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="9be8b-111">من خلال عرض منتجات تستهدف اهتمامات العملاء والعادات الشرائية، يمكن لتوصيات المنتج مساعدة تجار التجزئة في عمليات البيع الإضافي والبيع التكميلي، ويمكنها تحسين آلية الاحتفاظ بالعملاء.</span><span class="sxs-lookup"><span data-stu-id="9be8b-111">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="9be8b-112">في Dynamics 365 for Retail، يتم تشغيل توصيات المنتج من خلال الخدمات الإدراكية والتعلم الآلي من Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9be8b-112">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>

<a name="scenarios"></a><span data-ttu-id="9be8b-113">السيناريوهات</span><span class="sxs-lookup"><span data-stu-id="9be8b-113">Scenarios</span></span>
---------

<span data-ttu-id="9be8b-114">يتم تمكين توصيات المنتج لسيناريوهات نقطة البيع التالية.</span><span class="sxs-lookup"><span data-stu-id="9be8b-114">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="9be8b-115">تتوافر في نقطة بيع المجموعة (POS) أو نقطة بيع حديثة (MPOS).</span><span class="sxs-lookup"><span data-stu-id="9be8b-115">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="9be8b-116">في صفحة **تفاصيل المنتجات**:</span><span class="sxs-lookup"><span data-stu-id="9be8b-116">On the **Product details** page:</span></span>

-   <span data-ttu-id="9be8b-117">إذا قام موظف المتجر بزيارة صفحة **تفاصيل المنتج** عند النظر في الحركات السابقة عبر القنوات المختلفة، فإن محرك التوصيات يقترح بنود إضافية والتي من المرجح شرائها معًا.</span><span class="sxs-lookup"><span data-stu-id="9be8b-117">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="9be8b-118">إذا قام موظف المتجر بإضافة عميل إلى الحركة، ثم قام بزيارة صفحة **تفاصيل المنتج**، فيوفر محرك التوصيات توصيات مخصصة باستخدام محفوظات حركة العميل.</span><span class="sxs-lookup"><span data-stu-id="9be8b-118">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="9be8b-119">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="9be8b-119">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="9be8b-120">في صفحة **الحركة**:</span><span class="sxs-lookup"><span data-stu-id="9be8b-120">On the **Transaction** page:</span></span>

-   <span data-ttu-id="9be8b-121">يقترح محرك التوصيات الأصناف استنادًا إلى قائمة كاملة من العناصر الموجودة في السلة.</span><span class="sxs-lookup"><span data-stu-id="9be8b-121">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="9be8b-122">إذا قام موظف المتجر بإضافة عميل إلى الحركة، فمن ثم يوفر محرك التوصيات توصيات شخصية باستخدام محفوظات حركة العميل، وقائمة بالأصناف الموجودة في السلة.</span><span class="sxs-lookup"><span data-stu-id="9be8b-122">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

<span data-ttu-id="9be8b-123">**ملاحظة** لعرض التوصيات على صفحة **الحركة**، يحتاج تاجر التجزئة إلى تحديث تخطيط الشاشة في Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="9be8b-123">**Note**  To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="9be8b-124">يجب إسقاط عنصر تحكم **التوصيات** داخل صفحة **الحركة**.</span><span class="sxs-lookup"><span data-stu-id="9be8b-124">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="9be8b-125">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="9be8b-125">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="9be8b-126">في صفحة **تفاصيل العميل**:</span><span class="sxs-lookup"><span data-stu-id="9be8b-126">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="9be8b-127">يقترح محرك التوصيات الأصناف استنادًا إلى مُعرف المستخدم والأصناف الموجودة في قائمة أمنيات العميل.</span><span class="sxs-lookup"><span data-stu-id="9be8b-127">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="9be8b-128">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="9be8b-128">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="9be8b-129">تكوين Dynamics 365 for Retail لتمكين توصيات نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="9be8b-129">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="9be8b-130">لإعداد توصيات المنتج، تحتاج إلى القيام بالتالي.</span><span class="sxs-lookup"><span data-stu-id="9be8b-130">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="9be8b-131">تأكد من أنك قمت بتحديد **الكيان القانوني**الصحيح.</span><span class="sxs-lookup"><span data-stu-id="9be8b-131">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="9be8b-132">الانتقال إلى **متجر الكيان**، حدد **مبيعات بالتجزئة**، ثم انقر فوق **تحديث**. * * * * سوف يستخدم هذا بيانات العرض التجريبي (أو بياناتك) من قاعدة البيانات التشغيلية، ويقوم بنقلها إلى متجر الكيان.</span><span class="sxs-lookup"><span data-stu-id="9be8b-132">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.** **This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="9be8b-133">اختياري: لعرض التوصيات على شاشة الحركة، انتقل إلى * * "تخطيط الشاشة"، **اختر تخطيط الشاشة الخاص بك، ثم قم بإطلاق **مصمم تخطيط الشاشة**،** * * ثم قم بإفلات * * عنصر تحكم في التوصيات * * عند الحاجة.</span><span class="sxs-lookup"><span data-stu-id="9be8b-133">Optional: To display recommendations on the transaction screen, go to **Screen Layout, **choose your screen layout, launch the **Screen layout designer**,** **and then drop the **recommendations control **where needed.</span></span>
4.  <span data-ttu-id="9be8b-134">انتقل إلى **معلمات البيع بالتجزئة**، حدد **التعلم الآلي**، حدد * * نعم * * تحت **"تمكين توصيات نقطة البيع"**.</span><span class="sxs-lookup"><span data-stu-id="9be8b-134">Go to **Retail parameters**, select **Machine-learning**, select **Yes **under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="9be8b-135">لمشاهدة التوصيات في نقطة البيع، قم بتشغيل وظيفة التكوين العمومي **1110**.</span><span class="sxs-lookup"><span data-stu-id="9be8b-135">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="9be8b-136">لعكس التغييرات التي تم إجراؤها لمصم تخطيط شاشة نقطة البيع، قم بتشغيل وظيفة تكوين قناة **1070**.</span><span class="sxs-lookup"><span data-stu-id="9be8b-136">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="9be8b-137">[]()كيف يعمل؟</span><span class="sxs-lookup"><span data-stu-id="9be8b-137">[]()How does it work?</span></span>
<span data-ttu-id="9be8b-138">عند تحديث كيان **متجر الكيان**، تحدث الإجراءات التالية.</span><span class="sxs-lookup"><span data-stu-id="9be8b-138">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="9be8b-139">يتم استخراج البيانات بالتنسيق المطلوب من خلال الخدمات المعرفية من قاعدة البيانات التشغيلية لـ Dynamics 365 for Retail، وإرسالها إلى متجر الكيان.</span><span class="sxs-lookup"><span data-stu-id="9be8b-139">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="9be8b-140">تستخدم البيانات بواسطة Azure Data Factory لمسح البيانات باستخدام برامج Hive النصية كجزء من أنشطة ADF.</span><span class="sxs-lookup"><span data-stu-id="9be8b-140">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="9be8b-141">يتم تخزين البيانات التي تم مسحها في مخزن الكائن الثنائي كبير الحجم.</span><span class="sxs-lookup"><span data-stu-id="9be8b-141">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="9be8b-142">تستخدم البيانات الموجودة من مخزن الكائن الثنائي كبير الحجم بواسطة الخدمات الإدراكية API لتدريب نموذج التوصيات.</span><span class="sxs-lookup"><span data-stu-id="9be8b-142">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="9be8b-143">عندما تقوم بتشغيل **تمكين التوصيات** وتشغيل وظائف التكوين، تحدث الإجراءات التالية.</span><span class="sxs-lookup"><span data-stu-id="9be8b-143">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="9be8b-144">تم انتقاء بيانات الاعتماد النموذجية والمُعرف من API وتخزينها في قاعدة البيانات التشغيلية لـ Dynamics 365 for Retail، في web.config لـ AOS، وكذلك في خادم البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="9be8b-144">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="9be8b-145">تتاح بيانات الاعتماد النموذجية والمُعرف لـ CRT بحيث يتم الوفاء بطلبات توصيات المنتجات من نقطة بيع المجموعة و نقطة البيع الحديثة (MPOS) في وضع الاتصال.</span><span class="sxs-lookup"><span data-stu-id="9be8b-145">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="9be8b-146">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="9be8b-146">See also</span></span>
--------

[<span data-ttu-id="9be8b-147">إضافة عنصر التحكم في التوصيات لصفحة الحركة على جهاز نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="9be8b-147">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




