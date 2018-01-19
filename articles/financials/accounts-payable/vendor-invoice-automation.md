---
title: "التنفيذ التلقائي لفاتورة المورّد"
description: "يشرح هذا الموضوع الميزات المتوفرة للتنفيذ التلقائي لفواتير المورّد من نهاية إلى نهاية، حتى الفواتير التي تحتوي على مرفقات."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 8140b452e8f9c7b94b4466a57100a1559cf0919e
ms.contentlocale: ar-sa
ms.lasthandoff: 01/19/2018

---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="5e6d9-103">التنفيذ التلقائي لفاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="5e6d9-103">Vendor invoice automation</span></span>

<span data-ttu-id="5e6d9-104">يشرح هذا الموضوع الميزات المتوفرة للتنفيذ التلقائي لفواتير المورّد من نهاية إلى نهاية، حتى الفواتير التي تحتوي على مرفقات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="5e6d9-105">في أغلب الأحيان، تحدد الشركات التي تريد تنظيم عمليات حساباتها الدائنة عملية معالجة الفواتير على أنها إحدى أهم النواحي التي يجب أن تكون أكثر كفاءة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="5e6d9-106">في الكثير من الحالات، تقوم هذه الشركات بإحالة عملية معالجة الفواتير الورقية إلى موفر خارجي لخدمة التعرف البصري على الحروف (OCR).</span><span class="sxs-lookup"><span data-stu-id="5e6d9-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="5e6d9-107">بعد ذلك، تتلقى بيانات تعريف الفواتير التي يستطيع الجهاز قراءتها مع صورة ممسوحة ضوئيًا لكل فاتورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="5e6d9-108">للمساعدة في عملية التنفيذ التلقائي هذه، يتم عندئذٍ إنشاء حل "الميل الأخير" لتمكين استهلاك هذه النتائج الملموسة في نظام الفوترة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="5e6d9-109">يمكّن الآن Microsoft Dynamics 365 for Finance and Operations, Enterprise edition التنفيذ التلقائي "الميل الأخير" الجاهز، عبر حل التنفيذ التلقائي للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-109">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition now enables this “last mile” automation out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="5e6d9-110">سياق الحل</span><span class="sxs-lookup"><span data-stu-id="5e6d9-110">Solution context</span></span>

<span data-ttu-id="5e6d9-111">يمكّن حل التنفيذ التلقائي للفواتير واجهة قياسية يمكنها قبول بيانات تعريف الفواتير لرأس الفاتورة وبنود الفاتورة، وكذلك المرفقات التي تنطبق على الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="5e6d9-112">سيتمكن أي نظام خارجي يمكنه إنشاء نتائج ملموسة تتوافق مع هذه الواجهة من إرسال موجز ويب إلى Finance and Operations لإجراء معالجة تلقائية للفواتير والمرفقات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed into Finance and Operations for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="5e6d9-113">يبين الرسم التوضيحي التالي سيناريو تكامل نموذجي حيث عقدت شركة التعمير شراكة مع موفر خدمات التعرف الضوئي على الحروف لمعالجة فواتير المورّد.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="5e6d9-114">الموردون في شركة التعمير يرسلون الفواتير إلى موفر الخدمة بالبريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="5e6d9-115">من خلال معالجة التعرف الضوئي على الحروف، ينشئ موفر الخدمة بيانات تعريف الفواتير (الرأس و/أو البنود) وصورة ممسوحة ضوئيًا للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="5e6d9-116">ثم تقوم طبقة تكامل بتحويل هذه النتائج الملموسة لتمكين Finance and Operations من استعمالها.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-116">An integration layer then transforms these artifacts so that Finance and Operations can consume them.</span></span>

![سيناريو التكامل النموذجي](media/vendor_invoice_automation_01.png)

<span data-ttu-id="5e6d9-118">ستكون أشكال مختلفة من السيناريو السابق ممكنة إذا كان تكامل الفواتير ضروريًا.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="5e6d9-119">يُعتبر ترحيل البيانات حالة استخدام أخرى حيث يمكن استخدام هذه الواجهة لإنشاء الفواتير والمرفقات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-119">Data migration is another use case where this interface can be used to create invoices and attachments in Finance and Operations.</span></span>

