---
title: الموافقة على فاتورة المحمول
description: يهدف هذا الموضوع إلى توفير نهج عملي لتصميم سيناريوهات المحمول عبر أخذ عمليات الموافقة على فواتير المورّد للمحمول كحالة استخدام.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1e18d26a4ccee195d09560c62b1fb1dd05750cfd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991307"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="db42f-103">الموافقة على فاتورة المحمول</span><span class="sxs-lookup"><span data-stu-id="db42f-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db42f-104">تسمح قدرات المحمول لمستخدمي الشركات بتصميم تجارب المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="db42f-105">للسيناريوهات المتقدمة، يسمح النظام الأساسي أيضًا للمطورين بتوسيع القدرات بحسب رغباتهم.</span><span class="sxs-lookup"><span data-stu-id="db42f-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="db42f-106">وتُعد أفضل وسيلة للتعرف على بعض المفاهيم الجديدة على المحمول الانتقال عبر عملية تصميم بعض السيناريوهات.</span><span class="sxs-lookup"><span data-stu-id="db42f-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="db42f-107">يهدف هذا الموضوع إلى توفير نهج عملي لتصميم سيناريوهات المحمول عبر أخذ عمليات الموافقة على فواتير المورّد للمحمول كحالة استخدام.</span><span class="sxs-lookup"><span data-stu-id="db42f-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="db42f-108">من المفترض أن يساعدك هذا الموضوع على تصميم أشكال مختلفة أخرى للسيناريوهات ويمكن أيضًا تطبيقه على سيناريوهات أخرى لا علاقة لها بفواتير المورّد.</span><span class="sxs-lookup"><span data-stu-id="db42f-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="db42f-109">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="db42f-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="db42f-110">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="db42f-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="db42f-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="db42f-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db42f-112">قبل قراءة دليل المحمول</span><span class="sxs-lookup"><span data-stu-id="db42f-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="db42f-113">النظام الأساسي للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="db42f-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="db42f-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="db42f-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="db42f-115">بيئة يتوفر فيها الإصدار 1611 والتحديث الثالث للنظام الأساسي (نوفمبر 2016)</span><span class="sxs-lookup"><span data-stu-id="db42f-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="db42f-116">تثبيت الإصلاح العاجل KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="db42f-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="db42f-117">باستطاعة مسجل المهام تسجيل أمري "إغلاق" بطريق الخطأ لمربعات الحوار ذات القوائم المنسدلة المضمنة في التحديث الثالث للنظام الأساسي (تحديث نوفمبر 2016).</span><span class="sxs-lookup"><span data-stu-id="db42f-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="db42f-118">تثبيت الإصلاح العاجل KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="db42f-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="db42f-119">يتيح هذا الإصلاح العاجل عرض المرفقات على عميل المحمول المضمن في التحديث الثالث للنظام الأساسي (تحديث نوفمبر 2016).</span><span class="sxs-lookup"><span data-stu-id="db42f-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="db42f-120">تثبيت الإصلاح العاجل KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="db42f-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="db42f-121">التعليمات البرمجية للتطبيق لطلب الموافقة على فواتير المورّد على المحمول مضمنة في الإصدار 7.0.1 (مايو 2016).</span><span class="sxs-lookup"><span data-stu-id="db42f-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="db42f-122">جهاز يعمل بنظام Android أو iOS أو Windows تم فيه تثبيت تطبيق المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="db42f-123">البحث عن التطبيق في متجر التطبيقات المناسب.</span><span class="sxs-lookup"><span data-stu-id="db42f-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="db42f-124">مقدمة</span><span class="sxs-lookup"><span data-stu-id="db42f-124">Introduction</span></span>
<span data-ttu-id="db42f-125">تتطلب عمليات الموافقة على فواتير المحمول‬ للمورّد الإصلاحات العاجلة الثلاثة الموضحة في قسم "المتطلبات الأساسية‬".</span><span class="sxs-lookup"><span data-stu-id="db42f-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="db42f-126">لا توفر هذه الإصلاحات العاجلة مساحة عمل لعمليات الموافقة على الفواتير.</span><span class="sxs-lookup"><span data-stu-id="db42f-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="db42f-127">لمعرفة ما هي مساحة العمل في سياق المحمول، اقرأ دليل المحمول المذكور في قسم "المتطلبات الأساسية‬".</span><span class="sxs-lookup"><span data-stu-id="db42f-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="db42f-128">يجب تصميم مساحة عمل عمليات الموافقة على الفواتير.</span><span class="sxs-lookup"><span data-stu-id="db42f-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="db42f-129">تقوم كل مؤسسة بتنظيم وتعريف عمليات الأعمال الخاصة بفواتير المورّد بشكل مختلف.</span><span class="sxs-lookup"><span data-stu-id="db42f-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="db42f-130">قبل أن تقوم بتصميم تجربة المحمول لعمليات الموافقة على فواتير المورّد، يجب مراعاة الجوانب التالية من عملية الأعمال.</span><span class="sxs-lookup"><span data-stu-id="db42f-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="db42f-131">ويمكن استخدام نقاط البيانات هذه إلى أقصى حد ممكن لتحسين تجربة المستخدم على الجهاز.</span><span class="sxs-lookup"><span data-stu-id="db42f-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="db42f-132">ما هي الحقول من رأس الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟</span><span class="sxs-lookup"><span data-stu-id="db42f-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="db42f-133">ما هي الحقول من سطور الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟‬</span><span class="sxs-lookup"><span data-stu-id="db42f-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="db42f-134">ما عدد سطور الفاتورة الموجودة في فاتورة؟</span><span class="sxs-lookup"><span data-stu-id="db42f-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="db42f-135">يمكنك هنا تطبيق القاعدة 80-20، والتحسين إلى 80 في المائة.</span><span class="sxs-lookup"><span data-stu-id="db42f-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="db42f-136">هل سيرغب المستخدمون في رؤية التوزيع المحاسبي (أكواد الفواتير) على الجهاز المحمول أثناء المراجعات؟</span><span class="sxs-lookup"><span data-stu-id="db42f-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="db42f-137">إذا كان الجواب على هذا السؤال "نعم"، فعليك أخذ الأسئلة التالية في الاعتبار:</span><span class="sxs-lookup"><span data-stu-id="db42f-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="db42f-138">ما عدد التوزيعات المحاسبية (السعر المفصل وضريبة المبيعات والمصاريف والتقسيمات وغير ذلك) لبند الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="db42f-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="db42f-139">مرة أخرى، يجب تطبيق القاعدة 80-20.</span><span class="sxs-lookup"><span data-stu-id="db42f-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="db42f-140">هل تتضمن الفواتير توزيعات محاسبية على رأس الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="db42f-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="db42f-141">إذا كان الأمر كذلك، فيجب أن تكون هذه التوزيعات المحاسبية متوفرة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="db42f-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="db42f-142">لا يفسر هذا الموضوع كيفية تحرير التوزيعات المحاسبية، لأن هذه الوظيفة غير معتمدة حاليًا لسيناريوهات المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="db42f-143">هل سيحتاج المستخدمون لمشاهدة مرفقات الفاتورة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="db42f-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="db42f-144">سوف يختلف تصميم تجربة المحمول لعمليات الموافقة على الفواتير، وفقًا للإجابات على هذه الأسئلة.</span><span class="sxs-lookup"><span data-stu-id="db42f-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="db42f-145">يهدف ذلك إلى تحسين تجربة المستخدم الخاصة بعملية الأعمال على جهاز محمول في مؤسسة.</span><span class="sxs-lookup"><span data-stu-id="db42f-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="db42f-146">في بقية هذا الموضوع، سوف ننظر إلى شكلين مختلفين من السيناريوهات يستندان إلى أجوبة مختلفة على الأسئلة السابقة.</span><span class="sxs-lookup"><span data-stu-id="db42f-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="db42f-147">كتوجيه عام، عندما تعمل مع مصمم المحمول، تأكد من "نشر" التغييرات لتجنب فقدان التحديثات.</span><span class="sxs-lookup"><span data-stu-id="db42f-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="db42f-148">تصميم سيناريو بسيط للموافقة على الفواتير لشركة Contoso</span><span class="sxs-lookup"><span data-stu-id="db42f-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db42f-149">سمة السيناريو</span><span class="sxs-lookup"><span data-stu-id="db42f-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="db42f-150">الإجابة</span><span class="sxs-lookup"><span data-stu-id="db42f-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db42f-151">ما هي الحقول من رأس الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟</span><span class="sxs-lookup"><span data-stu-id="db42f-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="db42f-152">اسم المورّد</span><span class="sxs-lookup"><span data-stu-id="db42f-152">Vendor name</span></span></li>
<li><span data-ttu-id="db42f-153">إجمالي الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-153">Invoice total</span></span></li>
<li><span data-ttu-id="db42f-154">حساب الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-154">Invoice account</span></span></li>
<li><span data-ttu-id="db42f-155">رقم الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-155">Invoice number</span></span></li>
<li><span data-ttu-id="db42f-156">تاريخ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-156">Invoice date</span></span></li>
<li><span data-ttu-id="db42f-157">وصف الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-157">Invoice description</span></span></li>
<li><span data-ttu-id="db42f-158">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="db42f-158">Due date</span></span></li>
<li><span data-ttu-id="db42f-159">عملة الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db42f-160">ما هي الحقول من سطور الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟‬</span><span class="sxs-lookup"><span data-stu-id="db42f-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="db42f-161">فئة التدبير</span><span class="sxs-lookup"><span data-stu-id="db42f-161">Procurement category</span></span></li>
<li><span data-ttu-id="db42f-162">الكمية</span><span class="sxs-lookup"><span data-stu-id="db42f-162">Quantity</span></span></li>
<li><span data-ttu-id="db42f-163">سعر الوحدة</span><span class="sxs-lookup"><span data-stu-id="db42f-163">Unit price</span></span></li>
<li><span data-ttu-id="db42f-164">المبلغ الصافي للسطر</span><span class="sxs-lookup"><span data-stu-id="db42f-164">Line net amount</span></span></li>
<li><span data-ttu-id="db42f-165">مبلغ 1099</span><span class="sxs-lookup"><span data-stu-id="db42f-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db42f-166">ما عدد سطور الفاتورة الموجودة في فاتورة؟</span><span class="sxs-lookup"><span data-stu-id="db42f-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="db42f-167">يمكنك هنا تطبيق القاعدة 80-20، والتحسين إلى 80 في المائة.</span><span class="sxs-lookup"><span data-stu-id="db42f-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="db42f-168">1</span><span class="sxs-lookup"><span data-stu-id="db42f-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db42f-169">هل سيرغب المستخدمون في رؤية التوزيع المحاسبي (أكواد الفواتير) على الجهاز المحمول أثناء المراجعات؟</span><span class="sxs-lookup"><span data-stu-id="db42f-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="db42f-170">نعم</span><span class="sxs-lookup"><span data-stu-id="db42f-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db42f-171">ما عدد التوزيعات المحاسبية (السعر المفصل وضريبة المبيعات والمصاريف وغير ذلك) لبند الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="db42f-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="db42f-172">مرة أخرى، يجب تطبيق القاعدة 80-20.</span><span class="sxs-lookup"><span data-stu-id="db42f-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="db42f-173">السعر المفصل: 2 ضريبة المبيعات: 0 المصروفات: 0</span><span class="sxs-lookup"><span data-stu-id="db42f-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db42f-174">هل تتضمن الفواتير توزيعات محاسبية على رأس الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="db42f-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="db42f-175">إذا كان الأمر كذلك، فيجب أن تكون هذه التوزيعات المحاسبية متوفرة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="db42f-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="db42f-176">غير مستخدم</span><span class="sxs-lookup"><span data-stu-id="db42f-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db42f-177">هل سيحتاج المستخدمون لمشاهدة مرفقات الفاتورة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="db42f-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="db42f-178">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="db42f-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="db42f-179">إنشاء مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="db42f-179">Create the workspace</span></span>

