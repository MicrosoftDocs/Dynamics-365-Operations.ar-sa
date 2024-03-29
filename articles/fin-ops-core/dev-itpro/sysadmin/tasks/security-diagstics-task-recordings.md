---
title: ‏‫تشخيصات الأمان‬ لتسجيلات المهام
description: توفر هذه المقالة معلومات عن كيفية تحليل متطلبات أذونات الأمان وإدارتها استنادًا إلى تسجيل مهمة.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.search.form: ''
ms.openlocfilehash: e564a0499cb1a5dc00fc027c20a027f9b454600c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272509"
---
# <a name="security-diagnostics-for-task-recordings"></a>‏‫تشخيصات الأمان‬ لتسجيلات المهام

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>قبل البدء

توفر هذه المقالة معلومات عن كيفية تحليل متطلبات أذونات الأمان وإدارتها استنادًا إلى تسجيل مهمة. قبل إكمال الخطوات الواردة في هذه المقالة، يجب أن يكون لديك تسجيل مهمة للعملية التجارية التي ترغب في تحليلها. لتسجيل عمليه تجاريه، راجع [موارد مسجل المهام‬‏‫](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>إدارة الأمان لتسجيل مهمة

1. انتقل إلى **إدارة النظام** > **الأمان** > **تشخيص الأمان لتسجيل المهام**.
2. افتح تسجيل المهام من موقعه. حدد **‬‏‫فتح من هذا الكمبيوتر الشخصي‬‏‫** أو **افتح من Lifecycle Services** ثم حدد **إغلاق**.
3. سيؤدي ذلك إلى فتح صفحة **تفاصيل عناصر قائمة الأمان** التي تسرد كائنات الأمان المطلوبة للعملية.

 > [!NOTE]
 > عناصر قائمة **الإجراءات** و **الإخراج** غير مضمّنة في القائمة.

4. في حقل **‏‫معرف المستخدم** حدد مستخدم. إذا لم يكن لدي المستخدم أذونات لبعض عناصر القائمة، فسيتم تحديث حقل **الأذونات المفقودة** إلى **نعم**.
  
  ![صفحة تفاصيل عنصر قائمة الأمان.](../media/Security-Menu-Item-Details.png)

5. حدد **إضافة مرجع** لعرض قائمة بكائنات الأمان، بما في ذلك الأدوار والمهام والامتيازات التي تمنح الاذن المفقود.
6. حدد كائن أمان من القائمة:

    - في حالة تحديد **الدور** حدد **إضافة دور إلى المستخدم**. سيؤدي ذلك إلى فتح صفحة **تعيين مستخدمين إلى أدوار**. لمزيد من المعلومات، راجع [تعيين مستخدمين إلى أدوار أمان‬](assign-users-security-roles.md).
    - في حالة تحديد **الرسوم** فحدد **إضافة رسوم إلى الدور** ، وحدد الأدوار التي يجب إضافه الرسوم إليها، ثم حدد **موافق**.
    - في حالة تحديد **الامتياز** فحدد **إضافة امتياز إلى الرسوم** ، وحدد الأدوار التي يجب إضافه الرسوم إليها، ثم حدد **موافق**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