### <a name="solution-components"></a><span data-ttu-id="5e6d9-120">مكونات الحل</span><span class="sxs-lookup"><span data-stu-id="5e6d9-120">Solution components</span></span>

<span data-ttu-id="5e6d9-121">يتكون الحل من المكونات التالية:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="5e6d9-122">كيانات البيانات لرأس الفاتورة وبنود الفاتورة ومرفقات الفاتورة</span><span class="sxs-lookup"><span data-stu-id="5e6d9-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="5e6d9-123">معالجة الاستثناءات للفواتير</span><span class="sxs-lookup"><span data-stu-id="5e6d9-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="5e6d9-124">عارض المرفقات جنبًا إلى جنب في الفواتير</span><span class="sxs-lookup"><span data-stu-id="5e6d9-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="5e6d9-125">توفر بقية هذا الموضوع وصفًا مفصلا لمكونات هذا الحل.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="5e6d9-126">كيانات البيانات</span><span class="sxs-lookup"><span data-stu-id="5e6d9-126">Data entities</span></span>

<span data-ttu-id="5e6d9-127">حزمة البيانات عبارة عن وحدة عمل يجب إرسالها إلى Finance and Operations، لتمكين إنشاء رؤوس الفواتير وبنود الفواتير ومرفقات الفواتير.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-127">A data package is the unit of work that must be sent to Finance and Operations, so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="5e6d9-128">تستخدم كيانات البيانات التالية للعناصر الملموسة التي تشكل حزمة البيانات:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="5e6d9-129">رأس فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="5e6d9-129">Vendor invoice header</span></span>
+ <span data-ttu-id="5e6d9-130">سطر فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="5e6d9-130">Vendor invoice line</span></span>
+ <span data-ttu-id="5e6d9-131">مرفق مستند فاتورة المورد</span><span class="sxs-lookup"><span data-stu-id="5e6d9-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="5e6d9-132">مرفق مستند فاتورة المورد عبارة عن كيان بيانات جديد تم تقديمه كجزء من هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="5e6d9-133">تم تعديل كيان رأس فاتورة المورد بحيث يدعم المرفقات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="5e6d9-134">لم يتم تعديل كيان بند فاتورة المورد لهذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="5e6d9-135">لا يقدم هذا الموضوع وصفًا تفصيليًا لحزمة البيانات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-135">This topic doesn’t give a detailed definition of a data package.</span></span> <span data-ttu-id="5e6d9-136">كما أنه لا يشرح كيفية إنشاء حزم البيانات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-136">It also doesn’t explain how to create data packages.</span></span> <span data-ttu-id="5e6d9-137">للحصول على هذه المعلومات، راجع [إطار عمل كيانات البيانات وحزم البيانات](../../dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="5e6d9-137">For this information, see [Data entities and packages framework](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="5e6d9-138">لإنشاء بيانات الاختبار التي تشتمل على الفواتير والمرفقات بشكل سريع، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-138">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="5e6d9-139">سجل الدخول إلى مثيل Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-139">Sign in to your Finance and Operations instance.</span></span>
1. <span data-ttu-id="5e6d9-140">انتقل إلى **الحسابات الدائنة** > **الفواتير** > **‏‫فواتير المورّد المعلقة‬**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-140">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="5e6d9-141">أنشئ فواتير تحتوي على بنود ومرفقات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-141">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5e6d9-142">يجب أن تكون المرفقات مرفقات الرأس.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-142">The attachments must be header attachments.</span></span> <span data-ttu-id="5e6d9-143">في الوقت الحالي، لا يدعم كيان مرفق مستند فاتورة المورد مرفقات البنود.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-143">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="5e6d9-144">افتح مساحة العمل **إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-144">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="5e6d9-145">قم بإنشاء وظيفة تصدير تتضمن كيانات رأس فاتورة المورد وبند فاتورة المورد، ومرفق مستند فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-145">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="5e6d9-146">قم بتصدير البيانات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-146">Export the data.</span></span>
1. <span data-ttu-id="5e6d9-147">قم بتنزيل البيانات التي تم تصديرها كحزمة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-147">Download the exported data as a package.</span></span> <span data-ttu-id="5e6d9-148">يمكنك الآن استخدام الحزمة لاستيراد البيانات إلى مثيلات هدف لأغراض الاختبار.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-148">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="5e6d9-149">تحديد الكيان القانوني للفاتورة</span><span class="sxs-lookup"><span data-stu-id="5e6d9-149">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="5e6d9-150">يمكن ربط المرفقات التي يتم استيرادها عن طريق حزم البيانات بالكيان القانوني الذي تنتمي إليه بطريقتين:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-150">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="5e6d9-151">وظيفة الاستيراد التي تقوم بمعالجة عمليات استيراد الفواتير إلى نفس الشركة حيث تمت جدولة الوظيفة في مساحة العمل **إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-151">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="5e6d9-152">بمعنى آخر، تحدد الشركة الخاصة بالوظيفة الشركة التي تنتمي الفاتورة إليها.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-152">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="5e6d9-153">عند إرسال حزمة البيانات التي تحتوي على الفواتير إلى Finance and Operations، باستطاعة المستدعي (وهذا يعني تطبيق تكامل الذي يتم تشغيله خارج Finance and Operations) الإشارة إلى معرف الشركة بوضوح في طلب HTTP.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-153">When the data package that contains invoices is sent to Finance and Operations, the caller (that is, the integration application that runs outside of Finance and Operations) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="5e6d9-154">في هذه الحالة، يتم تجاوز سياق الشركة الذي يتم فيه تشغيل وظيفة المعالجة في Finance and Operations، ويتم استيراد الفواتير إلى الشركة التي تم تمريرها من خلال طلب HTTP.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-154">In this case, the company context in which the processing job runs in Finance and Operations is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="5e6d9-155">يعتبر هذا السلوك السلوك القياسي لإدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-155">This behavior is standard data management behavior.</span></span> <span data-ttu-id="5e6d9-156">يتم شرحه هنا، في سياق الفواتير، فقط من أجل الحصول على معلومات كاملة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-156">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="5e6d9-157">معالجة الاستثناءات</span><span class="sxs-lookup"><span data-stu-id="5e6d9-157">Exception processing</span></span>

