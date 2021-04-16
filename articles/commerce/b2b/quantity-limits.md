---
title: تعيين حدود كمية المنتج لمواقع التجارة الإلكترونية بين الشركات B2B
description: يوضح هذا الموضوع كيفيه تعيين حدود كمية المنتج لمواقع التجارة الإلكترونية بين الشركات (B2B).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e9f14bc9aa6586e87f3e8ccb82e63d0ec2e46534
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799771"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="2117f-103">تعيين حدود كمية المنتج لمواقع التجارة الإلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="2117f-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2117f-104">يوضح هذا الموضوع كيفيه تعيين حدود كمية المنتج لمواقع التجارة الإلكترونية بين الشركات (B2B).</span><span class="sxs-lookup"><span data-stu-id="2117f-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="2117f-105">تحتوي معظم المنتجات على وحدى قياس تحدد التجميع الخاص بها.</span><span class="sxs-lookup"><span data-stu-id="2117f-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="2117f-106">ويؤثر التجميع على كيفية بيع المنتجات.</span><span class="sxs-lookup"><span data-stu-id="2117f-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="2117f-107">قد يكون لبعض المنتجات تجميع إضافي للكميات.</span><span class="sxs-lookup"><span data-stu-id="2117f-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="2117f-108">يحدد هذا التجميع ما إذا كان من الممكن بيع المنتجات كوحدات فردية أو كمضاعفات، وما إذا كان هناك حد أدنى أو أقصى لكمية الأمر الذي يجب اتباعه.</span><span class="sxs-lookup"><span data-stu-id="2117f-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="2117f-109">وتضمن ميزة تحديد الكمية تطبيق الحد الأدنى والأقصى للكمية وتطبيق الكميات المتعددة والقياسية التي تم تكوينها في Microsoft Dynamics 365 Commerce (في إعدادات الأمر الافتراضية أو إعدادات موقع المنشئ لموقع Commerce) على أوامر العميل التي تم وضعها في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2117f-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="2117f-110">وحدود كمية المنتجات غير معتمدة حاليا بالنسبة لنقطة البيع (POS) ومراكز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="2117f-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="2117f-111">يوفر معظم بائعي التجزئي خيارًا لأوامر العميل (المعروفة أيضًا بالأوامر الخاصة)، للوفاء بالمنتجات المختلفة وتلبية المتطلبات.</span><span class="sxs-lookup"><span data-stu-id="2117f-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="2117f-112">وفيما يلي بعض السيناريوهات النموذجية:</span><span class="sxs-lookup"><span data-stu-id="2117f-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="2117f-113">يرغب العميل في أن يتم بيع منتجات بمتغيرات معينة بمضاعفات قليلة.</span><span class="sxs-lookup"><span data-stu-id="2117f-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="2117f-114">يرغب أحد العملاء في انتقاء المنتجات من متجر أو من موقع يختلف عن المتجر أو الموقع الذي اشتري منه العميل تلك المنتجات.</span><span class="sxs-lookup"><span data-stu-id="2117f-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="2117f-115">ومع ذلك، تختلف معايير التعبئة الخاصة بالمتاجر عن معايير التعبئة لتوزيع المبيعات على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="2117f-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="2117f-116">يرغب العميل في شراء منتج محدود الإصدار بحد أقصي لكمية الأصناف التي يمكن شراؤها.</span><span class="sxs-lookup"><span data-stu-id="2117f-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="2117f-117">تشغيل ميزة إعدادات الأمر الافتراضية في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="2117f-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="2117f-118">قبل أن تتمكن من إعداد حدود كمية المنتجات، يجب تشغيل ميزة إعدادات الأمر الافتراضية في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="2117f-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="2117f-119">لتشغيل ميزة إعدادات الأوامر الافتراضية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2117f-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="2117f-120">انتقل إلى **إدارة النظام \> مساحات العمل \> إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="2117f-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="2117f-121">ابحث عن وحدد ميزة **إعدادات الأمر الخاصة بالموقع والافتراضية في أمر العميل**.</span><span class="sxs-lookup"><span data-stu-id="2117f-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="2117f-122">في أسفل الجزء الأيمن، حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="2117f-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="2117f-123">تحديد إعدادات الكمية</span><span class="sxs-lookup"><span data-stu-id="2117f-123">Define quantity settings</span></span> 

