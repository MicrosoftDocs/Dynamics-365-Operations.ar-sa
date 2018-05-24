---
title: "نظرة عامة على سير عمل الاشتراك"
description: "يقدم هذا الموضوع نظرة عامة على سير عمل الاشتراك."
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b4872c0753b54bdddf2c7778a13819726eea4a90
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---


# <a name="subscription-workflow-overview"></a><span data-ttu-id="2dab0-103">نظرة عامة على سير عمل الاشتراك</span><span class="sxs-lookup"><span data-stu-id="2dab0-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2dab0-104">تعمل كمسؤول عن الاشتراكات لدى شركة إضاءة والتي تقدم اشتراكات لصيانة معدات الإضاءة.</span><span class="sxs-lookup"><span data-stu-id="2dab0-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="2dab0-105">ويتصل أحد العملاء بشركتك لشراء اشتراك سنوي للحصول على صيانة معدات الإضاءة.</span><span class="sxs-lookup"><span data-stu-id="2dab0-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="2dab0-106">إعداد الاشتراكات</span><span class="sxs-lookup"><span data-stu-id="2dab0-106">Setting up subscriptions</span></span>

<span data-ttu-id="2dab0-107">لإعداد اشتراك، يجب عليك أولا إنشاء مجموعة مشتركين لاتفاقية الخدمة الجديدة أو التحقق من وجود مجموعة مشتركين.</span><span class="sxs-lookup"><span data-stu-id="2dab0-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="2dab0-108">في حالة وجود مجموعة مشتركين، يجب إعدادها لإرسال فواتير للعميل سنويًا واستحقاق إيرادات المبيعات في كل شهر على مدار السنة.</span><span class="sxs-lookup"><span data-stu-id="2dab0-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="2dab0-109">للحصول على مزيد من المعلومات حول كيفية إعداد الاشتراكات، راجع [إعداد مجموعات الاشتراك](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="2dab0-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="2dab0-110">يُمكنك إنشاء الاشتراك بعد إنشاء مجموعة المشتركين.</span><span class="sxs-lookup"><span data-stu-id="2dab0-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="2dab0-111">للحصول على مزيد من المعلومات حول كيفية إنشاء اشتراكات الخدمة، راجع [إنشاء اشتراكات خدمة من مجموعة اشتراك](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="2dab0-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="2dab0-112">إنشاء حركات المشتركين وتعديلها</span><span class="sxs-lookup"><span data-stu-id="2dab0-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="2dab0-113">بعد إنشاء الاشتراك، يمكنك إنشاء حركة رسوم اشتراك لفترة الفوترة الأولى، والتي تبلغ عام واحد.</span><span class="sxs-lookup"><span data-stu-id="2dab0-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="2dab0-114">تكون الحركات من نوع **عادي**.</span><span class="sxs-lookup"><span data-stu-id="2dab0-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="2dab0-115">لذلك، يمكنك فقط إنشاء حركات الاشتراك التي يتوافق فيها من تاريخ والي تاريخ مع الفترات التي تم إنشاؤها مسبقاً في النموذج **أنواع الفترات**.</span><span class="sxs-lookup"><span data-stu-id="2dab0-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="2dab0-116">لمزيد من المعلومات حول حركات الرسوم، راجع [إنشاء حركات رسوم الاشتراك](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="2dab0-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="2dab0-117">بعد قيامك بإعداد اشتراك لعميلك، تتذكر أنه تفاوض للحصول على خصم يصل إلى 10 في المائة على كافة أسعار عروض الخدمة بالقائمة.</span><span class="sxs-lookup"><span data-stu-id="2dab0-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="2dab0-118">وبالتالي، يجب عليك تخفيض سعر رسوم الحركة التي قمت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="2dab0-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="2dab0-119">في وقت لاحق من اليوم، تتصل جهة الاتصال الخاصة بالعميل لتضيف أنه رغم احتياجهم إلى اتفاقية الخدمة الخاصة بمعدات الإضاءة، فهم يخططون لتقديم معدات إضاءة جديدة فيما بعد خلال العام.</span><span class="sxs-lookup"><span data-stu-id="2dab0-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="2dab0-120">بالتالي، فهم بحاجة فقط إلى تغطية الصيانة حتى أكتوبر 2013.</span><span class="sxs-lookup"><span data-stu-id="2dab0-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="2dab0-121">لتخفيض عدد أشهر اشتراك العميل، قمت بإنشاء حركة رسوم اشتراك جديدة من النوع **أيام التخفيض**.</span><span class="sxs-lookup"><span data-stu-id="2dab0-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="2dab0-122">للحصول على مزيد من المعلومات حول كيفية تقليل الأيام، راجع [تقليل الأيام على رسوم الاشتراك](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="2dab0-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="2dab0-123">فوترة حركات الاشتراك واستحقاقها</span><span class="sxs-lookup"><span data-stu-id="2dab0-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="2dab0-124">لقد انتهيت الآن من إعداد الاشتراك، وأنت مستعد الآن لإرسال الفواتير للعميل مقابله.</span><span class="sxs-lookup"><span data-stu-id="2dab0-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="2dab0-125">للحصول على مزيد من المعلومات حول كيفية فوترة الاشتراكات، راجع [حركات اشتراك الفاتورة](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="2dab0-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="2dab0-126">يتصل العميل بعد مرور يومين ليذكر بأنه يجب فوترة الاشتراك بالدولار الأمريكي، وليس باليورو.</span><span class="sxs-lookup"><span data-stu-id="2dab0-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="2dab0-127">بالتالي، عليك إنشاء إشعار دائن، وعليك إنشاء حركة اشتراك جديدة بالعملة الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="2dab0-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="2dab0-128">للحصول على مزيد من المعلومات حول كيفية ائتمان حركات الاشتراكات، راجع [ائتمان حركات اشتراك](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="2dab0-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="2dab0-129">في نهاية كل شهر، يمكن استحقاق إيراد شهر واحد من اشتراك العميل لحساب الربح والخسارة وحسابات الأعمال تحت التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="2dab0-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="2dab0-130">للحصول على مزيد من المعلومات عن كيفية استحقاق الإيراد للاشتراكات، راجع [إيراد اشتراك مستحق ](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="2dab0-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  



