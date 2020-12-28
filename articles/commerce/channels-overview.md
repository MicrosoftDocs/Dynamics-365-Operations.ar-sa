---
title: نظرة عامة على القنوات
description: يقدم هذا الموضوع نظرة عامة على القنوات في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 099ccd9f769ea5c431c1a82532d8654cbbd082b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409852"
---
# <a name="channels-overview"></a><span data-ttu-id="f7b85-103">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="f7b85-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f7b85-104">يقدم هذا الموضوع نظرة عامة على القنوات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7b85-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="f7b85-105">وهو يتضمن معلومات حول المهام التي يجب إتمامها قبل وبعد إعداد كل قناة.</span><span class="sxs-lookup"><span data-stu-id="f7b85-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="f7b85-106">أنواع القنوات</span><span class="sxs-lookup"><span data-stu-id="f7b85-106">Types of Channels</span></span>

<span data-ttu-id="f7b85-107">يدعم Dynamics 365 Commerce ثلاثة أنواع مختلفة من القنوات: البيع بالتجزئة ومركز الاتصال والقنوات عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="f7b85-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="f7b85-108">قنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="f7b85-108">Retail channels</span></span>

<span data-ttu-id="f7b85-109">تمثل قنوات البيع بالتجزئة المتاجر القياسية التقليدية.</span><span class="sxs-lookup"><span data-stu-id="f7b85-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="f7b85-110">بإمكان كل متجر أن يتضمن سجلات نقاط بيع (POS) بالإضافة إلى حسابات إيرادات ومصروفات خاصة به بالإضافة إلى فريق عمل خاص به أيضًا.</span><span class="sxs-lookup"><span data-stu-id="f7b85-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="f7b85-111">قنوات مراكز الاتصال</span><span class="sxs-lookup"><span data-stu-id="f7b85-111">Call center channels</span></span>

<span data-ttu-id="f7b85-112">تمثل قنوات مراكز الاتصال أوامر مراكز الاتصال وإدارة العملاء.</span><span class="sxs-lookup"><span data-stu-id="f7b85-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="f7b85-113">قنوات على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="f7b85-113">Online channels</span></span>

<span data-ttu-id="f7b85-114">تمثل القنوات عبر الإنترنت متاجر التجارة الإلكترونية عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="f7b85-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="f7b85-115">عن إنشاء قناة عبر الإنترنت، يجب إنشاء موقع باستخدام أداة منشئ الموقع من Microsoft Dynamics 365 Commerce أو حل تجارة إلكترونية خارجي آخر.</span><span class="sxs-lookup"><span data-stu-id="f7b85-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="f7b85-116">أساسيات إعداد القناة</span><span class="sxs-lookup"><span data-stu-id="f7b85-116">Channel setup basics</span></span>

<span data-ttu-id="f7b85-117">يتم تنفيذ إعداد القناة في أداة Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7b85-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="f7b85-118">تتوفر لدى كل قناة طرق دفع ومجموعات أسعار وتدرجات هرمية للمنتجات ومجموعات متنوعة ومجموعات من المنتجات خاصة بها.</span><span class="sxs-lookup"><span data-stu-id="f7b85-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="f7b85-119">وبعد إنشاء قناة، يمكنك تعيين المنتجات التي ترغب أن تتضمنها هذه القناة وتبيعها.</span><span class="sxs-lookup"><span data-stu-id="f7b85-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="f7b85-120">تتوفر مجموعة فريدة من الميزات التي تحتاج إلى تكوينها لكل نوع قناة.</span><span class="sxs-lookup"><span data-stu-id="f7b85-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="f7b85-121">على سبيل المثال، تحتاج قناة بيع بالتجزئة إلى موظفين وسجلات وعملاء معينين لها.</span><span class="sxs-lookup"><span data-stu-id="f7b85-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="f7b85-122">بعد إنشاء قناة جديدة، يجب تعيينها إلى تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="f7b85-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="f7b85-123">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="f7b85-123">Channel setup prerequisites</span></span>

<span data-ttu-id="f7b85-124">قبل إعداد قناة، يجب عليك إكمال بعض المهام المطلوبة استنادًا إلى نوع القناة.</span><span class="sxs-lookup"><span data-stu-id="f7b85-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="f7b85-125">لمزيد من المعلومات، راجع [المتطلبات الأساسية‬ لإعداد قناة‬](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="f7b85-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="f7b85-126">إعداد قناة</span><span class="sxs-lookup"><span data-stu-id="f7b85-126">Set up a channel</span></span>

<span data-ttu-id="f7b85-127">بعد إكمال المهام المطلوبة، استخدم الارتباطات التالية للحصل على مزيد من إرشادات الإعداد:</span><span class="sxs-lookup"><span data-stu-id="f7b85-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="f7b85-128">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="f7b85-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="f7b85-129">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="f7b85-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="f7b85-130">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="f7b85-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="f7b85-131">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f7b85-131">Additional resources</span></span>

[<span data-ttu-id="f7b85-132">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="f7b85-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="f7b85-133">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="f7b85-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="f7b85-134">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="f7b85-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="f7b85-135">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="f7b85-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="f7b85-136">إعداد التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="f7b85-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)