<span data-ttu-id="5e6d9-158">في السيناريوهات حيث تأتي فواتير المورد إلى Finance and Operations من خلال التكامل، يجب أن تتوفر طريقة سهلة لعضو فريق الحسابات الدائنة لمعالجة الاستثناءات أو الفواتير الفاشلة، ولإنشاء فواتير معلقة من الفواتير الفاشلة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-158">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="5e6d9-159">تشكل الآن معالجة الاستثناءات هذه لفواتير المورد جزءًا من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-159">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="5e6d9-160">صفحة قائمة الاستثناءات</span><span class="sxs-lookup"><span data-stu-id="5e6d9-160">Exceptions list page</span></span>

<span data-ttu-id="5e6d9-161">تتوفر صفحة القائمة الجديدة لاستثناءات الفاتورة في **الحسابات الدائنة** > **الفواتير** > **إخفاقات الاستيراد‬** > **فواتير المورد التي فشل استيرادها‬**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-161">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="5e6d9-162">تعرض هذه الصفحة جميع سجلات رؤوس فواتير المورد من جدول مرحلي لكيان بيانات رأس فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-162">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="5e6d9-163">لاحظ أنه يمكنك عرض السجلات نفسها من مساحة عمل **إدارة البيانات**، حيث يمكنك أيضًا تنفيذ نفس الإجراءات المتوفرة في ميزة التعامل مع الاستثناءات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-163">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="5e6d9-164">ومع ذلك، تم تحسين واجهة المستخدم التي توفرها ميزة التعامل مع الاستثناءات لمستخدمي الوظائف‬.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-164">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![صفحة قائمة الاستثناءات](media/vendor_invoice_automation_02.png)

