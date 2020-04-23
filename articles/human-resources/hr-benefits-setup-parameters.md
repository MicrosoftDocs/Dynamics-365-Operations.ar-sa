---
title: تعيين محددات إدارة الميزات
description: قم بتكوين المحددات لإدارة الميزات في Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d6d463df08b9ae68047f09316f19e98740a8441
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229753"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="e23ba-103">تعيين معلمات إدارة المزايا</span><span class="sxs-lookup"><span data-stu-id="e23ba-103">Set Benefits management parameters</span></span>

<span data-ttu-id="e23ba-104">قبل أن تقوم بإعداد خطط الإجازات في Microsoft Dynamics 365 Human Resources، يجب عليك تكوين محددات إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="e23ba-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="e23ba-105">تعمل هذه المحددات على تعيين القيم الافتراضية وأكواد الأسباب والخيارات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="e23ba-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="e23ba-106">تكوين المحددات العامة</span><span class="sxs-lookup"><span data-stu-id="e23ba-106">Configure general parameters</span></span>

1. <span data-ttu-id="e23ba-107">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **المحددات**.</span><span class="sxs-lookup"><span data-stu-id="e23ba-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="e23ba-108">في علامة التبويب **عام** ، حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="e23ba-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="e23ba-109">الحقل</span><span class="sxs-lookup"><span data-stu-id="e23ba-109">Field</span></span> | <span data-ttu-id="e23ba-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="e23ba-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e23ba-111">**البلد/المنطقة**</span><span class="sxs-lookup"><span data-stu-id="e23ba-111">**Country/region**</span></span> | <span data-ttu-id="e23ba-112">يحدد الحقل **البلد/المنطقة** ترتيب العرض الأكواد البريدية/الولايات .</span><span class="sxs-lookup"><span data-stu-id="e23ba-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="e23ba-113">يتم عرض البلد المحدد في القائمة المنسدلة أولاً.</span><span class="sxs-lookup"><span data-stu-id="e23ba-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="e23ba-114">**كود سبب التسجيل**</span><span class="sxs-lookup"><span data-stu-id="e23ba-114">**Enrollment reason code**</span></span> | <span data-ttu-id="e23ba-115">حدد كود السبب الافتراضي المراد استخدامه عند إنشاء خطط الموظفين أثناء معالجة التسجيل المفتوح.</span><span class="sxs-lookup"><span data-stu-id="e23ba-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="e23ba-116">**كود سبب الإلغاء**</span><span class="sxs-lookup"><span data-stu-id="e23ba-116">**Cancellation reason code**</span></span> | <span data-ttu-id="e23ba-117">كود السبب المطلوب استخدامه عند إلغاء خطة فائدة موظف.</span><span class="sxs-lookup"><span data-stu-id="e23ba-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="e23ba-118">ويتم عرضه في مربع حوار أثناء عملية الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="e23ba-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="e23ba-119">يمكن للمستخدمين تغيير **كود سبب الإلغاء** إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="e23ba-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="e23ba-120">**كود سبب إعادة الفتح**</span><span class="sxs-lookup"><span data-stu-id="e23ba-120">**Reopen reason code**</span></span> | <span data-ttu-id="e23ba-121">كود السبب المطلوب استخدامه عند إعادة فتح خطة فائدة موظف.</span><span class="sxs-lookup"><span data-stu-id="e23ba-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="e23ba-122">ويتم عرضه في مربع حوار أثناء عملية الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="e23ba-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="e23ba-123">يمكن للمستخدمين تغيير **إعادة فتح كود السبب** إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="e23ba-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="e23ba-124">**رمز سبب حدث الحياة**</span><span class="sxs-lookup"><span data-stu-id="e23ba-124">**Life event reason code**</span></span> | <span data-ttu-id="e23ba-125">كود السبب المراد استخدامه عند حدوث حدث حياتي.</span><span class="sxs-lookup"><span data-stu-id="e23ba-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="e23ba-126">**رمز سبب تغيير المعدل**</span><span class="sxs-lookup"><span data-stu-id="e23ba-126">**Rate change reason code**</span></span> | <span data-ttu-id="e23ba-127">كود السبب المراد استخدامه عند إلغاء خطة ميزة خاصة بموظف وإعادة فتحها أثناء عملية تحديث تغيير المعدل.</span><span class="sxs-lookup"><span data-stu-id="e23ba-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="e23ba-128">ويشير ذلك إلى السجلات التي تم تغييرها بواسطة عملية تحديث تغيير المعدل.</span><span class="sxs-lookup"><span data-stu-id="e23ba-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="e23ba-129">**توظيف جديد مستحق**</span><span class="sxs-lookup"><span data-stu-id="e23ba-129">**New hire eligible**</span></span> | <span data-ttu-id="e23ba-130">يحدد ما إذا كان الموظفين الجدد مؤهلين أم لا.</span><span class="sxs-lookup"><span data-stu-id="e23ba-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="e23ba-131">**فترة تسجيل التوظيف الجديدة**</span><span class="sxs-lookup"><span data-stu-id="e23ba-131">**New hire enrollment period**</span></span> | <span data-ttu-id="e23ba-132">الفترة الزمنية التي يتم فيها السماح بتسجيل التوظيف الجديد.</span><span class="sxs-lookup"><span data-stu-id="e23ba-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="e23ba-133">**ملاحظة**: يتجاوز هذا الإعداد أية فترة تسجيل توظيف جديدة قمت بتعيينها في القواعد الأهلية للخطة.</span><span class="sxs-lookup"><span data-stu-id="e23ba-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="e23ba-134">**تم تمكين أحداث الحياة**</span><span class="sxs-lookup"><span data-stu-id="e23ba-134">**Life events enabled**</span></span> | <span data-ttu-id="e23ba-135">يعمل على تمكين الأحداث الحياتية.</span><span class="sxs-lookup"><span data-stu-id="e23ba-135">Enables life events.</span></span> |
   | <span data-ttu-id="e23ba-136">**إخفاء نماذج المزايا القديمة**</span><span class="sxs-lookup"><span data-stu-id="e23ba-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="e23ba-137">يسمح لك بإخفاء نماذج الميزة القديمة.</span><span class="sxs-lookup"><span data-stu-id="e23ba-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="e23ba-138">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e23ba-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="e23ba-139">تكوين محددات خدمة الموظف الذاتية</span><span class="sxs-lookup"><span data-stu-id="e23ba-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="e23ba-140">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **المحددات**.</span><span class="sxs-lookup"><span data-stu-id="e23ba-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="e23ba-141">في علامة التبويب **خدمة الموظف الذاتية**، حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="e23ba-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="e23ba-142">الحقل</span><span class="sxs-lookup"><span data-stu-id="e23ba-142">Field</span></span> | <span data-ttu-id="e23ba-143">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="e23ba-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e23ba-144">**التحقق من صحة الميزة**</span><span class="sxs-lookup"><span data-stu-id="e23ba-144">**Benefit verification**</span></span> | <span data-ttu-id="e23ba-145">نص التحقق المطلوب استخدامه أثناء سحب ميزات الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="e23ba-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="e23ba-146">**تحديد المعينين تلقائيًا**</span><span class="sxs-lookup"><span data-stu-id="e23ba-146">**Auto select designees**</span></span> | <span data-ttu-id="e23ba-147">يحدد ما إذا كان سيتم تحديد المعالين والمستفيدين تلقائيًا وفقًا لأهلية خيارات الخطة أم لا.</span><span class="sxs-lookup"><span data-stu-id="e23ba-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="e23ba-148">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e23ba-148">Select **Save**.</span></span>
