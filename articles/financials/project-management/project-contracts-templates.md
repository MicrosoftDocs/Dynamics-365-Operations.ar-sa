---
title: "مزامنة عقود المشروع من Project Service Automation مباشرة إلى عقود مشروعات Finance and Operations"
description: "يوضح هذا الموضوع القالب والمهام الأساسية التي يتم استخدامها لمزامنة العقود والمشروعات مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 8d8e3268ae8c612bad87c3c6416f223219149ee6
ms.contentlocale: ar-sa
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-contracts-and-projects-from-project-service-automation-directly-to-project-contracts-and-projects-in-finance-and-operations"></a>مزامنة العقود والمشروعات من Project Service Automation مباشرة إلى العقود والمشروعات في Finance and Operations

يوضح هذا الموضوع القالب والمهام الأساسية التي يتم استخدامها لمزامنة العقود والمشروعات مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE] 
> إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations، إصدار Enterprise edition 7.3.0، فيجب عليك تثبيت قاعدة المعارف 4074835.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>تدفق البيانات الخاصة بـ Project Service Automation إلى Finance and Operations

> [!NOTE]
> قبل أن تتمكن من استخدام Project Service Automation إلى حل تكامل Finance and Operations، يجب أن تكون على دراية بميزة تكامل بيانات Dynamics 365.

يستخدم الحل المتكامل لـ Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations يُتيح تكامل القالب المتوفر مع ميزة تكامل البيانات تدفق البيانات حول عقود المشروعات والمشروعات وبنود عقود المشروعات والنقاط الهامة لبنود عقود المشروعات من Project Service Automation إلى Finance and Operations.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.

