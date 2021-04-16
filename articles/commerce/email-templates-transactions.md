---
title: إنشاء قوالب بريد إلكتروني لأحداث الحركات
description: يوضح هذا الموضوع كيفية إنشاء قوالب بريد إلكتروني وتحميلها وتكوينها لأحداث الحركات في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 55597e83a930fc7d8bcc4c0cf09abc82cb666b25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792621"
---
# <a name="create-email-templates-for-transactional-events"></a><span data-ttu-id="0a914-103">إنشاء قوالب بريد إلكتروني لأحداث المعاملات</span><span class="sxs-lookup"><span data-stu-id="0a914-103">Create email templates for transactional events</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0a914-104">يوضح هذا الموضوع كيفية إنشاء قوالب بريد إلكتروني وتحميلها وتكوينها لأحداث الحركات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0a914-104">This topic describes how to create, upload, and configure email templates for transactional events in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0a914-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="0a914-105">Overview</span></span>

<span data-ttu-id="0a914-106">يوفر Dynamics 365 Commerce حلاً جاهزًا لإرسال رسائل بريد إلكتروني والتي تقوم بتنبيه العملاء حول أحداث الحركات (على سبيل المثال، عند تقديم طلب ما أو عندما يصبح الأمر جاهزًا للالتقاط أو عندما يتم شحن الأمر).</span><span class="sxs-lookup"><span data-stu-id="0a914-106">Dynamics 365 Commerce provides an out-of-box solution for sending emails that alert customers about transactional events (for example, when an order is placed, an order is ready for pickup, or an order has been shipped).</span></span> <span data-ttu-id="0a914-107">يصف هذا الموضوع الخطوات الخاصة بإنشاء قوالب البريد الإلكتروني المستخدمة لإرسال رسائل بريد إلكتروني للحركات وتحميلها وتكوينها.</span><span class="sxs-lookup"><span data-stu-id="0a914-107">This topic describes the steps for creating, uploading, and configuring the email templates that are used to send transactional emails.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="0a914-108">إنشاء قالب بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="0a914-108">Create an email template</span></span>

<span data-ttu-id="0a914-109">قبل أن تتمكن من تعيين حدث حركة معين إلى قالب بريد إلكتروني، يجب عليك إنشاء القالب.</span><span class="sxs-lookup"><span data-stu-id="0a914-109">Before you can map a specific transactional event to an email template, you must create the template.</span></span>

<span data-ttu-id="0a914-110">لإنشاء قالب بريد إلكتروني، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0a914-110">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="0a914-111">في Commerce headquarters، انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> قوالب البريد الإلكتروني للمؤسسة** أو **إدارة المؤسسة \> الإعداد \> قوالب البريد الإلكتروني للمؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="0a914-111">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates** or **Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="0a914-112">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0a914-112">Select **New**.</span></span>
1. <span data-ttu-id="0a914-113">ضمن **عام**، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="0a914-113">Under **General**, set the following fields:</span></span>

    - <span data-ttu-id="0a914-114">**معرف البريد الإلكتروني** – معرف البريد الإلكتروني هو المعرف الفريد للقالب، وهو القيمة التي تظهر عند تحديد قالب لتعيينه إلى حدث.</span><span class="sxs-lookup"><span data-stu-id="0a914-114">**Email ID** – The email ID is the unique identifier for a template, and it's the value that is shown when you select a template to map to an event.</span></span>
    - <span data-ttu-id="0a914-115">**وصف البريد الإلكتروني** – يمكنك استخدام هذا الحقل الاختياري لتوفير وصف للقالب.</span><span class="sxs-lookup"><span data-stu-id="0a914-115">**Email description** – You can use this optional field to provide a description of the template.</span></span> <span data-ttu-id="0a914-116">تظهر القيمة التي تدخلها في Commerce Headquarters فقط.</span><span class="sxs-lookup"><span data-stu-id="0a914-116">The value that you enter appears only in Commerce headquarters.</span></span>
    - <span data-ttu-id="0a914-117">**اسم المرسل** – يظهر الاسم الذي تقوم بإدخاله في الحقل "من" الخاص بمعظم عملاء البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="0a914-117">**Sender name** – The name that you enter appears in the "from" field of most email clients.</span></span>
    - <span data-ttu-id="0a914-118">**البريد الإلكتروني للمرسل** – أدخل عنوان البريد الإلكتروني الذي يجب استخدامه لرسائل البريد الإلكتروني التي يتم إرسالها باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="0a914-118">**Sender email** – Enter the email address that should be used for emails that are sent by using this template.</span></span>
    - <span data-ttu-id="0a914-119">**كود اللغة الافتراضية** – يحدد هذا الحقل الإصدار المترجم من البريد الإلكتروني الذي يتم إرساله افتراضيًا، في حالة عدم توفير لغة بواسطة القناة التي تقوم باستدعاء هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="0a914-119">**Default language code** – This field specifies the localized version of the email that is sent by default, if no language is provided by the channel that invokes this template.</span></span>

