---
title: إطارات الوقت
description: يمكنك استخدام الإطارات الزمنية لتحسين جدولة بنود أمر الخدمة.
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f748268f6cb85ff835919485da2828689eee23c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555350"
---
# <a name="time-windows"></a><span data-ttu-id="108ce-103">إطارات الوقت</span><span class="sxs-lookup"><span data-stu-id="108ce-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="108ce-104">يمكنك استخدام الإطارات الزمنية لتحسين جدولة بنود أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="108ce-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="108ce-105">يمكن إعداد النظام بحيث ينشئ أوامر الخدمة بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="108ce-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="108ce-106">استنادًا إلى المعايير المحددة من خلال إطار زمني، يمكنك ربط أكبر عدد ممكن من بنود أوامر الخدمة بأقل عدد ممكن من أوامر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="108ce-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="108ce-107">تحدد الإطارات الزمنية إلى أي مدى يمكن لبند أمر الخدمة الانتقال من تاريخه المحسوب,</span><span class="sxs-lookup"><span data-stu-id="108ce-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="108ce-108">التاريخ المحسوب هو التاريخ الذي تم فيه جدولة حدوث بند أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="108ce-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="108ce-109">يستند التاريخ إلى إعداد فترته وفترة الخدمة التي حددتها في صفحة **إنشاء أوامر الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="108ce-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="108ce-110">يمكنك تحديد الإطار الزمني باستخدام القيم في الجدول التالي:</span><span class="sxs-lookup"><span data-stu-id="108ce-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="108ce-111">الأسلوب</span><span class="sxs-lookup"><span data-stu-id="108ce-111">Method</span></span> | <span data-ttu-id="108ce-112">الوصف</span><span class="sxs-lookup"><span data-stu-id="108ce-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="108ce-113">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="108ce-113">Week</span></span>   | <span data-ttu-id="108ce-114">يمكن نقل تاريخ بند أمر الخدمة إلى أي يوم مفتوح في نفس الأسبوع على أنه التاريخ المحسوب الابتدائي.</span><span class="sxs-lookup"><span data-stu-id="108ce-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="108ce-115">الشهر</span><span class="sxs-lookup"><span data-stu-id="108ce-115">Month</span></span>  | <span data-ttu-id="108ce-116">يمكن نقل تاريخ بند أمر الخدمة إلى أي يوم مفتوح في نفس الشهر على أنه التاريخ المحسوب الابتدائي.</span><span class="sxs-lookup"><span data-stu-id="108ce-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="108ce-117">على سبيل المثال، التاريخ المحسوب لبند أمر خدمة هو 15 فبراير 2017.</span><span class="sxs-lookup"><span data-stu-id="108ce-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="108ce-118">يمكن جدولة بند أمر الخدمة لأي يوم من أيام الأسبوع بين 1 فبراير و28 فبراير 2017.</span><span class="sxs-lookup"><span data-stu-id="108ce-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="108ce-119">يدوي</span><span class="sxs-lookup"><span data-stu-id="108ce-119">Manual</span></span> | <span data-ttu-id="108ce-120">يمكنك تحديد الحد الأقصى لعدد الأيام التي يمكن نقل بند أمر الخدمة بموجبها قبل أو بعد التاريخ المحسوب الابتدائي.</span><span class="sxs-lookup"><span data-stu-id="108ce-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="108ce-121">إذا لم يتم تحديد إطار زمني لبند اتفاقية الخدمة، فيجب أن يكون بند أمر الخدمة المشتق من اتفاقية الخدمة في نفس التاريخ الذي تمت جدولته له في الأصل.</span><span class="sxs-lookup"><span data-stu-id="108ce-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="108ce-122">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="108ce-122">Related topics</span></span>

[<span data-ttu-id="108ce-123">إنشاء الإطارات الزمنية</span><span class="sxs-lookup"><span data-stu-id="108ce-123">Create time windows</span></span>](create-time-windows.md)

