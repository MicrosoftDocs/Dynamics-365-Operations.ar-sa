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

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="02053-103">يمكن للمستخدم الوصول إلى Core HR ولكن ليس إلى تطبيق Onboard أو Attract</span><span class="sxs-lookup"><span data-stu-id="02053-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="02053-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="02053-104">**Environment details**</span></span>

- <span data-ttu-id="02053-105">تم نشر  Microsoft Dynamics Lifecycle Services (LCS) بواسطة المستخدم أ.</span><span class="sxs-lookup"><span data-stu-id="02053-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="02053-106">قام المستخدم أ بإضافة المستخدم ب كمستخدم إلى Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="02053-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="02053-107">**المشكلة**</span><span class="sxs-lookup"><span data-stu-id="02053-107">**Issue**</span></span>

<span data-ttu-id="02053-108">يمكن للمستخدم ب الوصول إلى Core HR، ولا يمكنه الوصول إلى Talent أو Attract أو Talent: تطبيق Onboard.</span><span class="sxs-lookup"><span data-stu-id="02053-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="02053-109">عندما يحاول المستخدم الانتقال إلى **تجربة التطبيقات**، فسوف يتم نقله إلى بيئة تجريبية بدلًا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="02053-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="02053-110">**الحل**</span><span class="sxs-lookup"><span data-stu-id="02053-110">**Solution**</span></span>

<span data-ttu-id="02053-111">يجب تعيين المستخدم ب للحقوق التي تخول له عرض بيئة Microsoft PowerApps التي قام المستخدم أ بإنشائها خلال عملية التوفير.</span><span class="sxs-lookup"><span data-stu-id="02053-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="02053-112">لمزيد من المعلومات، راجع قسم "منح الوصول إلى البيئة" في [توفير Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="02053-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="02053-113">**حل طويل الأجل**</span><span class="sxs-lookup"><span data-stu-id="02053-113">**Long-term solution**</span></span>

<span data-ttu-id="02053-114">يضع Microsoft في الاعتبار تعيين الحقوق المناسبة لتطبيق Onboard و Attract عند إضافة مستخدم إلى Core HR.</span><span class="sxs-lookup"><span data-stu-id="02053-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>

