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

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="06acb-103">عدم ظهور Talent بين تطبيقات Microsoft Dynamics 365 (CDS1.0)</span><span class="sxs-lookup"><span data-stu-id="06acb-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06acb-104">**المشكلة**</span><span class="sxs-lookup"><span data-stu-id="06acb-104">**Issue**</span></span>

<span data-ttu-id="06acb-105">العميل لا يرى تطبيق Microsoft Dynamics 365 for Talent بين تطبيقات Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="06acb-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="06acb-106">**‏‏الدقة**</span><span class="sxs-lookup"><span data-stu-id="06acb-106">**Resolution**</span></span>

<span data-ttu-id="06acb-107">يجب إضافة المستخدم إلى دور أداة إنشاء البيئة للبيئة في Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="06acb-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="06acb-108">يجب على المستخدم المسؤول الذي لديه ترخيص PowerApps Plan 2 فتح [مدخل إدارة PowerApps](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="06acb-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="06acb-109">حدد **البيئات**، ثم حدد البيئة الصحيحة لـ Talent.</span><span class="sxs-lookup"><span data-stu-id="06acb-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="06acb-110">في علامة تبويب **الأمان**، في علامة تبويب **أدوار البيئة** ، حدد **أداة إنشاء البيئة**.</span><span class="sxs-lookup"><span data-stu-id="06acb-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![علامة تبويب أدوار البيئة](media/environment-roles.png)

4. <span data-ttu-id="06acb-112">على علامة التبويب **المستخدمون**، قم بإضافة المستخدم أو المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="06acb-112">On the **Users** tab, add the user or your organization.</span></span>

    ![علامة التبويب المستخدمون](media/environment-maker.png)

5. <span data-ttu-id="06acb-114">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="06acb-114">Select **Save**.</span></span>
6. <span data-ttu-id="06acb-115">يجب على المستخدم الآن تسجيل الدخول إلى [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="06acb-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="06acb-116">حدد **مزامنة** لتحديث تطبيقات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="06acb-116">Select **Sync** to update the user apps.</span></span>

    ![زر المزامنة](media/get-more.png)

    <span data-ttu-id="06acb-118">بعد اكتمال المزامنة، سوف يظهر Talent في الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="06acb-118">After synchronization is completed, Talent will appear on the home page.</span></span>

