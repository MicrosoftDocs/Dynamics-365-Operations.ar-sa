---
title: تحرير وتدقيق الأوامر عبر الإنترنت وحركات أمر العميل غير المتزامنة
description: يوضح هذا الموضوع كيفيه تحرير وتدقيق الأوامر عبر الإنترنت وحركات أمر العميل غير المتزامنة في Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9f2db25c8897662baa177752d0c5fc4ac6178a4
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458410"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="22947-103">تحرير وتدقيق الأوامر عبر الإنترنت وحركات أمر العميل غير المتزامنة</span><span class="sxs-lookup"><span data-stu-id="22947-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22947-104">يوضح هذا الموضوع كيفيه تحرير وتدقيق الأوامر عبر الإنترنت وحركات أمر العميل غير المتزامنة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="22947-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="22947-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="22947-105">Overview</span></span>

<span data-ttu-id="22947-106">بين الإصدارين التجاريين 10.0.5 و10.0.6، تمت إضافة الدعم لتحرير حركات الدفع نقدًا والاستلام فورًا‬‬‏‫ (مثل المبيعات والمرتجعات) وحركات إدارة النقد (مثل إدخال معوم وإزالة العطاء).</span><span class="sxs-lookup"><span data-stu-id="22947-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="22947-107">في Commerce الإصدار 10.0.7، تمت إضافة الدعم لتحرير حركات الأوامر عبر الإنترنت وحركات أوامر العميل غير المتزامنة.</span><span class="sxs-lookup"><span data-stu-id="22947-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="22947-108">تحرير حركات الأمر وتدقيقها</span><span class="sxs-lookup"><span data-stu-id="22947-108">Edit and audit order transactions</span></span>

<span data-ttu-id="22947-109">لتحرير حركات الأمر وتدقيقها في المركز الرئيسي لـ Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="22947-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="22947-110">قم بتثبيت [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="22947-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="22947-111">في صفحة **معلمات البيع بالتجزئة** ، في علامة التبويب **أوامر العملاء** ، في علامة التبويب السريعة **الأمر** ، حدد كود الاحتجاز لـ **كود الاحتجاز لأخطاء مزامنة الأمر**.</span><span class="sxs-lookup"><span data-stu-id="22947-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="22947-112">افتح مساحة العمل **ماليات المتجر**.</span><span class="sxs-lookup"><span data-stu-id="22947-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="22947-113">يوفر الإطارين المتجانبين **أخطاء مزامنة الأمر عبر الإنترنت** و **أخطاء مزامنة أمر العميل** عرضًا مُصفى مسبقًا لصفحة حركة البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="22947-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="22947-114">يعرض كل منها سجلات الحركات التي تحتوي علي مزامنة فاشلة لنوع الأمر المطابق.</span><span class="sxs-lookup"><span data-stu-id="22947-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="22947-115">افتح صفحة **أخطاء مزامنة الأوامر عبر الإنترنت** أو صفحة **أخطاء مزامنة أوامر العميل**.</span><span class="sxs-lookup"><span data-stu-id="22947-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="22947-116">حدد سجلاً لعرض تفاصيل خطا المزامنة.</span><span class="sxs-lookup"><span data-stu-id="22947-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="22947-117">توفر علامة التبويب السريعة **حالة المزامنة** تفاصيل الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="22947-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="22947-118">حالة أمر معلق</span><span class="sxs-lookup"><span data-stu-id="22947-118">Pending order status</span></span>
    - <span data-ttu-id="22947-119">تفاصيل خطأ الأمر</span><span class="sxs-lookup"><span data-stu-id="22947-119">Order error details</span></span>
    - <span data-ttu-id="22947-120">تاريخ ووقت التعديل</span><span class="sxs-lookup"><span data-stu-id="22947-120">Modified date and time</span></span>
    - <span data-ttu-id="22947-121">عدد مرات إعادة المحاولة</span><span class="sxs-lookup"><span data-stu-id="22947-121">Retry count</span></span>

