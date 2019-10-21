---
title: تضمين تطبيقات PowerApps في Dynamics 365‏ - Core HR
description: يشرح هذا المقال كيفية حل هذه المشكلة التي يختفي فيها عنصر قائمة PowerApps من الوحدة النمطية "إدارة النظام".
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
ms.openlocfilehash: 4fbc24c5ceb73389b84b125eb942ac31757928aa
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008420"
---
# <a name="embed-powerapps-apps-in-core-hr"></a>تضمين تطبيقات PowerApps في Core HR

[!include [banner](includes/banner.md)]

**إصدار**

اختفى عنصر قائمة **PowerApps** من الوحدة النمطية **إدارة النظام**.

**السبب**

تم تغيير تصميم واجهة المستخدم، وتم الآن تضمين Microsoft PowerApps في نموذج التخصيص القياسي.

**الدقة**

تم تغيير الطريقة التي يتم من خلالها تضمين تطبيقات PowerApps. تمت الآن إضافة تطبيقات PowerApps من خلال نموذج التخصيص. يمكنك إضافة تطبيقات PowerApps إلى معظم الصفحات تقريبًا في Microsoft Dynamics 365 Talent.

للحصول على معلومات تفصيلية حول كيفية تضمين تطبيقات PowerApps في Talent، راجع [تضمين تطبيقات PowerApps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

يجب أن تتم ترقية أي عميل PowerApps قام بتضمين التطبيقات قبل التغيير إلى النموذج الجديد.

يقع زر **PowerApps** في الزاوية اليسرى العليا في كل صفحة من صفحات Talent تقريبًا. يمكنك استخدام هذا الزر لإدراج تطبيق PowerApps.

فيما يلي مثال على ذلك.

1. انتقل إلى **إدارة العاملين \> الارتباطات \> العاملون \> الموظفون**.
2. حدد زر **PowerApps**، ثم حدد **إدراج PowerApp**.

    ![زر PowerApps](media/png.png)

3. أكمل الحقول في مربع حوار **إدراج PowerApp**.

    ![إدراج مربع حوار PowerApp](media/insert-powerapp.png)

بدلًا من ذلك، اتبع الخطوات التالية.

1. في صفحة جزء الإجراءات، في علامة التبويب **خيارات**، في مجموعة **تخصيص**، حدد **تخصيص هذا النموذج**

    ![تخصيص مجموعة في علامة التبويب خيارات](media/options.png)

    يظهر شريط أدوات التخصيص.

2. على شريط الأدوات، حدد **إدراج \> PowerApp**.

    ![إدراج تطبيق PowerApps باستخدام شريط أدوات التخصيص](media/powerapp-bar.png)
