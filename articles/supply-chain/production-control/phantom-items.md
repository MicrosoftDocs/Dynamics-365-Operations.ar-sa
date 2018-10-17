---
title: "أصناف وهمية"
description: "يوضح هذا الموضوع، بالتفصيل، كيفية استخدام نوع الصنف الوهمي لبنود قائمة مكونات الصنف (BOM)، والمعادلة في Microsoft Dynamics 365 for Finance and Operations."
author: ShylaThompson
manager: AnnBe
ms.date: 06/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: 
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: a92dd82f309867586f047e0dfc36e452a44a0f9c
ms.contentlocale: ar-sa
ms.lasthandoff: 10/01/2018

---

# <a name="phantom-items"></a><span data-ttu-id="662cf-103">أصناف وهمية</span><span class="sxs-lookup"><span data-stu-id="662cf-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="662cf-104">يوضح هذا الموضوع، بالتفصيل، كيفية استخدام نوع الصنف الوهمي لبنود قائمة مكونات الصنف (BOM) والمعادلة.</span><span class="sxs-lookup"><span data-stu-id="662cf-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="662cf-105">في التوضيح التالي، تمثل (A) قائمة مكونات الصنف للمنتج H والأجزاء F و G و (b) كشف المسار للمنتجات H وجزء F.</span><span class="sxs-lookup"><span data-stu-id="662cf-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![المنتج H والجزء F](media/product-H-part-F.png)


<span data-ttu-id="662cf-107">يبين الرسم التوضيحي التالي مثال على بنيئة قائمة مكونات الصنف في مستويين.</span><span class="sxs-lookup"><span data-stu-id="662cf-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="662cf-108">يمثل المنتج المنتهي H منتج لتجميع جهاز.</span><span class="sxs-lookup"><span data-stu-id="662cf-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="662cf-109">يتكون تجميع الجهاز من جزئين، الوحدة الكهربائية (F) التي تحتوي على مادتين (A و B) ومجموعة من مواد التعبئة (G) التي يوجد بها مادتين أيضًا (C و D).</span><span class="sxs-lookup"><span data-stu-id="662cf-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="662cf-110">يتم استخدام مادة أخرى (E) خلال التعليم العام للجهاز.</span><span class="sxs-lookup"><span data-stu-id="662cf-110">Another material (E) is used during the general assembly of the machine.</span></span>

![المنتج H والجزء F](media/product-H-part-B.png)