1. <span data-ttu-id="0a914-120">ضمن **محتوي رسالة البريد الإلكتروني**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0a914-120">Under **Email message content**, select **New**.</span></span>
1. <span data-ttu-id="0a914-121">في حقل **اللغة**، ادخل اللغة لقالب البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="0a914-121">In the **Language** field, enter the language for the email template.</span></span> <span data-ttu-id="0a914-122">يمكنك إضافة المزيد من اللغات والقوالب المترجمة لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="0a914-122">You can add more languages and localized templates later.</span></span>
1. <span data-ttu-id="0a914-123">في حقل **الموضوع**، أدخل موضوع البريد الإلكتروني الذي يجب أن يظهر في حقل الموضوع الخاص بالبريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="0a914-123">In the **Subject** field, enter the email subject that should appear in the subject field of the email.</span></span>
1. <span data-ttu-id="0a914-124">حدد **تحرير** لتحميل قالب البريد الإلكتروني الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="0a914-124">Select **Edit** to upload your email template.</span></span>

## <a name="create-an-email-message-body-by-using-html"></a><span data-ttu-id="0a914-125">إنشاء نص رسالة بريد إلكتروني باستخدام HTML</span><span class="sxs-lookup"><span data-stu-id="0a914-125">Create an email message body by using HTML</span></span>

<span data-ttu-id="0a914-126">يتم تكوين نص رسالة البريد الإلكتروني الخاصة بك بتنسيق HTML.</span><span class="sxs-lookup"><span data-stu-id="0a914-126">The message body of your email is composed in HTML.</span></span> <span data-ttu-id="0a914-127">يمكنك استخدام أي تخطيط، ونمط، وعلامة تجارية يسمح بها HTML أوراق الأنماط المتتالية المدمجة (CSS).</span><span class="sxs-lookup"><span data-stu-id="0a914-127">You can use any layout, styling, and branding that HTML and inline Cascading Style Sheets (CSS) allow for.</span></span> <span data-ttu-id="0a914-128">يمكنك أيضًا استخدام الصور، إذا قمت باستضافتها على نقطة نهاية ويب متوفرة بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="0a914-128">You can also use images, if you host them on a publicly available web endpoint.</span></span> <span data-ttu-id="0a914-129">لإضافة صورة، أدخل عنوان URL الخاص بالصورة في سمة **src** الخاصة بعلامة **&lt;img&gt;** لـ HTML.</span><span class="sxs-lookup"><span data-stu-id="0a914-129">To add an image, enter the image's URL in the **src** attribute of the HTML **&lt;img&gt;** tag.</span></span>

> [!NOTE]
> <span data-ttu-id="0a914-130">يفرض عملاء البريد الإلكتروني قيودًا على المخطط والنمط قد تتطلب تعديلات على HTML وCSS التي تستخدمها لنص الرسالة.</span><span class="sxs-lookup"><span data-stu-id="0a914-130">Email clients impose layout and style limitations that might require adjustments to the HTML and CSS that you use for the message body.</span></span> <span data-ttu-id="0a914-131">نوصيك بالتعرف على أفضل الممارسات الخاصة بإنشاء HTML الذي يدعمه معظم عملاء البريد الإلكتروني المشهورين.</span><span class="sxs-lookup"><span data-stu-id="0a914-131">We recommend that you familiarize yourself with the best practices for creating HTML that will be supported by the most popular email clients.</span></span>

## <a name="add-placeholders-to-the-email-message-body"></a><span data-ttu-id="0a914-132">إضافة عناصر نائبة إلى نص رسالة البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0a914-132">Add placeholders to the email message body</span></span>

<span data-ttu-id="0a914-133">يمكن أن يحتوي بريدك الإلكتروني على عناصر نائبة يتم استبدالها بقيم خاصة بالعميل وقيم خاصة بالحركات عند إنشاء البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="0a914-133">Your email can contain placeholders that are replaced with customer-specific and transaction-specific values when the email is generated.</span></span> <span data-ttu-id="0a914-134">تكون العناصر النائبة دائمًا محاطة بعلامات النسبة المئوية (%) ويتم إدراجها مباشره في مستند HTML.</span><span class="sxs-lookup"><span data-stu-id="0a914-134">Placeholders are always surrounded by percent signs (%) and are inserted directly into the HTML document.</span></span>

