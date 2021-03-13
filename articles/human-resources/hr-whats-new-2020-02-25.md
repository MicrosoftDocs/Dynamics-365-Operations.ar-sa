---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (25 فبراير 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 25 فبراير 2020.
author: andreabichsel
manager: tfehr
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4faecb83518f3ef8af825872abc2a6ffb94162fc
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128008"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="115d9-103">ما الجديد أو المتغير في Dynamics 365 Human Resources (25 فبراير 2020)</span><span class="sxs-lookup"><span data-stu-id="115d9-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="115d9-104">تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="115d9-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="115d9-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.2927.</span><span class="sxs-lookup"><span data-stu-id="115d9-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="115d9-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.</span><span class="sxs-lookup"><span data-stu-id="115d9-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="115d9-107">تمكين التنقل في إدارة الحالات‬ وكيان إطار عمل إدارة البيانات (DMF) ‏(414754)</span><span class="sxs-lookup"><span data-stu-id="115d9-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="115d9-108">تقوم ميزة المعاينة هذه بتمكين التنقل الإضافي إلى حالات إدارة الحالات.</span><span class="sxs-lookup"><span data-stu-id="115d9-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="115d9-109">يمكنك تمكين ميزة المعاينة هذه في مساحة عمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="115d9-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="115d9-110">تظهر عناصر القائمة هذه في مساحة عمل **التوافق** Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="115d9-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="115d9-111">ومع هذا التغيير، بإمكان Human Resources الوصول إلى:</span><span class="sxs-lookup"><span data-stu-id="115d9-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="115d9-112">كل الحالات</span><span class="sxs-lookup"><span data-stu-id="115d9-112">All cases</span></span>
- <span data-ttu-id="115d9-113">الحالات الخاصة بي</span><span class="sxs-lookup"><span data-stu-id="115d9-113">My cases</span></span>
- <span data-ttu-id="115d9-114">الحالات المفتوحة  </span><span class="sxs-lookup"><span data-stu-id="115d9-114">My open cases</span></span>
- <span data-ttu-id="115d9-115">حالات التأخر</span><span class="sxs-lookup"><span data-stu-id="115d9-115">My overdue cases</span></span>
- <span data-ttu-id="115d9-116">الحالات المعيَّنة لي خلال سير العمل</span><span class="sxs-lookup"><span data-stu-id="115d9-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="115d9-117">إلى جانب طرق العرض الجديدة هذه، يتوفر أيضًا كيان DMF **تفاصيل الحالة**</span><span class="sxs-lookup"><span data-stu-id="115d9-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="115d9-118">تمكين تعريفات العلاقة في دفتر العناوين العمومي (414762)</span><span class="sxs-lookup"><span data-stu-id="115d9-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="115d9-119">تم الآن تمكين العلاقات في دفتر العناوين العمومي.</span><span class="sxs-lookup"><span data-stu-id="115d9-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="115d9-120">قبل إصدار هذا الأسبوع، عرض مربع الحقائق **العلاقة** أي علاقات معرفة من قبل النظام.</span><span class="sxs-lookup"><span data-stu-id="115d9-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="115d9-121">يمكنك الآن تعريف هذه العلاقات داخل صفحة دفتر العناوين العمومي.</span><span class="sxs-lookup"><span data-stu-id="115d9-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="115d9-122">يمكن إزالة منصب عند وجود سجلات تعويضات نشطة للمنصب (414568)</span><span class="sxs-lookup"><span data-stu-id="115d9-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="115d9-123">مع هذا التغيير، يظهر تحذير عندما تحاول حذف منصب وهناك سجل تعويض نشط لدى العامل لهذا المنصب نفسه.</span><span class="sxs-lookup"><span data-stu-id="115d9-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="115d9-124">وعند حدوث ذلك، يجب تحديث سجل التعويض الثابت للموظف قبل إزالة المنصب.</span><span class="sxs-lookup"><span data-stu-id="115d9-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="115d9-125">يقوم سير عمل مراجعة الأداء في بعض الأحيان بإضافة عمليات الاعتماد من أشخاص لا يشكلون جزءًا من العملية (414171)</span><span class="sxs-lookup"><span data-stu-id="115d9-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="115d9-126">يعمل هذا التغيير على تصحيح مشكلة حيث تتم فيها إضافة مشاركين إضافيين إلى عمليات الاعتماد إلى مراجعة الأداء.</span><span class="sxs-lookup"><span data-stu-id="115d9-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="115d9-127">لم يتم إنشاء تعيين منصب العامل في Dataverse عند تحديده في مربع الحوار "عامل جديد" (413479)</span><span class="sxs-lookup"><span data-stu-id="115d9-127">Worker position assignment not created in Dataverse when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="115d9-128">يعمل هذا التغيير على تصحيح مشكل عند توظيف عامل جديد وتعيين الموظف الجديد إلى منصب في مربع حوار **عامل جديد**.</span><span class="sxs-lookup"><span data-stu-id="115d9-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="115d9-129">يظهر الآن تعيين المنصب في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="115d9-129">Now the position assignment is reflected in Dataverse.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="115d9-130">قريبًا</span><span class="sxs-lookup"><span data-stu-id="115d9-130">Coming soon</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="115d9-131">حل Dataverse المحدث</span><span class="sxs-lookup"><span data-stu-id="115d9-131">Updated Dataverse solution</span></span>

<span data-ttu-id="115d9-132">سيتوفر حل Dataverse قريبًا بالتغييرات التالية:</span><span class="sxs-lookup"><span data-stu-id="115d9-132">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="115d9-133">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="115d9-133">Description</span></span> | <span data-ttu-id="115d9-134">التغيير</span><span class="sxs-lookup"><span data-stu-id="115d9-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="115d9-135">تغييرات كيان **الوظيفة/المنصب**</span><span class="sxs-lookup"><span data-stu-id="115d9-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="115d9-136">تم إضافة **منطقة التعويض**</span><span class="sxs-lookup"><span data-stu-id="115d9-136">**Compensation region** added</span></span></br><span data-ttu-id="115d9-137">تمت إضافة **الأبعاد المالية**</span><span class="sxs-lookup"><span data-stu-id="115d9-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="115d9-138">تغييرات كيان **العامل**</span><span class="sxs-lookup"><span data-stu-id="115d9-138">**Worker** entity changes</span></span> | <span data-ttu-id="115d9-139">تمت إضافة **تسلسل الاسم**</span><span class="sxs-lookup"><span data-stu-id="115d9-139">**Name sequence** added</span></span></br><span data-ttu-id="115d9-140">تم إضافة **الأعمال من الصفحة الرئيسية**</span><span class="sxs-lookup"><span data-stu-id="115d9-140">**Works from home** added</span></span></br><span data-ttu-id="115d9-141">تمت إضافة **اللغة**</span><span class="sxs-lookup"><span data-stu-id="115d9-141">**Language** added</span></span></br><span data-ttu-id="115d9-142">تمت إضافة **تاريخ الأقدمية**</span><span class="sxs-lookup"><span data-stu-id="115d9-142">**Seniority date** added</span></span></br><span data-ttu-id="115d9-143">تمت إضاف **تاريخ التفعيل السنوي**</span><span class="sxs-lookup"><span data-stu-id="115d9-143">**Anniversary date** added</span></span></br><span data-ttu-id="115d9-144">تمت إضافة **تاريخ التوظيف الأصلي**</span><span class="sxs-lookup"><span data-stu-id="115d9-144">**Original hire date** added</span></span> |
| <span data-ttu-id="115d9-145">تغييرات كيان **التوظيف**</span><span class="sxs-lookup"><span data-stu-id="115d9-145">**Employment** entity changes</span></span> | <span data-ttu-id="115d9-146">تمت إضافة **الأبعاد المالية**</span><span class="sxs-lookup"><span data-stu-id="115d9-146">**Financial dimensions** added</span></span></br><span data-ttu-id="115d9-147">تمت إضافة **سبب الإنهاء**</span><span class="sxs-lookup"><span data-stu-id="115d9-147">**Termination reason** added</span></span></br><span data-ttu-id="115d9-148">تمت إعادة تسمية **تاريخ الإنهاء** من **تاريخ الانتقال**</span><span class="sxs-lookup"><span data-stu-id="115d9-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="115d9-149">تمت إضافة **تاريخ فترة الاختبار**</span><span class="sxs-lookup"><span data-stu-id="115d9-149">**Probation date** added</span></span> |
| <span data-ttu-id="115d9-150">تغييرات كيان **عنوان العامل**</span><span class="sxs-lookup"><span data-stu-id="115d9-150">**Worker address** entity changes</span></span> | <span data-ttu-id="115d9-151">تمت إضافة **عنوان الشارع**</span><span class="sxs-lookup"><span data-stu-id="115d9-151">**Street address** added</span></span></br><span data-ttu-id="115d9-152">**سطر العنوان 1**، و **سطر العنوان 2**، و **سطر العنوان 3** المميز للإهلاك</span><span class="sxs-lookup"><span data-stu-id="115d9-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="115d9-153">كيانات إعداد التعويض المتغيرة الجديدة</span><span class="sxs-lookup"><span data-stu-id="115d9-153">New variable compensation setup entities</span></span> | <span data-ttu-id="115d9-154">**نوع خطة التعويض المتغير**</span><span class="sxs-lookup"><span data-stu-id="115d9-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="115d9-155">**خطة التعويض المتغيرة**</span><span class="sxs-lookup"><span data-stu-id="115d9-155">**Compensation variable plan**</span></span></br><span data-ttu-id="115d9-156">**قواعد الاستحقاق**</span><span class="sxs-lookup"><span data-stu-id="115d9-156">**Vesting rules**</span></span></br><span data-ttu-id="115d9-157">**مستوى خطة التعويض المتغير**</span><span class="sxs-lookup"><span data-stu-id="115d9-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="115d9-158">كيان **توظيف تقويم العامل** الجديد</span><span class="sxs-lookup"><span data-stu-id="115d9-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="115d9-159">تمت إضافة **كيان تقويم العمل**</span><span class="sxs-lookup"><span data-stu-id="115d9-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="115d9-160">كيان **تفاصيل المنصب في كشف الرواتب** الجديد</span><span class="sxs-lookup"><span data-stu-id="115d9-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="115d9-161">تمت إضافة **تفاصيل المنصب في كشف الرواتب**</span><span class="sxs-lookup"><span data-stu-id="115d9-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="115d9-162">كيان **العنوان** الجديد</span><span class="sxs-lookup"><span data-stu-id="115d9-162">New **Title** entity</span></span> | <span data-ttu-id="115d9-163">تمت إضافة **العنوان**.</span><span class="sxs-lookup"><span data-stu-id="115d9-163">**Title** added.</span></span> <span data-ttu-id="115d9-164">سيتم تضمين كيان **العنوان** الجديد في عملية المزامنة بين Human Resources وDataverse.</span><span class="sxs-lookup"><span data-stu-id="115d9-164">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="115d9-165">ولن تتم الإشارة إليه من كيانات **منصب الوظيفة** أو **الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="115d9-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="115d9-166">خلال الأسابيع القليلة التالية، ستتوفر هذه التغييرات الخاصة بالكيانات في كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="115d9-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="115d9-167">لتثبيت حل Dataverse الأحدث لـ Human Resources:</span><span class="sxs-lookup"><span data-stu-id="115d9-167">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="115d9-168">انتقل إلى [مركز إدارة Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="115d9-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="115d9-169">حدد **بيئات**.</span><span class="sxs-lookup"><span data-stu-id="115d9-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="115d9-170">ابحث عن البيئة التي تريد ترقيتها.</span><span class="sxs-lookup"><span data-stu-id="115d9-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="115d9-171">يجب أن تتطابق مع **اسم البيئة** في قسم **Common Data Service المعلومات** في النموذج **حول** في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="115d9-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="115d9-172">حدد البيئة لعرض تفاصيل البيئة.</span><span class="sxs-lookup"><span data-stu-id="115d9-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="115d9-173">حدد **إدارة الحلول** في شريط الإجراءات في الجزء العلوي.</span><span class="sxs-lookup"><span data-stu-id="115d9-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="115d9-174">ستفتح نافذة مستعرض جديدة وتنتقل إلى **مركز إدارة Dynamics 365** في سياق بيئتك.</span><span class="sxs-lookup"><span data-stu-id="115d9-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="115d9-175">في قائمة **الحل**، حدد **ارتساء Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="115d9-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="115d9-176">حدد **ترقية** لتطبيق الحل الأخير.</span><span class="sxs-lookup"><span data-stu-id="115d9-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="115d9-177">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="115d9-177">In preview</span></span>

<span data-ttu-id="115d9-178">أصبحت ميزات المعاينة التالية متوفرة في 3 فبراير 2020:</span><span class="sxs-lookup"><span data-stu-id="115d9-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="115d9-179">**ميزات معاينة الغياب والإجازات** - لمزيد من المعلومات، راجع [ميزات معاينة الإجازات والغياب](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="115d9-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="115d9-180">**ميزة معاينة إدارة الميزات** - لمزيد من المعلومات، بما في ذلك المشكلات المعروفة، راجع [نظرة عامة على إدارة الميزات](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="115d9-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="115d9-181">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="115d9-181">See also</span></span>

[<span data-ttu-id="115d9-182">المزايا الجديدة أو المتغيرة في Human Resources</span><span class="sxs-lookup"><span data-stu-id="115d9-182">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="115d9-183">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="115d9-183">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="115d9-184">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="115d9-184">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="115d9-185">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="115d9-185">Manage features</span></span>](hr-admin-manage-features.md)