---
title: تكوين قناة لاستخدام التدرج الهرمي للتنقل في قناة
description: يصف هذا الموضوع كيفية تكوين قناة لاستخدام تدرج هرمي للتنقل في قناة في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ceb6aa65c2ed5bc8d4224bdaf7095fba769181e8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220572"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="41fca-103">تكوين قناة لاستخدام التدرج الهرمي للتنقل في قناة</span><span class="sxs-lookup"><span data-stu-id="41fca-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="41fca-104">يصف هذا الموضوع كيفية تكوين قناة لاستخدام تدرج هرمي للتنقل في قناة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="41fca-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="41fca-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="41fca-105">Overview</span></span>

<span data-ttu-id="41fca-106">تقوم التدرجات الهرمية للتنقل في القناة بتنظيم المنتجات في فئات بحيث يمكن استعراض الفئات في موقع تجارة إلكترونية أو في نقاط البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="41fca-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="41fca-107">يجب تكوين قنوات البيع بالتجزئة والقنوات عبر الإنترنت بواسطة التدرجات الهرمية للتنقل في القناة.</span><span class="sxs-lookup"><span data-stu-id="41fca-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="41fca-108">تكوين القناة</span><span class="sxs-lookup"><span data-stu-id="41fca-108">Configure the channel</span></span>

<span data-ttu-id="41fca-109">لتكوين قناة لاستخدام تدرج هرمي للتنقل في القناة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="41fca-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="41fca-110">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> فئات القناة وسمات المنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="41fca-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="41fca-111">حدد القناة المطلوب تكوينها.</span><span class="sxs-lookup"><span data-stu-id="41fca-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="41fca-112">في جزء الإجراءات، حدد **تعيين بيانات تعريف السمة**.</span><span class="sxs-lookup"><span data-stu-id="41fca-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="41fca-113">في القائمة المنسدلة **التدرج الهرمي للفئات** ، حدد التدرج الهرمي المناسب للتنقل في القناة‬.</span><span class="sxs-lookup"><span data-stu-id="41fca-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="41fca-114">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="41fca-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="41fca-115">ضمن **مجموعة السمات**، أضف أي مجموعات سمات ستكون سمات عمومية لكافة العقد</span><span class="sxs-lookup"><span data-stu-id="41fca-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="41fca-116">تُظهر الصورة التالية كيفية تكوين قناة لاستخدام تدرج هرمي للتنقل في القناة.</span><span class="sxs-lookup"><span data-stu-id="41fca-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![مثال عن تكوين قناة](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="41fca-118">تعيين بيانات تعريف السمة</span><span class="sxs-lookup"><span data-stu-id="41fca-118">Set attribute metadata</span></span>

<span data-ttu-id="41fca-119">سيؤدي تعيين بيانات تعريف السمة إلى السماح بتكوين سمات في كل عقدة.</span><span class="sxs-lookup"><span data-stu-id="41fca-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="41fca-120">لتعيين بيانات تعريف السمة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="41fca-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="41fca-121">في جزء الإجراءات، حدد **تعيين بيانات تعريف السمة**.</span><span class="sxs-lookup"><span data-stu-id="41fca-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="41fca-122">لكل عقدة، حدد **سمات منتج القناة‬**.</span><span class="sxs-lookup"><span data-stu-id="41fca-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="41fca-123">قم بتعيين **إظهار السمة على القناة** إلى **نعم** و **يمكن تحسينه‬** إلى **نعم**، لتمكين المدققات على تلك القناة.</span><span class="sxs-lookup"><span data-stu-id="41fca-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="41fca-124">بعد تكوين كل عقدة كما هو مطلوب ،في **جزء الإجراءات**، حدد الزر **حفظ** للحفظ.</span><span class="sxs-lookup"><span data-stu-id="41fca-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="41fca-125">حدد **X** في الزاوية العلوية اليسرى للخروج من هذه الشاشة والعودة إلى صفحة **فئات القناة وسمات المنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="41fca-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="41fca-126">تعرض الصورة التالية مثالاً لمجموعة من سمات منتج القناة التي تم تكوينها علي عقدة فئة القناة.</span><span class="sxs-lookup"><span data-stu-id="41fca-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![سمات القناة في عقدة فئة القناة](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="41fca-128">نشر التغييرات</span><span class="sxs-lookup"><span data-stu-id="41fca-128">Publish changes</span></span>

<span data-ttu-id="41fca-129">لكي تسري التغييرات، يجب نشرها.</span><span class="sxs-lookup"><span data-stu-id="41fca-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="41fca-130">لنشر التغييرات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="41fca-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="41fca-131">في جزء الاجراءات، حدد **نشر تحديثات القناة**.</span><span class="sxs-lookup"><span data-stu-id="41fca-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="41fca-132">في الجزء **نشر تحديثات القناة**، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="41fca-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="41fca-133">تظهر الصورة التالية كيفية نشر تحديثات القناة.</span><span class="sxs-lookup"><span data-stu-id="41fca-133">The following image shows how to publish channel updates.</span></span>

![نشر تحديثات القناة](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="41fca-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="41fca-135">Additional resources</span></span>

[<span data-ttu-id="41fca-136">إنشاء تدرج هرمي للتنقل في قناة</span><span class="sxs-lookup"><span data-stu-id="41fca-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]