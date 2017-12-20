---
title: "إعادة تعيين متجر بيانات للتقارير المالية"
description: "يشرح هذا الموضوع كيفية إعادة تعيين متجر بيانات التقارير المالية."
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: ar-sa
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>إعادة تعيين متجر بيانات للتقارير المالية

[!include[banner](../includes/banner.md)]

يشرح هذا الموضوع كيفية إعادة تعيين متجر بيانات التقارير المالية للإصدارات التالية:

- إصدار التقارير المالية في Microsoft Dynamics 365 for Finance and Operations رقم 7.2.6.0 وإصدار أحدث
- إصدار التقارير المالية في Microsoft Dynamics 365 for Finance and Operations رقم 7.0.10000.4 وإصدار أحدث
- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (محلي)

للحصول على إصدار التقارير المالية 7.2.6.0 لـ Finance and Operations، يمكنك تنزيل قاعدة المعارف KB 4052514 من <https://support.microsoft.com/en-us/help/4052514>.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>إعادة تعيين متجر بيانات التقارير المالية لإصدار التقارير المالية لـ Finance and Operations رقم 7.2.6.0 أو إصدار أحدث

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>إعادة تعيين متجر بيانات التقارير المالية من مصمم التقارير

> [!NOTE]
> الخطوات المذكورة في هذه العملية مدعومة لإصدار التقارير المالية لـ Finance and Operations رقم 7.2.6.0 وإصدار أحدث. إذا كان لديك إصدار سابق، فاتصل بفريق الدعم للحصول على المساعدة.

في السيناريوهات المحددة، قد تحتاج إلى إعادة تعيين متجر البيانات للتقارير المالية. يمكنك إكمال هذه المهمة في عميل مصمم التقارير. فيما يلي بعض السيناريوهات التي قد تحتاج إلى إعادة تعيين متجر البيانات:

- تمت استعادة قاعدة بيانات Finance and Operations، ولكن لم تتم استعادة قاعدة بيانات متجر البيانات.
- تشاهد بيانات غير صحيحة لفترة.
- يرشدك الدعم إلى إعادة تعيين متجر البيانات كجزء من إحدى خطوات استكشاف الأخطاء وإصلاحها.

يجب ألا تتم إعادة تعيين متجر البيانات إلا عندما يكون مقدار المعالجة في قاعدة البيانات صغيرًا. لن تتوفر التقارير المالية أثناء عملية إعادة التعيين.

#### <a name="reset-the-data-mart"></a>إعادة تعيين متجر البيانات

لإعادة تعيين متجر البيانات، في مصمم التقرير، على القائمة **أدوات**، حدد **إعادة تعيين متجر البيانات**. يحتوي مربع الحوار الذي يظهر على قسمين: **الإحصاءات** و**إعادة التعيين**.

[![إعادة تعيين مربع حوار متجر البيانات](./media/Statistics.png)](./media/Statistics.png)

##### <a name="integration-attempts"></a>محاولات التكامل:

تعرض شبكة **محاولات التكامل** عدد المرات محاولة النظام دمج الحركات. يواصل النظام محاولة تكامل البيانات خلال فترة من الأيام إذا لم تنجح المحاولات القليلة الأولى. ستعرف أنه يجب إعادة تعيين متجر البيانات إذا كان عدد المحاولات 8 أو أكثر، وإذا كان لديك العديد من مجموعات الأبعاد أو سجلات الحركات. في هذه الحالة، لن يتم الإبلاغ عن البيانات.

##### <a name="data-status"></a>حالة البيانات

توفر شبكة **حالة البيانات** لقطة للحركات وأسعار الصرف وقيم الأبعاد في متجر البيانات. يشير عدد كبير من السجلات التالفة إلى التحديثات الهائلة التي تم إجراؤها على السجلات. قد يتسبب هذا الموقف في ظهور أوقات إنشاء تقارير أبطأ.

##### <a name="misaligned-main-account-categories"></a>فئات الحساب الرئيسي التي تمت محاذاتها بشكل غير صحيح

إذا كنت تستخدم إصدار أقدم من إصدار التقارير المالية 7.2.1 لـ Microsoft Dynamics 365 for Finance and Operations، فقد تضطر إلى إعادة تعيين متجر البيانات إذا قمت بإعادة تسمية حسابات ونقلها بين فئات الحسابات. قد تؤدي هذه الإجراءات إلى محاذاة فئات الحسابات الرئيسية بطريقة خاطئة. يعرض حقل **فئات الحسابات الرئيسية التي تمت محاذاتها طريقة خاطئة** ما إذا كنت تواجه هذه المشكلة أو لا.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>إعادة تعيين متجر البيانات في إصدار التقارير المالية 7.2.6.0 لـ Finance and Operations

