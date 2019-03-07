---
title: تعذر إنشاء بيئة في مركز إدارة PowerApps
description: يشرح هذا الموضوع الخطوات التي يجب اتخاذها إذا تعذر على المسؤول إنشاء بيئة في مركز إدارة Microsoft PowerApps.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "303159"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="83286-103">لا يمكن إنشاء بيئة في مركز إدارة PowerApps</span><span class="sxs-lookup"><span data-stu-id="83286-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83286-104">**المشكلة**</span><span class="sxs-lookup"><span data-stu-id="83286-104">**Issue**</span></span>

- <span data-ttu-id="83286-105">يتعذر على مسؤول المستأجر/البيئة إنشاء بيئة في مركز إدارة Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="83286-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="83286-106">لم يتم تعيين ترخيص يمنح المستخدمين حق تنفيذ خطوة إنشاء البيئة مباشرة إلى المستخدم الذي يقوم بتنفيذ هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="83286-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="83286-107">**الحل**</span><span class="sxs-lookup"><span data-stu-id="83286-107">**Solution**</span></span>

<span data-ttu-id="83286-108">تأكد من قيام مسؤول المستأجر بتعيين ترخيص PowerApps P2 صالح مباشرة إلى المستخدم الذي سوف يقوم بتنفيذ خطوة إنشاء البيئة.</span><span class="sxs-lookup"><span data-stu-id="83286-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="83286-109">فيما يلي خطط خدمة Microsoft Dynamics التي توفر هذا الحق.</span><span class="sxs-lookup"><span data-stu-id="83286-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="83286-110">وحدة حفظ مخزون المنتج الكلي (SKU)</span><span class="sxs-lookup"><span data-stu-id="83286-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="83286-111">خطة خدمة PowerApps P2</span><span class="sxs-lookup"><span data-stu-id="83286-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="83286-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="83286-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="83286-113">PowerApps لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="83286-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="83286-114">خطة Microsoft Dynamics 365، Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="83286-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="83286-115">PowerApps لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="83286-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="83286-116">لاحظ أن وحدات Microsoft Office SKU مختلفة توفر الحق أيضًا، بالإضافة إلى وحدات SKU مستقلة الخطة 2 من PowerApps.</span><span class="sxs-lookup"><span data-stu-id="83286-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="83286-117">النقطة المهمة هي وجود إحدى وحدات SKU.</span><span class="sxs-lookup"><span data-stu-id="83286-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="83286-118">الانتقال إلى [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="83286-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="83286-119">إنشاء البيئات باتباع الإرشادات الموجودة في [توفير Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="83286-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