<span data-ttu-id="662cf-112">يمثل التوضيح السابق قائمة مكونات الصنف للهندسة للمنتج H. وتوفر هذه البنية نظرة عامة جيدة لأجزاء ومكونات التجميع الكلي للجهاز.</span><span class="sxs-lookup"><span data-stu-id="662cf-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="662cf-113">ومع ذلك، على الرغم من أن مصممو المنتجات قد يفضلون الاطلاع على قائمة مكونات الصنف ممثلة بهذه الطريثة، فقد لا تمثل هذه البنية الطريقة التي تم بناء الجهاز بها في حالة العمل. </span><span class="sxs-lookup"><span data-stu-id="662cf-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="662cf-114">على سبيل المثال، تشير قائمة مكونات الصنف للهندسة في الرسم التوضيحي السابق أن الوحدة الكهربائية F تم تجميعها كجزء منفصل في أمر عمل منفصل.</span><span class="sxs-lookup"><span data-stu-id="662cf-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="662cf-115">ومع ذلك، في حالة العمل، قد يبدو الخيار الأكثر مثالية هو تجميع الوحدة الكهربائية كجزء من تجميع الجهاز الكلي، وليس كأمر عمل منفصل.</span><span class="sxs-lookup"><span data-stu-id="662cf-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="662cf-116">تشير شجرة المواد للهندسة هذه أيضًا إلى أن الجزء G جزء مستقل.</span><span class="sxs-lookup"><span data-stu-id="662cf-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="662cf-117">ومع ذلك، في هذه البنية، لا يمثل الجزء G الجزء الفعلي ولكن مجموعة من مواد التعبئة.</span><span class="sxs-lookup"><span data-stu-id="662cf-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="662cf-118">لذلك، على الرغم من أن قائمة مكونات الصنف للهندسة توفير قيمة كبيرة لتصميم أحد المنتجات وصيانته، فقد لا تكون الطريقة الأمثل منطقيًا لدعم عملية تنفيذ تصنيع المنتج.</span><span class="sxs-lookup"><span data-stu-id="662cf-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="662cf-119">وعلى النقيض، يمثل تصنيع قائمة مكونات الصنف الطريقة المُثلى لإنشاء منتج.</span><span class="sxs-lookup"><span data-stu-id="662cf-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="662cf-120">يبين الرسم التوضيحي التالي كيف يتم تحويل قائمة مكونات الصنف للهندسة السابقة إلى قائمة مكونات الصنف للتصنيع.</span><span class="sxs-lookup"><span data-stu-id="662cf-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="662cf-121">في الرسم التوضيحي التالي، تمثل (a) قائمة مكونات الصنف للمنتج H، و b هي كشف المسارات للمنتج H.</span><span class="sxs-lookup"><span data-stu-id="662cf-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="662cf-122">في هذه البنية، يمكنك رؤية أنه لا توجد أي فكرة عن الأجزاء F و G، وتم رفع المواد التي تتكون منها هذه الأجزاء إلى مستوى قائمة مكونات الصنف التالي.</span><span class="sxs-lookup"><span data-stu-id="662cf-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="662cf-123">بعكس "الهندسة شجرة المواد"، والتي لها ورقتين العمليات، "شجرة مواد التصنيع" على ورقة واحدة فقط من العمليات.</span><span class="sxs-lookup"><span data-stu-id="662cf-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="662cf-124">تم رفع عملية التعبئة التي تم ربطها بالجزء G أيضًا، وهي الآن جزء من ورقة العمليات للمنتج H. ويمثل تجميع الوحدة الكهربائية العملية الأولى.</span><span class="sxs-lookup"><span data-stu-id="662cf-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="662cf-125">وهذا الترتيب يبدو معقولًا، نظرًا لأنه يتم استخدام هذه الوحدة في العملية التالية، وهي عملية تجميع الجهاز.</span><span class="sxs-lookup"><span data-stu-id="662cf-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="662cf-126">العملية الأخيرة هي عملية التعبئة، والتي تستهلك مواد التعبئة الاثنين (C و D).</span><span class="sxs-lookup"><span data-stu-id="662cf-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="662cf-127">في Microsoft Dynamics 365 for Finance and Operations، يتم تمكين الانتقال بين قائمة مكونات الصنف للهندسة وقائمة مكونات الصنف للتصنيع من خلال نوع بند قائمة مكونات الصنف الوهمي.</span><span class="sxs-lookup"><span data-stu-id="662cf-127">In Microsoft Dynamics 365 for Finance and Operations, the transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="662cf-128">وحيث أن المصطلح "وهمي" يشير إلى اختفاء الأجزاء F و G خلال الانتقال بين نوعي قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="662cf-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="662cf-129">في هذا المثال، يتم تطبيق نوع البند الوهمي على بنود قائمة مكونات الصنف للأجزاء F و G في قائمة مكونات الصنف للهندسة.</span><span class="sxs-lookup"><span data-stu-id="662cf-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="662cf-130">عند إنشاء أمر إنتاج أو دفعة، يتم نسخ قائمة مكونات الصنف للهندسة إلى أمر الإنتاج أو الدفعة.</span><span class="sxs-lookup"><span data-stu-id="662cf-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="662cf-131">وبعد ذلك، عندما يتم تقدير الأمر، يحدث الانتقال من قائمة مكونات الصنف للهندسة إلى قائمة مكونات الصنف للتصنيع، على النحو الموضح في الرسومات التوضيحية السابقة.</span><span class="sxs-lookup"><span data-stu-id="662cf-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="662cf-132">من صفحة العمليات في الرسم التوضيحي الثاني، يتم إدخال مواد التعبئة C و D للعملية.</span><span class="sxs-lookup"><span data-stu-id="662cf-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="662cf-133">بُنى قوائم مكونات الصنف الوهمي متعددة المستويات</span><span class="sxs-lookup"><span data-stu-id="662cf-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="662cf-134">يمكن استخدام نوع البند الوهمي في بُنى قوائم كميات الصنف متعددة المستويات، على النحو الموضح في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="662cf-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="662cf-135">في الرسم التوضيحي التالي، تمثل (a) قائمة مكونات الصنف للمنتج G، و b هي كشف المسارات للأجزاء E و F والمنتج G.</span><span class="sxs-lookup"><span data-stu-id="662cf-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![المنتج G والجزء F مع كشوف المسارات](media/product-G-route-sheet-G.png)


<span data-ttu-id="662cf-137">يُظهر الرسم التوضيحي التالي قائمة مكونات الصنف للتصنيع الناتجة وسجل المسارات إذا تم تكوين بنود قائمة مكونات الصنف للأجزاء E و F بحيث يكون نوع البند وهمي.</span><span class="sxs-lookup"><span data-stu-id="662cf-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="662cf-138">في الرسم التوضيحي التالي، تمثل (a) قائمة مكونات الصنف للمنتج G، و (b) هي كشف المسارات للمنتج G.</span><span class="sxs-lookup"><span data-stu-id="662cf-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![منتج G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="662cf-140">الصنف الوهمي وشبكة المسارات</span><span class="sxs-lookup"><span data-stu-id="662cf-140">Phantom and route network</span></span>
<span data-ttu-id="662cf-141">يمكن أيضًا استخدام قوائم مكونات الصنف الوهمي لقائمة مكونات الصنف التي تحتوي على شبكة مسارات.</span><span class="sxs-lookup"><span data-stu-id="662cf-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="662cf-142">في شبكة المسارات، يتم تشغيل عملية واحدة أو أكثر بالتوازي.</span><span class="sxs-lookup"><span data-stu-id="662cf-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="662cf-143">يوضح الرسم البياني التالي مثالًا لشبكة المسارات المستخدمة في قائمة مكونات الصنف متعددة المستويات.</span><span class="sxs-lookup"><span data-stu-id="662cf-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="662cf-144">في الرسم التوضيحي التالي، تمثل (a) قائمة مكونات الصنف للمنتج G والجزء F، و(b) هي سجل المسارات للمنتج G والجزء F، والذي يحتوي على شبكة مسارات.</span><span class="sxs-lookup"><span data-stu-id="662cf-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![المنتج G والجزء F](media/product-G-part-F.png)


<span data-ttu-id="662cf-146">في الرسم التوضيحي التالي، تمثل (a) قائمة مكونات الصنف للمنتج G والجزء F، و(b) هي كشف المسارات للمنتج G والجزء F.</span><span class="sxs-lookup"><span data-stu-id="662cf-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![المنتج G والجزء F مع كشوف المسارات](media/product-G-part-F-with-route-sheet.png)

