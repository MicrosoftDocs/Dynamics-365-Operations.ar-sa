---
title: الشركات الهندسية وقواعد ملكيه البيانات
description: يشرح هذا الموضوع كيفيه استخدام شركه واحده أو أكثر من الشركات الهندسية لضمان إنشاء البيانات الرئيسية للمنتجات وصيانتها بشكل مركزي. تمثل الشركة الهندسية الشركة التي تملك المنتجات الهندسية والبيانات المتعلقة بالهندسة.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5cab02600e13a1a539b5ae0cd3ff66960430e826
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/29/2020
ms.locfileid: "4421816"
---
# <a name="engineering-companies-and-data-ownership-rules"></a><span data-ttu-id="0f6d6-104">الشركات الهندسية وقواعد ملكيه البيانات</span><span class="sxs-lookup"><span data-stu-id="0f6d6-104">Engineering companies and data ownership rules</span></span>

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a><span data-ttu-id="0f6d6-105">الشركات الهندسية والشركات التشغيلية</span><span class="sxs-lookup"><span data-stu-id="0f6d6-105">Engineering companies and operational companies</span></span>

<span data-ttu-id="0f6d6-106">لضمان إنشاء البيانات الرئيسية للمنتجات وصيانتها بشكل مركزي، يمكنك استخدام واحدة أو أكثر من *الشركات الهندسية*.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-106">To ensure that the master data for products is centrally created and maintained, you can use one or more *engineering companies*.</span></span> <span data-ttu-id="0f6d6-107">تملك الشركة الهندسية المنتجات الهندسية والبيانات المتعلقة بالهندسة.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-107">An engineering company owns the engineering products and their engineering-relevant data.</span></span> <span data-ttu-id="0f6d6-108">ويتم اتصاله دائما (يعتمد على) *بالكيان القانوني*  الموجود، وهو عبارة عن شركه أيضا.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-108">It's always connected to (based on) an existing *legal entity*, which is also a company.</span></span> <span data-ttu-id="0f6d6-109">ومن خلال هذا الاتصال ، يقوم النظام بتاسيس نقطه إدخال مركزيه لكافة البيانات المتعلقة بالهندسة للمنتجات الهندسية في الشركة الهندسية.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-109">Through this connection, the system establishes a central entry point for all engineering-relevant data for engineering products in the engineering company.</span></span> <span data-ttu-id="0f6d6-110">في نقطه الإدخال المركزية هذه ، يتم إنشاء منتجات الهندسية، ويتم الاحتفاظ بالبيانات ذات الصلة بالهندسة.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-110">In this central entry point, engineering products are created, and engineering-relevant data is maintained.</span></span> <span data-ttu-id="0f6d6-111">ومنه ، سيتم إصدار المنتجات الهندسية والبيانات ذات الصلة بالهندسة إلى *الشركات التشغيلية* ، وهي عبارة عن كيانات قانونيه أخرى.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-111">From it, the engineering products and engineering-relevant data will be released to *operational companies*, which are other legal entities.</span></span> <span data-ttu-id="0f6d6-112">(لمزيد من المعلومات حول أداره الإصدار، راجع [إصدار بنيات المنتج](release-product-structure.md).) ستستخدم هذه الشركات التشغيلية بيانات الهندسة كما تم تصميمها بواسطة الشركة الهندسية.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-112">(For more information about the release management, see [Release product structures](release-product-structure.md).) These operational companies will use the engineering data as it has been designed by the engineering company.</span></span> <span data-ttu-id="0f6d6-113">ويتم الاحتفاظ بآيه بيانات لوجيستية محليا بواسطة كل شركه هندسية وشركه تشغيليه.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-113">Any logistical data is locally maintained by each engineering company and operational company.</span></span>

<span data-ttu-id="0f6d6-114">لإنشاء شركه هندسية ، انتقل إلى **أداره التغييرات الهندسية\> اعداد\> مؤسسات هندسيه**.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-114">To create an engineering company, go to **Engineering change management \> Setup \> Engineering organizations**.</span></span> <span data-ttu-id="0f6d6-115">حدد **جديد**، وادخل اسما للشركة الهندسية ، وحدد الشركة الموجودة (الكيان القانوني) الذي تستند اليه.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-115">Select **New**, enter a name for the engineering company, and select the existing company (legal entity) that it's based on.</span></span>

