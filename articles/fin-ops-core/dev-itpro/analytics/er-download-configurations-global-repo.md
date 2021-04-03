---
title: تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي لخدمة التكوين
description: يشرح هذا الموضوع كيفية تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي لخدمة التكوين.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: c4f083163db72569d91825819a904319a0fe3123
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561892"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي لخدمة التكوين

[!include [banner](../includes/banner.md)]

يشرح هذا الموضوع كيفية تنزيل [تكوينات التقارير الإلكترونية](general-electronic-reporting.md#Configuration) من المستودع العمومي لخدمة التكوين. لمزيد من المعلومات، راجع [Microsoft Dynamics 365 for Finance and Operations -‏ Regulatory Services، خدمة التكوين](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>فتح مستودع التكوينات

1. سجّل دخولك إلى تطبيق Dynamics 365 Finance باستخدام أحد الأدوار التالية:

    - مطور إعداد التقارير الإلكتروني
    - مستشار وظيفي لإعداد التقارير الإلكتروني
    - مسؤول النظام

2. انتقل إلى **إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني**‬.
3. في مقطع **موفرو التكوين**، حدد لوحة **Microsoft**.
3. على لوحة **Microsoft**، حدد **مستودعات**.

    ![مساحة عمل إعداد التقارير الإلكترونية](./media/er-download-configurations-global-repo-er-workspace.png)

4. في صفحة **مستودعات التكوين**، في الشبكة، حدد المستودع الموجود من النوع **عمومي**. إذا لم يظهر هذا المستودع في الشبكة، فاتبع الخطوات التالية:

    1. حدد **إضافة** لإضافة مستودع جديد.
    2. حدد **عمومي** كنوع مستودع، ثم حدد **إنشاء مستودع**.
    3. اتبع الإرشادات التخويل، إذا طلب منك ذلك.
    4. أدخل اسمًا ووصفًا للمستودع، ثم حدد **موافق** لتأكيد إدخال المستودع الجديد.
    5. في الشبكة، حدد المستودع الجديد من النوع **عمومي‎**.

5. حدد **فتح** لعرض قائمة تكوينات التقارير الإلكترونية للمستودع المحدد.

    ![صفحة مستودعات التكوين](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>استيراد تكوين واحد

1. في صفحة **مستودعات التكوين**، في شجرة التكوينات، حدد تكوين التقارير الإلكترونية المطلوب.
2. على علامة التبويب السريعة **إصدارات**، حدد الإصدار المطلوب لتكوين التقارير الإلكترونية المحدد.
3. حدد **استيراد** لتنزيل الإصدار المحدد من المستودع العمومي إلى مثيل Finance and Operations الحالي.

    > [!NOTE]
    > لا يتوفر الزر **استيراد** لإصدارات تكوينات التقارير الإلكترونية الموجودة في مثيل Finance الحالي.

    ![صفحة مستودع التكوين](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>استيراد تكوينات تمت تصفيتها

1. في الصفحة **مستودعات التكوين**، في شجره التكوينات، قم بتوسيع علامة التبويب السريعة **عامل التصفية**.
2. في شبكة **العلامات**، أضف أي علامات.
3. في الحقل **إمكانية التطبيق على البلد/المنطقة** حدد رموز البلدان/المنطقة المناسبة، ثم حدد **تطبيق عامل التصفية**.

    > [!NOTE]
    > تعرض علامة التبويب السريعة **التكوينات** جميع التكوينات التي تفي بشروط التحديد المعينة.

4. على علامة التبويب السريعة **التكوينات**، حدد **استيراد** لتنزيل التكوينات التي تمت تصفيتها من المستودع العمومي إلى المثيل الحالي.
5. على علامة التبويب السريعة **التكوينات**، حدد **إعادة تعيين عامل التصفية** لتنظيف شروط التحديد المعينة.

    ![صفحة مستودع التكوين](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> استنادًا إلى إعدادات التقارير الإلكترونية، يتم التحقق من صحة التكوينات بعد استيرادها. قد يتم إعلامك بأي مشكلات عدم التوافق التي يتم اكتشافها. قبل أن تتمكن من استخدام إصدار التكوين المستورد، يجب حل المشاكل. لمزيد من المعلومات، راجع قائمة الموارد ذات الصلة لهذا الموضوع.

> [!NOTE]
> يمكن تكوين تكوينات التقارير الإلكترونية على أنها تعتمد على تكوينات أخرى. وبالتالي، قد يتم استيراد تكوينات أخرى، إلى جانب تكوين محدد، بشكل تلقائي. لمزيد من المعلومات حول تبعيات التكوين، راجع [تحديد تبعية تكوينات التقارير الإلكترونية (ER) على مكونات أخرى‬](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]