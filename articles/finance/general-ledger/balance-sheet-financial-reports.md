---
title: التقارير المالية للميزانية العمومية
description: توضح هذه المقالة التقارير الافتراضية للميزانيات العمومية. كما تصف العناصر الأساسية التي تقترن بهذه التقارير.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d249172c2bc4241a47502b57f2ac20b29111eeba
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985002"
---
# <a name="balance-sheet-financial-reports"></a>التقارير المالية للميزانية العمومية

[!include [banner](../includes/banner.md)]

توضح هذه المقالة التقارير الافتراضية للميزانيات العمومية. كما تصف العناصر الأساسية التي تقترن بهذه التقارير. 

<a name="default-balance-sheet-reports"></a>تقارير الميزانية العمومية الافتراضية
-----------------------------

هناك تقريران افتراضيان للميزانية العمومية. في تقرير واحد، يتم تكديس الأقسام. وفي التقرير الآخر، تكون الأقسام بجانب بعضها البعض.

| التقرير الافتراضي                       | مهامه                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| كشف الأرصدة - الافتراضي              | يوفر عرضًا للوضع المالي للمؤسسة للسنة.                                                                 |
| الميزانية العمومية جنبًا إلى جنب – الافتراضية | يوفر عرضًا للوضع المالي للمؤسسة للسنة. تظهر الأصول والالتزام وأسهم المساهم جنبًا إلى جنب. |

## <a name="building-blocks"></a>اللبنات الأساسية
تستخدم التقارير المالية للميزانية العمومية اللبنات الأساسية التالية.

| التقرير الافتراضي                       | تعريف الصف                       | تعريف العمود             |
|--------------------------------------|--------------------------------------|-------------------------------|
| الميزانية العمومية - الافتراضية              | الميزانية العمومية - الافتراضية              | السنة حتى تاريخه والفرق - الافتراضي    |
| الميزانية العمومية جنبًا إلى جنب – الافتراضية | الميزانية العمومية جنبًا إلى جنب – الافتراضية | عمود السنة حتى تاريخه - الافتراضي |

### <a name="row-definition"></a>تعريف الصف

تحتوي تعريفات الصف لكلٍّ من تقريري الميزانية العمومية على أقسام لكل جزء في الميزانية العمومية التقليدية. ويتضمن التقرير جنبًا إلى جنب فاصل أعمدة، بحيث يظهر الالتزام وأسهم المالك إلى جانب الأصول. ويتم استخدام بُعد "فئة الحساب الرئيسي" لإنشاء كلٍّ من تعريفي الصف. ولذلك، يمكن لأي شخص إنشاء التقارير دون الحاجة إلى إجراء أي تعديلات.

### <a name="column-definition"></a>تعريف العمود

وتحتوي تعريفات الأعمدة هذه على أنواع مختلفة من الأعمدة لتوفير مستويات مختلفة من التفاصيل والبيانات المالية.

-   **السنة حتى تاريخه والفرق – أنواع الأعمدة الافتراضية:**
    -   **DESC** – الوصف من كل تعريف صف
    -   **FD** – البيانات المالية للسنة حتى تاريخه للسنة الحالية
    -   **FD** – البيانات المالية للسنة حتى تاريخه للسنة الأخيرة
    -   **CALC** – الفرق من طرح العام الماضي من هذا العام

<!-- -->

-   **عمود السنة حتى تاريخه - الافتراضي:**
    -   **DESC** – الوصف من كل تعريف صف
    -   **FD** – البيانات المالية للسنة حتى تاريخه للسنة الحالية



<a name="additional-resources"></a>الموارد الإضافية
--------

[نظرة عامة على التقارير المالية](financial-reporting-getting-started.md)

[عرض التقارير المالية](view-financial-reports.md)

[مدونة التقارير المالية في Dynamics](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]