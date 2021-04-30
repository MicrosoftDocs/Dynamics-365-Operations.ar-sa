---
title: تأجيل تنفيذ عناصر التسلسل في تنسيقات إعداد التقارير الإلكترونية
description: يوضح هذا الموضوع كيفية تأجيل تنفيذ عنصر تسلسل في تنسيق إعداد التقارير الإلكترونية (ER).
author: NickSelin
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: cdcbc828fadce641cbee2cc6135be819a03275c9
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894090"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a><span data-ttu-id="12504-103">تأجيل تنفيذ عناصر التسلسل في تنسيقات إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="12504-103">Defer the execution of sequence elements in ER formats</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="12504-104">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="12504-104">Overview</span></span>

<span data-ttu-id="12504-105">يمكنك استخدام مصمم عمليات إطار عمل [إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md)[لتكوين](tasks/er-format-configuration-2016-11.md)[مكون التنسيق](general-electronic-reporting.md#FormatComponentOutbound)لحل إعداد التقارير الإلكترونية المستخدم لإنشاء المستندات الصادرة بتنسيق نصي.</span><span class="sxs-lookup"><span data-stu-id="12504-105">You can use the Operations designer of the [Electronic reporting (ER)](general-electronic-reporting.md) framework to [configure](tasks/er-format-configuration-2016-11.md) the [format component](general-electronic-reporting.md#FormatComponentOutbound) of an ER solution that is used to generate outbound documents in a text format.</span></span> <span data-ttu-id="12504-106">تتكون البنية الهرمية لمكون التنسيق المكون من عناصر تنسيق بأنواع مختلفة.</span><span class="sxs-lookup"><span data-stu-id="12504-106">The hierarchical structure of the configured format component consists of format elements of various types.</span></span> <span data-ttu-id="12504-107">يتم استخدام عناصر التنسيق هذه لملء المستندات التي تم إنشاؤها بالمعلومات المطلوبة في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="12504-107">These format elements are used to fill generated documents with the required information at runtime.</span></span> <span data-ttu-id="12504-108">عند تشغيل تنسيق إعداد التقارير الإلكترونية، يتم افتراضيًا تشغيل عناصر التنسيق بنفس الترتيب كما هو موضح في التدرج الهرمي للتنسيق: واحد تلو الآخر من أعلى إلى أسفل.</span><span class="sxs-lookup"><span data-stu-id="12504-108">By default, when you run an ER format, the format elements are run in the same order as they are presented in the format hierarchy: one by one, from top to bottom.</span></span> <span data-ttu-id="12504-109">ولكن في وقت التصميم يمكنك تغيير ترتيب التنفيذ لأي عناصر تسلسل لمكون التنسيق المكون.</span><span class="sxs-lookup"><span data-stu-id="12504-109">However, at design time, you can change the execution order for any sequence elements of the configured format component.</span></span>

<span data-ttu-id="12504-110">عن طريق تشغيل خيار <a name="DeferredSequenceExecution"></a>**التنفيذ المؤجل** لعنصر تنسيق تسلسل في التنسيق الذي تم تكوينه، يمكنك تأجيل (إرجاء) تنفيذ هذا العنصر.</span><span class="sxs-lookup"><span data-stu-id="12504-110">By turning on the <a name="DeferredSequenceExecution"></a>**Deferred execution** option for a sequence format element in the configured format, you can defer (postpone) the execution of that element.</span></span> <span data-ttu-id="12504-111">وفي هذه الحالة، لا يتم تشغيل العنصر حتى يتم تشغيل كافة العناصر الأخرى من نفس الأصل.</span><span class="sxs-lookup"><span data-stu-id="12504-111">In this case, the element isn't run until all other elements of its parent have been run.</span></span>

<span data-ttu-id="12504-112">لمعرفة المزيد حول هذه الميزة، أكمل المثال في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="12504-112">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="limitations"></a><span data-ttu-id="12504-113">قيود</span><span class="sxs-lookup"><span data-stu-id="12504-113">Limitations</span></span>

<span data-ttu-id="12504-114">خيار **التنفيذ المؤجل** غير معتمد إلا لعناصر التسلسل التي يتم تكوينها لتنسيق إعداد التقارير الإلكترونية المستخدم لإنشاء مستندات **صادرة** بتنسيق نصي.</span><span class="sxs-lookup"><span data-stu-id="12504-114">The **Deferred execution** option is supported only for sequence elements that are configured for an ER format that is used to generate **outbound** documents in text format.</span></span>

<span data-ttu-id="12504-115">لا ينطبق خيار **التنفيذ المؤجل** على التسلسلات التي تم تكوينها كتسلسلات مقتطعة حيث يكون الحد الأقصى للطول محدودًا.</span><span class="sxs-lookup"><span data-stu-id="12504-115">The **Deferred execution** option isn't applicable to sequences that have been configured as trimmed sequences where the maximum length is limited.</span></span>

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a><span data-ttu-id="12504-116">مثال: تأجيل تنفيذ عنصر تسلسل في تنسيق إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="12504-116">Example: Defer the execution of a sequence element in an ER format</span></span>

<span data-ttu-id="12504-117">توضح الخطوات التالية كيفية تكوين مستخدم في [دور](../sysadmin/tasks/assign-users-security-roles.md)مستشار وظيفة إعداد التقارير الإلكترونية أو مسؤول النظام لتنسيق إعداد التقارير الإلكترونية والذي يحتوي على عنصر تسلسل يختلف فيه ترتيب التنفيذ عن الترتيب الموجود في التدرج الهرمي للتنسيق.</span><span class="sxs-lookup"><span data-stu-id="12504-117">The following steps explain how a user in the System administrator or Electronic reporting functional consultant [role](../sysadmin/tasks/assign-users-security-roles.md) can configure an ER format that contains a sequence element where order of execution differs from the order in the format hierarchy.</span></span>

<span data-ttu-id="12504-118">يمكن تنفيذ هذه الخطوات في شركة **USMF** في Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="12504-118">These steps can be performed in the **USMF** company in Microsoft Dynamics 365 Finance.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="12504-119">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="12504-119">Prerequisites</span></span>

<span data-ttu-id="12504-120">لإكمال هذا المثال، يجب أن يكون لديك حق الوصول إلى شركة **USMF** في Finance لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="12504-120">To complete this example, you must have access to the **USMF** company in Finance for one of the following roles:</span></span>

- <span data-ttu-id="12504-121">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="12504-121">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="12504-122">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="12504-122">System administrator</span></span>

<span data-ttu-id="12504-123">إذا لم تكن قد أكملت المثال الموجود في موضوع [تأجيل تنفيذ عناصر XML في تنسيقات إعداد التقارير الإلكترونية](er-defer-xml-element.md#Example)، فنزِّل [التكوينات](general-electronic-reporting.md#Configuration) التالية لنموذج حل إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="12504-123">If you haven't yet completed the example in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example) topic, download the following [configurations](general-electronic-reporting.md#Configuration) of the sample ER solution.</span></span>

| <span data-ttu-id="12504-124">وصف المحتوى</span><span class="sxs-lookup"><span data-stu-id="12504-124">Content description</span></span>            | <span data-ttu-id="12504-125">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="12504-125">File name</span></span> |
|--------------------------------|-----------|
| <span data-ttu-id="12504-126">تكوين نموذج بيانات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="12504-126">ER data model configuration</span></span>    | [<span data-ttu-id="12504-127">Model to learn deferred elements.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="12504-127">Model to learn deferred elements.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="12504-128">تكوين تعيين نموذج إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="12504-128">ER model mapping configuration</span></span> | [<span data-ttu-id="12504-129">Mapping to learn deferred elements.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="12504-129">Mapping to learn deferred elements.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="12504-130">قبل البدء، يجب أيضًا تنزيل التكوين التالي لنموذج حل إعداد التقارير الإلكترونية وحفظه.</span><span class="sxs-lookup"><span data-stu-id="12504-130">Before you begin, you must also download and save the following configuration of the sample ER solution.</span></span>

| <span data-ttu-id="12504-131">وصف المحتوى</span><span class="sxs-lookup"><span data-stu-id="12504-131">Content description</span></span>     |<span data-ttu-id="12504-132">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="12504-132">File name</span></span> |
|-------------------------|----------|
| <span data-ttu-id="12504-133">تنسيق تكوين ER</span><span class="sxs-lookup"><span data-stu-id="12504-133">ER format configuration</span></span> | [<span data-ttu-id="12504-134">Format to learn deferred sequences.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="12504-134">Format to learn deferred sequences.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a><span data-ttu-id="12504-135">استيراد نموذج تكوينات إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="12504-135">Import the sample ER configurations</span></span>

1. <span data-ttu-id="12504-136">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="12504-136">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="12504-137">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="12504-137">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="12504-138">في صفحة **التكوينات**، في حالة عدم توفر تكوين **Model to learn deferred elements** في شجرة التكوين، استورد تكوين نموذج بيانات إعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="12504-138">On the **Configurations** page, if the **Model to learn deferred elements** configuration isn't available in the configuration tree, import the ER data model configuration:</span></span>

    1. <span data-ttu-id="12504-139">حدد **استبدال**، ثم حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="12504-139">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="12504-140">حدد **استعراض**، وابحث عن ملف **Model to learn deferred elements.1.xml** وحدده، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="12504-140">Select **Browse**, find and select the **Model to learn deferred elements.1.xml** file, and then select **OK**.</span></span>

4. <span data-ttu-id="12504-141">في حالة عدم توفر التكوين **تعيين للتعرف على العناصر المؤجلة** في شجرة التكوين، استورد تكوين تعيين نموذج إعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="12504-141">If the **Mapping to learn deferred elements** configuration isn't available in the configuration tree, import the ER model mapping configuration:</span></span>

    1. <span data-ttu-id="12504-142">حدد **استبدال**، ثم حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="12504-142">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="12504-143">حدد **استعراض**، وابحث عن ملف **تعيين للتعرف على العناصر المؤجلة.1.1.xml** وحدده، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="12504-143">Select **Browse**, find and select the **Mapping to learn deferred elements.1.1.xml** file, and then select **OK**.</span></span>

5. <span data-ttu-id="12504-144">استيراد تكوين تنسيق إعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="12504-144">Import the ER format configuration:</span></span>

    1. <span data-ttu-id="12504-145">حدد **استبدال**، ثم حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="12504-145">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="12504-146">حدد **استعراض**، وابحث عن الملف **Format to learn deferred sequences.1.1.xml** وحدده، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="12504-146">Select **Browse**, find and select the **Format to learn deferred sequences.1.1.xml** file, and then select **OK**.</span></span>

6. <span data-ttu-id="12504-147">في شجرة التكوين ، وسَّع **Model to learn deferred elements**.</span><span class="sxs-lookup"><span data-stu-id="12504-147">In the configuration tree, expand **Model to learn deferred elements**.</span></span>
7. <span data-ttu-id="12504-148">راجع قائمة تكوينات إعداد التقارير الإلكترونية المستوردة في شجرة التكوين.</span><span class="sxs-lookup"><span data-stu-id="12504-148">Review the list of imported ER configurations in the configuration tree.</span></span>

    ![تكوينات إعداد التقارير الإلكترونية المستوردة على صفحة التكوينات](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a><span data-ttu-id="12504-150">تنشيط موفر تكوينات</span><span class="sxs-lookup"><span data-stu-id="12504-150">Activate a configurations provider</span></span>

1. <span data-ttu-id="12504-151">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="12504-151">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="12504-152">في صفحة **ترجمة التكوينات**، في قسم **موفري التكوين**، تحقق من إدراج [ موفر التكوين ](general-electronic-reporting.md#Provider) لنموذج الشركة Litware, Inc (`http://www.litware.com`) ووضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="12504-152">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the [configuration provider](general-electronic-reporting.md#Provider) for the Litware, Inc. (`http://www.litware.com`) sample company is listed, and that it's marked as active.</span></span> <span data-ttu-id="12504-153">في حالة عدم إدراج موفر التكوين، أو عدم وضع علامة عليه كنشط، اتبع الخطوات الموجودة في الموضوع [إنشاء موفر تكوين ووضع علامة عليه على أنه نشط.](./tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="12504-153">If this configuration provider isn't listed, or if it isn't marked as active, follow the steps in the [Create a configuration provider and mark it as active](./tasks/er-configuration-provider-mark-it-active-2016-11.md) topic.</span></span>

    ![نموذج شركة Litware, Inc. في صفحة تكوينات الترجمة](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a><span data-ttu-id="12504-155">مراجعة تعيين النموذج المستورد</span><span class="sxs-lookup"><span data-stu-id="12504-155">Review the imported model mapping</span></span>

<span data-ttu-id="12504-156">راجع إعدادات مكون تعيين نموذج إعداد التقارير الإلكترونية الذي تم تكوينه للوصول إلى حركات الضريبة وعرض البيانات التي يتم الوصول اليها عند الطلب.</span><span class="sxs-lookup"><span data-stu-id="12504-156">Review the settings of the ER model mapping component that is configured to access tax transactions and expose accessed data on request.</span></span>

1. <span data-ttu-id="12504-157">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="12504-157">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="12504-158">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="12504-158">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="12504-159">في صفحة **التكوينات**، في شجرة التكوينات، وسَّع **Model to learn deferred elements**.</span><span class="sxs-lookup"><span data-stu-id="12504-159">On the **Configurations** page, in the configuration tree, expand **Model to learn deferred elements**.</span></span>
4. <span data-ttu-id="12504-160">حدد التكوين **Mapping to learn deferred elements**.</span><span class="sxs-lookup"><span data-stu-id="12504-160">Select the **Mapping to learn deferred elements** configuration.</span></span>
5. <span data-ttu-id="12504-161">حدد **المصمم** لفتح قائمة التعيينات.</span><span class="sxs-lookup"><span data-stu-id="12504-161">Select **Designer** to open the list of mappings.</span></span>
6. <span data-ttu-id="12504-162">حدد **المصمم** لمراجعة تفاصيل التعيين.</span><span class="sxs-lookup"><span data-stu-id="12504-162">Select **Designer** to review the mapping details.</span></span>
7. <span data-ttu-id="12504-163">حدد **إظهار التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="12504-163">Select **Show details**.</span></span>
8. <span data-ttu-id="12504-164">مراجعة مصادر البيانات التي يتم تكوينها للوصول إلى حركات الضريبة:</span><span class="sxs-lookup"><span data-stu-id="12504-164">Review the data sources that are configured to access tax transactions:</span></span>

    - <span data-ttu-id="12504-165">يتم تكوين مصدر بيانات **الحركات** لنوع *سجل الجدول* للوصول إلى جدول التطبيقات **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="12504-165">The **Transactions** data source of the *Table record* type is configured to access records of the **TaxTrans** application table.</span></span>
    - <span data-ttu-id="12504-166">يتم تكون مصدر بيانات **الإيصالات‬** لنوع *الحقل المحسوب* لإرجاع أكواد الإيصالات المطلوبة (**INV-10000349** و **INV-10000350**) كقائمة سجلات.</span><span class="sxs-lookup"><span data-stu-id="12504-166">The **Vouchers** data source of the *Calculated field* type is configured to return the required voucher codes (**INV-10000349** and **INV-10000350**) as a list of records.</span></span>
    - <span data-ttu-id="12504-167">كما يتم تكوين مصدر البيانات **التي تمت تصفيتها** لنوع *الحقل المحسوب* للتحديد، من مصدر بيانات **الحركات**، الحركات الضريبية للإيصالات المطلوبة فقط.</span><span class="sxs-lookup"><span data-stu-id="12504-167">The **Filtered** data source of the *Calculated field* type is configured to select, from the **Transactions** data source, only tax transactions of the required vouchers.</span></span>
    - <span data-ttu-id="12504-168">يتم إضافة الحقل **\$TaxAmoun** لنوع *الحقل المحسوب* لمصدر البيانات **التي تمت تصفيتها** لعرض قيمه الضريبة ذات العلامة المعاكسة.</span><span class="sxs-lookup"><span data-stu-id="12504-168">The **\$TaxAmount** field of the *Calculated field* type is added for the **Filtered** data source to expose the tax value that has the opposite sign.</span></span>
    - <span data-ttu-id="12504-169">يتم تكوين مصدر البيانات **المجمعة** للنوع *التجميع حسب* لتجميع حركات الضريبة المصفاة لمصدر البيانات **التي تمت تصفيتها**.</span><span class="sxs-lookup"><span data-stu-id="12504-169">The **Grouped** data source of the *Group By* type is configured to group filtered tax transactions of the **Filtered** data source.</span></span>
    - <span data-ttu-id="12504-170">يتم تكوين حقل التجميع **TotalSum** لمصدر البيانات **المجمعة** لتلخيص قيم الحقل **\$TaxAmount** لمصدر البيانات **التي تمت تصفيتها** لكافة حركات الضرائب المصفاة لمصدر البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="12504-170">The **TotalSum** aggregation field of the **Grouped** data source is configured to summarize values of the **\$TaxAmount** field of the **Filtered** data source for all filtered tax transactions of that data source.</span></span>

        ![حقل التجميع TotalSum في صفحة تحرير معلمات 'GroupBy'](./media/ER-DeferredSequence-GroupByParameters.png)

9. <span data-ttu-id="12504-172">راجع كيفية ربط مصادر البيانات التي تم تكوينها بنموذج البيانات، وكيفية عرضها للبيانات التي يتم الوصول إليها لتوفيرها في تنسيق إعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="12504-172">Review how the configured data sources are bound to the data model, and how they expose accessed data to make it available in an ER format:</span></span>

    - <span data-ttu-id="12504-173">يتم ربط مصدر البيانات **التي تمت تصفيتها** بحقل نموذج البيانات **Data.List**.</span><span class="sxs-lookup"><span data-stu-id="12504-173">The **Filtered** data source is bound to the **Data.List** field of the data model.</span></span>
    - <span data-ttu-id="12504-174">يتم ربط الحقل **\$TaxAmount** بمصدر البيانات **التي تمت تصفيتها** بحقل نموذج البيانات **Data.List.Value**.</span><span class="sxs-lookup"><span data-stu-id="12504-174">The **\$TaxAmount** field of the **Filtered** data source is bound to the **Data.List.Value** field of the data model.</span></span>
    - <span data-ttu-id="12504-175">يتم ربط الحقل **TotalSum** الخاص بمصدر البيانات **المجمعة** بحقل نموذج البيانات **Data.Summary.Total**.</span><span class="sxs-lookup"><span data-stu-id="12504-175">The **TotalSum** field of the **Grouped** data source is bound to the **Data.Summary.Total** field of the data model.</span></span>

    ![صفحة مصمم تعيين النموذج](./media/ER-DeferredSequence-ModelMapping.png)

10. <span data-ttu-id="12504-177">اغلق صفحات **مصمم تعيين النموذج** و **تعيينات النماذج**.</span><span class="sxs-lookup"><span data-stu-id="12504-177">Close the **Model mapping designer** and **Model mappings** pages.</span></span>

### <a name="review-the-imported-format"></a><span data-ttu-id="12504-178">مراجعة التنسيق المستورد</span><span class="sxs-lookup"><span data-stu-id="12504-178">Review the imported format</span></span>

1. <span data-ttu-id="12504-179">في صفحة **التكوينات**، في شجرة التكوين، حدد التكوين **التنسيق للتعرف على التسلسلات المؤجلة**.</span><span class="sxs-lookup"><span data-stu-id="12504-179">On the **Configurations** page, in the configuration tree, select the **Format to learn deferred sequences** configuration.</span></span>
2. <span data-ttu-id="12504-180">حدد **المصمم** لمراجعة تفاصيل التنسيق.</span><span class="sxs-lookup"><span data-stu-id="12504-180">Select **Designer** to review the format details.</span></span>
3. <span data-ttu-id="12504-181">حدد **إظهار التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="12504-181">Select **Show details**.</span></span>
4. <span data-ttu-id="12504-182">راجع إعدادات مكونات تنسيق إعداد التقارير الإلكترونية التي تم تكوينها لإنشاء مستند صادر بتنسيق نصي يتضمن تفاصيل حركات الضريبة:</span><span class="sxs-lookup"><span data-stu-id="12504-182">Review the settings of the ER format components that are configured to generate an outbound document in text format that includes details of the tax transactions:</span></span>

    - <span data-ttu-id="12504-183">يتم تكوين عنصر تنسيق التسلسل **التقرير\\السطور** لملء المستند الصادر بسطر واحد يتم إنشاؤه من عناصر التسلسل المتداخلة (**الرأس** و **السجل** و **الملخص**).</span><span class="sxs-lookup"><span data-stu-id="12504-183">The **Report\\Lines** sequence format element is configured to fill the outbound document with a single line that is generated from the nested sequence elements (**Header**, **Record**, and **Summary**).</span></span>

        ![عنصر تنسيق تسلسل السطور والعناصر المتداخلة في صفحة مصمم التنسيق](./media/ER-DeferredSequence-Format.png)

    - <span data-ttu-id="12504-185">يتم تكوين عنصر تنسيق التسلسل **التقرير\\السطور\\الرأس**  لملء المستند الصادر بسطر رأس واحد يعرض التاريخ والوقت عند بدء المعالجة.</span><span class="sxs-lookup"><span data-stu-id="12504-185">The **Report\\Lines\\Header** sequence format element is configured to fill the outbound document with a single header line that shows the date and time  when the processing starts.</span></span>
    - <span data-ttu-id="12504-186">يتم تكوين عنصر تنسيق التسلسل **التقرير \\السطور\\السجل** لملء المستند الصادر بسطر واحد يعرض تفاصيل الحركات الضريبية الفردية.</span><span class="sxs-lookup"><span data-stu-id="12504-186">The **Report \\Lines\\Record** sequence format element is configured to fill the outbound document with a single line that shows the details of individual tax transactions.</span></span> <span data-ttu-id="12504-187">ويتم فصل هذه الحركات الضريبية بفاصلة منقوطة.</span><span class="sxs-lookup"><span data-stu-id="12504-187">These tax transactions are separated by a semicolon.</span></span>

        ![عنصر تنسيق تسلسل السجل الذي يستخدم فاصلة منقوطة كمحدد](./media/ER-DeferredSequence-Format1.png)

    - <span data-ttu-id="12504-189">يتم تكوين عنصر تنسيق التسلسل **التقرير\\السطور\\الملخص** لملء المستند الصادر بسطر ملخص واحد يتضمن مجموع قيم الضريبة من حركات الضريبة التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="12504-189">The **Report\\Lines\\Summary** sequence format element is configured to fill the outbound document with a single summary line that includes the sum of the tax values from the processed tax transactions.</span></span>

4. <span data-ttu-id="12504-190">في علامة التبويب **تعيين**، راجع التفاصيل التالية:</span><span class="sxs-lookup"><span data-stu-id="12504-190">On the **Mapping** tab, review the following details:</span></span>

    - <span data-ttu-id="12504-191">ليس من الضروري ربط عنصر **التقرير\\السطور\\الرأس** بمصدر بيانات لإنشاء سطر واحد في مستند صادر.</span><span class="sxs-lookup"><span data-stu-id="12504-191">The **Report\\Lines\\Header** element doesn't have to be bound to a data source to generate a single line in an outbound document.</span></span>
    - <span data-ttu-id="12504-192">ينشئ العنصر **Prefix1** رموز **P1** للإشارة إلى أن السطر المضاف هو سطر رأس التقرير.</span><span class="sxs-lookup"><span data-stu-id="12504-192">The **Prefix1** element generates **P1** symbols to indicate that the line that is added is the report header line.</span></span>
    - <span data-ttu-id="12504-193">ينشئ العنصر **ExecutionDateTime** التاريخ والوقت (بما في ذلك المللي ثواني) عند إضافة رأس السطر.</span><span class="sxs-lookup"><span data-stu-id="12504-193">The **ExecutionDateTime** element generates the date and time (including milliseconds) when the header line is added.</span></span>
    - <span data-ttu-id="12504-194">يتم ربط عنصر **التقرير\\السطور\\ السجل** بقائمة **model.Data.List** لإنشاء سطر واحد لكل سجل من القائمة المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="12504-194">The **Report\\Lines\\Record** element is bound to the **model.Data.List** list to generate a single line for every record from the bound list.</span></span>
    - <span data-ttu-id="12504-195">ينشئ العنصر **Prefix2** رموز **P2** للإشارة إلى أن السطر المضاف يتعلق بتفاصيل الحركات الضريبية.</span><span class="sxs-lookup"><span data-stu-id="12504-195">The **Prefix2** element generates **P2** symbols to indicate that the line that is added is for the tax transaction details.</span></span>
    - <span data-ttu-id="12504-196">يرتبط العنصر **TaxAmount** بـ **model.Data.List.Value** (التي تظهر كـ **\@.قيمة** في عرض المسار النسبي) لإنشاء قيمة الضريبة لحركة الضريبة الحالية.</span><span class="sxs-lookup"><span data-stu-id="12504-196">The **TaxAmount** element is bound to **model.Data.List.Value** (which is shown as **\@.Value** in the relative path view) to generate the tax value of the current tax transaction.</span></span>
    - <span data-ttu-id="12504-197">يعد **RunningTotal** عنصرًا نائبًا للإجمالي الحالي لقيم الضريبة.</span><span class="sxs-lookup"><span data-stu-id="12504-197">The **RunningTotal** element is a placeholder for the running total of the tax values.</span></span> <span data-ttu-id="12504-198">لا يحتوي هذا العنصر على مخرجات في الوقت الحالي، نظرًا لعدم تكوين ربط أو قيمة افتراضية له.</span><span class="sxs-lookup"><span data-stu-id="12504-198">Currently, this element has no output, because neither a binding nor a default value is configured for it.</span></span>
    - <span data-ttu-id="12504-199">ينشئ العنصر **ExecutionDateTime** التاريخ والوقت (بما في ذلك المللي ثوانٍ) عند معالجة الحركة الحالية في هذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="12504-199">The **ExecutionDateTime** element generates the date and time (including milliseconds) when the current transaction is processed in this report.</span></span>
    - <span data-ttu-id="12504-200">ليس من الضروري ربط عنصر **التقرير\\السطور\\الملخص** بمصدر بيانات لإنشاء سطر واحد في مستند صادر.</span><span class="sxs-lookup"><span data-stu-id="12504-200">The **Report\\Lines\\Summary** element doesn't have to be bound to a data source to generate a single line in an outbound document.</span></span>
    - <span data-ttu-id="12504-201">ينشئ العنصر **Prefix3** رموز **P3** للإشارة إلى أن السطر المضاف يحتوي على إجمالي قيمة الضريبة.</span><span class="sxs-lookup"><span data-stu-id="12504-201">The **Prefix3** element generates **P3** symbols to indicate that the line that is added contains the total tax value.</span></span>
    - <span data-ttu-id="12504-202">يرتبط العنصر **TotalTaxAmount** بـ **model.Data.Summary.Total** لإنشاء مجموع قيم الضريبة لحركات الضريبة التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="12504-202">The **TotalTaxAmount** element is bound to **model.Data.Summary.Total** to generate the sum of the tax values of the processed tax transactions.</span></span>
    - <span data-ttu-id="12504-203">ينشئ العنصر **ExecutionDateTime** التاريخ والوقت (بما في ذلك المللي ثوانٍ) عند إضافة سطر التلخيص.</span><span class="sxs-lookup"><span data-stu-id="12504-203">The **ExecutionDateTime** element generates the date and time (including milliseconds) when the summary line is added.</span></span>

    ![علامة التبويب التعيين في صفحة مصمم التنسيق](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a><span data-ttu-id="12504-205">تشغيل التقارير الإلكترونية المستوردة</span><span class="sxs-lookup"><span data-stu-id="12504-205">Run the imported format</span></span>

1. <span data-ttu-id="12504-206">في صفحة **مصمم التنسيق**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="12504-206">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="12504-207">نزِّل الملف الذي يعرضه مستعرض الويب وافتحه للمراجعة.</span><span class="sxs-lookup"><span data-stu-id="12504-207">Download the file that the web browser offers, and open it for review.</span></span>

    ![الملف المنزَّل](./media/ER-DeferredSequence-Run.png)

<span data-ttu-id="12504-209">لاحظ أن سطر التلخيص 22 يعرض مجموع قيم الضريبة للحركات التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="12504-209">Notice that summary line 22 presents the sum of the tax values for the processed transactions.</span></span> <span data-ttu-id="12504-210">نظرًا لتكوين التنسيق لاستخدام الربط **model.Data.Summary.Total** لإرجاع هذا المجموع، يتم حساب المجموع باستدعاء تجميع **TotalSum** لمصدر البيانات **المجمعة** للنوع *GroupBy* الذي يستخدم تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="12504-210">Because the format is configured to use the **model.Data.Summary.Total** binding to return this sum, the sum is calculated by calling the **TotalSum** aggregation of the **Grouped** data source of the *GroupBy* type that uses the model mapping.</span></span> <span data-ttu-id="12504-211">لحساب هذا التجميع، يتكرر تعيين النموذج في كافة الحركات التي تم تحديدها في مصدر البيانات **التي تمت تصفيتها**.</span><span class="sxs-lookup"><span data-stu-id="12504-211">To calculate this aggregation, model mapping iterates over all transactions that have been selected in the **Filtered** data source.</span></span> <span data-ttu-id="12504-212">وبمقارنة أوقات تنفيذ السطرين 21 و 22، يمكنك تحديد استغراق عملية حساب المجموع 10 مللي ثانية (بالملي ثانية).</span><span class="sxs-lookup"><span data-stu-id="12504-212">By comparing the execution times of lines 21 and 22, you can determine that calculation of the sum took 10 milliseconds (ms).</span></span> <span data-ttu-id="12504-213">وبمقارنة أوقات تنفيذ السطرين 2 و 21، يمكنك تحديد استغراق عملية إنشاء كل سطور الحركات 7 مللي ثانية (بالملي ثانية).</span><span class="sxs-lookup"><span data-stu-id="12504-213">By comparing the execution times of lines 2 and 21, you can determine that generation of all transactional lines took 7 ms.</span></span> <span data-ttu-id="12504-214">لذلك كان إجمالي الوقت المطلوب هو 17 مللي ثانية.</span><span class="sxs-lookup"><span data-stu-id="12504-214">Therefore, a total of 17 ms was required.</span></span>

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a><span data-ttu-id="12504-215">تعديل التنسيق بحيث يعتمد التجميع على المخرجات المنشأة</span><span class="sxs-lookup"><span data-stu-id="12504-215">Modify the format so that the summing is based on generated output</span></span>

<span data-ttu-id="12504-216">إذا كان حجم الحركات أكبر بكثير من الحجم في المثال الحالي، فقد يزيد وقت الجمع ويسبب مشاكل في الأداء.</span><span class="sxs-lookup"><span data-stu-id="12504-216">If the volume of transactions is much larger than the volume in the current example, the summing time might increase and cause performance issues.</span></span> <span data-ttu-id="12504-217">ومن خلال تغيير إعداد التنسيق، يمكنك المساعدة في تجنب مشكلات الأداء هذه.</span><span class="sxs-lookup"><span data-stu-id="12504-217">By changing the setting of the format, you can help prevent these performance issues.</span></span> <span data-ttu-id="12504-218">ونظرًا لوصولك إلى قيم الضريبة لتضمينها في التقرير الذي يتم إنشاؤه، يمكنك إعادة استخدام هذه المعلومات لجمع قيم الضريبة.</span><span class="sxs-lookup"><span data-stu-id="12504-218">Because you access tax values to include them in the generated report, you can reuse this information to sum tax values.</span></span> <span data-ttu-id="12504-219">لمزيد من المعلومات، راجع [تكوين التنسيق لتنفيذ عمليات الجرد والتجميع‬](./tasks/er-format-counting-summing-1.md).</span><span class="sxs-lookup"><span data-stu-id="12504-219">For more information, see [Configure format to do counting and summing](./tasks/er-format-counting-summing-1.md).</span></span>

1. <span data-ttu-id="12504-220">في صفحة **مصمم التنسيق**، وفي علامة التبويب **التنسيق**، حدد عنصر ملف **التقرير** في شجرة التنسيق.</span><span class="sxs-lookup"><span data-stu-id="12504-220">On the **Format designer** page, on the **Format** tab, select the **Report** file element in the format tree.</span></span>
2. <span data-ttu-id="12504-221">عيّن الخيار **تجميع تفاصيل المخرجات** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="12504-221">Set the **Collect output details** option to **Yes**.</span></span> <span data-ttu-id="12504-222">يمكنك الآن تكوين هذا التنسيق باستخدام محتوى تقرير موجود كمصدر بيانات يمكن الوصول إليه باستخدام وظائف إعداد التقارير الإلكترونية المضمنة في فئة [تجميع البيانات](er-functions-category-data-collection.md).</span><span class="sxs-lookup"><span data-stu-id="12504-222">You can now configure this format by using the content of an existing report as a data source that can be accessed by using the built-in ER functions in the [Data collection](er-functions-category-data-collection.md) category.</span></span>
3. <span data-ttu-id="12504-223">في علامة التبويب **تعيين**، حدد  عنصر تسلسل **سطور\\التقرير**.</span><span class="sxs-lookup"><span data-stu-id="12504-223">On the **Mapping** tab, select the **Report\\Lines** sequence element.</span></span>
4. <span data-ttu-id="12504-224">كوِّن تعبير **اسم مفتاح البيانات المجمعة** ليكون `WsColumn`.</span><span class="sxs-lookup"><span data-stu-id="12504-224">Configure the **Collected data key name** expression as `WsColumn`.</span></span>
5. <span data-ttu-id="12504-225">كوِّن تعبير **قيمة مفتاح البيانات المجمعة** ليكون `WsRow`.</span><span class="sxs-lookup"><span data-stu-id="12504-225">Configure the **Collected data key value** expression as `WsRow`.</span></span>

    ![عنصر تسلسل السطور في صفحة مصمم التنسيق](./media/ER-DeferredSequence-Format3.png)

6. <span data-ttu-id="12504-227">حدد عنصر **التقرير\\السطور\\السجل\\TaxAmount** الرقمي.</span><span class="sxs-lookup"><span data-stu-id="12504-227">Select the **Report\\Lines\\Record\\TaxAmount** numeric element.</span></span>
7. <span data-ttu-id="12504-228">كوِّن تعبير **اسم مفتاح البيانات المجمعة** ليكون `SummingAmountKey`.</span><span class="sxs-lookup"><span data-stu-id="12504-228">Configure the **Collected data key name** expression as `SummingAmountKey`.</span></span>

    ![عنصر TaxAmount الرقمي في صفحة مصمم التنسيق](./media/ER-DeferredSequence-Format4.png)

    <span data-ttu-id="12504-230">ويمكنك اعتبار هذا الإعداد بمثابة تنفيذ ورقة عمل ظاهرية، حيث يتم إلحاق قيمة خلية A1 بقيمة مبلغ الضريبة من كل حركة ضريبية تتم معالجتها.</span><span class="sxs-lookup"><span data-stu-id="12504-230">You can consider this setting the fulfillment of a virtual worksheet, where the value of cell A1 is appended with the value of the tax amount from every processed tax transaction.</span></span>

8. <span data-ttu-id="12504-231">حدد العنصر الرقمي **التقرير\\السطور\\السجل\\RunningTotal**، ثم حدد **تحرير المعادلة‬**.</span><span class="sxs-lookup"><span data-stu-id="12504-231">Select the **Report\\Lines\\Record\\RunningTotal** numeric element, and then select **Edit formula**.</span></span>
9. <span data-ttu-id="12504-232">كوِّن التعبير `SUMIF(SummingAmountKey, WsColumn, WsRow)` باستخدام وظيفة إعداد التقارير الإلكترونية [SUMIF](er-functions-datacollection-sumif.md) المضمنة.</span><span class="sxs-lookup"><span data-stu-id="12504-232">Configure the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression by using the built-in [SUMIF](er-functions-datacollection-sumif.md) ER function.</span></span>
10. <span data-ttu-id="12504-233">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="12504-233">Select **Save**.</span></span>

    ![تعبير SUMIF](./media/ER-DeferredSequence-FormulaDesigner.png)

11. <span data-ttu-id="12504-235">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="12504-235">Close the **Formula designer** page.</span></span>
12. <span data-ttu-id="12504-236">حدد **حفظ**، ثم حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="12504-236">Select **Save**, and then select **Run**.</span></span>
13. <span data-ttu-id="12504-237">نزِّل الملف الذي يعرضه مستعرض الويب وراجعه.</span><span class="sxs-lookup"><span data-stu-id="12504-237">Download and review the file that the web browser offers.</span></span>

    ![الملف المنزَّل](./media/ER-DeferredSequence-Run1.png)

    <span data-ttu-id="12504-239">يحتوي السطر 21 على الإجمالي الحالي لقيم الضريبة التي يتم حسابها لكافة الحركات التي تمت معالجتها باستخدام المخرجات المنشأة كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="12504-239">Line 21 contains the running total of tax values that is calculated for all processed transactions by using the generated output as a data source.</span></span> <span data-ttu-id="12504-240">يبدأ مصدر البيانات هذا من بداية التقرير ويستمر خلال حركة الضريبة الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="12504-240">This data source starts from the beginning of the report and continues through the last tax transaction.</span></span> <span data-ttu-id="12504-241">يحتوي السطر 22 على مجموع قيم الضريبة لكافة الحركات التي تمت معالجتها والتي يتم حسابها في تعيين النموذج باستخدام مصدر بيانات النوع *GroupBy*.</span><span class="sxs-lookup"><span data-stu-id="12504-241">Line 22 contains the sum of the tax values for all processed transactions that are calculated in the model mapping by using the data source of the *GroupBy* type.</span></span> <span data-ttu-id="12504-242">لاحظ أن هذه القيم متساوية.</span><span class="sxs-lookup"><span data-stu-id="12504-242">Notice that these values are equal.</span></span> <span data-ttu-id="12504-243">لذا يمكن استخدام التجميع المبني على المخرجات بدلاً من **GroupBy**.</span><span class="sxs-lookup"><span data-stu-id="12504-243">Therefore, the output-based summing can be used instead of **GroupBy**.</span></span> <span data-ttu-id="12504-244">وبمقارنة أوقات تنفيذ السطرين 2 و 21، يمكنك تحديد استغراق عملية إنشاء كل سطور الحركات والتجميع 9 مللي ثانية.</span><span class="sxs-lookup"><span data-stu-id="12504-244">By comparing the execution times of lines 2 and 21, you can determine that generation of all the transactional lines and summing took 9 ms.</span></span> <span data-ttu-id="12504-245">لذا فيما يتعلق بإنشاء السطور التفصيلية وتجميع قيم الضريبة، فإن التنسيق المعدل يكون أسرع مرتين تقريبًا من التنسيق الأصلي.</span><span class="sxs-lookup"><span data-stu-id="12504-245">Therefore, as far as the generation of detailed lines and the summing of tax values are concerned, the modified format is approximately two times faster than the original format.</span></span>

14. <span data-ttu-id="12504-246">حدد العنصر الرقمي **التقرير\\السطور\\الملخص\\TotalTaxAmount**، ثم حدد **تحرير المعادلة‬**.</span><span class="sxs-lookup"><span data-stu-id="12504-246">Select the **Report\\Lines\\Summary\\TotalTaxAmount** numeric element, and then select **Edit formula**.</span></span>
15. <span data-ttu-id="12504-247">أدخل التعبير `SUMIF(SummingAmountKey, WsColumn, WsRow)` بدلاً من التعبير الموجود.</span><span class="sxs-lookup"><span data-stu-id="12504-247">Enter the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression instead of the existing expression.</span></span>
16. <span data-ttu-id="12504-248">حدد **حفظ**، ثم حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="12504-248">Select **Save**, and then select **Run**.</span></span>
17. <span data-ttu-id="12504-249">نزِّل الملف الذي يعرضه مستعرض الويب وراجعه.</span><span class="sxs-lookup"><span data-stu-id="12504-249">Download and review the file that the web browser offers.</span></span>

    ![الملف المنزَّل](./media/ER-DeferredSequence-Run2.png)

    <span data-ttu-id="12504-251">لاحظ أن الإجمالي الحالي لقيم الضريبة في سطر تفاصيل الحركة الأخيرة يساوي الآن مجموع سطر الملخص.</span><span class="sxs-lookup"><span data-stu-id="12504-251">Notice that the running total of tax values on the last transaction details line now equals the sum on the summary line.</span></span>

### <a name="put-values-of-output-based-summing-in-the-report-header"></a><span data-ttu-id="12504-252">وضع قيم التجميع المبني على المخرجات في رأس التقرير</span><span class="sxs-lookup"><span data-stu-id="12504-252">Put values of output-based summing in the report header</span></span>

<span data-ttu-id="12504-253">،إذا كان من الضروري على سبيل المثال تقديم مجموع قيم الضرائب في رأس التقرير، يمكنك تعديل التنسيق لديك.</span><span class="sxs-lookup"><span data-stu-id="12504-253">If, for example, you must present the sum of tax values in the header of your report, you can modify your format.</span></span>

1. <span data-ttu-id="12504-254">في صفحة  **مصمم التنسيق**، وفي علامة التبويب **التنسيق**، حدد عنصر التسلسل **التقرير\\السطور\\الملخص**.</span><span class="sxs-lookup"><span data-stu-id="12504-254">On the **Format designer** page, on the **Format** tab, select the **Report\\Lines\\Summary** sequence element.</span></span>
2. <span data-ttu-id="12504-255">حدد **تحريك لأعلى**.</span><span class="sxs-lookup"><span data-stu-id="12504-255">Select **Move up**.</span></span>
3. <span data-ttu-id="12504-256">حدد **حفظ**، ثم حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="12504-256">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="12504-257">نزِّل الملف الذي يعرضه مستعرض الويب وراجعه.</span><span class="sxs-lookup"><span data-stu-id="12504-257">Download and review the file that the web browser offers.</span></span>

    ![الملف المنزَّل](./media/ER-DeferredSequence-Run3.png)

    <span data-ttu-id="12504-259">لاحظ أن مجموع قيم الضريبة في سطر الملخص 2 يساوي الآن 0 (صفر)، لأن هذا المجموع يتم حسابه الآن استنادًا إلى المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="12504-259">Notice that the sum of tax values on summary line 2 now equals 0 (zero), because this sum is now calculated based on the generated output.</span></span> <span data-ttu-id="12504-260">عند إنشاء السطر 2، لن تحتوي المخرجات المنشأة بعد على السطور التي تحتوي على تفاصيل الحركة.</span><span class="sxs-lookup"><span data-stu-id="12504-260">When line 2 is generated, the generated output doesn't yet contain lines that have transaction details.</span></span> <span data-ttu-id="12504-261">يمكنك تكوين هذا التنسيق لتأجيل تنفيذ عنصر التسلسل **التقرير\\السطور\\الملخص** حتى يتم تشغيل عنصر التسلسل **التقرير\\السطور\\السجل** لكل الحركات الضريبية.</span><span class="sxs-lookup"><span data-stu-id="12504-261">You can configure this format to defer the execution of the **Report\\Lines\\Summary** sequence element until the **Report\\Lines\\Record** sequence element has been run for all tax transactions.</span></span>

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a><span data-ttu-id="12504-262">تأجيل تنفيذ تسلسل الملخص حتى يتم استخدام الإجمالي المحسوب</span><span class="sxs-lookup"><span data-stu-id="12504-262">Defer the execution of the summary sequence so that the calculated total is used</span></span>

1. <span data-ttu-id="12504-263">في صفحة  **مصمم التنسيق**، وفي علامة التبويب **التنسيق**، حدد عنصر التسلسل **التقرير\\السطور\\الملخص**.</span><span class="sxs-lookup"><span data-stu-id="12504-263">On the **Format designer** page, on the **Format** tab, select the **Report\\Lines\\Summary** sequence element.</span></span>
2. <span data-ttu-id="12504-264">عيّن الخيار **التنفيذ المؤجل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="12504-264">Set the **Deferred execution** option to **Yes**.</span></span>

    ![خيار التنفيذ المؤجل لعنصر تسلسل الملخص في صفحة مصمم التنسيق](./media/ER-DeferredSequence-Format5.png)

3. <span data-ttu-id="12504-266">حدد **حفظ**، ثم حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="12504-266">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="12504-267">نزِّل الملف الذي يعرضه مستعرض الويب وراجعه.</span><span class="sxs-lookup"><span data-stu-id="12504-267">Download and review the file that the web browser offers.</span></span>

    ![الملف المنزَّل](./media/ER-DeferredSequence-Run4.png)

    <span data-ttu-id="12504-269">يتم الآن تشغيل عنصر تسلسل **التقرير\\السطور \\الملخص** فقط بعد تشغيل كافة العناصر الأخرى التي تم إدراجها ضمن العنصر الأصلي **التقرير\\السطور**.</span><span class="sxs-lookup"><span data-stu-id="12504-269">The **Report\\Lines\\Summary** sequence element is now run only after all other items that are nested under its parent element, **Report\\Lines**, have been run.</span></span> <span data-ttu-id="12504-270">لذا يتم تشغيله بعد تشغيل عنصر التسلسل **التقرير\\السطور \\السجل** لكل الحركات الضريبية لمصدر البيانات **model.Data.List**.</span><span class="sxs-lookup"><span data-stu-id="12504-270">Therefore, it's run after the **Report\\Lines\\Record** sequence element has been run for all tax transactions of the **model.Data.List** data source.</span></span> <span data-ttu-id="12504-271">وتوضح أوقات تنفيذ السطور 1 و2 و3 والسطر الأخير 22 هذه الحقيقة.</span><span class="sxs-lookup"><span data-stu-id="12504-271">The execution times of lines 1, 2, and 3, and of the last line, 22, reveal this fact.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12504-272">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="12504-272">Additional resources</span></span>

- [<span data-ttu-id="12504-273">تكوين التنسيق لتنفيذ عمليات الجرد والتجميع</span><span class="sxs-lookup"><span data-stu-id="12504-273">Configure format to do counting and summing</span></span>](./tasks/er-format-counting-summing-1.md)
- [<span data-ttu-id="12504-274">تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="12504-274">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="12504-275">تأجيل تنفيذ عناصر XML في تنسيقات إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="12504-275">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]