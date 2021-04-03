---
title: مساحة العمل المحمولة الموافقات على الفواتير‬
description: يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة "الموافقات على الفواتير‬‬".
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3d90b89900b35bce648841aa9e49737a25309ce2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570058"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="a4931-103">مساحة العمل المحمولة الموافقات على الفواتير‬</span><span class="sxs-lookup"><span data-stu-id="a4931-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4931-104">يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة **الموافقات على الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="a4931-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="a4931-105">توفر مساحة العمل المحمولة قائمة بالفواتير التي تم تعيينها لك من خلال عملية سير عمل رأس فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="a4931-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="a4931-106">مساحة العمل المحمولة هذه مخصصة للاستخدام مع تطبيق Finance and Operations للأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="a4931-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="a4931-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="a4931-107">Overview</span></span>

<span data-ttu-id="a4931-108">تسمح مساحة العمل المحمولة **الموافقات على الفواتير** لموظفي ومدراء الحسابات الدائنة عرض الفواتير التي تم تعيينها لهم كجزء من عملية سير عمل رأس فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="a4931-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="a4931-109">يمكنك عرض معلومات الفواتير، وحتى تفاصيل البنود والتوزيع لمساعدتك في اتخاذ قرارات مدروسة تتعلق بالموافقات.</span><span class="sxs-lookup"><span data-stu-id="a4931-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="a4931-110">من مساحة العمل، يمكنك اتخاذ إجراء لنقل الفاتورة من خلال عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="a4931-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="a4931-111">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="a4931-111">Prerequisites</span></span>

<span data-ttu-id="a4931-112">قبل أن تتمكن من استخدام مساحة العمل المحمولة هذه، يجب عليك تلبية المتطلبات الأساسية التالية.</span><span class="sxs-lookup"><span data-stu-id="a4931-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a4931-113">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="a4931-113">Prerequisite</span></span></th>
<th><span data-ttu-id="a4931-114">دور</span><span class="sxs-lookup"><span data-stu-id="a4931-114">Role</span></span></th>
<th><span data-ttu-id="a4931-115">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="a4931-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4931-116">يجب نشر Microsoft Dynamics 365 Finance في مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="a4931-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="a4931-117">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="a4931-117">System administrator</span></span></td>
<td><span data-ttu-id="a4931-118">راجع <a href="../deployment/deploy-demo-environment.md">نشر بيئة عرض توضيحي</a>.</span><span class="sxs-lookup"><span data-stu-id="a4931-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4931-119">يجب نشر مساحة العمل المحمولة <strong>الموافقات على الفواتير</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4931-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="a4931-120">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="a4931-120">System administrator</span></span></td>
<td><span data-ttu-id="a4931-121">راجع <a href="publish-mobile-workspace.md">نشر مساحة عمل محمولة</a></span><span class="sxs-lookup"><span data-stu-id="a4931-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="a4931-122">تنزيل وتثبيت تطبيق المحمول</span><span class="sxs-lookup"><span data-stu-id="a4931-122">Download and install the mobile app</span></span>

<span data-ttu-id="a4931-123">تنزيل وتثبيت تطبيق Finance and Operations للأجهزة المحمولة:</span><span class="sxs-lookup"><span data-stu-id="a4931-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="a4931-124">لهواتف Android</span><span class="sxs-lookup"><span data-stu-id="a4931-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="a4931-125">لهواتف iPhone</span><span class="sxs-lookup"><span data-stu-id="a4931-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="a4931-126">تسجيل الدخول إلى تطبيق الهاتف الجوال</span><span class="sxs-lookup"><span data-stu-id="a4931-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="a4931-127">ابدأ تشغيل التطبيق على جهازك المحمول.</span><span class="sxs-lookup"><span data-stu-id="a4931-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="a4931-128">أدخل عنوان URL لـ Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a4931-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="a4931-129">في المرة الأولى التي تقوم بتسجيل الدخول فيها، تتم مطالبتك باسم المستخدم وكلمة المرور الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a4931-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="a4931-130">أدخل بيانات اعتمادك.</span><span class="sxs-lookup"><span data-stu-id="a4931-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="a4931-131">بعد تسجيل الدخول، تظهر مساحات العمل المتوفرة لشركتك.</span><span class="sxs-lookup"><span data-stu-id="a4931-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="a4931-132">تجدر الإشارة إلى أنه في حال قيام مسؤول النظام بنشر مساحة عمل جديدة في وقت لاحق، فسوف يكون عليك تحديث قائمة مساحات العمل المحمولة.</span><span class="sxs-lookup"><span data-stu-id="a4931-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="a4931-133">[![سحب للتحديث](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="a4931-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="a4931-134">الموافقة على الفواتير باستخدام مساحة العمل المحمولة "الموافقات على الفواتير"</span><span class="sxs-lookup"><span data-stu-id="a4931-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="a4931-135">على جهازك المحمول، حدد مساحة العمل **الموافقات على الفواتير‬**.</span><span class="sxs-lookup"><span data-stu-id="a4931-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="a4931-136">حدد الفاتورة التي تم تعيينها إليك عن طريق عملية سير عمل رأس فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="a4931-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="a4931-137">في صفحة **تفاصيل الفاتورة**، قم بمراجعة معلومات رأس الفاتورة، مثل معلومات المورد والتاريخ.</span><span class="sxs-lookup"><span data-stu-id="a4931-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="a4931-138">حدد بندًا على الفاتورة لعرض معلومات أكثر تفصيلاً تتعلق به في طريقة عرض **تفاصيل بند الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="a4931-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="a4931-139">في طريقة عرض **تفاصيل بند الفاتورة**، حدد **التوزيعات** لإظهار توزيعات البنود.</span><span class="sxs-lookup"><span data-stu-id="a4931-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="a4931-140">يمكنك هنا عرض التوزيعات المحاسبية لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="a4931-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="a4931-141">تتضمن المعلومات التي تظهر الأبعاد المالية والحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a4931-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="a4931-142">في صفحة **تفاصيل الفاتورة**، حدد **التوزيعات** لإظهار كافة التوزيعات.</span><span class="sxs-lookup"><span data-stu-id="a4931-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="a4931-143">يمكنك هنا عرض التوزيعات المحاسبية للفاتورة بكاملها.</span><span class="sxs-lookup"><span data-stu-id="a4931-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="a4931-144">تتضمن المعلومات التي تظهر الأبعاد المالية والحسابات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="a4931-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="a4931-145">حدد **المرفقات** لعرض أية ملاحظات أو ملفات مرفقة بالفاتورة.</span><span class="sxs-lookup"><span data-stu-id="a4931-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="a4931-146">في صفحة **تفاصيل الفاتورة**، حدد إجراء سير العمل المناسب لإكمال عملية المراجعة.</span><span class="sxs-lookup"><span data-stu-id="a4931-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="a4931-147">حدد **تم**.</span><span class="sxs-lookup"><span data-stu-id="a4931-147">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]