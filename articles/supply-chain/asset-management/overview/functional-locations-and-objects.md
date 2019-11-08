---
title: الأصول ومواقع العمل
description: يصف الأصول ومواقع العمل في إدارة الأصول. إدارة الأصول عبارة عن وحدة نمطية متقدمة لإدارة الأصول ومهام الصيانة في Dynamics 365 Supply Chain Management.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3a42d36fd137aa780886276a4235f1b8f3a3680
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653337"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="c5e7d-104">الأصول ومواقع العمل</span><span class="sxs-lookup"><span data-stu-id="c5e7d-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c5e7d-105">يصف الأصول ومواقع العمل في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="c5e7d-106">إدارة الأصول عبارة عن وحدة نمطية متقدمة لإدارة الأصول ومهام الصيانة في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="c5e7d-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="c5e7d-107">Overview</span></span>

<span data-ttu-id="c5e7d-108">تتكامل إدارة الأصول بسلاسة مع الوحدات النمطية المتعددة مع تطبيقات Finance and Operations الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="c5e7d-109">يبين الرسم التوضيحي التالي الواجهات مع الوحدات النمطية الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-109">The following illustration shows the interfaces with other modules.</span></span>

![يوضح الرسم التخطيطي كيفية عمل واجهات إدارة الأصول مع الوحدات النمطية الأخرى](media/01-overview-image.png)

<span data-ttu-id="c5e7d-111">تسمح لك إدارة الأصول بإدارة وتنفيذ جميع المهام المرتبطة بإدارة وخدمة الكثير من أنواع المعدات في شركتك بطريقة فعالة.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="c5e7d-112">تتضمن هذه المعدات الأجهزة ومعدات الإنتاج والمركبات.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="c5e7d-113">كما تدعم إدارة الأصول الحلول عبر العديد من الصناعات.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="c5e7d-114">يعرض الرسم التوضيحي التالي نظرة عامة على الوظيفة الرئيسية التي تغطيها إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![يوضح الرسم التخطيطي الوظيفة الرئيسية في إدارة الأصول](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="c5e7d-116">الأصول ومواقع العمل</span><span class="sxs-lookup"><span data-stu-id="c5e7d-116">Functional locations and assets</span></span>

<span data-ttu-id="c5e7d-117">تستخدم موقع العمل لإدارة الأصول على المواقع.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="c5e7d-118">وتشتمل عملية الإدارة هذه علي تتبع تكاليف الأصول في مواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="c5e7d-119">يتم بناء مواقع العمل بتدرج هرمي، وبإمكانها أن تتكون من مواقع فرعية.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="c5e7d-120">تعتبر بنية مواقع العمل ثابتة.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-120">The structure of functional locations is static.</span></span> <span data-ttu-id="c5e7d-121">بمعنى آخر، ليس باستطاعة المواقع تغيير مكانها.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-121">In other words, locations can't change place.</span></span> <span data-ttu-id="c5e7d-122">يمكن تثبيت الأصول في مواقع العمل ويمكن تثبيتها في مواقع عمل أخرى لاحقًا، بحسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="c5e7d-123">تتبع تكاليف الأصول دائمًا موقع الأصل.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="c5e7d-124">يعني ذلك أنك ذا قمت بتثبيت أصل في موقع عمل جديد، سيستخدم الأصل تلقائيًا الأبعاد المالية المرتبطة بموقع العمل الجديد.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="c5e7d-125">وبالتالي، ترتبط تكاليف الأصول دائمًا بموقع العمل الذي تم تثبيت الأصل عليه في الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="c5e7d-126">من شأن هذا التعامل التلقائي مع الأبعاد المالية أن يساعد على ضمان التعقب الكامل للتكاليف عندما تقوم شركتك بمراقبة المشاريع وإعداد تقارير بشأنها في مواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="c5e7d-127">تتوقف الطريقة التي تستخدمها لبناء التدرج الهرمي لمواقع العمل على متطلبات شركتك لصيانة المعدات الداخلية أو خدمة معدات العملاء.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="c5e7d-128">يبين الشكل التالي مثالاً عن مواقع العمل التي تستند إلى مواقع جغرافية.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![يوضح الرسم التخطيطي المواقع الوظيفية استنادًا إلى المواقع الجغرافية](media/03-overview-image.png)

<span data-ttu-id="c5e7d-130">يبين الشكل التالي مثالاً عن مواقع العمل التي تستند إلى العملاء.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![يوضح الرسم التخطيطي المواقع الوظيفية بناءً على العملاء](media/04-overview-image.png)
