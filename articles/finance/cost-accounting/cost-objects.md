---
title: أبعاد كائن التكاليف
description: عندما تقوم بتحليل التكاليف، يمكنك استخدام أبعاد عنصر التكلفة لتحديد المكان الذي تتدفق إليه التكاليف. ويمكنك استخدام أبعاد كائن التكلفة لتحديد المكان حيث يجب تعيين التكاليف. يوفر هذا الموضوع معلومات حول أبعاد كائن التكلفة.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: roschlom
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9a17eaf0a65f5228ec60391e22c98c2f383d7cce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990807"
---
# <a name="cost-object-dimensions"></a>أبعاد كائن التكاليف

[!include [banner](../includes/banner.md)]

عندما تقوم بتحليل التكاليف، يمكنك استخدام أبعاد عنصر التكلفة لتحديد المكان الذي تتدفق إليه التكاليف. ويمكنك استخدام أبعاد كائن التكلفة لتحديد المكان حيث يجب تعيين التكاليف. يوفر هذا الموضوع معلومات حول أبعاد كائن التكلفة.

بإمكان كائن التكلفة أن يكون أي نوع كائن تريد تقديره أو توزيع تكاليفه أو قياسه بشكل مباشر. وتتضمن كائنات التكلفة النموذجية المنتجات والمشاريع والموارد والأقسام ومراكز التكلفة والمناطق الجغرافية. تستخدم الإدارة كائنات التكلفة لتحديد التكاليف وأيضًا لتعزيز تحليل الربحية.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>أبعاد كائن التكلفة وأعضاء أبعاد كائن التكلفة
تُعرف كائنات التكلفة بالاسم *أبعاد كائن التكلفة*. بعد أن تحدد الكيان الذي يجب أن يرجع إليه بُعد كائن التكلفة، يجب تحديد قيم الأبعاد الفردية أو استيرادها إلى محاسبة التكاليف من أنظمة مصادر أخرى. تُعرف قيم الأبعاد الفردية هذه بالاسم *أعضاء أبعاد كائن التكلفة*. على سبيل المثال، تريد استخدام البعد المالي الذي يسمى مركز التكلفة كبُعد كائن التكلفة. للاطلاع على كيفية تدفق التكاليف إلى مراكز التكلفة الفردية، يجب عليك استيراد أعضاء أبعاد كائن التكلفة. وفي هذه الحالة، تكون أعضاء أبعاد كائن تكلفة مراكز التكلفة الفعلية، مثل المبيعات والإنتاج والإدارة والمواقع الجغرافية. تظهر لقطة الشاشة التالية مثالاً لمراكز التكلفة كبعد كائن التكلفة مع مراكز التكلفة الفعلية الخاصة به كأعضاء أبعاد كائن التكلفة. 

[![لقطة شاشة تعرض مراكز التكلفة كبعد كائن تكلفة](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>استيراد أعضاء أبعاد كائن التكلفة من خلال موصلات البيانات
لتسهيل عملية استيراد أعضاء أبعاد كائن التكلفة، استخدم موصلات البيانات لاسترداد القيم من الكيانات التي تريد استخدامها كأبعاد كائن التكلفة. ويمكنك استخدام موصلات البيانات المنشأة مسبقًا أو موصلات البيانات المخصصة التق تقوم أنت بإنشائها.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]