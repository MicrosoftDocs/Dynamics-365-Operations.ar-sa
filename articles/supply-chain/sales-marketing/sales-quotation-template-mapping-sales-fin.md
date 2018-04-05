---
title: "مزامنة رؤوس وبنود عرض أسعار المبيعات‬ مباشرةً من Sales إلى Finance and Operations"
description: "يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود عروض أسعار المبيعات مباشرةً من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 97536c27dea113cc3c019473f22d1925e7617f8f
ms.contentlocale: ar-sa
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="410e5-103">مزامنة رؤوس وبنود عرض أسعار المبيعات‬ مباشرةً من Sales إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="410e5-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="410e5-104">يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود عروض أسعار المبيعات مباشرةً من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="410e5-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="410e5-105">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="410e5-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="410e5-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="410e5-106">Template and tasks</span></span>

<span data-ttu-id="410e5-107">يتم استخدام القالب والمهام الأساسية التالية لمزامنة رؤوس وبنود عروض أسعار المبيعات مباشرةً من Sales إلى Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="410e5-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="410e5-108">**اسم القالب في تكامل البيانات:** عروض أسعار المبيعات (Sales إلى Fin and Ops)‬ - مباشر</span><span class="sxs-lookup"><span data-stu-id="410e5-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="410e5-109">**أسماء المهام في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="410e5-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="410e5-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="410e5-110">QuoteHeader</span></span>
    - <span data-ttu-id="410e5-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="410e5-111">QuoteLine</span></span>

