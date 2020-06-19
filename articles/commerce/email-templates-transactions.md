---
title: إنشاء قوالب بريد إلكتروني لأحداث الحركات
description: يوضح هذا الموضوع كيفية إنشاء قوالب بريد إلكتروني وتحميلها وتكوينها لأحداث الحركات في Microsoft Dynamics 365 Commerce.
author: stuharg
manager: annbe
ms.date: 06/01/2020
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
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a02839088addfa9b405af486f3b795eace1671cc
ms.sourcegitcommit: 4db8c30c2f26af1896938dd3ece3756577374ecb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/01/2020
ms.locfileid: "3416569"
---
# <a name="create-email-templates-for-transactional-events"></a><span data-ttu-id="9c4a2-103">إنشاء قوالب بريد إلكتروني لأحداث الحركات</span><span class="sxs-lookup"><span data-stu-id="9c4a2-103">Create email templates for transactional events</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9c4a2-104">يوضح هذا الموضوع كيفية إنشاء قوالب بريد إلكتروني وتحميلها وتكوينها لأحداث الحركات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-104">This topic describes how to create, upload, and configure email templates for transactional events in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9c4a2-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="9c4a2-105">Overview</span></span>

<span data-ttu-id="9c4a2-106">يوفر Dynamics 365 Commerce حلاً جاهزًا لإرسال رسائل بريد إلكتروني والتي تقوم بتنبيه العملاء حول أحداث الحركات (على سبيل المثال، عند تقديم طلب ما أو عندما يصبح الأمر جاهزًا للالتقاط أو عندما يتم شحن الأمر).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-106">Dynamics 365 Commerce provides an out-of-box solution for sending emails that alert customers about transactional events (for example, when an order is placed, an order is ready for pickup, or an order has been shipped).</span></span> <span data-ttu-id="9c4a2-107">يصف هذا الموضوع الخطوات الخاصة بإنشاء قوالب البريد الإلكتروني المستخدمة لإرسال رسائل بريد إلكتروني للحركات وتحميلها وتكوينها.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-107">This topic describes the steps for creating, uploading, and configuring the email templates that are used to send transactional emails.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="9c4a2-108">إنشاء قالب بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c4a2-108">Create an email template</span></span>

<span data-ttu-id="9c4a2-109">قبل أن تتمكن من تعيين حدث حركة معين إلى قالب بريد إلكتروني، يجب عليك إنشاء القالب.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-109">Before you can map a specific transactional event to an email template, you must create the template.</span></span>

<span data-ttu-id="9c4a2-110">لإنشاء قالب بريد إلكتروني، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-110">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="9c4a2-111">في Commerce headquarters، انتقل إلى **قوالب البريد الإلكتروني للمؤسسة** ضمن **Retail and Commerce \> إعداد Headquarters \> قوالب البريد الإلكتروني للمؤسسة** أو **إدارة المؤسسة \> إعداد \> قوالب البريد الإلكتروني للمؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-111">In Commerce headquarters, go to **Organization email templates**, which is under **Retail and Commerce \> Headquarters setup \> Organization email templates** or **Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="9c4a2-112">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-112">Select **New**.</span></span>
1. <span data-ttu-id="9c4a2-113">ضمن **عام**، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="9c4a2-113">Under **General**, set the following fields:</span></span>

    - <span data-ttu-id="9c4a2-114">**معرف البريد الإلكتروني** – معرف البريد الإلكتروني هو المعرف الفريد للقالب، وهو القيمة التي تظهر عند تحديد قالب لتعيينه إلى حدث.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-114">**Email ID** – The email ID is the unique identifier for a template, and it's the value that is shown when you select a template to map to an event.</span></span>
    - <span data-ttu-id="9c4a2-115">**وصف البريد الإلكتروني** – يمكنك استخدام هذا الحقل الاختياري لتوفير وصف للقالب.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-115">**Email description** – You can use this optional field to provide a description of the template.</span></span> <span data-ttu-id="9c4a2-116">تظهر القيمة التي تدخلها في Commerce Headquarters فقط.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-116">The value that you enter appears only in Commerce headquarters.</span></span>
    - <span data-ttu-id="9c4a2-117">**اسم المرسل** – يظهر الاسم الذي تقوم بإدخاله في الحقل "من" الخاص بمعظم عملاء البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-117">**Sender name** – The name that you enter appears in the "from" field of most email clients.</span></span>
    - <span data-ttu-id="9c4a2-118">**البريد الإلكتروني للمرسل** – أدخل عنوان البريد الإلكتروني الذي يجب استخدامه لرسائل البريد الإلكتروني التي يتم إرسالها باستخدام هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-118">**Sender email** – Enter the email address that should be used for emails that are sent by using this template.</span></span>
    - <span data-ttu-id="9c4a2-119">**كود اللغة الافتراضية** – يحدد هذا الحقل الإصدار المترجم من البريد الإلكتروني الذي يتم إرساله افتراضيًا، في حالة عدم توفير لغة بواسطة القناة التي تقوم باستدعاء هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-119">**Default language code** – This field specifies the localized version of the email that is sent by default, if no language is provided by the channel that invokes this template.</span></span>

