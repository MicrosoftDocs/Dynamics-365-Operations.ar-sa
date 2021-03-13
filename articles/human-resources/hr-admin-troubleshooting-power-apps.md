---
title: لا يمكن إنشاء بيئة في مركز إدارة Power Apps
description: يشرح هذا المقال الخطوات التي يجب اتخاذها إذا تعذر على المسؤول إنشاء بيئة في مركز إدارة Microsoft Power Apps.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111337"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="41d4b-103">لا يمكن إنشاء بيئة في مركز إدارة Power Apps</span><span class="sxs-lookup"><span data-stu-id="41d4b-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="41d4b-104">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="41d4b-104">**Issue**</span></span>

- <span data-ttu-id="41d4b-105">يتعذر على مسؤول المستأجر/البيئة إنشاء بيئة في مركز إدارة Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="41d4b-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="41d4b-106">لا يمتلك المستخدم ترخيصًا يمنح الحق في إنشاء البيئات.</span><span class="sxs-lookup"><span data-stu-id="41d4b-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="41d4b-107">**الحل**</span><span class="sxs-lookup"><span data-stu-id="41d4b-107">**Solution**</span></span>

<span data-ttu-id="41d4b-108">تأكد من أن مسؤول المستاجر قد قام بتعيين ترخيص Power Apps P2 صالح للمستخدم الذي يقوم بإنشاء البيئة.</span><span class="sxs-lookup"><span data-stu-id="41d4b-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="41d4b-109">توفر خطة خدمة Microsoft Dynamics التالية أذونات لإنشاء بيئات:</span><span class="sxs-lookup"><span data-stu-id="41d4b-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="41d4b-110">وحدة حفظ مخزون المنتج الكلي (SKU)</span><span class="sxs-lookup"><span data-stu-id="41d4b-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="41d4b-111">خطة خدمة Power Apps P2</span><span class="sxs-lookup"><span data-stu-id="41d4b-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="41d4b-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="41d4b-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="41d4b-113">Power Apps لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="41d4b-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="41d4b-114">خطة Microsoft Dynamics 365، Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="41d4b-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="41d4b-115">Power Apps لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="41d4b-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="41d4b-116">لاحظ أن وحدات Microsoft Office المختلفة توفر الحق أيضًا، بالإضافة إلى وحدات SKU المستقلة للخطة 2 من Power Apps.</span><span class="sxs-lookup"><span data-stu-id="41d4b-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="41d4b-117">النقطة المهمة هي وجود إحدى وحدات SKU.</span><span class="sxs-lookup"><span data-stu-id="41d4b-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="41d4b-118">الانتقال إلى [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="41d4b-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="41d4b-119">إنشاء البيئات باتباع الإرشادات الموجودة في [توفير Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="41d4b-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
