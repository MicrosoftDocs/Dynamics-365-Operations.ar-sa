---
title: مستوى الخدمة ووصفها
description: يشرح هذا المقال مستوى الخدمة ووصفها في إدارة الأصول.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 753ad36b1d01d1ce0594f477cf863ca0e4a1ac75
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879181"
---
# <a name="service-level-and-description"></a>مستوى الخدمة ووصفها

[!include [banner](../../includes/banner.md)]

 

عند إنشاء أمر عمل، قد ترغب في تحديد مستويات الخدمة له وإضافة وصف عام له. يمكنك إنشاء مستويات خدمة أمر العمل في الصفحة **مستويات خدمة أمر العمل** وإضافة الأوصاف في صفحة **وصف أمر العمل**.

## <a name="create-a-service-level"></a>إنشاء مستوى خدمة

1. حدد **إدارة الأصول** \> **الإعداد** \> **أوامر العمل** \> **مستوى الخدمة**.
2. حدد **جديد**.
3. في الحقل **مستوى الخدمة**، أدخل مستوى الخدمة (على سبيل المثال، رقم).
4. في حقل **الاسم**، أدخل اسمًا.

    على علامة التبويب السريعة **أوامر العمل**، يمكنك تحديد تواريخ وأوقات البدء والانتهاء المتوقعة. تحدد الحقول الموجودة على علامة التبويب السريعة الفترة التي يجب بدء وانتهاء أوامر العمل فيها. وتُستخدم لأوامر العمل التي يتم إنشاؤها يدويًا وأوامر العمل التي يتم إنشاؤها بناءً على طلبات الصيانة. 

5. في الحقل **يوم البدء**، أدخل عدد الأيام لتحديد الفترة التي يجب أن يبدأ خلالها أمر العمل. يتم حساب عدد الأيام من تاريخ إنشاء أمر العمل. على سبيل المثال، إذا كان يجب بدء أمر العمل عند إنشائه، أدخل **0**. إذا كان يجب بدء أمر العمل في خلال أسبوع من إنشائه، أدخل **7**.
6. لتعيين وقت بدء أمر العمل، بالإضافة إلى تاريخ بدء، قم بتعيين الخيار **تعيين وقت البدء** إلى **نعم**. ثم ادخل وقت البدء في الحقل **وقت البدء**. عند تعيين الخيار إلى **لا**، يتم استخدام الوقت الحالي من اليوم.
7. في الحقل **يوم الانتهاء**، أدخل عدد الأيام لتحديد الفترة التي يجب أن ينتهي خلالها أمر العمل. يتم حساب عدد الأيام من تاريخ بدء أمر العمل. على سبيل المثال، إذا كان من المفترض أن ينتهي أمر العمل في خلال أسبوع من تاريخ بدئه، فأدخل **7**.
8. لتعيين وقت انتهاء أمر العمل، بالإضافة إلى تاريخ انتهاء، قم بتعيين الخيار **تعيين وقت انتهاء** إلى **نعم**. ثم ادخل وقت الانتهاء في الحقل **وقت الانتهاء**. عند تعيين الخيار إلى **لا**، يتم استخدام الوقت الحالي من اليوم.
9. حدد **حفظ**.

![صفحة مستوى خدمة أوامر العمل.](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>إنشاء وصف

1. حدد **إدارة الأصول** \> **الإعداد** \> **أوامر العمل** \> **الأوصاف**.
2. حدد **جديد**.
3. في الحقل **الوصف**، أدخل الوصف.
4. حدد **حفظ**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]