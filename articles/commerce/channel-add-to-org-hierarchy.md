---
title: إضافة قناة إلى التدرج الهرمي للمؤسسة
description: يصف هذا الموضوع كيفية إضافة قناة إلى التدرج الهرمي لمؤسسة في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 701c90e8e28b4419422cddde698e9c9862a588a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409855"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="cb384-103">إضافة قناة إلى التدرج الهرمي للمؤسسة</span><span class="sxs-lookup"><span data-stu-id="cb384-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cb384-104">يصف هذا الموضوع كيفية إضافة قناة إلى التدرج الهرمي لمؤسسة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb384-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cb384-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="cb384-105">Overview</span></span>

<span data-ttu-id="cb384-106">يجب أن تقترن القنوات بتدرج هرمي أو أكثر للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="cb384-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="cb384-107">قبل إنشاء القنوات، يجب أن تؤكد إعداد التدرجات الهرمية لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="cb384-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="cb384-108">راجع [التدرجات الهرمية للمؤسسات](channels-org-hierarchies.md) لمزيد من التفاصيل حول كيفيه إنشاء التدرجات الهرمية للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="cb384-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="cb384-109">تحديد تدرج هرمي</span><span class="sxs-lookup"><span data-stu-id="cb384-109">Select a hierarchy</span></span>

<span data-ttu-id="cb384-110">لتحديد تدرج هرمي، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="cb384-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="cb384-111">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> التدرجات الهرمية للمؤسسات**.</span><span class="sxs-lookup"><span data-stu-id="cb384-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="cb384-112">من القائمة، حدد التدرج الهرمي للمؤسسات الذي ستضيف القناة إليه.</span><span class="sxs-lookup"><span data-stu-id="cb384-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="cb384-113">في جزء الاجراءات، حدد **عرض** لعرض تفاصيل التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="cb384-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="cb384-114">تظهر الصورة التالية تفاصيل التدرج الهرمي للمؤسسات للتدرج الهرمي المحدد.</span><span class="sxs-lookup"><span data-stu-id="cb384-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![تفاصيل التدرج الهرمي للمؤسسات للتدرج الهرمي المحدد](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="cb384-116">إضافة قناه إلى عقدة التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="cb384-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="cb384-117">لإضافة قناه إلى عقدة التدرج الهرمي، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="cb384-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="cb384-118">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="cb384-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="cb384-119">حدد عقدة التدرج الهرمي التي ترغب في إضافة القناة اليها، ثم حدد **قناة البيع بالتجزئة** من القائمة المنسدلة **ادراج قناة**.</span><span class="sxs-lookup"><span data-stu-id="cb384-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="cb384-120">حدد القناة التي تريد اضافتها، ثم حدد الزر **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cb384-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="cb384-121">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="cb384-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="cb384-122">في جزء الإجراءات، حدد **نشر** وأدخل **تاريخ سريان** في الماضي كي يدخل هذا الاجراء حيز التنفيذ على الفور.</span><span class="sxs-lookup"><span data-stu-id="cb384-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="cb384-123">تظهر الصورة التالية كيفية تحديد قناة لإضافتها إلى عقدة التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="cb384-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![تحديد قناة لإضافتها إلى عقدة التدرج الهرمي](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="cb384-125">تظهر الصورة التالية تدرجًا هرميًا أضيفت إليه قنوات متنوعة.</span><span class="sxs-lookup"><span data-stu-id="cb384-125">The following image shows a hierarchy with various channels added.</span></span>

![تدرج هرمي أضيفت إليه قنوات متعددة](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="cb384-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cb384-127">Additional resources</span></span>

[<span data-ttu-id="cb384-128">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="cb384-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="cb384-129">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="cb384-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="cb384-130">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="cb384-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="cb384-131">تخطيط التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="cb384-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="cb384-132">التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="cb384-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="cb384-133">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="cb384-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="cb384-134">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="cb384-134">Set up an online channel</span></span>](channel-setup-online.md)
