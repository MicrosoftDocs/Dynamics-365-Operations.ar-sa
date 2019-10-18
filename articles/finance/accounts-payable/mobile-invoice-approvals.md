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
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 956c866a6b39e2a81f085910e00d2bfe8683829c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176300"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="556be-103">الموافقة على فاتورة المحمول</span><span class="sxs-lookup"><span data-stu-id="556be-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="556be-104">تسمح قدرات المحمول لمستخدمي الشركات بتصميم تجارب المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="556be-105">للسيناريوهات المتقدمة، يسمح النظام الأساسي أيضًا للمطورين بتوسيع القدرات بحسب رغباتهم.</span><span class="sxs-lookup"><span data-stu-id="556be-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="556be-106">وتُعد أفضل وسيلة للتعرف على بعض المفاهيم الجديدة على المحمول الانتقال عبر عملية تصميم بعض السيناريوهات.</span><span class="sxs-lookup"><span data-stu-id="556be-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="556be-107">يهدف هذا الموضوع إلى توفير نهج عملي لتصميم سيناريوهات المحمول عبر أخذ عمليات الموافقة على فواتير المورّد للمحمول كحالة استخدام.</span><span class="sxs-lookup"><span data-stu-id="556be-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="556be-108">من المفترض أن يساعدك هذا الموضوع على تصميم أشكال مختلفة أخرى للسيناريوهات ويمكن أيضًا تطبيقه على سيناريوهات أخرى لا علاقة لها بفواتير المورّد.</span><span class="sxs-lookup"><span data-stu-id="556be-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="556be-109">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="556be-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="556be-110">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="556be-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="556be-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="556be-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="556be-112">قبل قراءة دليل المحمول</span><span class="sxs-lookup"><span data-stu-id="556be-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="556be-113">النظام الأساسي للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="556be-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="556be-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="556be-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="556be-115">بيئة يتوفر فيها الإصدار 1611 والتحديث الثالث للنظام الأساسي (نوفمبر 2016)</span><span class="sxs-lookup"><span data-stu-id="556be-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="556be-116">تثبيت الإصلاح العاجل KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="556be-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="556be-117">باستطاعة مسجل المهام تسجيل أمري "إغلاق" بطريق الخطأ لمربعات الحوار ذات القوائم المنسدلة المضمنة في التحديث الثالث للنظام الأساسي (تحديث نوفمبر 2016).</span><span class="sxs-lookup"><span data-stu-id="556be-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="556be-118">تثبيت الإصلاح العاجل KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="556be-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="556be-119">يتيح هذا الإصلاح العاجل عرض المرفقات على عميل المحمول المضمن في التحديث الثالث للنظام الأساسي (تحديث نوفمبر 2016).</span><span class="sxs-lookup"><span data-stu-id="556be-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="556be-120">تثبيت الإصلاح العاجل KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="556be-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="556be-121">التعليمات البرمجية للتطبيق لطلب الموافقة على فواتير المورّد على المحمول مضمنة في الإصدار 7.0.1 (مايو 2016).</span><span class="sxs-lookup"><span data-stu-id="556be-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="556be-122">جهاز يعمل بنظام Android أو iOS أو Windows تم فيه تثبيت تطبيق المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="556be-123">البحث عن التطبيق في متجر التطبيقات المناسب.</span><span class="sxs-lookup"><span data-stu-id="556be-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="556be-124">مقدمة</span><span class="sxs-lookup"><span data-stu-id="556be-124">Introduction</span></span>
<span data-ttu-id="556be-125">تتطلب عمليات الموافقة على فواتير المحمول‬ للمورّد الإصلاحات العاجلة الثلاثة الموضحة في قسم "المتطلبات الأساسية‬".</span><span class="sxs-lookup"><span data-stu-id="556be-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="556be-126">لا توفر هذه الإصلاحات العاجلة مساحة عمل لعمليات الموافقة على الفواتير.</span><span class="sxs-lookup"><span data-stu-id="556be-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="556be-127">لمعرفة ما هي مساحة العمل في سياق المحمول، اقرأ دليل المحمول المذكور في قسم "المتطلبات الأساسية‬".</span><span class="sxs-lookup"><span data-stu-id="556be-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="556be-128">يجب تصميم مساحة عمل عمليات الموافقة على الفواتير.</span><span class="sxs-lookup"><span data-stu-id="556be-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="556be-129">تقوم كل مؤسسة بتنظيم وتعريف عمليات الأعمال الخاصة بفواتير المورّد بشكل مختلف.</span><span class="sxs-lookup"><span data-stu-id="556be-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="556be-130">قبل أن تقوم بتصميم تجربة المحمول لعمليات الموافقة على فواتير المورّد، يجب مراعاة الجوانب التالية من عملية الأعمال.</span><span class="sxs-lookup"><span data-stu-id="556be-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="556be-131">ويمكن استخدام نقاط البيانات هذه إلى أقصى حد ممكن لتحسين تجربة المستخدم على الجهاز.</span><span class="sxs-lookup"><span data-stu-id="556be-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="556be-132">ما هي الحقول من رأس الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟</span><span class="sxs-lookup"><span data-stu-id="556be-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="556be-133">ما هي الحقول من سطور الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟‬</span><span class="sxs-lookup"><span data-stu-id="556be-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="556be-134">ما عدد سطور الفاتورة الموجودة في فاتورة؟</span><span class="sxs-lookup"><span data-stu-id="556be-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="556be-135">يمكنك هنا تطبيق القاعدة 80-20، والتحسين إلى 80 في المائة.</span><span class="sxs-lookup"><span data-stu-id="556be-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="556be-136">هل سيرغب المستخدمون في رؤية التوزيع المحاسبي (أكواد الفواتير) على الجهاز المحمول أثناء المراجعات؟</span><span class="sxs-lookup"><span data-stu-id="556be-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="556be-137">إذا كان الجواب على هذا السؤال "نعم"، فعليك أخذ الأسئلة التالية في الاعتبار:</span><span class="sxs-lookup"><span data-stu-id="556be-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="556be-138">ما عدد التوزيعات المحاسبية (السعر المفصل وضريبة المبيعات والمصاريف والتقسيمات وغير ذلك) لبند الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="556be-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="556be-139">مرة أخرى، يجب تطبيق القاعدة 80-20.</span><span class="sxs-lookup"><span data-stu-id="556be-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="556be-140">هل تتضمن الفواتير توزيعات محاسبية على رأس الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="556be-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="556be-141">إذا كان الأمر كذلك، فيجب أن تكون هذه التوزيعات المحاسبية متوفرة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="556be-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="556be-142">لا يفسر هذا الموضوع كيفية تحرير التوزيعات المحاسبية، لأن هذه الوظيفة غير معتمدة حاليًا لسيناريوهات المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="556be-143">هل سيحتاج المستخدمون لمشاهدة مرفقات الفاتورة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="556be-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="556be-144">سوف يختلف تصميم تجربة المحمول لعمليات الموافقة على الفواتير، وفقًا للإجابات على هذه الأسئلة.</span><span class="sxs-lookup"><span data-stu-id="556be-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="556be-145">يهدف ذلك إلى تحسين تجربة المستخدم الخاصة بعملية الأعمال على جهاز محمول في مؤسسة.</span><span class="sxs-lookup"><span data-stu-id="556be-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="556be-146">في بقية هذا الموضوع، سوف ننظر إلى شكلين مختلفين من السيناريوهات يستندان إلى أجوبة مختلفة على الأسئلة السابقة.</span><span class="sxs-lookup"><span data-stu-id="556be-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="556be-147">كتوجيه عام، عندما تعمل مع مصمم المحمول، تأكد من "نشر" التغييرات لتجنب فقدان التحديثات.</span><span class="sxs-lookup"><span data-stu-id="556be-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="556be-148">تصميم سيناريو بسيط للموافقة على الفواتير لشركة Contoso</span><span class="sxs-lookup"><span data-stu-id="556be-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="556be-149">سمة السيناريو</span><span class="sxs-lookup"><span data-stu-id="556be-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="556be-150">الإجابة</span><span class="sxs-lookup"><span data-stu-id="556be-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="556be-151">ما هي الحقول من رأس الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟</span><span class="sxs-lookup"><span data-stu-id="556be-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="556be-152">اسم المورّد</span><span class="sxs-lookup"><span data-stu-id="556be-152">Vendor name</span></span></li>
<li><span data-ttu-id="556be-153">إجمالي الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-153">Invoice total</span></span></li>
<li><span data-ttu-id="556be-154">حساب الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-154">Invoice account</span></span></li>
<li><span data-ttu-id="556be-155">رقم الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-155">Invoice number</span></span></li>
<li><span data-ttu-id="556be-156">تاريخ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-156">Invoice date</span></span></li>
<li><span data-ttu-id="556be-157">وصف الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-157">Invoice description</span></span></li>
<li><span data-ttu-id="556be-158">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="556be-158">Due date</span></span></li>
<li><span data-ttu-id="556be-159">عملة الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="556be-160">ما هي الحقول من سطور الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟‬</span><span class="sxs-lookup"><span data-stu-id="556be-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="556be-161">فئة التدبير</span><span class="sxs-lookup"><span data-stu-id="556be-161">Procurement category</span></span></li>
<li><span data-ttu-id="556be-162">الكمية</span><span class="sxs-lookup"><span data-stu-id="556be-162">Quantity</span></span></li>
<li><span data-ttu-id="556be-163">سعر الوحدة</span><span class="sxs-lookup"><span data-stu-id="556be-163">Unit price</span></span></li>
<li><span data-ttu-id="556be-164">المبلغ الصافي للسطر</span><span class="sxs-lookup"><span data-stu-id="556be-164">Line net amount</span></span></li>
<li><span data-ttu-id="556be-165">مبلغ 1099</span><span class="sxs-lookup"><span data-stu-id="556be-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="556be-166">ما عدد سطور الفاتورة الموجودة في فاتورة؟</span><span class="sxs-lookup"><span data-stu-id="556be-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="556be-167">يمكنك هنا تطبيق القاعدة 80-20، والتحسين إلى 80 في المائة.</span><span class="sxs-lookup"><span data-stu-id="556be-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="556be-168">1</span><span class="sxs-lookup"><span data-stu-id="556be-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="556be-169">هل سيرغب المستخدمون في رؤية التوزيع المحاسبي (أكواد الفواتير) على الجهاز المحمول أثناء المراجعات؟</span><span class="sxs-lookup"><span data-stu-id="556be-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="556be-170">نعم</span><span class="sxs-lookup"><span data-stu-id="556be-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="556be-171">ما عدد التوزيعات المحاسبية (السعر المفصل وضريبة المبيعات والمصاريف وغير ذلك) لبند الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="556be-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="556be-172">مرة أخرى، يجب تطبيق القاعدة 80-20.</span><span class="sxs-lookup"><span data-stu-id="556be-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="556be-173">السعر المفصل: 2 ضريبة المبيعات: 0 المصروفات: 0</span><span class="sxs-lookup"><span data-stu-id="556be-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="556be-174">هل تتضمن الفواتير توزيعات محاسبية على رأس الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="556be-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="556be-175">إذا كان الأمر كذلك، فيجب أن تكون هذه التوزيعات المحاسبية متوفرة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="556be-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="556be-176">غير مستخدم</span><span class="sxs-lookup"><span data-stu-id="556be-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="556be-177">هل سيحتاج المستخدمون لمشاهدة مرفقات الفاتورة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="556be-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="556be-178">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="556be-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="556be-179">إنشاء مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="556be-179">Create the workspace</span></span>

