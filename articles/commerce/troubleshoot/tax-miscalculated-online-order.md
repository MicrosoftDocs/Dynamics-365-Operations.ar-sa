---
title: حساب الضرائب على الأوامر عبر الإنترنت بشكل غير صحيح
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حال حساب الضرائب على الأوامر عبر الإنترنت بشكل غير صحيح، أو عند تعيين مجموعة الضريبة في بند المبيعات بشكل غير صحيح.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7f71add679e1d24f80db8ce3990058b591128ec1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801401"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="0f655-103">حساب الضرائب على الأوامر عبر الإنترنت بشكل غير صحيح</span><span class="sxs-lookup"><span data-stu-id="0f655-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f655-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حال حساب الضرائب على الأوامر عبر الإنترنت بشكل غير صحيح، أو عند تعيين مجموعة الضريبة في بند المبيعات بشكل غير صحيح.</span><span class="sxs-lookup"><span data-stu-id="0f655-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="0f655-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="0f655-105">Description</span></span>

<span data-ttu-id="0f655-106">عند تقديم أمر تجارة إلكترونية، يتم حساب الضرائب بشكل غير صحيح، أو تعيين مجموعة الضريبة في بند المبيعات بشكل غير صحيح.</span><span class="sxs-lookup"><span data-stu-id="0f655-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="0f655-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="0f655-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="0f655-108">تكوين ضريبة المبيعات لمتجر البيع بالتجزئة في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="0f655-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="0f655-109">لتكوين ضريبة المبيعات لمتجر البيع بالتجزئة في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0f655-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0f655-110">انتقل إلى **Retail وCommerce \> القنوات \> جميع المتاجر**.</span><span class="sxs-lookup"><span data-stu-id="0f655-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="0f655-111">حدد المتجر لتكوين ضريبة المبيعات الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="0f655-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="0f655-112">في علامة التبويب السريعة **عام**، في قسم **ضريبة المبيعات**، قم بتكوين معلومات ضريبة المبيعات للمتجر.</span><span class="sxs-lookup"><span data-stu-id="0f655-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="0f655-113">بالنسبة لانتقاء المنتج من المتجر، تأتي مجموعة الضريبة من المتجر المحدد للالتقاط.</span><span class="sxs-lookup"><span data-stu-id="0f655-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="0f655-114">لمزيد من المعلومات، راجع [تعيين خيارات ضريبة أخرى للمتاجر](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="0f655-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="0f655-115">تكوين ضريبة المبيعات لعنوان العميل في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="0f655-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="0f655-116">لتكوين ضريبة المبيعات لعنوان عميل في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0f655-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0f655-117">انتقل إلى **الحسابات المدينة \> العملاء \> كافة العملاء**.</span><span class="sxs-lookup"><span data-stu-id="0f655-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="0f655-118">حدد العميل المراد تكوين ضرائب مبيعات له.</span><span class="sxs-lookup"><span data-stu-id="0f655-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="0f655-119">في علامة التبويب السريعة **العناوين**، حدد عنوانًا لتكوين ضرائب المبيعات له، وحدد **مزيد من الخيارات**، ثم حدد **متقدم**.</span><span class="sxs-lookup"><span data-stu-id="0f655-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="0f655-120">في علامة التبويب السريعة **عام**، **مجموعة الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="0f655-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="0f655-121">في  حقل **ضريبة المبيعات**، حدد القيمة الملائمة.</span><span class="sxs-lookup"><span data-stu-id="0f655-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="0f655-122">بالنسبة للشحن الذي يتضمن ضريبة مبيعات على عنوان العميل، فإن عنوان تسليم البند يحدد مجموعة الضريبة للبند.</span><span class="sxs-lookup"><span data-stu-id="0f655-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="0f655-123">إذا كان العميل يقوم بالشحن إلى عنوان تم تكوين مجموعة ضرائب له بالفعل، سيتم استخدام مجموعة الضرائب الموجودة.</span><span class="sxs-lookup"><span data-stu-id="0f655-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="0f655-124">بشكل افتراضي، لا تحتوي العناوين على مجموعة ضرائب عند إنشائها.</span><span class="sxs-lookup"><span data-stu-id="0f655-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="0f655-125">تكوين مجموعات ضريبة المبيعات العامة في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="0f655-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="0f655-126">لتكوين مجموعات ضريبة المبيعات العامة في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0f655-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0f655-127">انتقل إلى **الضريبة‬ \> ضرائب غير مباشرة‬ \> ضريبة المبيعات \> مجموعة ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="0f655-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="0f655-128">في شريط التنقل الأيسر، حدد مجموعة الضريبة المطلوب تكوينها.</span><span class="sxs-lookup"><span data-stu-id="0f655-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="0f655-129">في علامة التبويب السريعة **الضرائب المستندة إلى وجهة البيع بالتجزئة**، قم بتكوين الضرائب لمجموعة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="0f655-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="0f655-130">بالنسبة للشحن الذي لا يتضمن ضريبة مبيعات على عنوان العميل، فإن عنوان تسليم البند والضرائب المستندة إلى الوجهة التي تم تكوينها لمجموعه الضريبة تحدد مجموعة الضريبة.</span><span class="sxs-lookup"><span data-stu-id="0f655-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="0f655-131">لمزيد من المعلومات، راجع [‏‫إعداد الضرائب للمتاجر على الإنترنت مستندة إلى الوجهة‬](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="0f655-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f655-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0f655-132">Additional resources</span></span>

[<span data-ttu-id="0f655-133">تكوين ضريبة المبيعات للأوامر عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="0f655-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)