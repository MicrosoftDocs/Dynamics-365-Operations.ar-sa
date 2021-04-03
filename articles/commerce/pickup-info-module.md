---
title: الوحدة النمطية لمعلومات الالتقاط
description: يتناول هذا الموضوع الوحدة النمطية لمعلومات الالتقاط ويوضح كيفية إضافتها إلى صفحات السداد مع الخروج في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 222e8ad79b30e5197f7140958309d442b284f286
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263170"
---
# <a name="pickup-information-module"></a><span data-ttu-id="fbc16-103">الوحدة النمطية لمعلومات الاستلام</span><span class="sxs-lookup"><span data-stu-id="fbc16-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fbc16-104">يتناول هذا الموضوع الوحدة النمطية لمعلومات الالتقاط ويوضح كيفية إضافتها إلى صفحات السداد مع الخروج في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fbc16-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fbc16-105">يمكن استخدام الوحدة النمطية لمعلومات الالتقاط في الوحدة النمطية للسداد والخروج لإظهار معلومات التقاط الأمر.</span><span class="sxs-lookup"><span data-stu-id="fbc16-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="fbc16-106">يمكن للعملاء عرض تواريخ الالتقاط والفترات الزمنية المتاحة، ثم تحديد الوقت المناسب لالتقاط أوامرهم.</span><span class="sxs-lookup"><span data-stu-id="fbc16-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="fbc16-107">على سبيل المثال، يمكن للعميل اختيار التقاط أمر الساعة 3 مساءً يوم 21 مارس من متجر سان فرانسيسكو.</span><span class="sxs-lookup"><span data-stu-id="fbc16-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="fbc16-108">يجب تكوين فترات زمنية للالتقاط للمخازن المناسبة في المراكز الرئيسية لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="fbc16-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="fbc16-109">لمزيد من المعلومات، راجع [إنشاء فترات زمنية لالتقاط العميل وتحديثها](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="fbc16-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="fbc16-110">إذا تم إنشاء الوحدة النمطية لمعلومات الالتقاط في صفحة السداد مع الخروج، ولكن دون تحديد فترات زمنية للمخزن الذي تم تحديده للالتقاط، فستعرض الوحدة النمطية معلومات، ولكن لن يتمكن المستخدم من تحديد أي فترات زمنية.</span><span class="sxs-lookup"><span data-stu-id="fbc16-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="fbc16-111">تكون الفترات الزمنية اختيارية ولا يلزم إنشاء أمر.</span><span class="sxs-lookup"><span data-stu-id="fbc16-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="fbc16-112">إذا تم تحديد العديد من العناصر للالتقاط عبر متاجر متعددة، فإن الوحدة النمطية لمعلومات الالتقاط ستتيح للمستخدم تحديد فترة زمنية لكل متجر، بشرط توفر فترات زمنية له.</span><span class="sxs-lookup"><span data-stu-id="fbc16-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="fbc16-113">يتوفر الدعم للفترات الزمنية والوحدة النمطية لمعلومات الالتقاط في Dynamics 365 Commerce الإصدار 10.0.15 والإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="fbc16-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="fbc16-114">يبين الرسم التوضيحي مثالاً على تحديد الفترة الزمنية من خلال الوحدة النمطية لمعلومات الالتقاط في صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="fbc16-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![مثال عن الوحدة النمطية لمعلومات الالتقاط على صفحة السداد مع الخروج](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="fbc16-116">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="fbc16-116">Module properties</span></span>

- <span data-ttu-id="fbc16-117">**العنوان** - أدخل عنوانًا للوحدة.</span><span class="sxs-lookup"><span data-stu-id="fbc16-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="fbc16-118">إظهار معلومات الفترة الزمنية بعد إنشاء الأمر</span><span class="sxs-lookup"><span data-stu-id="fbc16-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="fbc16-119">بعد إنشاء الطلب، يمكن الاطلاع على معلومات حول الفترة الزمنية المحددة في [الوحدة النمطية لتأكيد الأمر](order-confirmation-module.md) و [الوحدة النمطية لتفاصيل الأمر](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="fbc16-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="fbc16-120">تحتوي كلتا الوحدتين النمطيتين على خاصية **‏‫إظهار معلومات الفترة الزمنية**.</span><span class="sxs-lookup"><span data-stu-id="fbc16-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="fbc16-121">قبل أن يتمكنوا من إظهار الفترة الزمنية المحددة أثناء معالجة الأمر، يجب تعيين هذه الخاصية إلى **صحيح**.</span><span class="sxs-lookup"><span data-stu-id="fbc16-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="fbc16-122">إضافة الوحدة النمطية لمعلومات الالتقاط على صفحة السداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="fbc16-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="fbc16-123">للحصول على إرشادات حول كيفية إضافة الوحدة النمطية لمعلومات الالتقاط إلى صفحة السداد مع الخروج‬ وتعيين الخصائص المطلوبة، راجع [الوحدة النمطية للسداد مع الخروج](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="fbc16-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="fbc16-124">يبين الرسم التوضيحي التالي مثالاً على صفحة السداد مع الخروج من التجارة الإلكترونية التي تتضمن فترات زمنية لعناصر بند الالتقاط.</span><span class="sxs-lookup"><span data-stu-id="fbc16-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![مثال على صفحة السداد مع الخروج من التجارة الإلكترونية التي تتضمن فترات زمنية لعناصر بند الالتقاط](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="fbc16-126">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fbc16-126">Additional resources</span></span>

[<span data-ttu-id="fbc16-127">‬‏‫إنشاء فترات زمنية لالتقاط العميل وتحديثها</span><span class="sxs-lookup"><span data-stu-id="fbc16-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="fbc16-128">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="fbc16-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fbc16-129">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="fbc16-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fbc16-130">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="fbc16-130">Order details module</span></span>](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]