1. <span data-ttu-id="9c4a2-120">ضمن **محتوي رسالة البريد الإلكتروني**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-120">Under **Email message content**, select **New**.</span></span>
1. <span data-ttu-id="9c4a2-121">في حقل **اللغة**، ادخل اللغة لقالب البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-121">In the **Language** field, enter the language for the email template.</span></span> <span data-ttu-id="9c4a2-122">يمكنك إضافة المزيد من اللغات والقوالب المترجمة لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-122">You can add more languages and localized templates later.</span></span>
1. <span data-ttu-id="9c4a2-123">في حقل **الموضوع**، أدخل موضوع البريد الإلكتروني الذي يجب أن يظهر في حقل الموضوع الخاص بالبريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-123">In the **Subject** field, enter the email subject that should appear in the subject field of the email.</span></span>
1. <span data-ttu-id="9c4a2-124">حدد **تحرير** لتحميل قالب البريد الإلكتروني الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-124">Select **Edit** to upload your email template.</span></span>

## <a name="create-an-email-message-body-by-using-html"></a><span data-ttu-id="9c4a2-125">إنشاء نص رسالة بريد إلكتروني باستخدام HTML</span><span class="sxs-lookup"><span data-stu-id="9c4a2-125">Create an email message body by using HTML</span></span>

<span data-ttu-id="9c4a2-126">يتم تكوين نص رسالة البريد الإلكتروني الخاصة بك بتنسيق HTML.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-126">The message body of your email is composed in HTML.</span></span> <span data-ttu-id="9c4a2-127">يمكنك استخدام أي تخطيط، ونمط، وعلامة تجارية يسمح بها HTML أوراق الأنماط المتتالية المدمجة (CSS).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-127">You can use any layout, styling, and branding that HTML and inline Cascading Style Sheets (CSS) allow for.</span></span> <span data-ttu-id="9c4a2-128">يمكنك أيضًا استخدام الصور، إذا قمت باستضافتها على نقطة نهاية ويب متوفرة بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-128">You can also use images, if you host them on a publicly available web endpoint.</span></span> <span data-ttu-id="9c4a2-129">لإضافة صورة، أدخل عنوان URL الخاص بالصورة في سمة **src** الخاصة بعلامة **&lt;img&gt;** لـ HTML.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-129">To add an image, enter the image's URL in the **src** attribute of the HTML **&lt;img&gt;** tag.</span></span>

> [!NOTE]
> <span data-ttu-id="9c4a2-130">يفرض عملاء البريد الإلكتروني قيودًا على المخطط والنمط قد تتطلب تعديلات على HTML وCSS التي تستخدمها لنص الرسالة.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-130">Email clients impose layout and style limitations that might require adjustments to the HTML and CSS that you use for the message body.</span></span> <span data-ttu-id="9c4a2-131">نوصيك بالتعرف على أفضل الممارسات الخاصة بإنشاء HTML الذي يدعمه معظم عملاء البريد الإلكتروني المشهورين.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-131">We recommend that you familiarize yourself with the best practices for creating HTML that will be supported by the most popular email clients.</span></span>

## <a name="add-placeholders-to-the-email-message-body"></a><span data-ttu-id="9c4a2-132">إضافة عناصر نائبة إلى نص رسالة البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c4a2-132">Add placeholders to the email message body</span></span>

