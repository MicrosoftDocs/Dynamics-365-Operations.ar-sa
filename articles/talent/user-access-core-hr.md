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
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517254"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="73038-103">بإمكان المستخدم الوصول إلى Core HR ولكن ليس إلى تطبيق Onboard أو Attract</span><span class="sxs-lookup"><span data-stu-id="73038-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="73038-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="73038-104">**Environment details**</span></span>

- <span data-ttu-id="73038-105">تم تنفيذ عملية نشر Microsoft Dynamics Lifecycle Services (LCS) بواسطة المستخدم أ.</span><span class="sxs-lookup"><span data-stu-id="73038-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="73038-106">قام المستخدم أ بإضافة المستخدم ب كمستخدم إلى Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="73038-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="73038-107">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="73038-107">**Issue**</span></span>

<span data-ttu-id="73038-108">يمكن للمستخدم ب الوصول إلى Core HR، ولا يمكنه الوصول إلى Talent أو Attract أو Talent: تطبيق Onboard.</span><span class="sxs-lookup"><span data-stu-id="73038-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="73038-109">عندما يحاول المستخدم الانتقال إلى **تجربة التطبيقات**، فسوف يتم نقله إلى بيئة تجريبية بدلًا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="73038-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="73038-110">**الحل**</span><span class="sxs-lookup"><span data-stu-id="73038-110">**Solution**</span></span>

<span data-ttu-id="73038-111">يجب أن تعين إلى المستخدم ب الحقوق التي تخول له عرض بيئة Microsoft PowerApps التي قام المستخدم أ بإنشائها خلال عملية التوفير.</span><span class="sxs-lookup"><span data-stu-id="73038-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="73038-112">لمزيد من المعلومات، راجع قسم "منح الوصول إلى البيئة" في [توفير Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="73038-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="73038-113">**حل طويل الأجل**</span><span class="sxs-lookup"><span data-stu-id="73038-113">**Long-term solution**</span></span>

<span data-ttu-id="73038-114">يضع Microsoft في الاعتبار تعيين الحقوق المناسبة لتطبيق Onboard و Attract عند إضافة مستخدم إلى Core HR.</span><span class="sxs-lookup"><span data-stu-id="73038-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