<span data-ttu-id="5e6d9-166">تتضمن الصفحة القائمة هذه الحقول التالية التي تأتي عبر موجز ويب:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="5e6d9-167">**الشركة** – الشركة التي تنتمي إليها الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="5e6d9-168">**رسالة الخطأ** – رسالة الخطأ التي تصدر عن مشاكل إطار عمل إدارة البيانات لتوضيح سبب تعذر إنشاء الفاتورة</span><span class="sxs-lookup"><span data-stu-id="5e6d9-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="5e6d9-169">**الرقم** – رقم الفاتورة</span><span class="sxs-lookup"><span data-stu-id="5e6d9-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="5e6d9-170">**حساب الفاتورة**</span><span class="sxs-lookup"><span data-stu-id="5e6d9-170">**Invoice account**</span></span>
+ <span data-ttu-id="5e6d9-171">**الاسم** – اسم المورد</span><span class="sxs-lookup"><span data-stu-id="5e6d9-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="5e6d9-172">**حساب المورّد**</span><span class="sxs-lookup"><span data-stu-id="5e6d9-172">**Vendor account**</span></span>
+ <span data-ttu-id="5e6d9-173">**أمر الشراء** – رقم أمر الشراء للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="5e6d9-174">**تاريخ الترحيل**</span><span class="sxs-lookup"><span data-stu-id="5e6d9-174">**Posting date**</span></span>
+ <span data-ttu-id="5e6d9-175">**تاريخ الفاتورة**</span><span class="sxs-lookup"><span data-stu-id="5e6d9-175">**Invoice date**</span></span>
+ <span data-ttu-id="5e6d9-176">**وصف الفاتورة**</span><span class="sxs-lookup"><span data-stu-id="5e6d9-176">**Invoice description**</span></span>
+ <span data-ttu-id="5e6d9-177">**العملة**</span><span class="sxs-lookup"><span data-stu-id="5e6d9-177">**Currency**</span></span>
+ <span data-ttu-id="5e6d9-178">**السجل**</span><span class="sxs-lookup"><span data-stu-id="5e6d9-178">**Log**</span></span>
+ <span data-ttu-id="5e6d9-179">**مرجع البند** - المعرف الذي يأتي من النظام الخارجي</span><span class="sxs-lookup"><span data-stu-id="5e6d9-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="5e6d9-180">لا يعتبر مرجع البند معرف الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="5e6d9-181">تحتوي أيضًا صفحة القائمة هذه على جزء معاينة يمكنك استخدامه بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="5e6d9-182">عرض رسالة الخطأ الكاملة، بحيث لا تضطر إلى توسيع عمود **رسالة الخطأ** في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="5e6d9-183">عرض القائمة بأكملها للمرفقات الخاصة بالفاتورة، إذا كانت أي مرفقات تصحب الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-183">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="5e6d9-184">تدعم صفحة القائمة الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-184">The list page supports the following actions:</span></span>

+ <span data-ttu-id="5e6d9-185">**تحرير** – فتح سجل الاستثناءات في وضع التحرير، بحيث يمكن إصلاح المشكلات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-185">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="5e6d9-186">**خيارات** - الوصول إلى الخيارات القياسية المتوفرة في صفحات القوائم.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-186">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="5e6d9-187">يمكنك استخدام الخيار **إضافة إلى مساحة العمل** لإضافة صفحة قائمة الاستثناءات إلى مساحة العمل كقائمة أو لوحة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-187">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="5e6d9-188">صفحة تفاصيل الاستثناءات</span><span class="sxs-lookup"><span data-stu-id="5e6d9-188">Exception details page</span></span>

<span data-ttu-id="5e6d9-189">عند بدء العمل في وضع التحرير، تظهر الصفحة تفاصيل الاستثناءات للفاتورة التي تنطوي على مشاكل.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-189">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="5e6d9-190">في حالة وجود أي مرفقات، تظهر الفاتورة والمرفق الافتراضي جنبًا إلى جنب في صفحة تفاصيل الاستثناءات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-190">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![صفحة تفاصيل الاستثناءات](media/vendor_invoice_automation_03.png)