<span data-ttu-id="9c4a2-133">يمكن أن يحتوي بريدك الإلكتروني على عناصر نائبة يتم استبدالها بقيم خاصة بالعميل وقيم خاصة بالحركات عند إنشاء البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-133">Your email can contain placeholders that are replaced with customer-specific and transaction-specific values when the email is generated.</span></span> <span data-ttu-id="9c4a2-134">تكون العناصر النائبة دائمًا محاطة بعلامات النسبة المئوية (%) ويتم إدراجها مباشره في مستند HTML.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-134">Placeholders are always surrounded by percent signs (%) and are inserted directly into the HTML document.</span></span>

<span data-ttu-id="9c4a2-135">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-135">Here is an example.</span></span>

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a><span data-ttu-id="9c4a2-136">العناصر النائبة للأمر (مستوى أمر المبيعات)</span><span class="sxs-lookup"><span data-stu-id="9c4a2-136">Order placeholders (sales order level)</span></span>

<span data-ttu-id="9c4a2-137">تقوم العناصر النائبة التالية باسترداد وإظهار البيانات التي يتم تحديدها في مستوى أمر المبيعات (على عكس مستوى بند المبيعات).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-137">The following placeholders retrieve and show data that is defined at the sales order level (as opposed to the sales line level).</span></span>

