---
title: قواعد التكوين
description: توفر هذه المقالة معلومات عامة حول قواعد التكوين. تعرّف قواعد التكوين العلاقات بين الأصناف الموجودة في قائمة مكونات الصنف (BOM) للمنتجات التي تستخدم تقنية التكوين المستنِد إلى بُعد.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ddc74777ae0cde5367667f93eb29ffb21531e02
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570767"
---
# <a name="configuration-rules"></a>قواعد التكوين

[!include [banner](../includes/banner.md)]

توفر هذه المقالة معلومات عامة حول قواعد التكوين. تعرّف قواعد التكوين العلاقات بين الأصناف الموجودة في قائمة مكونات الصنف (BOM) للمنتجات التي تستخدم تقنية التكوين المستنِد إلى بُعد.

تتوفر قواعد التكوين عند قيامك بتحديد نماذج التكوين المستندة إلى بعد. ويتم استخدام قواعد التكوين لفرض أو منع مجموعات الأصناف المحددة في قائمة مكونات الصنف (BOM). وبعد إنشاء قائمة مكونات الصنف والأصناف ذات الصلة التي تم تعيينها إلى مجموعات التكوين الخاصة بها، يمكن تحديد واحد أو أكثر من قواعد التكوين. وفي حالة انتماء الصنفين لبعضهما، يتم استخدام عامل **التحديد** لضمان الإدراج. أما إذا كان يتم استثناء الصنفين بشكل متبادل، فإنه يتم استخدام عامل **إلغاء التحديد** لضمان الاستثناء.  

**ملاحظة:** تنطبق هذه المعلومات فقط على أصول المنتجات التي تستخدم تقنية التكوين المستندة إلى بعد.  

ولا تتأثر عمليات التكوين الحالية بالتغييرات المتتابعة على قواعد التكوين. ومع ذلك، يُعد من المهم تعيين القواعد قبل تحديد تكوين جديد، أو فحص هذه القواعد إذا كنت تعتقد أنه قد تم تغيير القواعد.  

**ملاحظة:** بالنسبة إلى طريقة **التحديد**، يتم تحديد مجموعة التكوين المشتق ورقم الصنف والتكوين تلقائيًا. وفي طريقة **إلغاء التحديد** لا يمكن تحديد مجموعة التكوين المشتق ورقم الصنف بالإضافة إلى التكوين.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على تكوين المنتجات المستند إلى الأبعاد](dimension-based-product-configuration.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]