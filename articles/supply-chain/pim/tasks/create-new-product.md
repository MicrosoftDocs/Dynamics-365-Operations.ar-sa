---
title: إنشاء منتج جديد
description: يصف هذا الموضوع كيفية إنشاء منتج مشترك جديد.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bf15359e085b541407bb49c266f7d9505893e25
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203700"
---
# <a name="create-a-new-product"></a><span data-ttu-id="5cb7a-103">إنشاء منتج جديد</span><span class="sxs-lookup"><span data-stu-id="5cb7a-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5cb7a-104">يصف هذا الموضوع كيفية إنشاء منتج مشترك جديد.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="5cb7a-105">عادة ما يتم تنفيذها عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="5cb7a-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="5cb7a-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="5cb7a-107">إنشاء منتج</span><span class="sxs-lookup"><span data-stu-id="5cb7a-107">Create a product</span></span>
1. <span data-ttu-id="5cb7a-108">‏‫في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة معلومات المنتج > المنتجات > المنتجات‬‏‎**.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="5cb7a-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-109">Select **New**.</span></span>
3. <span data-ttu-id="5cb7a-110">في الحقل **رقم المنتج**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="5cb7a-111">إذا لم يتم إعداد تسلسل الرقم لرقم المنتج، فإنه يجب إدخاله يدويًا.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="5cb7a-112">في الحقل **اسم المنتج**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="5cb7a-113">يتم وضع اسم المنتج في الوضع الافتراضي تبعًا لاسم البحث.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-113">The product name defaults to the search name.</span></span> <span data-ttu-id="5cb7a-114">يمكنك تغييرها، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="5cb7a-115">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="5cb7a-116">إعداد مجموعات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="5cb7a-116">Set up dimension groups</span></span>
1. <span data-ttu-id="5cb7a-117">انقر فوق **مجموعات الأبعاد** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="5cb7a-118">في الحقل **مجموعة أبعاد التخزين**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="5cb7a-119">تحدد مجموعة بُعد التخزين أبعاد التخزين التي يجب عليك إدخالها في كل حركة للمنتج، وكيف سيتم تعقبها في المخزون.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="5cb7a-120">في الحقل **مجموعة أبعاد التعقب**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="5cb7a-121">تحدد مجموعة بُعد التعقب أبعاد التعقب التي يجب عليك إدخالها في كل حركة للمنتج، وكيف سيتم التعامل معها في المخزون.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="5cb7a-122">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-122">Select **OK**.</span></span>

