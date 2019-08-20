---
title: التدرج الهرمي للمؤسسات في Common Data Service
description: يوضح هذا الموضوع تكامل البيانات التنظيمية بين Finance and Operations وCommon Data Service.
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
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789148"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="0ad49-103">التدرج الهرمي للمؤسسات في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="0ad49-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="0ad49-104">بما أن Microsoft Dynamics 365 for Finance and Operations عبارة عن نظام مالي، فإن *المؤسسة* عبارة عن مفهوم أساسي، ويبدأ إعداد النظام بتكوين التدرج الهرمي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="0ad49-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="0ad49-105">ويمكن بعد ذلك تتبع البيانات المالية للشركة وعملياتها على مستوى المؤسسة وكذلك على أي مستوى في التدرج الهرمي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="0ad49-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="0ad49-106">على الرغم من أن Common Data Service لا يتضمن مفهوم التدرج الهرمي للمؤسسة، إلا أنه يتضمن عددًا قليلاً من المفاهيم الفضفاضة، مثل إيراد المبيعات الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="0ad49-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="0ad49-107">كجزء من تكامل Common Data Service، تتم إضافة بنية بيانات التدرج الهرمي للمؤسسات إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0ad49-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="0ad49-108">تدفق البيانات</span><span class="sxs-lookup"><span data-stu-id="0ad49-108">Data flow</span></span>

<span data-ttu-id="0ad49-109">سيستمر وجود التدرج الهرمي للمؤسسات في النظام البيئي للأعمال الذي يتكون من Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="0ad49-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="0ad49-110">تم بناء هذا التدرج الهرمي للمؤسسات استنادًا إلى Finance and Operations، ولكنه يظهر لأغراض تتعلق بالمعلومات وقابلية التوسعة في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0ad49-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="0ad49-111">يبين الرسم التوضيحي التالي معلومات التدرج الهرمي للمؤسسات التي تظهر في Common Data Service كتدفق بيانات أحادي الاتجاه من Finance and Operations إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0ad49-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![صورة البنية الهندسية](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="0ad49-113">القوالب</span><span class="sxs-lookup"><span data-stu-id="0ad49-113">Templates</span></span>

<span data-ttu-id="0ad49-114">تتوفر مخططات كيان التدرج الهرمي للمؤسسات لمزامنة البيانات أحادية الاتجاه من Finance and Operations إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0ad49-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="0ad49-115">غرض التدرج الهرمي للمؤسسات الداخلي</span><span class="sxs-lookup"><span data-stu-id="0ad49-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="0ad49-116">يوفر هذا القالب المزامنة أحادية الاتجاه لكيان غرض التدرج الهرمي للمؤسسات من Finance and Operations إلى Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="0ad49-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="0ad49-117">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="0ad49-117">Source field</span></span> | <span data-ttu-id="0ad49-118">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="0ad49-118">Map type</span></span> | <span data-ttu-id="0ad49-119">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="0ad49-119">Destination field</span></span>
---|---|---
<span data-ttu-id="0ad49-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0ad49-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0ad49-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="0ad49-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="0ad49-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0ad49-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0ad49-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0ad49-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="0ad49-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="0ad49-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="0ad49-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="0ad49-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="0ad49-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="0ad49-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="0ad49-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="0ad49-127">msdyn\_immutable</span></span>
<span data-ttu-id="0ad49-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="0ad49-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="0ad49-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="0ad49-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="0ad49-130">نوع التدرج الهرمي للمؤسسات الداخلية</span><span class="sxs-lookup"><span data-stu-id="0ad49-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="0ad49-131">يوفر هذا القالب المزامنة أحادية الاتجاه لكيان نوع التدرج الهرمي للمؤسسات من Finance and Operations إلى Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="0ad49-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="0ad49-132">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="0ad49-132">Source field</span></span> | <span data-ttu-id="0ad49-133">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="0ad49-133">Map type</span></span> | <span data-ttu-id="0ad49-134">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="0ad49-134">Destination field</span></span>
---|---|---
<span data-ttu-id="0ad49-135">NAME</span><span class="sxs-lookup"><span data-stu-id="0ad49-135">NAME</span></span> | \> | <span data-ttu-id="0ad49-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0ad49-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="0ad49-137">التدرج الهرمي للمؤسسات الداخلية</span><span class="sxs-lookup"><span data-stu-id="0ad49-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="0ad49-138">يوفر هذا القالب المزامنة أحادية الاتجاه لكيان التدرج الهرمي للمؤسسات المنشور من Finance and Operations إلى Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="0ad49-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="0ad49-139">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="0ad49-139">Source field</span></span> | <span data-ttu-id="0ad49-140">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="0ad49-140">Map type</span></span> | <span data-ttu-id="0ad49-141">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="0ad49-141">Destination field</span></span>
---|---|---
<span data-ttu-id="0ad49-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="0ad49-142">VALIDTO</span></span> | \> | <span data-ttu-id="0ad49-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="0ad49-143">msdyn\_validto</span></span>
<span data-ttu-id="0ad49-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="0ad49-144">VALIDFROM</span></span> | \> | <span data-ttu-id="0ad49-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="0ad49-145">msdyn\_validfrom</span></span>
<span data-ttu-id="0ad49-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0ad49-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0ad49-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="0ad49-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="0ad49-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0ad49-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0ad49-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="0ad49-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="0ad49-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0ad49-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0ad49-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="0ad49-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="0ad49-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0ad49-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0ad49-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0ad49-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="0ad49-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0ad49-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0ad49-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0ad49-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="0ad49-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0ad49-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0ad49-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0ad49-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="0ad49-158">مؤسسة داخلية</span><span class="sxs-lookup"><span data-stu-id="0ad49-158">Internal Organization</span></span>

