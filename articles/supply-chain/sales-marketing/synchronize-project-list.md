---
title: مزامنة قائمة المشاريع من Finance and Operations إلى Field Service
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/14/2019
ms.locfileid: "842594"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>مزامنة قائمة المشاريع من Finance and Operations إلى Field Service

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يتم استخدام القالب التالي والمهام الأساسية التالية لتشغيل مزامنة المشاريع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

**قالب في تكامل البيانات**
- المشاريع (Fin and Ops إلى Field Service)

**مهمة في مشروع تكامل البيانات**
- المشاريع

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات قائمة المشاريع:
- الحسابات (Sales إلى Fin and Ops)‬ 

## <a name="entity-set"></a>مجموعة الكيانات
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | المشاريع                |

## <a name="entity-flow"></a>تدفق الكيان
يتم إنشاء المشاريع في Finance and Operations. ستتم مزامنة المشاريع التي تم فيها تعيين **نوع المشروع** إلى **الوقت والمادة** وتعيين **مرحلة المشروع** إلى **قيد التقدم** مع الكيان **مشروع خارجي** في Field Service، بما في ذلك رقم المشروع واسم المشروع ومرحلة المشروع ومعلومات حساب العميل. تُستخدم قائمة **المشروع الخارجي** لإقران أوامر عمل Field service مع مشاريع Finance and Operations.

## <a name="field-service-crm-solution"></a>حل Field Service CRM
يحصل الكيان **مشروع الخارجي** على جميع المشاريع من Finance and Operations. تمت إضافة الحقل **مشروع خارجي** إلى الكيان **أمر عمل**. هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Finance and Operations. عندما تتغير **حالة النظام** من **مفتوح – قيد التقدم(690,970,000)** إلى حالة أعلى، سيتم تأمين الحقل **مشروع خارجي** وسيتعذر عليك إضافة القيمة أو إزالتها أو تغييرها.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين
### <a name="finance-and-operations"></a>Finance and Operations
تمكين تعقب التغييرات لمشاريع كيان البيانات.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات


### <a name="projects-fin-and-ops-to-field-service-projects"></a>المشاريع (Fin and Ops إلى Field Service): المشاريع

[![تعيين القالب في تكامل البيانات](./media/FSProject1.png)](./media/FSProject1.png)
