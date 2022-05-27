---
title: قيود على إصدارات التكاليف للتكاليف القياسية
description: يوضح هذا الموضوع القيود التي يتم تطبيقها على إصدار التكلفة للتكاليف القياسية.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11bf14b2926fd4ff053697bef8b7dad781948a2c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672195"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>قيود على إصدارات التكاليف للتكاليف القياسية

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع القيود التي يتم تطبيقها على إصدار التكلفة للتكاليف القياسية. 

تساعد القيود التالية على ضمان الالتزام بمبادئ التكلفة القياسية:

-  يجب تضمين المصاريف في تكلفة الصنف. وتقدم المصاريف لصنف مصنّع التكاليف الثابتة المستهلكة في قائمة مكونات الصنف (BOM) ومعلومات التوجيه. لذلك، يجب تضمين المصاريف في تكلفة الوحدة. كما يتم تضمين المصاريف لصنف تم شراؤه أيضًا في تكلفة وحدة الصنف.

-  يجب أن يعتمد حساب التكاليف القياسية للأصناف المصنّعة على سجلات التكلفة في إصدار تكلفة للتكاليف القياسية. ويمكن استخدام المصادر البديلة لبيانات التكلفة فقط مع إصدار تكلفة للتكاليف المخططة، على سبيل المثال، اتفاقيات تجارية بسعر الشراء للأصناف التي تم شراؤها. يتم تحديد مصادر بديلة لبيانات التكلفة حسب مجموعة حساب قائمة مكونات الصنف (BOM).

-  يجب تنفيذ عمليات حساب قائمة مكونات الصنف (BOM) في وضع عملية تحديد إجمالي المكونات المطلوبة بمستوى واحد.

يمكن نسخ بيانات تكلفة الصنف للتكاليف القياسية إلى إصدار تكلفة آخر يحتوي على تكاليف قياسية أو تكاليف مخططة. ومع ذلك؛ لا يمكن نسخ بيانات تكلفة الصنف للتكاليف المخططة إلى إصدار تكلفة يحتوي على تكاليف قياسية؛ وذلك لأن القيود التي تم إدراجها في بداية هذا الموضوع لا تنطبق على التكاليف المخططة.

## <a name="related-topics"></a>مواضيع مرتبطة

[نظرة عامة حول إصدارات التكاليف](costing-versions.md)

[تحديث التكاليف القياسية في بيئة غير تصنيع](update-standard-costs-non-manufacturing-environment.md)

[الإعداد للاحتفاظ بالتكاليف القياسية للأصناف المصنعة](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]