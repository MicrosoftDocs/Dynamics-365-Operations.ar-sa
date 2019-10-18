---
title: التدرج الهرمي للمؤسسات في Common Data Service
description: يوضح هذا الموضوع تكامل البيانات التنظيمية بين تطبيقات Finance and Operations وCommon Data Service.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182015"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="21a7a-103">التدرج الهرمي للمؤسسات في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="21a7a-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="21a7a-104">بما أن Dynamics 365 Finance عبارة عن نظام مالي، فإن *المؤسسة* عبارة عن مفهوم أساسي، ويبدأ إعداد النظام بتكوين التدرج الهرمي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="21a7a-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="21a7a-105">ويمكن بعد ذلك تتبع البيانات المالية للشركة على مستوى المؤسسة وكذلك على أي مستوى في التدرج الهرمي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="21a7a-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="21a7a-106">على الرغم من أن Common Data Service لا يتضمن مفهوم التدرج الهرمي للمؤسسة، إلا أنه يتضمن عددًا قليلاً من المفاهيم الفضفاضة، مثل إيراد المبيعات الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="21a7a-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="21a7a-107">كجزء من تكامل Common Data Service، تتم إضافة بنية بيانات التدرج الهرمي للمؤسسات إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="21a7a-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="21a7a-108">تدفق البيانات</span><span class="sxs-lookup"><span data-stu-id="21a7a-108">Data flow</span></span>

<span data-ttu-id="21a7a-109">سيستمر وجود التدرج الهرمي للمؤسسات في النظام البيئي للأعمال الذي يتكون من تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="21a7a-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="21a7a-110">تم بناء هذا التدرج الهرمي للمؤسسات استنادًا إلى تطبيقات Finance and Operations، ولكنه يظهر لأغراض تتعلق بالمعلومات وقابلية التوسعة في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="21a7a-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="21a7a-111">يبين الرسم التوضيحي التالي معلومات التدرج الهرمي للمؤسسات التي تظهر في Common Data Service كتدفق بيانات أحادي الاتجاه من تطبيقات Finance and Operations إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="21a7a-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![صورة البنية الهندسية](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="21a7a-113">القوالب</span><span class="sxs-lookup"><span data-stu-id="21a7a-113">Templates</span></span>

<span data-ttu-id="21a7a-114">تتوفر مخططات كيان التدرج الهرمي للمؤسسات لمزامنة البيانات أحادية الاتجاه من تطبيقات Finance and Operations إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="21a7a-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="21a7a-115">غرض التدرج الهرمي للمؤسسات الداخلي</span><span class="sxs-lookup"><span data-stu-id="21a7a-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="21a7a-116">يوفر هذا القالب المزامنة أحادية الاتجاه لكيان غرض التدرج الهرمي للمؤسسات من Finance and Operations إلى تطبيقات Dynamics 365 الأخرى.</span><span class="sxs-lookup"><span data-stu-id="21a7a-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="21a7a-117">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="21a7a-117">Source field</span></span> | <span data-ttu-id="21a7a-118">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="21a7a-118">Map type</span></span> | <span data-ttu-id="21a7a-119">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="21a7a-119">Destination field</span></span>
---|---|---
<span data-ttu-id="21a7a-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="21a7a-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="21a7a-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="21a7a-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="21a7a-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="21a7a-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="21a7a-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="21a7a-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="21a7a-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="21a7a-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="21a7a-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="21a7a-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="21a7a-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="21a7a-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="21a7a-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="21a7a-127">msdyn\_immutable</span></span>
<span data-ttu-id="21a7a-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="21a7a-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="21a7a-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="21a7a-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="21a7a-130">نوع التدرج الهرمي للمؤسسات الداخلية</span><span class="sxs-lookup"><span data-stu-id="21a7a-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="21a7a-131">يوفر هذا القالب المزامنة أحادية الاتجاه لكيان نوع التدرج الهرمي للمؤسسات من Finance and Operations إلى تطبيقات Dynamics 365 الأخرى.</span><span class="sxs-lookup"><span data-stu-id="21a7a-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="21a7a-132">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="21a7a-132">Source field</span></span> | <span data-ttu-id="21a7a-133">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="21a7a-133">Map type</span></span> | <span data-ttu-id="21a7a-134">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="21a7a-134">Destination field</span></span>
---|---|---
<span data-ttu-id="21a7a-135">الاسم</span><span class="sxs-lookup"><span data-stu-id="21a7a-135">NAME</span></span> | \> | <span data-ttu-id="21a7a-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="21a7a-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="21a7a-137">التدرج الهرمي للمؤسسات الداخلية</span><span class="sxs-lookup"><span data-stu-id="21a7a-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="21a7a-138">يوفر هذا القالب المزامنة أحادية الاتجاه للكيان المنشور للتدرج الهرمي للمؤسسات من Finance and Operations إلى تطبيقات Dynamics 365 الأخرى.</span><span class="sxs-lookup"><span data-stu-id="21a7a-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="21a7a-139">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="21a7a-139">Source field</span></span> | <span data-ttu-id="21a7a-140">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="21a7a-140">Map type</span></span> | <span data-ttu-id="21a7a-141">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="21a7a-141">Destination field</span></span>
---|---|---
<span data-ttu-id="21a7a-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="21a7a-142">VALIDTO</span></span> | \> | <span data-ttu-id="21a7a-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="21a7a-143">msdyn\_validto</span></span>
<span data-ttu-id="21a7a-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="21a7a-144">VALIDFROM</span></span> | \> | <span data-ttu-id="21a7a-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="21a7a-145">msdyn\_validfrom</span></span>
<span data-ttu-id="21a7a-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="21a7a-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="21a7a-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="21a7a-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="21a7a-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="21a7a-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="21a7a-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="21a7a-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="21a7a-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="21a7a-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="21a7a-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="21a7a-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="21a7a-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="21a7a-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="21a7a-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="21a7a-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="21a7a-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="21a7a-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="21a7a-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="21a7a-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="21a7a-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="21a7a-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="21a7a-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="21a7a-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="21a7a-158">مؤسسة داخلية</span><span class="sxs-lookup"><span data-stu-id="21a7a-158">Internal Organization</span></span>

