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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572439"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="f0a83-103">التدرج الهرمي للمؤسسات في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f0a83-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="f0a83-104">بما أن Dynamics 365 Finance عبارة عن نظام مالي، فإن *المؤسسة* عبارة عن مفهوم أساسي، ويبدأ إعداد النظام بتكوين التدرج الهرمي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="f0a83-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="f0a83-105">ويمكن بعد ذلك تتبع البيانات المالية للشركة على مستوى المؤسسة وكذلك على أي مستوى في التدرج الهرمي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="f0a83-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="f0a83-106">على الرغم من أن Common Data Service لا يتضمن مفهوم التدرج الهرمي للمؤسسة، إلا أنه يتضمن عددًا قليلاً من المفاهيم الفضفاضة، مثل إيراد المبيعات الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="f0a83-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="f0a83-107">كجزء من تكامل Common Data Service، تتم إضافة بنية بيانات التدرج الهرمي للمؤسسات إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f0a83-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="f0a83-108">تدفق البيانات</span><span class="sxs-lookup"><span data-stu-id="f0a83-108">Data flow</span></span>

<span data-ttu-id="f0a83-109">سيستمر وجود التدرج الهرمي للمؤسسات في النظام البيئي للأعمال الذي يتكون من تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="f0a83-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="f0a83-110">تم بناء هذا التدرج الهرمي للمؤسسات استنادًا إلى تطبيقات Finance and Operations، ولكنه يظهر لأغراض تتعلق بالمعلومات وقابلية التوسعة في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f0a83-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="f0a83-111">يبين الرسم التوضيحي التالي معلومات التدرج الهرمي للمؤسسات التي تظهر في Common Data Service كتدفق بيانات أحادي الاتجاه من تطبيقات Finance and Operations إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f0a83-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![صورة البنية الهندسية](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="f0a83-113">القوالب</span><span class="sxs-lookup"><span data-stu-id="f0a83-113">Templates</span></span>

<span data-ttu-id="f0a83-114">تتوفر مخططات كيان التدرج الهرمي للمؤسسات لمزامنة البيانات أحادية الاتجاه من تطبيقات Finance and Operations إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f0a83-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="f0a83-115">غرض التدرج الهرمي للمؤسسات الداخلي</span><span class="sxs-lookup"><span data-stu-id="f0a83-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="f0a83-116">يوفر هذا القالب المزامنة أحادية الاتجاه لكيان غرض التدرج الهرمي للمؤسسات من Finance and Operations إلى تطبيقات Dynamics 365 الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f0a83-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="f0a83-117">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="f0a83-117">Source field</span></span> | <span data-ttu-id="f0a83-118">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="f0a83-118">Map type</span></span> | <span data-ttu-id="f0a83-119">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="f0a83-119">Destination field</span></span>
---|---|---
<span data-ttu-id="f0a83-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="f0a83-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="f0a83-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="f0a83-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="f0a83-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="f0a83-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="f0a83-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="f0a83-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="f0a83-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="f0a83-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="f0a83-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="f0a83-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="f0a83-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="f0a83-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="f0a83-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="f0a83-127">msdyn\_immutable</span></span>
<span data-ttu-id="f0a83-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="f0a83-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="f0a83-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="f0a83-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="f0a83-130">نوع التدرج الهرمي للمؤسسات الداخلية</span><span class="sxs-lookup"><span data-stu-id="f0a83-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="f0a83-131">يوفر هذا القالب المزامنة أحادية الاتجاه لكيان نوع التدرج الهرمي للمؤسسات من Finance and Operations إلى تطبيقات Dynamics 365 الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f0a83-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="f0a83-132">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="f0a83-132">Source field</span></span> | <span data-ttu-id="f0a83-133">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="f0a83-133">Map type</span></span> | <span data-ttu-id="f0a83-134">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="f0a83-134">Destination field</span></span>
---|---|---
<span data-ttu-id="f0a83-135">الاسم</span><span class="sxs-lookup"><span data-stu-id="f0a83-135">NAME</span></span> | \> | <span data-ttu-id="f0a83-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="f0a83-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="f0a83-137">التدرج الهرمي للمؤسسات الداخلية</span><span class="sxs-lookup"><span data-stu-id="f0a83-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="f0a83-138">يوفر هذا القالب المزامنة أحادية الاتجاه للكيان المنشور للتدرج الهرمي للمؤسسات من Finance and Operations إلى تطبيقات Dynamics 365 الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f0a83-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="f0a83-139">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="f0a83-139">Source field</span></span> | <span data-ttu-id="f0a83-140">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="f0a83-140">Map type</span></span> | <span data-ttu-id="f0a83-141">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="f0a83-141">Destination field</span></span>
---|---|---
<span data-ttu-id="f0a83-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="f0a83-142">VALIDTO</span></span> | \> | <span data-ttu-id="f0a83-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="f0a83-143">msdyn\_validto</span></span>
<span data-ttu-id="f0a83-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="f0a83-144">VALIDFROM</span></span> | \> | <span data-ttu-id="f0a83-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="f0a83-145">msdyn\_validfrom</span></span>
<span data-ttu-id="f0a83-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="f0a83-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="f0a83-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="f0a83-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="f0a83-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f0a83-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="f0a83-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="f0a83-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="f0a83-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f0a83-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="f0a83-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="f0a83-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="f0a83-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="f0a83-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="f0a83-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="f0a83-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="f0a83-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f0a83-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="f0a83-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="f0a83-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="f0a83-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f0a83-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="f0a83-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="f0a83-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="f0a83-158">مؤسسة داخلية</span><span class="sxs-lookup"><span data-stu-id="f0a83-158">Internal Organization</span></span>

