---
title: "مزامنة قائمة المشاريع من Finance and Operations إلى Field Service"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: ar-sa
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>مزامنة قائمة المشاريع من Finance and Operations إلى Field Service

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يُستخدم القالب التالي والمهام الأساسية التالية لتشغيل مزامنة المشاريع من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.

**اسم القالب في تكامل البيانات:**
- المشاريع (Finance and Operations إلى Field Service)

**أسماء المهام في مشروع تكامل البيانات:**
- المشاريع

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات قائمة المشاريع:
- الحسابات (Sales إلى Finance and Operations) 

## <a name="entity-set"></a>مجموعة الكيانات
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | المشاريع                |

## <a name="entity-flow"></a>تدفق الكيان
يتم إنشاء المشاريع في Finance and Operations. ستتم مزامنة المشاريع ذات **نوع مشروع** الوقت والمادة و**مرحلة مشروع** قيد التقدم إلى كيان **المشروع الخارجي** في Field Service، بما في ذلك رقم المشروع واسم المشروع ومرحلة المشروع ومعلومات حساب العميل. تُستخدم قائمة **المشروع الخارجي** لإقران أوامر عمل Field service مع مشاريع Finance and Operations.
حل Field Service CRM المشروع الخارجي عبارة عن كيان جديد يحصل على جميع المشاريع من Operations.
تمت إضافة حقل "المشروع الخارجي" إلى كيان "أمر العمل". هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Operations. عندما تتغير حالة النظام من مفتوح - قيد التقديم(690,970,000) إلى حالة أعلى، سيتم تأمين حقل المشروع الخارجي ولا يمكنك إضافة القيمة أو إزالتها أو تغييرها.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين
### <a name="in-finance-and-operations"></a>في Finance and Operations
تمكين تعقب التغييرات لمشاريع كيان البيانات

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات


### <a name="projects-finance-and-operations-to-field-service-projects"></a>المشاريع (Finance and Operations to Field Service): المشاريع

[![تعيين القالب في تكامل البيانات](./media/FSProject1.png)](./media/FSProject1.png)