<span data-ttu-id="5e6d9-192">في الرسم التوضيحي السابق، لم تظهر أية بنود لرأس فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-192">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="5e6d9-193">وبالتالي، يظهر مقطع البنود فارغًا.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-193">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="5e6d9-194">تدعم صفحة تفاصيل الاستثناءات العملية التالية:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-194">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="5e6d9-195">**إنشاء فاتورة معلقة** - بعد إصلاح المشكلات على الفاتورة كجزء من معالجة الاستثناءات، يمكنك النقر فوق هذا الزر لإنشاء الفاتورة المعلقة‏‎.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-195">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="5e6d9-196">يتم إنشاء الفواتير المعلقة في الخلفية (كعملية غير متزامنة).</span><span class="sxs-lookup"><span data-stu-id="5e6d9-196">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="5e6d9-197">معالجة استثناءات الخدمة المشتركة في مقابل معالجة الاستثناءات التي تستند إلى المؤسسة</span><span class="sxs-lookup"><span data-stu-id="5e6d9-197">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="5e6d9-198">تدعم صفحة قائمة الاستثناءات بنيات الأمان القياسية التي تدعمها مساحة عمل **إدارة البيانات** لمعالجة السجلات المرحلية.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-198">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="5e6d9-199">يمكن حماية وظيفة استيراد الفواتير بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-199">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="5e6d9-200">بواسطة دور المستخدم</span><span class="sxs-lookup"><span data-stu-id="5e6d9-200">By user role</span></span>
+ <span data-ttu-id="5e6d9-201">بواسطة المستخدم</span><span class="sxs-lookup"><span data-stu-id="5e6d9-201">By user</span></span>
+ <span data-ttu-id="5e6d9-202">بواسطة الكيان القانوني</span><span class="sxs-lookup"><span data-stu-id="5e6d9-202">By legal entity</span></span>

![وظيفة الاستيراد المحمية بواسطة دور المستخدم والكيان القانوني](media/vendor_invoice_automation_04.png)

<span data-ttu-id="5e6d9-204">إذا تم تكوين الأمان لوظيفة استيراد الفواتير، فإن صفحة قوائم الاستثناءات تلتزم بهذه الإعدادات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-204">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="5e6d9-205">سوف يتمكن المستخدمون من رؤية فقط سجلات استثناءات الفواتير التي يسمح لهم الإعداد برؤيتها.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-205">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="5e6d9-206">على سبيل المثال، قررت شركة التعمير معالجة استثناءات الفواتير بواسطة الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-206">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="5e6d9-207">وبالتالي، يتم تكوين الأمان على وظيفة استيراد الفواتير بحيث يتمكن مستخدم في الكيان القانوني أ من رؤية استثناءات الفواتير فقط في الكيان القانوني أ، في حين يستطيع مستخدم في الكيان القانوني ب رؤية استثناءات الفواتير فقط في الكيان القانوني ب. يمكّن هذا الإعداد الفصل بين المهام الخاصة فيما يتعلق بإدارة استثناءات الفواتير.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-207">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="5e6d9-208">قررت أيضًا شركة التعمير عدم فرض الأمان، لتمكين نفس المستخدمين من معالجة استثناءات الفواتير لكافة الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-208">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="5e6d9-209">يمكّن هذا الإعداد سيناريو خدمات مشتركة لإدارة استثناءات الفواتير.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-209">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="5e6d9-210">عارض المرفقات جنبًا إلى جنب</span><span class="sxs-lookup"><span data-stu-id="5e6d9-210">Side-by-side attachment viewer</span></span>

<span data-ttu-id="5e6d9-211">لمساعدتك على عرض مرفقات فواتير المورد بسهولة، توفر الآن الصفحات التالية التي يتم استخدامها في عملية الفوترة الآن عارض المرفقات:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-211">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="5e6d9-212">**معالجة الاستثناءات**</span><span class="sxs-lookup"><span data-stu-id="5e6d9-212">**Exception handling**</span></span>
+ <span data-ttu-id="5e6d9-213">صفحة **فواتير المورد المعلقة** (متوفرة أيضًا في عملية مراجعة الفاتورة)</span><span class="sxs-lookup"><span data-stu-id="5e6d9-213">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="5e6d9-214">صفحة استعلام **دفتر يومية الفواتير** (للفواتير التي تم ترحيلها)</span><span class="sxs-lookup"><span data-stu-id="5e6d9-214">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="5e6d9-215">فيما يلي الوظيفة الأساسية التي يوفرها عارض المرفقات:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-215">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="5e6d9-216">عرض كافة أنواع المرفقات التي تدعمها إدارة المستندات (الملفات والصور وعناوين URL والملاحظات).</span><span class="sxs-lookup"><span data-stu-id="5e6d9-216">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="5e6d9-217">عرض ملفات TIFF متعددة الصفحات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-217">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="5e6d9-218">تنفيذ الإجراءات التالية في ملفات الصور:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-218">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="5e6d9-219">تمييز أجزاء من الصورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-219">Highlight parts of the image.</span></span>
  + <span data-ttu-id="5e6d9-220">حظر أجزاء من الصورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-220">Block parts of the image.</span></span>
  + <span data-ttu-id="5e6d9-221">إضافة تعليقات توضيحية إلى الصورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-221">Add annotations to the image.</span></span>
  + <span data-ttu-id="5e6d9-222">التكبير والتصغير في الصورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-222">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="5e6d9-223">تحريك الصورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-223">Pan the image.</span></span>
  + <span data-ttu-id="5e6d9-224">التراجع عن الإجراءات وإعادتها.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-224">Undo and redo actions.</span></span>
  + <span data-ttu-id="5e6d9-225">ملاءمة حجم الصورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-225">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="5e6d9-226">تتوفر هذه الإجراءات فقط لملفات الصور (JPEG وPNG وTIFF، وهكذا).</span><span class="sxs-lookup"><span data-stu-id="5e6d9-226">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="5e6d9-227">يتم حفظ التغييرات التي تجريها على صورة باستخدام هذه الإجراءات في ملف الصورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-227">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="5e6d9-228">في الوقت الحالي، لا يتضمن عارض المرفقات قدرات تعيين الإصدار أو التدقيق.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-228">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="5e6d9-229">المرفق الافتراضي</span><span class="sxs-lookup"><span data-stu-id="5e6d9-229">Default attachment</span></span>

