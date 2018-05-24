---
title: "وظيفة مركز الاتصال"
description: "يوفر هذا الموضوع نظرة عامة على وظائف مبيعات مركز الاتصال في Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e85b65e116b32adca09e46252d7d3bbe5101e1cf
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="call-center"></a><span data-ttu-id="3cf04-103">مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="3cf04-103">Call center</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="3cf04-104">في Dynamics 365 for Retail، أحد مراكز اتصال هو نوع من قناة البيع بالتجزئة يمكن تعريفها في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="3cf04-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="3cf04-105">إن تحديد قناة محددة لكيانات مركز الاتصال الخاص بك يسمح للنظام بربط الإعدادات الافتراضية للبيانات الخاصة والإعدادات الافتراضية لمعالجة الأوامر مع أوامر المبيعات التي تم إنشاؤها بواسطة مستخدم القناة مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="3cf04-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="3cf04-106">تتضمن ميزات مركز الاتصال سعر البيع بالتجزئة المتقدم والعروض الترويجية والكتالوجات، وبطاقات الهدايا، وبرامج الولاء والقسائم.</span><span class="sxs-lookup"><span data-stu-id="3cf04-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="3cf04-107">كما يستفيد من أوامر مركز الاتصال أيضًا تطبيق نقطة البيع (POS) لدعم سيناريوهات استيفاء الأمر عبر القناة.</span><span class="sxs-lookup"><span data-stu-id="3cf04-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="3cf04-108">من المهم ملاحظة أنه بينما يمكن استخدام الوحدة النمطية لمركز الاتصال من جانب الصناعات الأخرى خارج البيع بالتجزئة (Retail)، ولكن الإصدار الحالي من تطبيق مركز الاتصال في Dynamics 365 for Retail لم يتم تحسينه للاستخدام في سيناريوهات معالجة الأوامر من شركة إلى شركة (B2B)، أو السيناريوهات التي تتضمن فيها الأوامر كمًا كبيرًا من بنود المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3cf04-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="3cf04-109">من المستحسن للمستخدمين الذين يريدون الاستفادة من ميزات مركز الاتصال لمعالجة الأوامر خارج معالجة الحركة المباشر إلى المستهلك النموذجية، أن يخصصوا وقتًا كافيًا لاختبار والتحقق من أن تمكين وظيفة مركز الاتصال يتواقف مع الاحتياجات الوظيفية ومتطلبات الأداء.</span><span class="sxs-lookup"><span data-stu-id="3cf04-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="3cf04-110">بالإضافة إلى دعم إنشاء الأمر، توفر الوحدة النمطية لمراكز الاتصال أيضًا تطبيق خدمة عملاء سهل الاستخدام والذي يسهل على المستخدمين تحديد موقع حسابات العملاء ومراجعة كافة بيانات أمر العميل ذي الصلة والسمات.</span><span class="sxs-lookup"><span data-stu-id="3cf04-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="3cf04-111">تم تصميم شاشة خدمة العميل لتمكين المستخدم من الوصول بسرعة إلى البيانات ذات الصلة بالأمر والسماح له بالرد على الأسئلة الشائعة المتعلقة بالأمر التي تم تلقيها من العملاء.</span><span class="sxs-lookup"><span data-stu-id="3cf04-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="3cf04-112">توفر هذه الصفحة ارتباطات إلى الوثائق ذات الصلة المتعلقة بالإعداد والتكوين، واستخدام ميزات مركز اتصال في Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3cf04-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="3cf04-113">تكوين مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="3cf04-113">Configure the call center</span></span>
[<span data-ttu-id="3cf04-114">إعداد خيارات معالجة الأوامر</span><span class="sxs-lookup"><span data-stu-id="3cf04-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="3cf04-115">تكوين معالجة الأمر</span><span class="sxs-lookup"><span data-stu-id="3cf04-115">Configure order processing</span></span>
<span data-ttu-id="3cf04-116">[إعداد تنبيهات الاحتيال](set-up-fraud-alerts.md)
[الاحتفاظ بالأوامر يدويًا](work-with-order-holds.md)</span><span class="sxs-lookup"><span data-stu-id="3cf04-116">[Set up fraud alerts](set-up-fraud-alerts.md)
[Manual Order Holds](work-with-order-holds.md)</span></span>

## <a name="configure-payment-processing"></a><span data-ttu-id="3cf04-117">تكوين معالجة الدفع</span><span class="sxs-lookup"><span data-stu-id="3cf04-117">Configure payment processing</span></span>
[<span data-ttu-id="3cf04-118">طرق الدفع في مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="3cf04-118">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="3cf04-119">تكوين التسويق المباشر</span><span class="sxs-lookup"><span data-stu-id="3cf04-119">Configure direct marketing</span></span>
[<span data-ttu-id="3cf04-120">كتالوجات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="3cf04-120">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="3cf04-121">إعداد تحليل RFM</span><span class="sxs-lookup"><span data-stu-id="3cf04-121">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="3cf04-122">تكوين برامج الاستمرارية</span><span class="sxs-lookup"><span data-stu-id="3cf04-122">Configure continuity programs</span></span>
[<span data-ttu-id="3cf04-123">إعداد برنامج استمرارية لمركز اتصال</span><span class="sxs-lookup"><span data-stu-id="3cf04-123">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)


