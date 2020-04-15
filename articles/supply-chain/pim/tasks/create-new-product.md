---
title: إنشاء منتج جديد
description: يصف هذا الموضوع كيفية إنشاء منتج مشترك جديد.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 611fc0cff7fe2d580e971149630e92afd16be228
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147838"
---
# <a name="create-a-new-product"></a><span data-ttu-id="2f918-103">إنشاء منتج جديد</span><span class="sxs-lookup"><span data-stu-id="2f918-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f918-104">يصف هذا الموضوع كيفية إنشاء منتج مشترك جديد.</span><span class="sxs-lookup"><span data-stu-id="2f918-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="2f918-105">عادة ما يتم تنفيذها عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="2f918-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="2f918-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="2f918-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="2f918-107">إنشاء منتج</span><span class="sxs-lookup"><span data-stu-id="2f918-107">Create a product</span></span>
1. <span data-ttu-id="2f918-108">‏‫في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة معلومات المنتج > المنتجات > المنتجات‬‏‎**.</span><span class="sxs-lookup"><span data-stu-id="2f918-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="2f918-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2f918-109">Select **New**.</span></span>
3. <span data-ttu-id="2f918-110">في الحقل **رقم المنتج**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2f918-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="2f918-111">إذا لم يتم إعداد تسلسل الرقم لرقم المنتج، فإنه يجب إدخاله يدويًا.</span><span class="sxs-lookup"><span data-stu-id="2f918-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="2f918-112">في الحقل **اسم المنتج**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2f918-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="2f918-113">يتم وضع اسم المنتج في الوضع الافتراضي تبعًا لاسم البحث.</span><span class="sxs-lookup"><span data-stu-id="2f918-113">The product name defaults to the search name.</span></span> <span data-ttu-id="2f918-114">يمكنك تغييرها، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="2f918-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="2f918-115">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2f918-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="2f918-116">إعداد مجموعات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="2f918-116">Set up dimension groups</span></span>
1. <span data-ttu-id="2f918-117">انقر فوق **مجموعات الأبعاد** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="2f918-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="2f918-118">في الحقل **مجموعة أبعاد التخزين**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2f918-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="2f918-119">تحدد مجموعة بُعد التخزين أبعاد التخزين التي يجب عليك إدخالها في كل حركة للمنتج، وكيف سيتم تعقبها في المخزون.</span><span class="sxs-lookup"><span data-stu-id="2f918-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="2f918-120">في الحقل **مجموعة أبعاد التعقب**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2f918-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="2f918-121">تحدد مجموعة بُعد التعقب أبعاد التعقب التي يجب عليك إدخالها في كل حركة للمنتج، وكيف سيتم التعامل معها في المخزون.</span><span class="sxs-lookup"><span data-stu-id="2f918-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="2f918-122">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2f918-122">Select **OK**.</span></span>

