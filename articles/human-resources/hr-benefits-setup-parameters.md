---
title: تعيين محددات إدارة الميزات
description: قم بتكوين المحددات لإدارة الميزات في Microsoft Dynamics 365 Human Resources.
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
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007967"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="44e23-103">تعيين محددات إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="44e23-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="44e23-104">قبل أن تقوم بإعداد خطط الإجازات في Microsoft Dynamics 365 Human Resources، فإنه يجب عليك تكوين محددات إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="44e23-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="44e23-105">تعمل هذه المحددات على تعيين القيم الافتراضية وأكواد الأسباب والخيارات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="44e23-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="44e23-106">تكوين المحددات العامة</span><span class="sxs-lookup"><span data-stu-id="44e23-106">Configure general parameters</span></span>

1. <span data-ttu-id="44e23-107">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **المحددات**.</span><span class="sxs-lookup"><span data-stu-id="44e23-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="44e23-108">في علامة التبويب **عام** ، حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="44e23-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="44e23-109">الحقل</span><span class="sxs-lookup"><span data-stu-id="44e23-109">Field</span></span> | <span data-ttu-id="44e23-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="44e23-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="44e23-111">**البلد/المنطقة**</span><span class="sxs-lookup"><span data-stu-id="44e23-111">**Country/region**</span></span> | <span data-ttu-id="44e23-112">يحدد الحقل **البلد/المنطقة** ترتيب العرض الأكواد البريدية/الولايات .</span><span class="sxs-lookup"><span data-stu-id="44e23-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="44e23-113">يتم عرض البلد المحدد في القائمة المنسدلة أولاً.</span><span class="sxs-lookup"><span data-stu-id="44e23-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="44e23-114">**كود سبب التسجيل**</span><span class="sxs-lookup"><span data-stu-id="44e23-114">**Enrollment reason code**</span></span> | <span data-ttu-id="44e23-115">حدد كود السبب الافتراضي المراد استخدامه عند إنشاء خطط الموظفين أثناء معالجة التسجيل المفتوح.</span><span class="sxs-lookup"><span data-stu-id="44e23-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="44e23-116">**كود سبب الإلغاء**</span><span class="sxs-lookup"><span data-stu-id="44e23-116">**Cancellation reason code**</span></span> | <span data-ttu-id="44e23-117">كود السبب المطلوب استخدامه عند إلغاء خطة فائدة موظف.</span><span class="sxs-lookup"><span data-stu-id="44e23-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="44e23-118">ويتم عرضه في مربع حوار أثناء عملية الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="44e23-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="44e23-119">يمكن للمستخدمين تغيير **كود سبب الإلغاء** إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="44e23-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="44e23-120">**كود سبب إعادة الفتح**</span><span class="sxs-lookup"><span data-stu-id="44e23-120">**Reopen reason code**</span></span> | <span data-ttu-id="44e23-121">كود السبب المطلوب استخدامه عند إعادة فتح خطة فائدة موظف.</span><span class="sxs-lookup"><span data-stu-id="44e23-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="44e23-122">ويتم عرضه في مربع حوار أثناء عملية الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="44e23-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="44e23-123">يمكن للمستخدمين تغيير **إعادة فتح كود السبب** إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="44e23-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="44e23-124">**رمز سبب حدث الحياة**</span><span class="sxs-lookup"><span data-stu-id="44e23-124">**Life event reason code**</span></span> | <span data-ttu-id="44e23-125">كود السبب المراد استخدامه عند حدوث حدث حياتي.</span><span class="sxs-lookup"><span data-stu-id="44e23-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="44e23-126">**رمز سبب تغيير المعدل**</span><span class="sxs-lookup"><span data-stu-id="44e23-126">**Rate change reason code**</span></span> | <span data-ttu-id="44e23-127">كود السبب المراد استخدامه عند إلغاء خطة ميزة خاصة بموظف وإعادة فتحها أثناء عملية تحديث تغيير المعدل.</span><span class="sxs-lookup"><span data-stu-id="44e23-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="44e23-128">ويشير ذلك إلى السجلات التي تم تغييرها بواسطة عملية تحديث تغيير المعدل.</span><span class="sxs-lookup"><span data-stu-id="44e23-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="44e23-129">**توظيف جديد مستحق**</span><span class="sxs-lookup"><span data-stu-id="44e23-129">**New hire eligible**</span></span> | <span data-ttu-id="44e23-130">يحدد ما إذا كان الموظفين الجدد مؤهلين أم لا.</span><span class="sxs-lookup"><span data-stu-id="44e23-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="44e23-131">**فترة تسجيل التوظيف الجديدة**</span><span class="sxs-lookup"><span data-stu-id="44e23-131">**New hire enrollment period**</span></span> | <span data-ttu-id="44e23-132">الفترة الزمنية التي يتم فيها السماح بتسجيل التوظيف الجديد.</span><span class="sxs-lookup"><span data-stu-id="44e23-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="44e23-133">**ملاحظة**: يتجاوز هذا الإعداد أية فترة تسجيل توظيف جديدة قمت بتعيينها في القواعد الأهلية للخطة.</span><span class="sxs-lookup"><span data-stu-id="44e23-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="44e23-134">**تحسين الراتب السنوي**</span><span class="sxs-lookup"><span data-stu-id="44e23-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="44e23-135">يحدد ما إذا كان سيتم حساب مبلغ **راتب الفائدة السنوية** تلقائيًا في **تفاصيل ميزة التوظيف** أم لا.</span><span class="sxs-lookup"><span data-stu-id="44e23-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="44e23-136">إنه يستند إلى **معدل الدفع الثابت** للموظف و**متوسط الساعات** و**تكرار الدفع**.</span><span class="sxs-lookup"><span data-stu-id="44e23-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="44e23-137">**متوسط الساعات** x **معدل الدفع الثابت** x **تكرار الدفع** (عدد فترات الدفع) = **راتب الفائدة السنوية**</span><span class="sxs-lookup"><span data-stu-id="44e23-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="44e23-138">في حالة تغيير أي من القيم في الحقول **متوسط الساعات** أو **معدل دفع تعويض ثابت** أو **تكرار الدفع**، يقوم النظام تلقائيًا بإعادة حساب **راتب الفائدة السنوية** للموظف بناءً على القيم المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="44e23-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="44e23-139">يقوم النظام بإنشاء سجل **تاريخ السريان** لتعريف نفس التاريخ والوقت الذي حدث فيه التغيير.</span><span class="sxs-lookup"><span data-stu-id="44e23-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="44e23-140">يمكنك تحرير مبلغ **راتب الفائدة السنوي** إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="44e23-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="44e23-141">**تم تمكين أحداث الحياة**</span><span class="sxs-lookup"><span data-stu-id="44e23-141">**Life events enabled**</span></span> | <span data-ttu-id="44e23-142">يعمل على تمكين الأحداث الحياتية.</span><span class="sxs-lookup"><span data-stu-id="44e23-142">Enables life events.</span></span> |
   | <span data-ttu-id="44e23-143">**إخفاء نماذج المزايا القديمة**</span><span class="sxs-lookup"><span data-stu-id="44e23-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="44e23-144">يسمح لك بإخفاء نماذج الميزة القديمة.</span><span class="sxs-lookup"><span data-stu-id="44e23-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="44e23-145">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="44e23-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="44e23-146">تكوين محددات خدمة الموظف الذاتية</span><span class="sxs-lookup"><span data-stu-id="44e23-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="44e23-147">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **المحددات**.</span><span class="sxs-lookup"><span data-stu-id="44e23-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="44e23-148">في علامة التبويب **خدمة الموظف الذاتية**، حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="44e23-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="44e23-149">الحقل</span><span class="sxs-lookup"><span data-stu-id="44e23-149">Field</span></span> | <span data-ttu-id="44e23-150">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="44e23-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="44e23-151">**التحقق من صحة الميزة**</span><span class="sxs-lookup"><span data-stu-id="44e23-151">**Benefit verification**</span></span> | <span data-ttu-id="44e23-152">نص التحقق المطلوب استخدامه أثناء سحب ميزات الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="44e23-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="44e23-153">**تحديد المعينين تلقائيًا**</span><span class="sxs-lookup"><span data-stu-id="44e23-153">**Auto select designees**</span></span> | <span data-ttu-id="44e23-154">يحدد ما إذا كان سيتم تحديد المعالين والمستفيدين تلقائيًا وفقًا لأهلية خيارات الخطة أم لا.</span><span class="sxs-lookup"><span data-stu-id="44e23-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="44e23-155">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="44e23-155">Select **Save**.</span></span>