| <span data-ttu-id="9c4a2-138">اسم العنصر النائب</span><span class="sxs-lookup"><span data-stu-id="9c4a2-138">Placeholder name</span></span>    | <span data-ttu-id="9c4a2-139">قيمة العنصر النائب</span><span class="sxs-lookup"><span data-stu-id="9c4a2-139">Placeholder value</span></span>                                                |
|---------------------|------------------------------------------------------------------|
| <span data-ttu-id="9c4a2-140">customername</span><span class="sxs-lookup"><span data-stu-id="9c4a2-140">customername</span></span>        | <span data-ttu-id="9c4a2-141">اسم العميل الذي قام بتقديم الأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-141">The name of the customer who placed the order.</span></span>                   |
| <span data-ttu-id="9c4a2-142">salesid</span><span class="sxs-lookup"><span data-stu-id="9c4a2-142">salesid</span></span>             | <span data-ttu-id="9c4a2-143">معرف المبيعات للأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-143">The sales ID of the order.</span></span>                                       |
| <span data-ttu-id="9c4a2-144">deliveryaddress</span><span class="sxs-lookup"><span data-stu-id="9c4a2-144">deliveryaddress</span></span>     | <span data-ttu-id="9c4a2-145">عنوان التسليم الخاص بالأوامر المشحونة.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-145">The delivery address for shipped orders.</span></span>                         |
| <span data-ttu-id="9c4a2-146">customeraddress</span><span class="sxs-lookup"><span data-stu-id="9c4a2-146">customeraddress</span></span>     | <span data-ttu-id="9c4a2-147">عنوان العميل.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-147">The address of the customer.</span></span>                                     |
| <span data-ttu-id="9c4a2-148">deliverydate</span><span class="sxs-lookup"><span data-stu-id="9c4a2-148">deliverydate</span></span>        | <span data-ttu-id="9c4a2-149">تاريخ التسليم.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-149">The delivery date.</span></span>                                               |
| <span data-ttu-id="9c4a2-150">shipdate</span><span class="sxs-lookup"><span data-stu-id="9c4a2-150">shipdate</span></span>            | <span data-ttu-id="9c4a2-151">تاريخ الشحن.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-151">The ship date.</span></span>                                                   |
| <span data-ttu-id="9c4a2-152">modeofdelivery</span><span class="sxs-lookup"><span data-stu-id="9c4a2-152">modeofdelivery</span></span>      | <span data-ttu-id="9c4a2-153">وضع التسليم الخاص بالأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-153">The delivery mode of the order.</span></span>                                  |
| <span data-ttu-id="9c4a2-154">التكاليف</span><span class="sxs-lookup"><span data-stu-id="9c4a2-154">charges</span></span>             | <span data-ttu-id="9c4a2-155">إجمالي المصاريف الخاصة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-155">The total charges for the order.</span></span>                                 |
| <span data-ttu-id="9c4a2-156">ضريبة</span><span class="sxs-lookup"><span data-stu-id="9c4a2-156">tax</span></span>                 | <span data-ttu-id="9c4a2-157">إجمالي الضرائب الخاصة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-157">The total tax for the order.</span></span>                                     |
| <span data-ttu-id="9c4a2-158">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="9c4a2-158">total</span></span>               | <span data-ttu-id="9c4a2-159">المبلغ الإجمالي الخاص بالأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-159">The total amount for the order.</span></span>                                  |
| <span data-ttu-id="9c4a2-160">ordernetamount</span><span class="sxs-lookup"><span data-stu-id="9c4a2-160">ordernetamount</span></span>      | <span data-ttu-id="9c4a2-161">المبلغ الإجمالي للأمر، مطروحًا منه إجمالي الضريبة.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-161">The total amount for the order, minus the total tax.</span></span>             |
| <span data-ttu-id="9c4a2-162">خصم</span><span class="sxs-lookup"><span data-stu-id="9c4a2-162">discount</span></span>            | <span data-ttu-id="9c4a2-163">إجمالي الخصم الخاص بالأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-163">The total discount for the order.</span></span>                                |
| <span data-ttu-id="9c4a2-164">storename</span><span class="sxs-lookup"><span data-stu-id="9c4a2-164">storename</span></span>           | <span data-ttu-id="9c4a2-165">اسم المتجر الذي تم فيه تقديم الأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-165">The name of the store where the order was placed.</span></span>                |
| <span data-ttu-id="9c4a2-166">storeaddress</span><span class="sxs-lookup"><span data-stu-id="9c4a2-166">storeaddress</span></span>        | <span data-ttu-id="9c4a2-167">عنوان المتجر الذي قام بتقديم الأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-167">The address of the store that placed the order.</span></span>                  |
| <span data-ttu-id="9c4a2-168">storeopenfrom</span><span class="sxs-lookup"><span data-stu-id="9c4a2-168">storeopenfrom</span></span>       | <span data-ttu-id="9c4a2-169">وقت فتح المتجر الذي قام بتقديم الأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-169">The opening time of the store that placed the order.</span></span>             |
| <span data-ttu-id="9c4a2-170">storeopento</span><span class="sxs-lookup"><span data-stu-id="9c4a2-170">storeopento</span></span>         | <span data-ttu-id="9c4a2-171">وقت إغلاق المتجر الذي قام بتقديم الأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-171">The closing time of the store that placed the order.</span></span>             |
| <span data-ttu-id="9c4a2-172">pickupstorename</span><span class="sxs-lookup"><span data-stu-id="9c4a2-172">pickupstorename</span></span>     | <span data-ttu-id="9c4a2-173">اسم المتجر الذي سيتم منه التقاط الأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-173">The name of the store where the order will be picked up.</span></span>         |
| <span data-ttu-id="9c4a2-174">pickupstoreaddress</span><span class="sxs-lookup"><span data-stu-id="9c4a2-174">pickupstoreaddress</span></span>  | <span data-ttu-id="9c4a2-175">عنوان المتجر الذي سيتم منه التقاط الأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-175">The address of the store where the order will be picked up.</span></span>      |
| <span data-ttu-id="9c4a2-176">pickupopenstorefrom</span><span class="sxs-lookup"><span data-stu-id="9c4a2-176">pickupopenstorefrom</span></span> | <span data-ttu-id="9c4a2-177">وقت فتح المتجر الذي سيتم منه التقاط الأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-177">The opening time of the store where the order will be picked up.</span></span> |
| <span data-ttu-id="9c4a2-178">pickupopenstoreto</span><span class="sxs-lookup"><span data-stu-id="9c4a2-178">pickupopenstoreto</span></span>   | <span data-ttu-id="9c4a2-179">وقت إغلاق المتجر الذي سيتم منه التقاط الأمر.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-179">The closing time of the store where the order will be picked up.</span></span> |

### <a name="order-line-placeholders-sales-line-level"></a><span data-ttu-id="9c4a2-180">العناصر النائبة لبنود الأمر (مستوى بند المبيعات)</span><span class="sxs-lookup"><span data-stu-id="9c4a2-180">Order line placeholders (sales line level)</span></span>

<span data-ttu-id="9c4a2-181">تسترد العناصر النائبة التالية وتعرض البيانات الخاصة بالمنتجات الفردية (البنود) في أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-181">The following placeholders retrieve and show data for individual products (lines) in the sales order.</span></span>

