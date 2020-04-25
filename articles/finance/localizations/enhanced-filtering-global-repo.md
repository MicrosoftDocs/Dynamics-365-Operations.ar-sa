---
title: التصفية المحسنة في RCS/المستودع العمومي
description: يصف هذا الموضوع قدرات التصفية المحسنة للمستودع العمومي RCS، التي تم تحسينها لتضمين عوامل تصفية إضافية.
author: JaneA07
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1adbd690795139778dc77a574e9d5f91a4bdeb3c
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249155"
---
# <a name="enhanced-filtering-options-for-finding-configurations-in-the-global-repository"></a>خيارات التصفية المحسنة للبحث عن التكوينات في المستودع العمومي

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع قدرات التصفية المحسنة للمستودع العمومي لخدمات Regulatory Configuration Services (RCS)، التي تم تحسينها لتضمين عوامل التصفية التالية: 
- **البلد/المنطقة** - بالاستناد إلى أكواد بلدان ISO  
- **علامات** - لمنطقه العمل/الميزة؛ الصناعة، نوع مستند الأعمال 

يمكنك تطبيق عوامل التصفية، إما بشكل فردي أو في مجموعات، للعثور على تكوينات محددة أو ذات صلة. على سبيل المثال، للبحث عن جميع مستندات الأعمال القابلة للتكوين ذات الصلة بفواتير الموردين، يمكن تطبيق عامل التصفية **نوع مستند الأعمال**. 

يمكنك إجراء مزيد من التنقيح في البحث عن طريق تحديد رمز البلد والنقر فوق **تطبيق عامل التصفية**.  

[![قسام عامل التصفية للمستودع العام](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

يبين المثال التالي النتائج عند إجراء التصفية على **نوع مستند الأعمال**. 

[![تطبيق عامل التصفية والاستيراد لنوع مستند الاعمال](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

يمكن استيراد النتائج المصفاة إلى RCS المستخدمين أو بيئة Dynamics 365 Finance، سواء بشكل فردي أو كمجموعة (بتحديد مجموعة التكوينات) والنقر فوق **استيراد**.






