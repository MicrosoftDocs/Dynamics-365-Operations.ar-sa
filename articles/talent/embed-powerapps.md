---
title: تضمين تطبيقات Power Apps في Dynamics 365 Human Resources
description: يشرح هذا المقال كيفية حل هذه المشكلة التي يختفي فيها عنصر قائمة Microsoft Power Apps من الوحدة النمطية "إدارة النظام".
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460169"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a>تضمين تطبيقات Power Apps في Dynamics 365 Human Resources

**إصدار**

اختفى عنصر قائمة **Power Apps** من الوحدة النمطية **إدارة النظام**.

**السبب**

تم تغيير تصميم واجهة المستخدم، وتم الآن تضمين Microsoft Power Apps في نموذج التخصيص القياسي.

**الدقة**

تم تغيير الطريقة التي يتم من خلالها تضمين Power Apps. تمت الآن إضافة Power Apps من خلال نموذج التخصيص. يمكنك إضافة Power Apps إلى معظم الصفحات تقريبًا في Microsoft Dynamics 365 Talent.

للحصول على معلومات تفصيلية حول كيفية تضمين Power Apps في Talent، راجع [تضمين Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

يجب أن تتم ترقية أي عميل Power Apps قام بتضمين التطبيقات قبل التغيير إلى النموذج الجديد.

يقع زر **Power Apps** في الزاوية اليسرى العليا في كل صفحة من صفحات Talent تقريبًا. يمكنك استخدام هذا الزر لإدراج تطبيقات.

فيما يلي مثال على ذلك.

1. انتقل إلى **إدارة العاملين \> الارتباطات \> العاملون \> الموظفون**.
2. حدد الزر **Power Apps**، ثم حدد **إضافة تطبيق من Power Apps**.

    ![زر Power Apps](media/png.png)

3. أكمل الحقول في مربع الحوار **إضافة تطبيق من Power Apps**.

    ![مربع الحوار إضافة تطبيق من Power Apps](media/insert-powerapp.png)

بدلًا من ذلك، اتبع الخطوات التالية.

1. في جزء الإجراءات بالصفحة، في علامة التبويب **الخيارات**، في مجموعة **تخصيص**، حدد **تخصيص هذه الصفحة**

    ![تخصيص مجموعة في علامة التبويب خيارات](media/options.png)

    يظهر شريط أدوات التخصيص.

2. في شريط الأدوات، حدد **إضافة تطبيق من Power Apps**.

    ![إضافة تطبيق من Power Apps باستخدام شريط أدوات التخصيص](media/powerapp-bar.png)