<span data-ttu-id="2117f-124">يمكنك تحديد إعدادات الكمية في صفحة **إعدادات الأمر الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="2117f-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="2117f-125">لتحديد إعدادات الكمية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2117f-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="2117f-126">انتقل إلى **البيع بالتجزئة والتجارة \> المنتجات والفئات \> المنتجات الصادرة حسب الفئة**.</span><span class="sxs-lookup"><span data-stu-id="2117f-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="2117f-127">حدد المنتج الصادر.</span><span class="sxs-lookup"><span data-stu-id="2117f-127">Select a released product.</span></span>
1. <span data-ttu-id="2117f-128">في جزء الإجراءات، من علامة التبويب **إدارة المخزون**، في مجموعة **إعدادات الأوامر**، حدد **إعدادات الأمر الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="2117f-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="2117f-129">في صفحة **إعدادات الأمر الافتراضية**، في علامة التبويب السريعة **أمر التوريد**، في قسم **كمية المبيعات**، قم بتعيين كميات مبيعات المنتج:</span><span class="sxs-lookup"><span data-stu-id="2117f-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="2117f-130">**متعددة** - الكمية التي يمكن شراء المنتج بها بمضاعفات.</span><span class="sxs-lookup"><span data-stu-id="2117f-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="2117f-131">**الحد الأدنى لكمية الأمر** – الحد الأدنى لعدد المنتجات التي يجب شراؤها.</span><span class="sxs-lookup"><span data-stu-id="2117f-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="2117f-132">**الحد الأقصى لكمية الأمر** – الحد الأقصى لعدد المنتجات التي يمكن شراؤها.</span><span class="sxs-lookup"><span data-stu-id="2117f-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="2117f-133">**كمية الأمر القياسية** – الكمية الافتراضية التي يتم إدخالها تلقائيا عند تحديد المنتج.</span><span class="sxs-lookup"><span data-stu-id="2117f-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="2117f-134">تشغيل ميزة حدود كمية أمر B2B في منشئ موقع Commerce</span><span class="sxs-lookup"><span data-stu-id="2117f-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="2117f-135">لتشغيل ميزة حدود كمية أمر B2B في منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2117f-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2117f-136">انتقل إلى **إعدادات الموقع \> الملحقات**</span><span class="sxs-lookup"><span data-stu-id="2117f-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="2117f-137">تحت **تمكين حدود كمية الأمر**، حدد **ممكن لعملاء B2B** في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="2117f-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="2117f-138">تصبح إعدادات منشئ الموقع المحدثة سارية المفعول فقط بعد تحديد ملف app.settings.json.</span><span class="sxs-lookup"><span data-stu-id="2117f-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="2117f-139">لمزيد من المعلومات ، راجع [تحديثات مكتبة SDK والوحدات النمطية](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="2117f-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2117f-140">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2117f-140">Additional resources</span></span>

[<span data-ttu-id="2117f-141">إعداد موقع تجارة إلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="2117f-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="2117f-142">إنشاء تدرجات هرمية لتصميم المؤسسة لمؤسسات B2B</span><span class="sxs-lookup"><span data-stu-id="2117f-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="2117f-143">إدارة مستخدمي شركاء الأعمال على مواقع التجارة الإلكترونية بين الشركات</span><span class="sxs-lookup"><span data-stu-id="2117f-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="2117f-144">تكوين طريقة دفع حساب العميل لمواقع التجارة الإلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="2117f-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]