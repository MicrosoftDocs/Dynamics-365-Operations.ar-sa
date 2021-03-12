---
title: تزويد فوري
description: يصف هذا الموضوع كيف يمكنك استخدام التزويد الفوري لتزويد المخزون عند فشل توجيه موقع في تخصيص المخزون.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 6e2919c003d1dc67b988345260b2747364752222
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004767"
---
# <a name="immediate-replenishment"></a><span data-ttu-id="41ade-103">تزويد فوري</span><span class="sxs-lookup"><span data-stu-id="41ade-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41ade-104">يتيح لك التزويد الفوري تزويد المخزون مباشرةً بعد فشل بند توجيه موقع في تخصيص المخزون.</span><span class="sxs-lookup"><span data-stu-id="41ade-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="41ade-105">يعتمد التزويد على بند واحد في إعداد توجيه الموقع.</span><span class="sxs-lookup"><span data-stu-id="41ade-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="41ade-106">إذا لم يكن المخزون متوفرًا في وحدة القياس المحددة بواسطة هذا البند، يحدث تزويد وحدة القياس هذه مباشرةً.</span><span class="sxs-lookup"><span data-stu-id="41ade-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="41ade-107">يوفر التزويد الفوري بديلاً للطريقة التي يستند فيها تخصيص المخزون يستند إلى بنود إضافية في توجيه الموقع، ويتم فيها تجميع المطلب في نهاية التخصيص وتزويده في وحدة القياس المحددة بواسطة البند الأخير في توجيه الموقع.</span><span class="sxs-lookup"><span data-stu-id="41ade-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="41ade-108">تتمثل مزايا استخدام التزويد الفوري في أن التزويد يمكن أن محدودًا بواسطة وحدات محددة ويمكن توجيه الكمية إلى مواقع محددة.</span><span class="sxs-lookup"><span data-stu-id="41ade-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="41ade-109">سيناريو الأعمال</span><span class="sxs-lookup"><span data-stu-id="41ade-109">Business scenario</span></span>

<span data-ttu-id="41ade-110">على سبيل المثال، لديك مستودع يحتوي على مناطق انتقاء منفصلة لـ "المربع" و"كل" وحدة من وحدات القياس.</span><span class="sxs-lookup"><span data-stu-id="41ade-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="41ade-111">تحتاج أنت إلى تحسين عملية الانتقاء من خلال انتقاء أكبر عدد ممكن من المربعات ثم انتقاء أي كمية متبقية أقل من مربع من منطقة "كل".</span><span class="sxs-lookup"><span data-stu-id="41ade-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="41ade-112">في هذه الحالة، يمكنك استخدام التزويد الفوري.</span><span class="sxs-lookup"><span data-stu-id="41ade-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="41ade-113">في توجيه الموقع، يمكنك إعداد تزويد فوري للمربعات حتى يتم استخدام تزويد الطلب بمجرد وجود نقص في المربعات التي يمكن انتقاؤها لكمية الطلب.</span><span class="sxs-lookup"><span data-stu-id="41ade-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="41ade-114">وبهذه الطريقة، تقوم بتحسين عملية الانتقاء حتى يشتمل الانتقاء على أكبر عدد من المربعات.</span><span class="sxs-lookup"><span data-stu-id="41ade-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="41ade-115">سيُنشئ التزويد الفوري تزويدًا للمربعات، ولن يتم تمرير الطلب حتى يتم انتقاء الكميات في وحدة القياس "كل".</span><span class="sxs-lookup"><span data-stu-id="41ade-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="41ade-116">بمعنى آخر، سيتم انتقاء الكميات التي يجب انتقاؤها في وحدة القياس "كل" (يعني الكميات الأقل من مربع) من المنطقة "كل".</span><span class="sxs-lookup"><span data-stu-id="41ade-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="41ade-117">في حالة حدوث نقص في منطقة "المربع"، يمكنك انتقاء أكبر عدد من المربعات من الطلب الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="41ade-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="41ade-118">سيتم بعد ذلك انتقاء الكميات المتبقية من المنطقة "كل".</span><span class="sxs-lookup"><span data-stu-id="41ade-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="41ade-119">أين يتم التطبيق</span><span class="sxs-lookup"><span data-stu-id="41ade-119">Where it applies</span></span>

<span data-ttu-id="41ade-120">يتم استخدام التزويد الفوري أثناء تنفيذ موجة إذا فشل تخصيص لبند توجيه موقع تم تعيين قالب تزويد له.</span><span class="sxs-lookup"><span data-stu-id="41ade-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="41ade-121">إعداد التزويد الفوري</span><span class="sxs-lookup"><span data-stu-id="41ade-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="41ade-122">انتقل إلى **إدارة المستودعات**\>**الإعداد**\>**توجيهات موقع**، ثم في علامة التبويب **بنود**، في قائمة **قالب التزويد الفوري**، حدد قالب تزويد لطلب الموجة.</span><span class="sxs-lookup"><span data-stu-id="41ade-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="41ade-123">يتم استخدام قالب التزويد في حالة فشل بند توجيه الموقع في تخصيص وحدة قياس مخصصة.</span><span class="sxs-lookup"><span data-stu-id="41ade-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="41ade-124">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="41ade-124">Troubleshooting</span></span>

<span data-ttu-id="41ade-125">إذا تم تحديد التزويد الفوري لبند توجيه موقع، ولكن لم يتم إنشاء أي عمل تزويد عند استخدامك قوالب تزويد طلبات لبند توجيه الموقع هذا، فيجب التحقيق في نوعين من الأسباب الرئيسية:</span><span class="sxs-lookup"><span data-stu-id="41ade-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="41ade-126">تأكد من إعداد قالب تزويد الطلب التي يتم تطبيقه لاستخدام قوالب المواقع وقوالب العمل الصحيحة من نوع **التزويد**.</span><span class="sxs-lookup"><span data-stu-id="41ade-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="41ade-127">تأكد من وجود مخزون فعلى كافٍ في المواقع التي يبحث فيها قالب تزويد الطلب عن مخزون فعلي للتزويد.</span><span class="sxs-lookup"><span data-stu-id="41ade-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>