<span data-ttu-id="f0a83-159">تأتي معلومات المؤسسة الداخلية في Common Data Service من كيانين، **وحدة التشغيل** و**الكيانات القانونية**.</span><span class="sxs-lookup"><span data-stu-id="f0a83-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="f0a83-160">وحدة التشغيل</span><span class="sxs-lookup"><span data-stu-id="f0a83-160">Operating unit</span></span>

<span data-ttu-id="f0a83-161">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="f0a83-161">Source field</span></span> | <span data-ttu-id="f0a83-162">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="f0a83-162">Map type</span></span> | <span data-ttu-id="f0a83-163">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="f0a83-163">Destination field</span></span>
---|---|---
<span data-ttu-id="f0a83-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="f0a83-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="f0a83-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="f0a83-165">msdyn\_languageid</span></span>
<span data-ttu-id="f0a83-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="f0a83-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="f0a83-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="f0a83-167">msdyn\_namealias</span></span>
<span data-ttu-id="f0a83-168">NAME</span><span class="sxs-lookup"><span data-stu-id="f0a83-168">NAME</span></span> | \> | <span data-ttu-id="f0a83-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="f0a83-169">msdyn\_name</span></span>
<span data-ttu-id="f0a83-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f0a83-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="f0a83-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="f0a83-171">msdyn\_partynumber</span></span>
<span data-ttu-id="f0a83-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="f0a83-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="f0a83-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="f0a83-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="f0a83-174">كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="f0a83-174">Legal entity</span></span>

<span data-ttu-id="f0a83-175">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="f0a83-175">Source field</span></span> | <span data-ttu-id="f0a83-176">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="f0a83-176">Map type</span></span> | <span data-ttu-id="f0a83-177">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="f0a83-177">Destination field</span></span>
---|---|---
<span data-ttu-id="f0a83-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="f0a83-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="f0a83-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="f0a83-179">msdyn\_namealias</span></span>
<span data-ttu-id="f0a83-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="f0a83-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="f0a83-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="f0a83-181">msdyn\_languageid</span></span>
<span data-ttu-id="f0a83-182">NAME</span><span class="sxs-lookup"><span data-stu-id="f0a83-182">NAME</span></span> | \> | <span data-ttu-id="f0a83-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="f0a83-183">msdyn\_name</span></span>
<span data-ttu-id="f0a83-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f0a83-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="f0a83-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="f0a83-185">msdyn\_partynumber</span></span>
<span data-ttu-id="f0a83-186">none</span><span class="sxs-lookup"><span data-stu-id="f0a83-186">none</span></span> | \>\> | <span data-ttu-id="f0a83-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="f0a83-187">msdyn\_type</span></span>
<span data-ttu-id="f0a83-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="f0a83-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="f0a83-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="f0a83-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="f0a83-190">الشركة</span><span class="sxs-lookup"><span data-stu-id="f0a83-190">Company</span></span>

<span data-ttu-id="f0a83-191">يوفر مزامنة ثنائية الاتجاه لمعلومات الكيان القانوني (الشركة) بين Finance and Operations وتطبيقات Dynamics 365 الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f0a83-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="f0a83-192">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="f0a83-192">Source field</span></span> | <span data-ttu-id="f0a83-193">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="f0a83-193">Map type</span></span> | <span data-ttu-id="f0a83-194">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="f0a83-194">Destination field</span></span>
---|---|---
<span data-ttu-id="f0a83-195">الاسم</span><span class="sxs-lookup"><span data-stu-id="f0a83-195">NAME</span></span> | = | <span data-ttu-id="f0a83-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="f0a83-196">cdm\_name</span></span>
<span data-ttu-id="f0a83-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="f0a83-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="f0a83-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="f0a83-198">cdm\_companycode</span></span>
