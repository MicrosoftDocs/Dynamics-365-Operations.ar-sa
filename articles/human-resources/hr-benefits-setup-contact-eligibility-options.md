---
title: تكوين خيارات أهلية جهة الاتصال الشخصية
description: قم بتكوين خيارات الأهلية لجهات الاتصال الشخصية في Microsoft Dynamics 365 Human Resources. يمكن أن تكون جهات الاتصال الشخصية من المستفيدين أو التابعين.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68364b0cc1c579a3ee9813474c9d3f6e4df1c05d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430752"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="ce886-104">تكوين خيارات أهلية جهة الاتصال الشخصية</span><span class="sxs-lookup"><span data-stu-id="ce886-104">Configure personal contact eligibility options</span></span>

<span data-ttu-id="ce886-105">يوضح هذا المقال كيفية تكوين أنواع جهات الاتصال الشخصية لاستخدامها في الميزات الموجودة في Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ce886-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ce886-106">يمكن أن تكون جهات الاتصال الشخصية من المستفيدين أو التابعين.</span><span class="sxs-lookup"><span data-stu-id="ce886-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="ce886-107">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **خيارات أهلية جهات الاتصال الشخصية**.</span><span class="sxs-lookup"><span data-stu-id="ce886-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="ce886-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ce886-108">Select **New**.</span></span>

3. <span data-ttu-id="ce886-109">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="ce886-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ce886-110">الحقل</span><span class="sxs-lookup"><span data-stu-id="ce886-110">Field</span></span> | <span data-ttu-id="ce886-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="ce886-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ce886-112">**خيار الاستحقاق**</span><span class="sxs-lookup"><span data-stu-id="ce886-112">**Eligibility option**</span></span> | <span data-ttu-id="ce886-113">اسم أو كود خيار أهلية فريد لتحديد خيار الأهلية.</span><span class="sxs-lookup"><span data-stu-id="ce886-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="ce886-114">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="ce886-114">**Description**</span></span> | <span data-ttu-id="ce886-115">وصف مختصر لخيار الأهلية.</span><span class="sxs-lookup"><span data-stu-id="ce886-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="ce886-116">**كود استحقاق جهات الاتصال**</span><span class="sxs-lookup"><span data-stu-id="ce886-116">**Contact eligibility code**</span></span> | <span data-ttu-id="ce886-117">كود النظام الذي يصف خيار الاستحقاق الشخصي بشكل أفضل.</span><span class="sxs-lookup"><span data-stu-id="ce886-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="ce886-118">يمكنك الاختيار من بين:</span><span class="sxs-lookup"><span data-stu-id="ce886-118">You can choose from:</span></span> <ul><li><span data-ttu-id="ce886-119">العلاقة</span><span class="sxs-lookup"><span data-stu-id="ce886-119">Relationship</span></span></li><li><span data-ttu-id="ce886-120">الطالب</span><span class="sxs-lookup"><span data-stu-id="ce886-120">Student</span></span></li><li><span data-ttu-id="ce886-121">معال مسن</span><span class="sxs-lookup"><span data-stu-id="ce886-121">Overage dependent</span></span></li><li><span data-ttu-id="ce886-122">المعال المعاق المسن</span><span class="sxs-lookup"><span data-stu-id="ce886-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="ce886-123">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="ce886-123">**Status**</span></span> | <span data-ttu-id="ce886-124">حالة خيار الأهلية.</span><span class="sxs-lookup"><span data-stu-id="ce886-124">The status of the eligibility option.</span></span> <span data-ttu-id="ce886-125">إذا تم تعيين حالة أحد خيارات الأهلية على غير نشط، فلا يمكنك تحديد خيار أهلية الاتصال الشخصي لجهات الاتصال الشخصية.</span><span class="sxs-lookup"><span data-stu-id="ce886-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="ce886-126">**العلاقة**</span><span class="sxs-lookup"><span data-stu-id="ce886-126">**Relationship**</span></span> | <span data-ttu-id="ce886-127">يحدد العلاقة بين جهة الاتصال الشخصية والموظف.</span><span class="sxs-lookup"><span data-stu-id="ce886-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="ce886-128">يكون هذا الحقل نشطًا فقط في حالة تعيين كود أهلية جهة الاتصال على العلاقة.</span><span class="sxs-lookup"><span data-stu-id="ce886-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="ce886-129">**العمر**</span><span class="sxs-lookup"><span data-stu-id="ce886-129">**Age**</span></span> | <span data-ttu-id="ce886-130">السن الأقصى لجهة اتصال شخصية مؤهلة لخطة الميزة.</span><span class="sxs-lookup"><span data-stu-id="ce886-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="ce886-131">يكون هذا الحقل نشطًا فقط في حالة تحديد علاقة.</span><span class="sxs-lookup"><span data-stu-id="ce886-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="ce886-132">تتم مقارنة هذا العمر بالسن المحسوب لجهة الاتصال الشخصية.</span><span class="sxs-lookup"><span data-stu-id="ce886-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="ce886-133">السن المحسوب هو: (تاريخ التغطية – تاريخ ميلاد جهة اتصال شخصية / 365).</span><span class="sxs-lookup"><span data-stu-id="ce886-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="ce886-134">ودائمًا ما يكون هذا الرقم عددًا صحيحًا.</span><span class="sxs-lookup"><span data-stu-id="ce886-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="ce886-135">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ce886-135">Select **Save**.</span></span> 
