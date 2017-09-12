---
title: "حجز نفس الدُفعة لأمر مبيعات"
description: "توضح هذه المقالة كيفية إعداد منتج للسماح بحجز المخزون مقابل دُفعة واحدة من المخزون."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 8e0f8f85609e7c3095f13738d43cdf5734018eaa
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="1f2e4-103">حجز نفس الدُفعة لأمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="1f2e4-103">Reserve the same batch for a sales order</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1f2e4-104">توضح هذه المقالة كيفية إعداد منتج للسماح بحجز المخزون مقابل دُفعة واحدة من المخزون.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="1f2e4-105">يتيح لك حجز نفس الدُفعة إمكانية حجز مخزون لبند أمر مبيعات مقابل دُفعة واحدة من المخزون.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="1f2e4-106">على سبيل المثال، يمكن لعميل يطلب خلفية المطالبة بملء الأمر بالكامل من نفس الدُفعة أو اللوط، لتجنب حالات عدم الاتساق بين القوائم.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="1f2e4-107">ولإعداد منتج لاستخدام حجز الدُفعة ذاتها، يجب أن تكون الإعدادات التالية نشطة في مجموعة نموذج الصنف، وتعقب مجموعة الأبعاد، ومجموعة أبعاد التخزين التي تقوم بتعيينها للمنتج:</span><span class="sxs-lookup"><span data-stu-id="1f2e4-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="1f2e4-108">**مجموعات نموذج الصنف** – يجب أن يتم لمجموعة نموذج الصنف تحديد حقلي **تحديد نفس الدُفعة** و**متطلبات التجميع** في مجموعة حقل **الحجز**لسياسات المخزون.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="1f2e4-109">**تعقب مجموعات الأبعاد** - يجب أن يتم لمجموعة تعقب الأبعاد تحديد حقل **خطة التغطية حسب البعد** لرقم الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="1f2e4-110">**مجموعات أبعاد التخزين** – يجب أن يتم لمجموعة أبعاد التخزين تحديد حقل **خطة التغطية حسب البعد** لـ **الموقع** و**المستودع**.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="1f2e4-111">عند قيامك بحجز المخزون الخاص بمنتج في بند أمر مبيعات تم إعداده لتحديد الدفعة ذاتها، يحاول Microsoft Dynamics 365 for Finance and Operations حجز الكمية المطلوبة من دُفعة مخزون واحدة.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="1f2e4-112">كما يُوضع في الحسبان أي متطلبات سمة دُفعة محددة.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="1f2e4-113">وإذا كان لا يمكن تعبئة الكمية من دُفعة واحدة، تظهر صفحة **تعارض حجز نفس الدُفعة**.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="1f2e4-114">وتصف هذه الصفحة المشاكل وكذلك الإجراءات التي يمكنك اتخاذها لمتابعة الحجز.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="1f2e4-115">وقد تمنع الحالات التالية حجز الدُفعة:</span><span class="sxs-lookup"><span data-stu-id="1f2e4-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="1f2e4-116">يحتوي كود إرجاع الدُفعة على **حظر الحجز** للمبيعات مميزًا بعلامة **محظورة**.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="1f2e4-117">انتهت مدة صلاحية الدُفعة، استناداً إلى تاريخ انتهاء الصلاحية وأي أيام البيع للعميل متاحة.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="1f2e4-118">ولا يزال يمكن وضع الصنف في الاعتبار للحجز في حالة التحكم في مجموعة نماذج الصنف للصنف بواسطة التحكم في تاريخ ‏‫‏‫ما تنتهي صلاحيته أولاً يصرف أولاً (FEFO)، وإذا تم تحديد تاريخ الأفضلية كمعيار انتقاء.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="1f2e4-119">لا تشتمل الدُفعة على أيام عمر متبقية كافية، استناداً إلى تاريخ انتهاء الصلاحية وتاريخ الأفضلية، بالإضافة إلى أية أيام بيع للعملاء.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>





