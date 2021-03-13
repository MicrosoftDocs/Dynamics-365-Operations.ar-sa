---
title: مزامنة أوامر العمل مع المشروع من Field Service إلى Supply Chain Management
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Dynamics 365 Field Service إلى Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 3ee512c2814b45a0bf35d1bee718b1ce37867bbb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010788"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>مزامنة أوامر العمل مع المشروع من Field Service إلى Supply Chain Management

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Dynamics 365 Field Service إلى Dynamics 365 Supply Chain Management.

[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

يستند قالب **أوامر العمل مع المشروع ‏(Field Service إلى Supply Chain Management)** إلى قالب **أوامر العمل (Field Service إلى Supply Chain Management)**. لمزيد من المعلومات، راجع [مزامنة أوامر العمل في Field Service إلى أوامر المبيعات في Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

يصف هذا الموضوع الاختلافات بين القالبين فقط:
- **أوامر العمل مع المشروع (Field Service إلى Supply Chain Management)**
- **أوامر العمل (Field Service إلى Supply Chain Management)**

الفارق الأساسي هو أن هذا القالب يتضمن تعيين رقم المشروع المعين إلى أمر العمل في Field Service، مما يضمن أن أمر المبيعات المنشأ في Supply Chain Management يتضمن رقم المشروع وأنه بإمكان الفوترة أن تحدث على المشروع ذي الصلة. بالإضافة إلى ذلك، يستخدم القالب وظائف الاستعلام والتصفية المتقدمة.

## <a name="templates-and-tasks"></a>القوالب والمهام

**اسم القالب في تكامل البيانات:**

- أوامر العمل مع المشروع (Field Service إلى Supply Chain Management)

**اسم المهمة في مشروع تكامل البيانات:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>حل Field Service CRM
تمت إضافة حقل **المشروع الخارجي** إلى كيان "أمر العمل". هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Supply Chain Management. عندما تتغير **حالة النظام** من مفتوح - قيد التقديم(690,970,000) إلى حالة أعلى، سيتم تأمين حقل **المشروع الخارجي** ولا يمكنك إضافة القيمة أو إزالتها أو تغييرها.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>أوامر العمل مع المشروع (Field Service إلى ‎Supply Chain Management)‎:‎‎ ‎‎WorkOrderHeader‎

[![تعيين القالب في تكامل البيانات](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>أوامر العمل مع المشروع (Field Service إلى Supply Chain Management): WorkOrderHeaderProject

[![تعيين القالب في تكامل البيانات](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>أوامر العمل مع المشروع (Field Service إلى Supply Chain Management): WorkOrderProduct

[![تعيين القالب في تكامل البيانات](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>أوامر العمل مع المشروع (Field Service إلى Supply Chain Management): WorkOrderService

[![تعيين القالب في تكامل البيانات](./media/FSWOP4.png)](./media/FSWOP4.png)
