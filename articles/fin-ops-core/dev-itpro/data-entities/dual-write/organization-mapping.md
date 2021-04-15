---
title: التدرج الهرمي للمؤسسات في Dataverse
description: يوضح هذا الموضوع تكامل بيانات المؤسسة بين تطبيقات Finance and Operations وDataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8b147c27b9309b1b3597f1194c415fbb2e2b7ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750802"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="35b61-103">التدرج الهرمي للمؤسسات في Dataverse</span><span class="sxs-lookup"><span data-stu-id="35b61-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="35b61-104">بما أن Dynamics 365 Finance عبارة عن نظام مالي، فإن *المؤسسة* عبارة عن مفهوم أساسي، ويبدأ إعداد النظام بتكوين التدرج الهرمي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="35b61-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="35b61-105">ويمكن بعد ذلك تتبع البيانات المالية للشركة على مستوى المؤسسة وكذلك على أي مستوى في التدرج الهرمي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="35b61-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="35b61-106">على الرغم من أن Dataverse لا يتضمن مفهوم التدرج الهرمي للمؤسسة، إلا أنه يتضمن عددًا قليلاً من المفاهيم الفضفاضة، مثل إيراد المبيعات الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="35b61-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="35b61-107">كجزء من تكامل Dataverse، تتم إضافة بنية بيانات التدرج الهرمي للمؤسسات إلى Dataverse.</span><span class="sxs-lookup"><span data-stu-id="35b61-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="35b61-108">تدفق البيانات</span><span class="sxs-lookup"><span data-stu-id="35b61-108">Data flow</span></span>

<span data-ttu-id="35b61-109">سيستمر وجود التدرج الهرمي للمؤسسات في النظام البيئي للأعمال الذي يتكون من تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="35b61-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="35b61-110">تم بناء هذا التدرج الهرمي للمؤسسات استنادًا إلى تطبيقات Finance and Operations ولكنه يظهر في Dataverse لأغراض تتعلق بالمعلومات وقابلية التوسعة.</span><span class="sxs-lookup"><span data-stu-id="35b61-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="35b61-111">يبين الرسم التوضيحي التالي معلومات التدرج الهرمي للمؤسسات التي تظهر في Dataverse كتدفق بيانات أحادي الاتجاه من تطبيقات Finance and Operations إلى Dataverse.</span><span class="sxs-lookup"><span data-stu-id="35b61-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![صورة البنية الهندسية](media/dual-write-data-flow.png)

<span data-ttu-id="35b61-113">تتوفر مخططات جدول التدرج الهرمي للمؤسسات لمزامنة البيانات أحادية الاتجاه من تطبيقات Finance and Operations إلى Dataverse.</span><span class="sxs-lookup"><span data-stu-id="35b61-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="35b61-114">القوالب</span><span class="sxs-lookup"><span data-stu-id="35b61-114">Templates</span></span>

<span data-ttu-id="35b61-115">تحتوي معلومات المنتج على كافة المعلومات المرتبطة بالمنتج وتعريفه، مثل أبعاد المنتج أو أبعاد التعقب والتخزين.</span><span class="sxs-lookup"><span data-stu-id="35b61-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="35b61-116">كما يوضح الجدول التالي، يتم إنشاء مجموعة من مخططات الجداول لمزامنة المنتجات والمعلومات المتعلقة بها.</span><span class="sxs-lookup"><span data-stu-id="35b61-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="35b61-117">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="35b61-117">Finance and Operations apps</span></span> | <span data-ttu-id="35b61-118">تطبيقات Dynamics 365 الأخرى</span><span class="sxs-lookup"><span data-stu-id="35b61-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="35b61-119">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="35b61-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="35b61-120">أغراض التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="35b61-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="35b61-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="35b61-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="35b61-122">يقدم هذا القالب مزامنة أحادية الاتجاه لجدول غرض التدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="35b61-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="35b61-123">نوع التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="35b61-123">Organization hierarchy type</span></span> | <span data-ttu-id="35b61-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="35b61-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="35b61-125">يقدم هذا القالب مزامنة أحادية الاتجاه لجدول نوع التدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="35b61-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="35b61-126">التدرج الهرمي للمؤسسات - منشور</span><span class="sxs-lookup"><span data-stu-id="35b61-126">Organization hierarchy - published</span></span> | <span data-ttu-id="35b61-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="35b61-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="35b61-128">يقدم هذا القالب مزامنة أحادية الاتجاه لجدول المنشور للتدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="35b61-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="35b61-129">وحدة التشغيل</span><span class="sxs-lookup"><span data-stu-id="35b61-129">Operating unit</span></span> | <span data-ttu-id="35b61-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="35b61-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="35b61-131">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="35b61-131">Legal entities</span></span> | <span data-ttu-id="35b61-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="35b61-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="35b61-133">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="35b61-133">Legal entities</span></span> | <span data-ttu-id="35b61-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="35b61-134">cdm_companies</span></span> | <span data-ttu-id="35b61-135">يوفر مزامنة ثنائيه الاتجاه لمعلومات الكيان القانوني (الشركة).</span><span class="sxs-lookup"><span data-stu-id="35b61-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="35b61-136">مؤسسة داخلية</span><span class="sxs-lookup"><span data-stu-id="35b61-136">Internal Organization</span></span>

<span data-ttu-id="35b61-137">تأتي معلومات المؤسسة الداخلية في Dataverse من جدولين، **وحدة التشغيل** و **الكيانات القانونية**.</span><span class="sxs-lookup"><span data-stu-id="35b61-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]