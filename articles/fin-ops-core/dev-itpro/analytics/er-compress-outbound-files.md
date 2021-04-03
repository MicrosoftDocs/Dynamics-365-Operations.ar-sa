---
title: ضغط المستندات الكبيرة المُنشأة بتنسيق التقارير الإلكترونية
description: يشرح هذا الموضوع كيفية ضغط المستندات الكبيرة المُنشأة بتنسيق التقارير الإلكترونية.
author: NickSelin
manager: kfend
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8a8f55b33624b057a6abf9af5084209ac6a0c778
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562324"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>ضغط المستندات الكبيرة المُنشأة بتنسيق التقارير الإلكترونية 

[!include [banner](../includes/banner.md)]

يمكنك استخدام [إطار عمل ‏‫إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md) لتكوين حل يُحضر بيانات الحركات‬ لإنشاء مستند صادر. قد يكون حجم هذا المستند المُنشأ كبيرًا جدًا. عند إنشاء هذا النوع من المستندات، يتم استخدام ذاكرة [خادم كائن التطبيق (AOS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/access-instances#location-of-packages-source-code-and-other-aos-configurations) لاحتوائه. في مرحلة معينة، يجب تحميل المستند من تطبيق Microsoft Dynamics 365 Finance. في الوقت الحالي، يقتصر الحد الأقصى لحجم مستند واحد يتم إنشاؤه بتنسيق التقارير الإلكترونية على 2 غيغابايت. علاوةً على ذلك، [يحدد](https://fix.lcs.dynamics.com/Issue/Details?kb=4569432&bugId=453907&dbType=3) تطبيق Finance حجم المستند المنزّل بغيغابايت واحد. وبالتالي، يجب عليك تكوين حل للتقارير الإلكترونية يقلل احتمال تجاوز هذه الحدود، وأنك ستتلقى استثناء **البث كان طويلاً جدًا** أو **تجاوز السعة أو نقص في السعة في العملية الحسابية**.

عند تكوين حل، يمكنك ضبط تنسيق التقارير الإلكترونية في مصمم العمليات عن طريق أضافه عنصر جذر من النوع **مجلد** لضغط المحتوى الذي يتم إنشاؤه بواسطة أي من العناصر المتداخلة فيه. يعمل الضغط "في الوقت المناسب"، حتى يمكن تقليل الاستخدام الأقصى لاستخدام الذاكرة وحجم الملف الذي سيتم تنزيله.

> [!NOTE]
> يتطلب ضغط الملفات نسبة مئوية إضافية من استخدام وحدة المعالجة المركزية.

لمعرفة المزيد عن هذا الأسلوب، أكمل المثال في هذا الموضوع.

## <a name="example-compress-an-outbound-document"></a>مثال: ضغط مستند صادر

يوضح هذا المثال كيف يمكن للمستخدم الذي تم تعيينه إلى دور **مسؤول النظام** أو **مستشار وظيفي لإعداد التقارير الإلكترونية** تكوين تنسيق تقارير إلكترونية لضغط مستند مُنشأ.

### <a name="prerequisites"></a>المتطلبات الأساسية

قبل أن تتمكن من استكمال الإجراءات في هذا الموضوع، يجب تنفيذ الخطوات التالية:

1. [تنشيط موفر تكوين](er-defer-xml-element.md#activate-a-configuration-provider).
2. [استيراد نموذج تكوينات التقارير الإلكترونية](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [مراجعة التنسيق المستورد](er-defer-xml-element.md#review-the-imported-format).

> [!NOTE]
> في الوقت الحالي، تبدأ بنية التنسيق من عنصر **التقرير** من النوع **ملف** وتحتوي على عناصر XML. وبالتالي، سيتم إنشاء مستند خارجي بتنسيق XML، ولن يتم استخدام أي ضغط.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>إنشاء تنسيق تقارير إلكترونية للحصول على مستند غير مضغوط

1. [تشغيل التنسيق المستورد](er-defer-xml-element.md#run-the-imported-format).
2. لاحظ أن حجم المستند المُنشأ بتنسيق XML هو 3 كيلوبايت (KB).

    ![معاينة المستند الصادر غير المضغوط](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>تعديل التنسيق لضغط الإخراج المُنشأ

1. انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.
2. في صفحة **التكوينات**، في شجرة التكوينات، وسَّع **Model to learn deferred elements**.
3. حدد التكوين **التنسيق للتعرف على عناصر XML المؤجلة**.
4. حدد **المصمم** لتعديل بنية التنسيق.
5. في صفحة  **مصمم التنسيق**، وفي علامة التبويب **التنسيق**، حدد **إضافة جذر** لإضافة عنصر تنسيق جذر.
6. في مربع الحوار **إضافة**، حدد **عام\\مجلد**.
7. حدد **موافق** لتأكيد إضافة العنصر الجذر الجديد.
8. حدد **حفظ**.

> [!NOTE]
> تبدأ بنية التنسيق من العنصر من النوع **مجلد**. سيقوم هذا العنصر بإنشاء الإخراج كملف مضغوط (zip). عند وضع مستند تم إنشاؤه بواسطة عنصر **التقرير** في ملف zip صادر، سيتم ضغط محتوياته لتقليل حجم الملف الصادر.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>إنشاء تنسيق تقارير إلكترونية للحصول على مستند مضغوط

1. في صفحة **مصمم التنسيق**، حدد **تشغيل**.
2. نزِّل ملف zip الذي يعرضه مستعرض الويب وافتحه للمراجعة.
3. لاحظ أن حجم المستند المُنشأ بتنسيق ZIP هو 1 كيلوبايت (KB).

    > [!NOTE] 
    > نسبة الضغط لملف XML الذي يحمله ملف zip هذا هي 87 بالمائة. تتوقف نسبة الضغط على البيانات التي يتم ضغطها.

    ![معاينة المستند الصادر المضغوط](./media/er-compress-outbound-files2.png)

> [!NOTE]
> إذا تم تكوين [وجهة](electronic-reporting-destinations.md) التقارير الإلكترونية لعنصر التنسيق الذي ينشئ الإخراج (عنصر **التقرير** في هذا المثال)، سيتم تجاوز ضغط الإخراج.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md)

[وجهات إعداد التقارير الإلكترونية (ER)‬](electronic-reporting-destinations.md)

[تأجيل تنفيذ عناصر XML في تنسيقات إعداد التقارير الإلكترونية](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]