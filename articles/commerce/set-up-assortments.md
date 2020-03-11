---
title: إعداد عمليات الفرز
description: توضح هذه المقالة ماهية عملية الفرز وتشرح كيفية إعداد عمليات الفرز في Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 26614d319453041177e8072793f09f52ebfd51fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021501"
---
# <a name="set-up-assortments"></a><span data-ttu-id="52e59-103">إعداد عمليات الفرز</span><span class="sxs-lookup"><span data-stu-id="52e59-103">Set up assortments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="52e59-104">توضح هذه المقالة ماهية عملية الفرز وتشرح كيفية إعداد عمليات الفرز في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="52e59-104">This article describes what an assortment is and explains how to set up assortments in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="52e59-105">عملية الفرز عبارة مجموعة من المنتجات ذات الصلة التي تقوم بتعيينها لقناة التجارة، مثل متجر تقليدي أو متجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="52e59-105">An assortment is a collection of related products that you assign to a commerce channel, such as a brick-and-mortar store or an online store.</span></span> <span data-ttu-id="52e59-106">وتستخدم عمليات الفرز لتحديد المنتجات التي تتوفر في كل متجر.</span><span class="sxs-lookup"><span data-stu-id="52e59-106">You use assortments to identify the products that are available in each store.</span></span> <span data-ttu-id="52e59-107">يمكن أن يتضمن الفرز فئات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="52e59-107">An assortment can include categories of products.</span></span> <span data-ttu-id="52e59-108">ولذلك، يتم تضمين كافة المنتجات التي تم تعيينها إلى فئة محددة في عملية الفرز.</span><span class="sxs-lookup"><span data-stu-id="52e59-108">Therefore, all products that are assigned to a specific category are included in the assortment.</span></span> <span data-ttu-id="52e59-109">كما يمكن أن تتضمن عملية فرز منتجات محددة ومتغيرات معينة من المنتجات.</span><span class="sxs-lookup"><span data-stu-id="52e59-109">An assortment can also include specific products and specific variants of products.</span></span> <span data-ttu-id="52e59-110">ومن خلال إعداد عملية فرز، يمكنك تعيين آلاف المنتجات للقنوات الخاصة بك في نفس الوقت، في أي مجموعة تتطلبها المتاجر الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="52e59-110">By setting up an assortment, you can assign thousands of products to your channels at that same time, in any combination that your stores require.</span></span> <span data-ttu-id="52e59-111">يمكنك إعداد العديد من عمليات فرز المنتجات كما تريد.</span><span class="sxs-lookup"><span data-stu-id="52e59-111">You can set up as many product assortments as you require.</span></span> <span data-ttu-id="52e59-112">ويمكن تضمين كل منتج في عملية فرز واحدة أو أكثر، ويمكن تعيين كل عملية فرز لقناة واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="52e59-112">Each product can be included in one or more assortments, and each assortment can be assigned to one or more channels.</span></span> <span data-ttu-id="52e59-113">على سبيل المثال، يمكنك تحديد عملية فرز واحدة تحتوي على مجموعة أساسية من المنتجات.</span><span class="sxs-lookup"><span data-stu-id="52e59-113">For example, you define one assortment that includes a base set of products.</span></span> <span data-ttu-id="52e59-114">وتتلقى كافة المتاجر عملية الفرز هذه.</span><span class="sxs-lookup"><span data-stu-id="52e59-114">All stores receive this assortment.</span></span> <span data-ttu-id="52e59-115">وتقوم فيما بعد بتحديد عملية فرز أخرى تتضمن المعدات الرياضية الكبيرة فقط.</span><span class="sxs-lookup"><span data-stu-id="52e59-115">You then define another assortment that includes only large sporting equipment.</span></span> <span data-ttu-id="52e59-116">تتلقى المتاجر الكبيرة فقط عملية الفرز هذه.</span><span class="sxs-lookup"><span data-stu-id="52e59-116">Only your larger stores receive this assortment.</span></span> <span data-ttu-id="52e59-117">يوضح الرسم التخطيطي التالي كيفية تعيين المنتجات لعمليات الفرز، وكيف يمكن تعيين عمليات الفرز هذه إلى القنوات.</span><span class="sxs-lookup"><span data-stu-id="52e59-117">The following diagram shows how products can be assigned to assortments, and how those assortments can be assigned to channels.</span></span>

