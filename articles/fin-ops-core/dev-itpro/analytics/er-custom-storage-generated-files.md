---
title: تحديد مواقع مساحة تخزين مخصصة للمستندات المُنشأة
description: يشرح هذا الموضوع كيفية توسيع قائمة مواقع التخزين للمستندات التي تم إنشاؤها بواسطة تنسيقات التقارير الإلكترونية (ER).
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bd979bf5369b6878caaee82fc9c6a40d363cc165
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894138"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="ba81c-103">تحديد مواقع مساحة تخزين مخصصة للمستندات المُنشأة</span><span class="sxs-lookup"><span data-stu-id="ba81c-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ba81c-104">تسمح لك واجهة برمجة التطبيقات (API) لإطار عمل التقارير الإلكترونية بتوسيع قائمة مواقع التخزين التي تقوم تنسيقات التقارير الإلكترونية بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="ba81c-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="ba81c-105">يشرح هذا الموضوع كيفية إضافة موقع تخزين مخصص للمستندات التي تم إنشاؤها عن طريق تفويض مهمة إنشاء وجهات إعداد التقارير الإلكترونية إلى المصنع الوجهة الافتراضي ثم تنفيذ فئة مخصصة لها منطق الوجهة الخاص بها.</span><span class="sxs-lookup"><span data-stu-id="ba81c-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ba81c-106">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="ba81c-106">Prerequisites</span></span>

<span data-ttu-id="ba81c-107">انشر طبولوجيا تدعم البناء المستمر.</span><span class="sxs-lookup"><span data-stu-id="ba81c-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="ba81c-108">لمزيد من المعلومات ، راجع [نشر مخططات تدعم البناء المستمر والتنفيذ التلقائي للاختبار‬ات](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span><span class="sxs-lookup"><span data-stu-id="ba81c-108">For more information, see [Deploy topologies that support continuous build and test automation](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="ba81c-109">يجب أن يكون لديك حق الوصول إلى هذه الطبولوجيا لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="ba81c-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="ba81c-110">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="ba81c-110">Electronic reporting developer</span></span>
- <span data-ttu-id="ba81c-111">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="ba81c-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="ba81c-112">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="ba81c-112">System administrator</span></span>

<span data-ttu-id="ba81c-113">يجب أن يكون لديك أيضًأ حق الوصول إلى بيئة التطوير لهذا المخطط.</span><span class="sxs-lookup"><span data-stu-id="ba81c-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="ba81c-114">يمكن إكمال جميع المهام الموجودة في هذا الموضوع في شركة **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="ba81c-115">استيراد تنسيق إعداد التقارير الإلكترونية لسجل نشاط الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="ba81c-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="ba81c-116">لإنشاء المستندات التي تخطط لإضافة موقع تخزين مخصص لها، [استورد](er-download-configurations-global-repo.md) تكوين تنسيق التقارير الإلكترونية لـ **سجل نشاط الأصول الثابتة‬** في الطبولوجيا الحالية.</span><span class="sxs-lookup"><span data-stu-id="ba81c-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![صفحة مستودع التكوين](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="ba81c-118">تشغيل تقرير سجل نشاط الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="ba81c-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="ba81c-119">انتقل إلى **الأصول الثابتة** \> **الاستعلامات والتقارير** \> **تقارير الحركة** \> **سجل نشاط الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="ba81c-120">في حقل **من تاريخ**، أدخل **1/1/2017**‏ (1 يناير 2017).</span><span class="sxs-lookup"><span data-stu-id="ba81c-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="ba81c-121">في حقل **إلى تاريخ**، أدخل **1/31/2017**‏ (31 يناير 2017).</span><span class="sxs-lookup"><span data-stu-id="ba81c-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="ba81c-122">في **حقل العملة**، حدد **عملة المحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="ba81c-123">في حقل **تعيين التنسيق**، حدد **سجل نشاط الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="ba81c-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-124">Select **OK**.</span></span>

