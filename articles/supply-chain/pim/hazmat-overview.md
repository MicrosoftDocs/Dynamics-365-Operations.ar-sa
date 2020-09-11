---
title: نظرة عامة على المواد الخطرة
description: يستعرض هذا الموضوع نظرة عامة حول الميزات المتعلقة بمناولة المواد الخطرة وتوثيقها في أثناء إدارة معلومات المنتج وإدارة المستودع.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 227111f4703d9dc381270382dcb796874d7de937
ms.sourcegitcommit: c009ec75f53872272f11c92a1ce81a391e3845a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699581"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="ed313-103">نظرة عامة على المواد الخطرة</span><span class="sxs-lookup"><span data-stu-id="ed313-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed313-104">لتظل المؤسسات ملتزمة بلوائح الشحن والنقل، يتعين على المؤسسات التي تقوم بشحن مواد مصنفة على أنها بضائع خطرة تضمين أعمال ورقية إضافية مع شحناتهم.</span><span class="sxs-lookup"><span data-stu-id="ed313-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="ed313-105">تتيح ميزة المواد الخطرة للعملاء تخزين المعلومات المرتبطة بالأصناف المُصدرة.</span><span class="sxs-lookup"><span data-stu-id="ed313-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="ed313-106">ويمكن بعد ذلك استخدام هذه المعلومات للمساعدة في تحضير وثائق الشحن.</span><span class="sxs-lookup"><span data-stu-id="ed313-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="ed313-107">يجب أن تمتلك المؤسسة التي تقوم بشحن بضائع خطرة عملياتها وإجراءتها الخاصة المتبعة لإدارة عملية الشحن.</span><span class="sxs-lookup"><span data-stu-id="ed313-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="ed313-108">يمثل Microsoft Dynamics 365 Supply Chain Management أداة تُساعد في إنشاء المستندات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ed313-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="ed313-109">يوضح المخطط التالي الخطوات اللازمة لإعداد ميزة المواد الخطرة واستخدامها.</span><span class="sxs-lookup"><span data-stu-id="ed313-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="ed313-110">![اعداد ميزة المواد الخطرة واستخدامها](media/hazmat-overview.png "اعداد ميزة المواد الخطرة واستخدامها")</span><span class="sxs-lookup"><span data-stu-id="ed313-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="ed313-111">يتم إعداد ميزة المواد الخطرة في إدارة معلومات المنتج، وتوفر المستندات التي يُمكن طباعتها من خلال إدارة المستودع.</span><span class="sxs-lookup"><span data-stu-id="ed313-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="ed313-112">بالتالي، وبالتحدث على نطاق أوسع، فهذه المناطق هي المناطق الرئيسية التي ستقوم فيها بمراجعة وإعداد واستخدام وظيفة هذه الميزة:</span><span class="sxs-lookup"><span data-stu-id="ed313-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="ed313-113">**إدارة معلومات المنتج:** - قم بإعداد الأكواد التي يمكن تطبيقها على المنتجات التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="ed313-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="ed313-114">**إدارة المستودع** - العمل باستخدام مستندات الشحن الإضافية التي سوف تتم طباعتها للشحنات.</span><span class="sxs-lookup"><span data-stu-id="ed313-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed313-115">توفر ميزات المواد الخطرة في Supply Chain Management مجموعة من الحقول المفيدة لمعلومات المنتجات والوظائف المرتبطة بها التي يُمكنها مساعدتك في تسجيل والرجوع إلى المعلومات المرتبطة بمنتجاتك الخطرة.</span><span class="sxs-lookup"><span data-stu-id="ed313-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="ed313-116">وقد تساعدك هذه الميزات أيضًا في تصميم وطباعة مستندات الشحنة التي تتضمن بعض المعلومات المتشابهة المتعلقة بأي مواد خطرة تقوم بشحنها.</span><span class="sxs-lookup"><span data-stu-id="ed313-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="ed313-117">ولكن، لا يتوافق النظام تلقائيًا مع اللوائح المنطبقة في بلدك أو منطقتك.</span><span class="sxs-lookup"><span data-stu-id="ed313-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="ed313-118">على الرغم من أن هذه الأدوات مخصصة لمساعدتك في التوافق مع اللوائح الشائعة، إلا أنها ليست كافية بحد ذاتها وليس مضمونًا أن تكون كذلك.</span><span class="sxs-lookup"><span data-stu-id="ed313-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="ed313-119">تتحمل مؤسستك المسؤولية عن الاطلاع على ومعرفة جميع اللوائح المعمول بها، وعن اتخاذ كافة الخطوات اللازمة للتوافق معها.</span><span class="sxs-lookup"><span data-stu-id="ed313-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="ed313-120">إدارة معلومات المنتج</span><span class="sxs-lookup"><span data-stu-id="ed313-120">Product information management</span></span>

<span data-ttu-id="ed313-121">توفر إدارة معلومات المنتج مجموعة من جداول الإعداد بحيث يُمكنك إدخال المعلومات المرجعية لقوائم البضائع الخطرة المختلفة للشحن برًا وبحرًا وجوًا.</span><span class="sxs-lookup"><span data-stu-id="ed313-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="ed313-122">تمت الإشارة إلى اللوائح المشتركة التالية عند تطوير هذه الوظيفة:</span><span class="sxs-lookup"><span data-stu-id="ed313-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="ed313-123">**ADR** – اللوائح المرتبطة بالنقل الدولي للبضائع الخطرة برًا</span><span class="sxs-lookup"><span data-stu-id="ed313-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="ed313-124">**CFR 49** – لوائح نقل البضائع الخطرة في الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="ed313-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="ed313-125">**IMDG** – رمز المدونة البحرية الدولية للبضائع الخطرة (IMDG)</span><span class="sxs-lookup"><span data-stu-id="ed313-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="ed313-126">**IATA** – لوائح الاتحاد الدولي للنقل الجوي (IATA) للبضائع الخطرة</span><span class="sxs-lookup"><span data-stu-id="ed313-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="ed313-127">توفر كل مجموعة من اللوائح قوائم قياسية للبضائع الخطرة والأكواد المرجعية.</span><span class="sxs-lookup"><span data-stu-id="ed313-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="ed313-128">بالتالي، توفر Supply Chain Management جدولاً مرجعيًا للرموز المشتركة في تلك القوائم.</span><span class="sxs-lookup"><span data-stu-id="ed313-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="ed313-129">وتحتوي كل قائمة أيضًا على بعض الأكواد الفريدة التي يمكن تحديدها.</span><span class="sxs-lookup"><span data-stu-id="ed313-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="ed313-130">لمزيد من المعلومات حول كيفية إعداد اللوائح والقيم الخاصة بالمواد الخطرة، وكيفية تعيين القيم للمنتجات ذات الصلة، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="ed313-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="ed313-131">إعداد المواد الخطرة</span><span class="sxs-lookup"><span data-stu-id="ed313-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="ed313-132">المواد الخطرة في المنتجات والأوامر والشحنات والأحمال</span><span class="sxs-lookup"><span data-stu-id="ed313-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="ed313-133">إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="ed313-133">Warehouse management</span></span>

<span data-ttu-id="ed313-134">عند إعداد شحنة في إدارة المستودع، فسوف تكون قادرًا على طباعة العديد من التقارير الجديدة التي تستخدم المعلومات التي قمت بإعدادها في إدارة معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="ed313-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="ed313-135">لمزيد من المعلومات حول التقارير المتوفرة وكيفية استخدامها، راجع [استعلامات وتقارير المواد الخطرة](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="ed313-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>