<span data-ttu-id="0f6d6-116">إذا كنت تقوم بالتكامل مع أنظمه أداره دوره حياه المنتج الخارجي (PLM) ، فيجب عليك إنشاء وحده اعمال (نوع الشركة) التي ستصبح شركه خارجيه.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-116">If you're integrating with external product lifecycle management (PLM) systems, you must create a business unit (type of company) that will become an external company.</span></span>

## <a name="engineering-product-categories-and-engineering-companies"></a><span data-ttu-id="0f6d6-117">الشركات الهندسية وفئات المنتجات الهندسية</span><span class="sxs-lookup"><span data-stu-id="0f6d6-117">Engineering product categories and engineering companies</span></span>

<span data-ttu-id="0f6d6-118">تساعد *فئات المنتجات الهندسية* في التاكد من إنشاء المنتجات الهندسية وفقا لقواعد اعمال شركتك وسلوكها كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-118">*Engineering product categories* help ensure that engineering products are created according to your company's business rules and behave as required.</span></span> <span data-ttu-id="0f6d6-119">لمزيد من المعلومات حول فئات المنتجات الهندسية ، راجع [الإصدارات الهندسية وفئات المنتجات الهندسية](engineering-versions-product-category.md).</span><span class="sxs-lookup"><span data-stu-id="0f6d6-119">For more information about engineering product categories, see [Engineering versions and engineering product categories](engineering-versions-product-category.md).</span></span>

<span data-ttu-id="0f6d6-120">تنتمي كل فئة من فئات المنتج الهندسي إلى شركه هندسية معينه ويمكنها إنشاء المنتجات التي تنتمي إلى تلك الشركة فقط.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-120">Each engineering product category belongs to a specific engineering company and can create only products that belong to that company.</span></span> <span data-ttu-id="0f6d6-121">المثل ، فان حق الاحتفاظ بالمنتج الهندسي أيضا ينتمي إلى الشركة المقترنة بفئة المنتج الهندسي لهذا المنتج.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-121">Likewise, the right to maintain an engineering product also belongs to the company that is associated with that product's engineering product category.</span></span>

## <a name="data-that-is-owned-by-the-engineering-company"></a><span data-ttu-id="0f6d6-122">البيانات التي تملكها الشركة الهندسية</span><span class="sxs-lookup"><span data-stu-id="0f6d6-122">Data that is owned by the engineering company</span></span>

<span data-ttu-id="0f6d6-123">ونظرا لان الشركة تملك البيانات ذات الصلة بالهندسة ، فانها تتحكم في العمليات التالية:</span><span class="sxs-lookup"><span data-stu-id="0f6d6-123">Because the engineering company owns the engineering-relevant data, it controls the following processes:</span></span>