<span data-ttu-id="0a914-135">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="0a914-135">Here is an example.</span></span>

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a><span data-ttu-id="0a914-136">العناصر النائبة للأمر (مستوى أمر المبيعات)</span><span class="sxs-lookup"><span data-stu-id="0a914-136">Order placeholders (sales order level)</span></span>

<span data-ttu-id="0a914-137">تقوم العناصر النائبة التالية باسترداد وإظهار البيانات التي يتم تحديدها في مستوى أمر المبيعات (على عكس مستوى بند المبيعات).</span><span class="sxs-lookup"><span data-stu-id="0a914-137">The following placeholders retrieve and show data that is defined at the sales order level (as opposed to the sales line level).</span></span>

| <span data-ttu-id="0a914-138">اسم العنصر النائب</span><span class="sxs-lookup"><span data-stu-id="0a914-138">Placeholder name</span></span>     | <span data-ttu-id="0a914-139">قيمة العنصر النائب</span><span class="sxs-lookup"><span data-stu-id="0a914-139">Placeholder value</span></span>                                            |
| -------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="0a914-140">customername</span><span class="sxs-lookup"><span data-stu-id="0a914-140">customername</span></span>         | <span data-ttu-id="0a914-141">اسم العميل الذي قام بتقديم الأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-141">The name of the customer who placed the order.</span></span>               |
| <span data-ttu-id="0a914-142">salesid</span><span class="sxs-lookup"><span data-stu-id="0a914-142">salesid</span></span>              | <span data-ttu-id="0a914-143">معرف المبيعات للأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-143">The sales ID of the order.</span></span>                                   |
| <span data-ttu-id="0a914-144">deliveryaddress</span><span class="sxs-lookup"><span data-stu-id="0a914-144">deliveryaddress</span></span>      | <span data-ttu-id="0a914-145">عنوان التسليم الخاص بالأوامر المشحونة.</span><span class="sxs-lookup"><span data-stu-id="0a914-145">The delivery address for shipped orders.</span></span>                     |
| <span data-ttu-id="0a914-146">customeraddress</span><span class="sxs-lookup"><span data-stu-id="0a914-146">customeraddress</span></span>      | <span data-ttu-id="0a914-147">عنوان العميل.</span><span class="sxs-lookup"><span data-stu-id="0a914-147">The address of the customer.</span></span>                                 |
| <span data-ttu-id="0a914-148">customeremailaddress</span><span class="sxs-lookup"><span data-stu-id="0a914-148">customeremailaddress</span></span> | <span data-ttu-id="0a914-149">عنوان البريد الكتروني الذي أدخله العميل عند السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="0a914-149">The email address that the customer entered at checkout.</span></span>     |
| <span data-ttu-id="0a914-150">deliverydate</span><span class="sxs-lookup"><span data-stu-id="0a914-150">deliverydate</span></span>         | <span data-ttu-id="0a914-151">تاريخ التسليم.</span><span class="sxs-lookup"><span data-stu-id="0a914-151">The delivery date.</span></span>                                           |
| <span data-ttu-id="0a914-152">shipdate</span><span class="sxs-lookup"><span data-stu-id="0a914-152">shipdate</span></span>             | <span data-ttu-id="0a914-153">تاريخ الشحن.</span><span class="sxs-lookup"><span data-stu-id="0a914-153">The ship date.</span></span>                                               |
| <span data-ttu-id="0a914-154">modeofdelivery</span><span class="sxs-lookup"><span data-stu-id="0a914-154">modeofdelivery</span></span>       | <span data-ttu-id="0a914-155">وضع التسليم الخاص بالأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-155">The delivery mode of the order.</span></span>                              |
| <span data-ttu-id="0a914-156">التكاليف</span><span class="sxs-lookup"><span data-stu-id="0a914-156">charges</span></span>              | <span data-ttu-id="0a914-157">إجمالي المصاريف الخاصة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-157">The total charges for the order.</span></span>                             |
| <span data-ttu-id="0a914-158">ضريبة</span><span class="sxs-lookup"><span data-stu-id="0a914-158">tax</span></span>                  | <span data-ttu-id="0a914-159">إجمالي الضرائب الخاصة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-159">The total tax for the order.</span></span>                                 |
| <span data-ttu-id="0a914-160">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="0a914-160">total</span></span>                | <span data-ttu-id="0a914-161">المبلغ الإجمالي الخاص بالأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-161">The total amount for the order.</span></span>                              |
| <span data-ttu-id="0a914-162">ordernetamount</span><span class="sxs-lookup"><span data-stu-id="0a914-162">ordernetamount</span></span>       | <span data-ttu-id="0a914-163">المبلغ الإجمالي للأمر، مطروحًا منه إجمالي الضريبة.</span><span class="sxs-lookup"><span data-stu-id="0a914-163">The total amount for the order, minus the total tax.</span></span>         |
| <span data-ttu-id="0a914-164">خصم</span><span class="sxs-lookup"><span data-stu-id="0a914-164">discount</span></span>             | <span data-ttu-id="0a914-165">إجمالي الخصم الخاص بالأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-165">The total discount for the order.</span></span>                            |
| <span data-ttu-id="0a914-166">storename</span><span class="sxs-lookup"><span data-stu-id="0a914-166">storename</span></span>            | <span data-ttu-id="0a914-167">اسم المتجر الذي تم فيه تقديم الأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-167">The name of the store where the order was placed.</span></span>            |
| <span data-ttu-id="0a914-168">storeaddress</span><span class="sxs-lookup"><span data-stu-id="0a914-168">storeaddress</span></span>         | <span data-ttu-id="0a914-169">عنوان المتجر الذي قام بتقديم الأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-169">The address of the store that placed the order.</span></span>              |
| <span data-ttu-id="0a914-170">storeopenfrom</span><span class="sxs-lookup"><span data-stu-id="0a914-170">storeopenfrom</span></span>        | <span data-ttu-id="0a914-171">وقت فتح المتجر الذي قام بتقديم الأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-171">The opening time of the store that placed the order.</span></span>         |
| <span data-ttu-id="0a914-172">storeopento</span><span class="sxs-lookup"><span data-stu-id="0a914-172">storeopento</span></span>          | <span data-ttu-id="0a914-173">وقت إغلاق المتجر الذي قام بتقديم الأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-173">The closing time of the store that placed the order.</span></span>         |
| <span data-ttu-id="0a914-174">pickupstorename</span><span class="sxs-lookup"><span data-stu-id="0a914-174">pickupstorename</span></span>      | <span data-ttu-id="0a914-175">اسم المتجر الذي سيتم منه التقاط الأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-175">The name of the store where the order will be picked up.</span></span>     |
| <span data-ttu-id="0a914-176">pickupstoreaddress</span><span class="sxs-lookup"><span data-stu-id="0a914-176">pickupstoreaddress</span></span>   | <span data-ttu-id="0a914-177">عنوان المتجر الذي سيتم منه التقاط الأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-177">The address of the store where the order will be picked up.</span></span>  |
| <span data-ttu-id="0a914-178">pickupopenstorefrom</span><span class="sxs-lookup"><span data-stu-id="0a914-178">pickupopenstorefrom</span></span>  | <span data-ttu-id="0a914-179">وقت فتح المتجر الذي سيتم منه التقاط الأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-179">The opening time of the store where the order will be picked up.</span></span> |
| <span data-ttu-id="0a914-180">pickupopenstoreto</span><span class="sxs-lookup"><span data-stu-id="0a914-180">pickupopenstoreto</span></span>    | <span data-ttu-id="0a914-181">وقت إغلاق المتجر الذي سيتم منه التقاط الأمر.</span><span class="sxs-lookup"><span data-stu-id="0a914-181">The closing time of the store where the order will be picked up.</span></span> |

