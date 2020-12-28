---
title: نظرة عامة على إدارة النقل
description: يقدم هذا الموضوع نظرة عامة حول وظائف إدارة النقل في Supply Chain Management.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4affc5846ee329a4571d6fb3e0c42873387241ad
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4421736"
---
# <a name="transportation-management-overview"></a>نظرة عامة على إدارة النقل

[!include [banner](../includes/banner.md)]

يقدم هذا الموضوع نظرة عامة حول وظائف إدارة النقل في Supply Chain Management.

تسمح لك إدارة النقل باستخدام وسائل النقل الخاص بالشركة، وتسمح لك أيضًا بتحديد المورّدين وحلول التوجيه للأوامر الواردة والصادرة. على سبيل المثال، يمكنك تعريف أسرع الطرق أو المعدل الأقل تكلفة لشحنة ما. يصف الجدول التالي السيناريوهات الأساسية لاستخدام إدارة النقل.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>سيناريو</th>
<th>كيف تستطيع إدارة النقل المساعدة</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>استخدام موفري الخدمات اللوجستية لأنشطة النقل.</td>
<td>استخدم إدارة النقل لعمليات النقل الواردة و/أو الصادرة.</td>
</tr>
<tr class="even">
<td>يتوفر أسطول الشركة الخاص للتسليم/الالتقاط، ويتم تحويل رسوم التسليم إلى العملاء.</td>
<td>للعمليات الصادرة، يمكنك استخدام إدارة النقل لتحديد رسوم النقل وتمريرها للعملاء. ومع ذلك، فإن عملية تسوية فواتير شركة النقل غير مطلوبة.</td>
</tr>
<tr class="odd">
<td>يتوفر أسطول الشركة الخاص للتسليم/الالتقاط، ولكن لا يتم تحويل رسوم التسليم إلى العملاء، لأن أسعار المنتجات تتضمن النقل.</td>
<td>الكثير من وظائف إدارة النقل غير مطلوب. ومع ذلك، يمكنك استخدام إدارة النقل لتحديد أسعار النقل وتعديل سعر المبيعات وفقًا لذلك.</td>
</tr>
<tr class="even">
<td>يتم توفير الخدمات اللوجستية من قبل كيان قانوني آخر في نفس الشركة.</td>
<td><ul>
<li>يمكنك استخدام إدارة النقل عن طريق معاملة الكيان القانوني الآخر كأي شركة شحن أخرى. لا يمكن أتمتة الحركات الاقتصادية بين الكيانات القانونية. ولذلك، يجب التعامل مع هذه الحركات يدويًا (على سبيل المثال، عن طريق إنشاء أمر شراء).</li>
<li>في الكيان القانوني الذي يوفر الخدمات اللوجستية، يمكن استخدام إدارة النقل لتحديد أسعار النقل.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a>تخطيط النقل في Supply Chain Management
في إدارة النقل، بإمكان تخطيط النقل أن يستند إما إلى الأوامر أو إلى الشحنات التي تم إنشاؤها بالاستناد إلى تلك الأوامر. تكون الشحنات موجودة دائمًا في مرحلة معينة، ولكنها ليست ضرورية لتخطيط النقل. تشكّل أوامر التحويل جزءًا من السيناريو الصادر ويمكن تخطيطها مع أوامر المبيعات. 

![رسم حمل العمل](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>النقل الوارد
‏‫إذا طلبت أصنافًا من المورّد وإذا كان يجب تسليم الأصناف إلى المستودع، فقد تحتاج إلى ترتيب عملية نقل الأصناف بنفسك. يمكنك استخدام Supply Chain Management لتخطيط النقل واستلام حمل العمل الوارد.‬ يبين الرسم التوضيحي التالي تدفق العملية التجارية لتخطيط نقل حمل العمل الداخلي. 

![سير إجراء العمل لنقل حمل العمل الوارد](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>النقل الصادر
يمكنك تخطيط ومعالجة حمل العمل الصادر لشحن أصناف معينة من مستودع للشركة لعميل. يمكنك استخدام Supply Chain Management لتخطيط النقل وشحن حمولة صادرة. يبين الرسم التوضيحي التالي تدفق العملية التجارية للتخطيط ومعالجة أحمال العمل الصادرة للشحن. 

![تخطيط أحمال العمل الصادرة ومعالجتها](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>إنشاء حمل العمل
يوفر Supply Chain Management استراتيجية بناء حمل العمل التي تسمى استراتيجية بناء حمل العمل على أساس الحجم. تسمح لك هذه الاستراتيجية باستخدام القيم القصوى المحددة للطول والوزن في قالب حمل العمل، أو يمكنك تجاوز الإعدادات بإدخال قيم جديدة. لاستخدام هذه الاستراتيجية، حددها في الحقل **إستراتيجية إنشاء الحِمل‬** على علامة التبويب السريعة **إعداد** في صفحة **منضدة عمل إنشاء الحِمل‬**. وبالإضافة إلى ذلك، يمكنك إضافة استراتيجيات بناء الأحمال الخاصة بك عن طريق إنشاء فئة جديدة في شجرة مكونات البرنامج (AOT).



