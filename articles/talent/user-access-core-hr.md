---
title: بإمكان المستخدم الوصول إلى Human Resources ولكن ليس إلى تطبيق Onboard أو Attract
description: يتناول هذا الموضوع كيفية حل هذه المشكلة، حيث يمكن للمستخدم الوصول إلى Microsoft Dynamics 365 Talent - Human Resources، ولكن لا يمكنه الوصول إلى تطبيق Attract أو Onboard.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460193"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>بإمكان المستخدم الوصول إلى Human Resources ولكن ليس إلى تطبيق Onboard أو Attract

[!include [banner](includes/banner.md)]

**تفاصيل البيئة**

- تم تنفيذ عملية نشر Microsoft Dynamics Lifecycle Services (LCS) بواسطة المستخدم أ.
- قام المستخدم أ بإضافة المستخدم ب كمستخدم إلى Microsoft Dynamics 365 Human Resources .

**إصدار**

يمكن للمستخدم ب الوصول إلى Human Resources، ولا يمكنه الوصول إلى Talent أو Attract أو Talent: تطبيق Onboard. عندما يحاول المستخدم الانتقال إلى **تجربة التطبيقات**، فسوف يتم نقله إلى بيئة تجريبية بدلًا من ذلك.

**الحل**

يجب أن تعين إلى المستخدم ب الحقوق التي تخول له عرض بيئة Microsoft Power Apps التي قام المستخدم أ بإنشائها خلال عملية التوفير.

لمزيد من المعلومات، راجع قسم "منح الوصول إلى البيئة" في [توفير Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**حل طويل الأجل**

يضع Microsoft في الاعتبار تعيين الحقوق المناسبة لتطبيق Onboard و Attract عند إضافة مستخدم إلى Human Resources.