### <a name="order-line-placeholders-sales-line-level"></a><span data-ttu-id="0a914-182">العناصر النائبة لبنود الأمر (مستوى بند المبيعات)</span><span class="sxs-lookup"><span data-stu-id="0a914-182">Order line placeholders (sales line level)</span></span>

<span data-ttu-id="0a914-183">تسترد العناصر النائبة التالية وتعرض البيانات الخاصة بالمنتجات الفردية (البنود) في أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="0a914-183">The following placeholders retrieve and show data for individual products (lines) in the sales order.</span></span>

| <span data-ttu-id="0a914-184">اسم العنصر النائب</span><span class="sxs-lookup"><span data-stu-id="0a914-184">Placeholder name</span></span>               | <span data-ttu-id="0a914-185">قيمة العنصر النائب</span><span class="sxs-lookup"><span data-stu-id="0a914-185">Placeholder value</span></span> |
|--------------------------------|-------------------|
| <span data-ttu-id="0a914-186">productid</span><span class="sxs-lookup"><span data-stu-id="0a914-186">productid</span></span>                      | <span data-ttu-id="0a914-187">معرف المنتج الخاص بالبند.</span><span class="sxs-lookup"><span data-stu-id="0a914-187">The product ID for the line.</span></span> |
| <span data-ttu-id="0a914-188">lineproductname</span><span class="sxs-lookup"><span data-stu-id="0a914-188">lineproductname</span></span>                | <span data-ttu-id="0a914-189">اسم المنتج.</span><span class="sxs-lookup"><span data-stu-id="0a914-189">The name of the product.</span></span> |
| <span data-ttu-id="0a914-190">lineproductdescription</span><span class="sxs-lookup"><span data-stu-id="0a914-190">lineproductdescription</span></span>         | <span data-ttu-id="0a914-191">وصف المنتج.</span><span class="sxs-lookup"><span data-stu-id="0a914-191">The description of the product.</span></span> |
| <span data-ttu-id="0a914-192">linequantity</span><span class="sxs-lookup"><span data-stu-id="0a914-192">linequantity</span></span>                   | <span data-ttu-id="0a914-193">عدد الوحدات التي تم طلبها للبند، بالإضافة إلى وحدة القياس (على سبيل المثال، **ea** أو **زوج**).</span><span class="sxs-lookup"><span data-stu-id="0a914-193">The number of units that were ordered for the line, plus the unit of measure (for example, **ea**, or **pair**).</span></span> |
| <span data-ttu-id="0a914-194">lineunit</span><span class="sxs-lookup"><span data-stu-id="0a914-194">lineunit</span></span>                       | <span data-ttu-id="0a914-195">وحدة القياس للبند.</span><span class="sxs-lookup"><span data-stu-id="0a914-195">The unit of measure for the line.</span></span> |
| <span data-ttu-id="0a914-196">linequantity_withoutunit</span><span class="sxs-lookup"><span data-stu-id="0a914-196">linequantity_withoutunit</span></span>       | <span data-ttu-id="0a914-197">عدد الوحدات التي تم طلبها للبند، بدون وحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="0a914-197">The number of units that were ordered for the line, without the unit of measure.</span></span> |
| <span data-ttu-id="0a914-198">linequantitypicked</span><span class="sxs-lookup"><span data-stu-id="0a914-198">linequantitypicked</span></span>             | <span data-ttu-id="0a914-199">عند استخدام حدث **PickOrder**، يتم التقاط عدد الوحدات.</span><span class="sxs-lookup"><span data-stu-id="0a914-199">When the **PickOrder** event is used, the number of units that were picked.</span></span> <span data-ttu-id="0a914-200">خلاف ذلك، **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="0a914-200">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="0a914-201">linequantitypicked_withoutunit</span><span class="sxs-lookup"><span data-stu-id="0a914-201">linequantitypicked_withoutunit</span></span> | <span data-ttu-id="0a914-202">عند استخدام حدث **PickOrder**، يتم التقاط عدد الوحدات، بدون وحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="0a914-202">When the **PickOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="0a914-203">خلاف ذلك، **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="0a914-203">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="0a914-204">linequantitypacked</span><span class="sxs-lookup"><span data-stu-id="0a914-204">linequantitypacked</span></span>             | <span data-ttu-id="0a914-205">عند استخدام أحداث **PackOrder** و **أمر جاهز للالتقاط**، يتم التقاط عدد الوحدات.</span><span class="sxs-lookup"><span data-stu-id="0a914-205">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed.</span></span> <span data-ttu-id="0a914-206">خلاف ذلك، **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="0a914-206">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="0a914-207">linequantitypacked_withoutuom</span><span class="sxs-lookup"><span data-stu-id="0a914-207">linequantitypacked_withoutuom</span></span>  | <span data-ttu-id="0a914-208">عند استخدام أحداث **PackOrder** و **أمر جاهز للالتقاط**، يتم التقاط عدد الوحدة، بدون وحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="0a914-208">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed, without the unit of measure.</span></span> <span data-ttu-id="0a914-209">خلاف ذلك، **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="0a914-209">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="0a914-210">linequantityshipped</span><span class="sxs-lookup"><span data-stu-id="0a914-210">linequantityshipped</span></span>            | <span data-ttu-id="0a914-211">دائمًا **0**، باستثناء عند استخدام أحداث خاصة، كما هو موضح في الصف التالي.</span><span class="sxs-lookup"><span data-stu-id="0a914-211">Always **0**, except when specific events are used, as described in the next row.</span></span> |
| <span data-ttu-id="0a914-212">linequantityshipped_withoutuom</span><span class="sxs-lookup"><span data-stu-id="0a914-212">linequantityshipped_withoutuom</span></span> | <span data-ttu-id="0a914-213">عند استخدام حدث **ShipOrder**، يتم التقاط عدد الوحدات، بدون وحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="0a914-213">When the **ShipOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="0a914-214">خلاف ذلك، **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="0a914-214">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="0a914-215">lineprice</span><span class="sxs-lookup"><span data-stu-id="0a914-215">lineprice</span></span>                      | <span data-ttu-id="0a914-216">سعر الوحدة الفردية.</span><span class="sxs-lookup"><span data-stu-id="0a914-216">The price of a single unit.</span></span> |
| <span data-ttu-id="0a914-217">linenetamount</span><span class="sxs-lookup"><span data-stu-id="0a914-217">linenetamount</span></span>                  | <span data-ttu-id="0a914-218">يتم تطبيق سعر البند بعد عدد الوحدات والخصم.</span><span class="sxs-lookup"><span data-stu-id="0a914-218">The price of the line after the number of units and discount are applied.</span></span> |
| <span data-ttu-id="0a914-219">linediscount</span><span class="sxs-lookup"><span data-stu-id="0a914-219">linediscount</span></span>                   | <span data-ttu-id="0a914-220">الخصم لوحدة فردية.</span><span class="sxs-lookup"><span data-stu-id="0a914-220">The discount for an individual unit.</span></span> |
| <span data-ttu-id="0a914-221">lineshipdate</span><span class="sxs-lookup"><span data-stu-id="0a914-221">lineshipdate</span></span>                   | <span data-ttu-id="0a914-222">تاريخ الشحن للبند.</span><span class="sxs-lookup"><span data-stu-id="0a914-222">The ship date for the line.</span></span> |
| <span data-ttu-id="0a914-223">linedeliverydate</span><span class="sxs-lookup"><span data-stu-id="0a914-223">linedeliverydate</span></span>               | <span data-ttu-id="0a914-224">تاريخ التسليم للبند.</span><span class="sxs-lookup"><span data-stu-id="0a914-224">The delivery date for the line.</span></span> |
| <span data-ttu-id="0a914-225">linedeliverymode</span><span class="sxs-lookup"><span data-stu-id="0a914-225">linedeliverymode</span></span>               | <span data-ttu-id="0a914-226">وضع التسليم للبند.</span><span class="sxs-lookup"><span data-stu-id="0a914-226">The delivery mode for the line.</span></span> |
| <span data-ttu-id="0a914-227">linedeliveryaddress</span><span class="sxs-lookup"><span data-stu-id="0a914-227">linedeliveryaddress</span></span>            | <span data-ttu-id="0a914-228">عنوان التسليم للبند.</span><span class="sxs-lookup"><span data-stu-id="0a914-228">The delivery address for the line.</span></span> |
| <span data-ttu-id="0a914-229">giftcardnumber</span><span class="sxs-lookup"><span data-stu-id="0a914-229">giftcardnumber</span></span>                 | <span data-ttu-id="0a914-230">رقم بطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="0a914-230">The gift card number, for products of the gift card type.</span></span> |
| <span data-ttu-id="0a914-231">giftcardbalance</span><span class="sxs-lookup"><span data-stu-id="0a914-231">giftcardbalance</span></span>                | <span data-ttu-id="0a914-232">رصيد بطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="0a914-232">The gift card balance, for products of the gift card type.</span></span> |
| <span data-ttu-id="0a914-233">giftcardmessage</span><span class="sxs-lookup"><span data-stu-id="0a914-233">giftcardmessage</span></span>                | <span data-ttu-id="0a914-234">رسالة بطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="0a914-234">The gift card message, for products of the gift card type.</span></span> |
| <span data-ttu-id="0a914-235">giftcardpin</span><span class="sxs-lookup"><span data-stu-id="0a914-235">giftcardpin</span></span>                    | <span data-ttu-id="0a914-236">رقم التعريف الشخصي (PIN) لبطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="0a914-236">The personal identification number (PIN) of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="0a914-237">(هذا العنصر النائب خاص ببطاقات الهدايا الخارجية.)</span><span class="sxs-lookup"><span data-stu-id="0a914-237">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="0a914-238">giftcardexpiration</span><span class="sxs-lookup"><span data-stu-id="0a914-238">giftcardexpiration</span></span>             | <span data-ttu-id="0a914-239">تاريخ انتهاء الصلاحية لبطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="0a914-239">The expiration date of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="0a914-240">(هذا العنصر النائب خاص ببطاقات الهدايا الخارجية.)</span><span class="sxs-lookup"><span data-stu-id="0a914-240">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="0a914-241">giftcardrecipientname</span><span class="sxs-lookup"><span data-stu-id="0a914-241">giftcardrecipientname</span></span>          | <span data-ttu-id="0a914-242">اسم مستلم بطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="0a914-242">The name of the gift card recipient, for products of the gift card type.</span></span> |
| <span data-ttu-id="0a914-243">giftcardbuyername</span><span class="sxs-lookup"><span data-stu-id="0a914-243">giftcardbuyername</span></span>              | <span data-ttu-id="0a914-244">اسم مشتري بطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="0a914-244">The name of the gift card buyer, for products of the gift card type.</span></span> |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a><span data-ttu-id="0a914-245">تنسيق العناصر النائبة لبند الأمر في نص رسالة البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0a914-245">Format of order line placeholders in the email message body</span></span>

