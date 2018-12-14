---
title: "يمكن للمستخدم الوصول إلى Core HR ولكن ليس إلى تطبيق Onboard أو Attract"
description: "يتناول هذا الموضوع كيفية حل هذه المشكلة، حيث يمكن للمستخدم الوصول إلى Microsoft Dynamics 365 for Talent Core HR، ولكن لا يمكنه الوصول إلى تطبيق Attract أو Onboard."
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
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: ar-sa
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>يمكن للمستخدم الوصول إلى Core HR ولكن ليس إلى تطبيق Onboard أو Attract

[!include [banner](includes/banner.md)]

**تفاصيل البيئة**

- تم نشر  Microsoft Dynamics Lifecycle Services (LCS) بواسطة المستخدم أ.
- قام المستخدم أ بإضافة المستخدم ب كمستخدم إلى Microsoft Dynamics 365 for Talent Core HR.

**المشكلة**

يمكن للمستخدم ب الوصول إلى Core HR، ولا يمكنه الوصول إلى Talent أو Attract أو Talent: تطبيق Onboard. عندما يحاول المستخدم الانتقال إلى **تجربة التطبيقات**، فسوف يتم نقله إلى بيئة تجريبية بدلًا من ذلك.

**الحل**

يجب تعيين المستخدم ب للحقوق التي تخول له عرض بيئة Microsoft PowerApps التي قام المستخدم أ بإنشائها خلال عملية التوفير.

لمزيد من المعلومات، راجع قسم "منح الوصول إلى البيئة" في [توفير Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

**حل طويل الأجل**

يضع Microsoft في الاعتبار تعيين الحقوق المناسبة لتطبيق Onboard و Attract عند إضافة مستخدم إلى Core HR.

