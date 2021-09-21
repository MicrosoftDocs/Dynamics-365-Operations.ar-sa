---
title: يعمل تحديد إجمالي قائمة مكونات الصنف بشكل مختلف لأوامر الإنتاج المؤكدة والمقدرة
description: يعمل تحديد إجمالي قائمه مكونات الصنف بشكل مختلف لأوامر الإنتاج المؤكدة ولأوامر الإنتاج المقدرة للعمل الذي تم إنشاؤه يدوياً
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475469"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>يعمل تحديد إجمالي قائمة مكونات الصنف بشكل مختلف لأوامر الإنتاج المؤكدة والمقدرة

## <a name="symptoms"></a>العلامات

عند تاكيد أمر الإنتاج ، لن تكون الأصناف مجزاه عند تحديد قائمة مكونات الصنف (BOM). ومع ذلك ، عند إنشاء أمر العمل يدويا ، ثم تقدير أمر الإنتاج ، يتم التعامل مع الأصناف.

### <a name="resolution"></a>الحل

ستشير عمليات التحديد التي تحدث عند تاكيد أمر الإنتاج إلى الأمر المخطط ، ولكنه لا يبدو ان الأمر المخطط مؤكد حاليا في هذه الحالة. ومع ذلك ، إذا تم تقدير أمر الإنتاج ، يتم تشغيل عمليه تحديد إجمالي المكونات المطلوبة من أمر الإنتاج الذي تم إصداره في حاله عدم وجود أمر مخطط.
