---
title: إنشاء أنواع الخطة
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: c12eecb38bd943a9c604f878644da289783d3f74
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007966"
---
# <a name="create-plan-types"></a><span data-ttu-id="3ef89-102">إنشاء أنواع الخطة</span><span class="sxs-lookup"><span data-stu-id="3ef89-102">Create plan types</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="3ef89-103">يُعد نوع الخطة في Microsoft Dynamics 365 Human Resources تجميعًا عالي المستوى لأنواع معينة من الميزات.</span><span class="sxs-lookup"><span data-stu-id="3ef89-103">A plan type in Microsoft Dynamics 365 Human Resources is a high-level grouping of specific types of benefits.</span></span> <span data-ttu-id="3ef89-104">ويكون لكل نوع خطة كود نوع خطة يحدد القواعد الخاصة بنوع الخطة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-104">Each plan type has a plan type code that determines rules for the plan type.</span></span> <span data-ttu-id="3ef89-105">على سبيل المثال، قد يكون للحياة الأساسية لنوع الخطة حياة كود نوع الخطة لأنه نوع من خطة التأمين على الحياة ويجب أن تتطابق مع القواعد المنشورة لكود نوع خطة الحياة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-105">For example, the plan type Basic life would have the plan type code Life because it’s a kind of life insurance plan and must conform to rules established for the Life plan type code.</span></span> <span data-ttu-id="3ef89-106">قد يكون نوع خطة آخر حياة تكميلية، وتحتوي كذلك على حياة كود نوع الخطة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-106">Another plan type might be Supplemental life, also with plan type code Life.</span></span>

<span data-ttu-id="3ef89-107">ويشير كل نوع خطة إلى ما إذا كان الموظف يمكنه التسجيل في نوع خطة واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="3ef89-107">Each plan type indicates whether an employee can enroll in one plan of its type or multiple.</span></span> <span data-ttu-id="3ef89-108">على سبيل المثال، من المحتمل أن يكون الموظف قادرًا على التسجيل في كلا سياستي الحياة الأساسية والحياة التكميلية لحياة نوع الخطة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-108">For example, an employee would likely be able to enroll in both the Basic life and the Supplemental life policies of plan type Life.</span></span> <span data-ttu-id="3ef89-109">من المحتمل أن يتم السماح للموظف بالتسجيل في سياسة واحدة فقط من النوع "طبي".</span><span class="sxs-lookup"><span data-stu-id="3ef89-109">An employee would likely be allowed to enroll in only one policy of type Medical.</span></span>

<span data-ttu-id="3ef89-110">إذا كان نوع الخطة يتضمن جهات اتصال، يشير نوع الخطة إلى ما إذا كانت جهات الاتصال مستفيدين أم معالين.</span><span class="sxs-lookup"><span data-stu-id="3ef89-110">If a plan type involves contacts, the plan type indicates whether contacts are beneficiaries or dependents.</span></span> <span data-ttu-id="3ef89-111">على سبيل المثال، قد يحتوي نوع خطة الحياة الأساسية على مستفيدين، بينما يحتوي نوع الخطة الطبية الأساسية على معالين.</span><span class="sxs-lookup"><span data-stu-id="3ef89-111">For example, a Basic life plan type would have beneficiaries, while a Basic medical plan type would have dependents.</span></span> <span data-ttu-id="3ef89-112">في بعض الحالات، قد لا تتضمن الخطة أية جهات اتصال شخصية.</span><span class="sxs-lookup"><span data-stu-id="3ef89-112">In some cases, a plan may not have any personal contacts.</span></span> <span data-ttu-id="3ef89-113">على سبيل المثال، حساب الانفاق المرن أو بدل الانتظار.</span><span class="sxs-lookup"><span data-stu-id="3ef89-113">For example, a Flexible Spending Account or Parking allowance.</span></span>