[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft PowerApps ، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب التالي والمهام الأساسية لمزامنة عقود المشروعات والمشروعات من Project Service Automation إلى Finance and Operations:

- **اسم القالب في تكامل البيانات:** المشروعات والعقود (PSA إلى Fin and Ops)
- **أسماء المهام في المشروع:**

  - عقود مشاريع PSA إلى Fin and Ops
  - مشروعات PSA إلى Fin and Ops
  - بنود عقود مشاريع PSA إلى Fin and Ops
  - المراحل الرئيسية لبنود عقود مشاريع PSA إلى Fin and Ops

قبل القيام بمزامنة عقود المشاريع والمشروعات، يجب عليك مزامنة الحسابات.

## <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| الأوامر                           | كيان تكامل عقد المشروع.                |
| المشاريع                         | كيان تكامل المشروع.                         |
| سطور الأمر                      | كيان تكامل بنود عقد المشروع.          |
| المراحل الرئيسية لبنود عقد المشروع | كيان تكامل النقاط الهامة لبنود عقد المشروع. |

## <a name="entity-flow"></a>تدفق الكيان

تتم إدارة عقود المشروعات في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كعقود مشروعات. كجزء من تكامل القالب، يمكنك تعيين مصدر التكامل في Finance and Operations لعقود المشروعات.

تتم إدارة الوقت والمواد والمشروعات ثابتة الأسعار في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كمشاريع. كجزء من تكامل القالب، يمكنك تعيين مصدر التكامل في Finance and Operations للمشروع.

تتم إدارة بنود عقود المشروعات في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كقواعد فوترة عقود مشروعات. سوف تقوم المزامنة بتحديث نوع المشروع لمشروع بند العقد ومجموعة المشروع إذا كان أسلوب الفوترة مختلف عن نوع المشروع الافتراضي.

تتم إدارة المراحل الرئيسية لبنود عقود المشروعات في Project Service Automation، وتتم مزامنتها إلى Finance and Operations كمراحل رئيسية لقواعد فوترة عقود المشروعات.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>حل تكامل Project Service Automation إلى Finance and Operations

يتوفر حقل **مُعرف عقد المشروع** في صفحة **عقود المشروع** . أنشأ هذا الحقل مفتاح طبيعي وفريد لدعم التكامل.

عند إنشاء حساب جديد، إذا لم تكن قيمة **مُعرف عقد المشروع** موجودة مسبقًا، فسيتم إنشاؤها تلقائيًا باستخدام تسلسل رقمي. تتكون القيمة من **ORD** ، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف. وفيما يلي مثال على ذلك: **ORD-01022-Z4M9Q0**.

يتوفر حقل **رقم المشروع** في صفحة **المشاريع**. أنشأ هذا الحقل مفتاح طبيعي وفريد لدعم التكامل.

عند إنشاء مشروع جديد، إذا لم تكن قيمة **رقم المشروع** موجودة مسبقًا، فسيتم إنشاؤها تلقائيًا باستخدام تسلسل رقمي. تتكون القيمة من **PRJ** ، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف. وفيما يلي مثال على ذلك: **PRJ-01049-CCNID0**.

عند تطبيق حل تكامل Project Service Automation إلى Finance and Operations integration <TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution> ، يقوم برنامج نصي للترقية بتعيين حقل **مُعرف عقد المشروع** لعقود المشروعات الحالية وحقل **رقم المشروع** للمشاريع الموجودة في Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

- قبل القيام بمزامنة عقود المشاريع والمشروعات، يجب عليك مزامنة الحسابات.
- في مجموعة الاتصال الخاصة بك، قم بإضافة تعيين حقل مفتاح التكامل لـ **msdyn\_‎organizationalunits** إلى **msdyn\_ name\[Name\]**. قدتحتاج أولًا إلى إضافة مشروع إلى مجموعة الاتصال. لمزيد من المعلومات حول مفاتيح التكامل، راجع تكامل بيانات Dynamics 365.
- في مجموعة الاتصال الخاصة بك، قم بإضافة تعيين حقل مفتاح التكامل لـ **msdyn\_‎projects‎** إلى **msdyn\_ projectnumber\[Project Number\]**. قدتحتاج أولًا إلى إضافة مشروع إلى مجموعة الاتصال. لمزيد من المعلومات حول مفاتيح التكامل، راجع تكامل بيانات Dynamics 365.
- **SourceDataID** لعقود المشاريع والمشاريع يمكن تحديثه إلى قيمة مختلفة أو إزالته من التعيين. قيمة القالب الافتراضي هي **Project Service Automation**.
- يجب تحديث **PaymentTerms** بحيث يعكس شروط الدفع الصالحة في Finance and Operations. يمكنك أيضًا إزالة التعيين من مهمة المشروع. يحتوي تعيين القيمة الافتراضية على قيم افتراضية لبيانات عرض توضيحي. يعرض الجدول التالي القيم في Project Service Automation.

    | القيمة | الوصف   |
    |-------|---------------|
    | 1     | صافي 30        |
    | 2     | ‏‫2%10، صافي 30 |
    | 3     | صافي 45        |
    | 4     | صافي 60        |

## <a name="power-query"></a>Power Query
يجب عليك استخدام Microsoft Power Query لتصفية البيانات في حالة تحقق الشروط التالية:

- لديك أوامر مبيعات في Microsoft Dynamics 365 for Sales.
- لديك العديد من الوحدات التنظيمية في Project Service Automation، وسوف يتم تعيين هذه الوحدات التنظيمية إلى كيانات قانونية متعددة في Finance and Operations.

إذا كنت مضطرًا إلى استخدام Power Query، اتبع هذه الإرشادات:

- يحتوي قالب عقود المشاريع (PSA إلى Fin and Ops) على عامل تصفية افتراضي يتضمن أوامر مبيعات من النوع **عنصر العمل (msdyn\_ordertype = 192350001)**. يضمن عامل التصفية هذا عدم إنشاء عقود المشروعات لأوامر المبيعات في Finance and Operations. إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا.
- يجب عليك إنشاء عامل تصفية Power Query الذي يتضمن فقط مؤسسات العقود التي ينبغي مزامنتها مع الكيان القانوني لمجموعة اتصال التكامل. على سبيل المثال، يجب مزامنة عقود المشاريع التي قمت بإنشائها باستخدام وحدة Contoso US التنظيمية للعقود مع الكيان القانوني USSI، ولكن ينبغي مزامنة عقود المشاريع التي قمت بإنشائها باستخدام وحدة Contoso Global التنظيمية للعقود مع الكيان القانوني USMF. إذا لم تُضف عامل التصفية هذا إلى تعيين المهمة الخاص بك، فسوف تتم مزامنة جميع عقود المشاريع مع الكيان القانوني المُحدد لمجموعة الاتصال، بغض النظر عن الوحدة التنظيمية للعقد.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

> [!NOTE] 
> لا يتم تضمين الحقول **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, و **AddressZipCode** في التعيين الافتراضي لعقود المشاريع. يمكنك إضافة التعيينات إذا رغبت في مزامنة هذه البيانات لعقود المشاريع.
> لا يتم تضمين الحقول **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, و **ProjectType** في التعيين الافتراضي للمشاريع. يمكنك إضافة التعيينات إذا رغبت في مزامنة هذه البيانات للمشاريع.

يبين الشكل التوضيحي التالي أمثلة لتعيينات مهام القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![تعيين القالب](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![تعيين القالب](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![تعيين القالب](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