<span data-ttu-id="0a914-246">عند إنشاء HTML لبنود الأمر الفردية في نص رسالة البريد الإلكتروني، قم بإحاطة الكتلة المكررة من HTML والعناصر النائبة الخاصة بالبنود بالعناصر النائبة التالية التي يتم وضعها داخل علامات تعليق HTML.</span><span class="sxs-lookup"><span data-stu-id="0a914-246">When you create the HTML for the individual order lines in the email message body, surround the repeating block of HTML and placeholders for the lines with the following placeholders that are put inside HTML comment tags.</span></span>

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

<span data-ttu-id="0a914-247">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="0a914-247">Here is an example.</span></span>

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a><span data-ttu-id="0a914-248">إنشاء قالب للإيصالات المرسلة بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0a914-248">Create a template for emailed receipts</span></span>

<span data-ttu-id="0a914-249">يمكن إرسال الإيصالات بالبريد الإلكتروني للعملاء الذين يقومون بإجراء عمليات شراء من نقطة البيع بالتجزئة (POS).</span><span class="sxs-lookup"><span data-stu-id="0a914-249">Receipts can be emailed to customers who make purchases at a retail point of sale (POS).</span></span> <span data-ttu-id="0a914-250">بشكل عام، تكون خطوات إنشاء قالب إيصال البريد الإلكتروني هي نفس خطوات إنشاء القوالب لأحداث الحركات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="0a914-250">In general, the steps for creating the emailed receipt template are the same as the steps for creating templates for other transactional events.</span></span> <span data-ttu-id="0a914-251">مع ذلك، بالتغييرات التالية مطلوبة:</span><span class="sxs-lookup"><span data-stu-id="0a914-251">However, the following changes are required:</span></span>

