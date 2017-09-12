---
title: "انتقاء الدُفعة الأقدم‬ على جهاز محمول"
description: "يصف هذا الموضوع كيفية إعداد وتطبيق الخيارات لانتقاء الدُفعة الأقدم‬ من جهاز محمول."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 25056886b1a18dbaef12c8732a1fd0bd92a6d04b
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="85829-103">انتقاء الدُفعة الأقدم‬ على جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="85829-103">Pick oldest batch on a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="85829-104">يمكنك الوصول إلى تكوين **انتقاء الدُفعة الأقدم‬** عن طريق قائمة جهاز محمول، وهو يسمح لك بتحذير العاملين في المستودع أو فرض عليهم انتقاء الدُفعة الأقدم‬ في موقعهم الحالي.</span><span class="sxs-lookup"><span data-stu-id="85829-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="85829-105">أين يتم التطبيق</span><span class="sxs-lookup"><span data-stu-id="85829-105">Where it applies</span></span>
<span data-ttu-id="85829-106">تم تكوين انتقاء الدُفعة الأقدم‬ على عناصر القائمة في جهاز محمول، ويتم تنفيذ الانتقاء للدُفعة أسفل العناصر.</span><span class="sxs-lookup"><span data-stu-id="85829-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="85829-107">كيفية إعداد التكوين لانتقاء الدُفعة الأقدم</span><span class="sxs-lookup"><span data-stu-id="85829-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="85829-108">فيما يتعلق بالأصناف التي تم تعيينها لاستخدام العمل الموجود، يمكن تعيين **انتقاء الدُفعة الأقدم** إلى **بلا** أو **تحذير** أو **فرض** من قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="85829-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="85829-109">**بلا**: لن يستلم العاملون أي رسائل، وسيسمح لهم بانتقاء أي دُفعة في موقعهم.</span><span class="sxs-lookup"><span data-stu-id="85829-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="85829-110">**تحذير** و**فرض**: سيتم عرض قائمة بالدُفعة (الدُفعات) ذات تاريخ انتهاء الصلاحية الأقدم فوق عنصر تحكم الدُفعة عندما يقوم العامل بتحديد دُفعة.</span><span class="sxs-lookup"><span data-stu-id="85829-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="85829-111">إذا كان الموقع يخضع لتحكم لوحة ترخيص، فستظهر قائمة بلوحات الترخيص ذات الدُفعة الأقدم فوق عنصر تحكم لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="85829-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="85829-112">**تحذير**: إذا اختار العامل لوحة ترخيص أو دُفعة غير موجودة في القائمة، فسيكون عنصر التحكم فارغًا وسيظهر تحذير يفيد بوجود دُفعة قديمة لتحديدها.</span><span class="sxs-lookup"><span data-stu-id="85829-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="85829-113">لكي يتمكن العامل من متابعة العمل، يستطيع تحديد لوحة الترخيص أو الدفعة نفسها مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="85829-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="85829-114">**فرض**: سوف يستمر العاملون في تلقي الرسالة التي تفيد بوجود دُفعة قديمة لانتقائها.</span><span class="sxs-lookup"><span data-stu-id="85829-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>

