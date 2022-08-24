---
title: تصفية RCS المحسنة في RCS/المستودع العمومي
description: تصف هذه المقالة إمكانيات التصفية المحسنة للمستودع العمومي RCS التي تم تحسينها لتضمين عوامل التصفية الإضافية.
author: kfend
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: e0408d0561c0cfead8781b9f49fdb84d5caf179a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274501"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>خيارات تصفية RCS المحسنة للبحث عن التكوينات في RCS/المستودع العمومي

[!include [banner](../includes/banner.md)]

تصف هذه المقالة قدرات التصفية المحسنة للمستودع العمومي لخدمات Regulatory Configuration Services‎‎‏ (RCS) التي تم تحسينها لتشمل القدرة على التصفية باستخدام العوامل التالية: 
- **البلد/المنطقة** - بالاستناد إلى أكواد بلدان ISO  
- أنواع **العلامات** لـ:
  - المنطقة الوظيفية
  - منطقة الميزة
  - المجال 
  - مستند الأعمال 

لتسهيل اكتشاف تكوينات خاصة أو متعلقة يمكنك تطبيق عوامل التصفية، إما بشكل فردي أو كمجموعة. على سبيل المثال، للعثور على نوع واحد من 'مستندات الأعمال القابلة للتكوين المرتبطة بفواتير المورد، يمكنك تطبيق عامل التصفية **نوع مستند الأعمال** للبحث عن هذا النوع من المستندات. 

[![قسام عامل التصفية للمستودع العام.](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

يمكنك إجراء مزيد من التنقيح في البحث بتحديد نوع المستند، على سبيل المثال 'فاتورة المورد' والنقر فوق **تطبيق عامل التصفية**. يبين المثال التالي النتائج عند إجراء التصفية على **نوع مستند الأعمال** مع نوع المستند المضاف. 

[![تطبيق عامل التصفية والاستيراد لنوع مستند الأعمال.](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

يمكن استيراد النتائج المصفاة إلى مستودع RCS للمستخدمين أو بيئة Dynamics 365 Finance سواء بشكل فردي أو كمجموعة. للقيام بذلك، حدد مجموعة التكوينات، وانقر فوق **استيراد**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