- <span data-ttu-id="0a914-252">يتم إدراج نص الإيصال في البريد الإلكتروني باستخدام العنصر النائب **%message%**.</span><span class="sxs-lookup"><span data-stu-id="0a914-252">The text of the receipt is inserted into the email by using the **%message%** placeholder.</span></span> <span data-ttu-id="0a914-253">للتأكد من أنه تم عرض نص الإيصال بشكل صحيح، قم بإحاطة العنصر النائب **%message%** بعلامات **&lt;pre&gt;** و **&lt;/pre&gt;** لـ HTML.</span><span class="sxs-lookup"><span data-stu-id="0a914-253">To ensure that the receipt body is correctly rendered, surround the **%message%** placeholder with HTML **&lt;pre&gt;** and **&lt;/pre&gt;** tags.</span></span>
- <span data-ttu-id="0a914-254">يمكن استخدام العنصر النائب **%receiptid%** لإظهار رمز الاستجابة السريعة (QR) أو الرمز الشريطي الذي يمثل معرف الإيصال.</span><span class="sxs-lookup"><span data-stu-id="0a914-254">The **%receiptid%** placeholder can be used to show a QR code or bar code that represents the receipt ID.</span></span> <span data-ttu-id="0a914-255">(يتم إنشاء رموز QR والرموز الشريطية بشكل ديناميكي ويتم تقديمها بواسطة خدمه جهة خارجية.) لمزيد من المعلومات حول كيفية إظهار رمز الاستجابة السريعة (QR) أو الرمز الشريطي في إيصال بريد الكتروني، راجع [إضافة رمز استجابة سريعة (QR) أو رمز شريطي إلى المعاملات ورسائل البريد الكتروني الخاصة بالحركات والاستلام](add-qr-code-barcode-email.md).</span><span class="sxs-lookup"><span data-stu-id="0a914-255">(QR codes and bar codes are dynamically generated and served by a third-party service.) For more information about how to show a QR code or bar code in an emailed receipt, see [Add a QR code or bar code to transactional and receipt emails](add-qr-code-barcode-email.md).</span></span>

