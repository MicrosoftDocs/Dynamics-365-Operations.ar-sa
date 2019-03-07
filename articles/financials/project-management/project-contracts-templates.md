---
title: مزامنة عقود المشاريع والمشاريع مباشرةً من Project Service Automation إلى Finance and Operations
description: يصف هذا الموضوع القالب والمهام الأساسية التي يتم استخدامها لمزامنة مهام المشاريع وعقود المشاريع مباشرة من Microsoft Dynamics 365 for Project Service Automation إلى Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0889bc233674cb80dd056ac77edb5c936c6633a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "312107"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>مزامنة عقود المشاريع والمشاريع مباشرةً من Project Service Automation إلى Finance and Operations

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القالب والمهام الأساسية التي يتم استخدامها لمزامنة مهام المشاريع وعقود المشاريع مباشرة من Microsoft Dynamics 365 for Project Service Automation إلى Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE] 
> إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0، فيجب تثبيت KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>تدفق البيانات الخاصة بـ Project Service Automation إلى Finance and Operations

> [!NOTE]
> قبل أن تتمكن من استخدام حل تكامل Project Service Automation مع Finance and Operations، يجب أن تكون ملمًا بميزة تكامل البيانات في Microsoft Dynamics 365.

يستخدم الحل المتكامل لـ Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations يُتيح تكامل القالب المتوفر مع ميزة تكامل البيانات تدفق البيانات حول عقود المشروعات والمشروعات وبنود عقود المشروعات والنقاط الهامة لبنود عقود المشروعات من Project Service Automation إلى Finance and Operations.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.

