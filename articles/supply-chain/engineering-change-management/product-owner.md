---
title: ملاك المنتجات
description: يوفر هذا الموضوع معلومات حول مالكو المنتج. يعد مالك المنتج مجموعه من المستخدمين المسؤولين عن منتجات محدده. يمكن لأعضاء المجموعة فقط تحرير هذه المنتجات. يمكن استخدام مالك المنتج أيضا في سير عمل الاعتماد.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 679712b2397f220e263da3df07ecd03c99bebf3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842009"
---
# <a name="product-owners"></a><span data-ttu-id="a91a2-106">ملاك المنتجات</span><span class="sxs-lookup"><span data-stu-id="a91a2-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a91a2-107">يعد مالك المنتج مجموعه من المستخدمين المسؤولين عن منتجات محدده.</span><span class="sxs-lookup"><span data-stu-id="a91a2-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="a91a2-108">عند تعيين مجموعه مالكي المنتج لأحد المنتجات ، يمكن لأعضاء هذه المجموعة فقط تحرير المنتج.</span><span class="sxs-lookup"><span data-stu-id="a91a2-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="a91a2-109">يمكن استخدام مالك المنتج أيضا في سير عمل الاعتماد في إدارة التغييرات الهندسية.</span><span class="sxs-lookup"><span data-stu-id="a91a2-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="a91a2-110">يعتبر مالكو المنتجات إعدادات عمومية.</span><span class="sxs-lookup"><span data-stu-id="a91a2-110">Product owners are global settings.</span></span> <span data-ttu-id="a91a2-111">بالتالي ، تكون متوفرة لكافة الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="a91a2-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="a91a2-112">إنشاء مجموعه مالكي منتجات</span><span class="sxs-lookup"><span data-stu-id="a91a2-112">Create a product owner group</span></span>

<span data-ttu-id="a91a2-113">لإنشاء مجموعه مالكي منتجات وأضافه أعضاء اليها ، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a91a2-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="a91a2-114">انتقل إلى **إدارة التغييرات الهندسية \> الإعداد \> مالكو المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="a91a2-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="a91a2-115">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a91a2-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="a91a2-116">في الحقل **مالك المنتج**، أدخل اسمًا وصفيًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="a91a2-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="a91a2-117">في الحقل **الاسم**، أدخل وصفًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="a91a2-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="a91a2-118">علي علامة التبويب السريعة **الأعضاء**، أضف العاملين الذين يجب ان يكونوا أعضاء في المجموعة.</span><span class="sxs-lookup"><span data-stu-id="a91a2-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="a91a2-119">تعيين مالك للمنتج</span><span class="sxs-lookup"><span data-stu-id="a91a2-119">Assign a product owner to a product</span></span>

<span data-ttu-id="a91a2-120">لتعيين مالك منتج لحجز منتج، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a91a2-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="a91a2-121">افتح صفحه **تفاصيل المنتج** للمنتج الرئيسي أو المنتج ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="a91a2-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="a91a2-122">في علام التبويب السريعة **عام**، قم بتعيين حقل **مالك المنتج** إلى اسم مجموعه مالكي المنتج المناسبة.</span><span class="sxs-lookup"><span data-stu-id="a91a2-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="a91a2-123">اثناء تعيين مالك المنتج لأحد المنتجات ، يمكن لأعضاء مجموعه مالكي المنتج فقط تحرير اعداد **مالك المنتج**.</span><span class="sxs-lookup"><span data-stu-id="a91a2-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="a91a2-124">كما يظهر مالك المنتج في صفحه **المنتجات التي تم إصدارها**.</span><span class="sxs-lookup"><span data-stu-id="a91a2-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="a91a2-125">مالكو المنتج وإصدارات المنتج</span><span class="sxs-lookup"><span data-stu-id="a91a2-125">Product owners and product releases</span></span>

<span data-ttu-id="a91a2-126">يمكن فقط للمستخدمين من مجموعه مالكي المنتج الخاصة بالمنتج إصدار هذا المنتج.</span><span class="sxs-lookup"><span data-stu-id="a91a2-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="a91a2-127">ومع ذلك ، يوجد استثناء عندما يكون المنتج عبارة عن صنف تابع ، ويتم تحرير الأصل الخاص به بواسطة مالك الأصل.</span><span class="sxs-lookup"><span data-stu-id="a91a2-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="a91a2-128">بمعني آخر ، إذا كان المنتج جزءا من قائمة مكونات الصنف لمنتج آخر ، فلن يقوم النظام بفحص مالك المنتج لكل صنف في قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="a91a2-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="a91a2-129">وهو يقوم فقط بالتحقق من مالك المنتج الخاص بالصنف الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a91a2-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="a91a2-130">علي سبيل المثال، يتم تعيين المنتج X إلى مجموعه مالكي المنتجات *تصميم الخزانات*.</span><span class="sxs-lookup"><span data-stu-id="a91a2-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="a91a2-131">المنتج X أيضا جزءا من قائمة مكونات الصنف Y، والذي يتم تعيينه لمجموعه مالكي المنتجات *تصميم السماعات*.</span><span class="sxs-lookup"><span data-stu-id="a91a2-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="a91a2-132">إذا قام مستخدم من مجموعة مالكي المنتجات *تصميم السماعات* بإصدار المنتج Y وقائمة مكونات الصنف الخاصة به، سيتم إصدار المنتج X مع المنتج Y.</span><span class="sxs-lookup"><span data-stu-id="a91a2-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="a91a2-133">مالكو المنتج والموافقات</span><span class="sxs-lookup"><span data-stu-id="a91a2-133">Product owners and approvals</span></span>

<span data-ttu-id="a91a2-134">ونظرا لان مالكي المنتجات يعرفون ما إذا كانت التغييرات الهندسية الخاصة ستستفيد من منتجاتها ، فانه غالبا ما يكون من المنطقي تضمينها كجزء من عمليه الاعتماد في أداره التغييرات الهندسية.</span><span class="sxs-lookup"><span data-stu-id="a91a2-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="a91a2-135">يمكنك تنفيذ هذا الأسلوب من خلال اعداد مالكي المنتج كموفر مشارك في مهام سير العمل التي يتم استخدامها لأداره التغييرات الهندسية.</span><span class="sxs-lookup"><span data-stu-id="a91a2-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="a91a2-136">سيقوم النظام بعد ذلك بتعيين مهام الموافقة في سير العمل ، وذلك استنادا إلى المنتجات الموجودة في طلبات التغيير الهندسي وأوامر التغيير الهندسي.</span><span class="sxs-lookup"><span data-stu-id="a91a2-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="a91a2-137">لمزيد من المعلومات ، راجع [أداره تغييرات المنتجات الهندسية](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="a91a2-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]