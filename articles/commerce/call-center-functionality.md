---
title: وظائف مبيعات مركز الاتصال
description: يقدم هذا الموضوع نظرة عامة حول وظائف مبيعات مركز الاتصال في Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7091e8ba7940e358d77c69c63e26c8f3d9337713
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107246"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="53288-103">وظيفة مبيعات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="53288-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="53288-104">في Dynamics 365 Commerce، يعتبر مركز الاتصال نوع قناة يمكن تعريفها في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="53288-104">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="53288-105">إن تحديد قناة محددة لكيانات مركز الاتصال الخاص بك يسمح للنظام بربط الإعدادات الافتراضية للبيانات الخاصة والإعدادات الافتراضية لمعالجة الأوامر مع أوامر المبيعات التي تم إنشاؤها بواسطة مستخدم القناة مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="53288-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="53288-106">تتضمن ميزات مركز الاتصال سعرًا متقدمًا وعروضًا ترويجية وكتالوجات وبطاقات هدايا وبرامج الولاء وقسائم.</span><span class="sxs-lookup"><span data-stu-id="53288-106">Call center features include advanced price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="53288-107">كما يستفيد من أوامر مركز الاتصال أيضًا تطبيق نقطة البيع (POS) لدعم سيناريوهات استيفاء الأمر عبر القناة.</span><span class="sxs-lookup"><span data-stu-id="53288-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="53288-108">تجدر الإشارة إلى عدم تحسين الإصدار الحالي من تطبيق مركز الاتصال للاستخدام في سيناريوهات معالجة الأوامر من شركة إلى شركة (B2B)، أو السيناريوهات التي تتضمن فيها الأوامر عددًا كبيرًا من بنود المبيعات بينما يمكن استخدام وحدة مركز الاتصال من جانب المجالات الأخرى خارج Commerce.</span><span class="sxs-lookup"><span data-stu-id="53288-108">It's important to note that while the call center module can be utilized by other industries outside of Commerce, the current release of the call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large number of sales lines.</span></span> <span data-ttu-id="53288-109">من المستحسن للمستخدمين الذين يريدون الاستفادة من ميزات مركز الاتصال لمعالجة الأوامر خارج معالجة الحركة المباشر إلى المستهلك النموذجية، أن يخصصوا وقتًا كافيًا لاختبار والتحقق من أن تمكين وظيفة مركز الاتصال يتواقف مع الاحتياجات الوظيفية ومتطلبات الأداء.</span><span class="sxs-lookup"><span data-stu-id="53288-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="53288-110">بالإضافة إلى دعم إنشاء الأمر، توفر الوحدة النمطية لمراكز الاتصال أيضًا تطبيق خدمة عملاء سهل الاستخدام والذي يسهل على المستخدمين تحديد موقع حسابات العملاء ومراجعة كافة بيانات أمر العميل ذي الصلة والسمات.</span><span class="sxs-lookup"><span data-stu-id="53288-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="53288-111">تم تصميم شاشة خدمة العميل لتمكين المستخدم من الوصول بسرعة إلى البيانات ذات الصلة بالأمر والسماح له بالرد على الأسئلة الشائعة المتعلقة بالأمر التي تم تلقيها من العملاء.</span><span class="sxs-lookup"><span data-stu-id="53288-111">The customer service screen is designed to enable a user to quickly access order-related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="53288-112">توفر هذه الصفحة ارتباطات إلى الوثائق ذات الصلة المتعلقة بالإعداد والتكوين والاستخدام الوظيفي لميزات مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="53288-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="53288-113">تكوين مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="53288-113">Configure the call center</span></span>

[<span data-ttu-id="53288-114">إعداد قنوات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="53288-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="53288-115">تكوين معالجة الأمر</span><span class="sxs-lookup"><span data-stu-id="53288-115">Configure order processing</span></span>

[<span data-ttu-id="53288-116">إعداد مركز اتصال تنبيهات الاحتيال والعمل باستخدامه</span><span class="sxs-lookup"><span data-stu-id="53288-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="53288-117">تكوين ‏‫تعليقات أوامر مركز الاتصال‬ والعمل باستخدامها</span><span class="sxs-lookup"><span data-stu-id="53288-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="53288-118">تكوين معالجة الدفع</span><span class="sxs-lookup"><span data-stu-id="53288-118">Configure payment processing</span></span>

[<span data-ttu-id="53288-119">طرق الدفع في مراكز الاتصال</span><span class="sxs-lookup"><span data-stu-id="53288-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="53288-120">تكوين أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="53288-120">Configure delivery modes</span></span>

[<span data-ttu-id="53288-121">تكوين أوضاع تسليم مركز الاتصال والمصاريف</span><span class="sxs-lookup"><span data-stu-id="53288-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="53288-122">تكوين التسويق المباشر</span><span class="sxs-lookup"><span data-stu-id="53288-122">Configure direct marketing</span></span>

[<span data-ttu-id="53288-123">كتالوجات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="53288-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="53288-124">إعداد تحليل Recency والتكرار والنقدية (RFM)</span><span class="sxs-lookup"><span data-stu-id="53288-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="53288-125">تكوين برامج الاستمرارية</span><span class="sxs-lookup"><span data-stu-id="53288-125">Configure continuity programs</span></span>

[<span data-ttu-id="53288-126">إعداد برامج الاستمرارية لمراكز الاتصال</span><span class="sxs-lookup"><span data-stu-id="53288-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
