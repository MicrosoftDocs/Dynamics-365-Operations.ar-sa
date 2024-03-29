---
title: علاقات كائنات الخدمة
description: يمكنك إنشاء علاقات كائنات الخدمة بين كائن خدمة واتفاقية خدمة أو أمر خدمة.
author: sorenva
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 831db29589826904666049edbc8be0c38e1d02a5
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676624"
---
# <a name="service-object-relations"></a>علاقات كائنات الخدمة 

[!include [banner](../includes/banner.md)]

يمكنك إنشاء علاقات كائنات الخدمة بين كائن خدمة واتفاقية خدمة أو أمر خدمة. عند قيامك بإنشاء علاقة، ستقوم بإرفاق كائن الخدمة باتفاقية الخدمة أو أمر الخدمة.

بعد إنشاء العلاقة، يمكنك إرفاق كائن الخدمة بأية بنود في اتفاقية الخدمة أو أمر الخدمة.

## <a name="template-boms"></a>شجرة المواد القالب

يمكنك أيضًا تحديد شجرة المواد القالب لعلاقة الكائن. وشجرة المواد القالب هي عبارة عن كمبيالة مواد للكائن الذي تُجري عليه الخدمة. إذا قمت باستبدال جزء مكون لكائن الخدمة أثناء زيارة خدمة، فيمكنك تسجيل هذا التغيير في قائمة مكونات الصنف الخاصة بالخدمة باستخدام نموذج كائنات الخدمة.

## <a name="example"></a>مثال

تقوم بإنشاء اتفاقية خدمة لصيانة مصعدين بموقع أحد العملاء.
وتشتمل اتفاقية الخدمة على المعرّف ID SAL-001.

تم إعداد المصعدين في نموذج كائنات الخدمات ككائنات، EL-S/1000 وEL-L/1000.

وستقوم بإرفاق كائني الخدمة، EL-S/1000 وEL-L/1000، باتفاقية الخدمة.

تريد تسجيل التغييرات في شجرة المواد لكائن الخدمة بينما تقوم باستبدال الأجزاء المكونة للكائن، لذا سترفق شجرة مواد الخدمة بعلاقة كائن الخدمة، كما هو موضح بالجدول التالي.

| كائن الخدمة | العلاقة – اتفاقية الخدمة | شجرة مواد للخدمة   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | BOM-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | BOM-EL-L/1000 |

نظرًا لتوافر علاقات كائن الخدمة للاتفاقية، يمكنك الآن إنشاء بنود اتفاقية خدمة تحتوي على هذه الكائنات، كما هو موضح بالجدول التالي.

| نوع الحركة | الفئة           | كائن الخدمة |
|------------------|--------------------|----------------|
| الساعة             | فحص         | EL-S/1000      |
| الساعة             | تنظيف صندوق التروس  | EL-S/1000      |
| الصنف             | مواد منظفة | EL-S/1000      |
| الساعة             | فحص         | EL-L/1000      |
| الساعة             | تنظيف صندوق التروس   | EL-L/1000      |
| الصنف             | مواد منظفة | EL-L/1000      |

أثناء إجراء زيارة خدمة، ينبغي استبدال صندوق تروس مصعد EL-S/1000. لاستبدال جزء مكون من الكائن، يمكنك الوصول إلى مصمم شجرة المواد باستخدام علاقة كائن الخدمة التي قمت بإعدادها لاتفاقية الخدمة الحالية.

الوصول إلى مصمم شجرة المواد باستخدام علاقة كائن خدمة

1. اتفاقيات الخدمة
2. انقر نقرًا مزدوجًا فوق اتفاقية خدمة، أو انقر فوق "اتفاقية الخدمة" لإنشاء اتفاقية خدمة جديدة.
3. انقر فوق علامة التبويب "إعداد".
4. انقر فوق "كائنات الخدمة" لإرفاق قائمة مكونات الصنف للقالب باتفاقية الخدمة.
5. في نموذج "كائنات الخدمة"، انقر فوق "المصمم" لفتح نموذج المصمم لتعديل قائمة مكونات الصنف للقالب.

## <a name="automatically-created-service-orders"></a>أوامر خدمة تم إنشاؤها تلقائيًا

إذا قمت بإنشاء أوامر الخدمة لاتفاقية الخدمة بشكل تلقائي، فإن علاقات كائن الخدمة في الاتفاقية ستنشأ أيضًا في أوامر الخدمة.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]