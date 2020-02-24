---
title: إنشاء عميل افتراضي
description: يوضح هذا الموضوع كيفية إنشاء عميل افتراضي لاستخدامه عند إنشاء قناة في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9e1087821b357c578993cdd5742399c5ec0ecc95
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001796"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="e8a71-103">إنشاء عميل افتراضي</span><span class="sxs-lookup"><span data-stu-id="e8a71-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e8a71-104">يوضح هذا الموضوع كيفية إنشاء عميل افتراضي لاستخدامه عند إنشاء قناة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e8a71-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e8a71-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="e8a71-105">Overview</span></span>

<span data-ttu-id="e8a71-106">عند إنشاء قناة عبر الإنترنت أو البيع بالتجزئة، ستحتاج إلى توفير عميل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="e8a71-106">When creating a retail or online channel, you will need to provide a default customer.</span></span> <span data-ttu-id="e8a71-107">يمكن إنشاء عميلاً افتراضيًا بسهولة بعد إنشاء مجموعة العميل ودفتر عناوين العميل أولاً.</span><span class="sxs-lookup"><span data-stu-id="e8a71-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="e8a71-108">إنشاء مجموعة عميل</span><span class="sxs-lookup"><span data-stu-id="e8a71-108">Create a customer group</span></span>

<span data-ttu-id="e8a71-109">في حالة عدم وجود أي مجموعات للعملاء بعد، يمكنك إنشاء واحدة.</span><span class="sxs-lookup"><span data-stu-id="e8a71-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="e8a71-110">قد تكون الأمثلة مجموعات لتمثيل مجموعات عملاء مختلفة، مثل البيع بالجملة والبيع بالتجزئة والإنترنت والموظفين وما إلى ذلك.</span><span class="sxs-lookup"><span data-stu-id="e8a71-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="e8a71-111">لإنشاء مجموعة عميل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e8a71-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="e8a71-112">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> العملاء \> مجموعات العملاء**.</span><span class="sxs-lookup"><span data-stu-id="e8a71-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="e8a71-113">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e8a71-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e8a71-114">في المربع **مجموعة العميل**، أدخل معرف مجموعة العميل.</span><span class="sxs-lookup"><span data-stu-id="e8a71-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="e8a71-115">في مربع **الوصف**، أدخل وصفًا مناسبًا.</span><span class="sxs-lookup"><span data-stu-id="e8a71-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="e8a71-116">في مربع **شروط الدفع**، أدخل قيمة مناسبة.</span><span class="sxs-lookup"><span data-stu-id="e8a71-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="e8a71-117">في مربع **‏‫الوقت بين تاريخ استحقاق الفاتورة وتاريخ الدفع‬**، أدخل قيمة مناسبة.</span><span class="sxs-lookup"><span data-stu-id="e8a71-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="e8a71-118">في مربع **مجموعة الضريبة الافتراضية**، أدخل مجموعة ضريبة إن وجدت.</span><span class="sxs-lookup"><span data-stu-id="e8a71-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="e8a71-119">حدد خانة الاختيار **الأسعار شاملة ضريبة المبيعات** إن وجدت.</span><span class="sxs-lookup"><span data-stu-id="e8a71-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="e8a71-120">في المربع **‏‫سبب الإلغاء الافتراضي‬**، أدخل قيمة مناسبة إن وجد.</span><span class="sxs-lookup"><span data-stu-id="e8a71-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="e8a71-121">تعرض الصورة التالية العديد من مجموعات العملاء التي تم تكوينها.</span><span class="sxs-lookup"><span data-stu-id="e8a71-121">The following image shows several configured customer groups.</span></span>