1.  <span data-ttu-id="556be-180">في المستعرض، قم بتسجيل الدخول إلى التطبيق.</span><span class="sxs-lookup"><span data-stu-id="556be-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="556be-181">بعد تسجيل الدخول، قم بإلحاق **&mode=mobile** بعنوان URL كما هو مبين في المثال التالي، وحدّث الصفحة: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="556be-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="556be-182">انقر فوق زر **الإعدادات** (الترس) في الجزء العلوي الأيسر من الصفحة، ثم انقر فوق **تطبيق المحمول**.</span><span class="sxs-lookup"><span data-stu-id="556be-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="556be-183">يجب أن يظهر مصمم التطبيق المحمول تمامًا كما يظهر مسجل المهام.</span><span class="sxs-lookup"><span data-stu-id="556be-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="556be-184">انقر فوق **إضافة** لإنشاء مساحة عمل جديدة.</span><span class="sxs-lookup"><span data-stu-id="556be-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="556be-185">على سبيل المثال، يمكنك تسمية مساحة العمل **موافقاتي**.</span><span class="sxs-lookup"><span data-stu-id="556be-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="556be-186">أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="556be-186">Enter a description.</span></span>
6.  <span data-ttu-id="556be-187">حدد لون مساحة عمل.</span><span class="sxs-lookup"><span data-stu-id="556be-187">Select a workspace color.</span></span> <span data-ttu-id="556be-188">سيتم استخدام لون مساحة العمل للنمط العام لتجربة المحمول لمساحة العمل هذه.</span><span class="sxs-lookup"><span data-stu-id="556be-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="556be-189">حدد أيقونة لمساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="556be-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="556be-190">انقر فوق **تم**</span><span class="sxs-lookup"><span data-stu-id="556be-190">Click **Done**</span></span>
9.  <span data-ttu-id="556be-191">انقر فوق **نشر مساحة العمل** لحفظ التغييرات</span><span class="sxs-lookup"><span data-stu-id="556be-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="556be-192">فواتير المورَّد المعينة إلي</span><span class="sxs-lookup"><span data-stu-id="556be-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="556be-193">صفحة المحمول الأولى التي يجب تصميمها هي قائمة الفواتير التي تم تعيينها للمستخدم لكي يراجعها.</span><span class="sxs-lookup"><span data-stu-id="556be-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="556be-194">لتصميم صفحة المحمول هذه استخدم الصفحة **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="556be-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="556be-195">قبل إكمال هذا الإجراء، تأكد من تعيين فاتورة مورّد واحد على الأقل لك للمراجعة، ومن وجود توزيعين لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="556be-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="556be-196">هذا الإعداد يفي بمتطلبات هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="556be-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="556be-197">في عنوان URL، استبدل اسم عنصر القائمة بالاسم **VendMobileInvoiceAssignedToMeListPage** لفتح إصدار المحمول لصفحة القائمة **فواتير المورّد المعلقة المعينة إليّ‬** في وحدة **الحسابات الدائنة**.</span><span class="sxs-lookup"><span data-stu-id="556be-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="556be-198">بحسب عدد الفواتير المعينة لك في النظام، ستعرض هذه الصفحة تلك الفواتير.</span><span class="sxs-lookup"><span data-stu-id="556be-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="556be-199">للبحث عن فاتورة معينة، يمكنك استخدام عامل التصفية إلى اليمين.</span><span class="sxs-lookup"><span data-stu-id="556be-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="556be-200">ومع ذلك، لا نحتاج إلى فاتورة معينة لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="556be-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="556be-201">نحن نحتاج فقط إلى فاتورة معينة لك سوف تسمح لك بتصميم صفحة المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="556be-202">تم تصميم الصفحات الجديدة المتوفرة خصيصًا لتطوير سيناريوهات المحمول لفاتورة المورّد.</span><span class="sxs-lookup"><span data-stu-id="556be-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="556be-203">ولذلك، يجب استخدام هذه الصفحات.</span><span class="sxs-lookup"><span data-stu-id="556be-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="556be-204">يجب أن يكون عنوان URL مماثلاً لعنوان URL التالي، وبعد إدخاله، يجب أن تظهر الصفحة المعروضة في الشكل التوضيحي: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![ فواتير المورّد المعلقة المعينة إليّ](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="556be-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="556be-205">انقر فوق زر **الإعدادات** (الترس) في الجزء العلوي الأيسر من الصفحة، ثم انقر فوق **تطبيق المحمول**</span><span class="sxs-lookup"><span data-stu-id="556be-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="556be-206">حدد مساحة العمل، ثم انقر فوق **تحرير**</span><span class="sxs-lookup"><span data-stu-id="556be-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="556be-207">انقر فوق **صفحة إضافة** لإنشاء صفحة المحمول الأولى.</span><span class="sxs-lookup"><span data-stu-id="556be-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="556be-208">أدخل اسمًا، مثل **فواتير المورّد الخاصة بي**، ووصفًا، مثل **فواتير المورّد المعينة إليّ للمراجعة**.</span><span class="sxs-lookup"><span data-stu-id="556be-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="556be-209">انقر فوق **تم‏‎**.</span><span class="sxs-lookup"><span data-stu-id="556be-209">Click **Done**.</span></span>
7.  <span data-ttu-id="556be-210">في مصمم المحمول، على علامة تبويب **الحقول**، انقر فوق **تحديد الحقول‬**.</span><span class="sxs-lookup"><span data-stu-id="556be-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="556be-211">يجب أن تكون الأعمدة في صفحة القائمة مماثلة للشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="556be-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="556be-212">[![أعمدة على صفحة فواتير المورّد المعلقة المعينة إليّ‬](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="556be-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="556be-213">أضف الأعمدة المطلوبة من صفحة القائمة التي يجب أن تظهر للمستخدم في صفحة المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="556be-214">الترتيب الذي تستخدمه لإضافة الأعمدة هو الترتيب الذي ستظهر فيه الحقول للمستخدم النهائي.</span><span class="sxs-lookup"><span data-stu-id="556be-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="556be-215">الطريقة الوحيدة لتغيير ترتيب حقول هي إعادة تحديد كافة الحقول.</span><span class="sxs-lookup"><span data-stu-id="556be-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="556be-216">استنادًا إلى متطلبات هذا السيناريو، تعتبر الحقول الثمانية التالية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="556be-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="556be-217">ومع ذلك، قد يجد بعض المستخدمين أن الحقول الثمانية تشكل كمية كبيرة جدًا من المعلومات على جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="556be-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="556be-218">ولذلك، سنعرض أهم الحقول فقط في طريقة عرض قائمة المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="556be-219">وستظهر الحقول المتبقية في طريقة عرض التفاصيل التي سوف نصممها لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="556be-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="556be-220">الآن، سوف نقوم بإضافة الحقول التالية.</span><span class="sxs-lookup"><span data-stu-id="556be-220">For now, we will add the following fields.</span></span> <span data-ttu-id="556be-221">انقر فوق علامة الجمع (**+**) في هذه الأعمدة لإضافتها إلى صفحة المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="556be-222">اسم المورّد</span><span class="sxs-lookup"><span data-stu-id="556be-222">Vendor name</span></span>
    - <span data-ttu-id="556be-223">إجمالي الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-223">Invoice total</span></span>
    - <span data-ttu-id="556be-224">حساب الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-224">Invoice account</span></span>
    - <span data-ttu-id="556be-225">رقم الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-225">Invoice number</span></span>
    - <span data-ttu-id="556be-226">تاريخ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-226">Invoice date</span></span>

    <span data-ttu-id="556be-227">بعد إضافة الحقول، يجب أن تشبه صفحة المحمول الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="556be-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="556be-228">[![الصفحة بعد إضافة الحقول](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="556be-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="556be-229">يجب أيضًا إضافة الأعمدة التالية الآن، من أجل تمكين إجراءات سير العمل فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="556be-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="556be-230">إظهار المهمة المكتملة</span><span class="sxs-lookup"><span data-stu-id="556be-230">Show complete task</span></span>
    - <span data-ttu-id="556be-231">إظهار تفويض المهمة</span><span class="sxs-lookup"><span data-stu-id="556be-231">Show delegate task</span></span>
    - <span data-ttu-id="556be-232">إظهار استدعاء المهمة</span><span class="sxs-lookup"><span data-stu-id="556be-232">Show recall task</span></span>
    - <span data-ttu-id="556be-233">إظهار رفض المهمة</span><span class="sxs-lookup"><span data-stu-id="556be-233">Show reject task</span></span>
    - <span data-ttu-id="556be-234">إظهار طلب إكمال المهمة</span><span class="sxs-lookup"><span data-stu-id="556be-234">Show request completion task</span></span>
    - <span data-ttu-id="556be-235">إظهار إعادة إرسال المهمة</span><span class="sxs-lookup"><span data-stu-id="556be-235">Show resubmit task</span></span>

10. <span data-ttu-id="556be-236">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="556be-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="556be-237">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="556be-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="556be-238">انقر فوق **نشر مساحة العمل** لحفظ عملك.</span><span class="sxs-lookup"><span data-stu-id="556be-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="556be-239">قم بتمكين **عرض إجماليات الفاتورة على قائمة فواتير المورد المعلقة‬** في معلمات الحسابات الدائنة ضمن **الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="556be-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="556be-240">تجدر الإشارة إلى أنه فقط من خلال تمكين هذه المعلمة، سيتم حساب إجماليات الفواتير لعرضها في صفحة قائمة فواتير المورد المعلقة.</span><span class="sxs-lookup"><span data-stu-id="556be-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="556be-241">هذه قدرة جديدة كجزء من الإصلاح العاجل 3208224 ضمن المتطلبات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="556be-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="556be-242">تفصيل فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="556be-242">Vendor invoice details</span></span>

<span data-ttu-id="556be-243">لتصميم صفحة تفاصيل الفاتورة للمحمول، استخدم الصفحة **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="556be-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="556be-244">لاحظ أنه، استنادًا إلى عدد الفواتير في النظام، تعرض هذه الصفحة الفواتير الأقدم (الفاتورة التي تم إنشاؤها أولاً).</span><span class="sxs-lookup"><span data-stu-id="556be-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="556be-245">للبحث عن فاتورة معينة، يمكنك استخدام عامل التصفية إلى اليمين.</span><span class="sxs-lookup"><span data-stu-id="556be-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="556be-246">ومع ذلك، لا نحتاج إلى فاتورة معينة لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="556be-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="556be-247">نحن نطلب فقط بعض بيانات الفاتورة لكي نتمكن من تصميم صفحة المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="556be-248">[![صفحة سير العمل](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="556be-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="556be-249">في عنوان URL، استبدل اسم عنصر القائمة بالاسم **VendMobileInvoiceHeaderDetails** لفتح النموذج</span><span class="sxs-lookup"><span data-stu-id="556be-249">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2. <span data-ttu-id="556be-250">افتح مصمم المحمول من زر **الإعدادات** (الترس).</span><span class="sxs-lookup"><span data-stu-id="556be-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3. <span data-ttu-id="556be-251">انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="556be-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4. <span data-ttu-id="556be-252">حدد صفحة **فواتير المورّد الخاصة بي** التي قمت بإنشائها سابقًا، ثم انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="556be-252">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>
5. <span data-ttu-id="556be-253">على علامة تبويب **الحقول**، انقر فوق عنوان العمود **الشبكة**.</span><span class="sxs-lookup"><span data-stu-id="556be-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6. <span data-ttu-id="556be-254">انقر فوق **‎خصائص &gt; إضافة صفحة**.</span><span class="sxs-lookup"><span data-stu-id="556be-254">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="556be-255">**ملاحظة:** عندما تنقر فوق العنوان **الشبكة** وتضيف صفحة، تتأسس العلاقة مع صفحة التفاصيل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="556be-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7. <span data-ttu-id="556be-256">أدخل عنوان صفحة، مثل **تفاصيل الفاتورة**، ووصفًا، مثل **عرض رأس الفاتورة وتفاصيل البنود**.</span><span class="sxs-lookup"><span data-stu-id="556be-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8. <span data-ttu-id="556be-257">انقر فوق **تحديد الحقول**.</span><span class="sxs-lookup"><span data-stu-id="556be-257">Click **Select fields**.</span></span> <span data-ttu-id="556be-258">لاحظ أن الترتيب الذي تستخدمه لإضافة الأعمدة هو الترتيب الذي ستظهر فيه الحقول للمستخدم النهائي.</span><span class="sxs-lookup"><span data-stu-id="556be-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="556be-259">الطريقة الوحيدة لتغيير ترتيب حقول هي إعادة تحديد كافة الحقول.</span><span class="sxs-lookup"><span data-stu-id="556be-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9. <span data-ttu-id="556be-260">أضف الحقول التالية من الرأس، استنادًا إلى متطلبات هذا السيناريو:</span><span class="sxs-lookup"><span data-stu-id="556be-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="556be-261">اسم المورّد</span><span class="sxs-lookup"><span data-stu-id="556be-261">Vendor name</span></span>
   - <span data-ttu-id="556be-262">إجمالي الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-262">Invoice total</span></span>
   - <span data-ttu-id="556be-263">حساب الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-263">Invoice account</span></span>
   - <span data-ttu-id="556be-264">رقم الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-264">Invoice number</span></span>
   - <span data-ttu-id="556be-265">تاريخ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-265">Invoice date</span></span>
   - <span data-ttu-id="556be-266">وصف الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-266">Invoice description</span></span>
   - <span data-ttu-id="556be-267">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="556be-267">Due date</span></span>
   - <span data-ttu-id="556be-268">عملة الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-268">Invoice currency</span></span>

10. <span data-ttu-id="556be-269">أضف الحقول التالية من خطوط الشبكة في الصفحة:</span><span class="sxs-lookup"><span data-stu-id="556be-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="556be-270">فئة التدبير</span><span class="sxs-lookup"><span data-stu-id="556be-270">Procurement category</span></span>
    - <span data-ttu-id="556be-271">الكمية</span><span class="sxs-lookup"><span data-stu-id="556be-271">Quantity</span></span>
    - <span data-ttu-id="556be-272">سعر الوحدة</span><span class="sxs-lookup"><span data-stu-id="556be-272">Unit price</span></span>
    - <span data-ttu-id="556be-273">المبلغ الصافي للسطر</span><span class="sxs-lookup"><span data-stu-id="556be-273">Line net amount</span></span>
    - <span data-ttu-id="556be-274">مبلغ 1099</span><span class="sxs-lookup"><span data-stu-id="556be-274">1099 amount</span></span>

11. <span data-ttu-id="556be-275">بعد إضافة كافة الحقول من الخطوتين السابقتين، انقر فوق **تم**.</span><span class="sxs-lookup"><span data-stu-id="556be-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="556be-276">يجب أن تكون الصفحة مماثلة للشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="556be-276">The page must resemble the following illustration.</span></span>
    <span data-ttu-id="556be-277">[![الصفحة بعد إضافة الحقول](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="556be-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="556be-278">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="556be-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="556be-279">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="556be-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="556be-280">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="556be-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="556be-281">إجراءات سير العمل</span><span class="sxs-lookup"><span data-stu-id="556be-281">Workflow actions</span></span>

<span data-ttu-id="556be-282">لإضافة إجراءات سير العمل، استخدم صفحة **VendMobileInvoiceHeaderDetails**. </span><span class="sxs-lookup"><span data-stu-id="556be-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="556be-283">لفتح هذه الصفحة، استبدل اسم عنصر القائمة في URL، كما فعلت سابقًا.</span><span class="sxs-lookup"><span data-stu-id="556be-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="556be-284">ثم افتح مصمم المحمول من زر **الإعدادات** (الترس).</span><span class="sxs-lookup"><span data-stu-id="556be-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="556be-285">اتبع هذه الخطوات لإضافة إجراءات سير العمل في صفحة التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="556be-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="556be-286">من الضروري أن تكون الفواتير المعينة لك في الحالة المناسبة التي تسمح بجعل إجراءات سير العمل التي ستعمل على تصميمها متوفرة لك.</span><span class="sxs-lookup"><span data-stu-id="556be-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="556be-287">تسجيل إجراءات سير العمل</span><span class="sxs-lookup"><span data-stu-id="556be-287">Record workflow actions</span></span>
1.  <span data-ttu-id="556be-288">انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="556be-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="556be-289">حدد صفحة **تفاصيل الفاتورة** التي قمت بإنشائها سابقًا، ومن ثم انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="556be-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="556be-290">على علامة تبويب **الإجراءات**، انقر فوق **إضافة إجراء**.</span><span class="sxs-lookup"><span data-stu-id="556be-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="556be-291">أدخل عنوان إجراء، مثل **الموافقة**، ووصفًا، مثل **الموافقة على الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="556be-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="556be-292">لاحظ أن عنوان الإجراء الذي تدخله هنا يصبح اسم الإجراء الذي يظهر للمستخدم في تطبيق المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="556be-293">انقر فوق **تم**.</span><span class="sxs-lookup"><span data-stu-id="556be-293">Click **Done**.</span></span>
6.  <span data-ttu-id="556be-294">انقر فوق **تحديد الحقول**.</span><span class="sxs-lookup"><span data-stu-id="556be-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="556be-295">انتقل عبر عملية سير العمل في صفحة **VendMobileInvoiceHeaderDetails‎**، وأكمل الإجراء الذي تريد تسجيله.</span><span class="sxs-lookup"><span data-stu-id="556be-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="556be-296">تأكد من إدخال تعليقات سير العمل أثناء هذه العملية، بحيث يتم أيضًا تضمين حقل تعليقات في تجربة المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="556be-297">بعد أن يتم تشغيل إجراء سير العمل، انقر فوق **تم** لإكمال مهمة تحديد الحقول.</span><span class="sxs-lookup"><span data-stu-id="556be-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="556be-298">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="556be-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="556be-299">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="556be-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="556be-300">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="556be-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="556be-301">كرر الخطوات السابقة لتسجيل كافة إجراءات سير العمل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="556be-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="556be-302">إنشاء ملف .js</span><span class="sxs-lookup"><span data-stu-id="556be-302">Create a .js file</span></span>
1. <span data-ttu-id="556be-303">افتح المفكرة أو Microsoft Visual Studio، ثم الصق التعليمات البرمجية التالية.</span><span class="sxs-lookup"><span data-stu-id="556be-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="556be-304">احفظ الملف بصيغة ملف .js.</span><span class="sxs-lookup"><span data-stu-id="556be-304">Save the file as a .js file.</span></span> <span data-ttu-id="556be-305">تقوم هذه التعليمات البرمجية بما يلي:</span><span class="sxs-lookup"><span data-stu-id="556be-305">This code does the following:</span></span>
    - <span data-ttu-id="556be-306">إنها تخفي الأعمدة الإضافية المرتبطة بسير العمل التي أضفناها في وقت سابق في صفحة قائمة المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="556be-307">لقد أضفنا هذه الأعمدة لكي يحصل التطبيق على هذه المعلومات في السياق ولكي يتمكن من القيام بالخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="556be-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="556be-308">استنادًا إلى خطوة سير العمل النشط، تطبق هذه التعليمات البرمجية المنطق لإظهار تلك الإجراءات فقط.</span><span class="sxs-lookup"><span data-stu-id="556be-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="556be-309">يجب أن يكون اسم الصفحات وعناصر التحكم الأخرى الموجودة في التعليمات البرمجية نفسها الأسماء الموجودة في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="556be-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="556be-310">تحميل ملف التعليمات البرمجية إلى مساحة العمل عن طريق تحديد علامة التبويب **منطق**</span><span class="sxs-lookup"><span data-stu-id="556be-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="556be-311">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="556be-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="556be-312">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="556be-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="556be-313">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="556be-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="556be-314">مرفقات فواتير المورّد</span><span class="sxs-lookup"><span data-stu-id="556be-314">Vendor invoice attachments</span></span>

1. <span data-ttu-id="556be-315">انقر فوق زر **الإعدادات** (الترس) في الجزء العلوي الأيسر من الصفحة، ثم انقر فوق **تطبيق المحمول**</span><span class="sxs-lookup"><span data-stu-id="556be-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2. <span data-ttu-id="556be-316">انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="556be-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3. <span data-ttu-id="556be-317">حدد صفحة <strong>تفاصيل الفاتورة\*\* التي قمت بإنشائها سابقًا، ثم انقر فوق \*\*تحرير</strong>.</span><span class="sxs-lookup"><span data-stu-id="556be-317">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>
4. <span data-ttu-id="556be-318">عيّن الخيار **إدارة المستندات** إلى **نعم** كما هو موضح أدناه.</span><span class="sxs-lookup"><span data-stu-id="556be-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="556be-319">**ملاحظة:** في حال عدم وجود أي متطلبات تتعلق بإظهار المرفقات على جهاز محمول، يمكنك ترك هذا الخيار معينًا إلى **لا**، وهو الإعداد الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="556be-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   <span data-ttu-id="556be-320">![إدارة المستندات](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="556be-320">![Document management](./media/docmanagement-216x300.png)</span></span>
5. <span data-ttu-id="556be-321">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="556be-321">Click **Done** to exit edit mode.</span></span>
6. <span data-ttu-id="556be-322">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="556be-322">Click **Back** and then **Done** to exit the workspace</span></span>
7. <span data-ttu-id="556be-323">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="556be-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="556be-324">توزيعات بنود فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="556be-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="556be-325">تؤكد متطلبات هذا السيناريو أنه سيكون هناك توزيعات على مستوى البنود فقط، وأن الفاتورة ستتضمن بندًا واحدًا فقط في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="556be-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="556be-326">ونظرًا لبساطة هذا السيناريو، يجب أن تكون تجربة المستخدم على الجهاز المحمول بسيطة بما يكفي بحيث لن يحتاج المستخدم إلى التنقل لعدة مستويات للأسفل لعرض التوزيعات.</span><span class="sxs-lookup"><span data-stu-id="556be-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="556be-327">تتضمن فواتير المورّد خيارًا يسمح بعرض كافة توزيعات من رأس الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="556be-327">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="556be-328">هذه التجربة هي تلك التي نحتاجها لسيناريو المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="556be-329">ولذلك، سوف نستخدم صفحة **VendMobileInvoiceAllDistributionTree** لتصميم هذا الجزء من سيناريو المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="556be-330">من شأن معرفة المتطلبات أن يساعدنا على تحديد الصفحة المحددة التي يجب استخدامها وكيفية تحسين تجربة المحمول للمستخدم بدقة عند تصميم السيناريو.</span><span class="sxs-lookup"><span data-stu-id="556be-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="556be-331">في السيناريو الثاني، سوف نستخدم صفحة مختلفة لعرض التوزيعات، بسبب اختلاف المتطلبات في ذلك السيناريو.</span><span class="sxs-lookup"><span data-stu-id="556be-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="556be-332">استبدل اسم عنصر القائمة في URL، كما فعلت سابقًا.</span><span class="sxs-lookup"><span data-stu-id="556be-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="556be-333">يجب أن تشبه الصفحة التي تظهر الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="556be-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="556be-334">[![صفحة كافة التوزيعات](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="556be-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="556be-335">افتح مصمم المحمول من زر **الإعدادات** (الترس).</span><span class="sxs-lookup"><span data-stu-id="556be-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="556be-336">انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="556be-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="556be-337">**ملاحظة:** سوف ترى أنه تم إنشاء صفحتين جديدتين تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="556be-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="556be-338">يقوم النظام بإنشاء هذه الصفحات نظرًا لتشغيل إدارة المستندات في المقطع السابق.</span><span class="sxs-lookup"><span data-stu-id="556be-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="556be-339">يمكنك تجاهل هذه الصفحات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="556be-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="556be-340">انقر فوق **إضافة صفحة**.</span><span class="sxs-lookup"><span data-stu-id="556be-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="556be-341">أدخل عنوان صفحة، مثل **عرض المحاسبة**، ووصفًا، مثل **عرض المحاسبة للفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="556be-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="556be-342">انقر فوق **تم**.</span><span class="sxs-lookup"><span data-stu-id="556be-342">Click **Done**.</span></span>
7.  <span data-ttu-id="556be-343">على علامة تبويب **الحقول**، انقر فوق **تحديد حقول**، وحدد الحقول التالية من صفحة التوزيعات وثم انقر فوق **تم**:</span><span class="sxs-lookup"><span data-stu-id="556be-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="556be-344">المبلغ</span><span class="sxs-lookup"><span data-stu-id="556be-344">Amount</span></span>
    2.  <span data-ttu-id="556be-345">العملة</span><span class="sxs-lookup"><span data-stu-id="556be-345">Currency</span></span>
    3.  <span data-ttu-id="556be-346">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="556be-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="556be-347">لم نحدد عمود **الوصف** من شبكة التوزيعات، لأن متطلبات هذا السيناريو أكدت أن السعر المفصل هو المبلغ الوحيد الذي سيكون هناك توزيعات له.</span><span class="sxs-lookup"><span data-stu-id="556be-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="556be-348">لذلك، لن يحتاج المستخدم إلى حقل آخر لتحديد نوع المبلغ الذي سيكون التوزيع متعلقًا به.</span><span class="sxs-lookup"><span data-stu-id="556be-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="556be-349">ومع ذلك، في السيناريو التالي، **سوف** نستخدم هذه المعلومات، لأن متطلبات هذا السيناريو تحدد أن أنواع المبالغ الأخرى لديها توزيعات (على سبيل المثال، ضريبة المبيعات).</span><span class="sxs-lookup"><span data-stu-id="556be-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="556be-350">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="556be-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="556be-351">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="556be-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="556be-352">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="556be-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="556be-353">إن صفحة المحمول **عرض المحاسبة** غير مرتبطة حاليًا بأي من صفحات المحمول التي قمنا بتصميمها حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="556be-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="556be-354">بما أنه يتعين على المستخدم أن يكون قادرًا على الانتقال إلى صفحة **عرض المحاسبة** من صفحة **تفاصيل الفاتورة** على الجهاز المحمول، يجب أن نوفر إمكانية التنقل من صفحة **تفاصيل الفاتورة** إلى صفحة **عرض المحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="556be-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="556be-355">إننا نستخدم منطقًا إضافيًا عبر JavaScript لتأسيس إمكانية التنقل هذه.</span><span class="sxs-lookup"><span data-stu-id="556be-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="556be-356">افتح ملف.js الذي أنشأته مسبقًا، وأضف البنود المميزة في التعليمات البرمجية التالية.</span><span class="sxs-lookup"><span data-stu-id="556be-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="556be-357">تقوم هذه التعليمات البرمجية بأمرين:</span><span class="sxs-lookup"><span data-stu-id="556be-357">This code does two things:</span></span>
    1.  <span data-ttu-id="556be-358">إنها تساعد على ضمان عدم قدرة المستخدمين على الانتقال مباشرة من مساحة العمل إلى صفحة **عرض المحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="556be-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="556be-359">إنها تنشئ عنصر تحكم تنقل من صفحة **تفاصيل الفاتورة** إلى صفحة **عرض المحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="556be-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="556be-360">يجب أن يكون اسم الصفحات وعناصر التحكم الأخرى الموجودة في التعليمات البرمجية نفسها الأسماء الموجودة في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="556be-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="556be-361">تحميل ملف التعليمات البرمجية إلى مساحة العمل عن طريق تحديد علامة التبويب **منطق** للكتابة فوق التعليمات البرمجية السابقة</span><span class="sxs-lookup"><span data-stu-id="556be-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="556be-362">انقر فوق **تم** لإنهاء وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="556be-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="556be-363">انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل</span><span class="sxs-lookup"><span data-stu-id="556be-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="556be-364">انقر فوق **نشر مساحة العمل** لحفظ عملك</span><span class="sxs-lookup"><span data-stu-id="556be-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="556be-365">التحقق من الصحة</span><span class="sxs-lookup"><span data-stu-id="556be-365">Validation</span></span>

<span data-ttu-id="556be-366">من الجهاز المحمول، افتح التطبيق، واتصل بالمثيل الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="556be-366">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="556be-367">تأكد من تسجيل الدخول إلى الشركة حيث تم تعيين لك فواتير المورّد للمراجعة.</span><span class="sxs-lookup"><span data-stu-id="556be-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="556be-368">يجب أن تكون قادرًا على تنفيذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="556be-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="556be-369">رؤية مساحة عمل **موافقاتي**.</span><span class="sxs-lookup"><span data-stu-id="556be-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="556be-370">التنقل في مساحة عمل **موافقاتي** ورؤية صفحة **فواتير المورّد الخاصة بي**.</span><span class="sxs-lookup"><span data-stu-id="556be-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="556be-371">التنقل في صفحة **فواتير المورّد الخاصة بي** ورؤية قائمة الفواتير التي تم تعيينها لك.</span><span class="sxs-lookup"><span data-stu-id="556be-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="556be-372">التنقل في إحدى الفواتير، ورؤية تفاصيل رأس الفاتورة وتفاصيل البنود.</span><span class="sxs-lookup"><span data-stu-id="556be-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="556be-373">في صفحة التفاصيل، رؤية ارتباط إلى المرفقات، واستخدام هذا الارتباط للانتقال إلى قائمة المرفقات وعرض المرفقات.</span><span class="sxs-lookup"><span data-stu-id="556be-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="556be-374">في صفحة التفاصيل، رؤية ارتباط إلى صفحة **عرض المحاسبة**، واستخدام هذا الارتباط للانتقال إلى صفحة التوزيعات وعرض التوزيعات.</span><span class="sxs-lookup"><span data-stu-id="556be-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="556be-375">في صفحة التفاصيل، النقر فوق قائمة **إجراءات** في الجزء السفلي، وتنفيذ إجراءات سير العمل التي تنطبق على خطوة سير العمل.</span><span class="sxs-lookup"><span data-stu-id="556be-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="556be-376">تصميم سيناريو معقد للموافقة على الفواتير لشركة Fabrikam</span><span class="sxs-lookup"><span data-stu-id="556be-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="556be-377">سمة السيناريو</span><span class="sxs-lookup"><span data-stu-id="556be-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="556be-378">الإجابة</span><span class="sxs-lookup"><span data-stu-id="556be-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="556be-379">ما هي الحقول من رأس الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟</span><span class="sxs-lookup"><span data-stu-id="556be-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="556be-380">اسم المورّد</span><span class="sxs-lookup"><span data-stu-id="556be-380">Vendor name</span></span></li>
<li><span data-ttu-id="556be-381">مبلغ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-381">Invoice amount</span></span></li>
<li><span data-ttu-id="556be-382">حساب الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-382">Invoice account</span></span></li>
<li><span data-ttu-id="556be-383">رقم الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-383">Invoice number</span></span></li>
<li><span data-ttu-id="556be-384">تاريخ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-384">Invoice date</span></span></li>
<li><span data-ttu-id="556be-385">وصف الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-385">Invoice description</span></span></li>
<li><span data-ttu-id="556be-386">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="556be-386">Due date</span></span></li>
<li><span data-ttu-id="556be-387">عملة الفاتورة</span><span class="sxs-lookup"><span data-stu-id="556be-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="556be-388">ما هي الحقول من سطور الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟‬</span><span class="sxs-lookup"><span data-stu-id="556be-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="556be-389">فئة التدبير</span><span class="sxs-lookup"><span data-stu-id="556be-389">Procurement category</span></span></li>
<li><span data-ttu-id="556be-390">الكمية</span><span class="sxs-lookup"><span data-stu-id="556be-390">Quantity</span></span></li>
<li><span data-ttu-id="556be-391">سعر الوحدة</span><span class="sxs-lookup"><span data-stu-id="556be-391">Unit price</span></span></li>
<li><span data-ttu-id="556be-392">المبلغ الصافي للسطر</span><span class="sxs-lookup"><span data-stu-id="556be-392">Line net amount</span></span></li>
<li><span data-ttu-id="556be-393">مبلغ 1099</span><span class="sxs-lookup"><span data-stu-id="556be-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="556be-394">ما عدد سطور الفاتورة الموجودة في فاتورة؟</span><span class="sxs-lookup"><span data-stu-id="556be-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="556be-395">يمكنك هنا تطبيق القاعدة 80-20، والتحسين إلى 80 في المائة.</span><span class="sxs-lookup"><span data-stu-id="556be-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="556be-396">5</span><span class="sxs-lookup"><span data-stu-id="556be-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="556be-397">هل سيرغب المستخدمون في رؤية التوزيع المحاسبي (أكواد الفواتير) على الجهاز المحمول أثناء المراجعات؟</span><span class="sxs-lookup"><span data-stu-id="556be-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="556be-398">نعم</span><span class="sxs-lookup"><span data-stu-id="556be-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="556be-399">ما عدد التوزيعات المحاسبية (السعر المفصل وضريبة المبيعات والمصاريف وغير ذلك) لبند الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="556be-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="556be-400">مرة أخرى، يجب تطبيق القاعدة 80-20.</span><span class="sxs-lookup"><span data-stu-id="556be-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="556be-401">السعر المفصل: 2 ضريبة المبيعات: 2 المصروفات: 2</span><span class="sxs-lookup"><span data-stu-id="556be-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="556be-402">هل تتضمن الفواتير توزيعات محاسبية على رأس الفاتورة؟</span><span class="sxs-lookup"><span data-stu-id="556be-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="556be-403">إذا كان الأمر كذلك، فيجب أن تكون هذه التوزيعات المحاسبية متوفرة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="556be-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="556be-404">غير مستخدم</span><span class="sxs-lookup"><span data-stu-id="556be-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="556be-405">هل سيحتاج المستخدمون لمشاهدة مرفقات الفاتورة على الجهاز؟</span><span class="sxs-lookup"><span data-stu-id="556be-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="556be-406">نعم</span><span class="sxs-lookup"><span data-stu-id="556be-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="556be-407">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="556be-407">Next steps</span></span>

<span data-ttu-id="556be-408">يمكن تنفيذ الأشكال المختلفة التالية للسيناريو الأول، استنادًا إلى متطلبات السيناريو الثاني.</span><span class="sxs-lookup"><span data-stu-id="556be-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="556be-409">يمكنك استخدام هذا المقطع لتحسين تجربتك في استخدام تطبيقات المحمول.</span><span class="sxs-lookup"><span data-stu-id="556be-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="556be-410">نظرًا لتوقع المزيد من بنود الفاتورة في السيناريو 2، تساعد التغييرات التالية على التصميم في تحسين تجربة المستخدم على الجهاز المحمول:</span><span class="sxs-lookup"><span data-stu-id="556be-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="556be-411">بدلاً من عرض بنود الفاتورة على صفحة "التفاصيل" (كما في السيناريو 1)، باستطاعة المستخدمين اختيار عرض البنود في صفحة محمول منفصلة.</span><span class="sxs-lookup"><span data-stu-id="556be-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="556be-412">نظرً لتوقع أكثر من بند فاتورة في هذا السيناريو، إذا تم استخدام صفحة **VendMobileInvoiceAllDistributionTree** لتصميم صفحة التوزيعات للمحمول (كما في السيناريو 1)، فقد يشكل ربط البنود بالتوزيعات مصدر إرباك للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="556be-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="556be-413">ولذلك، استخدم صفحة **VendMobileInvoiceLineDistributionTree‎** لتصميم صفحة التوزيعات.</span><span class="sxs-lookup"><span data-stu-id="556be-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="556be-414">ومن الناحية المثالية، ينبغي أن تظهر التوزيعات في سياق بند فاتورة في هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="556be-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="556be-415">لذلك، تأكد من أنه باستطاعة المستخدم الانتقال إلى البند لرؤية صفحة التوزيعات.</span><span class="sxs-lookup"><span data-stu-id="556be-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="556be-416">استخدم القدرة على ربط الصفحة لتأسيس عملية تنقل، تمامًا كما فعلت للرأس وصفحة التفاصيل في السيناريو 1.</span><span class="sxs-lookup"><span data-stu-id="556be-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="556be-417">نظرًا لتوقع أكثر من نوع مبلغ واحد على التوزيعات في السيناريو 2 (رسوم ضريبة المبيعات وغير ذلك)، سيكون من المفيد عرض الوصف الخاص بنوع المبلغ.</span><span class="sxs-lookup"><span data-stu-id="556be-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="556be-418">(لقد حذفنا هذه المعلومات في السيناريو 1.)</span><span class="sxs-lookup"><span data-stu-id="556be-418">(We omitted this information in scenario 1.)</span></span>




