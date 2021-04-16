---
title: إنشاء خطة مقيدة
description: يوضح هذا الموضوع كيفية إنشاء خطة تأخذ في الاعتبار القيود المادية وقيود القدرة.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c35d5a7465cc6cfe0bc12cb00796eff2aeed1ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808006"
---
# <a name="generate-a-constrained-plan"></a>إنشاء خطة مقيدة

[!include [banner](../../includes/banner.md)]

يوضح هذا الموضوع كيفية إنشاء خطة تأخذ في الاعتبار القيود المادية وقيود القدرة. تضمن الخطة عدم بدء التصنيع قبل أن تتوفر المواد وعدم تعرض الموارد لزيادة في الحجز. 

شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. هذا الإجراء مخصص لمخطط الإنتاج‬.


## <a name="set-up-a-constrained-plan"></a>إعداد خطة مقيدة
1. في الصفحة الرئيسية، حدد مساحة عمل **التخطيط الرئيسي**.
2. حدد **الخطط الرئيسية** في قائمة الارتباطات إلى أقصى يسار مساحة العمل.
3. في القائمة، قم بالبحث عن السجل المطلوب وحدده. مثال: **StaticPlan**  
4. حدد **نعم** في الحقل **قدرة محدودة‬**.
5. في الحقل **الحد الزمني للقدرة المحدودة‬**، أدخل `30`.
6. قم بتوسيع القسم **الحدود الزمنية بالأيام**.
7. حدد **نعم** في الحقل **قدرة**.
8. في الحقل **الحد الزمني لجدولة القدرة (بالأيام)‬**، أدخل رقمًا. مثال: `60`  
9. حدد **نعم** في الحقل **التأخيرات المحسوبة**‬.
10. في الحقل **الحد الزمني لحساب التأخيرات (بالأيام)‬‬**، أدخل رقمًا. مثال: `60` 
11. وسّع القسم **التأخيرات المحسوبة**.
12. حدد **نعم** في الحقل **إضافة التأخير المحسوب إلى تاريخ المتطلبات**‬.
13. قم بإغلاق الصفحة.

## <a name="create-a-constrained-plan"></a>إنشاء خطة مقيدة
1. حدد **تشغيل**.
2. في حقل **الخطة الرئيسية**، أدخل أو حدد الخطة التي قمت بإعداد قيود لها.  
3. حدد **موافق**.
4. حدد **الأوامر المخططة‬**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]