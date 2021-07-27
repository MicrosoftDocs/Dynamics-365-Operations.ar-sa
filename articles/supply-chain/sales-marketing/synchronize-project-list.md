---
title: مزامنة قائمة المشاريع من Supply Chain Management إلى Field Service
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: eb98f266a217fc16c56c38e2480b85f529fb1862
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359827"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>مزامنة قائمة المشاريع من Supply Chain Management إلى Field Service

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.

[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service.](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يتم استخدام القوالب والمهام الأساسية التالية لتشغيل مزامنة المشاريع من Supply Chain Management إلى Field Service.

**قالب في تكامل البيانات**
- المشاريع (Supply Chain Management إلى Field Service)

**مهمة في مشروع تكامل البيانات**
- المشاريع

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات قائمة المشاريع:
- الحسابات (Sales إلى Supply Chain Management) 

## <a name="entity-set"></a>مجموعة الكيانات
| Field Service           | Supply Chain Management  |
|-------------------------|-------------------------|
|msdynce_externalprojects | المشاريع                |

## <a name="entity-flow"></a>تدفق الكيان
يتم إنشاء المشاريع في Supply Chain Management. ستتم مزامنة المشاريع التي تم فيها تعيين **نوع المشروع** إلى **الوقت والمادة** وتعيين **مرحلة المشروع** إلى **قيد التقدم** مع الكيان **مشروع خارجي** في Field Service، بما في ذلك رقم المشروع واسم المشروع ومرحلة المشروع ومعلومات حساب العميل. تُستخدم قائمة **المشروع الخارجي** لإقران أوامر عمل Field service مع مشاريع Supply Chain Management.

## <a name="field-service-crm-solution"></a>حل Field Service CRM
يحصل الكيان **مشروع الخارجي** على جميع المشاريع من Supply Chain Management. تمت إضافة الحقل **مشروع خارجي** إلى الكيان **أمر عمل**. هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Supply Chain Management. عندما تتغير **حالة النظام** من **مفتوح – قيد التقدم(690,970,000)** إلى حالة أعلى، سيتم تأمين الحقل **مشروع خارجي** وسيتعذر عليك إضافة القيمة أو إزالتها أو تغييرها.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين
### <a name="supply-chain-management"></a>Supply Chain Management
تمكين تعقب التغييرات لمشاريع كيان البيانات.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات


### <a name="projects-supply-chain-management-to-field-service-projects"></a>المشاريع (Supply Chain Management إلى Field Service): المشاريع

[![تعيين القالب في تكامل البيانات.](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]