![علاقات عمليات فرز المنتجات](./media/assortments_relationship.gif)

## <a name="prerequisites"></a><span data-ttu-id="52e59-119">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="52e59-119">Prerequisites</span></span>

<span data-ttu-id="52e59-120">قبل أن يمكنك إعداد عملية فرز وتعيينها إلى قناة تجارة، يجب عليك إتمام المهام التالية.</span><span class="sxs-lookup"><span data-stu-id="52e59-120">Before you can set up an assortment and assign it to a commerce channel, you must complete the following tasks.</span></span>

| <span data-ttu-id="52e59-121">المهمة</span><span class="sxs-lookup"><span data-stu-id="52e59-121">Task</span></span>                              | <span data-ttu-id="52e59-122">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="52e59-122">Description</span></span> |
|-----------------------------------|-------------|
| <span data-ttu-id="52e59-123">يمكنك إعداد قناة.</span><span class="sxs-lookup"><span data-stu-id="52e59-123">Set up a channel.</span></span>          | <span data-ttu-id="52e59-124">تمثل القنوات متجر حركات ورقية أو متجر على الإنترنت أو سوق على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="52e59-124">Channels represent a brick-and-mortar store, an online store, or an online marketplace.</span></span> <span data-ttu-id="52e59-125">ويجب عليك إعداد قناة واحدة على الأقل وتكوين الخيارات للمتجر.</span><span class="sxs-lookup"><span data-stu-id="52e59-125">You must set up at least one channel and configure the options for the store.</span></span> <span data-ttu-id="52e59-126">ويتم تعيين عمليات الفرز إلى متاجر لتحديد المنتجات التي يشتمل عليها متجر معين.</span><span class="sxs-lookup"><span data-stu-id="52e59-126">Assortments are assigned to stores to identify the products that a particular store carries.</span></span> |
| <span data-ttu-id="52e59-127">إنشاء تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="52e59-127">Create an organization hierarchy.</span></span> | <span data-ttu-id="52e59-128">بعد إعداد قنوات التجارة للمؤسسة الخاصة بك، يجب عليك تكوين التدرج الهرمي لمؤسسة التجارة الذي يمثل الهيكل التنظيمي لقنوات التجارة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="52e59-128">After you set up the commerce channels for your organization, you must configure an organization hierarchy that represents the organizational structure of your channels.</span></span> <span data-ttu-id="52e59-129">ويمكن استخدام التدرج الهرمي للمؤسسات لعمليات الفرز، والتزويد، وإنشاء التقارير.</span><span class="sxs-lookup"><span data-stu-id="52e59-129">An organization hierarchy can be used for assortments, replenishment, and reporting.</span></span> <span data-ttu-id="52e59-130">وعن طريق إضافة القنوات الخاصة بك إلى تدرج هرمي للمؤسسات، يمكنك تعيين عمليات الفرز لمجموعات من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="52e59-130">By adding your channels to an organization hierarchy, you can assign assortments to groups of stores.</span></span> <span data-ttu-id="52e59-131">وبدلاً من تعيين عملية الفرز لكل متجر على حدة، يمكنك تعيين عملية الفرز إلى عقده المؤسسة رفيعة المستوى.</span><span class="sxs-lookup"><span data-stu-id="52e59-131">Instead of assigning the assortment individually to each store, you assign the assortment to the high-level organization node.</span></span> <span data-ttu-id="52e59-132">فكلما تمت إضافة قناة جديدة إلى عقده مؤسسة رفيعة المستوى، ترث القناة تلقائياً أي عمليات الفرز تم تعيينها إلى عقده مؤسسة ذات مستوى أعلى.</span><span class="sxs-lookup"><span data-stu-id="52e59-132">Then, whenever a new channel is added to the high-level organization node, that channel automatically inherits any assortments that were assigned to the higher-level organization node.</span></span> <span data-ttu-id="52e59-133">ويمكنك تعيين عمليات الفرز فقط إلى قنوات البيع بالتجزئة التي تم تضمينها في تدرج هرمي للمؤسسات تم تعيينه لغرض **فرز التجارة**.</span><span class="sxs-lookup"><span data-stu-id="52e59-133">You can assign assortments only to channels that are included in an organization hierarchy that is assigned the **Commerce assortment** purpose.</span></span> |
| <span data-ttu-id="52e59-134">تحديد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="52e59-134">Define products.</span></span>                  | <span data-ttu-id="52e59-135">قبل أن تتمكن من إضافة منتجات إلى عملية فرز، يجب إضافتها في Commerce.</span><span class="sxs-lookup"><span data-stu-id="52e59-135">Before you can add products to an assortment, you must add them in Commerce.</span></span> <span data-ttu-id="52e59-136">ويمكنك إضافة منتجات يدوياً، أو يمكنك استيرادها من أحد الموردين.</span><span class="sxs-lookup"><span data-stu-id="52e59-136">You can add products manually, or you can import them from a vendor.</span></span> <span data-ttu-id="52e59-137">وبعد إضافة المنتجات، يجب عليك إصدارها إلى كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="52e59-137">After you add the products, you must release them to a legal entity.</span></span> <span data-ttu-id="52e59-138">ويمكن توفير فقط المنتجات التي تم اعتمادها إلى كيان قانوني للقنوات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="52e59-138">Only products that have been released to a legal entity can be made available to your channels.</span></span> <span data-ttu-id="52e59-139">ويمكن إضافة المنتجات التي لم يتم إصدارها بعد إلى كيان قانوني إلى عملية فرز، ويمكن اعتماد عملية الفرز.</span><span class="sxs-lookup"><span data-stu-id="52e59-139">Products that haven't yet been released to a legal entity can be added to an assortment, and the assortment can be approved.</span></span> <span data-ttu-id="52e59-140">ومع ذلك، حتى يتم إصدار المنتجات إلى كيان قانوني، لا يمكن توفيرها إلى القنوات.</span><span class="sxs-lookup"><span data-stu-id="52e59-140">However, until the products have been released to a legal entity, they can't be made available to the channels.</span></span> |
| <span data-ttu-id="52e59-141">إعداد تدرج هرمي للفئات.</span><span class="sxs-lookup"><span data-stu-id="52e59-141">Set up a category hierarchy.</span></span>      | <span data-ttu-id="52e59-142">عندما تقوم بإنشاء منتجات التجارة الخاصة بك، يمكنك تجميعها ووضعها في فئات باستخدام ميزة التدرج الهرمي للفئات.</span><span class="sxs-lookup"><span data-stu-id="52e59-142">When you create your commerce products, you can group and categorize them by using the category hierarchy feature.</span></span> <span data-ttu-id="52e59-143">ويمكنك إنشاء تدرج هرمي رئيسي واحد لتجميع وتصنيف كافة المنتجات التي تقوم بتوزيعها عن طريق القنوات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="52e59-143">You can create one core hierarchy to group and categorize all products that you distribute through your channels.</span></span> <span data-ttu-id="52e59-144">ويمكنك أيضًا إنشاء التدرجات الهرمية للفئات المنفصلة والتكميلية لتجميع أو تصنيف المنتجات لأغراض خاصة، مثل الترقيات أو عمليات الفرز.</span><span class="sxs-lookup"><span data-stu-id="52e59-144">You can also create separate, supplemental category hierarchies to group or categorize your products for special purposes, such as promotions or assortments.</span></span> <span data-ttu-id="52e59-145">ومن خلال استخدام التدرجات الهرمية للفئات، يمكنك تعيين كافة المنتجات في فئة معينة لعملية فرز.</span><span class="sxs-lookup"><span data-stu-id="52e59-145">By using category hierarchies, you can assign all the products in a specific category to an assortment.</span></span> <span data-ttu-id="52e59-146">ويتم تضمين أي منتجات تمت إضافتها إلى الفئة التي يتم تضمينها في عملية الفرز تلقائياً في عملية الفرز.</span><span class="sxs-lookup"><span data-stu-id="52e59-146">Any products that are added to the category that is included in the assortment are automatically included in the assortment.</span></span> <span data-ttu-id="52e59-147">وبعد ذلك، في المرة التالية التي يتم فيها تشغيل جدولة فرز التجارة، تتوفر هذه المنتجات لقنوات التجارة التي تم تعيين عملية الفرز لها.</span><span class="sxs-lookup"><span data-stu-id="52e59-147">Then, the next time that the commerce assortment scheduler is run, these products become available to the channels that the assortment is assigned to.</span></span> |

