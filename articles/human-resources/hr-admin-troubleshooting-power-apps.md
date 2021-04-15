---
title: لا يمكن إنشاء بيئة في مركز إدارة Power Apps
description: يشرح هذا المقال الخطوات التي يجب اتخاذها إذا تعذر على المسؤول إنشاء بيئة في مركز إدارة Microsoft Power Apps.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f1a086f1b710de9bad898abc740286c174ae3be7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797975"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="13033-103">لا يمكن إنشاء بيئة في مركز إدارة Power Apps</span><span class="sxs-lookup"><span data-stu-id="13033-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="13033-104">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="13033-104">**Issue**</span></span>

- <span data-ttu-id="13033-105">يتعذر على مسؤول المستأجر/البيئة إنشاء بيئة في مركز إدارة Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="13033-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="13033-106">لا يمتلك المستخدم ترخيصًا يمنح الحق في إنشاء البيئات.</span><span class="sxs-lookup"><span data-stu-id="13033-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="13033-107">**الحل**</span><span class="sxs-lookup"><span data-stu-id="13033-107">**Solution**</span></span>

<span data-ttu-id="13033-108">تأكد من أن مسؤول المستاجر قد قام بتعيين ترخيص Power Apps P2 صالح للمستخدم الذي يقوم بإنشاء البيئة.</span><span class="sxs-lookup"><span data-stu-id="13033-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="13033-109">توفر خطة خدمة Microsoft Dynamics التالية أذونات لإنشاء بيئات:</span><span class="sxs-lookup"><span data-stu-id="13033-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="13033-110">وحدة حفظ مخزون المنتج الكلي (SKU)</span><span class="sxs-lookup"><span data-stu-id="13033-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="13033-111">خطة خدمة Power Apps P2</span><span class="sxs-lookup"><span data-stu-id="13033-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="13033-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="13033-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="13033-113">Power Apps لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="13033-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="13033-114">خطة Microsoft Dynamics 365، Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="13033-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="13033-115">Power Apps لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="13033-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="13033-116">لاحظ أن وحدات Microsoft Office المختلفة توفر الحق أيضًا، بالإضافة إلى وحدات SKU المستقلة للخطة 2 من Power Apps.</span><span class="sxs-lookup"><span data-stu-id="13033-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="13033-117">النقطة المهمة هي وجود إحدى وحدات SKU.</span><span class="sxs-lookup"><span data-stu-id="13033-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="13033-118">الانتقال إلى [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="13033-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="13033-119">إنشاء البيئات باتباع الإرشادات الموجودة في [توفير Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="13033-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]