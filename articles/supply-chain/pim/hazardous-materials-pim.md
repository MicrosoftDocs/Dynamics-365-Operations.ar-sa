---
title: المواد الخطرة
description: يوفر هذا الموضوع معلومات حول مستندات المواد الخطرة والمعلومات التي يتم تخزينها في بيئتك.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: feee6b348ac1870295a894ad988278b23a3f30a3
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979030"
---
# <a name="hazardous-materials"></a><span data-ttu-id="43c0d-103">المواد الخطرة</span><span class="sxs-lookup"><span data-stu-id="43c0d-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="43c0d-104">يتم إعداد المعلومات حول المواد الخطرة في إدارة معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="43c0d-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="43c0d-105">وتوفر هذه الوحدة النمطية أيضًا مستندات يمكن طباعتها من خلال إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="43c0d-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="43c0d-106">عند شحن المواد المصنفة كبضائع خطرة، يجب تضمين أوراق إضافية مع الشحنات.</span><span class="sxs-lookup"><span data-stu-id="43c0d-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="43c0d-107">تتيح وظيفة المواد الخطرة للعملاء تخزين معلومات التصنيف وربطها بإصدار الأصناف.</span><span class="sxs-lookup"><span data-stu-id="43c0d-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="43c0d-108">ويمكن بعد ذلك استخدام هذه المعلومات للمساعدة في تحضير وثائق الشحن.</span><span class="sxs-lookup"><span data-stu-id="43c0d-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43c0d-109">توفر ميزات المواد الخطرة في Microsoft Dynamics 365 Supply Chain Management مجموعة من الحقول المفيدة لمعلومات المنتجات والوظائف المرتبطة بها التي يُمكنها مساعدتك في تسجيل والرجوع إلى المعلومات المرتبطة بمنتجاتك الخطرة.</span><span class="sxs-lookup"><span data-stu-id="43c0d-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="43c0d-110">وقد تساعدك هذه الميزات أيضًا في تصميم وطباعة مستندات الشحنة التي تتضمن بعض المعلومات المتشابهة المتعلقة بأي مواد خطرة تقوم بشحنها.</span><span class="sxs-lookup"><span data-stu-id="43c0d-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="43c0d-111">ولكن، لا يتوافق النظام تلقائيًا مع اللوائح المنطبقة في بلدك أو منطقتك.</span><span class="sxs-lookup"><span data-stu-id="43c0d-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="43c0d-112">على الرغم من أن هذه الأدوات مخصصة لمساعدتك في التوافق مع اللوائح الشائعة، إلا أنها ليست كافية بحد ذاتها وليس مضمونًا أن تكون كذلك.</span><span class="sxs-lookup"><span data-stu-id="43c0d-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="43c0d-113">تتحمل مؤسستك المسؤولية عن الاطلاع على ومعرفة جميع اللوائح المعمول بها، وعن اتخاذ كافة الخطوات اللازمة للتوافق معها.</span><span class="sxs-lookup"><span data-stu-id="43c0d-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="43c0d-114">قبل أن تتمكن من استخدام هذه الوظيفة، يجب إجراء الإعداد التالي:</span><span class="sxs-lookup"><span data-stu-id="43c0d-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="43c0d-115">**إدارة معلومات المنتج:** قم بإعداد الأكواد التي يمكن تطبيقها على المنتجات التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="43c0d-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="43c0d-116">**إدارة المستودعات:** استخدم مستندات شحن إضافية لطباعة معلومات الشحنة.</span><span class="sxs-lookup"><span data-stu-id="43c0d-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="43c0d-117">إدارة معلومات المنتج</span><span class="sxs-lookup"><span data-stu-id="43c0d-117">Product information management</span></span>

<span data-ttu-id="43c0d-118">في إدارة معلومات المنتج، يوجد نطاق من جداول الإعداد حيث يمكنك إضافة المعلومات المرجعية المتوفرة في قوائم البضائع الخطرة للشحن برًا وبحرًا وجوًا.</span><span class="sxs-lookup"><span data-stu-id="43c0d-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="43c0d-119">وفيما يلي بعض اللوائح التي غالبًا ما يشار إليها:</span><span class="sxs-lookup"><span data-stu-id="43c0d-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="43c0d-120">**ADR** – اللوائح المرتبطة بالنقل الدولي للبضائع الخطرة برًا</span><span class="sxs-lookup"><span data-stu-id="43c0d-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="43c0d-121">**CFR 49** – لوائح نقل البضائع الخطرة في الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="43c0d-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="43c0d-122">**IMDG** – رمز المدونة البحرية الدولية للبضائع الخطرة (IMDG)</span><span class="sxs-lookup"><span data-stu-id="43c0d-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="43c0d-123">**IATA** – لوائح الاتحاد الدولي للنقل الجوي (IATA) للبضائع الخطرة</span><span class="sxs-lookup"><span data-stu-id="43c0d-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="43c0d-124">تحتوي كل من هذه اللوائح على قائمة بالبضائع الخطرة تتضمن الرموز المرجعية.</span><span class="sxs-lookup"><span data-stu-id="43c0d-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="43c0d-125">يتم تجميع القوائم الخاصة بكل نوع من أنواع النقل في التصنيفات الدولية المشتركة.</span><span class="sxs-lookup"><span data-stu-id="43c0d-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="43c0d-126">توفر Supply Chain Management جدولاً مرجعيًا للرموز المشتركة في تلك القوائم.</span><span class="sxs-lookup"><span data-stu-id="43c0d-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="43c0d-127">وتحتوي كل قائمة أيضًا على بعض الأكواد الفريدة التي يمكن تحديدها.</span><span class="sxs-lookup"><span data-stu-id="43c0d-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="43c0d-128">للبدء في تكوين هذه المعلومات، قم بإنشاء لائحة يمكنك استخدامها لتكوين المعلمات الأولية.</span><span class="sxs-lookup"><span data-stu-id="43c0d-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="43c0d-129">إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="43c0d-129">Warehouse management</span></span>

<span data-ttu-id="43c0d-130">وعند تحضير الشحنة، يمكن طباعة العديد من التقارير الجديدة.</span><span class="sxs-lookup"><span data-stu-id="43c0d-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="43c0d-131">تستخدم هذه التقارير المعلومات التي يتم إعدادها في إدارة معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="43c0d-131">These reports use the information that you set up in Product information management.</span></span>
