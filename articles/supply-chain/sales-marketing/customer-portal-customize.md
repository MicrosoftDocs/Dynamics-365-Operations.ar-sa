---
title: تخصيص مدخل العميل واستخدامه
description: يشرح هذا الموضوع كيفية تخصيص مدخل العميل بعد إضافته إلى نظامك.
author: dasani-madipalli
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ea1fe6ba374c77784c88cf8202bff2eace217b6a
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102676"
---
# <a name="customize-and-use-the-customer-portal"></a><span data-ttu-id="7e4ee-103">تخصيص مدخل العميل واستخدامه</span><span class="sxs-lookup"><span data-stu-id="7e4ee-103">Customize and use the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7e4ee-104">يشرح هذا الموضوع مختلف الصفحات الجاهزة المتوفرة في مدخل العميل.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-104">This topic describes the different pages that available in the Customer portal out of the box.</span></span> <span data-ttu-id="7e4ee-105">وهو يشرح العمل الذي تقوم به الصفحات وكيف يمكن تخصيصها.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-105">It explains what the pages do and how you can customize them.</span></span>

<span data-ttu-id="7e4ee-106">يقدم مدخل العميل بعض صفحات الويب والإجراءات الجاهزة.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-106">The Customer portal offers a few webpages and actions out of the box.</span></span> <span data-ttu-id="7e4ee-107">يوفر مخطط الموقع التالي نظرة عامة على صفحات الويب والإجراءات هذه، والأدوار التي يمكنها تنفيذ الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-107">The following site map provides an overview of those webpages and actions, and the roles that can perform the actions.</span></span>

<span data-ttu-id="7e4ee-108">![مخطط موقع مدخل العميل](media/customer-portal-site-map.png "مخطط موقع مدخل العميل")</span><span class="sxs-lookup"><span data-stu-id="7e4ee-108">![Customer portal site map](media/customer-portal-site-map.png "Customer portal site map")</span></span>

## <a name="typical-customizations"></a><span data-ttu-id="7e4ee-109">عمليات التخصيص النموذجية</span><span class="sxs-lookup"><span data-stu-id="7e4ee-109">Typical customizations</span></span>

<span data-ttu-id="7e4ee-110">ستساعدك المواضيع التالية في التعرف على الأساسيات حول مداخل Power Apps وكيف يمكنك تخصيص المداخل:</span><span class="sxs-lookup"><span data-stu-id="7e4ee-110">The following topics will help you learn the basics about Power Apps portals and how you can customize portals:</span></span>

