---
title: دورة حياة إدارة النموذج
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
ms.openlocfilehash: 0b16cfdce801e8a63b47397526b47995018b99c9
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594821"
---
# <a name="model-management-lifecycle"></a>دورة حياة إدارة النموذج

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع طرق الحفاظ على نماذج التعلم الآلي لمؤسستك لتحسين التنبؤات التي يتم إنشاؤها.

نوصي بتدريب نموذج الذكاء الاصطناعي في بيئة اختبار معزولة ثم استخدام الحلول المدارة لنشره في بيئة إنتاج. يساعد هذا النهج في ضمان وجود عناصر التحكم الصحيحة لإدارة دورة حياة النموذج.

نظرا لأن نموذج الذكاء الاصطناعي يستند إلى بيانات الفاتورة العميل المتوفرة، فمن المهم أن تحتوي بيئة الاختبار المعزولة على نسخة حديثة من بيانات الإنتاج. يمكنك البدء بتدريب النموذج باتباع الخطوات الواردة في [استخدام توقعات الدفع للعميل](use-customer-payment-predictions.md). بعد إعادة تدريب النموذج، قم بتقييم النتائج كما هو موضح في [تقييم نموذج تنبؤ الدفع للعميل الأولي](evaluate-payment-prediction.md). استخدم المعلومات الموجودة في [تحسين نموذج التنبؤ](improve-model.md) لتجربة مجموعات الميزات وعوامل التصفية التي يمكن أن تساعد في تحسين النموذج.

عندما تكون راضيا عن نتائج التدريب، اتبع الخطوات الواردة في [توزيع نموذج الذكاء الاصطناعي](/ai-builder/distribute-model) للانتقال بالطراز إلى بيئة الإنتاج.
