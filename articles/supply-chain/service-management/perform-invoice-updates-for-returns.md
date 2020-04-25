---
title: إجراء تحديثات الفاتورة للمرتجعات
description: تدعم هذه الوظائف العمليات التجارية للمؤسسات التي تختار إعداد فواتير أوامر الإرجاع وأوامر المبيعات لها في نفس الوقت وبواسطة نفس الشخص.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec803aaa2f750c43a1865c9536730b275e6ef1d4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202116"
---
# <a name="perform-invoice-updates-for-returns"></a>إجراء تحديثات الفاتورة للمرتجعات 

[!include [banner](../includes/banner.md)]


يعتبر أمر الإرجاع بمثابة نوع من أمر المبيعات الذي يتم تمييزه على أنه الأمر المرجع. لذلك، يتم استخدام صفحة قائمة **كافة أوامر المبيعات** لإنشاء فواتير لأوامر الإرجاع بدلاً من النموذج **أوامر الإرجاع**. تدعم هذه الوظائف العمليات التجارية للمؤسسات التي تختار إعداد فواتير أوامر الإرجاع وأوامر المبيعات لها في نفس الوقت وبواسطة نفس الشخص.

نظراً لأن الفاتورة الخاصة بصنف مرتجع تكون بمبلغ سالب، فهي تسمى إشعار دائن.

عند إعداد تحديث الفاتورة لمعالجة المجموعة، يجب أن يكون لأمر المبيعات من نوع **الأمر المرجع** بند مرتجع بالحالة **مستلم**، والذي يشير إلى أنه تم تحديث كشف التعبئة الخاص بالأمر.

## <a name="post-an-invoice-for-a-return-order"></a>ترحيل فاتورة لأمر مرتجع

1.  انقر فوق **حسابات مدينة** \> **عام** \> **أوامر المبيعات** \> **كل أوامر المبيعات**.

2.  حدد أمر مبيعات والذي يتم عرض **الأمر المرجع** له في الحقل **نوع أمر**.

3.  في جزء الإجراءات، في علامة التبويب **الفاتورة**، في المجموعة **إنشاء**، انقر فوق **فاتورة**.

4.  في علامة تبويب **المعلمات**، حدد خانة الاختيار **ترحيل**.

5.  راجع المعلومات الموجودة في النموذج وقم أي تغييرات ضرورية.

6.  وانقر فوق **موافق**. تم ترحيل إشعار الدائن.

## <a name="see-also"></a>راجع أيضًا

[تحديثات كشف التعبئة للمرتجعات](packing-slip-updates-returns.md)

  


