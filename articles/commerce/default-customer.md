---
title: إنشاء عميل افتراضي
description: يوضح هذا الموضوع كيفية إنشاء عميل افتراضي لاستخدامه عند إنشاء قناة في Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ecdf4e5618d3397527bf83977857fbe3f8dbb265
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799169"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="17fce-103">إنشاء عميل افتراضي</span><span class="sxs-lookup"><span data-stu-id="17fce-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17fce-104">يوضح هذا الموضوع كيفية إنشاء عميل افتراضي لاستخدامه عند إنشاء قناة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="17fce-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="17fce-105">عند إنشاء قناة، ستحتاج إلى توفير عميل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="17fce-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="17fce-106">يمكن إنشاء عميلاً افتراضيًا بسهولة بعد إنشاء مجموعة العميل ودفتر عناوين العميل أولاً.</span><span class="sxs-lookup"><span data-stu-id="17fce-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="17fce-107">إنشاء مجموعة عميل</span><span class="sxs-lookup"><span data-stu-id="17fce-107">Create a customer group</span></span>

<span data-ttu-id="17fce-108">في حالة عدم وجود أي مجموعات للعملاء بعد، يمكنك إنشاء واحدة.</span><span class="sxs-lookup"><span data-stu-id="17fce-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="17fce-109">قد تكون الأمثلة مجموعات لتمثيل مجموعات عملاء مختلفة، مثل البيع بالجملة والبيع بالتجزئة والإنترنت والموظفين وما إلى ذلك.</span><span class="sxs-lookup"><span data-stu-id="17fce-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="17fce-110">لإنشاء مجموعة عميل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="17fce-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="17fce-111">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> العملاء \> مجموعات العملاء**.</span><span class="sxs-lookup"><span data-stu-id="17fce-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="17fce-112">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="17fce-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="17fce-113">في المربع **مجموعة العميل**، أدخل معرف مجموعة العميل.</span><span class="sxs-lookup"><span data-stu-id="17fce-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="17fce-114">في مربع **الوصف**، أدخل وصفًا مناسبًا.</span><span class="sxs-lookup"><span data-stu-id="17fce-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="17fce-115">في مربع **شروط الدفع**، أدخل قيمة مناسبة.</span><span class="sxs-lookup"><span data-stu-id="17fce-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="17fce-116">في مربع **‏‫الوقت بين تاريخ استحقاق الفاتورة وتاريخ الدفع‬**، أدخل قيمة مناسبة.</span><span class="sxs-lookup"><span data-stu-id="17fce-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="17fce-117">في مربع **مجموعة الضريبة الافتراضية**، أدخل مجموعة ضريبة إن وجدت.</span><span class="sxs-lookup"><span data-stu-id="17fce-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="17fce-118">حدد خانة الاختيار **الأسعار شاملة ضريبة المبيعات** إن وجدت.</span><span class="sxs-lookup"><span data-stu-id="17fce-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="17fce-119">في المربع **‏‫سبب الإلغاء الافتراضي‬**، أدخل قيمة مناسبة إن وجد.</span><span class="sxs-lookup"><span data-stu-id="17fce-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="17fce-120">تعرض الصورة التالية العديد من مجموعات العملاء التي تم تكوينها.</span><span class="sxs-lookup"><span data-stu-id="17fce-120">The following image shows several configured customer groups.</span></span>

