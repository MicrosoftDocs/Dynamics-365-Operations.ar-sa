---
title: المواد الخطرة
description: يوفر هذا الموضوع معلومات حول مستندات المواد الخطرة والمعلومات التي يتم تخزينها في بيئتك.
author: lachlancashMS
manager: AnnBe
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
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 443d2eb545b2b7592e27ae037009720db0a71997
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092535"
---
# <a name="hazardous-materials"></a><span data-ttu-id="95b7a-103">المواد الخطرة</span><span class="sxs-lookup"><span data-stu-id="95b7a-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95b7a-104">يتم إعداد المعلومات حول المواد الخطرة في إدارة معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="95b7a-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="95b7a-105">وتوفر هذه الوحدة النمطية أيضًا مستندات يمكن طباعتها من خلال إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="95b7a-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="95b7a-106">عند شحن المواد المصنفة كبضائع خطرة، يجب تضمين أوراق إضافية مع الشحنات.</span><span class="sxs-lookup"><span data-stu-id="95b7a-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="95b7a-107">تتيح وظيفة المواد الخطرة للعملاء تخزين معلومات التصنيف وربطها بإصدار الأصناف.</span><span class="sxs-lookup"><span data-stu-id="95b7a-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="95b7a-108">ويمكن بعد ذلك استخدام هذه المعلومات للمساعدة في تحضير وثائق الشحن.</span><span class="sxs-lookup"><span data-stu-id="95b7a-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95b7a-109">وللمساعدة في إدارة شحنات البضائع الخطرة، تتيح لك Microsoft Dynamics 365 Supply Chain Management إعداد معلومات مرجعية إضافية مرتبطة بالمنتجات.</span><span class="sxs-lookup"><span data-stu-id="95b7a-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="95b7a-110">يمكنك أيضًا إعداد مستندات شحن إضافية.</span><span class="sxs-lookup"><span data-stu-id="95b7a-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="95b7a-111">ولكن لا يتوافق النظام مع لوائح البلد أو المنطقة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="95b7a-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="95b7a-112">وبدلاً من ذلك فهي أداة يمكنها مساعدة البرنامج بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="95b7a-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="95b7a-113">قبل أن تتمكن من استخدام هذه الوظيفة، يجب إجراء الإعداد التالي:</span><span class="sxs-lookup"><span data-stu-id="95b7a-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="95b7a-114">**إدارة معلومات المنتج:** قم بإعداد الأكواد التي يمكن تطبيقها على المنتجات التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="95b7a-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="95b7a-115">**إدارة المستودعات:** استخدم مستندات شحن إضافية لطباعة معلومات الشحنة.</span><span class="sxs-lookup"><span data-stu-id="95b7a-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="95b7a-116">إدارة معلومات المنتج</span><span class="sxs-lookup"><span data-stu-id="95b7a-116">Product information management</span></span>

<span data-ttu-id="95b7a-117">في إدارة معلومات المنتج، يوجد نطاق من جداول الإعداد حيث يمكنك إضافة المعلومات المرجعية المتوفرة في قوائم البضائع الخطرة للشحن برًا وبحرًا وجوًا.</span><span class="sxs-lookup"><span data-stu-id="95b7a-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="95b7a-118">وفيما يلي بعض اللوائح التي غالبًا ما يشار إليها:</span><span class="sxs-lookup"><span data-stu-id="95b7a-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="95b7a-119">**ADR** – اللوائح المرتبطة بالنقل الدولي للبضائع الخطرة برًا</span><span class="sxs-lookup"><span data-stu-id="95b7a-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="95b7a-120">**CFR 49** – لوائح نقل البضائع الخطرة في الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="95b7a-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="95b7a-121">**IMDG** – رمز المدونة البحرية الدولية للبضائع الخطرة (IMDG)</span><span class="sxs-lookup"><span data-stu-id="95b7a-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="95b7a-122">**IATA** – لوائح الاتحاد الدولي للنقل الجوي (IATA) للبضائع الخطرة</span><span class="sxs-lookup"><span data-stu-id="95b7a-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="95b7a-123">تحتوي كل من هذه اللوائح على قائمة بالبضائع الخطرة تتضمن الرموز المرجعية.</span><span class="sxs-lookup"><span data-stu-id="95b7a-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="95b7a-124">يتم تجميع القوائم الخاصة بكل نوع من أنواع النقل في التصنيفات الدولية المشتركة.</span><span class="sxs-lookup"><span data-stu-id="95b7a-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="95b7a-125">توفر Supply Chain Management جدولاً مرجعيًا للرموز المشتركة في تلك القوائم.</span><span class="sxs-lookup"><span data-stu-id="95b7a-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="95b7a-126">وتحتوي كل قائمة أيضًا على بعض الأكواد الفريدة التي يمكن تحديدها.</span><span class="sxs-lookup"><span data-stu-id="95b7a-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="95b7a-127">للبدء في تكوين هذه المعلومات، قم بإنشاء لائحة يمكنك استخدامها لتكوين المعلمات الأولية.</span><span class="sxs-lookup"><span data-stu-id="95b7a-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="95b7a-128">إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="95b7a-128">Warehouse management</span></span>

<span data-ttu-id="95b7a-129">وعند تحضير الشحنة، يمكن طباعة العديد من التقارير الجديدة.</span><span class="sxs-lookup"><span data-stu-id="95b7a-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="95b7a-130">تستخدم هذه التقارير المعلومات التي يتم إعدادها في إدارة معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="95b7a-130">These reports use the information that you set up in Product information management.</span></span>