لإعادة تعيين متجر البيانات في إصدار التقارير المالية 7.2.6.0 لـ Finance and Operations والإصدارات السابقة له، في مربع الحوار **"إعادة تعيين متجر البيانات"**، حدد خانة الاختيار **إعادة تعيين متجر البيانات**، ثم حدد **موافق**. يجب عليك إعادة تعيين متجر البيانات فقط أثناء وقت التعطل المجدول.

[![إعادة تعيين خانة اختيار متجر البيانات](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>إعادة تعيين متجر البيانات وتحديد أحد الأسباب في إصدار التقارير المالية 7.3.0 لـ Microsoft Dynamics 365 for Finance and Operations

إذا وجدت أن إعادة تعيين متجر بيانات مطلوبة، فحدد خانة الاختيار **إعادة تعيين متجر البيانات**، ثم حدد أحد الأسباب في حقل **السبب**. يتوفر الخياران التاليان:

- **البيانات المفقودة أو غير الصحيحة** -وفقًا للإحصاءات، لقد حددت أنك البيانات قد تكون مفقودة. قبل المتابعة، نوصي بأن تعمل مع الدعم لتحديد السبب الجذري.
- **استعادة قاعدة البيانات** – تمت استعادة قاعدة بيانات Finance and Operations، ولكن لم تتم استعادة قاعدة البيانات لمتجر بيانات التقارير المالية.
- **أخرى** -في حالة إعادة تعيين متجر البيانات لسبب آخر. إذا كنت معنياً بأن هناك مشكلة، فاتصل بالدعم للتعرف عليها.

> [!NOTE]
> تحقق من انتهاء تكامل جميع المهام الموجودة قبل إكمال الخطوات. يمكنك عرض حالة التكامل عن طريق تحديد **أدوات**&gt;**حالة التكامل**.

#### <a name="clear-users-and-companies"></a>مسح المستخدمين والشركات

حدد خانة الاختيار **إلغاء تحديد المستخدمين والشركات** في حالة استعادة قاعدة البيانات الخاصة بك، ولكن قمت بعد ذلك إجراء أي تغييرات على المستخدمين أو الشركات. يجب ألا تحدد خانة الاختيار هذه إلا في النادر.

عندما تكون مستعدًا لبدء عملية إعادة التعيين، حدد **موافق**. أنت مطالب بتأكيد أنك مستعد لبدء العملية. تجدر الإشارة إلى أن التقارير المالية لن تتوفر أثناء إعادة التعيين وتكامل البيانات الأولية التي تحدث بعد ذلك.

إذا كنت ترغب في مراجعة حالة التكامل، فحدد **أدوات**&gt;**حالة التكامل** لمشاهدة آخر مرة تم تشغيل التكامل فيها وحالة ذلك.

[![عرض حالة التكامل](./media/Integration.png)](./media/Integration.png)

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>إعادة تعيين متجر بيانات التقارير المالية لإصدار التقارير المالية لـ Finance and Operations رقم 7.0.10000.4 أو إصدار أحدث

إذا قمت في أي وقت باستعادة قاعدة بيانات Finance and Operations من نسخة احتياطية أو نسخ قاعدة البيانات من بيئة أخرى، فيجب اتباع الخطوات الواردة في هذا الموضوع للمساعدة على ضمان أن متجر بيانات التقارير المالية يستخدم قاعدة بيانات Finance and Operations التي تمت استعادتها بشكل صحيح.

> [!NOTE]
> الخطوات الواردة في هذه العملية مدعومة لإصدار 7.0.1 من تطبيق Microsoft Dynamics AX (مايو 2016) (إصدار التطبيق 7.0.1265.23014 وإصدار التقارير المالية 7.0.10000.4) والإصدار الأحدث. إذا كان لديك إصدار سابق من Finance and Operations، فاتصل بفريق الدعم للمساعدة.

### <a name="export-report-definitions"></a>تصدير تعريفات التقارير

أولاً، اتبع هذه الخطوات لتصدير تصميمات التقارير من "مصمم التقارير".

1. في مصمم التقارير، حدد **الشركة** &gt; **مجموعات كتل الإنشاء**.
2. حدد مجموعة كتلة الإنشاء لتصديرها، ثم حدد **تصدير**.

    > [!NOTE]
    > ملاحظة: بالنسبة إلى Finance and Operations، يتم دعم مجموعة واحدة فقط من كتل الإنشاء، وهي المجموعة **الافتراضية**.

3. حدد تعريفات التقارير لتصديرها:

    - لتصدير كل تعريفات التقارير وكتل الإنشاء المقترنة، حدد **تحديد الكل**.
    - لتصدير مجموعات محددة من التقارير أو الصفوف أو الأعمدة أو الأشجار أو الأبعاد، حدد علامة التبويب المناسبة ثم حدد العناصر المراد تصديرها. اضغط باستمرار على المفتاح Ctrl لتحديد عدة عناصر على علامة تبويب. عندما تحدد تقارير لتصديرها، سيتم تحديد الصفوف والأعمدة والأشجار ومجموعات الأبعاد ذات الصلة.‬

4. حدد **تصدير**.
5. أدخل اسم ملف وحدد موقعًا آمنًا حيث تريد حفظ تعريفات التقارير التي تم تصديرها.
6. حدد **حفظ**.

يمكنك نسخ أو تحميل الملف إلى موقع آمن. وبهذه الطريقة، يمكن استيراد الملف في بيئة مختلفة فيما بعد. لمزيد من المعلومات حول كيفية استخدام حساب Microsoft Azure storage، راجع [نقل البيانات باستخدام أداة سطر الأوامر المساعدة AzCopy](/azure/storage/storage-use-azcopy).

> [!NOTE]
> لا تقدم Microsoft حساب تخزين كجزء من اتفاقية Finance and Operations. يجب عليك شراء حساب تخزين أو استخدام حساب تخزين من اشتراك Azure منفصل.

> [!WARNING]
> يجب مراعاة سلوك محرك الأقراص D على أجهزة Azure الظاهرية (VMs). لا تقم بشكل دائم بتخزين مجموعة الكتل البرمجية الإنشائية المُصدَر الخاصة بك على محرك الأقراص D. وللحصول على مزيد من المعلومات حول محركات الأقراص المؤقتة، راجع [التعرف على محرك الأقراص المؤقت على الأجهزة الظاهرية من Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>وقف الخدمات

سيكون لخدمات Microsoft Windows التالية اتصالات مفتوحة بقاعدة بيانات Finance and Operations. ولذلك، يجب عليك استخدام سطح المكتب البعيد من Microsoft للاتصال بجميع أجهزة الكمبيوتر الموجودة في البيئة، ثم استخدام services.msc لإيقاف هذه الخدمات.

- خدمة النشر على شبكة الإنترنت العالمية (على جميع أجهزة الكمبيوتر التي تعمل بنظام خوادم كائنات التطبيقات [AOS])
- خدمة إدارة الدفعة لـ Microsoft Dynamics 365 for Finance and Operations (على أجهزة الكمبيوتر التي لا تعمل بنظام AOS فقط)
- خدمة عملية 2012 لأداة تقارير الإدارة (على أجهزة كمبيوتر BI فقط)

### <a name="reset"></a>إعادة التعيين

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>تنزيل موقع حزمة MinorVersionDataUpgrade.zip الأحدث

قم بتنزيل حزمة MinorVersionDataUpgrade.zip الأحدث. للحصول على إرشادات حول كيفية العثور على وتنزيل الإصدار الصحيح من حزمة ترقية البيانات، راجع[تنزيل حزمة ترقية البيانات الأحدث والقابلة للنشر](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). لا حاجة إلى إجراء عملية ترقية لتنزيل حزمة MinorVersionDataUpgrade.zip. ولذلك، ماعليك سوى اتباع الخطوات الواردة في قسم "تنزيل حزمة ترقية البيانات الأحدث والقابلة للنشر" في هذا الموضوع. يمكنك تخطي كل الخطوات الأخرى في الموضوع.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>تشغيل البرامج النصية مقابل قاعدة بيانات Finance and Operations

تشغيل البرامج النصية التالية مقابل قاعدة بيانات Finance and Operations (وليس مقابل قاعدة بيانات التقارير المالية):

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

تساعد هذه البرامج النصية على ضمان صحة إعدادات تتبع المستخدمين والأدوار والتغييرات.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>تشغيل أمر Windows PowerShell لإعادة تعيين قاعدة البيانات

على كمبيوتر AOS، ابدأ تشغيل Microsoft Windows PowerShell كمسؤول، وقم بتشغيل الأوامر التالية لإعادة تعيين التكامل بين التقارير المالية لـ Finance and Operations.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

فيما يلي توضيح للمعلمات في أمر **Reset-DatamartIntegration**:

- القيم الصالحة لـ **-Reason** هي **SERVICING**، و**BADDATA**، و**OTHER**.
- معلمة **-ReasonDetail** عبارة عن نص حر.
- سيتم تسجيل السبب وتفاصيل السبب في مراقبة القياس عن بعد/البيئة.

> [!NOTE]
> بعد تشغيل الأوامر، سوف يُطلب منك إدخال **ص** لتأكيد رغبتك في إعادة تعيين قاعدة البيانات.

#### <a name="restart-services"></a>إعادة تشغيل الخدمات

استخدم services.msc لإعادة تشغيل الخدمات التي قمت بوقفها في وقت سابق:

- خدمة النشر على شبكة الإنترنت العالمية (على كافة أجهزة الكمبيوتر التي تعمل بنظام AOS)
- خدمة إدارة الدفعة لـ Microsoft Dynamics 365 for Finance and Operations (على أجهزة الكمبيوتر التي لا تعمل بنظام AOS فقط)
- خدمة عملية 2012 لإدارة تقارير الأداة (على أجهزة كمبيوتر BI فقط)

#### <a name="import-report-definitions"></a>استيراد تعريفات التقارير

استورد تصاميم التقارير من مصمم التقارير باستخدام الملف الذي تم إنشاؤه أثناء عملية التصدير.

1. في مصمم التقارير، حدد **الشركة** &gt; **مجموعات كتل الإنشاء**.
2. حدد مجموعة كتلة الإنشاء لتصديرها، ثم حدد **تصدير**.

    > [!NOTE]
    > ملاحظة: بالنسبة إلى Finance and Operations، يتم دعم مجموعة واحدة فقط من كتل الإنشاء، وهي المجموعة **الافتراضية**.

3. حدد كتلة الإنشاء **الافتراضية**، ثم حدد **استيراد**.
4. حدد الملف الذي يحتوي على تعاريف التقارير التي تم تصديرها، ثم حدد **فتح**.
5. في مربع حوار **استيراد**، حدد تعريفات التقارير المطلوب استيرادها:

    - لاستيراد كل تعاريف التقارير وكتل الإنشاء المقترنة، حدد **تحديد الكل**.
    - لاستيراد تقارير أو صفوف أو أعمدة أو أشجار أو مجموعات أبعاد محددة، حدد التقارير أو الصفوف أو الأعمدة أو الأشجار أو مجموعات الأبعاد المطلوب استيرادها.

6. حدد **استيراد**.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>إعادة تعيين متجر بيانات التقارير المالية لـ Finance and Operations (محلي)

1. أرشد جميع المستخدمين إلى الخروج من منطقة التقارير المالية ومصمم التقارير في Finance and Operations.
2. قم بتشغيل البرنامج النصي التالي مقابل قاعدة بيانات التقارير المالية (MRDB).

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. قم بتقطيع أو حذف جميع السجلات من جدول FINANCIALREPORTS في قاعدة بيانات Finance and Operations ‏(AXDB).
4. قم بتقطيع أو حذف جميع السجلات من جدول FINANCIALREPORTVERSION، إذا كان هذا الجدول موجودًا في قاعدة بيانات Finance and Operations. في حالة عدم وجود الجدول في قاعدة بيانات Finance and Operations، تجاوز هذه الخطوة.
5. قم بتشغيل البرنامج النصي **ResetDatamart.sql** مقابل قاعدة بيانات التقارير المالية. يقوم هذا البرنامج النصي بتعطيل تكامل متجر البيانات، ويحذف كافة بيانات متجر البيانات، ثم يعيد تمكين تكامل متجر البيانات.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. بعد إعادة التعيين، يمكنك التحقق من إعادة تحميل البيانات يدوياً عن طريق تشغيل الاستعلام التالي مقابل قاعدة بيانات التقارير المالية.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    تأكد من أن جميع الصفوف تحتوي على قيمة **LastRunTime** ومن تعيين **StateType** على **5**. تشير قيمة **StateType** البالغة **5** إلى أنه تمت إعادة تحميل البيانات بنجاح. تشير القيمة البالغة **7** إلى حالة خطأ. في بعض الأحيان، تشتمل خريطة التدرج الهرمي للمؤسسات على هذه الحالة في أول مرة لتشغيلها. ومع ذلك، يجب أن يتم حل حالة الخطأ تلقائيًا.

