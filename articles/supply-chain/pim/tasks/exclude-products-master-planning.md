---
title: إنشاء حالة دورة حياة منتج لاستبعاد المنتجات من التخطيط الرئيسي
description: يُظهر هذا الإجراء كيفية إنشاء حالة دورة حياة منتج جديدة تستثني المنتجات من الحساب على مستوى التخطيط الرئيسي وقائمة مكونات الصنف.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc24aad05499adf9bfb2db3613c7f134c3a70770
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264688"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="1f8a7-103">إنشاء حالة دورة حياة منتج لاستبعاد المنتجات من التخطيط الرئيسي</span><span class="sxs-lookup"><span data-stu-id="1f8a7-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f8a7-104">يُظهر هذا الإجراء كيفية إنشاء حالة دورة حياة منتج جديدة تستثني المنتجات من الحساب على مستوى التخطيط الرئيسي وقائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="1f8a7-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="1f8a7-105">إنشاء حالة قديمة</span><span class="sxs-lookup"><span data-stu-id="1f8a7-105">Create an obsolete state</span></span>
1. <span data-ttu-id="1f8a7-106">انتقل إلى إدارة معلومات المنتج > الإعداد > حالة دورة حياة المنتج.</span><span class="sxs-lookup"><span data-stu-id="1f8a7-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="1f8a7-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1f8a7-107">Click New.</span></span>
3. <span data-ttu-id="1f8a7-108">في حقل "الحالة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1f8a7-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="1f8a7-109">حدد "لا" في حقل "نشط للتخطيط‬".</span><span class="sxs-lookup"><span data-stu-id="1f8a7-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="1f8a7-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1f8a7-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="1f8a7-111">إقران الحالة القديمة بمنتج صادر</span><span class="sxs-lookup"><span data-stu-id="1f8a7-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="1f8a7-112">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1f8a7-112">Close the page.</span></span>
2. <span data-ttu-id="1f8a7-113">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="1f8a7-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="1f8a7-114">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="1f8a7-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1f8a7-115">على سبيل المثال، قم بإجراء التصفية على حقل "اسم البحث" بقيمة "M00".</span><span class="sxs-lookup"><span data-stu-id="1f8a7-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="1f8a7-116">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="1f8a7-116">Click Edit.</span></span>
5. <span data-ttu-id="1f8a7-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1f8a7-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="1f8a7-118">في الحقل "حالة دورة حياة المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1f8a7-118">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]