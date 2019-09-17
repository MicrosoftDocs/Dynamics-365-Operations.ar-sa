---
title: يمكن للمستخدم الوصول إلى Core HR ولكن ليس إلى تطبيق Onboard أو Attract
description: يتناول هذا الموضوع كيفية حل هذه المشكلة، حيث يمكن للمستخدم الوصول إلى Microsoft Dynamics 365 for Talent Core HR، ولكن لا يمكنه الوصول إلى تطبيق Attract أو Onboard.
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
ms.openlocfilehash: 6fc27a4c137fef2f8d204d90366c316389da08e6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741696"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>بإمكان المستخدم الوصول إلى Core HR ولكن ليس إلى تطبيق Onboard أو Attract

[!include [banner](includes/banner.md)]

**تفاصيل البيئة**

- تم تنفيذ عملية نشر Microsoft Dynamics Lifecycle Services (LCS) بواسطة المستخدم أ.
- قام المستخدم أ بإضافة المستخدم ب كمستخدم إلى Microsoft Dynamics 365 for Talent Core HR.

**إصدار**

يمكن للمستخدم ب الوصول إلى Core HR، ولا يمكنه الوصول إلى Talent أو Attract أو Talent: تطبيق Onboard. عندما يحاول المستخدم الانتقال إلى **تجربة التطبيقات**، فسوف يتم نقله إلى بيئة تجريبية بدلًا من ذلك.

**الحل**

يجب أن تعين إلى المستخدم ب الحقوق التي تخول له عرض بيئة Microsoft PowerApps التي قام المستخدم أ بإنشائها خلال عملية التوفير.

لمزيد من المعلومات، راجع قسم "منح الوصول إلى البيئة" في [توفير Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**حل طويل الأجل**

يضع Microsoft في الاعتبار تعيين الحقوق المناسبة لتطبيق Onboard و Attract عند إضافة مستخدم إلى Core HR.