- <span data-ttu-id="0f6d6-124">**إنشاء المنتجات الهندسية:** يمكن لكل شركه هندسية إنشاء منتجات هندسه جديده تستند إلى فئة منتج هندسية يمتلكها.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-124">**Creation of engineering products:** Each engineering company can only create new engineering products that are based on an engineering product category that it owns.</span></span> <span data-ttu-id="0f6d6-125">في بعض الحالات ، تحتفظ الشركات التشغيلية بالبيانات المحلية الخاصة بها والمرتبطة بتلك المنتجات.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-125">In some cases, operational companies maintain their own local data that is related to those products.</span></span>
- <span data-ttu-id="0f6d6-126">**إنشاء الإصدارات الهندسية:** عندما تقوم أحدي الشركات بإنشاء منتج هندسي جديد ، يقوم النظام تلقائيا بإنشاء إصدار هندسي مبدئي له.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-126">**Creation of engineering versions:** When a company creates a new engineering product, the system automatically creates an initial engineering version for it.</span></span> <span data-ttu-id="0f6d6-127">ستتمكن الشركة الهندسية المالكة فقط من إنشاء إصدارات جديده من هذا المنتج.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-127">Only the owning engineering company will be able to create new versions of that product.</span></span>
- <span data-ttu-id="0f6d6-128">**إنشاء السمات الهندسية وصيانتها:** عندما تقوم أحدي الشركات بإنشاء منتج هندسي جديد ، يقوم النظام تلقائيا بإنشاء إصدار هندسي مبدئي له.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-128">**Creation and maintenance of engineering attributes:** When a company creates a new engineering product, the system automatically adds engineering attributes to it.</span></span> <span data-ttu-id="0f6d6-129">فقط الشركة الهندسية المالكة ستكون قادره علي إنشاء قيم هذه السمات والاحتفاظ بها.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-129">Only the owning engineering company will be able to create and maintain the values for those attributes.</span></span> <span data-ttu-id="0f6d6-130">لمزيد من المعلومات عن السمات الهندسية، راجع [السمات الهندسية والبحث عن السمات الهندسية](engineering-attributes-and-search.md).</span><span class="sxs-lookup"><span data-stu-id="0f6d6-130">For more information about engineering attributes, see [Engineering attributes and engineering attribute search](engineering-attributes-and-search.md).</span></span>
- <span data-ttu-id="0f6d6-131">**إنشاء قائمة مكونات الصنف (BOM) المتصلة بالإصدارات الهندسية وصيانتها:** يمكن للشركة الهندسية المالكة توصيل قائمة مكونات الصنف بإصدار منتج هندسي مباشره.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-131">**Creation and maintenance of bills of materials (BOMs) that are connected to the engineering versions:** The owning engineering company can directly connect a BOM to an engineering product version.</span></span> <span data-ttu-id="0f6d6-132">عند إصدار قائمة مكونات الصنف هذه للكيانات القانونية الأخرى ، يتم تحديد التغييرات التي يتم اجراؤها علي البيانات الهندسية في قائمة مكونات الصنف بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="0f6d6-132">When these BOMs are released to other legal entities, changes to the engineering data on the BOMs are limited in the following ways:</span></span>

    - <span data-ttu-id="0f6d6-133">لا يمكن للشركة التشغيلية أزاله بنود قائمة مكونات الصنف التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-133">The operational company can't remove released BOM lines.</span></span>
    - <span data-ttu-id="0f6d6-134">تكون الحقول الهندسية في بنود قائمة مكونات الصنف للقراءة فقط للشركة التشغيلية.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-134">The engineering fields on the BOM lines are read-only for the operational company.</span></span> <span data-ttu-id="0f6d6-135">وكافة الحقول الأخرى هي حقول تنفيذ لوجيستي ويمكن تحريرها بواسطة الشركة التشغيلية.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-135">All other fields are logistical implementation fields and can be edited by the operational company.</span></span>
    - <span data-ttu-id="0f6d6-136">ويمكن للشركة التشغيلية أضافه بنود قائمة مكونات الصنف إلى نفس قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-136">The operational company can add BOM lines to the same BOM.</span></span> <span data-ttu-id="0f6d6-137">بهذه الطريقة ، يمكنه أضافه إضافات محليه ، مثل مواد التعبئة أو سوائل التزليق.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-137">In this way, it can add local additions, such as packaging materials or lubrication fluids.</span></span>
    - <span data-ttu-id="0f6d6-138">يمكن للشركة التشغيلية أضافه قائمة مكونات صنف محليه جديده تماما.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-138">The operational company can add a completely new, local BOM.</span></span> <span data-ttu-id="0f6d6-139">قد يكون هذا التغيير مطلوبا في الحالات ، علي سبيل المثال ، لا يتم توفير قائمة مكونات الصنف اثناء الإصدار.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-139">This change might be required in cases where, for example, no BOM is provided during the release.</span></span> <span data-ttu-id="0f6d6-140">تمتلك الشركة التشغيلية قائمة مكونات الصنف المحلية هذه وتحتفظ بها.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-140">The operational company owns and maintains these local BOMs.</span></span> <span data-ttu-id="0f6d6-141">لمزيد من المعلومات حول أداره الإصدار ، راجع [إصدار بُنى المنتج](release-product-structure.md).</span><span class="sxs-lookup"><span data-stu-id="0f6d6-141">For more information about release management, see [Release product structures](release-product-structure.md).</span></span>
    - <span data-ttu-id="0f6d6-142">يتم حفظ كافة قائمة مكونات الصنف وبنود قائمة مكونات الصنف عند قيام الشركه الهندسية بتحديث قائمة مكونات الصنف الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-142">All local BOMs and BOM lines are preserved when the engineering company updates its BOM.</span></span>