- <span data-ttu-id="7e4ee-111">[استخدام القوالب](/powerapps/maker/portals/work-with-templates) – يوفر هذا الموضوع نظرة عامة حول كيفية عمل مداخل Power Apps وكيف يمكنك إجراء عمليات تخصيص بسيطة للمداخل.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-111">[Work with templates](/powerapps/maker/portals/work-with-templates) – This topic provides a general overview of how Power Apps portals works and how you can do simple customizations of portals.</span></span>
- <span data-ttu-id="7e4ee-112">[إدارة محتوى المدخل](/dynamics365/portals/manage-portal-content) – يشرح هذا الموضوع كيفية إدارة وتخصيص المحتوى الذي تعرضه في مدخلك.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-112">[Manage portal content](/dynamics365/portals/manage-portal-content) – This topic explains how you can manage and customize the content that you surface in your portal.</span></span>
- <span data-ttu-id="7e4ee-113">[تحرير CSS](/powerapps/maker/portals/edit-css) – يساعدك هذا الموضوع على اجراء المزيد من عمليات التخصيص المعقدة لواجهة المستخدم (UI) في مدخلك.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-113">[Edit CSS](/powerapps/maker/portals/edit-css) – This topic helps you make more complex customizations to the user interface (UI) of your portal.</span></span>
- <span data-ttu-id="7e4ee-114">[إنشاء نسق لمدخلك](/dynamics365/portals/create-theme) – يساعدك هذا الموضوع على إنشاء نسق لواجهة المستخدم في مدخلك.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-114">[Create a theme for your portal](/dynamics365/portals/create-theme) – This topic helps you create a UI theme for your portal.</span></span>
- <span data-ttu-id="7e4ee-115">[إنشاء محتوى المدخل وعرضه بسهولة](/dynamics365/portals/create-expose-portal-content) – يساعدك هذا الموضوع على إدارة البيانات والجداول الأساسية التي تستخدمها لمدخلك.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-115">[Create and expose portal content easily](/dynamics365/portals/create-expose-portal-content) – This topic helps you manage the underlying data and tables that you use for your portal.</span></span>
- <span data-ttu-id="7e4ee-116">[تكوين جهة اتصال لاستخدامها على مدخل](/powerapps/maker/portals/configure/configure-contacts) – يشرح هذا الموضوع كيفية إنشاء أدوار المستخدمين وتخصيصها، وكيفية عمل الأمان والمصادقة في مداخل Power Apps.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-116">[Configure a contact for use on a portal](/powerapps/maker/portals/configure/configure-contacts) – This topic explains how to create and customize user roles, and how security and authentication work in Power Apps portals.</span></span>
- <span data-ttu-id="7e4ee-117">[تكوين الملاحظات لنماذج الجدول ونماذج الويب على المداخل](/powerapps/maker/portals/configure-notes)– يشرح هذا الموضوع كيفية إضافة مستندات ومساحة تخزين إضافية إلى مدخلك.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-117">[Configure notes for table forms and web forms on portals](/powerapps/maker/portals/configure-notes) – This topic explains how to add documents and additional storage to your portal.</span></span>
- <span data-ttu-id="7e4ee-118">[معالجة الأخطاء لموقع ويب للدخل](/powerapps/maker/portals/admin/view-portal-error-log) – يشرح هذا الموضوع كيفية عرض سجلات أخطاء المدخل وتخزينها في حساب مخزن البيانات الثنائية كبيرة الحجم في Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-118">[Error handling for portal website](/powerapps/maker/portals/admin/view-portal-error-log) – This topic explains how to view portal error logs and store them in your Microsoft Azure Blob storage account.</span></span>

## <a name="customize-the-order-creation-process"></a><span data-ttu-id="7e4ee-119">تخصيص عملية إنشاء الأوامر</span><span class="sxs-lookup"><span data-stu-id="7e4ee-119">Customize the order creation process</span></span>

<span data-ttu-id="7e4ee-120">عندما يرسل المستخدم أمرًا باستخدام مدخل العميل، تتم مزامنة الأمر تلقائيًا مع بيئة Dynamics 365 Supply Chain Management المناظرة.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-120">When a user submits an order by using the Customer portal, the order is automatically synced to the corresponding Dynamics 365 Supply Chain Management environment.</span></span> <span data-ttu-id="7e4ee-121">ولأن المستخدم هو عميل خارجي، فإن بعض المعلومات المطلوبة تكون مخفية عنه بشكل مقصود.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-121">Because the user is an external customer, some required information is intentionally hidden from them.</span></span> <span data-ttu-id="7e4ee-122">سيتم ملء هذه المعلومات بشكل تلقائي عند إرسال النموذج.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-122">This information will automatically be filled in when the form is submitted.</span></span>

<span data-ttu-id="7e4ee-123">يبين هذا القسم الطريقة التي يجب أن تستخدمها لإعداد جهات الاتصال لتجنب الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-123">This section shows how you should set up contacts to avoid errors.</span></span> <span data-ttu-id="7e4ee-124">وهو يبين الحقول التي يتم تعيينها تلقائيًا وكيف يمكنك تعديل قيمة هذه الحقول إذا كان من الضروري القيام بذلك.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-124">It explains fields that are automatically set and how you can modify the value of those fields if you must.</span></span>

### <a name="the-out-of-box-order-creation-process"></a><span data-ttu-id="7e4ee-125">عملية إنشاء الأوامر الجاهزة</span><span class="sxs-lookup"><span data-stu-id="7e4ee-125">The out-of-box order creation process</span></span>

<span data-ttu-id="7e4ee-126">فيما يلي الخطوات القياسية التي يجب اتباعها لإرسال أمر من مدخل العميل.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-126">Here are the standard steps for submitting an order from the Customer portal.</span></span>

