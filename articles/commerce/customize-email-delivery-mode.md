---
title: تخصيص رسائل البريد الإلكتروني للحركات حسب وضع التسليم
description: يوضح هذا الموضوع كيفية إعداد قوالب بريد إلكتروني مخصصة لأنواع إخطارات معينة وأنماط التسليم في Microsoft Dynamics 365 Commerce.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: d0d96ddb20b2b09751d8c0c0bf8af713de35279a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222623"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="f65c4-103">تخصيص رسائل البريد الكتروني للحركات بحسب وضع التسليم</span><span class="sxs-lookup"><span data-stu-id="f65c4-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f65c4-104">يوضح هذا الموضوع كيفية إعداد قوالب بريد إلكتروني مخصصة لأنواع إخطارات معينة وأنماط التسليم في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f65c4-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f65c4-105">يمكن الآن تخصيص رسائل البريد الإلكتروني الخاصة بالحركات لمجموعة من نوع الأخطار (على سبيل المثال، **تم إنشاء الأمر** أو **تم تعبئة الأمر** أو **تم إصدار فاتورة الأمر**) ووضع التسليم‬ (على سبيل المثال، ليلاً، أو الاستلام من المتجر، أو الاستلام من جانب الرصيف).</span><span class="sxs-lookup"><span data-stu-id="f65c4-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="f65c4-106">تتيح رسائل البريد الإلكتروني للحركات المخصصة لبائعي التجزئة تزويد عملائهم بتجارب تنفيذ مصممة خصيصًا لوضع تسليم الأمر.</span><span class="sxs-lookup"><span data-stu-id="f65c4-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="f65c4-107">علي سبيل المثال، يمكن تخصيص الحدث "تم تعبئة الأمر" بحيث يوفر إرشادات الاستلام من جانب الرصيف للعملاء الذين يختارون الاستلام من جانب الرصيف.</span><span class="sxs-lookup"><span data-stu-id="f65c4-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="f65c4-108">وبدلاً من ذلك، يمكنه توفير معلومات شركة الشحن والتسليم للعملاء الذين يختارون شحن أوامرهم.</span><span class="sxs-lookup"><span data-stu-id="f65c4-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="f65c4-109">لاستخدام وظيفة رسائل البريد الكتروني للحركات المخصصة، يتعين أولاً تشغيل ميزة **تخصيص قوالب البريد الكتروني للحركات حسب وضع التسليم** من خلال الانتقال إلى **مساحات العمل \> إدارة الميزات** في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="f65c4-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="f65c4-110">يمكن تخصيص رسائل البريد الالكتروني بحسب وضع التسليم لأنواع الإخطارات التالية:</span><span class="sxs-lookup"><span data-stu-id="f65c4-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="f65c4-111">**إلغاء الأمر** – يكون نوع إخطار هذا البريد الإلكتروني جديد.</span><span class="sxs-lookup"><span data-stu-id="f65c4-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="f65c4-112">**تم إنشاء الأمر**</span><span class="sxs-lookup"><span data-stu-id="f65c4-112">**Order created**</span></span>
- <span data-ttu-id="f65c4-113">**تم تأكيد الأمر**</span><span class="sxs-lookup"><span data-stu-id="f65c4-113">**Order confirmed**</span></span>
- <span data-ttu-id="f65c4-114">**تم إصدار فاتورة الأمر** – يكون نوع إخطار هذا البريد الإلكتروني جديد.</span><span class="sxs-lookup"><span data-stu-id="f65c4-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="f65c4-115">ويمكن استخدامه بدلاً من نوع الإخطار **تم شحن الأمر** الذي سيرسل إخطارًا لأي حدث فاتورة يشتمل على طريقة الشحن للتسليم (لم يتم الاستلام، أو التنفيذ أو وضع التسليم الإلكتروني).</span><span class="sxs-lookup"><span data-stu-id="f65c4-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="f65c4-116">**تم انتقاء الأمر**</span><span class="sxs-lookup"><span data-stu-id="f65c4-116">**Order picked**</span></span>
- <span data-ttu-id="f65c4-117">**تم تعبئة الأمر**</span><span class="sxs-lookup"><span data-stu-id="f65c4-117">**Order packed**</span></span>
- <span data-ttu-id="f65c4-118">**الأمر جاهز للانتقاء** – يمكن تخصيص نوع الإخطار هذا بحسب وضع التسليم فقط في حالة تشغيل ميزة **دعم أوضاع الانتقاء المتعددة**.</span><span class="sxs-lookup"><span data-stu-id="f65c4-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="f65c4-119">في هذه الحالة، يكون نوع الاخطار هذا مساويًا تمامًا لنوع الإخطار **تمت تعبئة الأمر**.</span><span class="sxs-lookup"><span data-stu-id="f65c4-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="f65c4-120">**فشل الدفع**</span><span class="sxs-lookup"><span data-stu-id="f65c4-120">**Payment failed**</span></span>
- <span data-ttu-id="f65c4-121">**تم إنشاء أمر الاستبدال**</span><span class="sxs-lookup"><span data-stu-id="f65c4-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="f65c4-122">تكوين قوالب البريد الكتروني لأوضاع التسليم المحددة</span><span class="sxs-lookup"><span data-stu-id="f65c4-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="f65c4-123">بالنسبة لهذا الإجراء، فان الافتراض هو أنك قمت بالفعل بإنشاء قوالب بريد الكتروني جديدة ومخصصة وإضافتها إلى صفحة **قوالب البريد الكتروني للمؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="f65c4-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="f65c4-124">للحصول علي معلومات حول كيفية إنشاء قوالب البريد الكتروني وتحميلها، راجع [إنشاء قوالب بريد الكتروني لأحداث الحركات](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="f65c4-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="f65c4-125">لتكوين قوالب البريد الكتروني لأوضاع تسليم محددة في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f65c4-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f65c4-126">انتقل إلى **ملف تعريف اخطار البريد الإلكتروني لـ Commerce**.</span><span class="sxs-lookup"><span data-stu-id="f65c4-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="f65c4-127">ضمن **إعدادات إخطار حدث البيع بالتجزئة**، حدد نوع الإخطار الحالي.</span><span class="sxs-lookup"><span data-stu-id="f65c4-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="f65c4-128">بينما لا يزال نوع الإخطار محددًا، حدد **تكوين أوضاع التسليم**.</span><span class="sxs-lookup"><span data-stu-id="f65c4-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="f65c4-129">في مربع الحوار **أوضاع التسليم** ، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f65c4-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="f65c4-130">في الصف الجديد، في الحقل **وضع التسليم** ، حدد وضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="f65c4-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="f65c4-131">في الحقل **معرف البريد الإلكتروني** ، حدد قالب البريد الإلكتروني لتعيينه إلى وضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="f65c4-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="f65c4-132">حدد خانة الاختيار **نشط**.</span><span class="sxs-lookup"><span data-stu-id="f65c4-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="f65c4-133">كرر الخطوات من 4 إلى 7 لإضافة المزيد من أوضاع التسليم.</span><span class="sxs-lookup"><span data-stu-id="f65c4-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="f65c4-134">عند الانتهاء، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f65c4-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="f65c4-135">عند وجود أكثر من وضع تسليم واحد عبر البنود في أمر المبيعات، سيتم استخدام القالب الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="f65c4-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="f65c4-136">القالب الافتراضي هو القالب الذي يتم تعيينه إلى نوع الإخطار في صفحة **ملف تعريف إخطار البريد الكتروني لـ Commerce**.</span><span class="sxs-lookup"><span data-stu-id="f65c4-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="f65c4-137">إذا كان أمر المبيعات يحتوي علي وضع تسليم لم يتم تكوينه لقالب بريد الكتروني مخصص، سيتم استخدام قالب البريد الالكتروني الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="f65c4-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f65c4-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f65c4-138">Additional resources</span></span>

[<span data-ttu-id="f65c4-139">إنشاء أوامر مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="f65c4-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="f65c4-140">تغيير ‏‫وضع التسليم‬ في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="f65c4-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]