---
title: دورة حياة إدارة النماذج (معاينة)
description: يصف هذا الموضوع طرق الحفاظ على نماذج التعلم الآلي لمؤسستك لتحسين التنبؤات التي يتم إنشاؤها.
author: ShivamPandey-msft
ms.date: 07/16/2021
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
ms.openlocfilehash: c84f0a6079d7e599ed1f3e44c26c625e548c06d5a91447c46fc722ce6a6cf414
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741550"
---
# <a name="model-management-lifecycle-preview"></a>دورة حياة إدارة النماذج (معاينة)

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع طرق الحفاظ على نماذج التعلم الآلي لمؤسستك لتحسين التنبؤات التي يتم إنشاؤها.

نوصي بتدريب نموذج الذكاء الاصطناعي في بيئة اختبار معزولة ثم استخدام الحلول المدارة لنشره في بيئة إنتاج. يساعد هذا النهج في ضمان وجود عناصر التحكم الصحيحة لإدارة دورة حياة النموذج.

نظرا لأن نموذج الذكاء الاصطناعي يستند إلى بيانات الفاتورة العميل المتوفرة، فمن المهم أن تحتوي بيئة الاختبار المعزولة على نسخة حديثة من بيانات الإنتاج. يمكنك البدء بتدريب النموذج باتباع الخطوات الواردة في [استخدام توقعات الدفع للعميل](use-customer-payment-predictions.md). بعد إعادة تدريب النموذج، قم بتقييم النتائج كما هو موضح في [تقييم نموذج تنبؤ الدفع للعميل الأولي](evaluate-payment-prediction.md). استخدم المعلومات الموجودة في [تحسين نموذج التنبؤ](improve-model.md) لتجربة مجموعات الميزات وعوامل التصفية التي يمكن أن تساعد في تحسين النموذج.

عندما تكون راضيا عن نتائج التدريب، اتبع الخطوات الواردة في [توزيع نموذج الذكاء الاصطناعي](https://docs.microsoft.com/ai-builder/distribute-model) للانتقال بالطراز إلى بيئة الإنتاج.