1. <span data-ttu-id="7e4ee-127">في الصفحة الرئيسية، حدد اللوحة **إنشاء أمر** لفتح معالج **إنشاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-127">On the home page, select the **Create order** tile to open the **Create Order** wizard.</span></span>
1. <span data-ttu-id="7e4ee-128">في الصفحة **معلومات الأمر**، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="7e4ee-128">On the **Order Information** page, set the following fields:</span></span>

    - <span data-ttu-id="7e4ee-129">**تاريخ التسليم المطلوب** – حدد تاريخ التسليم.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-129">**Requested receipt date** – Specify the date of delivery.</span></span>
    - <span data-ttu-id="7e4ee-130">**عنوان التسليم** – ادخل العنوان الذي يجب تسليم الأمر اليه.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-130">**Delivery address** – Enter the address that the order should be delivered to.</span></span>
    - <span data-ttu-id="7e4ee-131">**الشركة** – حدد اسم شركة العميل.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-131">**Company** – Select the name of the customer company.</span></span> <span data-ttu-id="7e4ee-132">يتم تعيين هذا الحقل بشكل تلقائي إلى المستخدمين من غير المسؤولين.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-132">This field is automatically set for non-admin users.</span></span>
    - <span data-ttu-id="7e4ee-133">**رقم الطلب** – أدخل رقم طلب الأمر.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-133">**Requisition number** – Enter the requisition number of the order.</span></span> <span data-ttu-id="7e4ee-134">هذا الحقل غير مطلوب.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-134">This field isn't required.</span></span>
    - <span data-ttu-id="7e4ee-135">**شحن إلى البلد/المنطقة** – أدخل البلد أو المنطقة حيث سيتم تسليم الأصناف.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-135">**Ship to country/region** – Enter the country or region that the items will be delivered to.</span></span> <span data-ttu-id="7e4ee-136">يتم تعيين هذا الحقل بشكل تلقائي إلى المستخدمين من غير المسؤولين.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-136">This field is automatically set for non-admin users.</span></span>

    <span data-ttu-id="7e4ee-137">![صفحة معلومات الأمر](media/customer-portal-order-information.png "صفحة معلومات الأمر")</span><span class="sxs-lookup"><span data-stu-id="7e4ee-137">![Order information page](media/customer-portal-order-information.png "Order information page")</span></span>

1. <span data-ttu-id="7e4ee-138">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-138">Select **Next**.</span></span>
1. <span data-ttu-id="7e4ee-139">في صفحة **الأصناف**، حدد **إضافة صنف**.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-139">On the **Items** page, select **Add Item**.</span></span>

    <span data-ttu-id="7e4ee-140">![صفحة الأصناف](media/customer-portal-items.png "صفحة الأصناف")</span><span class="sxs-lookup"><span data-stu-id="7e4ee-140">![Items page](media/customer-portal-items.png "Items page")</span></span>

1. <span data-ttu-id="7e4ee-141">في مربع الحوار **معلومات الصنف**، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="7e4ee-141">In the **Item Information** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="7e4ee-142">**اسم المنتج** – ابحث عن منتج وحدده لإضافته إلى الأمر.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-142">**Product Name** – Find and select a product to add to the order.</span></span>
    - <span data-ttu-id="7e4ee-143">**الكمية** – أدخل كمية المنتج المحدد.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-143">**Quantity** – Enter the quantity of the selected product.</span></span>
    - <span data-ttu-id="7e4ee-144">**الوحدة** – حدد وحدة القياس (على سبيل المثال، **كل واحد** أو **كجم** أو **صندوق**).</span><span class="sxs-lookup"><span data-stu-id="7e4ee-144">**Unit** – Specify the unit of measure (for example, **ea.**, **kgs**, or **box**).</span></span>
    - <span data-ttu-id="7e4ee-145">**المبلغ الصافي المقدّر** – يتم حساب القيمة كالسعر المقدّر للصنف × الكمية للوحدة المحددة.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-145">**Estimated net amount** – The value is calculated as the estimated price of the item × the quantity for the selected unit.</span></span>

    <span data-ttu-id="7e4ee-146">![مربع الحوار "معلومات الصنف"](media/customer-portal-item-information.png "مربع الحوار &quot;معلومات الصنف&quot;")</span><span class="sxs-lookup"><span data-stu-id="7e4ee-146">![Item Information dialog box](media/customer-portal-item-information.png "Item Information dialog box")</span></span>

