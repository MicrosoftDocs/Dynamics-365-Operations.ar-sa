---
title: مزامنة رؤوس وبنود عروض أسعار المبيعات مباشرةً من Sales إلى Supply Chain Management.
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود عروض أسعار المبيعات مباشرةً من Dynamics 365 Sales إلى Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6b4f0006e4cacc2897d2b6c9c9dde88d0aafa4ad
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653169"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="e748a-103">مزامنة رؤوس وبنود عروض أسعار المبيعات مباشرةً من Sales إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e748a-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود عروض أسعار المبيعات مباشرةً من Dynamics 365 Sales إلى Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="e748a-105">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل البيانات في Common Data Service للتطبيقات‏‎](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="e748a-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="e748a-106">تدفق البيانات في حل العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="e748a-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="e748a-107">يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="e748a-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="e748a-108">تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="e748a-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="e748a-109">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="e748a-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="e748a-110">[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="e748a-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="e748a-111">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="e748a-111">Template and tasks</span></span>

<span data-ttu-id="e748a-112">يتم استخدام القالب والمهام الأساسية التالية لمزامنة رؤوس وبنود عروض أسعار المبيعات مباشرةً من Sales إلى Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="e748a-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="e748a-113">**اسم القالب في تكامل البيانات:** عروض أسعار المبيعات (من Sales إلى Supply Chain Management) - مباشر</span><span class="sxs-lookup"><span data-stu-id="e748a-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="e748a-114">**أسماء المهام في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="e748a-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="e748a-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e748a-115">QuoteHeader</span></span>
    - <span data-ttu-id="e748a-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e748a-116">QuoteLine</span></span>

<span data-ttu-id="e748a-117">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود عروض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e748a-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="e748a-118">المنتجات (من Supply Chain Management إلى Sales) - مباشر</span><span class="sxs-lookup"><span data-stu-id="e748a-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="e748a-119">الحسابات (من Sales إلى Supply Chain Management) - مباشر (إذا ما تم استخدامه)</span><span class="sxs-lookup"><span data-stu-id="e748a-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="e748a-120">جهات الاتصال إلى العملاء (من Sales إلى Supply Chain Management) - مباشر (إذا ما تم استخدامه)</span><span class="sxs-lookup"><span data-stu-id="e748a-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="e748a-121">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="e748a-121">Entity set</span></span>

| <span data-ttu-id="e748a-122">ال‏‏مبيعات</span><span class="sxs-lookup"><span data-stu-id="e748a-122">Sales</span></span>        | <span data-ttu-id="e748a-123">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e748a-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="e748a-124">الاقتباسات</span><span class="sxs-lookup"><span data-stu-id="e748a-124">Quotes</span></span>       | <span data-ttu-id="e748a-125">رأس عرض أسعار مبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="e748a-125">CDS sales quotation header</span></span> |
| <span data-ttu-id="e748a-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="e748a-126">QuoteDetails</span></span> | <span data-ttu-id="e748a-127">بنود عروض أسعار مبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="e748a-127">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="e748a-128">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="e748a-128">Entity flow</span></span>

<span data-ttu-id="e748a-129">يتم إنشاء عروض أسعار المبيعات في Sales وتتم مزامنتها إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="e748a-130">تتم مزامنة عروض أسعار المبيعات من Sales فقط إذا تحققت الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="e748a-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="e748a-131">تتم المحافظة على كافة المنتجات الموجودة في عرض أسعار المبيعات خارجيًا.</span><span class="sxs-lookup"><span data-stu-id="e748a-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="e748a-132">بعد النقر فوق **تنشيط عرض الأسعار**، يتم تنشيط عرض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e748a-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e748a-133">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="e748a-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="e748a-134">تمت إضافة الحقل **لديه منتجات تتم المحافظة عليها خارجيًا فقط** إلى كيان **عروض الأسعار** للتحقق بشكل مستمر مما إذا كان عرض أسعار المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا.</span><span class="sxs-lookup"><span data-stu-id="e748a-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="e748a-135">إذا كان لعرض الأسعار منتجات تتم المحافظة عليها خارجيًا فقط، فستتم المحافظة على المنتجات في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="e748a-136">يساعد هذا السلوك على ضمان عدم محاولتك مزامنة بنود عروض أسعار المبيعات التي تشتمل على منتجات غير معروفة إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="e748a-137">يتم تحديث كافة المنتجات الموجودة في عرض أسعار المبيعات بواسطة معلومات **لديه منتجات تتم المحافظة عليها خارجيًا فقط** من رأس عرض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e748a-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="e748a-138">يمكن العثور على هذه المعلومات في الحقل **‎لدى عرض الأسعار منتجات تتم المحافظة عليها خارجيًا فقط** في الكيان **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="e748a-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="e748a-139">يمكن إضافة خصم إلى منتج عرض الأسعار وستتم مزامنته إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="e748a-140">تخضع حقول **الخصم** و **التكاليف** و **الضريبة** للإعدادات في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="e748a-141">لا يدعم هذا الإعداد حاليًا تعيين التكامل.</span><span class="sxs-lookup"><span data-stu-id="e748a-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="e748a-142">في التصميم الحالي، يتم الاحتفاظ بحقول **السعر** و **الخصم** و **التكلفة** و **الضريبة** وتتم معالجتها في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="e748a-143">في Sales، يجعل الحل الحقول التالية للقراءة فقط، نظرًا لعدم مزامنة القيم إلى Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="e748a-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="e748a-144">حقول للقراءة فقط في رأس عرض أسعار المبيعات: **% الخصم‬**، و**الخصم‬**، و**مبلغ الشحن**</span><span class="sxs-lookup"><span data-stu-id="e748a-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="e748a-145">حقول للقراءة فقط على منتجات عرض الأسعار: **الضريبة**</span><span class="sxs-lookup"><span data-stu-id="e748a-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e748a-146">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="e748a-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="e748a-147">قبل إجراء مزامنة عروض أسعار المبيعات، لا بد من تحديث الإعدادات التالية.</span><span class="sxs-lookup"><span data-stu-id="e748a-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="e748a-148">الإعداد في Sales</span><span class="sxs-lookup"><span data-stu-id="e748a-148">Setup in Sales</span></span>

- <span data-ttu-id="e748a-149">تأكد من إعداد الأذونات للفريق الذي تم تعيين المستخدم من إعداد الاتصال في Sales إليه.</span><span class="sxs-lookup"><span data-stu-id="e748a-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="e748a-150">إذا كنت تستخدم بيانات العرض التوضيحي، فعادة ما يكون لدى المستخدم حق وصول المسؤول، ولكن هذا الحق لا يتوفر للفريق.</span><span class="sxs-lookup"><span data-stu-id="e748a-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="e748a-151">إذا لم يكن لدى الفريق حق وصول المسؤول عند تشغيل المشروع من تكامل البيانات، فسوف تتلقى رسالة خطأ تفيد بأن الفريق الرئيسي مفقود.</span><span class="sxs-lookup"><span data-stu-id="e748a-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="e748a-152">لإعداد الأذونات الخاصة بالفريق، انتقل إلى **الإعدادات**&gt;**الأمان**&gt;**الفرق**، وحدد الفريق ذا الصلة.</span><span class="sxs-lookup"><span data-stu-id="e748a-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="e748a-153">حدد **إدارة الأدوار**، ثم حدد دورًا يحتوي على الأذونات المطلوبة، مثل **مسؤول النظام**.</span><span class="sxs-lookup"><span data-stu-id="e748a-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="e748a-154">انتقل إلى **الإعدادات** &gt; **الإدارة** &gt; **إعدادات النظام** &gt; **Sales**‎، وتأكد من أنه يتم استخدام الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e748a-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="e748a-155">يكون الخيار **‬‏‫استخدام حساب أسعار النظام** معينًا إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e748a-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="e748a-156">يكون الحقل **طريقة حساب الخصم** معينًا إلى **صنف البند**.</span><span class="sxs-lookup"><span data-stu-id="e748a-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="e748a-157">إعداد مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="e748a-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="e748a-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e748a-158">QuoteHeader</span></span>

- <span data-ttu-id="e748a-159">تأكد من وجود التعيين المطلوب لـ **Shipto\_country** إلى **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="e748a-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="e748a-160">في تعيين القيمة، يمكنك تحديد قيمة افتراضية تُستخدم في حالة ترك القيمة فارغة.</span><span class="sxs-lookup"><span data-stu-id="e748a-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="e748a-161">ما عليك سوى ترك الجانب الأيمن فارغًا، وعيّن الجانب الأيسر إلى البلد أو المنطقة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="e748a-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="e748a-162">بهذه الطريقة، لا تحتاج إلى كتابة البلد أو المنطقة للأوامر المحلية.</span><span class="sxs-lookup"><span data-stu-id="e748a-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="e748a-163">قيمة القالب هي تعيين قيمة حيث يتم تعيين العديد من البلدان أو المناطق، وحيث تساوي القيمة الفارغة قيمة **US**.</span><span class="sxs-lookup"><span data-stu-id="e748a-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="e748a-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e748a-164">QuoteLine</span></span>

- <span data-ttu-id="e748a-165">تأكد من وجود تعيين القيمة المطلوب لـ **SalesUnitSymbol** في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="e748a-166">تأكد من تحديد الوحدات المطلوبة في Sales.</span><span class="sxs-lookup"><span data-stu-id="e748a-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="e748a-167">يتم تعريف قيمة القالب التي لها تعيين قيمة لـ **oumid.name** إلى **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="e748a-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="e748a-168">اختياري: يمكنك إضافة التعيينات التالية للمساعدة في ضمان استيراد بنود عروض أسعار المبيعات إلى Supply Chain Management إذا لم يكن هناك معلومات افتراضية من العميل أو المنتج:</span><span class="sxs-lookup"><span data-stu-id="e748a-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="e748a-169">**SiteId** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="e748a-170">لا توجد قيمة قالب افتراضي لـ **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="e748a-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="e748a-171">**WarehouseId** – المستودع مطلوب لمعالجة بنود أوامر المبيعات وعروض الأسعار في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="e748a-172">لا توجد قيمة قالب افتراضي لـ **WarehouseId‎**.</span><span class="sxs-lookup"><span data-stu-id="e748a-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="e748a-173">تعيين القالب في موحد البيانات</span><span class="sxs-lookup"><span data-stu-id="e748a-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="e748a-174">تخضع حقول **الخصم** و **التكاليف** و **الضريبة** للإعداد المعقد في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e748a-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="e748a-175">لا يدعم هذا الإعداد حاليًا تعيين التكامل.</span><span class="sxs-lookup"><span data-stu-id="e748a-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="e748a-176">في التصميم الحالي، يتولى Supply Chain Management إدارة حقول **السعر** و **الخصم** و **التكاليف**، و **الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="e748a-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="e748a-177">لا تشكل الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** جزءًا من التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="e748a-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="e748a-178">لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="e748a-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="e748a-179">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="e748a-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="e748a-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e748a-180">QuoteHeader</span></span>

![تعيين القالب في موحد البيانات](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="e748a-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e748a-182">QuoteLine</span></span>

![تعيين القالب في موحد البيانات](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="e748a-184">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="e748a-184">Related topics</span></span>

[<span data-ttu-id="e748a-185">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="e748a-185">Prospect to cash</span></span>](prospect-to-cash.md)