<span data-ttu-id="5e6d9-230">إذا تضمن فاتورة مورد أكثر من مرفق واحد، يمكنك تعيين أحد المستندات كمرفق افتراضي في صفحة **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-230">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="5e6d9-231">تمت إضافة الخيار الجديد **هو مرفق افتراضي‬** كجزء من هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-231">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="5e6d9-232">يتم عرض هذا الخيار أيضًا في كيان بيانات مرفق مستند فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-232">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="5e6d9-233">وبالتالي، يمكن تعيين المرفق الافتراضي من خلال عمليات التكامل.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-233">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="5e6d9-234">يمكن تعيين مستند واحد فقط كمرفق افتراضي.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-234">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="5e6d9-235">بعد تعيين مستند كمرفق افتراضي، يظهر تلقائيًا في عارض المرفقات عند فتح الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-235">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="5e6d9-236">إذا لم تعين أي مستند كمرفق افتراضي، لن يُظهر عارض المرفقات بشكل تلقائي أي مرفق عند فتح الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-236">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="5e6d9-237">إظهار/إخفاء مرفقات الفاتورة</span><span class="sxs-lookup"><span data-stu-id="5e6d9-237">Show/hide invoice attachments</span></span>

<span data-ttu-id="5e6d9-238">يتوفر زر جديد في صفحات استعلام **معالجة الاستثناءات** و**الفاتورة المعلقة** و**دفتر يومية الفواتير** للسماح لك بإظهار أو إخفاء عارض المرفقات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-238">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="5e6d9-239">الأمان</span><span class="sxs-lookup"><span data-stu-id="5e6d9-239">Security</span></span>

<span data-ttu-id="5e6d9-240">يتم التحكم في الإجراءات التالية في عارض المرفقات عن طريق الأمان المستند إلى الدور.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-240">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="5e6d9-241">تمييز</span><span class="sxs-lookup"><span data-stu-id="5e6d9-241">Highlighting</span></span>
+ <span data-ttu-id="5e6d9-242">تأمين</span><span class="sxs-lookup"><span data-stu-id="5e6d9-242">Block</span></span>
+ <span data-ttu-id="5e6d9-243">تعليق توضيحي</span><span class="sxs-lookup"><span data-stu-id="5e6d9-243">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="5e6d9-244">صفحة فواتير المورّد المعلقة</span><span class="sxs-lookup"><span data-stu-id="5e6d9-244">Pending vendor invoices page</span></span>