1. <span data-ttu-id="7e4ee-147">حدد **إرسال** لإضافة الصنف إلى الأمر.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-147">Select **Submit** to add the item to the order.</span></span>
1. <span data-ttu-id="7e4ee-148">كرر الخطوات من 4 إلى 6 حتى إضافة جميع الأصناف التي تريد طلبها.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-148">Repeat steps 4 through 6 until you've added all the items that you want to order.</span></span>
1. <span data-ttu-id="7e4ee-149">عند الانتهاء من إضافة الأصناف، حدد **التالي** على صفحة **الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-149">When you've finished adding items, select **Next** on the **Items** page.</span></span>
1. <span data-ttu-id="7e4ee-150">توفر صفحة **معلومات الأمر** ملخصًا للأمر.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-150">The **Order Information** page provides a summary of the order.</span></span> <span data-ttu-id="7e4ee-151">راجع محتويات الأمر وتفاصيل التسليم.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-151">Review the order contents and delivery details.</span></span> <span data-ttu-id="7e4ee-152">إذا بدا كل شيء صحيحًا، فحدد **إرسال** لإرسال الأمر.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-152">If everything looks correct, select **Submit** to submit the order.</span></span>

    <span data-ttu-id="7e4ee-153">![صفحة معلومات الأمر المكتمل](media/customer-portal-order-submit.png "صفحة معلومات الأمر المكتمل")</span><span class="sxs-lookup"><span data-stu-id="7e4ee-153">![Completed order information page](media/customer-portal-order-submit.png "Completed order information page")</span></span>

### <a name="standard-data-setup"></a><span data-ttu-id="7e4ee-154">إعداد البيانات القياسية</span><span class="sxs-lookup"><span data-stu-id="7e4ee-154">Standard data setup</span></span>

<span data-ttu-id="7e4ee-155">للمساعدة في ضمان تجربة سلسلة للمستخدم، يقوم مدخل العميل بملء القيم لعدة حقول مطلوبة بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-155">To help ensure a smooth user experience, the Customer portal automatically fills in values for several required fields.</span></span> <span data-ttu-id="7e4ee-156">تستند هذه القيم إلى المعلومات الموجودة في سجل جهة الاتصال الخاصة بالعميل الذي يرسل الأمر.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-156">These values are based on information in the contact record of the customer who is submitting the order.</span></span>

<span data-ttu-id="7e4ee-157">بالنسبة إلى كل [صف جهة اتصال](/powerapps/maker/portals/configure/configure-contacts) ينتمي إلى عميل سيقوم باستخدام مدخل العميل لإرسال الأوامر، يجب تحديد القيم للحقول المطلوبة التالية.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-157">For each [contact row](/powerapps/maker/portals/configure/configure-contacts) that belongs to a customer who will use the Customer portal to submit orders, values must be specified for the following required fields.</span></span> <span data-ttu-id="7e4ee-158">والا، ستحدث أخطاء.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-158">Otherwise, errors will occur.</span></span>

- <span data-ttu-id="7e4ee-159">**الشركة** – الكيان القانوني الذي ينتمي إليه الأمر</span><span class="sxs-lookup"><span data-stu-id="7e4ee-159">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="7e4ee-160">**العميل المحتمل** – حساب العميل المرتبط بالأمر.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-160">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="7e4ee-161">**قائمة الأسعار** – قائمة الأسعار المخصصة للعميل</span><span class="sxs-lookup"><span data-stu-id="7e4ee-161">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="7e4ee-162">**العملة** – عملة السعر</span><span class="sxs-lookup"><span data-stu-id="7e4ee-162">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="7e4ee-163">**شحن إلى البلد/المنطقة** – البلد أو المنطقة حيث سيتم تسليم الأصناف.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-163">**Ship to country/region** – The country or region that the items will be delivered to</span></span>

<span data-ttu-id="7e4ee-164">يتم تعيين الحقول التالية بشكل تلقائي إلى جدول أمر المبيعات:</span><span class="sxs-lookup"><span data-stu-id="7e4ee-164">The following fields are automatically set for the sales order table:</span></span>

