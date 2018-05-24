---
title: "إدارة الخدمة"
description: "استخدم إدارة الخدمة لإنشاء اشتراكات الخدمة واتفاقيات الخدمة، والتعامل مع أوامر الخدمة واستفسارات العملاء، ولإدارة وتحليل تقديم الخدمات للعملاء."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: ar-sa
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a>إدارة الخدمة 

[!include [banner](../includes/banner.md)]


استخدم **إدارة الخدمة** لإنشاء اشتراكات الخدمة واتفاقيات الخدمة، والتعامل مع أوامر الخدمة واستفسارات العملاء، ولإدارة وتحليل تقديم الخدمات للعملاء. يمكنك استخدام اتفاقيات الخدمة لتعريف الموارد التي يتم استخدامها في زيارة خدمة عادية. يمكنك أيضا استخدام اتفاقيات الخدمة لعرض كيفية فوترة هذه المصادر إلى العميل. يمكن لاتفاقية خدمة أن تتضمن اتفاقية مستوى خدمة تحدد أوقات الاستجابة القياسية، وتقدم أدوات لتسجيل الوقت الفعلي.

يمكنك إنشاء أوامر الخدمة لإدارة معلومات حول الزيارات المجدولة وغير المجدولة التي يقوم بها فَنِّي الخدمة إلى موقع أحد العملاء. أوامر الخدمة تتضمن معلومات مثل:

1.  ساعات العمل التي سيجريها فني الخدمة

2.  نوع الخدمة أو الإصلاح

3.  الصنف الذي سيتم إصلاحه، بما في ذلك تفاصيل حول الأعراض والتشخيص

4.  النفقات والرسوم المتعلقة بالخدمة أو الإصلاح

يمكن للعملاء إرسال طلبات الخدمة عبر الإنترنت باستخدام مدخل الشركة على الإنترنت. يمكنك تلقي ومعالجة وإرسال هذه الطلبات. بعد إنشاء أمر خدمة، يمكنك استخدام مراحل الخدمة لرصد التقدم المحرز وتحديد القواعد التي تتحكم في الإجراءات التي تم تمكينها في كل مرحلة. عند اكتمال أمر خدمة، يمكنك تسجيل الخروج عن الأمر للتأكد من أنه كامل ثم ترحيل الأمر لبدء عملية الفوترة.

استخدام أدوات إعداد التقارير لمراقبة هوامش أمر الخدمة وحركات الاشتراك ووصف أعمال الطباعة وإيصالات العمل.

## <a name="business-processes"></a>‏‏العمليات التجارية

يوضح المخطط التالي العمليات التجارية عالية المستوى لـ **إدارة الخدمة**، ويظهر أين تتكامل عمليات خدمة مع الوحدات النمطية الأخرى في Microsoft Dynamics 365 for Finance and Operations.

[![مخطط العمليات التجارية لإدارة الخدمات](./media/sm_home_page.gif)](./media/sm_home_page.gif)

## <a name="service-management-at-a-glance"></a>إدارة خدمة في لمحة

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>مهام مهمة</p></th>
<th><p>النماذج الأولية</p></th>
<th><p>تقارير شائعة</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>الوفاء باتفاقيات الخدمات</a></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">اتفاقيات الخدمات (نموذج)</a></p></td>
<td><p><strong>هامش أمر الخدمة</strong></p></td>
</tr>
<tr class="even">
<td><p>التعامل مع استعلامات العميل</a></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">أوامر الخدمة (نموذج)</a></p></td>
<td><p><strong>وصف العمل</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">‏‏لوحة الإرسال (نموذج)</a></p></td>
<td><p><strong>الحركة - الاشتراك</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><strong>حركات رسوم الاشتراك</strong></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a>دمج إدارة خدمة

يمكن أن تتكامل إداة الخدمات مع الوحدات النمطية التالية في Microsoft Dynamics 365 for Finance and Operations:

  - [المبيعات والتسويق](../sales-marketing/overview-sales-marketing.md)

  - [الموارد البشرية](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