| <span data-ttu-id="9c4a2-182">اسم العنصر النائب</span><span class="sxs-lookup"><span data-stu-id="9c4a2-182">Placeholder name</span></span>               | <span data-ttu-id="9c4a2-183">قيمة العنصر النائب</span><span class="sxs-lookup"><span data-stu-id="9c4a2-183">Placeholder value</span></span> |
|--------------------------------|-------------------|
| <span data-ttu-id="9c4a2-184">productid</span><span class="sxs-lookup"><span data-stu-id="9c4a2-184">productid</span></span>                      | <span data-ttu-id="9c4a2-185">معرف المنتج الخاص بالبند.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-185">The product ID for the line.</span></span> |
| <span data-ttu-id="9c4a2-186">lineproductname</span><span class="sxs-lookup"><span data-stu-id="9c4a2-186">lineproductname</span></span>                | <span data-ttu-id="9c4a2-187">اسم المنتج.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-187">The name of the product.</span></span> |
| <span data-ttu-id="9c4a2-188">lineproductdescription</span><span class="sxs-lookup"><span data-stu-id="9c4a2-188">lineproductdescription</span></span>         | <span data-ttu-id="9c4a2-189">وصف المنتج.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-189">The description of the product.</span></span> |
| <span data-ttu-id="9c4a2-190">linequantity</span><span class="sxs-lookup"><span data-stu-id="9c4a2-190">linequantity</span></span>                   | <span data-ttu-id="9c4a2-191">عدد الوحدات التي تم طلبها للبند، بالإضافة إلى وحدة القياس (على سبيل المثال، **ea** أو **زوج**).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-191">The number of units that were ordered for the line, plus the unit of measure (for example, **ea**, or **pair**).</span></span> |
| <span data-ttu-id="9c4a2-192">lineunit</span><span class="sxs-lookup"><span data-stu-id="9c4a2-192">lineunit</span></span>                       | <span data-ttu-id="9c4a2-193">وحدة القياس للبند.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-193">The unit of measure for the line.</span></span> |
| <span data-ttu-id="9c4a2-194">linequantity_withoutunit</span><span class="sxs-lookup"><span data-stu-id="9c4a2-194">linequantity_withoutunit</span></span>       | <span data-ttu-id="9c4a2-195">عدد الوحدات التي تم طلبها للبند، بدون وحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-195">The number of units that were ordered for the line, without the unit of measure.</span></span> |
| <span data-ttu-id="9c4a2-196">linequantitypicked</span><span class="sxs-lookup"><span data-stu-id="9c4a2-196">linequantitypicked</span></span>             | <span data-ttu-id="9c4a2-197">عند استخدام حدث **PickOrder**، يتم التقاط عدد الوحدات.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-197">When the **PickOrder** event is used, the number of units that were picked.</span></span> <span data-ttu-id="9c4a2-198">خلاف ذلك، **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-198">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="9c4a2-199">linequantitypicked_withoutunit</span><span class="sxs-lookup"><span data-stu-id="9c4a2-199">linequantitypicked_withoutunit</span></span> | <span data-ttu-id="9c4a2-200">عند استخدام حدث **PickOrder**، يتم التقاط عدد الوحدات، بدون وحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-200">When the **PickOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="9c4a2-201">خلاف ذلك، **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-201">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="9c4a2-202">linequantitypacked</span><span class="sxs-lookup"><span data-stu-id="9c4a2-202">linequantitypacked</span></span>             | <span data-ttu-id="9c4a2-203">عند استخدام أحداث **PackOrder** و**أمر جاهز للالتقاط**، يتم التقاط عدد الوحدات.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-203">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed.</span></span> <span data-ttu-id="9c4a2-204">خلاف ذلك، **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-204">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="9c4a2-205">linequantitypacked_withoutuom</span><span class="sxs-lookup"><span data-stu-id="9c4a2-205">linequantitypacked_withoutuom</span></span>  | <span data-ttu-id="9c4a2-206">عند استخدام أحداث **PackOrder** و**أمر جاهز للالتقاط**، يتم التقاط عدد الوحدة، بدون وحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-206">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed, without the unit of measure.</span></span> <span data-ttu-id="9c4a2-207">خلاف ذلك، **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-207">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="9c4a2-208">linequantityshipped</span><span class="sxs-lookup"><span data-stu-id="9c4a2-208">linequantityshipped</span></span>            | <span data-ttu-id="9c4a2-209">دائمًا **0**، باستثناء عند استخدام أحداث خاصة، كما هو موضح في الصف التالي.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-209">Always **0**, except when specific events are used, as described in the next row.</span></span> |
| <span data-ttu-id="9c4a2-210">linequantityshipped_withoutuom</span><span class="sxs-lookup"><span data-stu-id="9c4a2-210">linequantityshipped_withoutuom</span></span> | <span data-ttu-id="9c4a2-211">عند استخدام حدث **ShipOrder**، يتم التقاط عدد الوحدات، بدون وحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-211">When the **ShipOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="9c4a2-212">خلاف ذلك، **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-212">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="9c4a2-213">lineprice</span><span class="sxs-lookup"><span data-stu-id="9c4a2-213">lineprice</span></span>                      | <span data-ttu-id="9c4a2-214">سعر الوحدة الفردية.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-214">The price of a single unit.</span></span> |
| <span data-ttu-id="9c4a2-215">linenetamount</span><span class="sxs-lookup"><span data-stu-id="9c4a2-215">linenetamount</span></span>                  | <span data-ttu-id="9c4a2-216">يتم تطبيق سعر البند بعد عدد الوحدات والخصم.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-216">The price of the line after the number of units and discount are applied.</span></span> |
| <span data-ttu-id="9c4a2-217">linediscount</span><span class="sxs-lookup"><span data-stu-id="9c4a2-217">linediscount</span></span>                   | <span data-ttu-id="9c4a2-218">الخصم لوحدة فردية.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-218">The discount for an individual unit.</span></span> |
| <span data-ttu-id="9c4a2-219">lineshipdate</span><span class="sxs-lookup"><span data-stu-id="9c4a2-219">lineshipdate</span></span>                   | <span data-ttu-id="9c4a2-220">تاريخ الشحن للبند.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-220">The ship date for the line.</span></span> |
| <span data-ttu-id="9c4a2-221">linedeliverydate</span><span class="sxs-lookup"><span data-stu-id="9c4a2-221">linedeliverydate</span></span>               | <span data-ttu-id="9c4a2-222">تاريخ التسليم للبند.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-222">The delivery date for the line.</span></span> |
| <span data-ttu-id="9c4a2-223">linedeliverymode</span><span class="sxs-lookup"><span data-stu-id="9c4a2-223">linedeliverymode</span></span>               | <span data-ttu-id="9c4a2-224">وضع التسليم للبند.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-224">The delivery mode for the line.</span></span> |
| <span data-ttu-id="9c4a2-225">linedeliveryaddress</span><span class="sxs-lookup"><span data-stu-id="9c4a2-225">linedeliveryaddress</span></span>            | <span data-ttu-id="9c4a2-226">عنوان التسليم للبند.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-226">The delivery address for the line.</span></span> |
| <span data-ttu-id="9c4a2-227">giftcardnumber</span><span class="sxs-lookup"><span data-stu-id="9c4a2-227">giftcardnumber</span></span>                 | <span data-ttu-id="9c4a2-228">رقم بطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-228">The gift card number, for products of the gift card type.</span></span> |
| <span data-ttu-id="9c4a2-229">giftcardbalance</span><span class="sxs-lookup"><span data-stu-id="9c4a2-229">giftcardbalance</span></span>                | <span data-ttu-id="9c4a2-230">رصيد بطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-230">The gift card balance, for products of the gift card type.</span></span> |
| <span data-ttu-id="9c4a2-231">giftcardmessage</span><span class="sxs-lookup"><span data-stu-id="9c4a2-231">giftcardmessage</span></span>                | <span data-ttu-id="9c4a2-232">رسالة بطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-232">The gift card message, for products of the gift card type.</span></span> |
| <span data-ttu-id="9c4a2-233">giftcardpin</span><span class="sxs-lookup"><span data-stu-id="9c4a2-233">giftcardpin</span></span>                    | <span data-ttu-id="9c4a2-234">رقم التعريف الشخصي (PIN) لبطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-234">The personal identification number (PIN) of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="9c4a2-235">(هذا العنصر النائب خاص ببطاقات الهدايا الخارجية.)</span><span class="sxs-lookup"><span data-stu-id="9c4a2-235">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="9c4a2-236">giftcardexpiration</span><span class="sxs-lookup"><span data-stu-id="9c4a2-236">giftcardexpiration</span></span>             | <span data-ttu-id="9c4a2-237">تاريخ انتهاء الصلاحية لبطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-237">The expiration date of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="9c4a2-238">(هذا العنصر النائب خاص ببطاقات الهدايا الخارجية.)</span><span class="sxs-lookup"><span data-stu-id="9c4a2-238">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="9c4a2-239">giftcardrecipientname</span><span class="sxs-lookup"><span data-stu-id="9c4a2-239">giftcardrecipientname</span></span>          | <span data-ttu-id="9c4a2-240">اسم مستلم بطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-240">The name of the gift card recipient, for products of the gift card type.</span></span> |
| <span data-ttu-id="9c4a2-241">giftcardbuyername</span><span class="sxs-lookup"><span data-stu-id="9c4a2-241">giftcardbuyername</span></span>              | <span data-ttu-id="9c4a2-242">اسم مشتري بطاقة الهدايا، للمنتجات الخاصة بنوع بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-242">The name of the gift card buyer, for products of the gift card type.</span></span> |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a><span data-ttu-id="9c4a2-243">تنسيق العناصر النائبة لبند الأمر في نص رسالة البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c4a2-243">Format of order line placeholders in the email message body</span></span>