1.  <span data-ttu-id="db42f-180">في المستعرض، قم بتسجيل الدخول إلى التطبيق.</span><span class="sxs-lookup"><span data-stu-id="db42f-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="db42f-181">بعد تسجيل الدخول، قم بإلحاق **&mode=mobile** بعنوان URL كما هو مبين في المثال التالي، وحدّث الصفحة: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="db42f-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="db42f-182">انقر فوق زر **الإعدادات** (الترس) في الجزء العلوي الأيسر من الصفحة، ثم انقر فوق **تطبيق المحمول**.</span><span class="sxs-lookup"><span data-stu-id="db42f-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="db42f-183">يجب أن يظهر مصمم التطبيق المحمول تمامًا كما يظهر مسجل المهام.</span><span class="sxs-lookup"><span data-stu-id="db42f-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="db42f-184">انقر فوق **إضافة** لإنشاء مساحة عمل جديدة.</span><span class="sxs-lookup"><span data-stu-id="db42f-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="db42f-185">على سبيل المثال، يمكنك تسمية مساحة العمل **موافقاتي**.</span><span class="sxs-lookup"><span data-stu-id="db42f-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="db42f-186">أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="db42f-186">Enter a description.</span></span>
6.  <span data-ttu-id="db42f-187">حدد لون مساحة عمل.</span><span class="sxs-lookup"><span data-stu-id="db42f-187">Select a workspace color.</span></span> <span data-ttu-id="db42f-188">سيتم استخدام لون مساحة العمل للنمط العام لتجربة المحمول لمساحة العمل هذه.</span><span class="sxs-lookup"><span data-stu-id="db42f-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="db42f-189">حدد أيقونة لمساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="db42f-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="db42f-190">انقر فوق **تم**</span><span class="sxs-lookup"><span data-stu-id="db42f-190">Click **Done**</span></span>
9.  <span data-ttu-id="db42f-191">انقر فوق **نشر مساحة العمل** لحفظ التغييرات</span><span class="sxs-lookup"><span data-stu-id="db42f-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="db42f-192">فواتير المورَّد المعينة إلي</span><span class="sxs-lookup"><span data-stu-id="db42f-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="db42f-193">صفحة المحمول الأولى التي يجب تصميمها هي قائمة الفواتير التي تم تعيينها للمستخدم لكي يراجعها.</span><span class="sxs-lookup"><span data-stu-id="db42f-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="db42f-194">لتصميم صفحة المحمول هذه استخدم الصفحة **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="db42f-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="db42f-195">قبل إكمال هذا الإجراء، تأكد من تعيين فاتورة مورّد واحد على الأقل لك للمراجعة، ومن وجود توزيعين لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="db42f-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="db42f-196">هذا الإعداد يفي بمتطلبات هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="db42f-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="db42f-197">في عنوان URL، استبدل اسم عنصر القائمة بالاسم **VendMobileInvoiceAssignedToMeListPage** لفتح إصدار المحمول لصفحة القائمة **فواتير المورّد المعلقة المعينة إليّ‬** في وحدة **الحسابات الدائنة**.</span><span class="sxs-lookup"><span data-stu-id="db42f-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="db42f-198">بحسب عدد الفواتير المعينة لك في النظام، ستعرض هذه الصفحة تلك الفواتير.</span><span class="sxs-lookup"><span data-stu-id="db42f-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="db42f-199">للبحث عن فاتورة معينة، يمكنك استخدام عامل التصفية إلى اليمين.</span><span class="sxs-lookup"><span data-stu-id="db42f-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="db42f-200">ومع ذلك، لا نحتاج إلى فاتورة معينة لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="db42f-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="db42f-201">نحن نحتاج فقط إلى فاتورة معينة لك سوف تسمح لك بتصميم صفحة المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="db42f-202">تم تصميم الصفحات الجديدة المتوفرة خصيصًا لتطوير سيناريوهات المحمول لفاتورة المورّد.</span><span class="sxs-lookup"><span data-stu-id="db42f-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="db42f-203">ولذلك، يجب استخدام هذه الصفحات.</span><span class="sxs-lookup"><span data-stu-id="db42f-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="db42f-204">يجب أن يكون عنوان URL مماثلاً لعنوان URLالتالي، وبعد أن تقوم بإدخاله، يجب أن تظهر الصفحة المعروضة في الشكل التوضيحي: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="db42f-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="db42f-205">[![فواتير المورد المعلقة المعينة إلى صفحتي](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="db42f-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="db42f-206">انقر فوق زر **الإعدادات** (الترس) في الجزء العلوي الأيسر من الصفحة، ثم انقر فوق **تطبيق المحمول**</span><span class="sxs-lookup"><span data-stu-id="db42f-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="db42f-207">حدد مساحة العمل، ثم انقر فوق **تحرير**</span><span class="sxs-lookup"><span data-stu-id="db42f-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="db42f-208">انقر فوق **صفحة إضافة** لإنشاء صفحة المحمول الأولى.</span><span class="sxs-lookup"><span data-stu-id="db42f-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="db42f-209">أدخل اسمًا، مثل **فواتير المورّد الخاصة بي**، ووصفًا، مثل **فواتير المورّد المعينة إليّ للمراجعة**.</span><span class="sxs-lookup"><span data-stu-id="db42f-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="db42f-210">انقر فوق **تم‏‎**.</span><span class="sxs-lookup"><span data-stu-id="db42f-210">Click **Done**.</span></span>
7.  <span data-ttu-id="db42f-211">في مصمم المحمول، على علامة تبويب **الحقول**، انقر فوق **تحديد الحقول‬**.</span><span class="sxs-lookup"><span data-stu-id="db42f-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="db42f-212">يجب أن تكون الأعمدة في صفحة القائمة مماثلة للشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="db42f-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="db42f-213">[![أعمدة على صفحة فواتير المورّد المعلقة المعينة إليّ‬](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="db42f-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="db42f-214">أضف الأعمدة المطلوبة من صفحة القائمة التي يجب أن تظهر للمستخدم في صفحة المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="db42f-215">الترتيب الذي تستخدمه لإضافة الأعمدة هو الترتيب الذي ستظهر فيه الحقول للمستخدم النهائي.</span><span class="sxs-lookup"><span data-stu-id="db42f-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="db42f-216">الطريقة الوحيدة لتغيير ترتيب حقول هي إعادة تحديد كافة الحقول.</span><span class="sxs-lookup"><span data-stu-id="db42f-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="db42f-217">استنادًا إلى متطلبات هذا السيناريو، تعتبر الحقول الثمانية التالية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="db42f-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="db42f-218">ومع ذلك، قد يجد بعض المستخدمين أن الحقول الثمانية تشكل كمية كبيرة جدًا من المعلومات على جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="db42f-219">ولذلك، سنعرض أهم الحقول فقط في طريقة عرض قائمة المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="db42f-220">وستظهر الحقول المتبقية في طريقة عرض التفاصيل التي سوف نصممها لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="db42f-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="db42f-221">الآن، سوف نقوم بإضافة الحقول التالية.</span><span class="sxs-lookup"><span data-stu-id="db42f-221">For now, we will add the following fields.</span></span> <span data-ttu-id="db42f-222">انقر فوق علامة الجمع (**+**) في هذه الأعمدة لإضافتها إلى صفحة المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="db42f-223">اسم المورّد</span><span class="sxs-lookup"><span data-stu-id="db42f-223">Vendor name</span></span>
    - <span data-ttu-id="db42f-224">إجمالي الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-224">Invoice total</span></span>
    - <span data-ttu-id="db42f-225">حساب الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-225">Invoice account</span></span>
    - <span data-ttu-id="db42f-226">رقم الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-226">Invoice number</span></span>
    - <span data-ttu-id="db42f-227">تاريخ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-227">Invoice date</span></span>

    <span data-ttu-id="db42f-228">بعد إضافة الحقول، يجب أن تشبه صفحة المحمول الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="db42f-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="db42f-229">[![الصفحة بعد إضافة الحقول](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="db42f-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="db42f-230">يجب أيضًا إضافة الأعمدة التالية الآن، من أجل تمكين إجراءات سير العمل فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="db42f-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="db42f-231">إظهار المهمة المكتملة</span><span class="sxs-lookup"><span data-stu-id="db42f-231">Show complete task</span></span>
    - <span data-ttu-id="db42f-232">إظهار تفويض المهمة</span><span class="sxs-lookup"><span data-stu-id="db42f-232">Show delegate task</span></span>
    - <span data-ttu-id="db42f-233">إظهار استدعاء المهمة</span><span class="sxs-lookup"><span data-stu-id="db42f-233">Show recall task</span></span>
    - <span data-ttu-id="db42f-234">إظهار رفض المهمة</span><span class="sxs-lookup"><span data-stu-id="db42f-234">Show reject task</span></span>
    - <span data-ttu-id="db42f-235">إظهار طلب إكمال المهمة</span><span class="sxs-lookup"><span data-stu-id="db42f-235">Show request completion task</span></span>
    - <span data-ttu-id="db42f-236">إظهار إعادة إرسال المهمة</span><span class="sxs-lookup"><span data-stu-id="db42f-236">Show resubmit task</span></span>

10. <span data-ttu-id="db42f-237">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="db42f-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="db42f-238">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="db42f-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="db42f-239">انقر فوق **نشر مساحة العمل** لحفظ عملك.</span><span class="sxs-lookup"><span data-stu-id="db42f-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="db42f-240">قم بتمكين **عرض إجماليات الفاتورة على قائمة فواتير المورد المعلقة‬** في معلمات الحسابات الدائنة ضمن **الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="db42f-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="db42f-241">تجدر الإشارة إلى أنه فقط من خلال تمكين هذه المعلمة، سيتم حساب إجماليات الفواتير لعرضها في صفحة قائمة فواتير المورد المعلقة.</span><span class="sxs-lookup"><span data-stu-id="db42f-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="db42f-242">هذه قدرة جديدة كجزء من الإصلاح العاجل 3208224 ضمن المتطلبات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="db42f-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="db42f-243">تفصيل فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="db42f-243">Vendor invoice details</span></span>

<span data-ttu-id="db42f-244">لتصميم صفحة تفاصيل الفاتورة للمحمول، استخدم الصفحة **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="db42f-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="db42f-245">لاحظ أنه، استنادًا إلى عدد الفواتير في النظام، تعرض هذه الصفحة الفواتير الأقدم (الفاتورة التي تم إنشاؤها أولاً).</span><span class="sxs-lookup"><span data-stu-id="db42f-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="db42f-246">للبحث عن فاتورة معينة، يمكنك استخدام عامل التصفية إلى اليمين.</span><span class="sxs-lookup"><span data-stu-id="db42f-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="db42f-247">ومع ذلك، لا نحتاج إلى فاتورة معينة لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="db42f-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="db42f-248">نحن نطلب فقط بعض بيانات الفاتورة لكي نتمكن من تصميم صفحة المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="db42f-249">[![صفحة سير العمل](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="db42f-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="db42f-250">في عنوان URL، استبدل اسم عنصر القائمة بالاسم **VendMobileInvoiceHeaderDetails** لفتح النموذج</span><span class="sxs-lookup"><span data-stu-id="db42f-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="db42f-251">افتح مصمم المحمول من زر **الإعدادات** (الترس).</span><span class="sxs-lookup"><span data-stu-id="db42f-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="db42f-252">انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="db42f-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="db42f-253">حدد صفحة **فواتير المورّد الخاصة بي** التي قمت بإنشائها سابقًا، ثم انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="db42f-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="db42f-254">على علامة تبويب **الحقول**، انقر فوق عنوان العمود **الشبكة**.</span><span class="sxs-lookup"><span data-stu-id="db42f-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="db42f-255">انقر فوق **‎خصائص &gt; إضافة صفحة**.</span><span class="sxs-lookup"><span data-stu-id="db42f-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="db42f-256">**ملاحظة:** عندما تنقر فوق العنوان **الشبكة** وتضيف صفحة، تتأسس العلاقة مع صفحة التفاصيل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="db42f-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="db42f-257">أدخل عنوان صفحة، مثل **تفاصيل الفاتورة**، ووصفًا، مثل **عرض رأس الفاتورة وتفاصيل البنود**.</span><span class="sxs-lookup"><span data-stu-id="db42f-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="db42f-258">انقر فوق **تحديد الحقول**.</span><span class="sxs-lookup"><span data-stu-id="db42f-258">Click **Select fields**.</span></span> <span data-ttu-id="db42f-259">لاحظ أن الترتيب الذي تستخدمه لإضافة الأعمدة هو الترتيب الذي ستظهر فيه الحقول للمستخدم النهائي.</span><span class="sxs-lookup"><span data-stu-id="db42f-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="db42f-260">الطريقة الوحيدة لتغيير ترتيب حقول هي إعادة تحديد كافة الحقول.</span><span class="sxs-lookup"><span data-stu-id="db42f-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="db42f-261">أضف الحقول التالية من الرأس، استنادًا إلى متطلبات هذا السيناريو:</span><span class="sxs-lookup"><span data-stu-id="db42f-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="db42f-262">اسم المورّد</span><span class="sxs-lookup"><span data-stu-id="db42f-262">Vendor name</span></span>
   - <span data-ttu-id="db42f-263">إجمالي الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-263">Invoice total</span></span>
   - <span data-ttu-id="db42f-264">حساب الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-264">Invoice account</span></span>
   - <span data-ttu-id="db42f-265">رقم الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-265">Invoice number</span></span>
   - <span data-ttu-id="db42f-266">تاريخ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-266">Invoice date</span></span>
   - <span data-ttu-id="db42f-267">وصف الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-267">Invoice description</span></span>
   - <span data-ttu-id="db42f-268">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="db42f-268">Due date</span></span>
   - <span data-ttu-id="db42f-269">عملة الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-269">Invoice currency</span></span>

10. <span data-ttu-id="db42f-270">أضف الحقول التالية من خطوط الشبكة في الصفحة:</span><span class="sxs-lookup"><span data-stu-id="db42f-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="db42f-271">فئة التدبير</span><span class="sxs-lookup"><span data-stu-id="db42f-271">Procurement category</span></span>
    - <span data-ttu-id="db42f-272">الكمية</span><span class="sxs-lookup"><span data-stu-id="db42f-272">Quantity</span></span>
    - <span data-ttu-id="db42f-273">سعر الوحدة</span><span class="sxs-lookup"><span data-stu-id="db42f-273">Unit price</span></span>
    - <span data-ttu-id="db42f-274">المبلغ الصافي للسطر</span><span class="sxs-lookup"><span data-stu-id="db42f-274">Line net amount</span></span>
    - <span data-ttu-id="db42f-275">مبلغ 1099</span><span class="sxs-lookup"><span data-stu-id="db42f-275">1099 amount</span></span>

11. <span data-ttu-id="db42f-276">بعد إضافة كافة الحقول من الخطوتين السابقتين، انقر فوق **تم**.</span><span class="sxs-lookup"><span data-stu-id="db42f-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="db42f-277">يجب أن تكون الصفحة مماثلة للشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="db42f-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="db42f-278">[![الصفحة بعد إضافة الحقول](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="db42f-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="db42f-279">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="db42f-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="db42f-280">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="db42f-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="db42f-281">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="db42f-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="db42f-282">إجراءات سير العمل</span><span class="sxs-lookup"><span data-stu-id="db42f-282">Workflow actions</span></span>

<span data-ttu-id="db42f-283">لإضافة إجراءات سير العمل، استخدم صفحة **VendMobileInvoiceHeaderDetails**. </span><span class="sxs-lookup"><span data-stu-id="db42f-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="db42f-284">لفتح هذه الصفحة، استبدل اسم عنصر القائمة في URL، كما فعلت سابقًا.</span><span class="sxs-lookup"><span data-stu-id="db42f-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="db42f-285">ثم افتح مصمم المحمول من زر **الإعدادات** (الترس).</span><span class="sxs-lookup"><span data-stu-id="db42f-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="db42f-286">اتبع هذه الخطوات لإضافة إجراءات سير العمل في صفحة التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="db42f-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="db42f-287">من الضروري أن تكون الفواتير المعينة لك في الحالة المناسبة التي تسمح بجعل إجراءات سير العمل التي ستعمل على تصميمها متوفرة لك.</span><span class="sxs-lookup"><span data-stu-id="db42f-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="db42f-288">تسجيل إجراءات سير العمل</span><span class="sxs-lookup"><span data-stu-id="db42f-288">Record workflow actions</span></span>
1.  <span data-ttu-id="db42f-289">انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="db42f-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="db42f-290">حدد صفحة **تفاصيل الفاتورة** التي قمت بإنشائها سابقًا، ومن ثم انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="db42f-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="db42f-291">على علامة تبويب **الإجراءات**، انقر فوق **إضافة إجراء**.</span><span class="sxs-lookup"><span data-stu-id="db42f-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="db42f-292">أدخل عنوان إجراء، مثل **الموافقة**، ووصفًا، مثل **الموافقة على الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="db42f-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="db42f-293">لاحظ أن عنوان الإجراء الذي تدخله هنا يصبح اسم الإجراء الذي يظهر للمستخدم في تطبيق المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="db42f-294">انقر فوق **تم**.</span><span class="sxs-lookup"><span data-stu-id="db42f-294">Click **Done**.</span></span>
6.  <span data-ttu-id="db42f-295">انقر فوق **تحديد الحقول**.</span><span class="sxs-lookup"><span data-stu-id="db42f-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="db42f-296">انتقل عبر عملية سير العمل في صفحة **VendMobileInvoiceHeaderDetails‎**، وأكمل الإجراء الذي تريد تسجيله.</span><span class="sxs-lookup"><span data-stu-id="db42f-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="db42f-297">تأكد من إدخال تعليقات سير العمل أثناء هذه العملية، بحيث يتم أيضًا تضمين حقل تعليقات في تجربة المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="db42f-298">بعد أن يتم تشغيل إجراء سير العمل، انقر فوق **تم** لإكمال مهمة تحديد الحقول.</span><span class="sxs-lookup"><span data-stu-id="db42f-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="db42f-299">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="db42f-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="db42f-300">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="db42f-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="db42f-301">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="db42f-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="db42f-302">كرر الخطوات السابقة لتسجيل كافة إجراءات سير العمل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="db42f-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="db42f-303">إنشاء ملف .js</span><span class="sxs-lookup"><span data-stu-id="db42f-303">Create a .js file</span></span>
1. <span data-ttu-id="db42f-304">افتح المفكرة أو Microsoft Visual Studio، ثم الصق التعليمات البرمجية التالية.</span><span class="sxs-lookup"><span data-stu-id="db42f-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="db42f-305">احفظ الملف بصيغة ملف .js.</span><span class="sxs-lookup"><span data-stu-id="db42f-305">Save the file as a .js file.</span></span> <span data-ttu-id="db42f-306">تقوم هذه التعليمات البرمجية بما يلي:</span><span class="sxs-lookup"><span data-stu-id="db42f-306">This code does the following:</span></span>
    - <span data-ttu-id="db42f-307">إنها تخفي الأعمدة الإضافية المرتبطة بسير العمل التي أضفناها في وقت سابق في صفحة قائمة المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="db42f-308">لقد أضفنا هذه الأعمدة لكي يحصل التطبيق على هذه المعلومات في السياق ولكي يتمكن من القيام بالخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="db42f-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="db42f-309">استنادًا إلى خطوة سير العمل النشط، تطبق هذه التعليمات البرمجية المنطق لإظهار تلك الإجراءات فقط.</span><span class="sxs-lookup"><span data-stu-id="db42f-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db42f-310">يجب أن يكون اسم الصفحات وعناصر التحكم الأخرى الموجودة في التعليمات البرمجية نفسها الأسماء الموجودة في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="db42f-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }
    ```

2.  <span data-ttu-id="db42f-311">تحميل ملف التعليمات البرمجية إلى مساحة العمل عن طريق تحديد علامة التبويب **منطق**</span><span class="sxs-lookup"><span data-stu-id="db42f-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="db42f-312">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="db42f-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="db42f-313">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="db42f-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="db42f-314">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="db42f-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="db42f-315">مرفقات فواتير المورّد</span><span class="sxs-lookup"><span data-stu-id="db42f-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="db42f-316">انقر فوق زر **الإعدادات** (الترس) في الجزء العلوي الأيسر من الصفحة، ثم انقر فوق **تطبيق المحمول**</span><span class="sxs-lookup"><span data-stu-id="db42f-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="db42f-317">انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="db42f-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="db42f-318">حدد صفحة <strong>تفاصيل الفاتورة\*\* التي قمت بإنشائها سابقًا، ثم انقر فوق \*\*تحرير</strong>.</span><span class="sxs-lookup"><span data-stu-id="db42f-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="db42f-319">عيّن الخيار **إدارة المستندات** إلى **نعم** كما هو موضح أدناه.</span><span class="sxs-lookup"><span data-stu-id="db42f-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="db42f-320">**ملاحظة:** في حال عدم وجود أي متطلبات تتعلق بإظهار المرفقات على جهاز محمول، يمكنك ترك هذا الخيار معينًا إلى **لا**، وهو الإعداد الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="db42f-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![إدارة المستندات](./media/docmanagement-216x300.png)

5. <span data-ttu-id="db42f-322">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="db42f-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="db42f-323">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="db42f-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="db42f-324">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="db42f-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="db42f-325">توزيعات بنود فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="db42f-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="db42f-326">تؤكد متطلبات هذا السيناريو أنه سيكون هناك توزيعات على مستوى البنود فقط، وأن الفاتورة ستتضمن بندًا واحدًا فقط في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="db42f-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="db42f-327">ونظرًا لبساطة هذا السيناريو، يجب أن تكون تجربة المستخدم على الجهاز المحمول بسيطة بما يكفي بحيث لن يحتاج المستخدم إلى التنقل لعدة مستويات للأسفل لعرض التوزيعات.</span><span class="sxs-lookup"><span data-stu-id="db42f-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="db42f-328">تتضمن فواتير المورّد خيارًا يسمح بعرض كافة توزيعات من رأس الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="db42f-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="db42f-329">هذه التجربة هي تلك التي نحتاجها لسيناريو المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="db42f-330">ولذلك، سوف نستخدم صفحة **VendMobileInvoiceAllDistributionTree** لتصميم هذا الجزء من سيناريو المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="db42f-331">من شأن معرفة المتطلبات أن يساعدنا على تحديد الصفحة المحددة التي يجب استخدامها وكيفية تحسين تجربة المحمول للمستخدم بدقة عند تصميم السيناريو.</span><span class="sxs-lookup"><span data-stu-id="db42f-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="db42f-332">في السيناريو الثاني، سوف نستخدم صفحة مختلفة لعرض التوزيعات، بسبب اختلاف المتطلبات في ذلك السيناريو.</span><span class="sxs-lookup"><span data-stu-id="db42f-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="db42f-333">استبدل اسم عنصر القائمة في URL، كما فعلت سابقًا.</span><span class="sxs-lookup"><span data-stu-id="db42f-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="db42f-334">يجب أن تشبه الصفحة التي تظهر الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="db42f-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="db42f-335">[![صفحة كافة التوزيعات](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="db42f-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="db42f-336">افتح مصمم المحمول من زر **الإعدادات** (الترس).</span><span class="sxs-lookup"><span data-stu-id="db42f-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="db42f-337">انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="db42f-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="db42f-338">**ملاحظة:** سوف ترى أنه تم إنشاء صفحتين جديدتين تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="db42f-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="db42f-339">يقوم النظام بإنشاء هذه الصفحات نظرًا لتشغيل إدارة المستندات في المقطع السابق.</span><span class="sxs-lookup"><span data-stu-id="db42f-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="db42f-340">يمكنك تجاهل هذه الصفحات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="db42f-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="db42f-341">انقر فوق **إضافة صفحة**.</span><span class="sxs-lookup"><span data-stu-id="db42f-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="db42f-342">أدخل عنوان صفحة، مثل **عرض المحاسبة**، ووصفًا، مثل **عرض المحاسبة للفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="db42f-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="db42f-343">انقر فوق **تم**.</span><span class="sxs-lookup"><span data-stu-id="db42f-343">Click **Done**.</span></span>

7.  <span data-ttu-id="db42f-344">على علامة تبويب **الحقول**، انقر فوق **تحديد حقول**، وحدد الحقول التالية من صفحة التوزيعات وثم انقر فوق **تم**:</span><span class="sxs-lookup"><span data-stu-id="db42f-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="db42f-345">المبلغ</span><span class="sxs-lookup"><span data-stu-id="db42f-345">Amount</span></span>
    2.  <span data-ttu-id="db42f-346">العملة</span><span class="sxs-lookup"><span data-stu-id="db42f-346">Currency</span></span>
    3.  <span data-ttu-id="db42f-347">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="db42f-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="db42f-348">لم نحدد عمود **الوصف** من شبكة التوزيعات، لأن متطلبات هذا السيناريو أكدت أن السعر المفصل هو المبلغ الوحيد الذي سيكون هناك توزيعات له.</span><span class="sxs-lookup"><span data-stu-id="db42f-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="db42f-349">لذلك، لن يحتاج المستخدم إلى حقل آخر لتحديد نوع المبلغ الذي سيكون التوزيع متعلقًا به.</span><span class="sxs-lookup"><span data-stu-id="db42f-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="db42f-350">ومع ذلك، في السيناريو التالي، **سوف** نستخدم هذه المعلومات، لأن متطلبات هذا السيناريو تحدد أن أنواع المبالغ الأخرى لديها توزيعات (على سبيل المثال، ضريبة المبيعات).</span><span class="sxs-lookup"><span data-stu-id="db42f-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="db42f-351">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="db42f-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="db42f-352">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="db42f-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="db42f-353">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="db42f-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="db42f-354">إضافة التنقل إلى صفحة "عرض المحاسبة"</span><span class="sxs-lookup"><span data-stu-id="db42f-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="db42f-355">إن صفحة المحمول **عرض المحاسبة** غير مرتبطة حاليًا بأي من صفحات المحمول التي قمنا بتصميمها حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="db42f-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="db42f-356">بما أنه يتعين على المستخدم أن يكون قادرًا على الانتقال إلى صفحة **عرض المحاسبة** من صفحة **تفاصيل الفاتورة** على الجهاز المحمول، يجب أن نوفر إمكانية التنقل من صفحة **تفاصيل الفاتورة** إلى صفحة **عرض المحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="db42f-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="db42f-357">إننا نستخدم منطقًا إضافيًا عبر JavaScript لتأسيس إمكانية التنقل هذه.</span><span class="sxs-lookup"><span data-stu-id="db42f-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="db42f-358">افتح ملف.js الذي أنشأته مسبقًا، وأضف البنود المميزة في التعليمات البرمجية التالية.</span><span class="sxs-lookup"><span data-stu-id="db42f-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="db42f-359">تقوم هذه التعليمات البرمجية بأمرين:</span><span class="sxs-lookup"><span data-stu-id="db42f-359">This code does two things:</span></span>
    1.  <span data-ttu-id="db42f-360">إنها تساعد على ضمان عدم قدرة المستخدمين على الانتقال مباشرة من مساحة العمل إلى صفحة **عرض المحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="db42f-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="db42f-361">إنها تنشئ عنصر تحكم تنقل من صفحة **تفاصيل الفاتورة** إلى صفحة **عرض المحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="db42f-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="db42f-362">يجب أن يكون اسم الصفحات وعناصر التحكم الأخرى الموجودة في التعليمات البرمجية نفسها الأسماء الموجودة في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="db42f-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }
    ```
    
2.  <span data-ttu-id="db42f-363">تحميل ملف التعليمات البرمجية إلى مساحة العمل عن طريق تحديد علامة التبويب **منطق** للكتابة فوق التعليمات البرمجية السابقة</span><span class="sxs-lookup"><span data-stu-id="db42f-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="db42f-364">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="db42f-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="db42f-365">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="db42f-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="db42f-366">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="db42f-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="db42f-367">التحقق من الصحة</span><span class="sxs-lookup"><span data-stu-id="db42f-367">Validation</span></span>

<span data-ttu-id="db42f-368">من الجهاز المحمول، افتح التطبيق، واتصل بالمثيل الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="db42f-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="db42f-369">تأكد من تسجيل الدخول إلى الشركة حيث تم تعيين لك فواتير المورّد للمراجعة.</span><span class="sxs-lookup"><span data-stu-id="db42f-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="db42f-370">يجب أن تكون قادرًا على تنفيذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="db42f-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="db42f-371">رؤية مساحة عمل **موافقاتي**.</span><span class="sxs-lookup"><span data-stu-id="db42f-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="db42f-372">التنقل في مساحة عمل **موافقاتي** ورؤية صفحة **فواتير المورّد الخاصة بي**.</span><span class="sxs-lookup"><span data-stu-id="db42f-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="db42f-373">التنقل في صفحة **فواتير المورّد الخاصة بي** ورؤية قائمة الفواتير التي تم تعيينها لك.</span><span class="sxs-lookup"><span data-stu-id="db42f-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="db42f-374">التنقل في إحدى الفواتير، ورؤية تفاصيل رأس الفاتورة وتفاصيل البنود.</span><span class="sxs-lookup"><span data-stu-id="db42f-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="db42f-375">في صفحة التفاصيل، رؤية ارتباط إلى المرفقات، واستخدام هذا الارتباط للانتقال إلى قائمة المرفقات وعرض المرفقات.</span><span class="sxs-lookup"><span data-stu-id="db42f-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="db42f-376">في صفحة التفاصيل، رؤية ارتباط إلى صفحة **عرض المحاسبة**، واستخدام هذا الارتباط للانتقال إلى صفحة التوزيعات وعرض التوزيعات.</span><span class="sxs-lookup"><span data-stu-id="db42f-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="db42f-377">في صفحة التفاصيل، النقر فوق قائمة **إجراءات** في الجزء السفلي، وتنفيذ إجراءات سير العمل التي تنطبق على خطوة سير العمل.</span><span class="sxs-lookup"><span data-stu-id="db42f-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="db42f-378">تصميم سيناريو معقد للموافقة على الفواتير لشركة Fabrikam</span><span class="sxs-lookup"><span data-stu-id="db42f-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db42f-379">سمة السيناريو</span><span class="sxs-lookup"><span data-stu-id="db42f-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="db42f-380">الإجابة</span><span class="sxs-lookup"><span data-stu-id="db42f-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db42f-381">ما هي الحقول من رأس الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟</span><span class="sxs-lookup"><span data-stu-id="db42f-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="db42f-382">اسم المورّد</span><span class="sxs-lookup"><span data-stu-id="db42f-382">Vendor name</span></span></li>
<li><span data-ttu-id="db42f-383">مبلغ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-383">Invoice amount</span></span></li>
<li><span data-ttu-id="db42f-384">حساب الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-384">Invoice account</span></span></li>
<li><span data-ttu-id="db42f-385">رقم الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-385">Invoice number</span></span></li>
<li><span data-ttu-id="db42f-386">تاريخ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-386">Invoice date</span></span></li>
<li><span data-ttu-id="db42f-387">وصف الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-387">Invoice description</span></span></li>
<li><span data-ttu-id="db42f-388">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="db42f-388">Due date</span></span></li>
<li><span data-ttu-id="db42f-389">عملة الفاتورة</span><span class="sxs-lookup"><span data-stu-id="db42f-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db42f-390">ما هي الحقول من سطور الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟‬</span><span class="sxs-lookup"><span data-stu-id="db42f-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="db42f-391">فئة التدبير</span><span class="sxs-lookup"><span data-stu-id="db42f-391">Procurement category</span></span></li>
<li><span data-ttu-id="db42f-392">الكمية</span><span class="sxs-lookup"><span data-stu-id="db42f-392">Quantity</span></span></li>
<li><span data-ttu-id="db42f-393">سعر الوحدة</span><span class="sxs-lookup"><span data-stu-id="db42f-393">Unit price</span></span></li>
<li><span data-ttu-id="db42f-394">المبلغ الصافي للسطر</span><span class="sxs-lookup"><span data-stu-id="db42f-394">Line net amount</span></span></li>
<li><span data-ttu-id="db42f-395">مبلغ 1099</span><span class="sxs-lookup"><span data-stu-id="db42f-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db42f-396">ما عدد سطور الفاتورة الموجودة في فاتورة؟</span><span class="sxs-lookup"><span data-stu-id="db42f-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="db42f-397">يمكنك هنا تطبيق القاعدة 80-20، والتحسين إلى 80 في المائة.</span><span class="sxs-lookup"><span data-stu-id="db42f-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="db42f-398">5</span><span class="sxs-lookup"><span data-stu-id="db42f-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db42f-399">هل سيرغب المستخدمون في رؤية التوزيع المحاسبي (أكواد الفواتير) على الجهاز المحمول أثناء المراجعات؟</span><span class="sxs-lookup"><span data-stu-id="db42f-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="db42f-400">نعم</span><span class="sxs-lookup"><span data-stu-id="db42f-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db42f-401">ما عدد التوزيعات المحاسبية (السعر المفصل وضريبة المبيعات والمصاريف وغير ذلك) لبند الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="db42f-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="db42f-402">مرة أخرى، يجب تطبيق القاعدة 80-20.</span><span class="sxs-lookup"><span data-stu-id="db42f-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="db42f-403">السعر المفصل: 2 ضريبة المبيعات: 2 المصروفات: 2</span><span class="sxs-lookup"><span data-stu-id="db42f-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db42f-404">هل تتضمن الفواتير توزيعات محاسبية على رأس الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="db42f-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="db42f-405">إذا كان الأمر كذلك، فيجب أن تكون هذه التوزيعات المحاسبية متوفرة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="db42f-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="db42f-406">غير مستخدم</span><span class="sxs-lookup"><span data-stu-id="db42f-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db42f-407">هل سيحتاج المستخدمون لمشاهدة مرفقات الفاتورة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="db42f-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="db42f-408">نعم</span><span class="sxs-lookup"><span data-stu-id="db42f-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="db42f-409">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="db42f-409">Next steps</span></span>

<span data-ttu-id="db42f-410">يمكن تنفيذ الأشكال المختلفة التالية للسيناريو الأول، استنادًا إلى متطلبات السيناريو الثاني.</span><span class="sxs-lookup"><span data-stu-id="db42f-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="db42f-411">يمكنك استخدام هذا المقطع لتحسين تجربتك في استخدام تطبيقات المحمول.</span><span class="sxs-lookup"><span data-stu-id="db42f-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="db42f-412">نظرًا لتوقع المزيد من بنود الفاتورة في السيناريو 2، تساعد التغييرات التالية على التصميم في تحسين تجربة المستخدم على الجهاز المحمول:</span><span class="sxs-lookup"><span data-stu-id="db42f-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="db42f-413">بدلاً من عرض بنود الفاتورة على صفحة "التفاصيل" (كما في السيناريو 1)، باستطاعة المستخدمين اختيار عرض البنود في صفحة محمول منفصلة.</span><span class="sxs-lookup"><span data-stu-id="db42f-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="db42f-414">نظرً لتوقع أكثر من بند فاتورة في هذا السيناريو، إذا تم استخدام صفحة **VendMobileInvoiceAllDistributionTree** لتصميم صفحة التوزيعات للمحمول (كما في السيناريو 1)، فقد يشكل ربط البنود بالتوزيعات مصدر إرباك للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="db42f-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="db42f-415">ولذلك، استخدم صفحة **VendMobileInvoiceLineDistributionTree‎** لتصميم صفحة التوزيعات.</span><span class="sxs-lookup"><span data-stu-id="db42f-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="db42f-416">ومن الناحية المثالية، ينبغي أن تظهر التوزيعات في سياق بند فاتورة في هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="db42f-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="db42f-417">لذلك، تأكد من أنه باستطاعة المستخدم الانتقال إلى البند لرؤية صفحة التوزيعات.</span><span class="sxs-lookup"><span data-stu-id="db42f-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="db42f-418">استخدم القدرة على ربط الصفحة لتأسيس عملية تنقل، تمامًا كما فعلت للرأس وصفحة التفاصيل في السيناريو 1.</span><span class="sxs-lookup"><span data-stu-id="db42f-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="db42f-419">نظرًا لتوقع أكثر من نوع مبلغ واحد على التوزيعات في السيناريو 2 (رسوم ضريبة المبيعات وغير ذلك)، سيكون من المفيد عرض الوصف الخاص بنوع المبلغ.</span><span class="sxs-lookup"><span data-stu-id="db42f-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="db42f-420">(لقد حذفنا هذه المعلومات في السيناريو 1.)</span><span class="sxs-lookup"><span data-stu-id="db42f-420">(We omitted this information in scenario 1.)</span></span>




