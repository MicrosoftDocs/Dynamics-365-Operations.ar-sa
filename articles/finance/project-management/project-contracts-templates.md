---
title: مزامنة عقود المشاريع والمشاريع مباشرةً من Project Service Automation إلى Finance and Operations
description: يصف هذا الموضوع القالب والمهام الأساسية التي يتم استخدامها لمزامنة مهام المشاريع وعقود المشاريع مباشرة من Dynamics 365 Project Service Automation Microsoft إلى Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b44fc116f1dcaa1275b2262487ef9114bce639c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773844"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>مزامنة عقود المشاريع والمشاريع مباشرةً من Project Service Automation إلى Finance and Operations

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القالب والمهام الأساسية التي يتم استخدامها لمزامنة مهام المشاريع وعقود المشاريع مباشرة من Dynamics 365 Project Service Automation إلى Dynamics 365 Finance.

> [!NOTE] 
> إذا كنت تستخدم , Enterprise edition 7.3.0، فيجب تثبيت قاعدة المعارف 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>تدفق البيانات الخاصة بـ Project Service Automation إلى Finance

> [!NOTE]
> قبل أن تتمكن من استخدام حل تكامل Project Service Automation مع Finance، يجب أن تكون ملمًا بميزة تكامل البيانات في Dynamics 365.

يستخدم الحل المتكامل لـ Project Service Automation إلى Finance ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation وFinance يُتيح تكامل القالب المتوفر مع ميزة تكامل البيانات تدفق البيانات حول عقود المشروعات والمشروعات وبنود عقود المشروعات والنقاط الهامة لبنود عقود المشروعات من Project Service Automation إلى Finance.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance.

