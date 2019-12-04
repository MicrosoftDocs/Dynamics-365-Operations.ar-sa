---
title: تحديد موقع تخزين مخصص للمستندات التي يتم إنشاؤها
description: يشرح هذا الموضوع كيفية توسيع قائمة مواقع التخزين للمستندات التي تقوم تنسيقات التقارير الإلكترونية بإنشائها.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2c7ee610c6e3c446a4bcc9d6d46ca72dd71cb23c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771388"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="5b5ab-103">تحديد موقع تخزين مخصص للمستندات التي يتم إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="5b5ab-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5b5ab-104">تسمح لك واجهة برمجة التطبيقات (API) لإطار عمل التقارير الإلكترونية بتوسيع قائمة مواقع التخزين التي تقوم تنسيقات التقارير الإلكترونية بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="5b5ab-105">يتضمن هذا الموضوع نظرة عامة حول المهام الأساسية التي يجب إكمالها لإضافة موقع تخزين مخصص.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5b5ab-106">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="5b5ab-106">Prerequisites</span></span>

<span data-ttu-id="5b5ab-107">يجب نشر مخطط يدعم البناء المستمر.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="5b5ab-108">(لمزيد من المعلومات، راجع [نشر مخططات تدعم البناء المستمر والتنفيذ التلقائي للاختبار‬ات‬](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) يجب أن يكون لديك حق الوصول إلى هذا المخطط لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="5b5ab-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="5b5ab-109">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="5b5ab-109">Electronic reporting developer</span></span>
- <span data-ttu-id="5b5ab-110">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="5b5ab-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="5b5ab-111">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="5b5ab-111">System administrator</span></span>

<span data-ttu-id="5b5ab-112">يجب أن يكون لديك أيضًأ حق الوصول إلى بيئة التطوير لهذا المخطط.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-112">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="5b5ab-113">إنشاء تكوين تنسيق التقارير الإلكترونية أو استيراده</span><span class="sxs-lookup"><span data-stu-id="5b5ab-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="5b5ab-114">في المخطط الحالي، يمكنك [إنشاء تنسيق تقارير إلكترونية جديد](tasks/er-format-configuration-2016-11.md) لإنشاء المستندات التي تخطط لإضافتها إلى موقع التخزين المخصص.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-114">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="5b5ab-115">بدلاً من ذلك، يمكنك [استيراد تنسيق تقارير إلكترونية موجود إلى هذا المخطط](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="5b5ab-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![صفحة مصمم التنسيق‬](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="5b5ab-117">يجب أن يحتوي تنسيق التقارير الإلكترونية الذي تقوم بإنشائه أو استيراده على عنصر واحد على الأقل من عناصر التنسيق التالية:</span><span class="sxs-lookup"><span data-stu-id="5b5ab-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="5b5ab-118">ملف</span><span class="sxs-lookup"><span data-stu-id="5b5ab-118">File</span></span>
> - <span data-ttu-id="5b5ab-119">المجلد</span><span class="sxs-lookup"><span data-stu-id="5b5ab-119">Folder</span></span>
> - <span data-ttu-id="5b5ab-120">دمج</span><span class="sxs-lookup"><span data-stu-id="5b5ab-120">Merger</span></span>
> - <span data-ttu-id="5b5ab-121">مرفق</span><span class="sxs-lookup"><span data-stu-id="5b5ab-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="5b5ab-122">إنشاء نوع مستند جديد</span><span class="sxs-lookup"><span data-stu-id="5b5ab-122">Create a new document type</span></span>

<span data-ttu-id="5b5ab-123">لتحديد كيفية توجيه المستندات التي يقوم تنسيق التقارير الإلكترونية بإنشائها، يجب تكوين [وجهات التقارير الإلكترونية (ER)](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="5b5ab-123">To specify how documents that an ER format generates are routed, you must configure [Electronic reporting (ER) destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="5b5ab-124">في كل وجهة تقارير إلكترونية تم تكوينها لتخزين المستندات المنشأة كملفات، يجب تحديد نوع مستند من إطار عمل إدارة المستندات.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="5b5ab-125">ويمكن استخدام أنواع مستندات مختلفة لتوجيه المستندات التي تقوم تنسيقات تقارير إلكتروني مختلفة بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="5b5ab-126">أضف [نوع مستند](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) جديدًا لتنسيق التقارير الإلكترونية الذي أنشأته أو استوردته في خطوة سابقة.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-126">Add a new [document type](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="5b5ab-127">في الرسم التوضيحي الذي يلي، نوع المستند هو **FileX**.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="5b5ab-128">لتمييز نوع المستند هذا عن أنواع المستندات أخرى، يمكنك تضمين كلمة أساسية معينة في اسمه.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="5b5ab-129">على سبيل المثال، في الرسم التوضيحي الذي يلي، الاسم هو **المجلد (LOCAL)**.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="5b5ab-130">في حقل **الفئة**، حدد **إرفاق ملف**.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="5b5ab-131">في حقل **المجموعة**، حدد **ملف**.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-131">In the **Group** field, specify **File**.</span></span>

![صفحة أنواع المستندات](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="5b5ab-133">تتعلق أنواع المستندات بالشركة.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-133">Document types are company-specific.</span></span> <span data-ttu-id="5b5ab-134">لاستخدام تنسيق تقارير إلكترونية مع وجهة مكوّنة في شركات متعددة، يجب تكوين نوع مستند منفصل في كل شركة.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="5b5ab-135">مراجعة التعليمات البرمجية المصدر</span><span class="sxs-lookup"><span data-stu-id="5b5ab-135">Review source code</span></span>

<span data-ttu-id="5b5ab-136">راجع التعليمات البرمجية الخاصة بالأسلوب **insertFile()** للفئة **ERDocuManagement**.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="5b5ab-137">لاحظ ظهور الحدث **AttachingFile()** أثناء إرفاق الملف المُنشأ بسجل.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>

```
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

<span data-ttu-id="5b5ab-138">يظهر الحدث **AttachingFile()** عند معالجة الوجهات التالية للتقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="5b5ab-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="5b5ab-139">**أرشيف** - عند استخدام هذه الوجهة، يتم إنشاء سجل جديد لتنسيق التقارير الإلكترونية قيد التشغيل في الجدول ERFormatMappingRunJobTable.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="5b5ab-140">الحقل **مؤرشف** في هذا السجل معين إلى **False**.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="5b5ab-141">إذا نجح تشغيل تنسيق التقارير الإلكترونية، يتم إرفاق المستند المُنشأ بهذا السجل، ويظهر الحدث **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="5b5ab-142">يحدد نوع المستند المحدد في تنسيق التقارير الإلكترونية موقع تخزين الملف المرفق (Microsoft Azure Storage أو مجلد Microsoft SharePoint).</span><span class="sxs-lookup"><span data-stu-id="5b5ab-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="5b5ab-143">**أرشيف الوظائف** - عند استخدام هذه الوجهة، يتم إنشاء سجل جديد لنموذج التقارير الإلكترونية قيد التشغيل في الجدول ERFormatMappingRunJobTable.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="5b5ab-144">الحقل **مؤرشف** في هذا السجل معين إلى **True‎**.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="5b5ab-145">إذا نجح تشغيل تنسيق التقارير الإلكترونية، يتم إرفاق المستند المُنشأ بهذا السجل، ويظهر الحدث **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="5b5ab-146">يحدد نوع المستند المكوّن في معلمات التقارير الإلكترونية موقع تخزين الملف المرفق (Azure Storage أو مجلد SharePoint).</span><span class="sxs-lookup"><span data-stu-id="5b5ab-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![صفحة معلمات التقارير الإلكترونية](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="5b5ab-148">تكوين وجهة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5b5ab-148">Configure an ER destination</span></span>

1. <span data-ttu-id="5b5ab-149">كوّن الوجهة المؤرشفة لأحد العناصر المشار إليها في وقت سابق (ملف أو مجلد أو دمج أو مرفق) لتنسيق التقارير الإلكترونية الذي أنشأته أو استوردته.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="5b5ab-150">للحصول على إرشادات، راجع [التقارير الإلكترونية - تكوين الوجهات](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="5b5ab-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="5b5ab-151">استخدم نوع المستند الذي أضفته في وقت سابق للوجهة التي تم تكوينها.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="5b5ab-152">(على سبيل المثال في هذا الموضوع، نوع المستند هو **FileX**.)</span><span class="sxs-lookup"><span data-stu-id="5b5ab-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![مربع حوار إعدادات الوجهة](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="5b5ab-154">تعديل التعليمات البرمجية المصدر</span><span class="sxs-lookup"><span data-stu-id="5b5ab-154">Modify source code</span></span>

1. <span data-ttu-id="5b5ab-155">أضف فئة جديدة إلى مشروع Microsoft Visual Studio واكتب تعليمات برمجية للاشتراك في الحدث **AttachingFile()** الذي أشرنا إليه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="5b5ab-156">(للحصول على مزيد من المعلومات حول نمط قابلية التوسعة المستخدم، راجع [الاستجابة باستخدام EventHandlerResult‬](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) على سبيل المثال، في الفئة الجديدة، اكتب تعليمات برمجية تنفذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="5b5ab-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="5b5ab-157">قم بتخزين الملفات المُنشأة في مجلد في نظام الملفات المحلي للخادم الذي يقوم بتشغيل خدمة خادم كائنات التطبيق‬ (AOS).</span><span class="sxs-lookup"><span data-stu-id="5b5ab-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="5b5ab-158">قم تخزين هذه الملفات المُنشأة فقط عند استخدام نوع المستند الجديد (على سبيل المثال، نوع الملف **FileX‎** الذي يتضمن الكلمة الأساسية "(LOCAL)" في اسمه) أثناء إرفاق ملف بسجل في سجل وظيفة التنفيذ التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

    ```
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. <span data-ttu-id="5b5ab-159">أعد بناء مشروعك.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="5b5ab-160">تشغيل تنسيق التقارير الإلكترونية الذي أنشأته أو استوردته</span><span class="sxs-lookup"><span data-stu-id="5b5ab-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="5b5ab-161">نفّذ تنسيق التقارير الإلكترونية الذي أنشأته أو استوردته.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="5b5ab-162">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> وظائف إعداد التقارير الإلكترونية‬‬**.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="5b5ab-163">ابحث عن السجل التي تم إنشاؤه لوظيفة التنفيذ هذه، والذي يتضمن الملف المُنشأ المرفق به.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="5b5ab-164">استكشف المجلد المحلي **C:\\0** للعثور على الملف المنُشأ نفسه.</span><span class="sxs-lookup"><span data-stu-id="5b5ab-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b5ab-165">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5b5ab-165">Additional resources</span></span>

- [<span data-ttu-id="5b5ab-166">وجهات التقارير الإلكترونية‬</span><span class="sxs-lookup"><span data-stu-id="5b5ab-166">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="5b5ab-167">الصفحة الرئيسية لقابلية للتوسعة</span><span class="sxs-lookup"><span data-stu-id="5b5ab-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
