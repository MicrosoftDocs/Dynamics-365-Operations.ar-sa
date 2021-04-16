---
title: مستوى حساب التكلفة
description: يصف هذا الموضوع مستوى قائمة مكونات الصنف (BOM) الذي يسمى مستوى حساب التكلفة. يستثني مستوى BOM هذا أوامر الإنتاج والأوامر الدفعية من حساباته.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f7cde239107528a6bc2aeb0e424d024d4f3fb2a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839477"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="ff366-104">مستوى حساب التكلفة</span><span class="sxs-lookup"><span data-stu-id="ff366-104">Cost calculation level</span></span>

<span data-ttu-id="ff366-105">يستثني بمستوى قائمة مكونات صنف (BOM) المسمى **مستوى حساب التكلفة** أوامر الإنتاج والأوامر الدفعية من حساباته.</span><span class="sxs-lookup"><span data-stu-id="ff366-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="ff366-106">يستخدم النظام هذا المستوى عند تشغيل حسابات التكلفة في إصدارات التكاليف.</span><span class="sxs-lookup"><span data-stu-id="ff366-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="ff366-107">في بعض العمليات، مثل إعادة الحساب وإغلاق المخزون، يستخدم النظام مستوى BOM **مستوى التكلفة** بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="ff366-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="ff366-108">يعرض السيناريو البسيط التالي الاختلافات بين مستوى BOM **مستوى حساب التكلفة** ومستوى BOM **مستوى التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="ff366-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="ff366-109">لديك ثلاثة منتجات: A وB وC. المنتج C هو مكون المنتج B، والمنتج B هو مكون المنتج A.</span><span class="sxs-lookup"><span data-stu-id="ff366-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="ff366-110">يعيّن **مستوى التكلفة** مستويات BOM التالية:</span><span class="sxs-lookup"><span data-stu-id="ff366-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="ff366-111">**المنتج A:** 0</span><span class="sxs-lookup"><span data-stu-id="ff366-111">**Product A:** 0</span></span>
    - <span data-ttu-id="ff366-112">**المنتج B:** 1</span><span class="sxs-lookup"><span data-stu-id="ff366-112">**Product B:** 1</span></span>
    - <span data-ttu-id="ff366-113">**المنتج C:** 2</span><span class="sxs-lookup"><span data-stu-id="ff366-113">**Product C:** 2</span></span>

- <span data-ttu-id="ff366-114">يعيّن **مستوى حساب التكاليف** مستويات BOM التالية:</span><span class="sxs-lookup"><span data-stu-id="ff366-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="ff366-115">**المنتج A:** 0</span><span class="sxs-lookup"><span data-stu-id="ff366-115">**Product A:** 0</span></span>
    - <span data-ttu-id="ff366-116">**المنتج B:** 1</span><span class="sxs-lookup"><span data-stu-id="ff366-116">**Product B:** 1</span></span>
    - <span data-ttu-id="ff366-117">**المنتج C:** 2</span><span class="sxs-lookup"><span data-stu-id="ff366-117">**Product C:** 2</span></span>

<span data-ttu-id="ff366-118">وعندئذ يتم إنشاء أمر إنتاج للمنتج C، ويُضاف المنتج A إلى BOM أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ff366-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="ff366-119">بعد تقدير الأمر، يتم تحديث مستويات BOM بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="ff366-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="ff366-120">يعيّن **مستوى التكلفة** مستويات BOM التالية:</span><span class="sxs-lookup"><span data-stu-id="ff366-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="ff366-121">**المنتج B:** 1</span><span class="sxs-lookup"><span data-stu-id="ff366-121">**Product B:** 1</span></span>
    - <span data-ttu-id="ff366-122">**المنتج C:** 2</span><span class="sxs-lookup"><span data-stu-id="ff366-122">**Product C:** 2</span></span>
    - <span data-ttu-id="ff366-123">**المنتج A:** 3</span><span class="sxs-lookup"><span data-stu-id="ff366-123">**Product A:** 3</span></span>

- <span data-ttu-id="ff366-124">يعيّن **مستوى حساب التكاليف** مستويات BOM التالية:</span><span class="sxs-lookup"><span data-stu-id="ff366-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="ff366-125">**المنتج A:** 0</span><span class="sxs-lookup"><span data-stu-id="ff366-125">**Product A:** 0</span></span>
    - <span data-ttu-id="ff366-126">**المنتج B:** 1</span><span class="sxs-lookup"><span data-stu-id="ff366-126">**Product B:** 1</span></span>
    - <span data-ttu-id="ff366-127">**المنتج C:** 2</span><span class="sxs-lookup"><span data-stu-id="ff366-127">**Product C:** 2</span></span>

<span data-ttu-id="ff366-128">يضمن هذا السلوك عدم تأثير قوائم BOMs لأوامر الإنتاج على حسابات التكلفة اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="ff366-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]