## <a name="setting-up-an-assortment"></a><span data-ttu-id="52e59-148">إعداد عملية فرز</span><span class="sxs-lookup"><span data-stu-id="52e59-148">Setting up an assortment</span></span>

<span data-ttu-id="52e59-149">بعد إكمال المتطلبات المسبقة، يمكنك إنشاء عملية فرز وتعيينها إلى القنوات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="52e59-149">After you complete the prerequisites, you can create an assortment and assign it to your channels.</span></span> <span data-ttu-id="52e59-150">ولإعداد عملية فرز، يجب عليك إكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="52e59-150">To set up an assortment, you must complete the following tasks.</span></span>

1. <span data-ttu-id="52e59-151">إنشاء عملية فرز جديدة أو نسخ عملية فرز موجودة</span><span class="sxs-lookup"><span data-stu-id="52e59-151">Create a new assortment, or copy an existing assortment.</span></span>
2. <span data-ttu-id="52e59-152">تحديد القنوات أو المجموعات رفيعة المستوى من القنوات التي تنطبق عليها عملية الفرز.</span><span class="sxs-lookup"><span data-stu-id="52e59-152">Select the channels or the high-level groups of channels that the assortment applies to.</span></span>
3. <span data-ttu-id="52e59-153">إضافة فئات المنتج أو المنتجات الفردية أو متغيرات المنتج إلى عملية الفرز.</span><span class="sxs-lookup"><span data-stu-id="52e59-153">Add product categories, individual products, or product variants to the assortment.</span></span> <span data-ttu-id="52e59-154">يمكنك تضمين كافة المنتجات في فئة محددة، أو يمكنك استبعاد منتجات مختارة من فئة يتم تضمينها في عملية الفرز.</span><span class="sxs-lookup"><span data-stu-id="52e59-154">You can include all products in a specific category, or you can exclude selected products from a category that is included in the assortment.</span></span>
4. <span data-ttu-id="52e59-155">نشر الفرز.</span><span class="sxs-lookup"><span data-stu-id="52e59-155">Publish the assortment.</span></span> <span data-ttu-id="52e59-156">عندما تقوم بنشر عملية فرز، يتم تشغيل مجدول عمليات فرز تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="52e59-156">When you publish an assortment, the assortment scheduler is automatically run.</span></span> <span data-ttu-id="52e59-157">وتُنشئ هذه العملية قائمة المنتجات.</span><span class="sxs-lookup"><span data-stu-id="52e59-157">This process generates the list of products.</span></span> <span data-ttu-id="52e59-158">وعند اكتمال هذه العملية، تتوفر المنتجات لقنوات التي تم تعيين عملية فرز المنتجات لها.</span><span class="sxs-lookup"><span data-stu-id="52e59-158">When this process is completed, the products become available to the channels that the product assortment is assigned to.</span></span> <span data-ttu-id="52e59-159">وإذا تم إجراء تغييرات على عملية فرز تم نشرها أو قنوات التي تم تعيين عملية الفرز لها، يجب تحديث عملية الفرز.</span><span class="sxs-lookup"><span data-stu-id="52e59-159">If changes are made to an assortment that has been published, or to the channels that the assortment is assigned to, the assortment must be updated.</span></span> <span data-ttu-id="52e59-160">ولتحديث عمية الفرز عند إجراء التغييرات، يمكنك تشغيل مجدول فرز كوظيفة دُفعية.</span><span class="sxs-lookup"><span data-stu-id="52e59-160">To update the assortment when changes are made, you can run the assortment scheduler as a batch job.</span></span>