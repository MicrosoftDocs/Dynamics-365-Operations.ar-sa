--- 
title: "إنشاء منتج جديد"
description: "توضح هذه المهمة كيفية إنشاء منتج مشترك جديد."
author: BibiSp
manager: AnnBe
ms.date: 06/08/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d9307abf5e9543c8a2c880330c4430f5e4c5b340
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-new-product"></a><span data-ttu-id="f013d-103">إنشاء منتج جديد</span><span class="sxs-lookup"><span data-stu-id="f013d-103">Create a new product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f013d-104">توضح هذه المهمة كيفية إنشاء منتج مشترك جديد.</span><span class="sxs-lookup"><span data-stu-id="f013d-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="f013d-105">عادة ما يتم تنفيذها عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="f013d-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="f013d-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="f013d-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="f013d-107">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات.</span><span class="sxs-lookup"><span data-stu-id="f013d-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="f013d-108">إنشاء منتج</span><span class="sxs-lookup"><span data-stu-id="f013d-108">Create a product</span></span>
1. <span data-ttu-id="f013d-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f013d-109">Click New.</span></span>
2. <span data-ttu-id="f013d-110">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f013d-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f013d-111">إذا لم يتم إعداد تسلسل الرقم لرقم المنتج، فإنه يجب إدخاله يدويًا.</span><span class="sxs-lookup"><span data-stu-id="f013d-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="f013d-112">في الحقل "اسم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f013d-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="f013d-113">يتم وضع اسم المنتج في الوضع الافتراضي تبعًا لاسم البحث.</span><span class="sxs-lookup"><span data-stu-id="f013d-113">The product name defaults to the search name.</span></span> <span data-ttu-id="f013d-114">يمكنك تغييرها، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="f013d-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="f013d-115">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f013d-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="f013d-116">إعداد مجموعات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="f013d-116">Set up dimension groups</span></span>
1. <span data-ttu-id="f013d-117">انقر فوق "مجموعات الأبعاد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="f013d-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="f013d-118">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f013d-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f013d-119">تحدد مجموعة بُعد التخزين أبعاد التخزين التي يجب عليك إدخالها في كل حركة للمنتج، وكيف سيتم تعقبها في المخزون.</span><span class="sxs-lookup"><span data-stu-id="f013d-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="f013d-120">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f013d-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f013d-121">تحدد مجموعة بُعد التعقب أبعاد التعقب التي يجب عليك إدخالها في كل حركة للمنتج، وكيف سيتم التعامل معها في المخزون.</span><span class="sxs-lookup"><span data-stu-id="f013d-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="f013d-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f013d-122">Click OK.</span></span>