## <a name="upload-the-email-html"></a><span data-ttu-id="0a914-256">تحميل HTML للبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0a914-256">Upload the email HTML</span></span>

<span data-ttu-id="0a914-257">بعد إنشاء واختبار HTML لنص الرسالة الخاصة بك، يجب أن يتم تحميله إلى Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0a914-257">After you've created and tested the HTML for your message body, it must be uploaded to Commerce headquarters.</span></span> <span data-ttu-id="0a914-258">لا يمكن تصدير HTML الخاص بالبريد الإلكتروني حاليًا.</span><span class="sxs-lookup"><span data-stu-id="0a914-258">Currently, email HTML can't be exported.</span></span> <span data-ttu-id="0a914-259">لذلك، يجب الاحتفاظ بالنسخة الرئيسية من HTML خارج Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0a914-259">Therefore, you must maintain the master copy of your HTML outside Commerce headquarters.</span></span>

<span data-ttu-id="0a914-260">لتحميل HTML لقالب بريد إلكتروني جديد أو محرر، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0a914-260">To upload a new or edited email template HTML, follow these steps.</span></span>

1. <span data-ttu-id="0a914-261">في Commerce headquarters، انتقل إلى **Retail and Commerce \> إعداد Headquarters \> قوالب البريد الإلكتروني للمؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="0a914-261">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="0a914-262">حدد صف اللغة التي تريد إضافة أو استبدال HTML لها.</span><span class="sxs-lookup"><span data-stu-id="0a914-262">Select the row for the language that you want to add or replace HTML for.</span></span> <span data-ttu-id="0a914-263">بدلا من ذلك، حدد **جديد** لإنشاء صف للغة جديدة.</span><span class="sxs-lookup"><span data-stu-id="0a914-263">Alternatively, select **New** to create a row for a new language.</span></span>
1. <span data-ttu-id="0a914-264">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0a914-264">Select **Edit**.</span></span>
1. <span data-ttu-id="0a914-265">في مربع الحوار الذي يظهر، حدد **استعراض**.</span><span class="sxs-lookup"><span data-stu-id="0a914-265">In the dialog box that appears, select **Browse**.</span></span> <span data-ttu-id="0a914-266">قم بالاستعراض بحثا عن مستند HTML الذي تريد تحميله، وحدده، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="0a914-266">Browse to the HTML document that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="0a914-267">ثم حدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="0a914-267">Select **Upload**.</span></span>
1. <span data-ttu-id="0a914-268">بعد ظهور HTML بالبريد الإلكتروني الخاص بك في نافذة المعاينة، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0a914-268">After your email HTML appears in the preview window, select **OK**.</span></span>
1. <span data-ttu-id="0a914-269">تأكد من تحديد خانة الاختيار **يتضمن نص** للصف.</span><span class="sxs-lookup"><span data-stu-id="0a914-269">Make sure that the **Has body** check box is selected for the row.</span></span>

