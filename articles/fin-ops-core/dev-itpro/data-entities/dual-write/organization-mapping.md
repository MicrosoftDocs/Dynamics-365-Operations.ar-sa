---
title: التدرج الهرمي للمؤسسات في Common Data Service
description: يوضح هذا الموضوع تكامل بيانات المؤسسة بين تطبيقات Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f502519ba419cb8fa322eb1d22f06d2b805f5f05
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000724"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="43a92-103">التدرج الهرمي للمؤسسات في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="43a92-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="43a92-104">بما أن Dynamics 365 Finance عبارة عن نظام مالي، فإن *المؤسسة* عبارة عن مفهوم أساسي، ويبدأ إعداد النظام بتكوين التدرج الهرمي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="43a92-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="43a92-105">ويمكن بعد ذلك تتبع البيانات المالية للشركة على مستوى المؤسسة وكذلك على أي مستوى في التدرج الهرمي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="43a92-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="43a92-106">على الرغم من أن Common Data Service لا يتضمن مفهوم التدرج الهرمي للمؤسسة، إلا أنه يتضمن عددًا قليلاً من المفاهيم الفضفاضة، مثل إيراد المبيعات الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="43a92-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="43a92-107">كجزء من تكامل Common Data Service، تتم إضافة بنية بيانات التدرج الهرمي للمؤسسات إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="43a92-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="43a92-108">تدفق البيانات</span><span class="sxs-lookup"><span data-stu-id="43a92-108">Data flow</span></span>

<span data-ttu-id="43a92-109">سيستمر وجود التدرج الهرمي للمؤسسات في النظام البيئي للأعمال الذي يتكون من تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="43a92-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="43a92-110">تم بناء هذا التدرج الهرمي للمؤسسات استنادًا إلى تطبيقات Finance and Operations ولكنه يظهر في Common Data Service لأغراض تتعلق بالمعلومات وقابلية التوسعة.</span><span class="sxs-lookup"><span data-stu-id="43a92-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="43a92-111">يبين الرسم التوضيحي التالي معلومات التدرج الهرمي للمؤسسات التي تظهر في Common Data Service كتدفق بيانات أحادي الاتجاه من تطبيقات Finance and Operations إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="43a92-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![صورة البنية الهندسية](media/dual-write-data-flow.png)

<span data-ttu-id="43a92-113">تتوفر مخططات كيان التدرج الهرمي للمؤسسات لمزامنة البيانات أحادية الاتجاه من تطبيقات Finance and Operations إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="43a92-113">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="43a92-114">القوالب</span><span class="sxs-lookup"><span data-stu-id="43a92-114">Templates</span></span>

<span data-ttu-id="43a92-115">تحتوي معلومات المنتج على كافة المعلومات المرتبطة بالمنتج وتعريفه، مثل أبعاد المنتج أو أبعاد التعقب والتخزين.</span><span class="sxs-lookup"><span data-stu-id="43a92-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="43a92-116">كما يوضح الجدول التالي، يتم إنشاء مجموعة من مخططات الكيانات لمزامنة المنتجات والمعلومات المتعلقة بها.</span><span class="sxs-lookup"><span data-stu-id="43a92-116">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="43a92-117">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="43a92-117">Finance and Operations apps</span></span> | <span data-ttu-id="43a92-118">تطبيقات Dynamics 365 الأخرى</span><span class="sxs-lookup"><span data-stu-id="43a92-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="43a92-119">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="43a92-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="43a92-120">أغراض التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="43a92-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="43a92-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="43a92-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="43a92-122">يقدم هذا القالب مزامنة أحادية الاتجاه لكيان غرض التدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="43a92-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="43a92-123">نوع التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="43a92-123">Organization hierarchy type</span></span> | <span data-ttu-id="43a92-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="43a92-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="43a92-125">يقدم هذا القالب مزامنة أحادية الاتجاه لكيان نوع التدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="43a92-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="43a92-126">التدرج الهرمي للمؤسسات - منشور</span><span class="sxs-lookup"><span data-stu-id="43a92-126">Organization hierarchy - published</span></span> | <span data-ttu-id="43a92-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="43a92-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="43a92-128">يقدم هذا القالب مزامنة أحادية الاتجاه للكيان المنشور للتدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="43a92-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="43a92-129">وحدة التشغيل</span><span class="sxs-lookup"><span data-stu-id="43a92-129">Operating unit</span></span> | <span data-ttu-id="43a92-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="43a92-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="43a92-131">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="43a92-131">Legal entities</span></span> | <span data-ttu-id="43a92-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="43a92-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="43a92-133">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="43a92-133">Legal entities</span></span> | <span data-ttu-id="43a92-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="43a92-134">cdm_companies</span></span> | <span data-ttu-id="43a92-135">يوفر مزامنة ثنائيه الاتجاه لمعلومات الكيان القانوني (الشركة).</span><span class="sxs-lookup"><span data-stu-id="43a92-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="43a92-136">مؤسسة داخلية</span><span class="sxs-lookup"><span data-stu-id="43a92-136">Internal Organization</span></span>

<span data-ttu-id="43a92-137">تأتي معلومات المؤسسة الداخلية في Common Data Service من كيانين، **وحدة التشغيل** و **الكيانات القانونية**.</span><span class="sxs-lookup"><span data-stu-id="43a92-137">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
