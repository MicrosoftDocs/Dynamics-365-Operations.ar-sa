---
title: إنشاء منتج جديد
description: توضح هذه المهمة كيفية إنشاء منتج مشترك جديد.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "328529"
---
# <a name="create-a-new-product"></a><span data-ttu-id="31003-103">إنشاء منتج جديد</span><span class="sxs-lookup"><span data-stu-id="31003-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31003-104">توضح هذه المهمة كيفية إنشاء منتج مشترك جديد.</span><span class="sxs-lookup"><span data-stu-id="31003-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="31003-105">عادة ما يتم تنفيذها عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="31003-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="31003-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="31003-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="31003-107">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات.</span><span class="sxs-lookup"><span data-stu-id="31003-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="31003-108">إنشاء منتج</span><span class="sxs-lookup"><span data-stu-id="31003-108">Create a product</span></span>
1. <span data-ttu-id="31003-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31003-109">Click New.</span></span>
2. <span data-ttu-id="31003-110">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="31003-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="31003-111">إذا لم يتم إعداد تسلسل الرقم لرقم المنتج، فإنه يجب إدخاله يدويًا.</span><span class="sxs-lookup"><span data-stu-id="31003-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="31003-112">في الحقل "اسم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="31003-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="31003-113">يتم وضع اسم المنتج في الوضع الافتراضي تبعًا لاسم البحث.</span><span class="sxs-lookup"><span data-stu-id="31003-113">The product name defaults to the search name.</span></span> <span data-ttu-id="31003-114">يمكنك تغييرها، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="31003-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="31003-115">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="31003-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="31003-116">إعداد مجموعات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="31003-116">Set up dimension groups</span></span>
1. <span data-ttu-id="31003-117">انقر فوق "مجموعات الأبعاد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="31003-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="31003-118">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31003-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="31003-119">تحدد مجموعة بُعد التخزين أبعاد التخزين التي يجب عليك إدخالها في كل حركة للمنتج، وكيف سيتم تعقبها في المخزون.</span><span class="sxs-lookup"><span data-stu-id="31003-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="31003-120">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31003-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="31003-121">تحدد مجموعة بُعد التعقب أبعاد التعقب التي يجب عليك إدخالها في كل حركة للمنتج، وكيف سيتم التعامل معها في المخزون.</span><span class="sxs-lookup"><span data-stu-id="31003-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="31003-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="31003-122">Click OK.</span></span>