![مجموعات العملاء](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="17fce-122">إنشاء دفتر عناوين للعميل.</span><span class="sxs-lookup"><span data-stu-id="17fce-122">Create a customer address book</span></span>

<span data-ttu-id="17fce-123">يجب إقران العميل بدفتر عناوين.</span><span class="sxs-lookup"><span data-stu-id="17fce-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="17fce-124">إذا لم يتم إنشاء دفتر عناوين بعد، ستحتاج إلى إنشاء واحدًا.</span><span class="sxs-lookup"><span data-stu-id="17fce-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="17fce-125">لإنشاء دفتر عناوين عميل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="17fce-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="17fce-126">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> دفاتر العناوين**.</span><span class="sxs-lookup"><span data-stu-id="17fce-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="17fce-127">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="17fce-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="17fce-128">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="17fce-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="17fce-129">في مربع **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="17fce-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="17fce-130">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="17fce-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="17fce-131">تعرض الصورة التالية مثالاً لدفتر عناوين.</span><span class="sxs-lookup"><span data-stu-id="17fce-131">The following image shows an example address book.</span></span>

![دفتر العناوين](media/address-book.png)

## <a name="create-a-default-customer&quot;></a><span data-ttu-id=&quot;17fce-133&quot;>إنشاء عميل افتراضي</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;17fce-133&quot;>Create a default customer</span></span>

<span data-ttu-id=&quot;17fce-134&quot;>لإنشاء عميل افتراضي، اتبع الخطوات التالية.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;17fce-134&quot;>To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id=&quot;17fce-135&quot;>في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> العملاء \> كل العملاء**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;17fce-135&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id=&quot;17fce-136&quot;>في جزء الإجراءات، حدد **جديد**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;17fce-136&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;17fce-137&quot;>من القائمة المنسدلة **النوع** حدد &quot;شخص&quot;.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;17fce-137&quot;>In the **Type** drop-down list, select &quot;Person&quot;.</span></span>
1. <span data-ttu-id=&quot;17fce-138&quot;>في القائمة المنسدلة **حساب العميل**، حدد رقم حساب أو أدخله (على سبيل المثال، &quot;100001").</span><span class="sxs-lookup"><span data-stu-id="17fce-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="17fce-139">في القائمة المنسدلة **الاسم الأول**، حدد اسمًا أو أدخله (على سبيل المثال، "الافتراضي").</span><span class="sxs-lookup"><span data-stu-id="17fce-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="17fce-140">في القائمة المنسدلة **الاسم الأوسط**، حدد اسمًا أو أدخله (على سبيل المثال، "البيع بالتجزئة").</span><span class="sxs-lookup"><span data-stu-id="17fce-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="17fce-141">في القائمة المنسدلة **الاسم الأخير**، حدد اسمًا أو أدخله (على سبيل المثال، "العميل").</span><span class="sxs-lookup"><span data-stu-id="17fce-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="17fce-142">في القائمة المنسدلة **العملة**، حدد عملة أو أدخلها (على سبيل المثال، "دولار أمريكي").</span><span class="sxs-lookup"><span data-stu-id="17fce-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="17fce-143">في القائمة المنسدلة **العملة**، حدد مجموعة العملاء التي تم إنشاؤها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="17fce-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="17fce-144">في القائمة المنسدلة **دفاتر العناوين**، حدد دفتر عناوين عميل موجود.</span><span class="sxs-lookup"><span data-stu-id="17fce-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="17fce-145">حدد **حفظ** للحفظ والرجوع إلى شاشة تفاصيل العميل للعميل الجديد.</span><span class="sxs-lookup"><span data-stu-id="17fce-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="17fce-146">ليس من الضروري إضافة عنوان لعميل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="17fce-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="17fce-147">تعرض الصورة التالية مثالاً لإنشاء عميل.</span><span class="sxs-lookup"><span data-stu-id="17fce-147">The following image shows an example of customer creation.</span></span>

![إنشاء عميل افتراضي](media/default-customer-creation.png)

<span data-ttu-id="17fce-149">تظهر الصورة التالية تكوين عميل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="17fce-149">The following image shows a default customer configuration.</span></span>

![عينة تكوين عميل](media/default-customer-configuration1.png)

<span data-ttu-id="17fce-151">يمكن أن تبقى معظم القيم الافتراضية على شاشة تفاصيل العميل، ولكن يجب تغيير قيمتين.</span><span class="sxs-lookup"><span data-stu-id="17fce-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="17fce-152">من شاشة تفاصيل العميل، وسَّع **إعدادات أوامر المبيعات الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="17fce-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="17fce-153">من القائمة المنسدلة **الموقع**، حدد موقعًا تم تكوينه مسبقًا أو أدخله.</span><span class="sxs-lookup"><span data-stu-id="17fce-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="17fce-154">في القائمة المنسدلة **المستودع**، حدد مستودعًا تم تكوينه مسبقًا أو أدخله.</span><span class="sxs-lookup"><span data-stu-id="17fce-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="17fce-155">تعرض الصورة التالية مثالاً لتكوين عميل.</span><span class="sxs-lookup"><span data-stu-id="17fce-155">The following image shows an example customer configuration.</span></span>

![مثال تكوين عميل](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="17fce-157">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="17fce-157">Additional resources</span></span>

[<span data-ttu-id="17fce-158">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="17fce-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="17fce-159">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="17fce-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
