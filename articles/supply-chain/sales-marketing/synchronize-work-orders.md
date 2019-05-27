---
title: مزامنة أوامر العمل مع مشروع من Field Service إلى Finance and Operations
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536723"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>مزامنة أوامر العمل مع مشروع من Field Service إلى Finance and Operations

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

يستند قالب **أوامر العمل مع المشروع ‏(Field Service إلى Fin and Ops)** إلى قالب **أوامر العمل (Field Service إلى Fin and Ops)**. لمزيد من المعلومات، راجع [مزامنة أوامر العمل في Field Service إلى أوامر المبيعات في Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

يصف هذا الموضوع الاختلافات بين القالبين فقط:
- **أوامر العمل مع المشروع (Field Service إلى Fin and Ops)**
- **أوامر العمل (Field Service إلى Fin and Ops)**

الفارق الأساسي هو أن هذا القالب يتضمن تعيين رقم المشروع المعين إلى أمر العمل في Field Service، مما يضمن أن أمر المبيعات المنشأ في Finance and Operations يتضمن رقم المشروع وأنه بإمكان الفوترة أن تحدث على المشروع ذي الصلة. بالإضافة إلى ذلك، يستخدم القالب وظائف الاستعلام والتصفية المتقدمة.

## <a name="templates-and-tasks"></a>القوالب والمهام

**اسم القالب في تكامل البيانات:**

- أوامر العمل مع المشروع (Field Service إلى Fin and Ops)

**اسم المهمة في مشروع تكامل البيانات:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>حل Field Service CRM
تمت إضافة حقل **المشروع الخارجي** إلى كيان "أمر العمل". هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Finance and Operations. عندما تتغير **حالة النظام** من مفتوح - قيد التقديم(690,970,000) إلى حالة أعلى، سيتم تأمين حقل **المشروع الخارجي** ولا يمكنك إضافة القيمة أو إزالتها أو تغييرها.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderHeader

[![تعيين القالب في تكامل البيانات](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderHeaderProject

[![تعيين القالب في تكامل البيانات](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderProduct

[![تعيين القالب في تكامل البيانات](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderService

[![تعيين القالب في تكامل البيانات](./media/FSWOP4.png)](./media/FSWOP4.png)
