---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (18 فبراير 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 18 فبراير 2020.
author: andreabichsel
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6c28d0dc76195cc0aedc132f348a229af0421c43
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790418"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="e932a-103">ما الجديد أو المتغير في Dynamics 365 Human Resources (18 فبراير 2020)</span><span class="sxs-lookup"><span data-stu-id="e932a-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e932a-104">تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e932a-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e932a-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.2903.</span><span class="sxs-lookup"><span data-stu-id="e932a-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="e932a-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.</span><span class="sxs-lookup"><span data-stu-id="e932a-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="e932a-107">update 32 للنظام الأساسي</span><span class="sxs-lookup"><span data-stu-id="e932a-107">Platform update 32</span></span> 

<span data-ttu-id="e932a-108">التحديث الخاص بالنظام الأساسي 32 متوفر الآن.</span><span class="sxs-lookup"><span data-stu-id="e932a-108">Platform update 32 is now available.</span></span> <span data-ttu-id="e932a-109">لمزيد من المعلومات، راجع [المزايا الجديدة أو المتغيرة في تحديث النظام الأساسي 32 لتطبيقات Finance and Operations (فبراير 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span><span class="sxs-lookup"><span data-stu-id="e932a-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="e932a-110">يتم تذكر قيم البحث عند تغيير خيارات العرض في نموذج موظف المبسط (383833)</span><span class="sxs-lookup"><span data-stu-id="e932a-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="e932a-111">يحتفظ الآن نموذج **العامل** بقيم البحث عند تغيير خيارات العرض وتطبيق التغييرات.</span><span class="sxs-lookup"><span data-stu-id="e932a-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="e932a-112">إطارات ملخص إدارة التعويض في إعادة توجيه ميزة المعاينة إلى نموذج خاطئ (401861)</span><span class="sxs-lookup"><span data-stu-id="e932a-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="e932a-113">تعرض الآن تجانبات إدارة التعويض الثابتة والمتغيرة السجلات الصحيحة في نموذج **العامل** الجديد.</span><span class="sxs-lookup"><span data-stu-id="e932a-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="e932a-114">ينطبق فقط على ميزة معاينة نموذج الموظف المبسط.</span><span class="sxs-lookup"><span data-stu-id="e932a-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="e932a-115">يمكنك تمكين ميزة المعاينة هذه في **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="e932a-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="e932a-116">لمزيد من المعلومات، راجع [إدارة الميزات](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="e932a-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a><span data-ttu-id="e932a-117">حقل الحالة فارغ لبعض سجلات طلب الإجازة في Dataverse (414915)</span><span class="sxs-lookup"><span data-stu-id="e932a-117">Empty Status field for some leave request records in Dataverse (414915)</span></span>

<span data-ttu-id="e932a-118">يعمل هذا التغيير على تصحيح مشكلة في Dataverse عندما يتم تعيين حقل **الحالة** في طلب إجازة إلى **المراجعة**.</span><span class="sxs-lookup"><span data-stu-id="e932a-118">This change corrects an issue in Dataverse when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="e932a-119">Dataverse يعكس الآن الحالة.</span><span class="sxs-lookup"><span data-stu-id="e932a-119">Dataverse now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="e932a-120">يكون تحليل فروق المهارات ممكنًا للوظيفة المعينة (411390) فقط</span><span class="sxs-lookup"><span data-stu-id="e932a-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="e932a-121">يمكنك الآن القيام بتحليل فروق المهارات في أي وظيفة محددة في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e932a-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="e932a-122">لا تتم مزامنة عملة النظام من Dataverse إلى Human Resources في البيئات الجديدة (418011)</span><span class="sxs-lookup"><span data-stu-id="e932a-122">System currency doesn't sync from Dataverse to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="e932a-123">الآن، يمكن أن تتزامن عملة النظام في Dataverse إلى Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e932a-123">The system currency in Dataverse can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="e932a-124">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="e932a-124">In preview</span></span>

- [<span data-ttu-id="e932a-125">ميزات مُعاينة الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="e932a-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="e932a-126">ميزة معاينة إدارة المزايا</span><span class="sxs-lookup"><span data-stu-id="e932a-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="e932a-127">قريبًا</span><span class="sxs-lookup"><span data-stu-id="e932a-127">Coming soon</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="e932a-128">حل Dataverse المحدث</span><span class="sxs-lookup"><span data-stu-id="e932a-128">Updated Dataverse solution</span></span>

<span data-ttu-id="e932a-129">سيتوفر حل Dataverse قريبًا بالتغييرات التالية:</span><span class="sxs-lookup"><span data-stu-id="e932a-129">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="e932a-130">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="e932a-130">Description</span></span> | <span data-ttu-id="e932a-131">التغيير</span><span class="sxs-lookup"><span data-stu-id="e932a-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="e932a-132">تغييرات كيان **الوظيفة/المنصب**</span><span class="sxs-lookup"><span data-stu-id="e932a-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="e932a-133">تم إضافة **منطقة التعويض**</span><span class="sxs-lookup"><span data-stu-id="e932a-133">**Compensation region** added</span></span></br><span data-ttu-id="e932a-134">تمت إضافة **الأبعاد المالية**</span><span class="sxs-lookup"><span data-stu-id="e932a-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="e932a-135">تغييرات كيان **العامل**</span><span class="sxs-lookup"><span data-stu-id="e932a-135">**Worker** entity changes</span></span> | <span data-ttu-id="e932a-136">تمت إضافة **تسلسل الاسم**</span><span class="sxs-lookup"><span data-stu-id="e932a-136">**Name sequence** added</span></span></br><span data-ttu-id="e932a-137">تم إضافة **الأعمال من الصفحة الرئيسية**</span><span class="sxs-lookup"><span data-stu-id="e932a-137">**Works from home** added</span></span></br><span data-ttu-id="e932a-138">تمت إضافة **اللغة**</span><span class="sxs-lookup"><span data-stu-id="e932a-138">**Language** added</span></span></br><span data-ttu-id="e932a-139">تمت إضافة **تاريخ الأقدمية**</span><span class="sxs-lookup"><span data-stu-id="e932a-139">**Seniority date** added</span></span></br><span data-ttu-id="e932a-140">تمت إضاف **تاريخ التفعيل السنوي**</span><span class="sxs-lookup"><span data-stu-id="e932a-140">**Anniversary date** added</span></span></br><span data-ttu-id="e932a-141">تمت إضافة **تاريخ التوظيف الأصلي**</span><span class="sxs-lookup"><span data-stu-id="e932a-141">**Original hire date** added</span></span> |
| <span data-ttu-id="e932a-142">تغييرات كيان **التوظيف**</span><span class="sxs-lookup"><span data-stu-id="e932a-142">**Employment** entity changes</span></span> | <span data-ttu-id="e932a-143">تمت إضافة **الأبعاد المالية**</span><span class="sxs-lookup"><span data-stu-id="e932a-143">**Financial dimensions** added</span></span></br><span data-ttu-id="e932a-144">تمت إضافة **سبب الإنهاء**</span><span class="sxs-lookup"><span data-stu-id="e932a-144">**Termination reason** added</span></span></br><span data-ttu-id="e932a-145">تمت إعادة تسمية **تاريخ الإنهاء** من **تاريخ الانتقال**</span><span class="sxs-lookup"><span data-stu-id="e932a-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="e932a-146">تمت إضافة **تاريخ فترة الاختبار**</span><span class="sxs-lookup"><span data-stu-id="e932a-146">**Probation date** added</span></span> |
| <span data-ttu-id="e932a-147">تغييرات كيان **عنوان العامل**</span><span class="sxs-lookup"><span data-stu-id="e932a-147">**Worker address** entity changes</span></span> | <span data-ttu-id="e932a-148">تمت إضافة **عنوان الشارع**</span><span class="sxs-lookup"><span data-stu-id="e932a-148">**Street address** added</span></span></br><span data-ttu-id="e932a-149">**سطر العنوان 1**، و **سطر العنوان 2**، و **سطر العنوان 3** المميز للإهلاك</span><span class="sxs-lookup"><span data-stu-id="e932a-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="e932a-150">كيانات إعداد التعويض المتغيرة الجديدة</span><span class="sxs-lookup"><span data-stu-id="e932a-150">New variable compensation setup entities</span></span> | <span data-ttu-id="e932a-151">**نوع خطة التعويض المتغير**</span><span class="sxs-lookup"><span data-stu-id="e932a-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="e932a-152">**خطة التعويض المتغيرة**</span><span class="sxs-lookup"><span data-stu-id="e932a-152">**Compensation variable plan**</span></span></br><span data-ttu-id="e932a-153">**قواعد الاستحقاق**</span><span class="sxs-lookup"><span data-stu-id="e932a-153">**Vesting rules**</span></span></br><span data-ttu-id="e932a-154">**مستوى خطة التعويض المتغير**</span><span class="sxs-lookup"><span data-stu-id="e932a-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="e932a-155">كيان **توظيف تقويم العامل** الجديد</span><span class="sxs-lookup"><span data-stu-id="e932a-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="e932a-156">تمت إضافة **كيان تقويم العمل**</span><span class="sxs-lookup"><span data-stu-id="e932a-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="e932a-157">كيان **تفاصيل المنصب في كشف الرواتب** الجديد</span><span class="sxs-lookup"><span data-stu-id="e932a-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="e932a-158">تمت إضافة **تفاصيل المنصب في كشف الرواتب**</span><span class="sxs-lookup"><span data-stu-id="e932a-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="e932a-159">كيان **العنوان** الجديد</span><span class="sxs-lookup"><span data-stu-id="e932a-159">New **Title** entity</span></span> | <span data-ttu-id="e932a-160">تمت إضافة **العنوان**.</span><span class="sxs-lookup"><span data-stu-id="e932a-160">**Title** added.</span></span> <span data-ttu-id="e932a-161">سيتم تضمين كيان **العنوان** الجديد في عملية المزامنة بين Human Resources وDataverse.</span><span class="sxs-lookup"><span data-stu-id="e932a-161">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="e932a-162">ولن تتم الإشارة إليه من كيانات **منصب الوظيفة** أو **الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="e932a-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e932a-163">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="e932a-163">See also</span></span>

[<span data-ttu-id="e932a-164">المزايا الجديدة أو المتغيرة في Human Resources</span><span class="sxs-lookup"><span data-stu-id="e932a-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="e932a-165">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="e932a-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="e932a-166">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="e932a-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="e932a-167">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="e932a-167">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]