---
title: الصفحة الرئيسية لإدارة التكلفة
description: تسمح لك إدارة التكلفة بالتعامل مع تقييم وحساب المواد الخام والسلع شبه النهائية والسلع النهائية وأصول العمل قيد التقدم‬.
author: AndersGirke
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd94ae4c5ea855139fd1c41060de7db455ffab06
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "333934"
---
# <a name="cost-management-home-page"></a>الصفحة الرئيسية لإدارة التكلفة

[!include [banner](../includes/banner.md)]

[تسمح لك إدارة التكلفة (فيديو)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be) بالتعامل مع تقييم وحساب المواد الخام والسلع شبه النهائية والسلع النهائية وأصول العمل قيد التقدم‬. إنها عملية تحديد وإدارة وإعداد تقارير حول [محاسبة المخزون](cost-object.md) و[محاسبة التصنيع](bom-calculations.md).

يمكن تحديد سياسات التكلفة في النواحي التالية: 
-  [التكلفة المحددة مسبقًا](costing-versions.md)
-  [محاسبة المخزون](cost-object.md)
-  [محاسبة التصنيع](bom-calculations.md)
-  [محاسبة التكلفة غير المباشرة](costing-sheets.md)
-  [تكامل دفتر الأستاذ](production-order-cost-analysis.md)

على سبيل المثال، يمكنك تحديد أي من أساليب تقييم المخزون، مثل [FIFO](fifo-physical-value-marking.md)، أو [المتوسط المرجح‬](weighted-average-physical-value-marking.md)، أو [التكلفة القياسية‬](prerequisites-standard-costs.md)، أو [المتوسط المتحرك‬](moving-average.md) الذي تريد تطبيقه على المنتجات في [مجموعة نماذج الصنف‬](../inventory/reserve-inventory-quantities.md) في محاسبة المخزون.

يمكنك الوصول إلى محاسبة المخزون ومحاسبة التصنيع من مساحتي العمل **إدارة التكلفة** و**تحليل التكلفة**. توفر مساحات العمل هذه نظرة عامة شاملة حول الحالة الحالية ومؤشرات الأداء الرئيسية (KPI) ز الكشف عن الانحرافات. 

تسمح لك محاسبة التصنيع بالتعامل مع [تحديد تكلفة أمر الشغل](production-order-cost-analysis.md) في أوامر الإنتاج والأوامر الدفعية، بالإضافة إلى [تحديد تكاليف الإصدار التلقائي](backflush-costing.md) في Lean Manufacturing.

يوفر [محتوى "إدارة التكلفة" في Power BI](../../dev-itpro/analytics/cost-management-content-pack.md) رؤية إدارية داخل المخزون ومخزون العمل قيد التقدم، وكيفية تدفق التكلفة من خلالهما حسب الفئة مع مرور الوقت. يمكن استخدام المعلومات أيضًا بوصفها تكملة تفصيلية للقائمة المالية.

### <a name="additional-resources"></a>الموارد الإضافية

#### <a name="whats-new-and-in-development"></a>ما الجديد وقيد التطوير

انتقل إلى [خارطة طريق Microsoft Dynamics 365](https://roadmap.dynamics.com/) للاطلاع على الميزات الجديدة التي تم إصدارها والميزات الجديدة قيد التطوير. 

#### <a name="white-paper"></a>مستند تقني
يصف المستند التقني [حساب قائمة مكونات الصنف باستخدام كشف التكاليف](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/white-papers/365operationsbomcalsheet) كيفية إعداد كشف تكاليف يتضمن التصنيع والمواد، ومدى تأثير الإعداد على نتائج حساب قائمة مكونات الصنف. وهو يوفر وحدات سيناريو ملموسة بالإضافة إلى بيانات تُظهر تأثير مختلف الإعدادات والتكوينات، من أجل توضيح هذه المواضيع بشكل أفضل. نحن لا نتوقع منك أن تتبع جميع هذه السيناريوهات، لأن هذا المستند لا يوفر تفاصيل كافية لتكوينها. وبالرغم من ذلك، إذا كانت لديك المعلومات الأساسية، فيمكنك محاولة تشغيل دلائل المهام المدرجة أدناه حسب ترتيب ظهورها. استخدم المعرفة التي اكتسبتها من قراءة هذا المستند لإجراء تحليل حساب قائمة مكونات الصنف. 

-  [إنشاء منتج نهائي](tasks/create-finished-product-2016-02.md)
-  [إنشاء منتج غير نهائي](tasks/create-semi-finished-product-2016-02.md)
-  [إنشاء مواد خام‬](tasks/create-raw-materials-2016-02.md)
-  [إنشاء قوائم مكونات الصنف](tasks/create-boms-2016-02.md)
-  [إنشاء مسارات](tasks/create-routes-2016-02.md)
-  [حساب قائمة مكونات الصنف باستخدام هيكل أحادي المستوى](tasks/calculate-bom-single-level-structure-2016-02.md)
-  [حساب قائمة مكونات الصنف باستخدام هيكل متعدد المستويات](tasks/calculate-bom-multilevel-structure-2016-02.md)


#### <a name="blogs"></a>المدونات
يمكنك العثور على آراء وأخبار وغيرها من المعلومات حول إدارة التكلفة في [مدونة فريق بحث وتطوير Dynamics AX Manufacturing R&D](https://blogs.msdn.microsoft.com/axmfg) وفي [إدارة سلسلة التوريد في مدونة فريق بحث وتطوير Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm). على الرغم من أن بعض هذه المنشورات تمت كتابتها للإصدار السابق من إدارة التكلفة، إلا أن المفاهيم نفسها ما زالت تنطبق كما أن الإجراءات مماثلة في الإصدار الحالي.

#### <a name="task-guides"></a>دلائل المهام
تتوفر التعليمات الإضافية كدلائل مهام داخل Finance and Operations. وللوصول إلى دلائل المهام، انقر فوق الزر "تعليمات" في أي صفحة.

