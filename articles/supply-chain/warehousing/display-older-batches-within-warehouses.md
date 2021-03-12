---
title: تكوين عرض المجموعات القديمة داخل المستودع على جهاز محمول
description: يصف هذا الموضوع كيفية إعداد جهاز محمول لعرض قائمة بالمواقع مع دُفعات أقدم من الموقع الحالي لخط العمل.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 418ce3b320024780def0f7c5687b7c2e1c6b6f2b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996213"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="8f27a-103">تكوين عرض المجموعات القديمة داخل المستودع على جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="8f27a-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f27a-104">يسمح لك تكوين **عرض المجموعات القديمة داخل المستودع** بعرض قائمة بالمواقع مع دُفعات أقدم من الموقع الحالي لخط العمل.</span><span class="sxs-lookup"><span data-stu-id="8f27a-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="8f27a-105">تتضمن قائمة المواقع التي يتم عرضها معلومات حول الدُفعات الأقدم في الموقع مع تاريخ انتهاء الصلاحية والمخزون الفعلي لكل دُفعة.</span><span class="sxs-lookup"><span data-stu-id="8f27a-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="8f27a-106">يمكنك اختيار الانتقاء من موقع جديد أو متابعة الانتقاء من الموقع الحالي.</span><span class="sxs-lookup"><span data-stu-id="8f27a-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="8f27a-107">انتقاء من موقع جديد- إذا قمت بتحديد موقع جديد للانتقاء منه، يتم تحديث خط العمل الحالي لاستخدام الموقع الجديد وسيستمر العمل كالمعتاد مع الموقع الجديد.</span><span class="sxs-lookup"><span data-stu-id="8f27a-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="8f27a-108">لكي يكون الموقع الجديد صالحًا، يجب أن يتضمن الكمية المتوفرة الكافية لخط العمل بكامله.</span><span class="sxs-lookup"><span data-stu-id="8f27a-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="8f27a-109">في حالة عدم توفر الكمية المطلوبة، لن يتم تحديث خط العمل، وستظهر القائمة.</span><span class="sxs-lookup"><span data-stu-id="8f27a-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="8f27a-110">متابعة الانتقاء من الموقع الحالي - إذا تابعت مع موقع حط العمل الحالي، فسيستمر انتقاء الكميات الخاصة بخط العمل من الموقع الأصلي.</span><span class="sxs-lookup"><span data-stu-id="8f27a-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="8f27a-111">أين يتم التطبيق</span><span class="sxs-lookup"><span data-stu-id="8f27a-111">Where it applies</span></span>
<span data-ttu-id="8f27a-112">تم تكوين عرض المجموعات القديمة داخل المستودع على أصناف قائمة جهاز محمول، وهذا يؤثر على انتقاء الدُفعة أسفل الأصناف.</span><span class="sxs-lookup"><span data-stu-id="8f27a-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="8f27a-113">إعداد عرض المجموعات القديمة داخل المستودع</span><span class="sxs-lookup"><span data-stu-id="8f27a-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="8f27a-114">يتوفر تكوين **عرض المجموعات القديمة داخل المستودع** على أصناف قائمة الجهاز المحمول عند تعيين الخيار **انتقاء الدُفعة الأقدم‬** إلى **تحذير**.</span><span class="sxs-lookup"><span data-stu-id="8f27a-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="8f27a-115">ضمن **إدارة المستودعات** > **الإعداد** > **الجهاز المحمول** > **أصناف قائمة الجهاز المحمول**، عيّن **استخدام العمل الموجود** إلى **نعم** لصنف القائمة، وحدد **تحذير** في الحقل **انتقاء الدُفعة الأقدم‬**.</span><span class="sxs-lookup"><span data-stu-id="8f27a-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 

