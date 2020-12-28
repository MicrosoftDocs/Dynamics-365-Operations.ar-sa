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
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="bcf0f-103">بإمكان المستخدم الوصول إلى Human Resources ولكن ليس إلى تطبيق Onboard أو Attract</span><span class="sxs-lookup"><span data-stu-id="bcf0f-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bcf0f-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="bcf0f-104">**Environment details**</span></span>

- <span data-ttu-id="bcf0f-105">تم تنفيذ عملية نشر Microsoft Dynamics Lifecycle Services (LCS) بواسطة المستخدم أ.</span><span class="sxs-lookup"><span data-stu-id="bcf0f-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="bcf0f-106">قام المستخدم أ بإضافة المستخدم ب كمستخدم إلى Microsoft Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="bcf0f-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="bcf0f-107">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="bcf0f-107">**Issue**</span></span>

<span data-ttu-id="bcf0f-108">يمكن للمستخدم ب الوصول إلى Human Resources، ولا يمكنه الوصول إلى Talent أو Attract أو Talent: تطبيق Onboard.</span><span class="sxs-lookup"><span data-stu-id="bcf0f-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="bcf0f-109">عندما يحاول المستخدم الانتقال إلى **تجربة التطبيقات**، فسوف يتم نقله إلى بيئة تجريبية بدلًا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="bcf0f-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="bcf0f-110">**الحل**</span><span class="sxs-lookup"><span data-stu-id="bcf0f-110">**Solution**</span></span>

<span data-ttu-id="bcf0f-111">يجب أن تعين إلى المستخدم ب الحقوق التي تخول له عرض بيئة Microsoft Power Apps التي قام المستخدم أ بإنشائها خلال عملية التوفير.</span><span class="sxs-lookup"><span data-stu-id="bcf0f-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="bcf0f-112">لمزيد من المعلومات، راجع قسم "منح الوصول إلى البيئة" في [توفير Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="bcf0f-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="bcf0f-113">**حل طويل الأجل**</span><span class="sxs-lookup"><span data-stu-id="bcf0f-113">**Long-term solution**</span></span>

<span data-ttu-id="bcf0f-114">يضع Microsoft في الاعتبار تعيين الحقوق المناسبة لتطبيق Onboard و Attract عند إضافة مستخدم إلى Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bcf0f-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
