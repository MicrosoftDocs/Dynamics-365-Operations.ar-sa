---
title: استيراد البيانات التاريخية‬ للتنبؤات بالطلب
description: للحصول على تنبؤات بالطلب‬ دقيقة، تحتاج إلى بيانات تاريخية لكل صنف أو مفتاح توزيع الصنف. يشرح هذا الموضوع كيفية استخدام كيانات البيانات لاستيراد بيانات الطلب التاريخية من أي نظام، بحيث تحصل على سجل طويل لبيانات التنبؤات بالطلب.
author: ChristianRytt
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6dba31279541c20949dd1e86236103045c48b701
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579654"
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

انظر أيضًا [إنشاء تنبؤ أساسي إحصائي](generate-statistical-baseline-forecast.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]