![مربع حوار وقت التشغيل الخاص بتقرير سجل نشاط الأصول الثابتة](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="ba81c-126">في Microsoft Excel، راجع المستند الصادر الذي تم إنشاؤه والمتوفر للتنزيل.</span><span class="sxs-lookup"><span data-stu-id="ba81c-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="ba81c-127">ويعد هذا السلوك هو [السلوك الافتراضي](electronic-reporting-destinations.md#default-behavior) لتنسيق التقارير الإلكترونية الذي لم يتم تكوين أي [وجهات](electronic-reporting-destinations.md) له، ويتم تشغيله في وضع تفاعلي.</span><span class="sxs-lookup"><span data-stu-id="ba81c-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="ba81c-128">مراجعة كود المصدر</span><span class="sxs-lookup"><span data-stu-id="ba81c-128">Review the source code</span></span>

<span data-ttu-id="ba81c-129">راجع كود أسلوب `generateReportByGER()` لفئة `AssetRollForwardService`.</span><span class="sxs-lookup"><span data-stu-id="ba81c-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="ba81c-130">لاحظ أنه يتم استخدام أسلوب `Run()` لاستدعاء إطار عمل التقارير الإلكترونية وإنشاء تقرير **سجل نشاط الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a><span data-ttu-id="ba81c-131">تعديل كود المصدر</span><span class="sxs-lookup"><span data-stu-id="ba81c-131">Modify the source code</span></span>

1. <span data-ttu-id="ba81c-132">في مشروع Visual Studio الخاص بك، أضف فئة جديدة (`AssetRollForwardDestination` في هذا المثال)، واكتب الكود لتنفيذ الوجهة المخصصة الخاصة بك لتقارير **سجل نشاط الأصول الثابتة** التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="ba81c-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="ba81c-133">تم تصميم أسلوب `new()` للحصول علي كائن وجهة التقارير الإلكترونية الأصلية ومعلمة تستند إلى منطق التطبيق التي تحدد الموقع المخصص حيث يجب تخزين التقارير التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="ba81c-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="ba81c-134">في هذا المثال، يكون الموقع المخصص هو اسم مجلد لنظام الملفات المحلي للخادم الذي يقوم بتشغيل خدمة خادم كائنات التطبيق (AOS).</span><span class="sxs-lookup"><span data-stu-id="ba81c-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="ba81c-135">تم تصميم أسلوب `saveFile()` لحفظ المستند الذي تم إنشاؤه في مجلد نظام الملفات المحلي الخاص بالخادم الذي يقوم بتشغيل خدمة AOS.</span><span class="sxs-lookup"><span data-stu-id="ba81c-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="ba81c-136">في مشروع Visual Studio الخاص بك، أضف فئة `AssetRollForwardDestinationFactory` جديدة (في هذا المثال)، واكتب التعليمات البرمجية لإعداد مصنع وجهة مخصص يقوم بتفويض إنشاء وجهة إلى مصنع الوجهة الافتراضي، ولتلخيص وجهة ملف بوجهتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="ba81c-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="ba81c-137">قم بتعديل فئة `AssetRollForwardService` الموجودة، واكتب التعليمات البرمجية لإعداد مصنع وجهة مخصص لمشغل التقارير.</span><span class="sxs-lookup"><span data-stu-id="ba81c-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="ba81c-138">لاحظ أنه عند إنشاء مصنع وجهة مخصص، يتم تمرير المعلمة التي تعتمد على التطبيق وتحدد مجلدًا هدفًا.</span><span class="sxs-lookup"><span data-stu-id="ba81c-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="ba81c-139">بهذه الطريقة، يتم استخدام هذا المجلد المستهدف لتخزين الملفات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="ba81c-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="ba81c-140">تأكد من وجود المجلد المحدد ( **c:\\0** في هذا المثال) في نظام الملفات المحلي للخادم الذي يقوم بتشغيل خدمة AOS.</span><span class="sxs-lookup"><span data-stu-id="ba81c-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="ba81c-141">وبخلاف ذلك، سيتم طرح استثناء [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="ba81c-141">Otherwise, a [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. <span data-ttu-id="ba81c-142">أعد بناء مشروعك.</span><span class="sxs-lookup"><span data-stu-id="ba81c-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="ba81c-143">إعادة تشغيل تقرير سجل نشاط الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="ba81c-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="ba81c-144">انتقل إلى **الأصول الثابتة** \> **الاستعلامات والتقارير** \> **تقارير الحركة** \> **سجل نشاط الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="ba81c-145">في حقل **‏من التاريخ**، أدخل **1/1/2017**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="ba81c-146">في حقل **‏إلى التاريخ**، أدخل **1/31/2017**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="ba81c-147">في **حقل العملة**، حدد **عملة المحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="ba81c-148">في حقل **تعيين التنسيق**، حدد **سجل نشاط الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="ba81c-149">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ba81c-149">Select **OK**.</span></span>
7. <span data-ttu-id="ba81c-150">استعرض المجلد المحلي **C:\\0** للعثور على الملف المنُشأ.</span><span class="sxs-lookup"><span data-stu-id="ba81c-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="ba81c-151">بسبب عدم استخدام كائن `originDestination` في كائن `AssetRollForwardDestination` في هذا المثال، فسيتم تجاهل تكوينات تنسيق التقارير الإلكترونية [الوجهات](electronic-reporting-destinations.md) في وقت الشغيل.</span><span class="sxs-lookup"><span data-stu-id="ba81c-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba81c-152">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ba81c-152">Additional resources</span></span>

- [<span data-ttu-id="ba81c-153">وجهات إعداد التقارير الإلكترونية (ER)‬</span><span class="sxs-lookup"><span data-stu-id="ba81c-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="ba81c-154">الصفحة الرئيسية لقابلية للتوسعة</span><span class="sxs-lookup"><span data-stu-id="ba81c-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]