<span data-ttu-id="3ef89-114">قد يحدد نوع الخطة خيارات التغطية.</span><span class="sxs-lookup"><span data-stu-id="3ef89-114">A plan type may define coverage options.</span></span> <span data-ttu-id="3ef89-115">يتم تحديد خيارات التغطية في نموذج خيار التغطية.</span><span class="sxs-lookup"><span data-stu-id="3ef89-115">The coverage options are defined in the Coverage option form.</span></span> <span data-ttu-id="3ef89-116">يمكن لخيار التغطية تحديد مقدار الميزة أو جهات الاتصال المؤهلة لنوع الخطة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-116">A coverage option can specify the amount of the benefit or the contacts who are eligible for the plan type.</span></span> <span data-ttu-id="3ef89-117">على سبيل المثال، إذا كان نوع جهة الاتصال مستفيد، فيجب أن يحدد خيار التغطية الشروط الخاصة بما يستحق المستفيد الحصول عليه عند استخدام الميزة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-117">For example, if the contact type is Beneficiary, the coverage option should define the terms of what the beneficiary is eligible to receive when the benefit is utilized.</span></span> <span data-ttu-id="3ef89-118">إذا كان نوع جهة الاتصال معال، فإن خيار التغطية يجب أ ن يحدد العلاقة بين المعال والموظف.</span><span class="sxs-lookup"><span data-stu-id="3ef89-118">If the contact type is Dependent, the coverage option should define the relationship between the dependent and employee.</span></span> 

1. <span data-ttu-id="3ef89-119">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **أنواع الخطط**.</span><span class="sxs-lookup"><span data-stu-id="3ef89-119">In the **Benefits management** workspace, under **Setup**, select **Plan types**.</span></span>

2. <span data-ttu-id="3ef89-120">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="3ef89-120">Select **New**.</span></span>

3. <span data-ttu-id="3ef89-121">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="3ef89-121">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3ef89-122">الحقل</span><span class="sxs-lookup"><span data-stu-id="3ef89-122">Field</span></span> | <span data-ttu-id="3ef89-123">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="3ef89-123">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3ef89-124">نوع الخطة</span><span class="sxs-lookup"><span data-stu-id="3ef89-124">Plan type</span></span> | <span data-ttu-id="3ef89-125">اسم فريد يحدد نوع الخطة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-125">A unique name that identifies the plan type.</span></span> |
   | <span data-ttu-id="3ef89-126">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="3ef89-126">Description</span></span> | <span data-ttu-id="3ef89-127">وصف نوع الخطة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-127">A description of the plan type.</span></span> |
   | <span data-ttu-id="3ef89-128">كود نوع الخطة</span><span class="sxs-lookup"><span data-stu-id="3ef89-128">Plant type code</span></span> | <span data-ttu-id="3ef89-129">حدد كود نوع الخطة من قائمة القيم المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-129">Select a plan type code from the drop down list of values.</span></span> <span data-ttu-id="3ef89-130">تعرض قائمة كود نوع الخطة كافة أنواع الخطط التي يتم دعمها في الإصدار الحالي.</span><span class="sxs-lookup"><span data-stu-id="3ef89-130">The plan type code list displays all the plan types that are supported in the current version.</span></span> |
   | <span data-ttu-id="3ef89-131">التسجيل المتزامن</span><span class="sxs-lookup"><span data-stu-id="3ef89-131">Concurrent enrollment</span></span> | <span data-ttu-id="3ef89-132">يحدد ما إذا كان بإمكان الموظف التسجيل في خطط الميزات المتعددة لنوع الخطة نفسه أم خطة ميزة واحدة فقط لكل نوع خطة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-132">Specifies whether an employee can enroll in multiple benefit plans of the same plan type or only one benefit plan per plan type.</span></span> |
   | <span data-ttu-id="3ef89-133">نوع الاتصال</span><span class="sxs-lookup"><span data-stu-id="3ef89-133">Contact type</span></span> | <span data-ttu-id="3ef89-134">يحدد دور جهة الاتصال الشخصية.</span><span class="sxs-lookup"><span data-stu-id="3ef89-134">Specifies the role of the personal contact.</span></span> <span data-ttu-id="3ef89-135">تكون القيم فارغ ومعال ومستفيد.</span><span class="sxs-lookup"><span data-stu-id="3ef89-135">The values are blank, Dependent, and Beneficiary.</span></span> <span data-ttu-id="3ef89-136">يمكنك ترك نوع الاتصال فارغًا إذا كان نوع الخطة لا يتطلب معال أو مستفيد بناءً على خيار التغطية.</span><span class="sxs-lookup"><span data-stu-id="3ef89-136">You can leave Contact type blank if their plan type does not require a dependent or beneficiary based on the coverage option.</span></span> |