<span data-ttu-id="9c4a2-244">عند إنشاء HTML لبنود الأمر الفردية في نص رسالة البريد الإلكتروني، قم بإحاطة الكتلة المكررة من HTML والعناصر النائبة الخاصة بالبنود بالعناصر النائبة التالية التي يتم وضعها داخل علامات تعليق HTML.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-244">When you create the HTML for the individual order lines in the email message body, surround the repeating block of HTML and placeholders for the lines with the following placeholders that are put inside HTML comment tags.</span></span>

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

<span data-ttu-id="9c4a2-245">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-245">Here is an example.</span></span>

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

## <a name="create-a-template-for-emailed-receipts"></a><span data-ttu-id="9c4a2-246">إنشاء قالب للإيصالات المرسلة بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c4a2-246">Create a template for emailed receipts</span></span>

<span data-ttu-id="9c4a2-247">يمكن إرسال الإيصالات بالبريد الإلكتروني للعملاء الذين يقومون بإجراء عمليات شراء من نقطة البيع بالتجزئة (POS).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-247">Receipts can be emailed to customers who make purchases at a retail point of sale (POS).</span></span> <span data-ttu-id="9c4a2-248">بشكل عام، تكون خطوات إنشاء قالب إيصال البريد الإلكتروني هي نفس خطوات إنشاء القوالب لأحداث الحركات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-248">In general, the steps for creating the emailed receipt template are the same as the steps for creating templates for other transactional events.</span></span> <span data-ttu-id="9c4a2-249">مع ذلك، بالتغييرات التالية مطلوبة:</span><span class="sxs-lookup"><span data-stu-id="9c4a2-249">However, the following changes are required:</span></span>