- <span data-ttu-id="7e4ee-165">**اللغة** – لغة الأمر (افتراضيًا، تؤخذ القيمة من سجل جهة الاتصال.)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-165">**Language** – The language of the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7e4ee-166">**شحن إلى البلد/المنطقة** – البلد أو المنطقة حيث سيتم تسليم الأصناف (بشكل افتراضي، تؤخذ القيمة من سجل جهة الاتصال.)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-166">**Ship to country/region** – The country or region that the items will be delivered to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7e4ee-167">**جهة الاتصال‬** – المستخدم الذي يمكن الاتصال به للحصول على معلومات حول الأمر (افتراضيًا، تؤخذ القيمة من سجل جهة الاتصال.)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-167">**Contact person** – The user who can be contacted for information about the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7e4ee-168">**الشركة** – الكيان القانوني الذي ينتمي اليه الأمر (بشكل افتراضيًا، تؤخذ القيمة من سجل جهة الاتصال.)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-168">**Company** – The legal entity that the order belongs to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7e4ee-169">**العميل المحتمل** – حساب العميل المرتبط بالأمر (افتراضيًا، تؤخذ القيمة من سجل جهة الاتصال.)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-169">**Potential customer** – The customer account that is associated with the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7e4ee-170">**فاتورة العميل** – حساب الفوترة المرتبط بالأمر (افتراضيًا، تؤخذ القيمة من سجل جهة الاتصال.)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-170">**Invoice customer** – The billing account of the order (The default value is the potential customer from the contact record.)</span></span>
- <span data-ttu-id="7e4ee-171">**اسم أمر المبيعات** – اسم أمر المبيعات (القيمة الافتراضية هي **أمر مبيعات**.)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-171">**Sales order name** – The name of the sales order (The default value is **sales order**.)</span></span>
- <span data-ttu-id="7e4ee-172">**العملة** – عملة السعر (افتراضيًا، تؤخذ القيمة من سجل جهة الاتصال.)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-172">**Currency** – The currency of the price (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7e4ee-173">**قائمة الأسعار** – قائمة الأسعار المخصصة للعميل (افتراضيًا، تؤخذ القيمة من سجل جهة الاتصال.)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-173">**Price list** – The custom price list for the customer (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7e4ee-174">**وصف عنوان التسليم** – عنوان التسليم الخاص بأمر المبيعات (القيمة الافتراضية هي **وصف عنوان التسليم** .)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-174">**Delivery address description** – The delivery address of the sales order (The default value is **delivery address description**.)</span></span>

### <a name="modify-the-order-creation-process"></a><span data-ttu-id="7e4ee-175">تعديل عملية إنشاء الأوامر</span><span class="sxs-lookup"><span data-stu-id="7e4ee-175">Modify the order creation process</span></span>

<span data-ttu-id="7e4ee-176">يمكنك تعديل مظهر واجهة المستخدم ومدخل العميل إذا لم تقم بتغيير عملية إنشاء الأوامر الأساسية.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-176">You can freely modify the appearance and UI of the Customer portal if you don't change the basic order creation process.</span></span> <span data-ttu-id="7e4ee-177">إذا أردت تغيير عملية إنشاء الأوامر الأساسية، ثمة نقاط قليلة يجب أخذها في الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-177">If you want to change the order creation process, there are a few points that you must keep in mind.</span></span>

<span data-ttu-id="7e4ee-178">لا تقم بإزالة الأعمدة التالية من جدول أمر العمل في Microsoft Dataverse، لأنها مطلوبة لإنشاء أمر مبيعات في الكتابة المزدوجة:</span><span class="sxs-lookup"><span data-stu-id="7e4ee-178">Don't remove the following columns from the sales order table in Microsoft Dataverse, because they are required to create a sales order in dual-write:</span></span>

- <span data-ttu-id="7e4ee-179">**الشركة** – الكيان القانوني الذي ينتمي إليه الأمر</span><span class="sxs-lookup"><span data-stu-id="7e4ee-179">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="7e4ee-180">**الاسم‏‎** – اسم أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="7e4ee-180">**Name** – The name of the sales order</span></span>
- <span data-ttu-id="7e4ee-181">**العملة** – عملة السعر</span><span class="sxs-lookup"><span data-stu-id="7e4ee-181">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="7e4ee-182">**قائمة الأسعار** – قائمة الأسعار المخصصة للعميل</span><span class="sxs-lookup"><span data-stu-id="7e4ee-182">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="7e4ee-183">**شحن إلى البلد/المنطقة** – البلد أو المنطقة حيث سيتم تسليم الأصناف.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-183">**Ship to country/region** – The country or region that the items will be delivered to</span></span>
- <span data-ttu-id="7e4ee-184">**العميل المحتمل** – حساب العميل المرتبط بالأمر.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-184">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="7e4ee-185">**اللغة** – لغة الأمر (عادةً ما تكون هذه اللغة لغة العميل المحتمل.)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-185">**Language** – The language of the order (Typically, this language is the language of the potential customer.)</span></span>
- <span data-ttu-id="7e4ee-186">**وصف عنوان التسليم** – عنوان التسليم الخاص بأمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="7e4ee-186">**Delivery address description** – The delivery address of the sales order</span></span>

