---
title: نظرة عامة على ميزة إقرار الإيرادات
description: يوفر هذا الموضوع معلومات حول ميزة إقرار الإيرادات. توفر هذه الميزة اطار عمل مرنًا يتيح لك تحديد القواعد الخاصة بالشركة للتعرف على سعر الإيرادات وجدول الإيرادات للأوامر متعددة العناصر.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8743183c46463395cad3138261860442701e0178
ms.sourcegitcommit: 0138b6c108a10f2bcb90c91205da8092917160d8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/11/2019
ms.locfileid: "2781886"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="07602-104">نظرة عامة على ميزة إقرار الإيرادات</span><span class="sxs-lookup"><span data-stu-id="07602-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="07602-105">لا يمكن تشغيل ميزة إقرار الإيرادات عبر إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="07602-105">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="07602-106">في الوقت الحالي، يجب استخدام مفاتيح التكوين لتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="07602-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="07602-107">يجب أن تكون الشركات في المجالات التي تبيع عناصر متعددة، مثل المنتجات والخدمات والاشتراكات وغير ذلك، قادرة على تقسيم الأوامر متعددة العناصر بحيث يمكن التعرف على الإيرادات استنادًا إلى مجموعة من الإرشادات الخاصة بالشركة والمجال.</span><span class="sxs-lookup"><span data-stu-id="07602-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="07602-108">بشكل عام، يمكن استخدام عملية إقرار الإيرادات لتنفيذ هذه المهام:</span><span class="sxs-lookup"><span data-stu-id="07602-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="07602-109">تخصيص الإيرادات للمساعدة في ضمان معرفة سعر الإيرادات المناسب استنادًا إلى قيمة المكونات في الأوامر متعددة العناصر.</span><span class="sxs-lookup"><span data-stu-id="07602-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="07602-110">تأجيل الإيرادات استنادًا إلى جدول الإيرادات الذي يمثل الإطار الزمني التعاقدي والنسب المئوية لإقرار الإيرادات بمرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="07602-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE44iER]

<span data-ttu-id="07602-111">تم تضمين الفيديو [كيفية استخدام ميزة إقرار الإيرادات في Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (يظهر أعلاه) في [قائمة تشغيل Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) المتوفرة على YouTube.</span><span class="sxs-lookup"><span data-stu-id="07602-111">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="07602-112">توفر ميزة إقرار الإيرادات اطار عمل مرنًا يتيح لك تحديد القواعد الخاصة بالشركة للتعرف على سعر الإيرادات وجدول الإيرادات للأوامر متعددة العناصر.</span><span class="sxs-lookup"><span data-stu-id="07602-112">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="07602-113">يتم استخدام المنتجات الصادرة لدعم إقرار الإيرادات في مستندات أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="07602-113">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="07602-114">تحتوي المنتجات الصادرة على الإعداد المطلوب لتحديد سعر الإيرادات وجدول الإيرادات.</span><span class="sxs-lookup"><span data-stu-id="07602-114">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="07602-115">يمكن إنشاء أمر المبيعات من مشروع وقت ومادة.</span><span class="sxs-lookup"><span data-stu-id="07602-115">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="07602-116">يمكن للشركات استخدام وظيفة جدول الإيرادات دون استخدام وظيفة سعر الإيرادات.</span><span class="sxs-lookup"><span data-stu-id="07602-116">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="07602-117">وبالتالي، سيتم استخدام السعر الموجود في بنود أمر المبيعات إما كإيرادات أو كإيرادات مؤجلة.</span><span class="sxs-lookup"><span data-stu-id="07602-117">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="07602-118">في حال وجود جدول إيرادات في بند أمر المبيعات، سيتم تأجيل السعر على بند أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="07602-118">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="07602-119">في حال عدم وجود جدول إيرادات في بند أمر المبيعات، فسيتم ترحيل بند أمر المبيعات إلى حساب إيرادات عند فوترته.</span><span class="sxs-lookup"><span data-stu-id="07602-119">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="07602-120">يتم حساب سعر الإيرادات إما عند تأكيد أمر المبيعات أو عند ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="07602-120">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="07602-121">لمعاينة سعر الإيرادات قبل ترحيل الفاتورة، يجب تأكيد أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="07602-121">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="07602-122">عند تأكيد أمر المبيعات، يتم أيضاً إنشاء جدول للإيرادات المتوقعة في حالة وجود جدول إيرادات داخل أي من بنود أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="07602-122">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="07602-123">عند فوترة أمر المبيعات، يتم حذف جدول الإيرادات المتوقعة ويتم استبداله بجدول إقرار الإيرادات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="07602-123">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="07602-124">ويتم الاحتفاظ بتفاصيل جدول إقرار الإيرادات لكل بند من بنود أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="07602-124">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="07602-125">وبالتالي، بإمكان مدير إقرار الإيرادات عرض التفاصيل وإصدار البنود إلى الإيرادات عند اكتمال الالتزام التعاقدي.</span><span class="sxs-lookup"><span data-stu-id="07602-125">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="07602-126">وفي نهاية كل فترة، بإمكان مدير إقرار الإيرادات إنشاء دفتر يومية إيرادات لإصدار أي بنود جدول تستحق في تاريخ قام بتحديده أو قبله.</span><span class="sxs-lookup"><span data-stu-id="07602-126">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date that he or she defines.</span></span> <span data-ttu-id="07602-127">لا يتم ترحيل دفتر يومية الإيرادات هذا على الفور.</span><span class="sxs-lookup"><span data-stu-id="07602-127">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="07602-128">والتالي، بإمكان مدير إقرار الإيرادات التحقق من إصدار المبالغ الصحيحة من الإيرادات المؤجلة إلى الإيرادات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="07602-128">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="07602-129">إذا تسبب تغيير تعاقدي في إضافة بند أمر مبيعات جديد إما إلى أمر المبيعات الموجود أو إلى أمر مبيعات جديد، يمكن إجراء عملية إعادة تخصيص لتصحيح سعر الإيرادات عبر جميع البنود في أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="07602-129">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