<span data-ttu-id="0ad49-159">إن معلومات المؤسسة الداخلية في Common Data Service تأتي من كيانين في Finance and Operations، **وحدة التشغيل** و**الكيانات القانونية**.</span><span class="sxs-lookup"><span data-stu-id="0ad49-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="0ad49-160">وحدة التشغيل</span><span class="sxs-lookup"><span data-stu-id="0ad49-160">Operating unit</span></span>

<span data-ttu-id="0ad49-161">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="0ad49-161">Source field</span></span> | <span data-ttu-id="0ad49-162">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="0ad49-162">Map type</span></span> | <span data-ttu-id="0ad49-163">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="0ad49-163">Destination field</span></span>
---|---|---
<span data-ttu-id="0ad49-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="0ad49-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="0ad49-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="0ad49-165">msdyn\_languageid</span></span>
<span data-ttu-id="0ad49-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="0ad49-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="0ad49-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="0ad49-167">msdyn\_namealias</span></span>
<span data-ttu-id="0ad49-168">NAME</span><span class="sxs-lookup"><span data-stu-id="0ad49-168">NAME</span></span> | \> | <span data-ttu-id="0ad49-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0ad49-169">msdyn\_name</span></span>
<span data-ttu-id="0ad49-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0ad49-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="0ad49-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0ad49-171">msdyn\_partynumber</span></span>
<span data-ttu-id="0ad49-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="0ad49-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="0ad49-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="0ad49-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="0ad49-174">كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="0ad49-174">Legal entity</span></span>

<span data-ttu-id="0ad49-175">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="0ad49-175">Source field</span></span> | <span data-ttu-id="0ad49-176">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="0ad49-176">Map type</span></span> | <span data-ttu-id="0ad49-177">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="0ad49-177">Destination field</span></span>
---|---|---
<span data-ttu-id="0ad49-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="0ad49-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="0ad49-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="0ad49-179">msdyn\_namealias</span></span>
<span data-ttu-id="0ad49-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="0ad49-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="0ad49-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="0ad49-181">msdyn\_languageid</span></span>
<span data-ttu-id="0ad49-182">NAME</span><span class="sxs-lookup"><span data-stu-id="0ad49-182">NAME</span></span> | \> | <span data-ttu-id="0ad49-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0ad49-183">msdyn\_name</span></span>
<span data-ttu-id="0ad49-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0ad49-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="0ad49-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0ad49-185">msdyn\_partynumber</span></span>
<span data-ttu-id="0ad49-186">none</span><span class="sxs-lookup"><span data-stu-id="0ad49-186">none</span></span> | \>\> | <span data-ttu-id="0ad49-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="0ad49-187">msdyn\_type</span></span>
<span data-ttu-id="0ad49-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="0ad49-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="0ad49-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="0ad49-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="0ad49-190">الشركة</span><span class="sxs-lookup"><span data-stu-id="0ad49-190">Company</span></span>

<span data-ttu-id="0ad49-191">يوفر مزامنة ثنائية الاتجاه لمعلومات الكيان القانوني (الشركة) بين Finance and Operations وCustomer Engagement.</span><span class="sxs-lookup"><span data-stu-id="0ad49-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="0ad49-192">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="0ad49-192">Source field</span></span> | <span data-ttu-id="0ad49-193">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="0ad49-193">Map type</span></span> | <span data-ttu-id="0ad49-194">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="0ad49-194">Destination field</span></span>
---|---|---
<span data-ttu-id="0ad49-195">NAME</span><span class="sxs-lookup"><span data-stu-id="0ad49-195">NAME</span></span> | = | <span data-ttu-id="0ad49-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="0ad49-196">cdm\_name</span></span>
<span data-ttu-id="0ad49-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="0ad49-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="0ad49-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="0ad49-198">cdm\_companycode</span></span>