![مجموعات العملاء](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="e8a71-123">إنشاء دفتر عناوين للعميل.</span><span class="sxs-lookup"><span data-stu-id="e8a71-123">Create a customer address book</span></span>

<span data-ttu-id="e8a71-124">يجب إقران العميل بدفتر عناوين.</span><span class="sxs-lookup"><span data-stu-id="e8a71-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="e8a71-125">إذا لم يتم إنشاء دفتر عناوين بعد، ستحتاج إلى إنشاء واحدًا.</span><span class="sxs-lookup"><span data-stu-id="e8a71-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="e8a71-126">لإنشاء دفتر عناوين عميل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e8a71-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="e8a71-127">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> دفاتر العناوين**.</span><span class="sxs-lookup"><span data-stu-id="e8a71-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="e8a71-128">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e8a71-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e8a71-129">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="e8a71-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="e8a71-130">في مربع **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="e8a71-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="e8a71-131">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e8a71-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="e8a71-132">تعرض الصورة التالية مثالاً لدفتر عناوين.</span><span class="sxs-lookup"><span data-stu-id="e8a71-132">The following image shows an example address book.</span></span>

![دفتر العناوين](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="e8a71-134">إنشاء عميل افتراضي</span><span class="sxs-lookup"><span data-stu-id="e8a71-134">Create a default customer</span></span>

<span data-ttu-id="e8a71-135">لإنشاء عميل افتراضي، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e8a71-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="e8a71-136">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> العملاء \> كل العملاء**.</span><span class="sxs-lookup"><span data-stu-id="e8a71-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="e8a71-137">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e8a71-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e8a71-138">من القائمة المنسدلة **النوع** حدد "شخص".</span><span class="sxs-lookup"><span data-stu-id="e8a71-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="e8a71-139">في القائمة المنسدلة **حساب العميل**، حدد رقم حساب أو أدخله (على سبيل المثال، "100001").</span><span class="sxs-lookup"><span data-stu-id="e8a71-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="e8a71-140">في القائمة المنسدلة **الاسم الأول**، حدد اسمًا أو أدخله (على سبيل المثال، "الافتراضي").</span><span class="sxs-lookup"><span data-stu-id="e8a71-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="e8a71-141">في القائمة المنسدلة **الاسم الأوسط**، حدد اسمًا أو أدخله (على سبيل المثال، "البيع بالتجزئة").</span><span class="sxs-lookup"><span data-stu-id="e8a71-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="e8a71-142">في القائمة المنسدلة **الاسم الأخير**، حدد اسمًا أو أدخله (على سبيل المثال، "العميل").</span><span class="sxs-lookup"><span data-stu-id="e8a71-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="e8a71-143">في القائمة المنسدلة **العملة**، حدد عملة أو أدخلها (على سبيل المثال، "دولار أمريكي").</span><span class="sxs-lookup"><span data-stu-id="e8a71-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="e8a71-144">في القائمة المنسدلة **العملة**، حدد مجموعة العملاء التي تم إنشاؤها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="e8a71-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="e8a71-145">في القائمة المنسدلة **دفاتر العناوين**، حدد دفتر عناوين عميل موجود.</span><span class="sxs-lookup"><span data-stu-id="e8a71-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="e8a71-146">حدد **حفظ** للحفظ والرجوع إلى شاشة تفاصيل العميل للعميل الجديد.</span><span class="sxs-lookup"><span data-stu-id="e8a71-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="e8a71-147">ليس من الضروري إضافة عنوان لعميل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="e8a71-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="e8a71-148">تعرض الصورة التالية مثالاً لإنشاء عميل.</span><span class="sxs-lookup"><span data-stu-id="e8a71-148">The following image shows an example of customer creation.</span></span>

![إنشاء عميل افتراضي](media/default-customer-creation.png)

<span data-ttu-id="e8a71-150">تظهر الصورة التالية تكوين عميل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="e8a71-150">The following image shows a default customer configuration.</span></span>

![عينة تكوين عميل](media/default-customer-configuration1.png)

<span data-ttu-id="e8a71-152">يمكن أن تبقى معظم القيم الافتراضية على شاشة تفاصيل العميل، ولكن يجب تغيير قيمتين.</span><span class="sxs-lookup"><span data-stu-id="e8a71-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="e8a71-153">من شاشة تفاصيل العميل، وسَّع **إعدادات أوامر المبيعات الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="e8a71-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="e8a71-154">من القائمة المنسدلة **الموقع**، حدد موقعًا تم تكوينه مسبقًا أو أدخله.</span><span class="sxs-lookup"><span data-stu-id="e8a71-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="e8a71-155">في القائمة المنسدلة **المستودع**، حدد مستودعًا تم تكوينه مسبقًا أو أدخله.</span><span class="sxs-lookup"><span data-stu-id="e8a71-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="e8a71-156">تعرض الصورة التالية مثالاً لتكوين عميل.</span><span class="sxs-lookup"><span data-stu-id="e8a71-156">The following image shows an example customer configuration.</span></span>

![مثال تكوين عميل](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="e8a71-158">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e8a71-158">Additional resources</span></span>

[<span data-ttu-id="e8a71-159">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="e8a71-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e8a71-160">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="e8a71-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)
