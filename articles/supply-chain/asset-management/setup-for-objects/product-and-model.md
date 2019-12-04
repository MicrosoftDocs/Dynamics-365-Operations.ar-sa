---
title: الشركات المصنعة للأصول ونماذج الأصول
description: يشرح هذا الموضوع كيفية إعداد الشركات المصنعة للأصول والنماذج ذات الصلة في "إدارة الأصول".
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
ms.openlocfilehash: b77605070387871335c480e25cbe23af1155d6e8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812158"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="71529-103">الشركات المصنعة للأصول ونماذج الأصول</span><span class="sxs-lookup"><span data-stu-id="71529-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="71529-104">يشرح هذا الموضوع كيفية إعداد الشركات المصنعة للأصول والنماذج ذات الصلة في "إدارة الأصول".</span><span class="sxs-lookup"><span data-stu-id="71529-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="71529-105">قد ترتبط النماذج بأنواع الأصول.</span><span class="sxs-lookup"><span data-stu-id="71529-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="71529-106">إعداد علاقات المنتجات والنماذج</span><span class="sxs-lookup"><span data-stu-id="71529-106">Set up product-model relations</span></span>

1. <span data-ttu-id="71529-107">حدد **إدارة الأصول** \> **الإعداد** \> **الأصول‏‎** \> **الشركة المصنعة والنموذج‬**.</span><span class="sxs-lookup"><span data-stu-id="71529-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="71529-108">حدد **جديد** لإنشاء منتج جديد.</span><span class="sxs-lookup"><span data-stu-id="71529-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="71529-109">في الحقل **الشركة المصنعة**، أدخل اسمًا للشركة المصنعة للأصل.</span><span class="sxs-lookup"><span data-stu-id="71529-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="71529-110">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="71529-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="71529-111">على علامة التبويب السريعة **النماذج،** حدد **إضافة** لإنشاء نموذج أصل يجب أن يكون مرتبطًا بالشركة المصنعة للأصل.</span><span class="sxs-lookup"><span data-stu-id="71529-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="71529-112">في الحقل **النموذج**، أدخل اسمًا لنموذج الأصل.</span><span class="sxs-lookup"><span data-stu-id="71529-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="71529-113">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="71529-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="71529-114">في الحقل **نوع الأصل**، حدد نوع الأصل الذي يجب أن يرتبط به نموذج الشركة المصنعة.</span><span class="sxs-lookup"><span data-stu-id="71529-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="71529-115">يمكنك أيضًا إعداد علاقات لأنواع الأصول والشركات المصنعة والنماذج في بحث **أنواع الأصول**.</span><span class="sxs-lookup"><span data-stu-id="71529-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="71529-116">لمزيد من المعلومات، راجع [أنواع الأصول](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="71529-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="71529-117">على علامة التبويب السريعة **التفاصيل** يعرض حقل **النماذج** عدد نماذج الأصول التي تم إعدادها على الشركة المصنعة للأصول المحددة.</span><span class="sxs-lookup"><span data-stu-id="71529-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="71529-118">يعرض حقل **الأصول** عدد الأصول التي تستخدم الشركة المصنعة المحددة.</span><span class="sxs-lookup"><span data-stu-id="71529-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="71529-119">يعرض حقل **الأصول** عدد الكائنات التي تستخدم نموذج الشركة المصنعة.</span><span class="sxs-lookup"><span data-stu-id="71529-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="71529-120">قد لا يكون لنوع الأصل أي علاقات بين نماذج الشركة المصنعة للأصول، أو يمكنه أن يكون مرتبطًا بنموذج واحد للشركة المصنعة للأصول، أو يمكنه أن يكون مرتبطًا بنماذج متعددة للشركة المصنعة للأصول.</span><span class="sxs-lookup"><span data-stu-id="71529-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="71529-121">إذا كان نوع الأصل مرتبطًا بنموذج شركة مصنعة واحد على الأقل، فيمكن تحديد فقط المجموعات التي تم إعدادها في بحث **نموذج الشركة المصنعة** على صفحات "إدارة الأصول" حيث يمكن إعداد مجموعة من نوع الأصل والشركة المصنعة والنموذج.</span><span class="sxs-lookup"><span data-stu-id="71529-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="71529-122">تتضمن هذه الصفحات **كل الأصول** و**مستويات خدمة الأصول‬** و**الإعدادات الافتراضية لنوع الوظيف** و**بنود موازنة الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="71529-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="71529-123">إذا كانت بعض أنواع الأصول غير مرتبطة بأي نموذج من نماذج الشركة المصنعة، فلن تظهر على الصفحات سوى أنواع الأصول هذه والشركات المصنعة التي لا علاقة لها أيضًا بأنواع الأصول.</span><span class="sxs-lookup"><span data-stu-id="71529-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="71529-124">تحديد شركة مصنعة ونموذج على كائن</span><span class="sxs-lookup"><span data-stu-id="71529-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="71529-125">حدد **إدارة الأصول** \> **عام** \> **الأصول** \> **كل الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="71529-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="71529-126">في عمود ‏‎**الأصل**، حدد الارتباط الخاص بالأصل.</span><span class="sxs-lookup"><span data-stu-id="71529-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="71529-127">تظهر الصفحة **التفاصيل‬**.</span><span class="sxs-lookup"><span data-stu-id="71529-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="71529-128">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="71529-128">Select **Edit**.</span></span>
4. <span data-ttu-id="71529-129">على علامة التبويب السريعة **عام**، حدد القيم في الحقلين **الشركة‏‎ المصنعة** و**النموذج**.</span><span class="sxs-lookup"><span data-stu-id="71529-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
