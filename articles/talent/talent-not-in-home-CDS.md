---
title: عدم ظهور Talent بين تطبيقات Microsoft Dynamics 365 (Common Data Service 1.0)
description: يشرح هذا الموضوع ما يجب عليك فعله إذا لم تتمكن من رؤية تطبيق Microsoft Dynamics 365 for Talent بين تطبيقات Microsoft Dynamics 365.
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
ms.openlocfilehash: ad5add2b572ccb6bff175806b965f63b53986152
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517285"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="603df-103">عدم ظهور Talent بين تطبيقات Microsoft Dynamics 365 (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="603df-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="603df-104">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="603df-104">**Issue**</span></span>

<span data-ttu-id="603df-105">يتعذر على العميل رؤية تطبيق Microsoft Dynamics 365 for Talent بين تطبيقات Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="603df-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="603df-106">**‏‏الدقة**</span><span class="sxs-lookup"><span data-stu-id="603df-106">**Resolution**</span></span>

<span data-ttu-id="603df-107">يجب إضافة المستخدم إلى دور أداة إنشاء البيئة للبيئة في Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="603df-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="603df-108">يجب على المستخدم المسؤول الذي لديه ترخيص PowerApps Plan 2 فتح [مدخل إدارة PowerApps](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="603df-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="603df-109">حدد **البيئات**، ثم حدد البيئة الصحيحة لـ Talent.</span><span class="sxs-lookup"><span data-stu-id="603df-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="603df-110">في علامة تبويب **الأمان**، في علامة تبويب **أدوار البيئة** ، حدد **أداة إنشاء البيئة**.</span><span class="sxs-lookup"><span data-stu-id="603df-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![علامة تبويب أدوار البيئة](media/environment-roles.png)

4. <span data-ttu-id="603df-112">على علامة التبويب **المستخدمون**، قم بإضافة المستخدم أو المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="603df-112">On the **Users** tab, add the user or your organization.</span></span>

    ![علامة التبويب المستخدمون](media/environment-maker.png)

5. <span data-ttu-id="603df-114">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="603df-114">Select **Save**.</span></span>
6. <span data-ttu-id="603df-115">يجب على المستخدم الآن تسجيل الدخول إلى [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="603df-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="603df-116">حدد **مزامنة** لتحديث تطبيقات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="603df-116">Select **Sync** to update the user apps.</span></span>

    ![زر المزامنة](media/get-more.png)

    <span data-ttu-id="603df-118">بعد اكتمال المزامنة، سوف يظهر Talent في الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="603df-118">After synchronization is completed, Talent will appear on the home page.</span></span>
