---
title: تصفية RCS المحسنة في RCS/المستودع العمومي
description: يصف هذا الموضوع قدرات التصفية المحسنة للمستودع العمومي RCS، التي تم تحسينها لتضمين عوامل تصفية إضافية.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a67a4345271cbeffc100fc1d9077cc866846a4d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005832"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>خيارات تصفية RCS المحسنة للبحث عن التكوينات في RCS/المستودع العمومي

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع قدرات التصفية المحسنة للمستودع العمومي لخدمات Regulatory Configuration Services (RCS)، التي تم تحسينها لتشمل القدرة على التصفية باستخدام العوامل التالية: 
- **البلد/المنطقة** - بالاستناد إلى أكواد بلدان ISO  
- أنواع **العلامات** لـ:
  - المنطقة الوظيفية
  - منطقة الميزة
  - المجال 
  - مستند الأعمال 

لتسهيل اكتشاف تكوينات خاصة أو متعلقة يمكنك تطبيق عوامل التصفية، إما بشكل فردي أو كمجموعة. على سبيل المثال، للعثور على نوع واحد من 'مستندات الأعمال القابلة للتكوين المرتبطة بفواتير المورد، يمكنك تطبيق عامل التصفية **نوع مستند الأعمال** للبحث عن هذا النوع من المستندات. 

[![قسام عامل التصفية للمستودع العام](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

يمكنك إجراء مزيد من التنقيح في البحث بتحديد نوع المستند، على سبيل المثال 'فاتورة المورد' والنقر فوق **تطبيق عامل التصفية**. يبين المثال التالي النتائج عند إجراء التصفية على **نوع مستند الأعمال** مع نوع المستند المضاف. 

[![تطبيق عامل التصفية والاستيراد لنوع مستند الاعمال](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

يمكن استيراد النتائج المصفاة إلى مستودع RCS للمستخدمين أو بيئة Dynamics 365 Finance، سواء بشكل فردي أو كمجموعة. للقيام بذلك، حدد مجموعة التكوينات، وانقر فوق **استيراد**.