- <span data-ttu-id="9c4a2-250">يجب أن يكون معرف البريد الإلكتروني لقالب البريد الإلكتروني **emailRecpt**.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-250">The email ID of the email template must be **emailRecpt**.</span></span>
- <span data-ttu-id="9c4a2-251">يتم إدراج نص الإيصال في البريد الإلكتروني باستخدام العنصر النائب **%message%**.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-251">The text of the receipt is inserted into the email by using the **%message%** placeholder.</span></span> <span data-ttu-id="9c4a2-252">للتأكد من أنه تم عرض نص الإيصال بشكل صحيح، قم بإحاطة العنصر النائب **%message%** بعلامات **&lt;pre&gt;** و**&lt;/pre&gt;** لـ HTML.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-252">To ensure that the receipt body is correctly rendered, surround the **%message%** placeholder with HTML **&lt;pre&gt;** and **&lt;/pre&gt;** tags.</span></span>
- <span data-ttu-id="9c4a2-253">يتم تحويل فواصل الأسطر في HTML لرأس وتذييل البريد الإلكتروني إلى علامات **&lt;br /&gt;** في HTML بحيث يتم عرض نص الإيصال بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-253">Line breaks in the HTML for the header and footer of the email are converted to HTML **&lt;br /&gt;** tags so that the receipt body is rendered correctly.</span></span> <span data-ttu-id="9c4a2-254">لحذف المساحة العمودية غير المرغوب فيها في رسائل البريد الإلكتروني الخاصة بالإيصال، قم بإزالة فواصل الأسطر من أي مكان في HTML لا تكون فيه المساحة الرأسية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-254">To eliminate unwanted vertical space in your receipt emails, remove line breaks from any place in the HTML where vertical space isn't required.</span></span>