<span data-ttu-id="7e4ee-187">بالنسبة للأصناف، الأعمدة التالية مطلوبة:</span><span class="sxs-lookup"><span data-stu-id="7e4ee-187">For items, the following columns are required:</span></span>

- <span data-ttu-id="7e4ee-188">**المنتج** – المنتج المطلوب طلبه</span><span class="sxs-lookup"><span data-stu-id="7e4ee-188">**Product** – The product to order</span></span>
- <span data-ttu-id="7e4ee-189">**الكمية** – كمية المنتج المحدد.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-189">**Quantity** – The quantity of the selected product</span></span>
- <span data-ttu-id="7e4ee-190">**الوحدة** – وحدة القياس (على سبيل المثال، **كل واحد** أو **كجم** أو **صندوق**)</span><span class="sxs-lookup"><span data-stu-id="7e4ee-190">**Unit** – The unit of measure (for example, **ea.**, **kgs**, or **box**)</span></span>
- <span data-ttu-id="7e4ee-191">**شحن إلى بلد/منطقة** – بلد أو منطقة التسليم</span><span class="sxs-lookup"><span data-stu-id="7e4ee-191">**Ship to country/region** – The country or region of delivery</span></span>
- <span data-ttu-id="7e4ee-192">**وصف عنوان التسليم** – عنوان التسليم الخاص بالأمر</span><span class="sxs-lookup"><span data-stu-id="7e4ee-192">**Delivery address description** – The delivery address of the order</span></span>

<span data-ttu-id="7e4ee-193">يجب أن تتأكد من أن مدخل العميل يرسل القيم لجميع هذه الأعمدة.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-193">You must make sure that your Customer portal somehow submits values for all these columns.</span></span>

