---
title: نظرة عامة على ميزة إقرار الإيرادات
description: يوفر هذا الموضوع معلومات حول ميزة إقرار الإيرادات. توفر هذه الميزة اطار عمل مرنًا يتيح لك تحديد القواعد الخاصة بالشركة للتعرف على سعر الإيرادات وجدول الإيرادات للأوامر متعددة العناصر.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: d52a9c7315cccf668a8b9bcf7ba5cad7039e186e
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863553"
---
# <a name="revenue-recognition-overview"></a>نظرة عامة على ميزة إقرار الإيرادات

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> لا يمكن تشغيل ميزة إقرار الإيرادات عبر إدارة الميزات. في الوقت الحالي، يجب استخدام مفاتيح التكوين لتشغيلها.

يجب أن تكون الشركات في المجالات التي تبيع عناصر متعددة، مثل المنتجات والخدمات والاشتراكات وغير ذلك، قادرة على تقسيم الأوامر متعددة العناصر بحيث يمكن التعرف على الإيرادات استنادًا إلى مجموعة من الإرشادات الخاصة بالشركة والمجال.

بشكل عام، يمكن استخدام عملية إقرار الإيرادات لتنفيذ هذه المهام:

* تخصيص الإيرادات للمساعدة في ضمان التعرف على سعر الإيرادات المناسب استنادًا إلى قيمة المكونات في الأوامر متعددة العناصر.
* تأجيل الإيرادات، استنادًا إلى جدول الإيرادات الذي يمثل الإطار الزمني التعاقدي والنسب المئوية لإقرار الإيرادات على مدار الوقت.

توفر ميزة إقرار الإيرادات اطار عمل مرنًا يتيح لك تحديد القواعد الخاصة بالشركة للتعرف على سعر الإيرادات وجدول الإيرادات للأوامر متعددة العناصر.

يتم استخدام المنتجات الصادرة لدعم إقرار الإيرادات في مستندات أوامر المبيعات. تحتوي المنتجات الصادرة على الإعداد المطلوب لتحديد سعر الإيرادات وجدول الإيرادات. بإمكان أمر المبيعات أن ينشأ من مشروع وقت ومادة.

بإمكان الشركات استخدام وظيفة جدول الإيرادات بدون استخدام وظيفة سعر الإيرادات. وبالتالي، سيتم استخدام السعر الموجود في بنود أمر المبيعات إما كإيرادات أو كإيرادات مؤجلة. في حال وجود جدول إيرادات في بند أمر المبيعات، سيتم تأجيل السعر على بند أمر المبيعات. في حال عدم وجود جدول إيرادات في بند أمر المبيعات، فسيتم ترحيل بند أمر المبيعات إلى حساب إيرادات عند فوترته.

يتم حساب سعر الإيرادات إما عند تأكيد أمر المبيعات أو عند ترحيل الفاتورة. لمعاينة سعر الإيرادات قبل ترحيل الفاتورة، يجب تأكيد أمر المبيعات.

عند تأكيد أمر المبيعات، يتم أيضاً إنشاء جدول إيرادات متوقع إذا تضمن أي بند في أمر المبيعات جدول إيرادات. عند فوتره أمر المبيعات، يتم حذف جدول الإيرادات المتوقع، ويتم استبدال جدول الإيرادات المتوقع بجدول إقرار الإيرادات الفعلي.

ويتم الاحتفاظ بتفاصيل جدول إقرار الإيرادات لكل بند من بنود أمر المبيعات. وبالتالي، بإمكان مدير إقرار الإيرادات عرض التفاصيل وإصدار البنود إلى الإيرادات عند اكتمال الالتزام التعاقدي. وفي نهاية كل فترة، بإمكان مدير إقرار الإيرادات إنشاء دفتر يومية إيرادات لإصدار أي بنود جدول تستحق في تاريخ قام بتحديده أو قبله. لا يتم ترحيل دفتر يومية الإيرادات هذا على الفور. والتالي، بإمكان مدير إقرار الإيرادات التحقق من إصدار المبالغ الصحيحة من الإيرادات المؤجلة إلى الإيرادات الفعلية.

إذا تسبب تغيير تعاقدي في إضافة بند أمر مبيعات جديد إما إلى أمر المبيعات الموجود أو إلى أمر مبيعات جديد، فيمكن تشغيل عملية إعادة تخصيص لتصحيح سعر الإيرادات عبر جميع بنود أمر المبيعات.