<span data-ttu-id="5e6d9-245">توفر الامتيازات التالية حق الوصول للقراءة فقط أو حق الوصول للقراءة/الكتابة إلى عارض المرفقات لإجراءات التمييز والحظر وإدخال التعليقات التوضيحية:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-245">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="5e6d9-246">**الاحتفاظ بصورة فاتورة المورّد‬** - يوفر هذا الامتياز حق الوصول للقراءة/الكتابة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-246">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="5e6d9-247">**عرض صورة فاتورة المورّد‬** - يوفر هذا الامتياز حق الوصول للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-247">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="5e6d9-248">توفر المهام التالية حق الوصول للقراءة فقط أو حق الوصول للقراءة/الكتابة إلى عارض المرفقات لهذه الإجراءات:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-248">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="5e6d9-249">**الاحتفاظ بفواتير المورد** - يتم تعيين امتياز "الاحتفاظ بصورة فاتورة المورّد‬" لهذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-249">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="5e6d9-250">**الاستعلام عن حالة فواتير المورّد‬** - يتم تعيين امتياز "الاحتفاظ بصورة فاتورة المورّد‬" لهذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-250">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="5e6d9-251">توفر الأدوار التالية حق الوصول للقراءة فقط أو حق الوصول للقراءة/الكتابة إلى عارض المرفقات لهذه الإجراءات:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-251">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="5e6d9-252">**موظف الحسابات الدائنة‬** و**مدير الحسابات الدائنة** - يتم تعيين مهمة "الاحتفاظ بفواتير المورّد" لهذه الأدوار.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-252">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="5e6d9-253">**موظف الحسابات الدائنة** و**مدير الحسابات الدائنة** و**موظف المدفوعات المركزية للحسابات الدائنة‬** و**موظف مدفوعات الحسابات الدائنة** - يتم تعيين مهمة "الاستعلام عن حالة فواتير المورّد‬" لهذه الأدوار.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-253">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="5e6d9-254">صفحة تفاصيل استثناءات الفواتير</span><span class="sxs-lookup"><span data-stu-id="5e6d9-254">Invoice exception details page</span></span>

<span data-ttu-id="5e6d9-255">توفر الامتيازات التالية حق الوصول للقراءة فقط أو حق الوصول للقراءة/الكتابة إلى عارض المرفقات لإجراءات التمييز والحظر وإضافة التعليقات التوضيحية.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-255">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="5e6d9-256">توفر الأدوار التي تمت الإشارة إليها في هذا المقطع حق الوصول للقراءة فقط إلى صور الفواتير في عارض المرفقات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-256">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="5e6d9-257">إذا كان من المفترض أن يتوفر لأحد الأدوار حق الوصول للكتابة إلى الصور، فيمكنك منح حق الوصول للكتابة إلى ذلك الدور باستخدام الامتياز والمهمة التي ورد صفها هنا.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-257">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="5e6d9-258">**الاحتفاظ بصورة كيان رأس فاتورة المورّد‬** - يوفر هذا الامتياز حق الوصول قراءة/الكتابة إلى صور الفواتير في عارض المرفقات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-258">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="5e6d9-259">**عرض صورة كيان رأس فاتورة المورّد‬‬** - يوفر هذا الامتياز حق الوصول للقراءة فقط إلى صور الفواتير في عارض المرفقات.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-259">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="5e6d9-260">توفر المهام التالية حق الوصول للقراءة فقط إلى عارض المرفقات لهذه الإجراءات:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-260">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="5e6d9-261">**الاحتفاظ بفواتير المورد** - يتم تعيين امتياز "الاحتفاظ بصورة كيان رأس فاتورة المورّد‬‬" لهذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-261">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="5e6d9-262">توفر الأدوار التالية حق الوصول للقراءة فقط إلى عارض المرفقات لهذه الإجراءات:</span><span class="sxs-lookup"><span data-stu-id="5e6d9-262">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="5e6d9-263">**موظف الحسابات الدائنة‬** و**مدير الحسابات الدائنة** - يتم تعيين مهمة "الاحتفاظ بفواتير المورّد" لهذه الأدوار.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-263">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="5e6d9-264">بشكل افتراضي، إذا وفر دور المستخدم حقوق التحرير في أية صفحة، فستتوفر أيضًا للمستخدم حقوق التحرير في عارض المرفقات لإجراءات التمييز والحظر وإدخال التعليقات التوضيحية.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-264">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="5e6d9-265">ومع ذلك، إذا كان هناك سيناريوهات حيث يجب أن تتوفر لدور معين حقوق التحرير في الصفحة ولكن ليس في عارض المرفقات، يمكن استخدام الامتيازات المناسبة من القائمة السابقة لتلبية حالة الاستخدام.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-265">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>