<span data-ttu-id="7e4ee-194">إذا أردت إضافة الأعمدة إلى الصفحة، أو إزالة الأعمدة، راجع [إنشاء نماذج إنشاء سريعة أو تحريرها للحصول على تجربة إدخال بيانات مبسطة](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span><span class="sxs-lookup"><span data-stu-id="7e4ee-194">If you want to add columns to the page, or remove columns, see [Create or edit quick create forms for a streamlined data entry experience](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span></span>

<span data-ttu-id="7e4ee-195">إذا أردت تغيير طريقة الإعداد المسبق للأعمدة وكيفية تعيين القيم عند حفظ الصفحة، راجع المعلومات التالية في وثائق مداخل Power Apps:</span><span class="sxs-lookup"><span data-stu-id="7e4ee-195">If you want to change how columns are preset and how values are set when the page is saved, see the following information in the Power Apps portals documentation:</span></span>

- [<span data-ttu-id="7e4ee-196">ملء الحق بشكل مسبق</span><span class="sxs-lookup"><span data-stu-id="7e4ee-196">Prepopulate field</span></span>](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [<span data-ttu-id="7e4ee-197">تعيين القيمة عند الحفظ</span><span class="sxs-lookup"><span data-stu-id="7e4ee-197">Set Value On Save</span></span>](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a><span data-ttu-id="7e4ee-198">تخصيص الصفحة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="7e4ee-198">Customize the home page</span></span>

<span data-ttu-id="7e4ee-199">كافة عناصر التحكم الموجودة في مدخل العميل هي عناصر تحكم مضمنه في مداخل Power Apps.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-199">All the controls in the Customer portal are built-in Power Apps portals controls.</span></span> <span data-ttu-id="7e4ee-200">يمكنك تخصيصها باتباع الخطوات الموجودة في [إنشاء صفحة](/powerapps/maker/portals/compose-page) في وثائق مداخل Power Apps.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-200">You can customize them by following the steps in [Compose a page](/powerapps/maker/portals/compose-page) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="7e4ee-201">يتم استخدام عنصر التحكم المخصص الوحيد المضمن في قالب مدخل العميل لإنشاء اللوحات في الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-201">The only custom control that is included in the Customer portal template is used to create the tiles on the home page.</span></span>

<span data-ttu-id="7e4ee-202">![لوحات في الصفحة الرئيسية](media/customer-portal-home-page-tiles.png "لوحات في الصفحة الرئيسية")</span><span class="sxs-lookup"><span data-stu-id="7e4ee-202">![Tiles on the home page](media/customer-portal-home-page-tiles.png "Tiles on the home page")</span></span>

<span data-ttu-id="7e4ee-203">لتعديل اللوحات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="7e4ee-203">To modify the tiles, follow these steps.</span></span>

1. <span data-ttu-id="7e4ee-204">افتح [تطبيق إدارة المدخل](/powerapps/maker/portals/configure/configure-portal).</span><span class="sxs-lookup"><span data-stu-id="7e4ee-204">Open the [Portal Management app](/powerapps/maker/portals/configure/configure-portal).</span></span>
1. <span data-ttu-id="7e4ee-205">في جزء التنقل إلى اليمين، حدد **قوالب الصفحة**.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-205">In the navigation pane on the left, select **Page Templates**.</span></span>

    <span data-ttu-id="7e4ee-206">![جزء التنقل في إدارة المدخل](media/customer-portal-nav.png "جزء التنقل في إدارة المدخل")</span><span class="sxs-lookup"><span data-stu-id="7e4ee-206">![Portal Management navigation pane](media/customer-portal-nav.png "Portal Management navigation pane")</span></span>

1. <span data-ttu-id="7e4ee-207">حدد قالب الصفحة باسم **الصفحة الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-207">Select the page template that is named **Home**.</span></span>
1. <span data-ttu-id="7e4ee-208">في حقل **قالب ويب**، حدد ارتباط **الصفحة الرئيسية** لفتح التعليمات البرمجية المصدر لهذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-208">In the **Web Template** field, select the **Home** link to open the source code for that page.</span></span>

    <span data-ttu-id="7e4ee-209">![حقل قالب ويب](media/customer-portal-web-template.png "حقل قالب ويب")</span><span class="sxs-lookup"><span data-stu-id="7e4ee-209">![Web Template field](media/customer-portal-web-template.png "Web Template field")</span></span>

1. <span data-ttu-id="7e4ee-210">يجب أن ترى الآن كل التعليمات البرمجية المصدر للصفحة الرئيسية ويمكنك تعديلها وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="7e4ee-210">You should now see all the source code for the home page and can modify it as you require.</span></span>

## <a name="resources"></a><span data-ttu-id="7e4ee-211">الموارد</span><span class="sxs-lookup"><span data-stu-id="7e4ee-211">Resources</span></span>

<span data-ttu-id="7e4ee-212">لمعرفة المزيد حول كيفية إعداد مدخل العميل وتخصيصه، راجع الموارد التالية:</span><span class="sxs-lookup"><span data-stu-id="7e4ee-212">To learn more about how you can set up and customize the Customer portal, see the following resources:</span></span>

- [<span data-ttu-id="7e4ee-213">وثائق مداخل Power Apps</span><span class="sxs-lookup"><span data-stu-id="7e4ee-213">Power Apps portals documentation</span></span>](/powerapps/maker/portals/overview)
- [<span data-ttu-id="7e4ee-214">وثائق الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="7e4ee-214">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [<span data-ttu-id="7e4ee-215">حول دورة حياة المدخل</span><span class="sxs-lookup"><span data-stu-id="7e4ee-215">About portal lifecycle</span></span>](/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="7e4ee-216">ترقية مدخل</span><span class="sxs-lookup"><span data-stu-id="7e4ee-216">Upgrade a portal</span></span>](/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="7e4ee-217">ترحيل تكوين المدخل</span><span class="sxs-lookup"><span data-stu-id="7e4ee-217">Migrate portal configuration</span></span>](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="7e4ee-218">إدارة دورة حياة الحل: تطبيقات Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="7e4ee-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]