[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft PowerApps، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

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
| الأوامر                           | كيان تكامل عقد المشروع                |
| المشاريع                         | كيان تكامل المشروع                         |
| سطور الأمر                      | كيان تكامل بنود عقد المشروع           |
| المراحل الرئيسية لبنود عقد المشروع | كيان تكامل النقاط الهامة لبنود عقد المشروع |

## <a name="entity-flow"></a>تدفق الكيان

تتم إدارة عقود المشروعات في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كعقود مشروعات. كجزء من تكامل القالب، يمكنك تعيين مصدر التكامل في Finance and Operations لعقود المشروعات.

تتم إدارة مشروع الوقت والمواد والمشروعات ثابتة الأسعار في Project Service Automation، وتتم مزامنتها إلى Finance and Operations كمشاريع. كجزء من تكامل القالب، يمكنك تعيين مصدر التكامل في Finance and Operations للمشروع.

تتم إدارة بنود عقود المشروعات في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كقواعد فوترة عقود مشروعات. إذا كانت طريقة الفوترة مختلفة عن نوع المشروع الافتراضي، سوف تقوم المزامنة بتحديث نوع المشروع لمشروع بند العقد ومجموعة المشاريع.

تتم إدارة المراحل الرئيسية لبنود عقود المشروعات في Project Service Automation، وتتم مزامنتها إلى Finance and Operations كمراحل رئيسية لقواعد فوترة عقود المشروعات.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>حل تكامل Project Service Automation إلى Finance and Operations

يتوفر حقل **مُعرف عقد المشروع** في صفحة **عقود المشروع** . أنشأ هذا الحقل مفتاح طبيعي وفريد لدعم التكامل.

عند إنشاء حساب جديد، إذا لم تكن قيمة **مُعرف عقد المشروع** موجودة مسبقًا، فسيتم إنشاؤها تلقائيًا باستخدام تسلسل رقمي. تتكون القيمة من **ORD** ، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف. وفيما يلي مثال على ذلك: **ORD-01022-Z4M9Q0**.

يتوفر حقل **رقم المشروع** في صفحة **المشاريع**. أنشأ هذا الحقل مفتاح طبيعي وفريد لدعم التكامل.

عند إنشاء مشروع جديد، إذا لم تكن قيمة **رقم المشروع** موجودة مسبقًا، فسيتم إنشاؤها تلقائيًا باستخدام تسلسل رقمي. تتكون القيمة من **PRJ** ، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف. وفيما يلي مثال على ذلك: **PRJ-01049-CCNID0**.

عند تطبيق حل تكامل Project Service Automation إلى Finance and Operations integration <TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution> ، يقوم برنامج نصي للترقية بتعيين حقل **مُعرف عقد المشروع** لعقود المشروعات الحالية وحقل **رقم المشروع** للمشاريع الموجودة في Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

- قبل القيام بمزامنة عقود المشاريع والمشروعات، يجب عليك مزامنة الحسابات.
- في مجموعة الاتصال الخاصة بك، قم بإضافة تعيين حقل مفتاح التكامل لـ **msdyn\_‎organizationalunits** إلى **msdyn\_ name\[Name\]**. قد تحتاج أولًا إلى إضافة مشروع إلى مجموعة الاتصال. للحصول على مزيد من المعلومات، راجع [دمج البيانات في Common Data Service للتطبيقات](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- في مجموعة الاتصال الخاصة بك، قم بإضافة تعيين حقل مفتاح التكامل لـ **msdyn\_‎projects‎** إلى **msdyn\_ projectnumber\[Project Number\]**. قد تحتاج أولًا إلى إضافة مشروع إلى مجموعة الاتصال. للحصول على مزيد من المعلومات، راجع [دمج البيانات في Common Data Service للتطبيقات](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- **SourceDataID** لعقود المشاريع والمشاريع يمكن تحديثه إلى قيمة مختلفة أو إزالته من التعيين. قيمة القالب الافتراضي هي **Project Service Automation**.
- يجب تحديث **PaymentTerms** بحيث يعكس شروط الدفع الصالحة في Finance and Operations. يمكنك أيضًا إزالة التعيين من مهمة المشروع. يحتوي تعيين القيمة الافتراضية على قيم افتراضية لبيانات عرض توضيحي. يعرض الجدول التالي القيم في Project Service Automation.

    | القيمة | الوصف   |
    |-------|---------------|
    | 1     | صافي 30        |
    | 2     | ‏‫2%10، صافي 30 |
    | 3     | صافي 45        |
    | 4     | صافي 60        |

## <a name="power-query"></a>Power Query

يجب عليك استخدام Microsoft Power Query لـ Excel لتصفية البيانات في حالة تحققت الشروط التالية:

- لديك أوامر مبيعات في Microsoft Dynamics 365 for Sales.
- لديك العديد من الوحدات التنظيمية في Project Service Automation، وسوف يتم تعيين هذه الوحدات التنظيمية إلى كيانات قانونية متعددة في Finance and Operations.

إذا كنت مضطرًا إلى استخدام Power Query، اتبع هذه الإرشادات:

- يتضمن قالب المشاريع والعقود (PSA إلى Fin and Ops) عامل تصفية افتراضيًا يتضمن أوامر مبيعات من النوع **عنصر العمل (msdyn\_ordertype = 192350001)**. يساعد عامل التصفية هذا على ضمان عدم إنشاء عقود المشروعات لأوامر المبيعات في Finance and Operations. إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا.
- يجب عليك إنشاء عامل تصفية Power Query الذي يتضمن فقط مؤسسات العقود التي ينبغي مزامنتها مع الكيان القانوني لمجموعة اتصال التكامل. على سبيل المثال، يجب مزامنة عقود المشاريع التي قمت بإنشائها باستخدام وحدة Contoso US التنظيمية للعقود مع الكيان القانوني USSI، ولكن ينبغي مزامنة عقود المشاريع التي قمت بإنشائها باستخدام وحدة Contoso Global التنظيمية للعقود مع الكيان القانوني USMF. إذا لم تُضف عامل التصفية هذا إلى تعيين المهمة الخاص بك، فسوف تتم مزامنة جميع عقود المشاريع مع الكيان القانوني المُحدد لمجموعة الاتصال، بغض النظر عن الوحدة التنظيمية للعقد.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

> [!NOTE] 
> لا يتم تضمين الحقول **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, و **AddressZipCode** في التعيين الافتراضي لعقود المشاريع. يمكنك إضافة التعيينات إذا رغبت في مزامنة هذه البيانات لعقود المشاريع.
>
> لا يتم تضمين الحقول **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, و **ProjectType** في التعيين الافتراضي للمشاريع. يمكنك إضافة التعيينات إذا رغبت في مزامنة هذه البيانات للمشاريع.

يبين الشكل التوضيحي التالي أمثلة لتعيينات مهام القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![تعيين القالب](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![تعيين القالب](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![تعيين القالب](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)
