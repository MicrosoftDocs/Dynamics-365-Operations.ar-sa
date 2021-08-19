---
title: تحديد موقع تخزين مخصص للمستندات التي يتم إنشاؤها
description: يشرح هذا الموضوع كيفية توسيع قائمة مواقع التخزين للمستندات التي تقوم تنسيقات التقارير الإلكترونية بإنشائها.
author: NickSelin
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 61a1e46497d650e2c063a5fe7537d17cf7aa1828a5a4504bb781e84aeb88f04a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718491"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>تحديد موقع تخزين مخصص للمستندات التي يتم إنشاؤها

[!include[banner](../includes/banner.md)]

تسمح لك واجهة برمجة التطبيقات (API) لإطار عمل التقارير الإلكترونية بتوسيع قائمة مواقع التخزين التي تقوم تنسيقات التقارير الإلكترونية بإنشائها. يتضمن هذا الموضوع نظرة عامة حول المهام الأساسية التي يجب إكمالها لإضافة موقع تخزين مخصص.

## <a name="prerequisites"></a>المتطلبات الأساسية

يجب نشر مخطط يدعم البناء المستمر. (لمزيد من المعلومات، راجع [نشر مخططات تدعم البناء المستمر والتنفيذ التلقائي للاختبار‬ات‬](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) يجب أن يكون لديك حق الوصول إلى هذا المخطط لأحد الأدوار التالية:

- مطور إعداد التقارير الإلكتروني
- مستشار وظيفي لإعداد التقارير الإلكتروني
- مسؤول النظام

يجب أن يكون لديك أيضًأ حق الوصول إلى بيئة التطوير لهذا المخطط.

## <a name="create-or-import-an-er-format-configuration"></a>إنشاء تكوين تنسيق التقارير الإلكترونية أو استيراده

في المخطط الحالي، يمكنك [إنشاء تنسيق تقارير إلكترونية جديد](tasks/er-format-configuration-2016-11.md) لإنشاء المستندات التي تخطط لإضافتها إلى موقع التخزين المخصص. بدلاً من ذلك، يمكنك [استيراد تنسيق تقارير إلكترونية موجود إلى هذا المخطط](general-electronic-reporting-manage-configuration-lifecycle.md).

![صفحة مصمم التنسيق‬.](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> يجب أن يحتوي تنسيق التقارير الإلكترونية الذي تقوم بإنشائه أو استيراده على عنصر واحد على الأقل من عناصر التنسيق التالية:
>
> - ملف
> - المجلد
> - دمج
> - مرفق

## <a name="create-a-new-document-type"></a>إنشاء نوع مستند جديد

لتحديد كيفية توجيه المستندات التي يقوم تنسيق التقارير الإلكترونية بإنشائها، يجب تكوين [وجهات التقارير الإلكترونية (ER)](electronic-reporting-destinations.md). في كل وجهة تقارير إلكترونية تم تكوينها لتخزين المستندات المنشأة كملفات، يجب تحديد نوع مستند من إطار عمل إدارة المستندات. ويمكن استخدام أنواع مستندات مختلفة لتوجيه المستندات التي تقوم تنسيقات تقارير إلكتروني مختلفة بإنشائها.

1. أضف [نوع مستند](../../fin-ops/organization-administration/configure-document-management.md) جديدًا لتنسيق التقارير الإلكترونية الذي أنشأته أو استوردته في خطوة سابقة. في الرسم التوضيحي الذي يلي، نوع المستند هو **FileX**.
2. لتمييز نوع المستند هذا عن أنواع المستندات أخرى، يمكنك تضمين كلمة أساسية معينة في اسمه. على سبيل المثال، في الرسم التوضيحي الذي يلي، الاسم هو **المجلد (LOCAL)**.
3. في حقل **الفئة**، حدد **إرفاق ملف**.
4. في حقل **المجموعة**، حدد **ملف**.

![صفحة أنواع المستندات.](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> تتعلق أنواع المستندات بالشركة. لاستخدام تنسيق تقارير إلكترونية مع وجهة مكوّنة في شركات متعددة، يجب تكوين نوع مستند منفصل في كل شركة.

## <a name="review-source-code"></a>مراجعة التعليمات البرمجية المصدر

راجع التعليمات البرمجية الخاصة بالأسلوب **insertFile()** للفئة **ERDocuManagement**. لاحظ ظهور الحدث **AttachingFile()** أثناء إرفاق الملف المُنشأ بسجل.


```xpp
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

يظهر الحدث **AttachingFile()** عند معالجة الوجهات التالية للتقارير الإلكترونية:

- **أرشيف** - عند استخدام هذه الوجهة، يتم إنشاء سجل جديد لتنسيق التقارير الإلكترونية قيد التشغيل في الجدول ERFormatMappingRunJobTable. الحقل **مؤرشف** في هذا السجل معين إلى **False**. إذا نجح تشغيل تنسيق التقارير الإلكترونية، يتم إرفاق المستند المُنشأ بهذا السجل، ويظهر الحدث **AttachingFile()**. يحدد نوع المستند المحدد في تنسيق التقارير الإلكترونية موقع تخزين الملف المرفق (Microsoft Azure Storage أو مجلد Microsoft SharePoint).
- **أرشيف الوظائف** - عند استخدام هذه الوجهة، يتم إنشاء سجل جديد لنموذج التقارير الإلكترونية قيد التشغيل في الجدول ERFormatMappingRunJobTable. الحقل **مؤرشف** في هذا السجل معين إلى **True‎**. إذا نجح تشغيل تنسيق التقارير الإلكترونية، يتم إرفاق المستند المُنشأ بهذا السجل، ويظهر الحدث **AttachingFile()**. يحدد نوع المستند المكوّن في معلمات التقارير الإلكترونية موقع تخزين الملف المرفق (Azure Storage أو مجلد SharePoint).

![صفحة معلمات التقارير الإلكترونية.](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>تكوين وجهة التقارير الإلكترونية

1. كوّن الوجهة المؤرشفة لأحد العناصر المشار إليها في وقت سابق (ملف أو مجلد أو دمج أو مرفق) لتنسيق التقارير الإلكترونية الذي أنشأته أو استوردته. للحصول على إرشادات، راجع [التقارير الإلكترونية - تكوين الوجهات](/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. استخدم نوع المستند الذي أضفته في وقت سابق للوجهة التي تم تكوينها. (على سبيل المثال في هذا الموضوع، نوع المستند هو **FileX**.)

![مربع حوار إعدادات الوجهة.](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>تعديل التعليمات البرمجية المصدر

1. أضف فئة جديدة إلى مشروع Microsoft Visual Studio واكتب تعليمات برمجية للاشتراك في الحدث **AttachingFile()** الذي أشرنا إليه سابقًا. (للحصول على مزيد من المعلومات حول نمط قابلية التوسعة المستخدم، راجع [الاستجابة باستخدام EventHandlerResult‬](/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) على سبيل المثال، في الفئة الجديدة، اكتب تعليمات برمجية تنفذ الإجراءات التالية:

    1. قم بتخزين الملفات المُنشأة في مجلد في نظام الملفات المحلي للخادم الذي يقوم بتشغيل خدمة خادم كائنات التطبيق‬ (AOS).
    2. قم تخزين هذه الملفات المُنشأة فقط عند استخدام نوع المستند الجديد (على سبيل المثال، نوع الملف **FileX‎** الذي يتضمن الكلمة الأساسية "(LOCAL)" في اسمه) أثناء إرفاق ملف بسجل في سجل وظيفة التنفيذ التقارير الإلكترونية.

    ```xpp
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

2. أعد بناء مشروعك.

## <a name="run-the-er-format-that-you-created-or-imported"></a>تشغيل تنسيق التقارير الإلكترونية الذي أنشأته أو استوردته

1. نفّذ تنسيق التقارير الإلكترونية الذي أنشأته أو استوردته.
2. انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> وظائف إعداد التقارير الإلكترونية‬‬**. ابحث عن السجل التي تم إنشاؤه لوظيفة التنفيذ هذه، والذي يتضمن الملف المُنشأ المرفق به.
3. استكشف المجلد المحلي **C:\\0** للعثور على الملف المنُشأ نفسه.

## <a name="additional-resources"></a>الموارد الإضافية

- [وجهات التقارير الإلكترونية‬](electronic-reporting-destinations.md)
- [الصفحة الرئيسية لقابلية للتوسعة](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]