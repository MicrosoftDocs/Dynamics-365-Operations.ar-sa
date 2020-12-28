---
title: تعيين معلمات إدارة المزايا والخدمة الذاتية للموظفين لجميع الشركات
description: تكوين معلمات لإدارة المزايا والخدمة الذاتية للموظفين في Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692687"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="bb5f2-103">تعيين معلمات إدارة المزايا والخدمة الذاتية للموظفين لجميع الشركات</span><span class="sxs-lookup"><span data-stu-id="bb5f2-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

<span data-ttu-id="bb5f2-104">قبل أن تقوم بإعداد خطط المزايا في Microsoft Dynamics 365 Human Resources، يجب عليك تكوين معلمات إدارة المزايا.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="bb5f2-105">تعمل هذه المحددات على تعيين القيم الافتراضية وأكواد الأسباب والخيارات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="bb5f2-106">تكوين المحددات العامة</span><span class="sxs-lookup"><span data-stu-id="bb5f2-106">Configure general parameters</span></span>

1. <span data-ttu-id="bb5f2-107">في مساحة عمل **إدارة الميزات**، ضمن **الإعداد**، حدد **المعلمات المشتركة للموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="bb5f2-108">في علامة التبويب **إدارة المزايا**، حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="bb5f2-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="bb5f2-109">الحقل</span><span class="sxs-lookup"><span data-stu-id="bb5f2-109">Field</span></span> | <span data-ttu-id="bb5f2-110">الوصف</span><span class="sxs-lookup"><span data-stu-id="bb5f2-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bb5f2-111">**البلد/المنطقة**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-111">**Country/region**</span></span> | <span data-ttu-id="bb5f2-112">يحدد الحقل **البلد/المنطقة** ترتيب العرض الأكواد البريدية/الولايات .</span><span class="sxs-lookup"><span data-stu-id="bb5f2-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="bb5f2-113">يتم عرض البلد المحدد في القائمة المنسدلة أولاً.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="bb5f2-114">**كود سبب التسجيل**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-114">**Enrollment reason code**</span></span> | <span data-ttu-id="bb5f2-115">حدد كود السبب الافتراضي المراد استخدامه عند إنشاء خطط الموظفين أثناء معالجة التسجيل المفتوح.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="bb5f2-116">**كود سبب الإلغاء**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-116">**Cancellation reason code**</span></span> | <span data-ttu-id="bb5f2-117">كود السبب المطلوب استخدامه عند إلغاء خطة فائدة موظف.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="bb5f2-118">ويتم عرضه في مربع حوار أثناء عملية الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="bb5f2-119">يمكن للمستخدمين تغيير **كود سبب الإلغاء** إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="bb5f2-120">**كود سبب إعادة الفتح**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-120">**Reopen reason code**</span></span> | <span data-ttu-id="bb5f2-121">كود السبب المطلوب استخدامه عند إعادة فتح خطة فائدة موظف.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="bb5f2-122">ويتم عرضه في مربع حوار أثناء عملية الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="bb5f2-123">يمكن للمستخدمين تغيير **إعادة فتح كود السبب** إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="bb5f2-124">**رمز سبب حدث الحياة**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-124">**Life event reason code**</span></span> | <span data-ttu-id="bb5f2-125">كود السبب المراد استخدامه عند حدوث حدث حياتي.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="bb5f2-126">**رمز سبب تغيير المعدل**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-126">**Rate change reason code**</span></span> | <span data-ttu-id="bb5f2-127">كود السبب المراد استخدامه عند إلغاء خطة ميزة خاصة بموظف وإعادة فتحها أثناء عملية تحديث تغيير المعدل.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="bb5f2-128">ويشير ذلك إلى السجلات التي تم تغييرها بواسطة عملية تحديث تغيير المعدل.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="bb5f2-129">**راتب المزايا السنوي**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-129">**Benefits annual salary**</span></span> | <span data-ttu-id="bb5f2-130">يمكِّنك من تعيين مبلغ **الراتب السنوي للميزات** لأحد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="bb5f2-131">تستخدم الموارد البشرية مبلغ **الراتب السنوي للميزات** عند تحديد مبالغ التغطية، بدلاً من المبلغ السنوي للتعويض الثابت.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="bb5f2-132">**توظيف جديد مستحق**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-132">**New hire eligible**</span></span> | <span data-ttu-id="bb5f2-133">يحدد ما إذا كان الموظفين الجدد مؤهلين أم لا.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="bb5f2-134">**فترة تسجيل التوظيف الجديدة**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-134">**New hire enrollment period**</span></span> | <span data-ttu-id="bb5f2-135">الفترة الزمنية التي يتم فيها السماح بتسجيل التوظيف الجديد.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="bb5f2-136">**ملاحظة**: يتجاوز هذا الإعداد أية فترة تسجيل توظيف جديدة قمت بتعيينها في القواعد الأهلية للخطة.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="bb5f2-137">**تكرار الدفع الافتراضي**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-137">**Default pay frequency**</span></span> | <span data-ttu-id="bb5f2-138">تكرار الدفع الافتراضي المطلوب استخدامه عند إضافة عمال جدد.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="bb5f2-139">**تم تمكين أحداث الحياة**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-139">**Life events enabled**</span></span> | <span data-ttu-id="bb5f2-140">يعمل على تمكين الأحداث الحياتية.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-140">Enables life events.</span></span> |
   | <span data-ttu-id="bb5f2-141">**إخفاء نماذج المزايا القديمة**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="bb5f2-142">يسمح لك بإخفاء نماذج الميزة القديمة.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="bb5f2-143">**التحقق من صحة الميزة**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-143">**Benefit verification**</span></span> | <span data-ttu-id="bb5f2-144">نص التحقق المطلوب استخدامه أثناء سحب ميزات الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="bb5f2-145">**تحديد المعينين تلقائيًا**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-145">**Auto select designees**</span></span> | <span data-ttu-id="bb5f2-146">يحدد ما إذا كان سيتم تحديد المعالين والمستفيدين تلقائيًا وفقًا لأهلية خيارات الخطة أم لا.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="bb5f2-147">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="bb5f2-148">تكوين معلمات خدمة الموظف الذاتية</span><span class="sxs-lookup"><span data-stu-id="bb5f2-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="bb5f2-149">في مساحة عمل **إدارة الميزات**، ضمن **الإعداد**، حدد **معلمات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="bb5f2-150">في علامة التبويب **إدارة المزايا**، حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="bb5f2-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="bb5f2-151">الحقل</span><span class="sxs-lookup"><span data-stu-id="bb5f2-151">Field</span></span> | <span data-ttu-id="bb5f2-152">الوصف</span><span class="sxs-lookup"><span data-stu-id="bb5f2-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bb5f2-153">**التحقق من صحة الميزة**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-153">**Benefit verification**</span></span> | <span data-ttu-id="bb5f2-154">نص التحقق المطلوب استخدامه أثناء سحب ميزات الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="bb5f2-155">**تحديد المعينين تلقائيًا**</span><span class="sxs-lookup"><span data-stu-id="bb5f2-155">**Auto select designees**</span></span> | <span data-ttu-id="bb5f2-156">يحدد ما إذا كان سيتم تحديد المعالين والمستفيدين تلقائيًا وفقًا لأهلية خيارات الخطة أم لا.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="bb5f2-157">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bb5f2-157">Select **Save**.</span></span>


