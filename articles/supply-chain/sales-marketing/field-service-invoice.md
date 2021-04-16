---
title: مزامنة فواتير الاتفاقيات في Field Service مع فواتير النص الحر في Supply Chain Management
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فواتير الاتفاقيات في Dynamics 365 Field Service مع فواتير النص الحر في Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: f3066741781bd9058e09d7f577a35df4c9b453d4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819198"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="b4423-103">مزامنة فواتير الاتفاقيات في Field Service مع فواتير النص الحر في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b4423-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b4423-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فواتير الاتفاقيات في Dynamics 365 Field Service مع فواتير النص الحر في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b4423-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b4423-105">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="b4423-105">Templates and tasks</span></span>

<span data-ttu-id="b4423-106">يتم استخدام القالب والمهام الأساسية التالية لتشغيل مزامنة فواتير الاتفاقيات من Field Service لفواتير النص الحر في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b4423-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="b4423-107">**اسم القالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="b4423-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="b4423-108">فواتير الاتفاقيات (Field Service إلى Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="b4423-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="b4423-109">**أسماء المهام في مشروع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="b4423-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="b4423-110">عناوين الفواتير</span><span class="sxs-lookup"><span data-stu-id="b4423-110">Invoice headers</span></span>
- <span data-ttu-id="b4423-111">بنود الفاتورة</span><span class="sxs-lookup"><span data-stu-id="b4423-111">Invoice lines</span></span>

<span data-ttu-id="b4423-112">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة فواتير الاتفاقيات:</span><span class="sxs-lookup"><span data-stu-id="b4423-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="b4423-113">الحسابات (Sales إلى Supply Chain Management) - مباشر</span><span class="sxs-lookup"><span data-stu-id="b4423-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="b4423-114">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="b4423-114">Entity set</span></span>

| <span data-ttu-id="b4423-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="b4423-115">Field Service</span></span>  | <span data-ttu-id="b4423-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b4423-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="b4423-117">الفواتير</span><span class="sxs-lookup"><span data-stu-id="b4423-117">invoices</span></span>       | <span data-ttu-id="b4423-118">رؤوس فاتورة النص الحر لعميل Dataverse</span><span class="sxs-lookup"><span data-stu-id="b4423-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="b4423-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="b4423-119">invoicedetails</span></span> | <span data-ttu-id="b4423-120">بنود فاتورة النص الحر لعميل Dataverse</span><span class="sxs-lookup"><span data-stu-id="b4423-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="b4423-121">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="b4423-121">Entity flow</span></span>

<span data-ttu-id="b4423-122">يمكن مزامنة الفواتير التي يتم إنشاؤها من اتفاقية في Field Service مع Supply Chain Management عبر مشروع تكامل بيانات Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b4423-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="b4423-123">ستتم مزامنة تحديثات هذه الفواتير مع فواتير النص الحر في Supply Chain Management إذا كانت حالة المحاسبة للفواتير ذات النص الحر **قيد المعالجة**.</span><span class="sxs-lookup"><span data-stu-id="b4423-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="b4423-124">بعد ترحيل فواتير النص الحر في Supply Chain Management، وتحديث حالة المحاسبة إلى **مكتمل**، لن تتمكن بعد ذلك من مزامنة التحديثات من Field Service.</span><span class="sxs-lookup"><span data-stu-id="b4423-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b4423-125">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="b4423-125">Field Service CRM solution</span></span>