- <span data-ttu-id="0f6d6-143">**إنشاء قائمة مكونات الصنف (BOM) المتصلة بالإصدارات الهندسية وصيانتها:** يمكن للشركة الهندسية المالكة توصيل قائمة مكونات الصنف بكل إصدار منتج هندسي مباشره.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-143">**Creation and maintenance of routes that are connected to the engineering versions:** The engineering company can directly connect a route to each engineering version.</span></span> <span data-ttu-id="0f6d6-144">عند إصدار هذه المسارات للكيانات القانونية الأخرى ، يتم تحديد التغييرات التي يتم اجراؤها علي البيانات الهندسية في المسارات بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="0f6d6-144">When these routes are released to other legal entities, changes to the data on the routes are limited in the following ways:</span></span>

    - <span data-ttu-id="0f6d6-145">لا يمكن للكيانات القانونية الأخرى أزاله بيانات الهندسة الموجودة في المسارات.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-145">The other legal entities can't remove the engineering data on the routes.</span></span>
    - <span data-ttu-id="0f6d6-146">ويمكن للكيانات القانونية الأخرى أضافه عمليات إلى المسار.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-146">The other legal entities can add operations to the route.</span></span> <span data-ttu-id="0f6d6-147">وبهذه الطريقة ، يمكنهم أضافه خطوات المسار المحلي.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-147">In this way, they can add local route steps.</span></span>
    - <span data-ttu-id="0f6d6-148">يمكن للشركات التشغيلية أضافه مسارات محليه جديده تماما.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-148">Operational companies can add completely new, local routes.</span></span> <span data-ttu-id="0f6d6-149">قد يكون هذا التغيير مطلوبا في الحالات ، علي سبيل المثال ، لم تقم بتضمين مسارات اثناء الإصدار.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-149">This change might be required if, for example, you haven't included routes during the release.</span></span> <span data-ttu-id="0f6d6-150">تمتلك الشركات التشغيلية هذه المسارات وتحتفظ بها.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-150">The operational companies own and maintain these local routes.</span></span> <span data-ttu-id="0f6d6-151">لمزيد من المعلومات حول أداره الإصدار ، راجع [إصدار بُنى المنتج](release-product-structure.md).</span><span class="sxs-lookup"><span data-stu-id="0f6d6-151">For more information about release management, see [Release product structures](release-product-structure.md).</span></span>
    - <span data-ttu-id="0f6d6-152">يتم الاحتفاظ بكافة التغييرات التي يتم اجراؤها محليا عند إصدار تحديثات من الشركة الهندسية مره أخرى إلى المسارات.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-152">All changes that are made locally are preserved when updates from the engineering company are released again to the routes.</span></span>

- <span data-ttu-id="0f6d6-153">**إنشاء وصيانة المستندات الهندسية:** يمكن للشركة الهندسية إرفاق مستندات هندسية بكل إصدار هندسي.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-153">**Creation and maintenance of engineering documents:** The engineering company can attach engineering documents to each engineering version.</span></span>

    - <span data-ttu-id="0f6d6-154">عند إصدار هذه المستندات لكيانات القانونية الأخرى ، تتم حماية المستندات من ان تتم ازالتها بواسطة الشركة التشغيلية.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-154">When these documents are released to other legal entities, the documents are protected from being removed by the operational company.</span></span>
    - <span data-ttu-id="0f6d6-155">ويمكن للكيانات القانونية الأخرى أضافه مستندات محليه جديده تماما.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-155">Other legal entities can add completely new, local documents.</span></span> <span data-ttu-id="0f6d6-156">تمتلك الشركة التشغيلية قائمة هذه المستندات وتحتفظ بها.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-156">The operational company owns and maintains these local documents.</span></span>