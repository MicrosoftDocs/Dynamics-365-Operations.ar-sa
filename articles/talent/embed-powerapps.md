---
title: تضمين تطبيقات Power Apps في Dynamics 365‏ - Core HR
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830199"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a>تضمين تطبيقات Power Apps في Dynamics 365‏ - Core HR

[!include [banner](includes/banner.md)]

**إصدار**

اختفى عنصر قائمة **Power Apps** من الوحدة النمطية **إدارة النظام**.

**السبب**

تم تغيير تصميم واجهة المستخدم، وتم الآن تضمين Microsoft Power Apps في نموذج التخصيص القياسي.

**الدقة**

تم تغيير الطريقة التي يتم من خلالها تضمين Power Apps. تمت الآن إضافة Power Apps من خلال نموذج التخصيص. يمكنك إضافة Power Apps إلى معظم الصفحات تقريبًا في Microsoft Dynamics 365 Talent.

للحصول على معلومات تفصيلية حول كيفية تضمين Power Apps في Talent، راجع [تضمين Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

يجب أن تتم ترقية أي عميل Power Apps قام بتضمين التطبيقات قبل التغيير إلى النموذج الجديد.

يقع زر **Power Apps** في الزاوية اليسرى العليا في كل صفحة من صفحات Talent تقريبًا. يمكنك استخدام هذا الزر لإدراج Power Apps.

فيما يلي مثال على ذلك.

1. انتقل إلى **إدارة العاملين \> الارتباطات \> العاملون \> الموظفون**.
2. حدد زر **Power Apps**، ثم حدد **إدراج PowerApp**.

    ![زر Power Apps](media/png.png)

3. أكمل الحقول في مربع حوار **إدراج PowerApp**.

    ![إدراج مربع حوار PowerApp](media/insert-powerapp.png)

بدلًا من ذلك، اتبع الخطوات التالية.

1. في صفحة جزء الإجراءات، في علامة التبويب **خيارات**، في مجموعة **تخصيص**، حدد **تخصيص هذا النموذج**

    ![تخصيص مجموعة في علامة التبويب خيارات](media/options.png)

    يظهر شريط أدوات التخصيص.

2. على شريط الأدوات، حدد **إدراج \> PowerApp**.

    ![إدراج تطبيق Power Apps باستخدام شريط أدوات التخصيص](media/powerapp-bar.png)
