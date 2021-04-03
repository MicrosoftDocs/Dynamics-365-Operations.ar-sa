---
title: لا يظهر Human Resources في تطبيقات Microsoft Dynamics 365
description: يتناول هذا المقال ما يجب عليك فعله إذا لم تتمكن من رؤية تطبيق Microsoft Dynamics 365 Human Resources بين تطبيقات Microsoft Dynamics 365.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9be1c2b862a01d6f14ad98dbcb01e061649c6af0
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463974"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>لا يظهر Human Resources في تطبيقات Microsoft Dynamics 365

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**إصدار**

لا يظهر Dynamics 365 Human Resources للعميل بين تطبيقات Microsoft Dynamics 365.

**الدقة**

يجب إضافة المستخدم إلى دور أداة إنشاء البيئة للبيئة في Microsoft Power Apps.

1. يجب على المستخدم المسؤول الذي لديه ترخيص Power Apps Plan 2 فتح مدخل إدارة [Power Apps](https://preview.admin.powerapps.com/).

2. حدد **البيئات**، ثم حدد البيئة الصحيحة لـ Human Resources.

3. في علامة تبويب **الأمان**، في علامة تبويب **أدوار البيئة**، حدد **أداة إنشاء البيئة**.

    ![علامة تبويب أدوار البيئة](media/environment-roles.png)

4. على علامة التبويب **المستخدمون**، قم بإضافة المستخدم أو المؤسسة الخاصة بك.

    ![علامة التبويب المستخدمون](media/environment-maker.png)

5. حدد **حفظ**.

6. يجب على المستخدم الآن تسجيل الدخول إلى [Microsoft Dynamics 365](https://home.dynamics.com/).

7. حدد **مزامنة** لتحديث تطبيقات المستخدم.

    ![زر المزامنة](media/get-more.png)

    بعد اكتمال المزامنة، سوف يظهر Human Resources في الصفحة الرئيسية.


[!INCLUDE[footer-include](../includes/footer-banner.md)]