4. <span data-ttu-id="3ef89-137">لتكوين خيارات الحدث الحياتي، حدد **الإجراءات**، ثم حدد **خيارات الحدث الحياتي**.</span><span class="sxs-lookup"><span data-stu-id="3ef89-137">To configure life event options, select **Actions**, and then select **Life event options**.</span></span> <span data-ttu-id="3ef89-138">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="3ef89-138">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3ef89-139">الحقل</span><span class="sxs-lookup"><span data-stu-id="3ef89-139">Field</span></span> | <span data-ttu-id="3ef89-140">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="3ef89-140">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3ef89-141">نوع الخطة</span><span class="sxs-lookup"><span data-stu-id="3ef89-141">Plan type</span></span> | <span data-ttu-id="3ef89-142">نوع الخطة المراد تكوين خيارات الحدث الحياتي به.</span><span class="sxs-lookup"><span data-stu-id="3ef89-142">The plan type to configure life event options for.</span></span> |
   | <span data-ttu-id="3ef89-143">معرف نوع الحدث الحياتي</span><span class="sxs-lookup"><span data-stu-id="3ef89-143">Life event type id</span></span> | <span data-ttu-id="3ef89-144">معرف نوع الحدث الحياتي.</span><span class="sxs-lookup"><span data-stu-id="3ef89-144">The ID of the life event type.</span></span> |
   | <span data-ttu-id="3ef89-145">السماح بالإلغاء</span><span class="sxs-lookup"><span data-stu-id="3ef89-145">Allow cancellation</span></span> | <span data-ttu-id="3ef89-146">يحدد ما إذا كان بإمكان الموظف إلغاء خطة ميزات أثناء الحدث الحياتي أم لا.</span><span class="sxs-lookup"><span data-stu-id="3ef89-146">Specifies whether an employee can cancel a benefits plan during the life event.</span></span> |
   |<span data-ttu-id="3ef89-147">تغيير خيار التغطية</span><span class="sxs-lookup"><span data-stu-id="3ef89-147">Change coverage option</span></span> | <span data-ttu-id="3ef89-148">يحدد ما إذا كان بإمكان الموظف تغيير خيارات التغطية أثناء الحدث الحياتي أم لا.</span><span class="sxs-lookup"><span data-stu-id="3ef89-148">Specifies whether an employee can change coverage options during the life event.</span></span> |
   | <span data-ttu-id="3ef89-149">التغيير إلى خطة جديدة</span><span class="sxs-lookup"><span data-stu-id="3ef89-149">Change to a new plan</span></span> | <span data-ttu-id="3ef89-150">يحدد ما إذا كان بإمكان الموظف تغيير الخطط أثناء الحدث الحياتي أم لا.</span><span class="sxs-lookup"><span data-stu-id="3ef89-150">Specifies whether an employee can change plans during the life event.</span></span> |
   | <span data-ttu-id="3ef89-151">الإلغاء التلقائي للخطة</span><span class="sxs-lookup"><span data-stu-id="3ef89-151">Auto cancel plan</span></span> |<span data-ttu-id="3ef89-152">يحدد ما إذا كان سيتم إلغاء الخطة تلقائيًا اثناء الحدث الحياتي أم لا.</span><span class="sxs-lookup"><span data-stu-id="3ef89-152">Specifies whether to automatically cancel the plan during the life event.</span></span> |
   | <span data-ttu-id="3ef89-153">إعادة الفتح التلقائي لفحص الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="3ef89-153">Auto reopen eligibility check</span></span> | <span data-ttu-id="3ef89-154">لتحديد ما إذا كان ستتم تلقائيًا إعادة فتح فحص استحقاق تسجيل المزايا أثناء حدث الحياة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-154">Specifies whether to automatically reopen the benefits enrollment eligibility check during the life event.</span></span> |
   | <span data-ttu-id="3ef89-155">نافذة التقارير</span><span class="sxs-lookup"><span data-stu-id="3ef89-155">Reporting window</span></span> | <span data-ttu-id="3ef89-156">لتحديد إطار التقارير بالأيام لحدث الحياة.</span><span class="sxs-lookup"><span data-stu-id="3ef89-156">Specifies the reporting window, in days, of the life event.</span></span> <span data-ttu-id="3ef89-157">**ملاحظة**: إذا لم تقم بإدخال مبلغ، سيفترض النظام أن نافذة الإبلاغ صفرًا ولن يعالج الحدث الحياتي.</span><span class="sxs-lookup"><span data-stu-id="3ef89-157">**Note**: If you don't enter an amount, the system assumes the reporting window to be zero and won't process the life event.</span></span> |

5. <span data-ttu-id="3ef89-158">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3ef89-158">Select **Save**.</span></span> 
