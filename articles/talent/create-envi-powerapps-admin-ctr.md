---
title: تعذر إنشاء بيئة في مركز إدارة PowerApps
description: يشرح هذا الموضوع الخطوات التي يجب اتخاذها إذا تعذر على المسؤول إنشاء بيئة في مركز إدارة Microsoft PowerApps.
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
ms.openlocfilehash: 97d44dc034cb8097fc0ecf9ac4e485425f097102
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517199"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="346b8-103">لا يمكن إنشاء بيئة في مركز إدارة PowerApps</span><span class="sxs-lookup"><span data-stu-id="346b8-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="346b8-104">**المشكلة**</span><span class="sxs-lookup"><span data-stu-id="346b8-104">**Issue**</span></span>

- <span data-ttu-id="346b8-105">يتعذر على مسؤول المستأجر/البيئة إنشاء بيئة في مركز إدارة Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="346b8-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="346b8-106">لم يتم تعيين ترخيص يمنح المستخدمين حق تنفيذ خطوة إنشاء البيئة مباشرة إلى المستخدم الذي يقوم بتنفيذ هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="346b8-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="346b8-107">**الحل**</span><span class="sxs-lookup"><span data-stu-id="346b8-107">**Solution**</span></span>

<span data-ttu-id="346b8-108">تأكد من قيام مسؤول المستأجر بتعيين ترخيص PowerApps P2 صالح مباشرة إلى المستخدم الذي سوف يقوم بتنفيذ خطوة إنشاء البيئة.</span><span class="sxs-lookup"><span data-stu-id="346b8-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="346b8-109">فيما يلي خطط خدمة Microsoft Dynamics التي توفر هذا الحق.</span><span class="sxs-lookup"><span data-stu-id="346b8-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="346b8-110">وحدة حفظ مخزون المنتج الكلي (SKU)</span><span class="sxs-lookup"><span data-stu-id="346b8-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="346b8-111">خطة خدمة PowerApps P2</span><span class="sxs-lookup"><span data-stu-id="346b8-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="346b8-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="346b8-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="346b8-113">PowerApps لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="346b8-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="346b8-114">خطة Microsoft Dynamics 365، Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="346b8-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="346b8-115">PowerApps لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="346b8-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="346b8-116">لاحظ أن وحدات Microsoft Office SKU مختلفة توفر الحق أيضًا، بالإضافة إلى وحدات SKU مستقلة الخطة 2 من PowerApps.</span><span class="sxs-lookup"><span data-stu-id="346b8-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="346b8-117">النقطة المهمة هي وجود إحدى وحدات SKU.</span><span class="sxs-lookup"><span data-stu-id="346b8-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="346b8-118">الانتقال إلى [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="346b8-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="346b8-119">إنشاء البيئات باتباع الإرشادات الموجودة في [توفير Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="346b8-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
