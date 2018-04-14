--- 
title: "تعيين حالة دورة حياة منتج لأصل منتج صادر"
description: "يُظهر هذا الإجراء كيفية تعيين حالة دورة حياة منتج إلى أصل منتج صادر ومتغيراته."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8447e4e05e274a48623804435f4d3f6ed89665d0
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="6b28b-103">تعيين حالة دورة حياة منتج لأصل منتج صادر</span><span class="sxs-lookup"><span data-stu-id="6b28b-103">Assign a product lifecycle state to a released product master</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b28b-104">يُظهر هذا الإجراء كيفية تعيين حالة دورة حياة منتج إلى أصل منتج صادر ومتغيراته.</span><span class="sxs-lookup"><span data-stu-id="6b28b-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="6b28b-105">المتطلبات الأساسية: يجب أولاً تشغيل دليل المهام "إنشاء حالة دورة حياة منتج جديدة" للتأكد من أن لديك حالة دورة حياة منتج واحدة على الأقل تم إنشاؤها قبل تشغيل دليل المهام هذا.</span><span class="sxs-lookup"><span data-stu-id="6b28b-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="6b28b-106">البحث عن أصل منتج صادر</span><span class="sxs-lookup"><span data-stu-id="6b28b-106">Find a released product master</span></span>
1. <span data-ttu-id="6b28b-107">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="6b28b-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="6b28b-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6b28b-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="6b28b-109">أصل المنتج يتضمن أصل المنتج للنوع الفرعي للمنتج.</span><span class="sxs-lookup"><span data-stu-id="6b28b-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="6b28b-110">تحديث حالة دورة الحياة</span><span class="sxs-lookup"><span data-stu-id="6b28b-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="6b28b-111">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="6b28b-111">Click Edit.</span></span>
2. <span data-ttu-id="6b28b-112">في الحقل "حالة دورة حياة المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6b28b-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="6b28b-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6b28b-113">Click Save.</span></span>
4. <span data-ttu-id="6b28b-114">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="6b28b-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="6b28b-115">إذا تم تحديد "نعم"، فسيتم أيضًا تحديث كافة متغيرات المنتجات الصادرة ذات الحالة الأصلية نفسها لأصل المنتج الصادر إلى حالة دورة حياة المنتج الجديدة.</span><span class="sxs-lookup"><span data-stu-id="6b28b-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="6b28b-116">أما إذا تم تحديد "لا"، فستحافظ كافة المتغيرات على حالتها الفعلية.</span><span class="sxs-lookup"><span data-stu-id="6b28b-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="6b28b-117">لن يتم تحديث المتغيرات ذات حالة دورة حياة منتج مختلفة عن أصل المنتج الصادر.</span><span class="sxs-lookup"><span data-stu-id="6b28b-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="6b28b-118">التحقق من حالة دورة الحياة للمتغيرات</span><span class="sxs-lookup"><span data-stu-id="6b28b-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="6b28b-119">انقر فوق "متغيرات المنتج الذي تم إصداره".</span><span class="sxs-lookup"><span data-stu-id="6b28b-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="6b28b-120">لاحظ أن كافة المتغيرات قد ورثت حالة دورة الحياة المحددة من أصل المنتج الصادر.</span><span class="sxs-lookup"><span data-stu-id="6b28b-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="6b28b-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6b28b-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="6b28b-122">في الحقل "حالة دورة حياة المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6b28b-122">In the Product lifecycle state field, enter or select a value.</span></span>


