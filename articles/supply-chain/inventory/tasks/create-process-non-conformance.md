---
title: إنشاء ومعالجته توافق
description: يشرح هذا الموضوع كيفية تنفيذ إدارة عدم المطابقة استناداً إلى أمر جودة موجود.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0c0c4415f490219485b3d96fa678a317c1f12f2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204115"
---
# <a name="create-and-process-a-conformance"></a>إنشاء ومعالجته توافق

[!include [banner](../../includes/banner.md)]

يشرح هذا الموضوع كيفية تنفيذ إدارة عدم المطابقة استناداً إلى أمر جودة موجود. يمكنك تشغيل هذا التسجيل في شركة العرض التوضيحي USMF ويمكنك استخدام القيم المقترحة. عادة ما يتم تنفيذ هذا الإجراء بواسطة كاتب جودة.  كشرط مسبق، أكمل الإرشادات في [فحص جودة البضائع‬](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md). لمعالجة اعتماد عدم المطابقة، يجب أن تكون للمستخدم الذي يقوم بتشغيل تسجيل المهمة قيمة "اسم" معينة بصفحة "المستخدمين". لاستخدام ملاحظات المستند، يجب أيضًا تنشيط "معالجة المستندات" للمستخدم في خيارات المستخدم.


## <a name="select-a-quality-order"></a>تحديد أمر جودة
1. في جزء التنقل، انتقل إلى **الوحدات النمطية >‬ ‏‫إدارة المخزون > المهام الدورية‬ > إدارة الجودة > أوامر الجودة**.
2. في القائمة، حدد أمر الجودة الذي تم إنشاؤه في [فحص جودة البضائع](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).  

## <a name="create-a-nonconformance"></a>إنشاء عدم المطابقة
1. في جزء الإجراءات، حدد **استعلامات**.
2. حدد **حالات عدم المطابقة**.
3. حدد **جديد**.
4. في القائمة المنسدلة لحقل **نوع المشكلة**، حدد المشكلة التي تم العثور عليها أثناء عملية الفحص.  
5. حدد **موافق**.

## <a name="approvereject-a-nonconformance"></a>اعتماد/رفض عدم المطابقة
1. حدد **الوظائف**.
2. حدد **الموافقة على عدم المطابقة**. على سبيل المثال، قم باعتماد عدم المطابقة. يمكن ربط حالات عدم المطابقة الموافق عليها بالعمليات ذات الصلة لتسجيل العمل الذي يتم تنفيذه كجزء من معالجة عدم المطابقة وكما ورد في هذا الموضوع، معالجة التعامل مع التصحيح.  
3. حدد **نعم**.

## <a name="create-a-correction-action"></a>إنشاء إجراء تصحيح
1. حدد **التصحيحات**.
2. حدد **جديد**.
3. في الحقل **رقم الموظف‬** في الصف الجديد، حدد السجل المطلوب من القائمة المنسدلة.
4. انقر فوق **تحديد**.
5. حدد **إرفاق**. قم بإنشاء ملاحظة حول التصحيح. على سبيل المثال، يتمثل الإجراء في الاتصال بالمورد لمناقشة حالة عدم المطابقة.  
6. حدد **جديد**.
7. حدد **ملاحظة**. تبعًا لإعداد التقرير، يمكن طباعة أنواع مختلفة من المستندات على التقارير المتعلقة بإدارة عدم المطابقة.  
8. في حقل **الوصف**، اكتب قيمة.
9. قم بإغلاق الصفحة.

## <a name="maintain-a-correction"></a>الاحتفاظ بإجراء التصحيح
1. حدد **وضع علامة كمكتمل**.
2. حدد **موافق**.
3. قم بإغلاق الصفحة.

## <a name="close-a-nonconformance"></a>إغلاق حالة عدم مطابقة
1. حدد **الوظائف**.
2. حدد **إغلاق عدم المطابقة**.
3. حدد **نعم**.
4. قم بإغلاق الصفحات.
