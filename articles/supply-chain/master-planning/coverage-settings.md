---
title: "إعدادات التغطية"
description: "تستخدم الجدولة الرئيسية إعدادات التغطية لحساب متطلبات الصنف."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fb11a470d98a9742749daaac3244a5bb0d3a689c
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---

# <a name="coverage-settings"></a><span data-ttu-id="b397d-103">إعدادات التغطية</span><span class="sxs-lookup"><span data-stu-id="b397d-103">Coverage settings</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b397d-104">تستخدم الجدولة الرئيسية إعدادات التغطية لحساب متطلبات الصنف.</span><span class="sxs-lookup"><span data-stu-id="b397d-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="b397d-105">يمكنك تحديد إعدادات التغطية بعدة طرق:</span><span class="sxs-lookup"><span data-stu-id="b397d-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="b397d-106">حدد إعدادات التغطية لمجموعة تغطية.</span><span class="sxs-lookup"><span data-stu-id="b397d-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="b397d-107">يمكنك إنشاء مجموعة تغطية تحتوي على إعدادات لكل المنتجات المرتبطة بمجموعة التغطية.</span><span class="sxs-lookup"><span data-stu-id="b397d-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="b397d-108">انقر فوق **التخطيط الرئيسي &gt; إعداد &gt; تغطية &gt; مجموعات التغطية** لإنشاء مجموعة تغطية.</span><span class="sxs-lookup"><span data-stu-id="b397d-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="b397d-109">يمكن ربط مجموعة تغطية لأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="b397d-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="b397d-110">إذا كان الارتباط خاصًا بموقع أو مستودع أو بُعد منتج، فاستخدم حقل **مجموعة التغطية** في صفحة **تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="b397d-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="b397d-111">أما إذا كان الارتباط عامًا، بغض النظر عن أبعاد المنتج، فاستخدم **مجموعة التغطية** في علامة التبويب السريع **خطة** في صفحة **تفاصيل المنتج**.</span><span class="sxs-lookup"><span data-stu-id="b397d-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="b397d-112">وإذا لم تقم بربط مجموعة تغطية بمنتج، يستخدم التخطيط الرئيسي **مجموعة التغطية العامة** التي تم تعيينها في صفحة **معلمات التخطيط الرئيسي** حسب الإعدادات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="b397d-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="b397d-113">تحديد إعدادات التغطية لمنتج.</span><span class="sxs-lookup"><span data-stu-id="b397d-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="b397d-114">يمكنك إنشاء إعدادات التغطية لمنتج محدد.</span><span class="sxs-lookup"><span data-stu-id="b397d-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="b397d-115">انقر فوق **إدارة معلومات المنتج &gt; المنتجات &gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="b397d-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="b397d-116">حدد المنتج، في **جزء الإجراءات**، علامة التبويب **خطة**، في **مجموعة التغطية**، انقر فوق **تغطية الصنف** لفتح صفحة **تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="b397d-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="b397d-117">إذا تم ربط المنتج بمجموعة تغطية بالفعل، فيمكنك تجاوز إعدادات مجموعة التغطية باستخدام حقل **التجاوز**.</span><span class="sxs-lookup"><span data-stu-id="b397d-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="b397d-118">تأخذ إعدادات التغطية في صفحة **تغطية الصنف** الأسبقية على الإعدادات في صفحة **مجموعة التغطية**.</span><span class="sxs-lookup"><span data-stu-id="b397d-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="b397d-119">تحديد إعدادات التغطية لمنتج باستخدام معالج.</span><span class="sxs-lookup"><span data-stu-id="b397d-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="b397d-120">المعالج هو دليل خطوة بخطوة يساعدك لإعداد معلمات تغطية الصنف الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="b397d-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="b397d-121">في صفحة **تغطية الصنف**، انقر فوق **معالج** لفتح **معالج تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="b397d-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

-   <span data-ttu-id="b397d-122">تحديد إعدادات تغطية لمجموعة أبعاد.</span><span class="sxs-lookup"><span data-stu-id="b397d-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="b397d-123">انقر فوق **إدارة معلومات المنتج‬ &gt; عام &gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="b397d-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="b397d-124">وفي صفحة **إصدار تفاصيل المنتج **، في علامة التبويب **عام**، في مجموعة **الإدارة** ، انقر فوق رابط **مجموعة أبعاد التخزين**.</span><span class="sxs-lookup"><span data-stu-id="b397d-124">On the **Released product detail **page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="b397d-125">في صفحة **مجموعة أبعاد التخزين**، حدد حقل **خطة التغطية حسب البعد** لإنشاء إعدادات التغطية لبُعد في مجموعة أبعاد التخزين.</span><span class="sxs-lookup"><span data-stu-id="b397d-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="b397d-126">ويجب أن يتم في كافة أبعاد المنتج، مثل التكوين واللون والحجم والنمط تحديد حقل **خطة التغطية حسب البُعد**.</span><span class="sxs-lookup"><span data-stu-id="b397d-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="b397d-127">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="b397d-127">See also</span></span>
--------

[<span data-ttu-id="b397d-128">الخطط الرئيسية</span><span class="sxs-lookup"><span data-stu-id="b397d-128">Master plans</span></span>](master-plans.md)




