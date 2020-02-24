---
title: لا يمكن إنشاء بيئة في مركز إدارة Power Apps
description: يشرح هذا المقال الخطوات التي يجب اتخاذها إذا تعذر على المسؤول إنشاء بيئة في مركز إدارة Microsoft Power Apps.
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
ms.openlocfilehash: f4c75706183a3d6c961852395e464d46ba3ec1f2
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007926"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="012c1-103">لا يمكن إنشاء بيئة في مركز إدارة Power Apps</span><span class="sxs-lookup"><span data-stu-id="012c1-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="012c1-104">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="012c1-104">**Issue**</span></span>

- <span data-ttu-id="012c1-105">يتعذر على مسؤول المستأجر/البيئة إنشاء بيئة في مركز إدارة Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="012c1-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="012c1-106">لم يتم تعيين ترخيص يمنح المستخدمين حق تنفيذ خطوة إنشاء البيئة مباشرة إلى المستخدم الذي يقوم بتنفيذ هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="012c1-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="012c1-107">**الحل**</span><span class="sxs-lookup"><span data-stu-id="012c1-107">**Solution**</span></span>

<span data-ttu-id="012c1-108">تأكد من قيام مسؤول المستأجر بتعيين ترخيص Power Apps P2 صالح مباشرة إلى المستخدم الذي سوف يقوم بتنفيذ خطوة إنشاء البيئة.</span><span class="sxs-lookup"><span data-stu-id="012c1-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="012c1-109">فيما يلي خطط خدمة Microsoft Dynamics التي توفر هذا الحق.</span><span class="sxs-lookup"><span data-stu-id="012c1-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="012c1-110">وحدة حفظ مخزون المنتج الكلي (SKU)</span><span class="sxs-lookup"><span data-stu-id="012c1-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="012c1-111">خطة خدمة Power Apps P2</span><span class="sxs-lookup"><span data-stu-id="012c1-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="012c1-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="012c1-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="012c1-113">Power Apps لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="012c1-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="012c1-114">خطة Microsoft Dynamics 365، Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="012c1-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="012c1-115">Power Apps لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="012c1-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="012c1-116">لاحظ أن وحدات Microsoft Office المختلفة توفر الحق أيضًا، بالإضافة إلى وحدات SKU المستقلة للخطة 2 من Power Apps.</span><span class="sxs-lookup"><span data-stu-id="012c1-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="012c1-117">النقطة المهمة هي وجود إحدى وحدات SKU.</span><span class="sxs-lookup"><span data-stu-id="012c1-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="012c1-118">الانتقال إلى [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="012c1-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="012c1-119">إنشاء البيئات باتباع الإرشادات الموجودة في [توفير Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="012c1-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
