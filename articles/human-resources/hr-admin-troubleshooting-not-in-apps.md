---
title: لا يظهر Human Resources في تطبيقات Microsoft Dynamics 365
description: يتناول هذا المقال ما يجب عليك فعله إذا لم تتمكن من رؤية تطبيق Microsoft Dynamics 365 Human Resources بين تطبيقات Microsoft Dynamics 365.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d39e6ef4168f08f20b92979a296ed088744ad0da
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008032"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="a7d6c-103">لا يظهر Human Resources في تطبيقات Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a7d6c-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="a7d6c-104">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="a7d6c-104">**Issue**</span></span>

<span data-ttu-id="a7d6c-105">لا يظهر Dynamics 365 Human Resources للعميل بين تطبيقات Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="a7d6c-106">**الدقة**</span><span class="sxs-lookup"><span data-stu-id="a7d6c-106">**Resolution**</span></span>

<span data-ttu-id="a7d6c-107">يجب إضافة المستخدم إلى دور أداة إنشاء البيئة للبيئة في Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="a7d6c-108">يجب على المستخدم المسؤول الذي لديه ترخيص Power Apps Plan 2 فتح مدخل إدارة [Power Apps](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="a7d6c-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="a7d6c-109">حدد **البيئات**، ثم حدد البيئة الصحيحة لـ Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="a7d6c-110">في علامة تبويب **الأمان**، في علامة تبويب **أدوار البيئة** ، حدد **أداة إنشاء البيئة**.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![علامة تبويب أدوار البيئة](media/environment-roles.png)

4. <span data-ttu-id="a7d6c-112">على علامة التبويب **المستخدمون**، قم بإضافة المستخدم أو المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-112">On the **Users** tab, add the user or your organization.</span></span>

    ![علامة التبويب المستخدمون](media/environment-maker.png)

5. <span data-ttu-id="a7d6c-114">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-114">Select **Save**.</span></span>

6. <span data-ttu-id="a7d6c-115">يجب على المستخدم الآن تسجيل الدخول إلى [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="a7d6c-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="a7d6c-116">حدد **مزامنة** لتحديث تطبيقات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-116">Select **Sync** to update the user apps.</span></span>

    ![زر المزامنة](media/get-more.png)

    <span data-ttu-id="a7d6c-118">بعد اكتمال المزامنة، سوف يظهر Human Resources في الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>
