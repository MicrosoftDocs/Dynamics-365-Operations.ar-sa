---
title: إنشاء خطة مقيدة
description: يوضح هذا المقال كيفية إنشاء خطة تأخذ في الاعتبار القيود المادية وقيود القدرة.
author: t-benebo
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65884d556724cd6132fe328e95a5bec78885c174
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904003"
---
# <a name="generate-a-constrained-plan"></a>إنشاء خطة مقيدة

[!include [banner](../../includes/banner.md)]

يوضح هذا المقال كيفية إنشاء خطة تأخذ في الاعتبار القيود المادية وقيود القدرة. تضمن الخطة عدم بدء التصنيع قبل أن تتوفر المواد وعدم تعرض الموارد لزيادة في الحجز. 

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