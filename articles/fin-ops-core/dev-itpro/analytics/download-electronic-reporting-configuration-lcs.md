---
title: تنزيل تكوينات التقارير الإلكترونية من Lifecycle Services
description: يوضح هذا الموضوع كيفية تنزيل تكوينات التقارير الإلكترونية من Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271173"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>تنزيل تكوينات إعداد التقارير الإلكترونية من Lifecycle Services

[!include [banner](../includes/banner.md)]

يشرح هذا الموضوع كيفية تنزيل أحدث إصدار من [تكوينات التقارير الإلكترونية](general-electronic-reporting.md#Configuration) من [مكتبة الأصول المشتركة](../lifecycle-services/asset-library.md) في Microsoft Dynamics Lifecycle Services (LCS).

> [!IMPORTANT]
> إن استخدام LCS كمستودع تخزين لتكوينات التقارير الإلكترونية يكون [مهملاً](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). لمزيد من المعلومات، [إهلاك تخزين Regulatory Configuration Service (RCS) – Lifecycle Services (LCS)](../../../finance/localizations/rcs-lcs-repo-dep-faq.md)

1. سجّل دخولك إلى التطبيق باستخدام أحد الأدوار التالية:

    - مطور إعداد التقارير الإلكتروني
    - مستشار وظيفي لإعداد التقارير الإلكتروني
    - مسؤول النظام

2. انتقل إلى **إدارة المؤسسة** &gt; **مساحات العمل** &gt; **التقارير الإلكترونية**.
3. في مقطع **موفرو التكوين**، حدد لوحة **Microsoft**.
4. على لوحة **Microsoft**، حدد **مستودعات**.

    [![لوحة Microsoft في صفحة تكوينات الترجمة](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. في صفحة **مستودعات التكوين**، في الشبكة، حدد المستودع الموجود من النوع **LCS**. إذا لم يظهر هذا المستودع في الشبكة، فاتبع الخطوات التالية:

    1. حدد **إضافة** لإضافة مستودع.
    2. حدد **LCS** كنوع المستودع.
    3. حدد **إنشاء مستودع**.
    4. إذا تمت مطالبتك بالتخويل، فاتبع الإرشادات التي تظهر على الشاشة.
    5. قم بإدخال اسم ووصف للمستودع.
    6. حدد **موافق** لتأكيد إدخال المستودع الجديد.
    7. في الشبكة، حدد المستودع الجديد من النوع **LCS‎**.

6. حدد **فتح** لعرض قائمة تكوينات التقارير الإلكترونية للمستودع المحدد.

    [![صفحة مستودعات التكوين](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > إذا واجهت مشكلة في الوصول إلى مستودع LCS لتنزيل التكوينات من مكتبة الأصول المشتركة في LCS، فيمكنك تنزيل التكوينات من [المستودع العمومي](er-download-configurations-global-repo.md) بدلاً من ذلك.

7. في شجرة التكوينات في الجزء الأيمن، حدد تكوين التقارير الإلكترونية المطلوب.
8. على علامة التبويب السريعة **إصدارات**، حدد الإصدار المطلوب لتكوين التقارير الإلكترونية المحدد.
9. حدد **استيراد** لتنزيل الإصدار المحدد من LCS إلى المثيل الحالي.

    > [!NOTE]
    > لا يتوفر الزر **استيراد** لإصدارات تكوينات التقارير الإلكترونية الموجودة في المثيل الحالي.

    [![صفحة مستودع التكوين](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> استنادًا إلى إعدادات التقارير الإلكترونية، يتم التحقق من صحة التكوينات بعد استيرادها. قد يتم إعلامك بأي مشكلات عدم التوافق التي يتم اكتشافها. يجب حل هذه المشكلات قبل أن تتمكن من استخدام إصدار التكوين المستورد. لمزيد من المعلومات، راجع قائمة المواضيع ذات الصلة لهذا الموضوع.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md)

[تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي لخدمة التكوين](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
