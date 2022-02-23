---
title: تحديد مواقع مساحة تخزين مخصصة للمستندات المُنشأة
description: يشرح هذا الموضوع كيفية توسيع قائمة مواقع التخزين للمستندات التي تم إنشاؤها بواسطة تنسيقات التقارير الإلكترونية (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 362ac7f10cc61e26be89dfbae0e84745d42588a3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680748"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>تحديد مواقع مساحة تخزين مخصصة للمستندات المُنشأة

[!include[banner](../includes/banner.md)]

تسمح لك واجهة برمجة التطبيقات (API) لإطار عمل التقارير الإلكترونية بتوسيع قائمة مواقع التخزين التي تقوم تنسيقات التقارير الإلكترونية بإنشائها. يشرح هذا الموضوع كيفية إضافة موقع تخزين مخصص للمستندات التي تم إنشاؤها عن طريق تفويض مهمة إنشاء وجهات إعداد التقارير الإلكترونية إلى المصنع الوجهة الافتراضي ثم تنفيذ فئة مخصصة لها منطق الوجهة الخاص بها.

## <a name="prerequisites"></a>المتطلبات الأساسية

انشر طبولوجيا تدعم البناء المستمر. لمزيد من المعلومات ، راجع [نشر مخططات تدعم البناء المستمر والتنفيذ التلقائي للاختبار‬ات](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation). يجب أن يكون لديك حق الوصول إلى هذه الطبولوجيا لأحد الأدوار التالية:

- مطور إعداد التقارير الإلكتروني
- مستشار وظيفي لإعداد التقارير الإلكتروني
- مسؤول النظام

يجب أن يكون لديك أيضًأ حق الوصول إلى بيئة التطوير لهذا المخطط.

يمكن إكمال جميع المهام الموجودة في هذا الموضوع في شركة **USMF**.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>استيراد تنسيق إعداد التقارير الإلكترونية لسجل نشاط الأصول الثابتة

لإنشاء المستندات التي تخطط لإضافة موقع تخزين مخصص لها، [استورد](er-download-configurations-global-repo.md) تكوين تنسيق التقارير الإلكترونية لـ **سجل نشاط الأصول الثابتة‬** في الطبولوجيا الحالية.

![صفحة مستودع التكوين](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>تشغيل تقرير سجل نشاط الأصول الثابتة

1. انتقل إلى **الأصول الثابتة** \> **الاستعلامات والتقارير** \> **تقارير الحركة** \> **سجل نشاط الأصول الثابتة**.
2. في حقل **من تاريخ**، أدخل **1/1/2017**‏ (1 يناير 2017).
3. في حقل **إلى تاريخ**، أدخل **1/31/2017**‏ (31 يناير 2017).
4. في **حقل العملة**، حدد **عملة المحاسبة**.
5. في حقل **تعيين التنسيق**، حدد **سجل نشاط الأصول الثابتة**.
6. حدد **موافق**.

![مربع حوار وقت التشغيل الخاص بتقرير سجل نشاط الأصول الثابتة](./media/er-custom-storage-generated-files-runtime-dialog.png)

في Microsoft Excel، راجع المستند الصادر الذي تم إنشاؤه والمتوفر للتنزيل. ويعد هذا السلوك هو [السلوك الافتراضي](electronic-reporting-destinations.md#default-behavior) لتنسيق التقارير الإلكترونية الذي لم يتم تكوين أي [وجهات](electronic-reporting-destinations.md) له، ويتم تشغيله في وضع تفاعلي.

## <a name="review-the-source-code"></a>مراجعة كود المصدر

راجع كود أسلوب `generateReportByGER()` لفئة `AssetRollForwardService`. لاحظ أنه يتم استخدام أسلوب `Run()` لاستدعاء إطار عمل التقارير الإلكترونية وإنشاء تقرير **سجل نشاط الأصول الثابتة**.

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

## <a name="modify-the-source-code"></a>تعديل كود المصدر

1. في مشروع Visual Studio الخاص بك، أضف فئة جديدة (`AssetRollForwardDestination` في هذا المثال)، واكتب الكود لتنفيذ الوجهة المخصصة الخاصة بك لتقارير **سجل نشاط الأصول الثابتة** التي تم إنشاؤها.

    - تم تصميم أسلوب `new()` للحصول علي كائن وجهة التقارير الإلكترونية الأصلية ومعلمة تستند إلى منطق التطبيق التي تحدد الموقع المخصص حيث يجب تخزين التقارير التي تم إنشاؤها. في هذا المثال، يكون الموقع المخصص هو اسم مجلد لنظام الملفات المحلي للخادم الذي يقوم بتشغيل خدمة خادم كائنات التطبيق (AOS).
    - تم تصميم أسلوب `saveFile()` لحفظ المستند الذي تم إنشاؤه في مجلد نظام الملفات المحلي الخاص بالخادم الذي يقوم بتشغيل خدمة AOS.

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

2. في مشروع Visual Studio الخاص بك، أضف فئة `AssetRollForwardDestinationFactory` جديدة (في هذا المثال)، واكتب التعليمات البرمجية لإعداد مصنع وجهة مخصص يقوم بتفويض إنشاء وجهة إلى مصنع الوجهة الافتراضي، ولتلخيص وجهة ملف بوجهتك الخاصة.

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

3. قم بتعديل فئة `AssetRollForwardService` الموجودة، واكتب التعليمات البرمجية لإعداد مصنع وجهة مخصص لمشغل التقارير. لاحظ أنه عند إنشاء مصنع وجهة مخصص، يتم تمرير المعلمة التي تعتمد على التطبيق وتحدد مجلدًا هدفًا. بهذه الطريقة، يتم استخدام هذا المجلد المستهدف لتخزين الملفات التي تم إنشاؤها.

    > [!NOTE] 
    > تأكد من وجود المجلد المحدد ( **c:\\0** في هذا المثال) في نظام الملفات المحلي للخادم الذي يقوم بتشغيل خدمة AOS. وبخلاف ذلك، سيتم طرح استثناء [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) في وقت التشغيل.

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

4. أعد بناء مشروعك.

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>إعادة تشغيل تقرير سجل نشاط الأصول الثابتة

1. انتقل إلى **الأصول الثابتة** \> **الاستعلامات والتقارير** \> **تقارير الحركة** \> **سجل نشاط الأصول الثابتة**.
2. في حقل **‏من التاريخ**، أدخل **1/1/2017**.
3. في حقل **‏إلى التاريخ**، أدخل **1/31/2017**.
4. في **حقل العملة**، حدد **عملة المحاسبة**.
5. في حقل **تعيين التنسيق**، حدد **سجل نشاط الأصول الثابتة**.
6. حدد **موافق**.
7. استعرض المجلد المحلي **C:\\0** للعثور على الملف المنُشأ.

> [!NOTE]
> بسبب عدم استخدام كائن `originDestination` في كائن `AssetRollForwardDestination` في هذا المثال، فسيتم تجاهل تكوينات تنسيق التقارير الإلكترونية [الوجهات](electronic-reporting-destinations.md) في وقت الشغيل.

## <a name="additional-resources"></a>الموارد الإضافية

- [وجهات إعداد التقارير الإلكترونية (ER)‬](electronic-reporting-destinations.md)
- [الصفحة الرئيسية لقابلية للتوسعة](../extensibility/extensibility-home-page.md)
