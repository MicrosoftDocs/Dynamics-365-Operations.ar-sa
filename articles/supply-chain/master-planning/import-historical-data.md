---
title: استيراد البيانات التاريخية‬ للتنبؤات بالطلب
description: للحصول على تنبؤات بالطلب‬ دقيقة، تحتاج إلى بيانات تاريخية لكل صنف أو مفتاح توزيع الصنف. يشرح هذا الموضوع كيفية استخدام كيانات البيانات لاستيراد بيانات الطلب التاريخية من أي نظام، بحيث تحصل على سجل طويل لبيانات التنبؤات بالطلب.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6ba2e1a3a884d29bff491f914aa2d5f9ece2b84
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154217"
---
# <a name="import-historical-data-for-demand-forecasts"></a>استيراد البيانات التاريخية‬ للتنبؤات بالطلب

[!include [banner](../includes/banner.md)]

للمساعدة في ضمان دقة التنبؤات بالطلب، يجب أن تكون بيانات الطلب التاريخية لديك بمقدار مماثل لما يمكنك الحصول عليه لكل صنف أو مفتاح توزيع الصنف. إذا لم يكن قد تم بعد استيراد بيانات الطلب التاريخية، فاستخدم كيان البيانات **الطلب الخارجي التاريخي‬** (ReqDemPlanHistoricalExternalDemandEntity) في Dynamics 365 Supply Chain Management لاستيرادها.

في مساحة العمل **إدارة البيانات**، يمكنك الاطلاع على نظرة عامة على كافة الحقول الموجودة في الكيان.

1. افتح مساحة العمل **إدارة البيانات**.
2. حدد لوحة **كيانات البيانات**.
3. ابحث في قائمة الكيانات عن **الطلب الخارجي التاريخي**.
4. حدد **الحقول المستهدفة**. تُعتبر حقول الكيانات التالية إلزامية: الموقع (**DeliveringSiteId**)، والتاريخ (**DemandDate**) والكمية، (**DemandQuantity**)، وإما رقم الصنف (**ItemNumber**) أو مفتاح توزيع الصنف (**ProductAllocationKeyId**).

لاستخدام كيان البيانات، يجب أن يكون لديك ملف Microsoft Excel أو ملف قيم تفصلها الفواصل (CSV) يحتوي على بيانات الطلب التاريخية. يوضح المثال التالي كيفية استيراد البيانات من ملف CSV.

لمزيد من المعلومات حول كيفيه استيراد البيانات، بما في ذلك كيفيه تنظيف البيانات بعد الاستيراد، راجع [نظره عامه حول استيراد البيانات](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)وتصديرها وموضوعاتها ذات صله.

## <a name="example"></a>مثال

يمكن استخدام الملف التالي كمثال. قم بتنزيل [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/). يحتوي هذا الملف على بيانات الطلب التاريخية للصنف D0001. إنه يحتوي على الحقول الإلزامية التالية فقط: الموقع والكمية وتاريخ الطلب.

1. حدد الشركة لاستيراد بيانات الطلب التاريخية إليها.
2. افتح مساحة العمل **إدارة البيانات**.
3. تحديد تجانب **الاستيراد**.
4. أدخل اسمًا لمشروع الاستيراد، مثل **استيراد الطلب التاريخي للصنف D0001**.
5. في الحقل **تنسيق بيانات المصدر** ، حدد تنسيق الملف للملف الذي تريد استيراده. لاستيراد الملف HistoricalDemandData لهذا المثال، حدد **CSV**.
6. في الحقل **اسم الكيان**، حدد **الطلب الخارجي التاريخي‬**.
7. احفظ الملف في الكمبيوتر، ثم قم بتحميله.
8. حدد **استيراد**.
9. تفتح صفحة **ملخص التنفيذ** بشكل تلقائي. تحقق من صحة البيانات التي تم استيرادها في الصفحة.

بعد استيراد بيانات الطلب التاريخية، يمكنك إنشاء تنبؤ بالطلب.

## <a name="additional-resources"></a>الموارد الإضافية

[إنشاء تنبؤ أساسي إحصائي](generate-statistical-baseline-forecast.md)  
[نظرة عامة حول مهام استيراد البيانات وتصديرها](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]