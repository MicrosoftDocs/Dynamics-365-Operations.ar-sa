---
title: تأكيد انتقاء الأجزاء
description: يصف هذا الموضوع كيفية إعداد وتطبيق تأكيد انتقاء الأجزاء من جهاز محمول.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66903d142ecb7228e4fdec56dbd45472acbdeb69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989633"
---
# <a name="piece-picking-confirmation"></a><span data-ttu-id="3b10c-103">تأكيد انتقاء الأجزاء</span><span class="sxs-lookup"><span data-stu-id="3b10c-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b10c-104">يسمح لك انتقاء الأجزاء بتأكيد كل جزء من المخزون من خلال الانتقاء أو الجرد على جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="3b10c-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="3b10c-105">بالنسبة إلى عمليات الانتقاء، يمكنك تأكيد كمية العمل التي ستتم معالجتها وصولاً إلى الكمية المحددة في العمل المراد انتقاؤه.</span><span class="sxs-lookup"><span data-stu-id="3b10c-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="3b10c-106">بالنسبة إلى الجرد، يمكنك فحص المخزون الذي تجري جردًا له وتعقب المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="3b10c-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="3b10c-107">عند تمكين انتقاء الأجزاء، يتم تحديد تأكيد المنتجات تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="3b10c-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="3b10c-108">بالنسبة إلى عمليات الانتقاء من نوع العمل، يتم تمكين حد أقصى من عدد الأجزاء.</span><span class="sxs-lookup"><span data-stu-id="3b10c-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="3b10c-109">سيسمح لك ذلك بتعيين حد أقصى لعدد الأجزاء التي يجب تأكيدها أثناء عملية العمل.</span><span class="sxs-lookup"><span data-stu-id="3b10c-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="3b10c-110">تستند الكمية القصوى إلى وحدة العمل الحالية التي تتم معالجتها.</span><span class="sxs-lookup"><span data-stu-id="3b10c-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="3b10c-111">لا يسمح نوع عمل الجرد بحد أقصى.</span><span class="sxs-lookup"><span data-stu-id="3b10c-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="3b10c-112">يمكنك أيضًا استخدام الكمية ووحدة القياس المقترنة بكود شريطي تم مسحه.</span><span class="sxs-lookup"><span data-stu-id="3b10c-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="3b10c-113">سيصلح هذا الأسلوب للتدفقات المستلمة أو الواردة بما في ذلك استلام لوحة الترخيص المختلطة وصنف أمر الشراء وصنف أمر التحويل وصنف حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="3b10c-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="3b10c-114">ويصلح أيضًا لانتقاء الأجزاء حيث سيؤدي مسح الكود الشريطي إلى إضافة الكمية إلى العدد الإجمالي للأجزاء المؤكدة من خلال التحويل بين وحدة القياس على الكود الشريطي ووحدة العمل.</span><span class="sxs-lookup"><span data-stu-id="3b10c-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="3b10c-115">عند حساب وحدة قياس الكود الشريطي، إذا تأكد أن الكمية مسموحة للجرد في مجموعة التسلسلات، ستتم إضافة الكمية إلى العدد الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="3b10c-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="3b10c-116">أين يتم التطبيق</span><span class="sxs-lookup"><span data-stu-id="3b10c-116">Where it applies</span></span>

<span data-ttu-id="3b10c-117">يصلح انتقاء الأجزاء لكل أعمال الجرد وللانتقال الأولي لأي نوع عمل.</span><span class="sxs-lookup"><span data-stu-id="3b10c-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="3b10c-118">لا ينطبق انتقاء الأجزاء إذا كان الصنف خاضعًا لتحكم الأرقام المسلسلة أو إذا كان عبارة عن إنتاج أو انتقاء كانبان‬ من موقع لوحة ترخيص وإذا تم تعيين الصنف إلى تشغيل مرحلي.</span><span class="sxs-lookup"><span data-stu-id="3b10c-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="3b10c-119">إعداد انتقاء الأجزاء</span><span class="sxs-lookup"><span data-stu-id="3b10c-119">Set up piece picking</span></span>

1.  <span data-ttu-id="3b10c-120">في عنصر قائمة جهاز محمول، قم بفتح نموذج الإعداد من تأكيد العمل: إدارة المستودعات‬ > **إدارة المستودعات‬** > **الإعداد** > **جهاز محمول** > **عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="3b10c-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="3b10c-121">من عنصر قائمة الجهاز المحمول، قم بفتح إعداد تأكيد العمل.</span><span class="sxs-lookup"><span data-stu-id="3b10c-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="3b10c-122">تصبح الخيارات التالية متوفرة للاختيار منها عندما يكون نوع العمل انتقاء أو جرد.</span><span class="sxs-lookup"><span data-stu-id="3b10c-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="3b10c-123">الخيار</span><span class="sxs-lookup"><span data-stu-id="3b10c-123">Option</span></span>           |                                                                            <span data-ttu-id="3b10c-124">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="3b10c-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b10c-125">تأكيد انتقاء الأجزاء</span><span class="sxs-lookup"><span data-stu-id="3b10c-125">Piece picking confirmation</span></span> | <span data-ttu-id="3b10c-126">أنواع العمل المتوفرة للانتقاء والجرد.</span><span class="sxs-lookup"><span data-stu-id="3b10c-126">Available for pick and counting work types.</span></span> <span data-ttu-id="3b10c-127">يتم تحديد تأكيد المنتج تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="3b10c-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="3b10c-128">يسمح لك بتأكيد كل جزء من المخزون من الهاتف المحمول.</span><span class="sxs-lookup"><span data-stu-id="3b10c-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="3b10c-129">أقصى عدد للأجزاء</span><span class="sxs-lookup"><span data-stu-id="3b10c-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="3b10c-130">متوفر لعمل الانتقاء إذا تم تمكين تأكيد انتقاء الأجزاء.</span><span class="sxs-lookup"><span data-stu-id="3b10c-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="3b10c-131">تعيين حد لعدد الأجزاء التي يجب عليك تأكيدها.</span><span class="sxs-lookup"><span data-stu-id="3b10c-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |

