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
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97e84b478b8fd65313d8c3be5c9a50756d8b4924
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213827"
---
# <a name="import-historical-data-for-demand-forecasts"></a>استيراد البيانات التاريخية‬ للتنبؤات بالطلب

[!include [banner](../includes/banner.md)]

للمساعدة في ضمان دقة التنبؤات بالطلب، يجب أن تكون بيانات الطلب التاريخية لديك بمقدار مماثل لما يمكنك الحصول عليه لكل صنف أو مفتاح توزيع الصنف. إذا لم يكن قد تم بعد استيراد بيانات الطلب التاريخية، فاستخدم كيان البيانات **الطلب الخارجي التاريخي‬** (ReqDemPlanHistoricalExternalDemandEntity) في Dynamics 365 Supply Chain Management لاستيرادها.

في مساحة العمل **إدارة البيانات**، يمكنك الاطلاع على نظرة عامة على كافة الحقول الموجودة في الكيان.

1. افتح مساحة العمل **إدارة البيانات**.
2. انقر فوق لوحة **كيانات البيانات**.
3. ابحث في قائمة الكيانات عن **الطلب الخارجي التاريخي**.
4. انقر فوق **الحقول الهدف**. تُعتبر حقول الكيانات التالية إلزامية: الموقع (**DeliveringSiteId**)، والتاريخ (**DemandDate**) والكمية، (**DemandQuantity**)، وإما رقم الصنف (**ItemNumber**) أو مفتاح توزيع الصنف (**ProductAllocationKeyId**).

لاستخدام كيان البيانات، يجب أن يكون لديك ملف Microsoft Excel أو ملف قيم تفصلها الفواصل (CSV) يحتوي على بيانات الطلب التاريخية. يوضح المثال التالي كيفية استيراد البيانات من ملف CSV.

## <a name="example"></a>مثال

يمكن استخدام الملف التالي كمثال. قم بتنزيل [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast). يحتوي هذا الملف على بيانات الطلب التاريخية للصنف D0001. إنه يحتوي على الحقول الإلزامية التالية فقط: الموقع والكمية وتاريخ الطلب.

1. حدد الشركة لاستيراد بيانات الطلب التاريخية إليها.
2. افتح مساحة العمل **إدارة البيانات**.
3. انقر فوق اللوحة **استيراد**.
4. أدخل اسمًا لمشروع الاستيراد، مثل **استيراد الطلب التاريخي للصنف D0001**.
5. في الحقل **تنسيق بيانات المصدر** ، حدد تنسيق الملف للملف الذي تريد استيراده. لاستيراد الملف HistoricalDemandData لهذا المثال، حدد **CSV**.
6. في الحقل **اسم الكيان**، حدد **الطلب الخارجي التاريخي‬**.
7. احفظ الملف في الكمبيوتر، ثم قم بتحميله.
8. انقر فوق **استيراد**.
9. تفتح صفحة **ملخص التنفيذ** بشكل تلقائي. تحقق من صحة البيانات التي تم استيرادها في الصفحة.

بعد استيراد بيانات الطلب التاريخية، يمكنك إنشاء تنبؤ بالطلب.

## <a name="additional-resources"></a>الموارد الإضافية

[إنشاء تنبؤ أساسي إحصائي](generate-statistical-baseline-forecast.md)
