---
title: مستوى حساب التكلفة
description: يصف هذا الموضوع مستوى قائمة مكونات الصنف (BOM) الذي يسمى مستوى حساب التكلفة. يستثني مستوى BOM هذا أوامر الإنتاج والأوامر الدفعية من حساباته.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421279"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="6acc1-104">مستوى حساب التكلفة</span><span class="sxs-lookup"><span data-stu-id="6acc1-104">Cost calculation level</span></span>

<span data-ttu-id="6acc1-105">يستثني بمستوى قائمة مكونات صنف (BOM) المسمى **مستوى حساب التكلفة** أوامر الإنتاج والأوامر الدفعية من حساباته.</span><span class="sxs-lookup"><span data-stu-id="6acc1-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="6acc1-106">يستخدم النظام هذا المستوى عند تشغيل حسابات التكلفة في إصدارات التكاليف.</span><span class="sxs-lookup"><span data-stu-id="6acc1-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="6acc1-107">في بعض العمليات، مثل إعادة الحساب وإغلاق المخزون، يستخدم النظام مستوى BOM **مستوى التكلفة** بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="6acc1-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="6acc1-108">يعرض السيناريو البسيط التالي الاختلافات بين مستوى BOM **مستوى حساب التكلفة** ومستوى BOM **مستوى التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="6acc1-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="6acc1-109">لديك ثلاثة منتجات: A وB وC. المنتج C هو مكون المنتج B، والمنتج B هو مكون المنتج A.</span><span class="sxs-lookup"><span data-stu-id="6acc1-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="6acc1-110">يعيّن **مستوى التكلفة** مستويات BOM التالية:</span><span class="sxs-lookup"><span data-stu-id="6acc1-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6acc1-111">**المنتج A:** 0</span><span class="sxs-lookup"><span data-stu-id="6acc1-111">**Product A:** 0</span></span>
    - <span data-ttu-id="6acc1-112">**المنتج B:** 1</span><span class="sxs-lookup"><span data-stu-id="6acc1-112">**Product B:** 1</span></span>
    - <span data-ttu-id="6acc1-113">**المنتج C:** 2</span><span class="sxs-lookup"><span data-stu-id="6acc1-113">**Product C:** 2</span></span>

- <span data-ttu-id="6acc1-114">يعيّن **مستوى حساب التكاليف** مستويات BOM التالية:</span><span class="sxs-lookup"><span data-stu-id="6acc1-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6acc1-115">**المنتج A:** 0</span><span class="sxs-lookup"><span data-stu-id="6acc1-115">**Product A:** 0</span></span>
    - <span data-ttu-id="6acc1-116">**المنتج B:** 1</span><span class="sxs-lookup"><span data-stu-id="6acc1-116">**Product B:** 1</span></span>
    - <span data-ttu-id="6acc1-117">**المنتج C:** 2</span><span class="sxs-lookup"><span data-stu-id="6acc1-117">**Product C:** 2</span></span>

<span data-ttu-id="6acc1-118">وعندئذ يتم إنشاء أمر إنتاج للمنتج C، ويُضاف المنتج A إلى BOM أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="6acc1-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="6acc1-119">بعد تقدير الأمر، يتم تحديث مستويات BOM بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="6acc1-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="6acc1-120">يعيّن **مستوى التكلفة** مستويات BOM التالية:</span><span class="sxs-lookup"><span data-stu-id="6acc1-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6acc1-121">**المنتج B:** 1</span><span class="sxs-lookup"><span data-stu-id="6acc1-121">**Product B:** 1</span></span>
    - <span data-ttu-id="6acc1-122">**المنتج C:** 2</span><span class="sxs-lookup"><span data-stu-id="6acc1-122">**Product C:** 2</span></span>
    - <span data-ttu-id="6acc1-123">**المنتج A:** 3</span><span class="sxs-lookup"><span data-stu-id="6acc1-123">**Product A:** 3</span></span>

- <span data-ttu-id="6acc1-124">يعيّن **مستوى حساب التكاليف** مستويات BOM التالية:</span><span class="sxs-lookup"><span data-stu-id="6acc1-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6acc1-125">**المنتج A:** 0</span><span class="sxs-lookup"><span data-stu-id="6acc1-125">**Product A:** 0</span></span>
    - <span data-ttu-id="6acc1-126">**المنتج B:** 1</span><span class="sxs-lookup"><span data-stu-id="6acc1-126">**Product B:** 1</span></span>
    - <span data-ttu-id="6acc1-127">**المنتج C:** 2</span><span class="sxs-lookup"><span data-stu-id="6acc1-127">**Product C:** 2</span></span>

<span data-ttu-id="6acc1-128">يضمن هذا السلوك عدم تأثير قوائم BOMs لأوامر الإنتاج على حسابات التكلفة اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="6acc1-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
