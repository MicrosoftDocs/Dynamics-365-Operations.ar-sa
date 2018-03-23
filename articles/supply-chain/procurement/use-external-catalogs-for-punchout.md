---
title: "استخدام الكتالوجات الخارجية للتدبير الإلكتروني PunchOut"
description: "يشرح هذا المقال كيفية استخدام الكتالوجات الخارجية لإنشاء طلبات وإرسالها."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 76d0c911bdddbc5a34644dc96ec13dd8fd53a338
ms.contentlocale: ar-sa
ms.lasthandoff: 03/07/2018

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a><span data-ttu-id="c9660-103">استخدام الكتالوجات الخارجية للتدبير الإلكتروني PunchOut</span><span class="sxs-lookup"><span data-stu-id="c9660-103">Use external catalogs for PunchOut eProcurement</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c9660-104">باستخدام الكتالوجات الخارجية للتدبير الإلكتروني PunchOut، لست بحاجة إلى الاحتفاظ بمعلومات حول منتجات للموردين في بياناتك الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="c9660-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="c9660-105">بدلاً من ذلك، يتم تحويل عربة التسوق في موقع ويب للمورد إلى بنود طلب تحتوي على معلومات صحيحة عن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="c9660-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="c9660-106">يجب تجنب الاحتفاظ بأوصاف وأسعار منتجات الموردين في أصل منتجاتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="c9660-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="c9660-107">بدلاً من ذلك استخدم الكتالوجات الخارجية للتدبير الإلكتروني PunchOut</span><span class="sxs-lookup"><span data-stu-id="c9660-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="c9660-108">وبعد ذلك، عندما يقوم الموظفون بإنشاء طلبات، يمكنهم "الدخول" إلى موقع كتالوج خارجي لمورد (بمعنى آخر، يغادرون نظامك وينتقلون إلى موقع المورد).</span><span class="sxs-lookup"><span data-stu-id="c9660-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="c9660-109">يمكن تحويل المنتجات التي تمت إضافتها إلى عربة التسوق في موقع ويب الخاص بالمورد إلى بنود طلب.</span><span class="sxs-lookup"><span data-stu-id="c9660-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="c9660-110">وبالتالي، يمكنك الحصول على معلومات صحيحة عن المنتج: معرف المنتج والاسم والسعر وهكذا.</span><span class="sxs-lookup"><span data-stu-id="c9660-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="c9660-111">لاستخدام الكتالوجات الخارجية، يجب على الموظف إنشاء طلب في صفحة **طلبات الشراء الخاصة بي‬**.</span><span class="sxs-lookup"><span data-stu-id="c9660-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="c9660-112">تتم الإشارة إلى الموظف الذي يقوم بإنشاء طلب على أنه معد الطلب.</span><span class="sxs-lookup"><span data-stu-id="c9660-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="c9660-113">بصفتك معد الطلب، يمكنك أيضًا إكمال المهام التالية.</span><span class="sxs-lookup"><span data-stu-id="c9660-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="c9660-114">استخدم إجراء بند **الكتالوجات الخارجية** لفتح صفحة تتضمن كافة الكتالوجات الخارجية المتوفرة للطالب المحدد والكيان القانوني للشراء ووحدة التشغيل للاستلام.</span><span class="sxs-lookup"><span data-stu-id="c9660-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="c9660-115">بحسب أذوناتك، يمكنك تغيير الطالب والكيان القانوني للشراء ووحدة التشغيل للاستلام.</span><span class="sxs-lookup"><span data-stu-id="c9660-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="c9660-116">قد يؤدي حدوث تغيير في تلك القيم إلى تغيير قائمة الكتالوجات الخارجية المتوافرة للطالب.</span><span class="sxs-lookup"><span data-stu-id="c9660-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="c9660-117">الكتالوجات الخارجية المتوفرة تعتمد على سياسات الشراء النشطة الحالية للكيان القانوني للشراء أو وحدة التشغيل للاستلام.</span><span class="sxs-lookup"><span data-stu-id="c9660-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="c9660-118">باستطاعة هذه السياسات السماح بالوصول إلى فئات تدبير محددة أو منع الوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="c9660-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="c9660-119">لذلك، يمكن أن تتأثر قائمة الكتالوجات الخارجية التي تم تعيينها إلى فئات التدبير هذه.</span><span class="sxs-lookup"><span data-stu-id="c9660-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="c9660-120">لمزيد من المعلومات حول السياسات، راجع [سياسات الشراء](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c9660-120">For more information about policies, see [Purchasing policies](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="c9660-121">للبحث عن الكتالوجات الخارجية لفئات تدبير محددة، أدخل النص في حقل البحث عن الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="c9660-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="c9660-122">لإضافة المنتجات من الكتالوج الخارجي لمورد على موقع ويب الخاص بالمورد، انقر فوق الكتالوج الخارجي.</span><span class="sxs-lookup"><span data-stu-id="c9660-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="c9660-123">ثم أضف المنتجات إلى سلة التسوق، وسجل خروجك مع السداد. سيتم تحويل بنود سلة التسوق إلى Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c9660-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="c9660-124">إذا كان هناك العديد من الخيارات لفئات التدبير، حدد فئة التدبير الصحيحة قبل إضافة البنود إلى الطلب.</span><span class="sxs-lookup"><span data-stu-id="c9660-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="c9660-125">بعد أن تتم إضافة بنود إلى الطلب، يمكنك إضافة المزيد من البنود دون استخدام الكتالوجات الخارجية.</span><span class="sxs-lookup"><span data-stu-id="c9660-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="c9660-126">بدلاً من ذلك، يمكنك الاستمرار في استخدام الكتالوجات الخارجية لإضافة البنود.</span><span class="sxs-lookup"><span data-stu-id="c9660-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="c9660-127">عندما يصبح الطلب جاهزًا، استخدم إجراء **سير العمل** > **إرسال** لإرساله للموافقة.</span><span class="sxs-lookup"><span data-stu-id="c9660-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

