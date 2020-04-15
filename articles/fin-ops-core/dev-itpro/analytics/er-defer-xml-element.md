---
title: تأجيل تنفيذ عناصر XML في تنسيقات إعداد التقارير الإلكترونية
description: يوضح هذا الموضوع كيفية تأجيل تنفيذ عنصر XML في تنسيق إعداد التقارير الإلكترونية (ER).
author: NickSelin
manager: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58381f491cda199d77e555e5d3da04714b6a5f8f
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138913"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a><span data-ttu-id="46642-103">تأجيل تنفيذ عناصر XML في تنسيقات إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="46642-103">Defer the execution of XML elements in ER formats</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="46642-104">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="46642-104">Overview</span></span>

<span data-ttu-id="46642-105">يمكنك استخدام مصمم عمليات إطار عمل [إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md) [لتكوين](./tasks/er-format-configuration-2016-11.md) [مكون التنسيق](general-electronic-reporting.md#FormatComponentOutbound) لحل إعداد التقارير الإلكترونية المستخدم لإنشاء المستندات الصادرة بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="46642-105">You can use the Operations designer of the [Electronic reporting (ER)](general-electronic-reporting.md) framework to [configure](./tasks/er-format-configuration-2016-11.md) the [format component](general-electronic-reporting.md#FormatComponentOutbound) of an ER solution that is used to generate outbound documents in XML format.</span></span> <span data-ttu-id="46642-106">تتكون البنية الهرمية لمكون التنسيق المكون من عناصر تنسيق بأنواع مختلفة.</span><span class="sxs-lookup"><span data-stu-id="46642-106">The hierarchical structure of the configured format component consists of format elements of various types.</span></span> <span data-ttu-id="46642-107">يتم استخدام عناصر التنسيق هذه لملء المستندات التي تم إنشاؤها بالمعلومات المطلوبة في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="46642-107">These format elements are used to fill generated documents with the required information at runtime.</span></span> <span data-ttu-id="46642-108">عند تشغيل تنسيق إعداد التقارير الإلكترونية، يتم افتراضيًا تشغيل عناصر التنسيق بنفس الترتيب كما هو موضح في التدرج الهرمي للتنسيق: واحد تلو الآخر من أعلى إلى أسفل.</span><span class="sxs-lookup"><span data-stu-id="46642-108">By default, when you run an ER format, the format elements are run in the same order as they are presented in the format hierarchy: one by one, from top to bottom.</span></span> <span data-ttu-id="46642-109">ولكن في وقت التصميم يمكنك تغيير ترتيب التنفيذ لأي عناصر XML لمكون التنسيق المكون.</span><span class="sxs-lookup"><span data-stu-id="46642-109">However, at design time, you can change the execution order for any XML elements of the configured format component.</span></span>

<span data-ttu-id="46642-110">بتشغيل خيار <a name="DeferredXmlElementExecution"></a>**التنفيذ المؤجل** لعنصر XML في التنسيق المكوَّن، يمكنك تأجيل (إرجاء) تنفيذ هذا العنصر.</span><span class="sxs-lookup"><span data-stu-id="46642-110">By turning on the <a name="DeferredXmlElementExecution"></a>**Deferred execution** option for an XML element in the configured format, you can defer (postpone) the execution of that element.</span></span> <span data-ttu-id="46642-111">وفي هذه الحالة، لا يتم تشغيل العنصر حتى يتم تشغيل كافة العناصر الأخرى من نفس الأصل.</span><span class="sxs-lookup"><span data-stu-id="46642-111">In this case, the element isn't run until all other elements of its parent have been run.</span></span>

<span data-ttu-id="46642-112">لمعرفة المزيد حول هذه الميزة، أكمل المثال في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="46642-112">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="limitations"></a><span data-ttu-id="46642-113">قيود</span><span class="sxs-lookup"><span data-stu-id="46642-113">Limitations</span></span>

<span data-ttu-id="46642-114">خيار **التنفيذ المؤجل** غير معتمد إلا لعناصر XML التي يتم تكوينها لتنسيق إعداد التقارير الإلكترونية المستخدم لإنشاء مستندات **صادرة** بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="46642-114">The **Deferred execution** option is supported only for XML elements that are configured for an ER format that is used to generate **outbound** documents in XML format.</span></span>

<span data-ttu-id="46642-115">خيار **التنفيذ المؤجل** غير معتمد إلا لعناصر xml التي توجد في عنصر xml واحد آخر.</span><span class="sxs-lookup"><span data-stu-id="46642-115">The **Deferred execution** option is supported only for XML elements that reside in only one other XML element.</span></span> <span data-ttu-id="46642-116">لذا لا ينطبق على عناصر XML التي تتواجد في أنواع أخرى من عناصر التنسيق (على سبيل المثال، في عنصر**تسلسل XML**).</span><span class="sxs-lookup"><span data-stu-id="46642-116">Therefore, it isn't applicable to XML elements that reside in other types of format elements (for example, in an **XML sequence** element).</span></span>

<span data-ttu-id="46642-117">خيار **التنفيذ المؤجل** غير معتمد لعناصر XML الموجودة في عنصر التنسيق**العام\\الملف** عند تعيين خيار**تقسيم الملف** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="46642-117">The **Deferred execution** option isn't supported for XML elements that reside in the **Common\\File** format element when the **Split file** option is set to **Yes**.</span></span> <span data-ttu-id="46642-118">لمزيد من المعلومات حول كيفية تقسيم ملفات XML، راجع [تقسيم ملفات XML المنشأة حسب حجم الملف وكمية المحتوى](er-split-files.md).</span><span class="sxs-lookup"><span data-stu-id="46642-118">For more information about how to split XML files, see [Split generated XML files based on file size and content quantity](er-split-files.md).</span></span>

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a><span data-ttu-id="46642-119">مثال: تأجيل تنفيذ عنصر XML في تنسيق إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="46642-119">Example: Defer the execution of an XML element in an ER format</span></span>

<span data-ttu-id="46642-120">توضح الخطوات التالية كيفية تكوين مستخدم في [دور](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles)مستشار وظيفة إعداد التقارير الإلكترونية أو مسؤول النظام لتنسيق إعداد التقارير الإلكترونية الذي يحتوي على عنصر XML يختلف فيه ترتيب التنفيذ عن الترتيب الموجود في التدرج الهرمي للتنسيق.</span><span class="sxs-lookup"><span data-stu-id="46642-120">The following steps explain how a user in the System administrator or Electronic reporting functional consultant [role](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) can configure an ER format that contains an XML element where the order of execution differs from the order in the format hierarchy.</span></span>

<span data-ttu-id="46642-121">يمكن تنفيذ هذه الخطوات في شركة **USMF** في Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="46642-121">These steps can be performed in the **USMF** company in Microsoft Dynamics 365 Finance.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="46642-122">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="46642-122">Prerequisites</span></span>

<span data-ttu-id="46642-123">لإكمال هذا المثال، يجب أن يكون لديك حق الوصول إلى شركة **USMF** في Finance لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="46642-123">To complete this example, you must have access to the **USMF** company in Finance for one of the following roles:</span></span>

- <span data-ttu-id="46642-124">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="46642-124">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="46642-125">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="46642-125">System administrator</span></span>

<span data-ttu-id="46642-126">إذا لم تكن قد أكملت بعد المثال الموجود في موضوع [تأجيل تنفيذ عناصر التسلسل في تنسيقات إعداد التقارير الإلكترونية](er-defer-sequence-element.md#Example)، فنزِّل [التكوينات](general-electronic-reporting.md#Configuration) التالية لنموذج حل إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="46642-126">If you haven't yet completed the example in the [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) topic, download the following [configurations](general-electronic-reporting.md#Configuration) of the sample ER solution.</span></span>

| <span data-ttu-id="46642-127">وصف المحتوى</span><span class="sxs-lookup"><span data-stu-id="46642-127">Content description</span></span>            | <span data-ttu-id="46642-128">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="46642-128">File name</span></span> |
|--------------------------------|-----------|
| <span data-ttu-id="46642-129">تكوين نموذج بيانات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="46642-129">ER data model configuration</span></span>    | [<span data-ttu-id="46642-130">Model to learn deferred elements.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="46642-130">Model to learn deferred elements.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="46642-131">تكوين تعيين نموذج إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="46642-131">ER model mapping configuration</span></span> | [<span data-ttu-id="46642-132">Mapping to learn deferred elements.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="46642-132">Mapping to learn deferred elements.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="46642-133">قبل البدء، يجب أيضًا تنزيل التكوين التالي لنموذج حل إعداد التقارير الإلكترونية على الكمبيوتر المحلي وحفظه.</span><span class="sxs-lookup"><span data-stu-id="46642-133">Before you begin, you must also download and save the following configuration of the sample ER solution to your local computer.</span></span>

| <span data-ttu-id="46642-134">وصف المحتوى</span><span class="sxs-lookup"><span data-stu-id="46642-134">Content description</span></span>     | <span data-ttu-id="46642-135">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="46642-135">File name</span></span> |
|-------------------------|-----------|
| <span data-ttu-id="46642-136">تنسيق تكوين ER</span><span class="sxs-lookup"><span data-stu-id="46642-136">ER format configuration</span></span> | [<span data-ttu-id="46642-137">Format to learn deferred XML elements.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="46642-137">Format to learn deferred XML elements.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a><span data-ttu-id="46642-138">استيراد نموذج تكوينات إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="46642-138">Import the sample ER configurations</span></span>

1. <span data-ttu-id="46642-139">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="46642-139">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="46642-140">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="46642-140">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="46642-141">في صفحة **التكوينات**، في حالة عدم توفر تكوين **Model to learn deferred elements** في شجرة التكوين، استورد تكوين نموذج بيانات إعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="46642-141">On the **Configurations** page, if the **Model to learn deferred elements** configuration isn't available in the configuration tree, import the ER data model configuration:</span></span>

    1. <span data-ttu-id="46642-142">حدد **استبدال**، ثم حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="46642-142">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="46642-143">حدد **استعراض**، وابحث عن ملف **Model to learn deferred elements.1.xml** وحدده، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="46642-143">Select **Browse**, find and select the **Model to learn deferred elements.1.xml** file, and then select **OK**.</span></span>

4. <span data-ttu-id="46642-144">في حالة عدم توفر التكوين **تعيين للتعرف على العناصر المؤجلة** في شجرة التكوين، استورد تكوين تعيين نموذج إعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="46642-144">If the **Mapping to learn deferred elements** configuration isn't available in the configuration tree, import the ER model mapping configuration:</span></span>

    1. <span data-ttu-id="46642-145">حدد **استبدال**، ثم حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="46642-145">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="46642-146">حدد **استعراض**، وابحث عن ملف **تعيين للتعرف على العناصر المؤجلة.1.1.xml** وحدده، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="46642-146">Select **Browse**, find and select the **Mapping to learn deferred elements.1.1.xml** file, and then select **OK**.</span></span>

5. <span data-ttu-id="46642-147">استيراد تكوين تنسيق إعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="46642-147">Import the ER format configuration:</span></span>

    1. <span data-ttu-id="46642-148">حدد **استبدال**، ثم حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="46642-148">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="46642-149">حدد **استعراض**، وابحث عن الملف **Format to learn deferred XML elements.1.1.xml** وحدده، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="46642-149">Select **Browse**, find and select the **Format to learn deferred XML elements.1.1.xml** file, and then select **OK**.</span></span>

6. <span data-ttu-id="46642-150">في شجرة التكوين ، وسَّع **Model to learn deferred elements**.</span><span class="sxs-lookup"><span data-stu-id="46642-150">In the configuration tree, expand **Model to learn deferred elements**.</span></span>
7. <span data-ttu-id="46642-151">راجع قائمة تكوينات إعداد التقارير الإلكترونية المستوردة في شجرة التكوين.</span><span class="sxs-lookup"><span data-stu-id="46642-151">Review the list of imported ER configurations in the configuration tree.</span></span>

    ![تكوينات إعداد التقارير الإلكترونية المستوردة على صفحة التكوينات](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a><span data-ttu-id="46642-153">تنشيط موفر تكوين</span><span class="sxs-lookup"><span data-stu-id="46642-153">Activate a configuration provider</span></span>

1. <span data-ttu-id="46642-154">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="46642-154">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="46642-155">في صفحة **ترجمة التكوينات**، في قسم **موفري التكوين**، تحقق من إدراج [ موفر التكوين ](general-electronic-reporting.md#Provider) لنموذج الشركة Litware, Inc (`http://www.litware.com`) ووضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="46642-155">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the [configuration provider](general-electronic-reporting.md#Provider) for the Litware, Inc. (`http://www.litware.com`) sample company is listed, and that it's marked as active.</span></span> <span data-ttu-id="46642-156">في حالة عدم إدراج موفر التكوين، أو عدم وضع علامة عليه كنشط، اتبع الخطوات الموجودة في الموضوع [إنشاء موفر تكوين ووضع علامة عليه على أنه نشط.](./tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="46642-156">If this configuration provider isn't listed, or if it isn't marked as active, follow the steps in the [Create a configuration provider and mark it as active](./tasks/er-configuration-provider-mark-it-active-2016-11.md) topic.</span></span>

    ![نموذج شركة Litware, Inc. في صفحة تكوينات الترجمة](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a><span data-ttu-id="46642-158">مراجعة تعيين النموذج المستورد</span><span class="sxs-lookup"><span data-stu-id="46642-158">Review the imported model mapping</span></span>

<span data-ttu-id="46642-159">راجع إعدادات مكون تعيين نموذج إعداد التقارير الإلكترونية الذي تم تكوينه للوصول إلى حركات الضريبة وعرض البيانات التي يتم الوصول اليها عند الطلب.</span><span class="sxs-lookup"><span data-stu-id="46642-159">Review the settings of the ER model mapping component that is configured to access tax transactions and expose accessed data on request.</span></span>

1. <span data-ttu-id="46642-160">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="46642-160">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="46642-161">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="46642-161">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="46642-162">في صفحة **التكوينات**، في شجرة التكوينات، وسَّع **Model to learn deferred elements**.</span><span class="sxs-lookup"><span data-stu-id="46642-162">On the **Configurations** page, in the configuration tree, expand **Model to learn deferred elements**.</span></span>
4. <span data-ttu-id="46642-163">حدد التكوين **Mapping to learn deferred elements**.</span><span class="sxs-lookup"><span data-stu-id="46642-163">Select the **Mapping to learn deferred elements** configuration.</span></span>
5. <span data-ttu-id="46642-164">حدد **المصمم** لفتح قائمة التعيينات.</span><span class="sxs-lookup"><span data-stu-id="46642-164">Select **Designer** to open the list of mappings.</span></span>
6. <span data-ttu-id="46642-165">حدد **المصمم** لمراجعة تفاصيل التعيين.</span><span class="sxs-lookup"><span data-stu-id="46642-165">Select **Designer** to review the mapping details.</span></span>
7. <span data-ttu-id="46642-166">حدد **إظهار التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="46642-166">Select **Show details**.</span></span>
8. <span data-ttu-id="46642-167">مراجعة مصادر البيانات التي يتم تكوينها للوصول إلى حركات الضريبة:</span><span class="sxs-lookup"><span data-stu-id="46642-167">Review the data sources that are configured to access tax transactions:</span></span>

    - <span data-ttu-id="46642-168">يتم تكوين مصدر بيانات **الحركات** لنوع *سجل الجدول* للوصول إلى جدول التطبيقات **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="46642-168">The **Transactions** data source of the *Table record* type is configured to access records of the **TaxTrans** application table.</span></span>
    - <span data-ttu-id="46642-169">يتم تكون مصدر بيانات **الإيصالات‬** لنوع *الحقل المحسوب* لإرجاع أكواد الإيصالات المطلوبة (**INV-10000349** و**INV-10000350**) كقائمة سجلات.</span><span class="sxs-lookup"><span data-stu-id="46642-169">The **Vouchers** data source of the *Calculated field* type is configured to return the required voucher codes (**INV-10000349** and **INV-10000350**) as a list of records.</span></span>
    - <span data-ttu-id="46642-170">كما يتم تكوين مصدر البيانات **التي تمت تصفيتها** لنوع *الحقل المحسوب* للتحديد، من مصدر بيانات **الحركات**، الحركات الضريبية للإيصالات المطلوبة فقط.</span><span class="sxs-lookup"><span data-stu-id="46642-170">The **Filtered** data source of the *Calculated field* type is configured to select, from the **Transactions** data source, only tax transactions of the required vouchers.</span></span>
    - <span data-ttu-id="46642-171">يتم إضافة الحقل **\$TaxAmoun** لنوع *الحقل المحسوب* لمصدر البيانات **التي تمت تصفيتها** لعرض قيمه الضريبة ذات العلامة المعاكسة.</span><span class="sxs-lookup"><span data-stu-id="46642-171">The **\$TaxAmount** field of the *Calculated field* type is added for the **Filtered** data source to expose the tax value that has the opposite sign.</span></span>
    - <span data-ttu-id="46642-172">يتم تكوين مصدر البيانات **المجمعة** للنوع *التجميع حسب* لتجميع حركات الضريبة المصفاة لمصدر البيانات **التي تمت تصفيتها**.</span><span class="sxs-lookup"><span data-stu-id="46642-172">The **Grouped** data source of the *Group By* type is configured to group filtered tax transactions of the **Filtered** data source.</span></span>
    - <span data-ttu-id="46642-173">يتم تكوين حقل التجميع **TotalSum** لمصدر البيانات **المجمعة** لتلخيص قيم الحقل **\$TaxAmount** لمصدر البيانات **التي تمت تصفيتها** لكافة حركات الضرائب المصفاة لمصدر البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="46642-173">The **TotalSum** aggregation field of the **Grouped** data source is configured to summarize values of the **\$TaxAmount** field of the **Filtered** data source for all filtered tax transactions of that data source.</span></span>

        ![حقل التجميع TotalSum في صفحة تحرير معلمات 'GroupBy'](./media/ER-DeferredXml-GroupByParameters.png)

9. <span data-ttu-id="46642-175">راجع كيفية ربط مصادر البيانات التي تم تكوينها بنموذج البيانات، وكيفية عرضها للبيانات التي يتم الوصول إليها لتوفيرها في تنسيق إعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="46642-175">Review how the configured data sources are bound to the data model, and how they expose accessed data to make it available in an ER format:</span></span>

    - <span data-ttu-id="46642-176">يتم ربط مصدر البيانات **التي تمت تصفيتها** بحقل نموذج البيانات **Data.List**.</span><span class="sxs-lookup"><span data-stu-id="46642-176">The **Filtered** data source is bound to the **Data.List** field of the data model.</span></span>
    - <span data-ttu-id="46642-177">يتم ربط الحقل **\$TaxAmount** بمصدر البيانات **التي تمت تصفيتها** بحقل نموذج البيانات **Data.List.Value**.</span><span class="sxs-lookup"><span data-stu-id="46642-177">The **\$TaxAmount** field of the **Filtered** data source is bound to the **Data.List.Value** field of the data model.</span></span>
    - <span data-ttu-id="46642-178">يتم ربط الحقل **TotalSum** الخاص بمصدر البيانات **المجمعة** بحقل نموذج البيانات **Data.Summary.Total**.</span><span class="sxs-lookup"><span data-stu-id="46642-178">The **TotalSum** field of the **Grouped** data source is bound to the **Data.Summary.Total** field of the data model.</span></span>

    ![صفحة مصمم تعيين النموذج](./media/ER-DeferredXml-ModelMapping.png)

10. <span data-ttu-id="46642-180">اغلق صفحات **مصمم تعيين النموذج** و**تعيينات النماذج**.</span><span class="sxs-lookup"><span data-stu-id="46642-180">Close the **Model mapping designer** and **Model mappings** pages.</span></span>

### <a name="review-the-imported-format"></a><span data-ttu-id="46642-181">مراجعة التنسيق المستورد</span><span class="sxs-lookup"><span data-stu-id="46642-181">Review the imported format</span></span>

1. <span data-ttu-id="46642-182">في صفحة **التكوينات**، في شجرة التكوين، حدد التكوين**التنسيق للتعرف على عناصر XML المؤجلة**.</span><span class="sxs-lookup"><span data-stu-id="46642-182">On the **Configurations** page, in the configuration tree, select the **Format to learn deferred XML elements** configuration.</span></span>
2. <span data-ttu-id="46642-183">حدد **المصمم** لمراجعة تفاصيل التنسيق.</span><span class="sxs-lookup"><span data-stu-id="46642-183">Select **Designer** to review the format details.</span></span>
3. <span data-ttu-id="46642-184">حدد **إظهار التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="46642-184">Select **Show details**.</span></span>
4. <span data-ttu-id="46642-185">راجع إعدادات مكونات تنسيق إعداد التقارير الإلكترونية التي تم تكوينها لإنشاء مستند صادر بتنسيق XML يتضمن تفاصيل الحركات الضريبية:</span><span class="sxs-lookup"><span data-stu-id="46642-185">Review the settings of the ER format components that are configured to generate an outbound document in XML format that includes details of the tax transactions:</span></span>

    - <span data-ttu-id="46642-186">تم تكوين عنصر XML **التقرير\\الرسالة** لملء المستند الصادر بعقده مفردة تتضمن عناصر XML المتداخلة (**الرأس** و**السجل** و**الملخص**).</span><span class="sxs-lookup"><span data-stu-id="46642-186">The **Report\\Message** XML element is configured to fill the outbound document with a single node that includes the nested XML elements (**Header**, **Record**, and **Summary**).</span></span>
    - <span data-ttu-id="46642-187">يتم تكوين عنصر XML **التقرير\\الرسالة\\الرأس** لملء المستند الصادر بعقدة رأس واحدة لعرض التاريخ والوقت عند بدء المعالجة.</span><span class="sxs-lookup"><span data-stu-id="46642-187">The **Report\\Message\\Header** XML element is configured to fill the outbound document with a single header node that shows the date and time when the processing starts.</span></span>
    - <span data-ttu-id="46642-188">يتم تكوين عنصر تنسيق XML **التقرير \\الرسالة\\السجل** لملء المستند الصادر بعقدة سجل واحدة لعرض تفاصيل حركة ضريبية واحدة.</span><span class="sxs-lookup"><span data-stu-id="46642-188">The **Report \\Message\\Record** XML element is configured to fill the outbound document with a single record node that shows the details of a single tax transaction.</span></span>
    - <span data-ttu-id="46642-189">يتم تكوين عنصر تنسيق XML **التقرير\\الرسالة\\الملخص** لملء المستند الصادر بعقدة ملخص واحدة تتضمن مجموع قيم الضريبة من الحركات الضريبية التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="46642-189">The **Report\\Message\\Summary** XML element is configured to fill the outbound document with a single summary node that includes the sum of the tax values from the processed tax transactions.</span></span>

    ![عنصر XML للرسالة وعناصر XML المتداخلة في صفحة مصمم التنسيق](./media/ER-DeferredXml-Format.png)

5. <span data-ttu-id="46642-191">في علامة التبويب **تعيين**، راجع التفاصيل التالية:</span><span class="sxs-lookup"><span data-stu-id="46642-191">On the **Mapping** tab, review the following details:</span></span>

    - <span data-ttu-id="46642-192">ليس من الضروري ربط عنصر **التقرير\\الرسالة\\الرأس** بمصدر لإنشاء عقدة واحدة في مستند صادر.</span><span class="sxs-lookup"><span data-stu-id="46642-192">The **Report\\Message\\Header** element doesn't have to be bound to a source to generate a single node in an outbound document.</span></span>
    - <span data-ttu-id="46642-193">تنشئ السمة **ExecutionDateTime** التاريخ والوقت (بما في ذلك المللي ثوانس) عند إضافة عقدة رأس.</span><span class="sxs-lookup"><span data-stu-id="46642-193">The **ExecutionDateTime** attribute generates the date and time (including milliseconds) when the header node is added.</span></span>
    - <span data-ttu-id="46642-194">يتم ربط عنصر **التقرير\\الرسالة\\ السجل** بقائمة **model.Data.List** لإنشاء عقدة سجل واحدة لكل سجل من القائمة المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="46642-194">The **Report\\Message\\Record** element is bound to the **model.Data.List** list to generate a single record node for every record from the bound list.</span></span>
    - <span data-ttu-id="46642-195">ترتبط السمة **TaxAmount** بـ **model.Data.List.Value** (التي تظهر كـ **\@.قيمة** في عرض المسار النسبي) لإنشاء قيمة الضريبة لحركة الضريبة الحالية.</span><span class="sxs-lookup"><span data-stu-id="46642-195">The **TaxAmount** attribute is bound to **model.Data.List.Value** (which is shown as **\@.Value** in the relative path view) to generate the tax value of the current tax transaction.</span></span>
    - <span data-ttu-id="46642-196">تعد **RunningTotal** سمة نائبة للإجمالي الحالي لقيم الضريبة.</span><span class="sxs-lookup"><span data-stu-id="46642-196">The **RunningTotal** attribute is a placeholder for the running total of the tax values.</span></span> <span data-ttu-id="46642-197">لا تحتوي هذه السمة على مخرجات في الوقت الحالي، نظرًا لعدم تكوين ربط أو قيمة افتراضية لها.</span><span class="sxs-lookup"><span data-stu-id="46642-197">Currently, this attribute has no output, because neither a binding nor a default value is configured for it.</span></span>
    - <span data-ttu-id="46642-198">تنشئ السمة **ExecutionDateTime** التاريخ والوقت (بما في ذلك المللي ثوانٍ) عند معالجة الحركة الحالية في هذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="46642-198">The **ExecutionDateTime** attribute generates the date and time (including milliseconds) when the current transaction is processed in this report.</span></span>
    - <span data-ttu-id="46642-199">ليس من الضروري ربط عنصر **التقرير\\الرسالة\\الملخص** بمصدر بيانات لإنشاء عقدة واحدة في مستند صادر.</span><span class="sxs-lookup"><span data-stu-id="46642-199">The **Report\\Message\\Summary** element doesn't have to be bound to a data source to generate a single node in an outbound document.</span></span>
    - <span data-ttu-id="46642-200">ترتبط السمة **TotalTaxAmount** بـ **model.Data.Summary.Total** لإنشاء مجموع قيم الضريبة لحركات الضريبة التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="46642-200">The **TotalTaxAmount** attribute is bound to **model.Data.Summary.Total** to generate the sum of the tax values of the processed tax transactions.</span></span>
    - <span data-ttu-id="46642-201">تنشئ السمة **ExecutionDateTime** التاريخ والوقت (بما في ذلك المللي ثوانس) عند إضافة عقدة الملخص.</span><span class="sxs-lookup"><span data-stu-id="46642-201">The **ExecutionDateTime** attribute generates the date and time (including milliseconds) when the summary node is added.</span></span>

    ![علامة التبويب التعيين في صفحة مصمم التنسيق](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a><span data-ttu-id="46642-203">تشغيل التقارير الإلكترونية المستوردة</span><span class="sxs-lookup"><span data-stu-id="46642-203">Run the imported format</span></span>

1. <span data-ttu-id="46642-204">في صفحة **مصمم التنسيق**، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="46642-204">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="46642-205">نزِّل الملف الذي يعرضه مستعرض الويب وافتحه للمراجعة.</span><span class="sxs-lookup"><span data-stu-id="46642-205">Download the file that the web browser offers, and open it for review.</span></span>

    ![الملف المنزَّل](./media/ER-DeferredXml-Run.png)

<span data-ttu-id="46642-207">لاحظ أن عقدة الملخص تعرض مجموع قيم الضريبة للحركات التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="46642-207">Notice that the summary node presents the sum of the tax values for the processed transactions.</span></span> <span data-ttu-id="46642-208">نظرًا لتكوين التنسيق لاستخدام الربط **model.Data.Summary.Total** لإرجاع هذا المجموع، يتم حساب المجموع باستدعاء تجميع **TotalSum** لمصدر البيانات **المجمعة** للنوع *GroupBy* في تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="46642-208">Because the format is configured to use the **model.Data.Summary.Total** binding to return this sum, the sum is calculated by calling the **TotalSum** aggregation of the **Grouped** data source of the *GroupBy* type in the model mapping.</span></span> <span data-ttu-id="46642-209">لحساب هذا التجميع، يتكرر تعيين النموذج في كافة الحركات التي تم تحديدها في مصدر البيانات **التي تمت تصفيتها**.</span><span class="sxs-lookup"><span data-stu-id="46642-209">To calculate this aggregation, the model mapping iterates over all transactions that have been selected in the **Filtered** data source.</span></span> <span data-ttu-id="46642-210">وبمقارنة أوقات تنفيذ عقدة الملخص وعقدة السجل الأخير، يمكنك تحديد استغراق عملية حساب المجموع 12 مللي ثانية.</span><span class="sxs-lookup"><span data-stu-id="46642-210">By comparing the execution times of the summary node and the last record node, you can determine that calculation of the sum took 12 milliseconds (ms).</span></span> <span data-ttu-id="46642-211">وبمقارنة أوقات تنفيذ عقدتا السجل الأول والسجل الأخير، يمكنك تحديد استغراق عملية إنشاء كل عقد السجلات 9 مللي ثانية.</span><span class="sxs-lookup"><span data-stu-id="46642-211">By comparing the execution times of the first and last record nodes, you can determine that generation of all record nodes took 9 ms.</span></span> <span data-ttu-id="46642-212">لذا كان إجمالي الوقت المطلوب هو 21 مللي ثانية.</span><span class="sxs-lookup"><span data-stu-id="46642-212">Therefore, a total of 21 ms was required.</span></span>

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a><span data-ttu-id="46642-213">تعديل التنسيق بحيث يعتمد الحساب على المخرجات المنشأة</span><span class="sxs-lookup"><span data-stu-id="46642-213">Modify the format so that the calculation is based on generated output</span></span>

<span data-ttu-id="46642-214">إذا كان حجم الحركة أكبر بكثير من الحجم في المثال الحالي، فقد يزيد وقت الحساب ويسبب مشاكل في الأداء.</span><span class="sxs-lookup"><span data-stu-id="46642-214">If the volume of transaction is much larger than the volume in the current example, the calculation time might increase and cause performance issues.</span></span> <span data-ttu-id="46642-215">ومن خلال تغيير إعداد التنسيق، يمكنك المساعدة في تجنب مشكلات الأداء هذه.</span><span class="sxs-lookup"><span data-stu-id="46642-215">By changing the setting of the format, you can help prevent these performance issues.</span></span> <span data-ttu-id="46642-216">ونظرًا لوصولك إلى قيم الضريبة لتضمينها في التقرير الذي يتم إنشاؤه، يمكنك إعادة استخدام هذه المعلومات لحساب قيم الضريبة.</span><span class="sxs-lookup"><span data-stu-id="46642-216">Because you access tax values to include them in the generated report, you can reuse this information to calculate tax values.</span></span> <span data-ttu-id="46642-217">لمزيد من المعلومات، راجع [تكوين التنسيق لتنفيذ عمليات الجرد والتجميع‬](./tasks/er-format-counting-summing-1.md).</span><span class="sxs-lookup"><span data-stu-id="46642-217">For more information, see [Configure format to do counting and summing](./tasks/er-format-counting-summing-1.md).</span></span>

1. <span data-ttu-id="46642-218">في صفحة **مصمم التنسيق**، وفي علامة التبويب **التنسيق**، حدد عنصر ملف **التقرير** في شجرة التنسيق.</span><span class="sxs-lookup"><span data-stu-id="46642-218">On the **Format designer** page, on the **Format** tab, select the **Report** file element in the format tree.</span></span>
2. <span data-ttu-id="46642-219">عيّن الخيار **تجميع تفاصيل المخرجات** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="46642-219">Set the **Collect output details** option to **Yes**.</span></span> <span data-ttu-id="46642-220">يمكنك الآن تكوين هذا التنسيق باستخدام محتوى تقرير تم إنشاؤه كمصدر بيانات يمكن الوصول إليه باستخدام وظائف إعداد التقارير الإلكترونية المضمنة في فئة [تجميع البيانات](er-functions-category-data-collection.md).</span><span class="sxs-lookup"><span data-stu-id="46642-220">You can now configure this format by using the content of a generated report as a data source that can be accessed by using the built-in ER functions in the [Data collection](er-functions-category-data-collection.md) category.</span></span>
3. <span data-ttu-id="46642-221">في علامة التبويب **التعيين**، حدد  عنصر XML **التقرير\\الرسالة\\السجل**.</span><span class="sxs-lookup"><span data-stu-id="46642-221">On the **Mapping** tab, select the **Report\\Message\\Record** XML element.</span></span>
4. <span data-ttu-id="46642-222">كوِّن تعبير **اسم مفتاح البيانات المجمعة** ليكون `WsColumn`.</span><span class="sxs-lookup"><span data-stu-id="46642-222">Configure the **Collected data key name** expression as `WsColumn`.</span></span>
5. <span data-ttu-id="46642-223">كوِّن تعبير **قيمة مفتاح البيانات المجمعة** ليكون `WsRow`.</span><span class="sxs-lookup"><span data-stu-id="46642-223">Configure the **Collected data key value** expression as `WsRow`.</span></span>

    ![عنصر XML السجل في صفحة مصمم التنسيق](./media/ER-DeferredXml-Format3.png)

6. <span data-ttu-id="46642-225">حدد سمة **التقرير\\الرسالة\\السجل\\TaxAmount**.</span><span class="sxs-lookup"><span data-stu-id="46642-225">Select the **Report\\Message\\Record\\TaxAmount** attribute.</span></span>
7. <span data-ttu-id="46642-226">كوِّن تعبير **اسم مفتاح البيانات المجمعة** ليكون `SummingAmountKey`.</span><span class="sxs-lookup"><span data-stu-id="46642-226">Configure the **Collected data key name** expression as `SummingAmountKey`.</span></span>

    ![سمة TaxAmount في صفحة مصمم التنسيق](./media/ER-DeferredXml-Format4.png)

    <span data-ttu-id="46642-228">ويمكنك اعتبار هذا الإعداد بمثابة تنفيذ ورقة عمل ظاهرية، حيث يتم إلحاق قيمة خلية A1 بقيمة مبلغ الضريبة من كل حركة ضريبية تتم معالجتها.</span><span class="sxs-lookup"><span data-stu-id="46642-228">You can consider this setting the fulfillment of a virtual worksheet, where the value of cell A1 is appended with the value of the tax amount from every processed tax transaction.</span></span>

8. <span data-ttu-id="46642-229">حدد سمة **التقرير\\الرسالة\\السجل\\RunningTotal**، ثم حدد **تحرير المعادلة‬**.</span><span class="sxs-lookup"><span data-stu-id="46642-229">Select the **Report\\Message\\Record\\RunningTotal** attribute, and then select **Edit formula**.</span></span>
9. <span data-ttu-id="46642-230">كوِّن التعبير `SUMIF(SummingAmountKey, WsColumn, WsRow)` باستخدام وظيفة إعداد التقارير الإلكترونية [SUMIF](er-functions-datacollection-sumif.md) المضمنة، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="46642-230">Configure the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression by using the built-in [SUMIF](er-functions-datacollection-sumif.md) ER function, and then select **Save**.</span></span>

    ![تعبير SUMIF](./media/ER-DeferredXml-FormulaDesigner.png)

10. <span data-ttu-id="46642-232">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="46642-232">Close the **Formula designer** page.</span></span>
11. <span data-ttu-id="46642-233">حدد **حفظ**، ثم حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="46642-233">Select **Save**, and then select **Run**.</span></span>
12. <span data-ttu-id="46642-234">نزِّل الملف الذي يعرضه مستعرض الويب وراجعه.</span><span class="sxs-lookup"><span data-stu-id="46642-234">Download and review the file that the web browser offers.</span></span>

    ![الملف المنزَّل](./media/ER-DeferredXml-Run1.png)

    <span data-ttu-id="46642-236">تحتوي عقدة السجل الأخير على الإجمالي الحالي لقيم الضريبة التي يتم حسابها لكافة الحركات التي تمت معالجتها باستخدام المخرجات المنشأة كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="46642-236">The last record node contains the running total of tax values that is calculated for all processed transactions by using the generated output as a data source.</span></span> <span data-ttu-id="46642-237">يبدأ مصدر البيانات هذا من بداية التقرير ويستمر خلال حركة الضريبة الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="46642-237">This data source starts from the beginning of the report and continues through the last tax transaction.</span></span> <span data-ttu-id="46642-238">تحتوي عقدة الملخص على مجموع قيم الضريبة لكافة الحركات التي تمت معالجتها والتي يتم حسابها في تعيين النموذج باستخدام مصدر بيانات النوع *GroupBy*.</span><span class="sxs-lookup"><span data-stu-id="46642-238">The summary node contains the sum of the tax values for all processed transactions that are calculated in the model mapping by using the data source of the *GroupBy* type.</span></span> <span data-ttu-id="46642-239">لاحظ أن هذه القيم متساوية.</span><span class="sxs-lookup"><span data-stu-id="46642-239">Notice that these values are equal.</span></span> <span data-ttu-id="46642-240">لذا يمكن استخدام التجميع المبني على المخرجات بدلاً من **GroupBy**.</span><span class="sxs-lookup"><span data-stu-id="46642-240">Therefore, the output-based summing can be used instead of **GroupBy**.</span></span> <span data-ttu-id="46642-241">وبمقارنة أوقات تنفيذ عقدة السجل الأول وعقدة الملخص، يمكنك تحديد استغراق عملية إنشاء كل عقد السجلات والجمع 11 مللي ثانية.</span><span class="sxs-lookup"><span data-stu-id="46642-241">By comparing the execution times of the first record node and the summary node, you can determine that generation of all the record nodes and summing took 11 ms.</span></span> <span data-ttu-id="46642-242">لذا فيما يتعلق بإنشاء عقد السجلات وجمع قيم الضريبة، فإن التنسيق المعدل يكون أسرع مرتين تقريبًا من التنسيق الأصلي.</span><span class="sxs-lookup"><span data-stu-id="46642-242">Therefore, as far as the generation of record nodes and the summing of tax values are concerned, the modified format is approximately two times faster than the original format.</span></span>

13. <span data-ttu-id="46642-243">حدد سمة **التقرير\\الرسالة\\الملخص\\RunningTotal**، ثم حدد **تحرير المعادلة‬**.</span><span class="sxs-lookup"><span data-stu-id="46642-243">Select the **Report\\Message\\Summary\\TotalTaxAmount** attribute, and then select **Edit formula**.</span></span>
14. <span data-ttu-id="46642-244">أدخل التعبير `SUMIF(SummingAmountKey, WsColumn, WsRow)` بدلاً من التعبير الموجود.</span><span class="sxs-lookup"><span data-stu-id="46642-244">Enter the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression instead of the existing expression.</span></span>
15. <span data-ttu-id="46642-245">حدد **حفظ**، ثم حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="46642-245">Select **Save**, and then select **Run**.</span></span>
16. <span data-ttu-id="46642-246">نزِّل الملف الذي يعرضه مستعرض الويب وراجعه.</span><span class="sxs-lookup"><span data-stu-id="46642-246">Download and review the file that the web browser offers.</span></span>

    ![الملف المنزَّل](./media/ER-DeferredXml-Run2.png)

    <span data-ttu-id="46642-248">لاحظ أن الإجمالي الحالي لقيم الضريبة في عقدة السجل الأخير يساوي الآن المجموع في عقدة الملخص.</span><span class="sxs-lookup"><span data-stu-id="46642-248">Notice that the running total of tax values in the last record node now equals the sum in the summary node.</span></span>

### <a name="put-values-of-output-based-summing-in-the-report-header"></a><span data-ttu-id="46642-249">وضع قيم التجميع المبني على المخرجات في رأس التقرير</span><span class="sxs-lookup"><span data-stu-id="46642-249">Put values of output-based summing in the report header</span></span>

<span data-ttu-id="46642-250">،إذا كان من الضروري على سبيل المثال تقديم مجموع قيم الضرائب في رأس التقرير، يمكنك تعديل التنسيق لديك.</span><span class="sxs-lookup"><span data-stu-id="46642-250">If, for example, you must present the sum of tax values in the header of your report, you can modify your format.</span></span>

1. <span data-ttu-id="46642-251">في صفحة  **مصمم التنسيق**، وفي علامة التبويب **التنسيق**، حدد عنصر XML **التقرير\\الرسالة\\الملخص**.</span><span class="sxs-lookup"><span data-stu-id="46642-251">On the **Format designer** page, on the **Format** tab, select the **Report\\Message\\Summary** XML element.</span></span>
2. <span data-ttu-id="46642-252">حدد **تحريك لأعلى**.</span><span class="sxs-lookup"><span data-stu-id="46642-252">Select **Move up**.</span></span>
3. <span data-ttu-id="46642-253">حدد **حفظ**، ثم حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="46642-253">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="46642-254">نزِّل الملف الذي يعرضه مستعرض الويب وراجعه.</span><span class="sxs-lookup"><span data-stu-id="46642-254">Download and review the file that the web browser offers.</span></span>

    ![الملف المنزَّل](./media/ER-DeferredXml-Run3.png)

    <span data-ttu-id="46642-256">لاحظ أن مجموع قيم الضريبة في عقدة الملخص يساوي الآن 0 (صفر)، لأن هذا المجموع يتم حسابه الآن استنادًا إلى المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="46642-256">Notice that the sum of tax values in the summary node now equals 0 (zero), because this sum is now calculated based on the generated output.</span></span> <span data-ttu-id="46642-257">عند إنشاء عقدة السجل الأول، لن تحتوي المخرجات المنشأة حينها على عقدالسجلات التي تحتوي على تفاصيل الحركة.</span><span class="sxs-lookup"><span data-stu-id="46642-257">When the first record node is generated, the generated output doesn't yet contain record nodes that have transaction details.</span></span> <span data-ttu-id="46642-258">يمكنك تكوين هذا التنسيق لتأجيل تنفيذ عنصر **التقرير\\الرسالة\\الملخص** حتى يتم تشغيل عنصر **التقرير\\الرسالة\\السجل** لكل الحركات الضريبية.</span><span class="sxs-lookup"><span data-stu-id="46642-258">You can configure this format to defer the execution of the **Report\\Message\\Summary** element until the **Report\\Message\\Record** element has been run for all tax transactions.</span></span>

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a><span data-ttu-id="46642-259">تأجيل تنفيذ عنصر XML الملخص حتى يتم استخدام الإجمالي المحسوب</span><span class="sxs-lookup"><span data-stu-id="46642-259">Defer the execution of the summary XML element so that the calculated total is used</span></span>

1. <span data-ttu-id="46642-260">في صفحة  **مصمم التنسيق**، وفي علامة التبويب **التنسيق**، حدد عنصر XML **التقرير\\الرسالة\\الملخص**.</span><span class="sxs-lookup"><span data-stu-id="46642-260">On the **Format designer** page, on the **Format** tab, select the **Report\\Message\\Summary** XML element.</span></span>
2. <span data-ttu-id="46642-261">عيّن الخيار **التنفيذ المؤجل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="46642-261">Set the **Deferred execution** option to **Yes**.</span></span>

    ![خيار التنفيذ المؤجل لعنصر XML الملخص في صفحة مصمم التنسيق](./media/ER-DeferredXml-Format5.png)

3. <span data-ttu-id="46642-263">حدد **حفظ**، ثم حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="46642-263">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="46642-264">نزِّل الملف الذي يعرضه مستعرض الويب وراجعه.</span><span class="sxs-lookup"><span data-stu-id="46642-264">Download and review the file that the web browser offers.</span></span>

    ![الملف المنزَّل](./media/ER-DeferredXml-Run4.png)

    <span data-ttu-id="46642-266">يتم الآن تشغيل عنصر **التقرير\\الرسالة \\الملخص** فقط بعد تشغيل كافة العناصر الأخرى التي تم إدراجها ضمن العنصر الأصلي **التقرير\\الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="46642-266">The **Report\\Message\\Summary** element is now run only after all other items that are nested under its parent element, **Report\\Message**, have been run.</span></span> <span data-ttu-id="46642-267">لذا يتم تشغيله بعد تشغيل عنصر **التقرير\\الرسالة \\السجل** لكل الحركات الضريبية لمصدر البيانات **model.Data.List**.</span><span class="sxs-lookup"><span data-stu-id="46642-267">Therefore, it's run after the **Report\\Message\\Record** element has been run for all tax transactions of the **model.Data.List** data source.</span></span> <span data-ttu-id="46642-268">توضح أوقات تنفيذ عقد السجل الأول والأخير وعقد الرأس والملخص هذه الحقيقة.</span><span class="sxs-lookup"><span data-stu-id="46642-268">The execution times of the first and last record nodes, and of the header and summary nodes, reveal this fact.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46642-269">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="46642-269">Additional resources</span></span>

- [<span data-ttu-id="46642-270">تكوين التنسيق لتنفيذ عمليات الجرد والتجميع</span><span class="sxs-lookup"><span data-stu-id="46642-270">Configure format to do counting and summing</span></span>](./tasks/er-format-counting-summing-1.md)
- [<span data-ttu-id="46642-271">تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="46642-271">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="46642-272">تأجيل تنفيذ عناصر التسلسل في تنسيقات إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="46642-272">Defer the execution of sequence elements in ER formats</span></span>](er-defer-sequence-element.md#Example)
