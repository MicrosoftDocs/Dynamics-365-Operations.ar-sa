---
title: الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Finance
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها من Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a406db6d78302fa05596a58fffb7464222d4bfea
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689484"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="ec97f-103">الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="ec97f-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec97f-104">يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها من Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ec97f-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="ec97f-105">لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.</span><span class="sxs-lookup"><span data-stu-id="ec97f-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="ec97f-106">لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.</span><span class="sxs-lookup"><span data-stu-id="ec97f-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="ec97f-107">تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="ec97f-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="ec97f-108">يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="ec97f-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="ec97f-109">يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ec97f-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a><span data-ttu-id="ec97f-110">ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.16 من Finance</span><span class="sxs-lookup"><span data-stu-id="ec97f-110">Features removed or deprecated in the Finance 10.0.16 release</span></span>

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a><span data-ttu-id="ec97f-111">"تنسيق تصدير حركة دفتر الأستاذ (BE)" تنسيق التقارير الإلكترونية ونموذج تصدير حركة دفتر الأستاذ (BE) "الخاص ببلجيكا</span><span class="sxs-lookup"><span data-stu-id="ec97f-111">"Ledger transaction export format (BE)" Electronic reporting format and respective "Ledger transaction export (BE)" model for Belgium</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="ec97f-112">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="ec97f-113">تم استبداله بتنسيق جديد للتقارير الإلكترونية ضمن النموذج "ملف مراجعة قياسي (SAF-T)".</span><span class="sxs-lookup"><span data-stu-id="ec97f-113">Replaced with new ER format under "Standard Audit File (SAF-T)" model.</span></span>  |
| <span data-ttu-id="ec97f-114">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="ec97f-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="ec97f-115">نعم</span><span class="sxs-lookup"><span data-stu-id="ec97f-115">Yes</span></span> |
| <span data-ttu-id="ec97f-116">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-116">**Product areas affected**</span></span>         | <span data-ttu-id="ec97f-117">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="ec97f-117">Application</span></span> |
| <span data-ttu-id="ec97f-118">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="ec97f-118">**Deployment option**</span></span>              | <span data-ttu-id="ec97f-119">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="ec97f-119">All</span></span> |
| <span data-ttu-id="ec97f-120">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-120">**Status**</span></span>                         | <span data-ttu-id="ec97f-121">مهمل: بحلول 1 ديسمبر، 2021، إننا نخطط إلى عدم دعم "تنسيق تصدير حركة دفتر الأستاذ (BE)" وتنسيق التقارير الإلكترونية (ER) والنموذج المعني "تصدير حركة دفتر الأستاذ (BE)".</span><span class="sxs-lookup"><span data-stu-id="ec97f-121">Deprecated: By December 1, 2021, we plan to no longer support the "Ledger transaction export format (BE)" Electronic reporting (ER) format and respective "Ledger transaction export (BE)" model.</span></span> <span data-ttu-id="ec97f-122">يتم تقديم تنسيق "تصدير بيانات دفتر الأستاذ العام (BE)" الجديد مع "تعيين نموذج بيانات دفتر الأستاذ العام" بدلاً من النموذج "ملف مراجعة قياسي (SAF-T)".</span><span class="sxs-lookup"><span data-stu-id="ec97f-122">A new "General ledger data export (BE)" format together with "General ledger data model mapping" are introduced instead under the "Standard Audit File (SAF-T)" model.</span></span> |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a><span data-ttu-id="ec97f-123">تقرير "ضريبة القيمة المضافة 100" للمملكة المتحدة بتنسيق SSRS.</span><span class="sxs-lookup"><span data-stu-id="ec97f-123">"VAT 100" report for the United Kingdom in SSRS format</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="ec97f-124">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="ec97f-125">تم استبداله بتنسيق ER الجديد - تنسيق Excel لإقرار ضريبة القيمة المضافة (المملكة المتحدة)" ضمن "نموذج إقرار الضريبة".</span><span class="sxs-lookup"><span data-stu-id="ec97f-125">Replaced with new ER format - "VAT Declaration Excel (UK)" format under "Tax declaration model".</span></span>  |
| <span data-ttu-id="ec97f-126">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="ec97f-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="ec97f-127">نعم</span><span class="sxs-lookup"><span data-stu-id="ec97f-127">Yes</span></span> |
| <span data-ttu-id="ec97f-128">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-128">**Product areas affected**</span></span>         | <span data-ttu-id="ec97f-129">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="ec97f-129">Application</span></span> |
| <span data-ttu-id="ec97f-130">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="ec97f-130">**Deployment option**</span></span>              | <span data-ttu-id="ec97f-131">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="ec97f-131">All</span></span> |
| <span data-ttu-id="ec97f-132">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-132">**Status**</span></span>                         | <span data-ttu-id="ec97f-133">مهمل: بحلول 1 ديسمبر، 2021، لن نقوم بعد الآن بتقديم الدعم لإصدار "تقرير ضريبة القيمة المضافة 100" بتنسيق SSRS.</span><span class="sxs-lookup"><span data-stu-id="ec97f-133">Deprecated: By December 1, 2021, we plan to no longer support the "VAT 100 report" in SSRS format.</span></span> <span data-ttu-id="ec97f-134">تم تقديم التنسيق الجديد " Excel لإقرار بضريبة القيمة المضافة (المملكة المتحدة) ضمن "نموذج إقرار الضريبة" في [ميزة ضريبة القيمة المضافة لرقمنة الضرائب MTD](../localizations/emea-gbr-mtd-vat-integration.md).</span><span class="sxs-lookup"><span data-stu-id="ec97f-134">A new "VAT Declaration Excel (UK)" format under "Tax declaration model" was introduced in the [MTD VAT feature](../localizations/emea-gbr-mtd-vat-integration.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a><span data-ttu-id="ec97f-135">ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.15 من Finance</span><span class="sxs-lookup"><span data-stu-id="ec97f-135">Features removed or deprecated in the Finance 10.0.15 release</span></span>

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a><span data-ttu-id="ec97f-136">تم إهمال دعم Internet Explorer 11 لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ec97f-136">Internet Explorer 11 support for Dynamics 365 is deprecated</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="ec97f-137">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-137">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="ec97f-138">اعتبارًا من ديسمبر 2020، تم إهمال دعم Microsoft Internet Explorer 11 لجميع منتجات Dynamics 365، ولن يتم دعم Internet Explorer 11 بعد أغسطس 2021.</span><span class="sxs-lookup"><span data-stu-id="ec97f-138">Effective December 2020, Microsoft Internet Explorer 11 support for all Dynamics 365 products is deprecated, and Internet Explorer 11 won’t be supported after August 2021.</span></span><br><br><span data-ttu-id="ec97f-139">سيؤثر هذا الاجراء علي العملاء الذين يستخدمون منتجات Dynamics 365 التي تم تصميمها ليتم استخدامها من خلال واجهة Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="ec97f-139">This will impact customers who use Dynamics 365 products that are designed to be used through an Internet Explorer 11 interface.</span></span> <span data-ttu-id="ec97f-140">بعد أغسطس 2021، لن يتم دعم Internet Explorer 11 لمنتجات Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ec97f-140">After August 2021, Internet Explorer 11 won't be supported for such Dynamics 365 products.</span></span> |
| <span data-ttu-id="ec97f-141">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="ec97f-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="ec97f-142">نوصي العملاء بالانتقال إلى Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ec97f-142">We recommend that customers transition to Microsoft Edge.</span></span>|
| <span data-ttu-id="ec97f-143">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-143">**Product areas affected**</span></span>         | <span data-ttu-id="ec97f-144">كافة منتجات Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ec97f-144">All Dynamics 365 products</span></span> |
| <span data-ttu-id="ec97f-145">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="ec97f-145">**Deployment option**</span></span>              | <span data-ttu-id="ec97f-146">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="ec97f-146">All</span></span>|
| <span data-ttu-id="ec97f-147">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-147">**Status**</span></span>                         | <span data-ttu-id="ec97f-148">مهملة.</span><span class="sxs-lookup"><span data-stu-id="ec97f-148">Deprecated.</span></span> <span data-ttu-id="ec97f-149">لن يتم دعم Internet Explorer 11 بعد (أغسطس) 2021.</span><span class="sxs-lookup"><span data-stu-id="ec97f-149">Internet Explorer 11 won’t be supported after August 2021.</span></span>|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="ec97f-150">ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.12 من Finance</span><span class="sxs-lookup"><span data-stu-id="ec97f-150">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="ec97f-151">تقارير SSRS البولندية: سجل ضريبة القيمة المضافة للإخراج، سجل ضريبة القيمة المضافة للإدخال، سجل تقرير ملخص ضريبة القيمة المضافة للاتحاد الأوروبي‬، مرجع الميزة PL-00014</span><span class="sxs-lookup"><span data-stu-id="ec97f-151">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="ec97f-152">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-152">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="ec97f-153">غير مطلوبة من الناحية القانونية.</span><span class="sxs-lookup"><span data-stu-id="ec97f-153">Not legally required.</span></span>  |
| <span data-ttu-id="ec97f-154">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="ec97f-154">**Replaced by another feature?**</span></span>   | <span data-ttu-id="ec97f-155">نعم (تنسيق Excel لملف المراجعة القياسي مع إقرار ضريبة القيمة المضافة - JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="ec97f-155">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="ec97f-156">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-156">**Product areas affected**</span></span>         | <span data-ttu-id="ec97f-157">التطبيق</span><span class="sxs-lookup"><span data-stu-id="ec97f-157">Application</span></span> |
| <span data-ttu-id="ec97f-158">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="ec97f-158">**Deployment option**</span></span>              | <span data-ttu-id="ec97f-159">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="ec97f-159">All</span></span> |
| <span data-ttu-id="ec97f-160">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-160">**Status**</span></span>                         | <span data-ttu-id="ec97f-161">ميزات مهملة: بحلول 1 يوليو 2021، سنتوقف عن توفير الدعم لتقارير SSRS: **سجل ضريبة القيمة المضافة للإخراج، سجل ضريبة القيمة المضافة للإدخال، سجل تقرير ملخص ضريبة القيمة المضافة للاتحاد الأوروبي‬، مرجع الميزة PL-00014‬**.</span><span class="sxs-lookup"><span data-stu-id="ec97f-161">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="ec97f-162">بدلاً من ذلك، سيتم تقديم مثال عن تنسيق Excel لملف المراجعة القياسي مع إقرار ضريبة القيمة المضافة (JPK_VDEK).</span><span class="sxs-lookup"><span data-stu-id="ec97f-162">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="ec97f-163">ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.11 من Finance</span><span class="sxs-lookup"><span data-stu-id="ec97f-163">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="ec97f-164">الحسابات النرويجية الرئيسية القياسية</span><span class="sxs-lookup"><span data-stu-id="ec97f-164">Norwegian Standard main accounts</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="ec97f-165">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-165">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="ec97f-166">إعادة التصميم</span><span class="sxs-lookup"><span data-stu-id="ec97f-166">Redesign</span></span>  |
| <span data-ttu-id="ec97f-167">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="ec97f-167">**Replaced by another feature?**</span></span>   | <span data-ttu-id="ec97f-168">نعم (تم استبداله بالمعلمات الخاصة بتطبيق تنسيق التقارير الإلكترونية)</span><span class="sxs-lookup"><span data-stu-id="ec97f-168">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="ec97f-169">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-169">**Product areas affected**</span></span>         | <span data-ttu-id="ec97f-170">التطبيق</span><span class="sxs-lookup"><span data-stu-id="ec97f-170">Application</span></span> |
| <span data-ttu-id="ec97f-171">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="ec97f-171">**Deployment option**</span></span>              | <span data-ttu-id="ec97f-172">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="ec97f-172">All</span></span> |
| <span data-ttu-id="ec97f-173">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-173">**Status**</span></span>                         | <span data-ttu-id="ec97f-174">ميزة مهملة: بحلول 1 ابريل 2021، نخطط لإيقاف دعم الوظيفة ذات الصلة بالحسابات الرئيسية القياسية: حقل المرجع، الجدول ذو الصلة، كيان البيانات.</span><span class="sxs-lookup"><span data-stu-id="ec97f-174">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="ec97f-175">ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.7 من Finance</span><span class="sxs-lookup"><span data-stu-id="ec97f-175">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="ec97f-176">لم يعد مربع حوار تغيير طلب سير العمل يتضمن القائمة المنسدلة لتحديد المستخدم</span><span class="sxs-lookup"><span data-stu-id="ec97f-176">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="ec97f-177">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-177">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="ec97f-178">يتم تغييرها إلى الميزة مع تحديد مجموعات الحساب.</span><span class="sxs-lookup"><span data-stu-id="ec97f-178">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="ec97f-179">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="ec97f-179">**Replaced by another feature?**</span></span>   | <span data-ttu-id="ec97f-180">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="ec97f-180">Yes</span></span> |
| <span data-ttu-id="ec97f-181">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-181">**Product areas affected**</span></span>         | <span data-ttu-id="ec97f-182">سير العمل</span><span class="sxs-lookup"><span data-stu-id="ec97f-182">Workflow</span></span> |
| <span data-ttu-id="ec97f-183">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="ec97f-183">**Deployment option**</span></span>              | <span data-ttu-id="ec97f-184">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="ec97f-184">All</span></span> |
| <span data-ttu-id="ec97f-185">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="ec97f-185">**Status**</span></span>                         | <span data-ttu-id="ec97f-186">مهمل: بحلول 1 ديسمبر 2020، لا نقدم خطط لدعم إعداد أنواع الإيصالات الصينية دون تحديد مجموعات الحساب.</span><span class="sxs-lookup"><span data-stu-id="ec97f-186">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="ec97f-187">يمكنك العثور على مزيد من التفاصيل حول التصميم الجديد في [ما الجديد في الإصدار 10.0.7](whats-new-changed-10-0-7.md).</span><span class="sxs-lookup"><span data-stu-id="ec97f-187">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="ec97f-188">الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها</span><span class="sxs-lookup"><span data-stu-id="ec97f-188">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="ec97f-189">لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="ec97f-189">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