[![تدفق البيانات الخاصة بتكامل Project Service Automation مع Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft Power Apps، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القوالب والمهام الأساسية التالية لمزامنة عقود المشروعات والمشروعات من Project Service Automation إلى Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>التكامل مع Dynamics 365 Project Service Automation v2.x
- **اسم القالب في تكامل البيانات:** المشروعات والعقود (PSA إلى Fin and Ops)
- **أسماء المهام في المشروع:**

    - عقود مشاريع PSA إلى Fin and Ops
    - مشروعات PSA إلى Fin and Ops
    - بنود عقود مشاريع PSA إلى Fin and Ops
    - المراحل الرئيسية لبنود عقود مشاريع PSA إلى Fin and Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>التكامل مع Dynamics 365 Project Service Automation v3.x
هناك تغيير في المخطط في Project Service Automation يؤثر على القالب الرئيسي لبنود عقد المشروع واستخدام الإصدار v2 من القالب مطلوب لدمج Project Service Automation v3.x مع Dynamics 365.

- **اسم القالب في تكامل البيانات:** المشروعات والعقود (PSA 3.x إلى Fin and Ops)‏ - v2
- **أسماء المهام في المشروع:**

    - عقود مشاريع PSA إلى Fin and Ops
    - مشروعات PSA إلى Fin and Ops
    - بنود عقود مشاريع PSA إلى Fin and Ops
    - المراحل الرئيسية لبنود عقود مشاريع PSA إلى Fin and Ops

قبل القيام بمزامنة عقود المشاريع والمشروعات، يجب عليك مزامنة الحسابات.

## <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation       | المالية                                                |
|----------------------------------|--------------------------------------------------------|
| الأوامر                           | كيان تكامل عقد المشروع                |
| المشاريع                         | كيان تكامل المشروع                         |
| سطور الأمر                      | كيان تكامل بنود عقد المشروع           |
| المراحل الرئيسية لبنود عقد المشروع | كيان تكامل النقاط الهامة لبنود عقد المشروع |

## <a name="entity-flow"></a>تدفق الكيان

تتم إدارة عقود المشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance كعقود المشروع. كجزء من تكامل القالب، يمكنك تعيين مصدر التكامل في Finance لعقود المشروع.

تتم إدارة مشروع الوقت والمواد والمشروعات ثابتة الأسعار في Project Service Automation، وتتم مزامنتها إلى Finance كمشاريع. كجزء من تكامل القالب، يمكنك تعيين مصدر التكامل في Finance للمشروع.

تتم إدارة بنود عقود المشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance كقواعد فوترة عقد المشروع. إذا كانت طريقة الفوترة مختلفة عن نوع المشروع الافتراضي، سوف تقوم المزامنة بتحديث نوع المشروع لمشروع بند العقد ومجموعة المشاريع.

تتم إدارة المراحل الرئيسية لبنود عقد المشروع في Project Service Automation، وتتم مزامنتها إلى Finance كمراحل رئيسية لقواعد فوترة عقد المشروع.

## <a name="project-service-automation-to-finance-integration-solution"></a>حل تكامل Project Service Automation إلى Finance

يتوفر حقل **مُعرف عقد المشروع** في صفحة **عقود المشروع** . أنشأ هذا الحقل مفتاح طبيعي وفريد لدعم التكامل.

عند إنشاء حساب جديد، إذا لم تكن قيمة **مُعرف عقد المشروع** موجودة مسبقًا، فسيتم إنشاؤها تلقائيًا باستخدام تسلسل رقمي. تتكون القيمة من **ORD**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف. وفيما يلي مثال على ذلك: **ORD-01022-Z4M9Q0**.

يتوفر حقل **رقم المشروع** في صفحة **المشاريع**. أنشأ هذا الحقل مفتاح طبيعي وفريد لدعم التكامل.

عند إنشاء مشروع جديد، إذا لم تكن قيمة **رقم المشروع** موجودة مسبقًا، فسيتم إنشاؤها تلقائيًا باستخدام تسلسل رقمي. تتكون القيمة من **PRJ**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف. وفيما يلي مثال على ذلك: **PRJ-01049-CCNID0**.

عند تطبيق حل تكامل Project Service Automation إلى حل تكامل Finance، يقوم برنامج نصي للترقية بتعيين حقل **مُعرف عقد المشروع** لعقود المشروعات الحالية وحقل **رقم المشروع** للمشاريع الموجودة في Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

- قبل القيام بمزامنة عقود المشاريع والمشروعات، يجب عليك مزامنة الحسابات.
- في مجموعة الاتصال الخاصة بك، قم بإضافة تعيين حقل مفتاح التكامل لـ **msdyn\_‎organizationalunits** إلى **msdyn\_ name\[Name\]**. قد تحتاج أولًا إلى إضافة مشروع إلى مجموعة الاتصال. للحصول على مزيد من المعلومات، راجع [دمج البيانات في Common Data Service للتطبيقات](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- في مجموعة الاتصال الخاصة بك، قم بإضافة تعيين حقل مفتاح التكامل لـ **msdyn\_‎projects‎** إلى **msdyn\_ projectnumber\[Project Number\]**. قد تحتاج أولًا إلى إضافة مشروع إلى مجموعة الاتصال. للحصول على مزيد من المعلومات، راجع [دمج البيانات في Common Data Service للتطبيقات](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** لعقود المشاريع والمشاريع يمكن تحديثه إلى قيمة مختلفة أو إزالته من التعيين. قيمة القالب الافتراضي هي **Project Service Automation**.
- يجب تحديث **PaymentTerms** بحيث يعكس شروط الدفع الصالحة في Finance. يمكنك أيضًا إزالة التعيين من مهمة المشروع. يحتوي تعيين القيمة الافتراضية على قيم افتراضية لبيانات عرض توضيحي. يعرض الجدول التالي القيم في Project Service Automation.

    | القيمة | الوصف   |
    |-------|---------------|
    | 1     | صافي 30        |
    | 2     | 2% 10، صافي 30 |
    | 3     | صافي 45        |
    | 4     | صافي 60        |

## <a name="power-query"></a>Power Query

يجب عليك استخدام Microsoft Power Query لـ Excel لتصفية البيانات في حالة تحققت الشروط التالية:

- لديك أوامر مبيعات في Dynamics 365 Sales.
- لديك العديد من الوحدات التنظيمية في Project Service Automation، وسوف يتم تعيين هذه الوحدات التنظيمية إلى كيانات قانونية متعددة في Finance.

إذا كنت مضطرًا إلى استخدام Power Query، اتبع هذه الإرشادات:

- يتضمن قالب المشاريع والعقود (PSA إلى Fin and Ops) عامل تصفية افتراضيًا يتضمن أوامر مبيعات من النوع **عنصر العمل (msdyn\_ordertype = 192350001)**. يساعد عامل التصفية هذا على ضمان عدم إنشاء عقود المشروعات لأوامر المبيعات في Finance. إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا.
- يجب عليك إنشاء عامل تصفية Power Query الذي يتضمن فقط مؤسسات العقود التي ينبغي مزامنتها مع الكيان القانوني لمجموعة اتصال التكامل. على سبيل المثال، يجب مزامنة عقود المشاريع التي قمت بإنشائها باستخدام وحدة Contoso US التنظيمية للعقود مع الكيان القانوني USSI، ولكن ينبغي مزامنة عقود المشاريع التي قمت بإنشائها باستخدام وحدة Contoso Global التنظيمية للعقود مع الكيان القانوني USMF. إذا لم تُضف عامل التصفية هذا إلى تعيين المهمة الخاص بك، فسوف تتم مزامنة جميع عقود المشاريع مع الكيان القانوني المُحدد لمجموعة الاتصال، بغض النظر عن الوحدة التنظيمية للعقد.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

> [!NOTE] 
> لا يتم تضمين الحقول **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, و **AddressZipCode** في التعيين الافتراضي لعقود المشاريع. يمكنك إضافة التعيينات إذا رغبت في مزامنة هذه البيانات لعقود المشاريع.
>
> لا يتم تضمين الحقول **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, و **ProjectType** في التعيين الافتراضي للمشاريع. يمكنك إضافة التعيينات إذا رغبت في مزامنة هذه البيانات للمشاريع.

يبين الشكل التوضيحي التالي أمثلة لتعيينات مهام القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance.

[![تعيين القالب](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![تعيين القالب](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![تعيين القالب](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![تعيين القالب](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>تعيين الحدث الرئيسي لبنود عقد المشروع في قالب المشاريع والعقود (PSA 3.x to Dynamics) - v2:

[![تعيين القالب](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