<span data-ttu-id="410e5-112">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود عروض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="410e5-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="410e5-113">‏‫المنتجات (Fin and Ops إلى Sales)‬ - مباشر</span><span class="sxs-lookup"><span data-stu-id="410e5-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="410e5-114">الحسابات (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="410e5-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="410e5-115">جهات الاتصال إلى العملاء (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="410e5-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="410e5-116">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="410e5-116">Entity set</span></span>

| <span data-ttu-id="410e5-117">مبيعات</span><span class="sxs-lookup"><span data-stu-id="410e5-117">Sales</span></span>        | <span data-ttu-id="410e5-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="410e5-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="410e5-119">الاقتباسات</span><span class="sxs-lookup"><span data-stu-id="410e5-119">Quotes</span></span>       | <span data-ttu-id="410e5-120">رأس عرض أسعار مبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="410e5-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="410e5-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="410e5-121">QuoteDetails</span></span> | <span data-ttu-id="410e5-122">بنود عروض أسعار مبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="410e5-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="410e5-123">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="410e5-123">Entity flow</span></span>

<span data-ttu-id="410e5-124">يتم إنشاء عروض أسعار المبيعات في Sales وتتم مزامنتها إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="410e5-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="410e5-125">تتم مزامنة عروض أسعار المبيعات من Sales فقط إذا تحققت الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="410e5-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="410e5-126">تتم المحافظة على كافة المنتجات الموجودة في عرض أسعار المبيعات خارجيًا.</span><span class="sxs-lookup"><span data-stu-id="410e5-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="410e5-127">بعد النقر فوق **تنشيط عرض الأسعار**، يتم تنشيط عرض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="410e5-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="410e5-128">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="410e5-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="410e5-129">تمت إضافة الحقل **لديه منتجات تتم المحافظة عليها خارجيًا فقط** إلى كيان **عروض الأسعار** للتحقق بشكل مستمر مما إذا كان عرض أسعار المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا.</span><span class="sxs-lookup"><span data-stu-id="410e5-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="410e5-130">إذا كان لعرض الأسعار منتجات تتم المحافظة عليها خارجيًا فقط، فستتم المحافظة على المنتجات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="410e5-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="410e5-131">يساعد هذا السلوك على ضمان عدم محاولتك مزامنة بنود عروض أسعار المبيعات التي تشتمل على منتجات غير معروفة إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="410e5-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="410e5-132">يتم تحديث كافة المنتجات الموجودة في عرض أسعار المبيعات بواسطة معلومات **لديه منتجات تتم المحافظة عليها خارجيًا فقط** من رأس عرض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="410e5-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="410e5-133">يمكن العثور على هذه المعلومات في الحقل **‎لدى عرض الأسعار منتجات تتم المحافظة عليها خارجيًا فقط** في الكيان **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="410e5-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="410e5-134">يمكن إضافة خصم إلى منتج عرض الأسعار وستتم مزامنته إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="410e5-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="410e5-135">تخضع حقول **الخصم** و**التكاليف** و**الضريبة** لمراقبة أحد الإعدادات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="410e5-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="410e5-136">لا يدعم هذا الإعداد حاليًا تعيين التكامل.</span><span class="sxs-lookup"><span data-stu-id="410e5-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="410e5-137">في التصميم الحالي، يتم الاحتفاظ بحقول **السعر** و**الخصم** و**التكلفة** و**الضريبة** وتتم معالجتها في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="410e5-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="410e5-138">في Sales، يجعل الحل الحقول التالية للقراءة فقط، نظرًا لعدم مزامنة القيم إلى Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="410e5-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="410e5-139">حقول للقراءة فقط في رأس عرض أسعار المبيعات: **% الخصم‬**، و**الخصم‬**، و**مبلغ الشحن**</span><span class="sxs-lookup"><span data-stu-id="410e5-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="410e5-140">حقول للقراءة فقط على منتجات عرض الأسعار: **الضريبة**</span><span class="sxs-lookup"><span data-stu-id="410e5-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="410e5-141">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="410e5-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="410e5-142">قبل إجراء مزامنة عروض أسعار المبيعات، لا بد من تحديث الإعدادات التالية.</span><span class="sxs-lookup"><span data-stu-id="410e5-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="410e5-143">الإعداد في Sales</span><span class="sxs-lookup"><span data-stu-id="410e5-143">Setup in Sales</span></span>

- <span data-ttu-id="410e5-144">تأكد من إعداد الأذونات للفريق الذي تم تعيين المستخدم من إعداد الاتصال في Sales إليه.</span><span class="sxs-lookup"><span data-stu-id="410e5-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="410e5-145">إذا كنت تستخدم بيانات العرض التوضيحي، فعادة ما يكون لدى المستخدم حق وصول المسؤول، ولكن هذا الحق لا يتوفر للفريق.</span><span class="sxs-lookup"><span data-stu-id="410e5-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="410e5-146">إذا لم يكن لدى الفريق حق وصول المسؤول عند تشغيل المشروع من تكامل البيانات، فسوف تتلقى رسالة خطأ تفيد بأن الفريق الرئيسي مفقود.</span><span class="sxs-lookup"><span data-stu-id="410e5-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="410e5-147">لإعداد الأذونات الخاصة بالفريق، انتقل إلى **الإعدادات**&gt;**الأمان**&gt;**الفرق**، وحدد الفريق ذا الصلة.</span><span class="sxs-lookup"><span data-stu-id="410e5-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="410e5-148">حدد **إدارة الأدوار**، ثم حدد دورًا يحتوي على الأذونات المطلوبة، مثل **مسؤول النظام**.</span><span class="sxs-lookup"><span data-stu-id="410e5-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="410e5-149">انتقل إلى **الإعدادات** &gt; **الإدارة** &gt; **إعدادات النظام** &gt; **Sales**‎، وتأكد من أنه يتم استخدام الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="410e5-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="410e5-150">يكون الخيار **‬‏‫استخدام حساب أسعار النظام** معينًا إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="410e5-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="410e5-151">يكون الحقل **طريقة حساب الخصم** معينًا إلى **صنف البند**.</span><span class="sxs-lookup"><span data-stu-id="410e5-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="410e5-152">إعداد مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="410e5-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="410e5-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="410e5-153">QuoteHeader</span></span>

- <span data-ttu-id="410e5-154">تأكد من وجود التعيين المطلوب لـ **Shipto\_country** إلى **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="410e5-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="410e5-155">في تعيين القيمة، يمكنك تحديد قيمة افتراضية تُستخدم في حالة ترك القيمة فارغة.</span><span class="sxs-lookup"><span data-stu-id="410e5-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="410e5-156">ما عليك سوى ترك الجانب الأيمن فارغًا، وعيّن الجانب الأيسر إلى البلد أو المنطقة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="410e5-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="410e5-157">بهذه الطريقة، لا تحتاج إلى كتابة البلد أو المنطقة للأوامر المحلية.</span><span class="sxs-lookup"><span data-stu-id="410e5-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="410e5-158">قيمة القالب هي تعيين قيمة حيث يتم تعيين العديد من البلدان أو المناطق، وحيث تساوي القيمة الفارغة قيمة **US**.</span><span class="sxs-lookup"><span data-stu-id="410e5-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="410e5-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="410e5-159">QuoteLine</span></span>

- <span data-ttu-id="410e5-160">تأكد من وجود تعيين القيمة المطلوب لـ **SalesUnitSymbol** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="410e5-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="410e5-161">تأكد من تحديد الوحدات المطلوبة في Sales.</span><span class="sxs-lookup"><span data-stu-id="410e5-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="410e5-162">يتم تعريف قيمة القالب التي لها تعيين قيمة لـ **oumid.name** إلى **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="410e5-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="410e5-163">اختياري: يمكنك إضافة التعيينات التالية للمساعدة في ضمان استيراد بنود عروض أسعار المبيعات إلى Finance and Operations إذا لم يكن هناك معلومات افتراضية من العميل أو المنتج:</span><span class="sxs-lookup"><span data-stu-id="410e5-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="410e5-164">**SiteId** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="410e5-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="410e5-165">لا توجد قيمة قالب افتراضي لـ **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="410e5-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="410e5-166">**WarehouseId** – المستودع مطلوب لمعالجة بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="410e5-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="410e5-167">لا توجد قيمة قالب افتراضي لـ **WarehouseId‎**.</span><span class="sxs-lookup"><span data-stu-id="410e5-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="410e5-168">تعيين القالب في موحد البيانات</span><span class="sxs-lookup"><span data-stu-id="410e5-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="410e5-169">تخضع حقول **الخصم** و**التكاليف** و**الضريبة** لمراقبة إعداد معقد في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="410e5-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="410e5-170">لا يدعم هذا الإعداد حاليًا تعيين التكامل.</span><span class="sxs-lookup"><span data-stu-id="410e5-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="410e5-171">في التصميم الحالي، يتولى Finance and Operations إدارة حقول **السعر** و**الخصم** و**التكاليف**، و**الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="410e5-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="410e5-172">لا تشكل الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** جزءًا من التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="410e5-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="410e5-173">لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="410e5-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="410e5-174">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="410e5-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="410e5-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="410e5-175">QuoteHeader</span></span>

![تعيين القالب في موحد البيانات](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="410e5-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="410e5-177">QuoteLine</span></span>

![تعيين القالب في موحد البيانات](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="410e5-179">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="410e5-179">Related topics</span></span>

[<span data-ttu-id="410e5-180">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="410e5-180">Prospect to cash</span></span>](prospect-to-cash.md)