<span data-ttu-id="b4423-126">تمت إضافة عمود **لديه بنود في أصل الاتفاقية** إلى جدول **الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="b4423-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="b4423-127">يساعد هذا العمود على ضمان مزامنة الفواتير التي تم إنشاؤها من اتفاقية.</span><span class="sxs-lookup"><span data-stu-id="b4423-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="b4423-128">تكون القيمة **صواب** إذا كانت الفاتورة تحتوي على بند فاتورة واحد على الأقل موجودة أصلاً في اتفاقية.</span><span class="sxs-lookup"><span data-stu-id="b4423-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="b4423-129">تمت إضافة عمود **لديه أصل الاتفاقية** إلى جدول **الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="b4423-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="b4423-130">يساعد هذا العمود على ضمان مزامنة بنود الفواتير التي تم إنشاؤها من اتفاقية.</span><span class="sxs-lookup"><span data-stu-id="b4423-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="b4423-131">تكون القيمة **صواب** إذا كان بند الفاتورة نشأ من اتفاقية.</span><span class="sxs-lookup"><span data-stu-id="b4423-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="b4423-132">**تاريخ الفاتورة** عبارة عن حقل إلزامي في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b4423-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="b4423-133">لذلك، يجب أن يكون للعمود قيمة في Field Service قبل إجراء المزامنة.</span><span class="sxs-lookup"><span data-stu-id="b4423-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="b4423-134">لتلبية هذا المتطلب، تتم إضافة المنطق التالي:</span><span class="sxs-lookup"><span data-stu-id="b4423-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="b4423-135">إذا كان عمود **تاريخ الفاتورة** فارغًا في جدول **الفاتورة** (بمعنى، في حالة عدم وجود قيمة)، يتم تعيينه إلى التاريخ الحالي عندما تتم إضافة بند فاتورة ينشأ من اتفاقية.</span><span class="sxs-lookup"><span data-stu-id="b4423-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="b4423-136">يمكن للمستخدم تغيير عمود **تاريخ الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="b4423-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="b4423-137">ومع ذلك، عندما يحاول المستخدم حفظ فاتورة تنشأ من اتفاقية، فإنه يتلقى خطأ في عملية أعمال إذا كان عمود **تاريخ الفاتورة** فارغاً في الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="b4423-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b4423-138">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="b4423-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="b4423-139">في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b4423-139">In Supply Chain Management</span></span>

<span data-ttu-id="b4423-140">يجب إعداد أصل فاتورة للتكامل، لتمييز الفواتير ذات النص الحر في Supply Chain Management والتي تم إنشاؤها من فواتير الاتفاقيات في Field Service.</span><span class="sxs-lookup"><span data-stu-id="b4423-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="b4423-141">عندما تشتمل فاتورة على أصل فاتورة من نوع **تكامل فاتورة الاتفاقية**، يتم عرض حقل **رقم الفاتورة الخارجية** في عنوان **فاتورة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="b4423-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="b4423-142">بالإضافة إلى الظهور في عنوان الفاتورة، يمكن استخدام معلومات **رقم الفاتورة الخارجية** للمساعدة في ضمان تصفية الفواتير التي تم إنشاؤها من فواتير الاتفاقيات في Field Service أثناء مزامنة الفواتير من Supply Chain Management إلى Field Service.</span><span class="sxs-lookup"><span data-stu-id="b4423-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="b4423-143">انتقل إلى **الحسابات المدينة** \> **الإعداد** \> **أكواد أصل الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="b4423-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="b4423-144">حدد **جديد** لإنشاء أصل فاتورة جديد.</span><span class="sxs-lookup"><span data-stu-id="b4423-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="b4423-145">في حقل **أصل الفاتورة**، أدخل اسمًا لأصل الفاتورة، مثل **FS**.</span><span class="sxs-lookup"><span data-stu-id="b4423-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="b4423-146">في حقل **الوصف**، أدخل وصفاً، مثل **فاتورة اتفاقية Field Service**.</span><span class="sxs-lookup"><span data-stu-id="b4423-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="b4423-147">حدد خانة الاختيار **مهمة نوع الأصل**.</span><span class="sxs-lookup"><span data-stu-id="b4423-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="b4423-148">قم بتعيين حقل **نوع أصل الفاتورة** إلى **تكامل فاتورة الاتفاقية**.</span><span class="sxs-lookup"><span data-stu-id="b4423-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="b4423-149">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b4423-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="b4423-150">في مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="b4423-150">In the Data Integration project</span></span>

<span data-ttu-id="b4423-151">المهمة: **بنود الفاتورة**</span><span class="sxs-lookup"><span data-stu-id="b4423-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="b4423-152">تأكد من تحديث القيمة الافتراضية لحقل Supply Chain Management **قيمة عرض الحساب الرئيسي** لمطابقة القيمة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b4423-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="b4423-153">قيمة القالب الافتراضية هي **401100**.</span><span class="sxs-lookup"><span data-stu-id="b4423-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b4423-154">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="b4423-154">Template mapping in Data integration</span></span>

<span data-ttu-id="b4423-155">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="b4423-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="b4423-156">فواتير الاتفاقيات (Field Service إلى Supply Chain Management): رؤوس الفواتير</span><span class="sxs-lookup"><span data-stu-id="b4423-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="b4423-157">[![تعيين القالب في تكامل البيانات](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="b4423-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="b4423-158">فواتير الاتفاقيات (Field Service إلى Supply Chain Management): بنود الفواتير</span><span class="sxs-lookup"><span data-stu-id="b4423-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="b4423-159">[![تعيين القالب في تكامل البيانات](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="b4423-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]