<span data-ttu-id="0a914-270">إذا كنت قد قمت بالفعل بتكوين Commerce Headquarters لإرسال البريد الإلكتروني، سيتم إرسال بريد إلكتروني جديد أو محدث خاص بك إلى كافة العملاء الذين ينفذون حركة تستدعي الحدث الذي تم تعيينه إلى القالب.</span><span class="sxs-lookup"><span data-stu-id="0a914-270">If you've already configured Commerce headquarters to send email, your new or updated email will be sent to all customers who perform a transaction that invokes the event that is mapped to the template.</span></span>

<span data-ttu-id="0a914-271">للحصول على مزيد من المعلومات حول كيفية تكوين رسائل البريد الإلكتروني في Dynamics 365 Commerce، راجع [تكوين وإرسال البريد الإلكتروني](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="0a914-271">For more information about how to configure emails in Dynamics 365 Commerce, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a914-272">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0a914-272">Additional resources</span></span> 

[<span data-ttu-id="0a914-273">إنشاء ملف تعريف الإخطار بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0a914-273">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="0a914-274">تكوين وإرسال البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0a914-274">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[<span data-ttu-id="0a914-275">إعداد إيصالات بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0a914-275">Set up email receipts</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[<span data-ttu-id="0a914-276">إرسال إيصالات البريد الإلكتروني من Modern POS</span><span class="sxs-lookup"><span data-stu-id="0a914-276">Send email receipts from Modern POS </span></span>](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
