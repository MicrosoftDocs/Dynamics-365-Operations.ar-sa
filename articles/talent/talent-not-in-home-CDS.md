---
title: "عدم ظهور Talent بين تطبيقات Microsoft Dynamics 365 (CDS1.0)"
description: "يشرح هذا الموضوع ما يجب عليك فعله إذا لم يرى العميل تطبيق Microsoft Dynamics 365 for Talent من بين تطبيقات Microsoft Dynamics 365."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: ar-sa
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>عدم ظهور Talent بين تطبيقات Microsoft Dynamics 365 (CDS1.0)

[!include [banner](includes/banner.md)]

**المشكلة**

العميل لا يرى تطبيق Microsoft Dynamics 365 for Talent بين تطبيقات Microsoft Dynamics 365.

**‏‏الدقة**

يجب إضافة المستخدم إلى دور أداة إنشاء البيئة للبيئة في Microsoft PowerApps.

1. يجب على المستخدم المسؤول الذي لديه ترخيص PowerApps Plan 2 فتح [مدخل إدارة PowerApps](https://preview.admin.powerapps.com/).
2. حدد **البيئات**، ثم حدد البيئة الصحيحة لـ Talent.
3. في علامة تبويب **الأمان**، في علامة تبويب **أدوار البيئة** ، حدد **أداة إنشاء البيئة**.

    ![علامة تبويب أدوار البيئة](media/environment-roles.png)

4. على علامة التبويب **المستخدمون**، قم بإضافة المستخدم أو المؤسسة الخاصة بك.

    ![علامة التبويب المستخدمون](media/environment-maker.png)

5. حدد **حفظ**.
6. يجب على المستخدم الآن تسجيل الدخول إلى [Microsoft Dynamics 365](https://home.dynamics.com/).
7. حدد **مزامنة** لتحديث تطبيقات المستخدم.

    ![زر المزامنة](media/get-more.png)

    بعد اكتمال المزامنة، سوف يظهر Talent في الصفحة الرئيسية.

