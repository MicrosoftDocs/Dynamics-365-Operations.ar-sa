---
title: "مساحة العمل المحمولة الموافقات على الفواتير‬"
description: "يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة \"الموافقات على الفواتير‬‬\". توفر مساحة العمل المحمولة قائمة بالفواتير التي تم تعيينها لك من خلال عملية سير عمل رأس فاتورة المورد."
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 24818afbbdf328c8fd3eea691634db24e443b07b
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="c294f-104">مساحة العمل المحمولة الموافقات على الفواتير‬</span><span class="sxs-lookup"><span data-stu-id="c294f-104">Invoice approvals mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c294f-105">يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة **الموافقات على الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="c294f-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="c294f-106">توفر مساحة العمل المحمولة قائمة بالفواتير التي تم تعيينها لك من خلال عملية سير عمل رأس فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="c294f-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="c294f-107">تهدف مساحة العمل المحمولة هذه إلى استخدامها بواسطة تطبيق المحمول Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="c294f-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="c294f-108">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="c294f-108">Overview</span></span>

<span data-ttu-id="c294f-109">تسمح مساحة العمل المحمولة **الموافقات على الفواتير** لموظفي ومدراء الحسابات الدائنة عرض الفواتير التي تم تعيينها لهم كجزء من عملية سير عمل رأس فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="c294f-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="c294f-110">يمكنك عرض معلومات الفواتير، وحتى تفاصيل البنود والتوزيع لمساعدتك في اتخاذ قرارات مدروسة تتعلق بالموافقات.</span><span class="sxs-lookup"><span data-stu-id="c294f-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="c294f-111">من مساحة العمل، يمكنك اتخاذ إجراء لنقل الفاتورة من خلال عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="c294f-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="c294f-112">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="c294f-112">Prerequisites</span></span>

<span data-ttu-id="c294f-113">قبل أن تتمكن من استخدام مساحة العمل المحمولة هذه، يجب عليك تلبية المتطلبات الأساسية التالية.</span><span class="sxs-lookup"><span data-stu-id="c294f-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c294f-114">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="c294f-114">Prerequisite</span></span></th>
<th><span data-ttu-id="c294f-115">الدور</span><span class="sxs-lookup"><span data-stu-id="c294f-115">Role</span></span></th>
<th><span data-ttu-id="c294f-116">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="c294f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c294f-117">يجب نشر Microsoft Dynamics 365 for Finance and Operations, Enterprise edition، تحديث شهر يوليو 2017 في مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="c294f-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="c294f-118">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="c294f-118">System administrator</span></span></td>
<td><span data-ttu-id="c294f-119">راجع <a href="../deployment/deploy-demo-environment.md">نشر بيئة عرض توضيحي</a>.</span><span class="sxs-lookup"><span data-stu-id="c294f-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c294f-120">يجب نشر مساحة العمل المحمولة <strong>الموافقات على الفواتير</strong>.</span><span class="sxs-lookup"><span data-stu-id="c294f-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="c294f-121">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="c294f-121">System administrator</span></span></td>
<td><span data-ttu-id="c294f-122">راجع <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">نشر مساحة عمل محمولة</a></span><span class="sxs-lookup"><span data-stu-id="c294f-122">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="c294f-123">تحميل وتثبيت تطبيق الجوال</span><span class="sxs-lookup"><span data-stu-id="c294f-123">Download and install the mobile app</span></span>

<span data-ttu-id="c294f-124">تنزيل وتثبيت تطبيق Dynamics 365 for Unified Operations للأجهزة المحمولة:</span><span class="sxs-lookup"><span data-stu-id="c294f-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="c294f-125">لهواتف Android</span><span class="sxs-lookup"><span data-stu-id="c294f-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="c294f-126">لهواتف iPhone</span><span class="sxs-lookup"><span data-stu-id="c294f-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="c294f-127">تسجيل الدخول إلى تطبيق الهاتف الجوال</span><span class="sxs-lookup"><span data-stu-id="c294f-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="c294f-128">ابدأ تشغيل التطبيق على جهازك المحمول.</span><span class="sxs-lookup"><span data-stu-id="c294f-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="c294f-129">أدخل عنوان URL لـ Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c294f-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="c294f-130">في المرة الأولى التي تقوم بتسجيل الدخول فيها، تتم مطالبتك باسم المستخدم وكلمة المرور الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c294f-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="c294f-131">أدخل بيانات اعتمادك.</span><span class="sxs-lookup"><span data-stu-id="c294f-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="c294f-132">بعد تسجيل الدخول، تظهر مساحات العمل المتوفرة لشركتك.</span><span class="sxs-lookup"><span data-stu-id="c294f-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="c294f-133">تجدر الإشارة إلى أنه في حال قيام مسؤول النظام بنشر مساحة عمل جديدة في وقت لاحق، فسوف يكون عليك تحديث قائمة مساحات العمل المحمولة.</span><span class="sxs-lookup"><span data-stu-id="c294f-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="c294f-134">[![سحب للتحديث](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="c294f-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="c294f-135">الموافقة على الفواتير باستخدام مساحة العمل المحمولة "الموافقات على الفواتير"</span><span class="sxs-lookup"><span data-stu-id="c294f-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="c294f-136">على جهازك المحمول، حدد مساحة العمل **الموافقات على الفواتير‬**.</span><span class="sxs-lookup"><span data-stu-id="c294f-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="c294f-137">حدد الفاتورة التي تم تعيينها إليك عن طريق عملية سير عمل رأس فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="c294f-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="c294f-138">في صفحة **تفاصيل الفاتورة**، قم بمراجعة معلومات رأس الفاتورة، مثل معلومات المورد والتاريخ.</span><span class="sxs-lookup"><span data-stu-id="c294f-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="c294f-139">حدد بندًا على الفاتورة لعرض معلومات أكثر تفصيلاً تتعلق به في طريقة عرض **تفاصيل بند الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="c294f-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="c294f-140">في طريقة عرض **تفاصيل بند الفاتورة**، حدد **التوزيعات** لإظهار توزيعات البنود.</span><span class="sxs-lookup"><span data-stu-id="c294f-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="c294f-141">يمكنك هنا عرض التوزيعات المحاسبية لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c294f-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="c294f-142">تتضمن المعلومات التي تظهر الأبعاد المالية والحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="c294f-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="c294f-143">في صفحة **تفاصيل الفاتورة**، حدد **التوزيعات** لإظهار كافة التوزيعات.</span><span class="sxs-lookup"><span data-stu-id="c294f-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="c294f-144">يمكنك هنا عرض التوزيعات المحاسبية للفاتورة بكاملها.</span><span class="sxs-lookup"><span data-stu-id="c294f-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="c294f-145">تتضمن المعلومات التي تظهر الأبعاد المالية والحسابات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="c294f-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="c294f-146">حدد **المرفقات** لعرض أية ملاحظات أو ملفات مرفقة بالفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c294f-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="c294f-147">في صفحة **تفاصيل الفاتورة**، حدد إجراء سير العمل المناسب لإكمال عملية المراجعة.</span><span class="sxs-lookup"><span data-stu-id="c294f-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="c294f-148">حدد **تم**.</span><span class="sxs-lookup"><span data-stu-id="c294f-148">Select **Done**.</span></span>