1. <span data-ttu-id="22947-122">إذا كانت تشير تفاصيل الخطأ إلى وجوب إصلاح السجل، فحدد **وظيفة Office الإضافية**، ثم حدد **تحرير الحركة المحددة**.</span><span class="sxs-lookup"><span data-stu-id="22947-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="22947-123">يتم فتح ملف Excel يعرض تفاصيل الحركة المحددة.</span><span class="sxs-lookup"><span data-stu-id="22947-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="22947-124">إذا كانت الحركة التي يتم تحريرها هي حركة أمر عبر الإنترنت، سيحتوي ملف Excel علي أوراق العمل التالية:</span><span class="sxs-lookup"><span data-stu-id="22947-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="22947-125">**الحركة**: تحتوي ورقة العمل هذه على تفاصيل الرأس الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="22947-126">**حركة المبيعات**: تحتوي ورقة العمل هذه على تفاصيل بنود الحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="22947-127">**حركات الدفع**: تتضمن ورقة العمل هذه تفاصيل بنود الدفع الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="22947-128">**حركات الخصم** - تتضمن ورقة العمل هذه تفاصيل تتعلق بالخصومات الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="22947-129">**الحركات الضريبية** : تتضمن ورقة العمل هذه تفاصيل تتعلق بالضريبة ذات الصلة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="22947-130">**حركات المصروفات**: تتضمن ورقة العمل هذه ببيانات المصاريف ذات الصلة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="22947-131">إذا كانت الحركة التي يتم تحريرها هي حركة لأمر العميل غير متزامنة‬، سيحتوي ملف Excel علي أوراق العمل التالية:</span><span class="sxs-lookup"><span data-stu-id="22947-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="22947-132">**البنود**: تحتوي ورقة العمل هذه على الرأس وتفاصيل بنود الحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="22947-133">**المدفوعات**: تتضمن ورقة العمل هذه تفاصيل بنود الدفع الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="22947-134">**الخصومات**: تتضمن ورقة العمل هذه تفاصيل تتعلق بالخصومات الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="22947-135">**الضرائب**: تتضمن ورقة العمل هذه تفاصيل تتعلق بالضرائب الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="22947-136">**المصاريف**: تتضمن ورقة العمل هذه بيانات تتعلق بمصاريف الحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="22947-137">في ملف Excel، في الحقل **حالة الأمر المعلق** ، ادخل **تحرير**، ثم قم بنشر التغيير.</span><span class="sxs-lookup"><span data-stu-id="22947-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="22947-138">وبهذه الطريقة، تمنع مهمة **مزامنة الأمر** التي تعمل في وضع الدُفعات من تخطي هذا السجل أثناء المعالجة.</span><span class="sxs-lookup"><span data-stu-id="22947-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="22947-139">في ملف Excel، قم بتعديل الحقول المناسبة، ثم قم بتحميل البيانات مرة أخرى إلى المركز الرئيسي لـ Commerce باستخدام وظيفة النشر الخاصة بالوظيفة الإضافية Dynamics Excel.</span><span class="sxs-lookup"><span data-stu-id="22947-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="22947-140">ستنعكس التغييرات في النظام بعد نشر البيانات.</span><span class="sxs-lookup"><span data-stu-id="22947-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="22947-141">أثناء عملية النشر، لا يتم إجراء عملية التحقق من صحة التغييرات التي يُجريها المستخدمون.</span><span class="sxs-lookup"><span data-stu-id="22947-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="22947-142">يمكنك عرض مسار تدقيق كامل للتغييرات عن طريق تحديد **عرض مسار التدقيق** في عنوان **حركة البيع بالتجزئة** للتغييرات على مستوى الرأس، وفي القسم والسجل ذي الصلة في صفحة الحركة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="22947-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="22947-143">علي سبيل المثال، سيتم عرض كافة التغييرات المرتبطة ببنود المبيعات في صفحة **حركات المبيعات** ، وسيتم عرض كافة التغييرات المرتبطة بالمدفوعات في صفحة **حركات الدفع**.</span><span class="sxs-lookup"><span data-stu-id="22947-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="22947-144">يتم الاحتفاظ بتفاصيل التدقيق للتغييرات على النحو التالي:</span><span class="sxs-lookup"><span data-stu-id="22947-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="22947-145">تاريخ ووقت التعديل</span><span class="sxs-lookup"><span data-stu-id="22947-145">Modified date and time</span></span>
    - <span data-ttu-id="22947-146">الحقل</span><span class="sxs-lookup"><span data-stu-id="22947-146">Field</span></span>
    - <span data-ttu-id="22947-147">قيمة قديمة</span><span class="sxs-lookup"><span data-stu-id="22947-147">Old value</span></span>
    - <span data-ttu-id="22947-148">قيمة جديدة</span><span class="sxs-lookup"><span data-stu-id="22947-148">New value</span></span>
    - <span data-ttu-id="22947-149">تعديل بواسطة</span><span class="sxs-lookup"><span data-stu-id="22947-149">Modified by</span></span>

1. <span data-ttu-id="22947-150">بعد اجراء التغييرات ونشرها، حدد **مزامنة الأمر** لبدء عملية المزامنة علي الفور.</span><span class="sxs-lookup"><span data-stu-id="22947-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="22947-151">وبدلاً من ذلك، يمكنك انتظار عملية المزامنة التي تعمل في الوضع الدفعي لمعالجه الحركة.</span><span class="sxs-lookup"><span data-stu-id="22947-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="22947-152">وبشكل افتراضي، بعد مزامنة الأوامر بنجاح، يتم وضعها في حاله الاحتجاز، وذلك استنادًا إلى كود الاحتجاز المحدد في محددات Commerce.</span><span class="sxs-lookup"><span data-stu-id="22947-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="22947-153">يتعين إزالة التعليق على الأوامر قبل أن تتم معالجة الأوامر بشكل أكبر للوفاء بها أو عمليات أخرى.</span><span class="sxs-lookup"><span data-stu-id="22947-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22947-154">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="22947-154">Additional resources</span></span>

[<span data-ttu-id="22947-155">تحرير وتدقيق حركات الدفع نقدًا والاستلام فورًا وإدارة النقد</span><span class="sxs-lookup"><span data-stu-id="22947-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="22947-156">تحرير الأبعاد المالية لحركات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="22947-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="22947-157">إنشاء مصنف Excel لتحرير حركات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="22947-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="22947-158">إضافة الحقول إلى مصنف Excel لتحرير حركات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="22947-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