<span data-ttu-id="9c4a2-255">للحصول على مزيد من المعلومات حول كيفية تكوين إيصالات البريد الإلكتروني، راجع [إعداد إيصالات البريد الإلكتروني](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-255">For more information about how to configure email receipts, see [Set up email receipts](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts).</span></span>

## <a name="upload-the-email-html"></a><span data-ttu-id="9c4a2-256">تحميل HTML للبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c4a2-256">Upload the email HTML</span></span>

<span data-ttu-id="9c4a2-257">بعد إنشاء واختبار HTML لنص الرسالة الخاصة بك، يجب أن يتم تحميله إلى Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-257">After you've created and tested the HTML for your message body, it must be uploaded to Commerce headquarters.</span></span> <span data-ttu-id="9c4a2-258">لا يمكن تصدير HTML الخاص بالبريد الإلكتروني حاليًا.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-258">Currently, email HTML can't be exported.</span></span> <span data-ttu-id="9c4a2-259">لذلك، يجب الاحتفاظ بالنسخة الرئيسية من HTML خارج Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-259">Therefore, you must maintain the master copy of your HTML outside Commerce headquarters.</span></span>

<span data-ttu-id="9c4a2-260">لتحميل HTML لقالب بريد إلكتروني جديد أو محرر، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-260">To upload a new or edited email template HTML, follow these steps.</span></span>

1. <span data-ttu-id="9c4a2-261">في Commerce headquarters، انتقل إلى **Retail and Commerce \> إعداد Headquarters \> قوالب البريد الإلكتروني للمؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-261">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="9c4a2-262">حدد صف اللغة التي تريد إضافة أو استبدال HTML لها.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-262">Select the row for the language that you want to add or replace HTML for.</span></span> <span data-ttu-id="9c4a2-263">بدلا من ذلك، حدد **جديد** لإنشاء صف للغة جديدة.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-263">Alternatively, select **New** to create a row for a new language.</span></span>
1. <span data-ttu-id="9c4a2-264">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-264">Select **Edit**.</span></span>
1. <span data-ttu-id="9c4a2-265">في مربع الحوار الذي يظهر، حدد **استعراض**.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-265">In the dialog box that appears, select **Browse**.</span></span> <span data-ttu-id="9c4a2-266">قم بالاستعراض بحثا عن مستند HTML الذي تريد تحميله، وحدده، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-266">Browse to the HTML document that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="9c4a2-267">ثم حدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-267">Select **Upload**.</span></span>
1. <span data-ttu-id="9c4a2-268">بعد ظهور HTML بالبريد الإلكتروني الخاص بك في نافذة المعاينة، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-268">After your email HTML appears in the preview window, select **OK**.</span></span>
1. <span data-ttu-id="9c4a2-269">تأكد من تحديد خانة الاختيار **يتضمن نص** للصف.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-269">Make sure that the **Has body** check box is selected for the row.</span></span>

<span data-ttu-id="9c4a2-270">إذا كنت قد قمت بالفعل بتكوين Commerce Headquarters لإرسال البريد الإلكتروني، سيتم إرسال بريد إلكتروني جديد أو محدث خاص بك إلى كافة العملاء الذين ينفذون حركة تستدعي الحدث الذي تم تعيينه إلى القالب.</span><span class="sxs-lookup"><span data-stu-id="9c4a2-270">If you've already configured Commerce headquarters to send email, your new or updated email will be sent to all customers who perform a transaction that invokes the event that is mapped to the template.</span></span>

<span data-ttu-id="9c4a2-271">للحصول على مزيد من المعلومات حول كيفية تكوين رسائل البريد الإلكتروني في Dynamics 365 Commerce، راجع [تكوين وإرسال البريد الإلكتروني](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="9c4a2-271">For more information about how to configure emails in Dynamics 365 Commerce, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c4a2-272">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9c4a2-272">Additional resources</span></span> 

[<span data-ttu-id="9c4a2-273">إنشاء ملف تعريف الإخطار بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c4a2-273">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="9c4a2-274">تكوين وإرسال البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c4a2-274">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[<span data-ttu-id="9c4a2-275">إعداد إيصالات بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="9c4a2-275">Set up email receipts</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[<span data-ttu-id="9c4a2-276">إرسال إيصالات البريد الإلكتروني من Modern POS</span><span class="sxs-lookup"><span data-stu-id="9c4a2-276">Send email receipts from Modern POS </span></span>](email-receipts.md)