<span data-ttu-id="21a7a-159">تأتي معلومات المؤسسة الداخلية في Common Data Service من كيانين، **وحدة التشغيل** و**الكيانات القانونية**.</span><span class="sxs-lookup"><span data-stu-id="21a7a-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="21a7a-160">وحدة التشغيل</span><span class="sxs-lookup"><span data-stu-id="21a7a-160">Operating unit</span></span>

<span data-ttu-id="21a7a-161">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="21a7a-161">Source field</span></span> | <span data-ttu-id="21a7a-162">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="21a7a-162">Map type</span></span> | <span data-ttu-id="21a7a-163">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="21a7a-163">Destination field</span></span>
---|---|---
<span data-ttu-id="21a7a-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="21a7a-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="21a7a-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="21a7a-165">msdyn\_languageid</span></span>
<span data-ttu-id="21a7a-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="21a7a-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="21a7a-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="21a7a-167">msdyn\_namealias</span></span>
<span data-ttu-id="21a7a-168">NAME</span><span class="sxs-lookup"><span data-stu-id="21a7a-168">NAME</span></span> | \> | <span data-ttu-id="21a7a-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="21a7a-169">msdyn\_name</span></span>
<span data-ttu-id="21a7a-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="21a7a-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="21a7a-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="21a7a-171">msdyn\_partynumber</span></span>
<span data-ttu-id="21a7a-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="21a7a-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="21a7a-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="21a7a-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="21a7a-174">كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="21a7a-174">Legal entity</span></span>

<span data-ttu-id="21a7a-175">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="21a7a-175">Source field</span></span> | <span data-ttu-id="21a7a-176">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="21a7a-176">Map type</span></span> | <span data-ttu-id="21a7a-177">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="21a7a-177">Destination field</span></span>
---|---|---
<span data-ttu-id="21a7a-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="21a7a-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="21a7a-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="21a7a-179">msdyn\_namealias</span></span>
<span data-ttu-id="21a7a-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="21a7a-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="21a7a-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="21a7a-181">msdyn\_languageid</span></span>
<span data-ttu-id="21a7a-182">NAME</span><span class="sxs-lookup"><span data-stu-id="21a7a-182">NAME</span></span> | \> | <span data-ttu-id="21a7a-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="21a7a-183">msdyn\_name</span></span>
<span data-ttu-id="21a7a-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="21a7a-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="21a7a-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="21a7a-185">msdyn\_partynumber</span></span>
<span data-ttu-id="21a7a-186">none</span><span class="sxs-lookup"><span data-stu-id="21a7a-186">none</span></span> | \>\> | <span data-ttu-id="21a7a-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="21a7a-187">msdyn\_type</span></span>
<span data-ttu-id="21a7a-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="21a7a-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="21a7a-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="21a7a-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="21a7a-190">الشركة</span><span class="sxs-lookup"><span data-stu-id="21a7a-190">Company</span></span>

<span data-ttu-id="21a7a-191">يوفر مزامنة ثنائية الاتجاه لمعلومات الكيان القانوني (الشركة) بين Finance and Operations وتطبيقات Dynamics 365 الأخرى.</span><span class="sxs-lookup"><span data-stu-id="21a7a-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="21a7a-192">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="21a7a-192">Source field</span></span> | <span data-ttu-id="21a7a-193">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="21a7a-193">Map type</span></span> | <span data-ttu-id="21a7a-194">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="21a7a-194">Destination field</span></span>
---|---|---
<span data-ttu-id="21a7a-195">الاسم</span><span class="sxs-lookup"><span data-stu-id="21a7a-195">NAME</span></span> | = | <span data-ttu-id="21a7a-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="21a7a-196">cdm\_name</span></span>
<span data-ttu-id="21a7a-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="21a7a-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="21a7a-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="21a7a-198">cdm\_companycode</span></span>
