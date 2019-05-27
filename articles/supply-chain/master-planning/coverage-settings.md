---
title: إعدادات التغطية
description: يوفر هذا الموضوع معلومات حول إعدادات التغطية التي تستخدمها الجدولة الرئيسية لحساب متطلبات الصنف.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538884"
---
# <a name="coverage-settings"></a><span data-ttu-id="1dcf5-103">إعدادات التغطية</span><span class="sxs-lookup"><span data-stu-id="1dcf5-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1dcf5-104">تستخدم الجدولة الرئيسية إعدادات التغطية لحساب متطلبات الصنف.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="1dcf5-105">يمكنك تحديد إعدادات التغطية بعدة طرق:</span><span class="sxs-lookup"><span data-stu-id="1dcf5-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="1dcf5-106">حدد إعدادات التغطية لمجموعة تغطية.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="1dcf5-107">يمكنك إنشاء مجموعة تغطية تحتوي على إعدادات لكل المنتجات المرتبطة بمجموعة التغطية.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="1dcf5-108">لإنشاء مجموعة تغطية، انتقل إلى **التخطيط الرئيسي &gt; الإعداد &gt; التغطية &gt; مجموعات التغطية**.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="1dcf5-109">يمكن ربط مجموعة تغطية لأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="1dcf5-110">إذا كان الارتباط خاصًا بموقع أو مستودع أو بُعد منتج، فاستخدم حقل **مجموعة التغطية** في صفحة **تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="1dcf5-111">إذا كان الارتباط عامًا، وبغض النظر عن أبعاد المنتج، فاستخدم حقل **مجموعة التغطية** في علامة التبويب السريعة **خطة** في صفحة **تفاصيل المنتج**.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="1dcf5-112">بشكل افتراضي، إذا لم تربط مجموعة تغطية بمنتج، يستخدم التخطيط الرئيسي مجموعة التغطية العامة المحددة في صفحة **معلمات التخطيط الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="1dcf5-113">تحديد إعدادات التغطية لمنتج.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="1dcf5-114">يمكنك إنشاء إعدادات التغطية لمنتج محدد.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="1dcf5-115">انتقل إلى **إدارة معلومات المنتج‬ &gt; المنتجات &gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="1dcf5-116">حدد المنتج، ثم في جزء الإجراءات، علامة التبويب **خطة**، في مجموعة **التغطية‏‎**، حدد **تغطية الصنف** لفتح صفحة **تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="1dcf5-117">إذا تم ربط المنتج بمجموعة تغطية بالفعل، فيمكنك تجاوز إعدادات مجموعة التغطية باستخدام حقل **التجاوز**.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="1dcf5-118">تأخذ إعدادات التغطية في صفحة **تغطية الصنف** الأسبقية على الإعدادات في صفحة **مجموعة التغطية**.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="1dcf5-119">تحديد إعدادات التغطية لمنتج باستخدام معالج.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="1dcf5-120">يقوم المعالج بإرشادك خطوة بخطوة خلال عملية إعداد معلمات تغطية الصنف الرئيسية.‬</span><span class="sxs-lookup"><span data-stu-id="1dcf5-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="1dcf5-121">في صفحة **تغطية الصنف**، على جزء الإجراءات، حدد **معالج** لفتح **معالج تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="1dcf5-122">تحديد إعدادات تغطية لمجموعة أبعاد.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="1dcf5-123">انتقل إلى **إدارة معلومات المنتج‬ &gt; المنتجات &gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="1dcf5-124">في صفحة **تفاصيل المنتجات الصادرة‬**، في علامة التبويب السريعة **عام**، في القسم **الإدارة**، حدد الارتباط في الحقل **مجموعة أبعاد التخزين**.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="1dcf5-125">في صفحة **مجموعات أبعاد التخزين**، حدد خانة الاختيار **خطة التغطية حسب البعد** لإنشاء إعدادات التغطية لبُعد في مجموعة أبعاد التخزين.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="1dcf5-126">يجب تحديد الحقل **خطة التغطية حسب البُعد** لجميع أبعاد المنتج، مثل التكوين واللون والحجم والنمط.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1dcf5-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1dcf5-127">Additional resources</span></span>

[<span data-ttu-id="1dcf5-128">الخطط الرئيسية</span><span class="sxs-lookup"><span data-stu-id="1dcf5-128">Master plans</span></span>](master-plans.md)
