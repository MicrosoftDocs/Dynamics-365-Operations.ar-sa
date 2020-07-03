---
title: لا يظهر Human Resources في تطبيقات Microsoft Dynamics 365
description: يتناول هذا المقال ما يجب عليك فعله إذا لم تتمكن من رؤية تطبيق Microsoft Dynamics 365 Human Resources بين تطبيقات Microsoft Dynamics 365.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: cbf47b4673e1c97965bba7728e5669b7639c4d56
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431074"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>لا يظهر Human Resources في تطبيقات Microsoft Dynamics 365

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
