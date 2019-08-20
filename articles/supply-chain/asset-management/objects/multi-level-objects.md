---
title: الأصول متعددة المستويات
description: يشرح هذا الموضوع كيفية إنشاء أصول متعددة المستويات وحذفها.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f38253317ed8f06318fc501511ca5263a614e20
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783037"
---
# <a name="multi-level-assets"></a><span data-ttu-id="5b0ae-103">الأصول متعددة المستويات</span><span class="sxs-lookup"><span data-stu-id="5b0ae-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5b0ae-104">يشرح هذا الموضوع كيفية إنشاء أصول متعددة المستويات وحذفها.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="5b0ae-105">يمكنك إنشاء الأصول والأصول الفرعية ذات الصلة في بنية شجرة هرمية.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="5b0ae-106">وبهذه الطريقة، يمكنك إظهار العلاقات والتبعيات بين الأصول.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="5b0ae-107">بإمكان مهام الصيانة أن تكون ذات صلة بجميع مستويات بنية الشجرة.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="5b0ae-108">ويمكن أيضًا إنشاء الإحصاءات على مستوى فردي أو كمجموع لجميع مستويات الأصول الفرعية.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="5b0ae-109">في صفحة قائمة **كل الأصول‬** (**إدارة الأصول‬** \> **عام** \> **الأصول‬** \> **كل الأصول‬**)، يسرد عمود **الأصل** الأصول‬ بترتيب هرمي.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="5b0ae-110">يعرض عمود **الأصل الأساسي** الأصل الأساسي ذا الصلة.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="5b0ae-111">بالإضافة إلى ذلك، إذا تم إنشاء أصول وأصول فرعية، فسيعرض قسم **شجرة الأصول** في جزء **المعلومات‏‎ ذات الصلة** الأصول في بنية شجرة.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="5b0ae-112">لمزيد من المعلومات حول كيفية إنشاء أصل، راجع [إنشاء أصل](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="5b0ae-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="5b0ae-113">لإنشاء أصل فرعي، حدد الأصل الأساسي في حقل **الأصل الأساسي** على علامة التبويب السريعة **عام**.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="5b0ae-114">نسخ أصل أو بنية أصل</span><span class="sxs-lookup"><span data-stu-id="5b0ae-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="5b0ae-115">عند وجود بنى أصول متعددة في شركتك، يمكنك استخدام دالة النسخ في إدارة الأصول لإنشائها بسرعة.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="5b0ae-116">حدد **إدارة الأصول** \> **عام** \> **الأصول** \> **كل الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="5b0ae-117">في صفحة قائمة **كل الأصول**، حدد الأصل المراد نسخه.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="5b0ae-118">على سبيل المثال، إذا كنت ترغب في نسخ بنية الأصل بالكامل، بما في ذلك الأصول الفرعية، فحدد أصلاً أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="5b0ae-119">حدد **نسخ الأصل**.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-119">Select **Copy asset**.</span></span> <span data-ttu-id="5b0ae-120">في القسم **نسخ من**، يتم تعيين حقل **الأصل** إلى الأصل الذي قمت بتحديده في صفحة القائمة.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="5b0ae-121">في القسم **نسخ إلى**، في حقل **الأصل**، أدخل اسم الأصل الجديد.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="5b0ae-122">إذا كان من المفترض أن يكون الأصل الذي تقوم بإنشائه جزءًا من بنية أصل موجودة، في قسم **الأصل الأساسي**، في حقل **الأصل**، حدد معرف الأصل الأساسي.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="5b0ae-123">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-123">Select **OK**.</span></span> <span data-ttu-id="5b0ae-124">تظهر بنية الأصل الجديدة في صفحة قائمة **كل الأصول**.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="5b0ae-125">تُنقل إلى الأصل الجديد أو بنية الأصل الجديدة جميع سمات الأصل وخطط الصيانة ودورات الصيانة المرتبطة بالأصل الذي قمت بنسخه.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="5b0ae-126">عند نسخ بنية أصل، تحمل الأصول الفرعية في البنية الجديدة نفس اسم الأصول الفرعية التي قمت بنسخها.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="5b0ae-127">بعد اكتمال إجراء النسخ، يمكنك بسهولة تغيير اسم الأصل وإعداداته الأخرى.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="5b0ae-128">حدد الأصل في صفحة‏‎ قائمة **كل الأصول**، ثم حدد الزر **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="5b0ae-129">عند نسخ أصل أو بنية أصل، يُعاد تعيين حالة دورة حياة الأصل الجديدة إلى أي حالة قمت بتعريفها كحالة دورة حياة أولية للأصل.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="5b0ae-130">يُعاد تعيين موقع العمل إلى موقع العمل الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="5b0ae-131">حذف أصل أو بنية أصل</span><span class="sxs-lookup"><span data-stu-id="5b0ae-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="5b0ae-132">إذا تكوّن أحد الأصول من أصول فرعية ذات صلة، فلا يمكنك حذفه إلا إذا لم يتم تسجيل أي طلبات صيانة أو وظائف أمر عمل أو تسجيلات خطأ أو تقييمات حالة على أي من الأصول.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="5b0ae-133">في صفحة قائمة **كل الأصول**، حدد الأصل المراد حذفه.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="5b0ae-134">حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="5b0ae-135">إذا لم تتمكن من حذف أصل باستخدام هذا الإجراء، فهناك طريقة أخرى لمعالجة عملية الحذف وهي إعداد حالة دورة حياة أصل لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="5b0ae-136">على سبيل المثال، يمكنك إعداد حالة دورة الحياة **خردة** أو **محذوف** في صفحة قائمة **حالات دورة حياة الأصل**.</span><span class="sxs-lookup"><span data-stu-id="5b0ae-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
