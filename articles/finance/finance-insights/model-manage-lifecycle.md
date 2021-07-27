---
title: دورة حياة إدارة النماذج (معاينة)
description: يصف هذا الموضوع طرق الحفاظ على نماذج التعلم الآلي لمؤسستك لتحسين التنبؤات التي يتم إنشاؤها.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d5566bde97a2e60d050f4a7b499b554df4848bf9
ms.sourcegitcommit: f6050b444e636ba662c00d0443c94a99f8ea0b0d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/28/2021
ms.locfileid: "6309780"
---
# <a name="model-management-lifecycle-preview"></a>دورة حياة إدارة النماذج (معاينة)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يصف هذا الموضوع طرق الحفاظ على نماذج التعلم الآلي لمؤسستك لتحسين التنبؤات التي يتم إنشاؤها.

نوصي بتدريب نموذج الذكاء الاصطناعي في بيئة اختبار معزولة ثم استخدام الحلول المدارة لنشره في بيئة إنتاج. يساعد هذا النهج في ضمان وجود عناصر التحكم الصحيحة لإدارة دورة حياة النموذج.

نظرا لأن نموذج الذكاء الاصطناعي يستند إلى بيانات الفاتورة العميل المتوفرة، فمن المهم أن تحتوي بيئة الاختبار المعزولة على نسخة حديثة من بيانات الإنتاج. يمكنك البدء بتدريب النموذج باتباع الخطوات الواردة في [استخدام توقعات الدفع للعميل](use-customer-payment-predictions.md). بعد إعادة تدريب النموذج، قم بتقييم النتائج كما هو موضح في [تقييم نموذج تنبؤ الدفع للعميل الأولي](evaluate-payment-prediction.md). استخدم المعلومات الموجودة في [تحسين نموذج التنبؤ](improve-model.md) لتجربة مجموعات الميزات وعوامل التصفية التي يمكن أن تساعد في تحسين النموذج.

عندما تكون راضيا عن نتائج التدريب، اتبع الخطوات الواردة في [توزيع نموذج الذكاء الاصطناعي](https://docs.microsoft.com/ai-builder/distribute-model) للانتقال بالطراز إلى بيئة الإنتاج.
