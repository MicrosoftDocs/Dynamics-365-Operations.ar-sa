---
title: لا يظهر Human Resources في تطبيقات Microsoft Dynamics 365
description: توضح هذه المقالة ما يجب فعله إذا لم يتم سرد Microsoft Dynamics 365 Human Resources بين تطبيقات Microsoft Dynamics ‏365.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d520ac06bcc0990714929c0fdd622516eda5f30
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872228"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>لا يظهر تطبيق Human Resources في تطبيقات Microsoft Dynamics ‏365


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**المشكلة**

لا يظهر Dynamics 365 Human Resources للعميل بين تطبيقات Microsoft Dynamics 365.

**الدقة**

يجب إضافة المستخدم إلى دور أداة إنشاء البيئة للبيئة في Microsoft Power Apps.

1. يجب على المستخدم المسؤول الذي لديه ترخيص Power Apps Plan 2 فتح مدخل إدارة [Power Apps](https://preview.admin.powerapps.com/).

2. حدد **البيئات**، ثم حدد البيئة الصحيحة لـ Human Resources.

3. في علامة تبويب **الأمان**، في علامة تبويب **أدوار البيئة**، حدد **أداة إنشاء البيئة**.

    ![علامة تبويب أدوار البيئة.](media/environment-roles.png)

4. على علامة التبويب **المستخدمون**، قم بإضافة المستخدم أو المؤسسة الخاصة بك.

    ![علامة التبويب المستخدمون.](media/environment-maker.png)

5. حدد **حفظ**.

6. يجب على المستخدم الآن تسجيل الدخول إلى [Microsoft Dynamics 365](https://home.dynamics.com/).

7. حدد **مزامنة** لتحديث تطبيقات المستخدم.

    ![زر المزامنة.](media/get-more.png)

    بعد اكتمال المزامنة، سوف يظهر Human Resources في الصفحة الرئيسية.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
