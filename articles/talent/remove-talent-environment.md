---
title: إزالة بيئات Talent
description: ينقلك هذا الموضوع عبر عملية إزالة بيئة إنتاج أو بيئة إصدار تجريبي جديدة لتطبيق Dynamics 365 for Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 904c8eb1254a65e1627c33f14488a1a8e12f7c2b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517243"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="49c91-103">إزالة بيئات Talent</span><span class="sxs-lookup"><span data-stu-id="49c91-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49c91-104">ينقلك هذا الموضوع عبر عملية إزالة بيئة إنتاج أو بيئة إصدار تجريبي جديدة لتطبيق Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="49c91-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="49c91-105">إزالة بيئة محرك أقراص اختبار</span><span class="sxs-lookup"><span data-stu-id="49c91-105">Removing a test drive environment</span></span>

<span data-ttu-id="49c91-106">يتم توفير محركات أقراص اختبارات Talent باستخدام سياسة انتهاء صلاحية مدتها 60 يومًا.</span><span class="sxs-lookup"><span data-stu-id="49c91-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="49c91-107">ومع ذلك، يتوفر لمالكي بيئات محركات أقراص الاختبار خيار إنهاء الخدمة التجريبية الخاصة بها بواسطة إكمال الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="49c91-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="49c91-108">انتقل إلى [مركز إدارة PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="49c91-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="49c91-109">حدد **بيئات**.</span><span class="sxs-lookup"><span data-stu-id="49c91-109">Select **Environments**.</span></span>
3. <span data-ttu-id="49c91-110">حدد بيئة الإصدار التجريبي، ذات نمط تسمية مماثل للنمط التالي: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="49c91-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="49c91-111">حدد **حذف** وقم بتأكيد القرار.</span><span class="sxs-lookup"><span data-stu-id="49c91-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="49c91-112">ستتم إزالة بيئة محرك أقراص الاختبار الموجودة.</span><span class="sxs-lookup"><span data-stu-id="49c91-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="49c91-113">عندما تتم إزالتها، يمكنك تسجيل الاشتراك في بيئة محرك أقراص اختبار جديدة.</span><span class="sxs-lookup"><span data-stu-id="49c91-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="49c91-114">إزالة بيئة إنتاج</span><span class="sxs-lookup"><span data-stu-id="49c91-114">Removing a production environment</span></span>

<span data-ttu-id="49c91-115">يفترض هذا الموضوع أنك قمت بشراء Talent من خلال اتفاقية هندسة مؤسسة (EA) أو موفر حلول مجموعة (CSP).</span><span class="sxs-lookup"><span data-stu-id="49c91-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="49c91-116">نظرًا لأن هناك بيئة Talent واحدة "مشمولة" ضمن بيئة PowerApps واحدة، هناك خياران ينبغي أخذهما بعين الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="49c91-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="49c91-117">الخيار الأول يتضمن إزالة بيئة PowerApps بالكامل، والثاني يتضمن إزالة Talent فقط.</span><span class="sxs-lookup"><span data-stu-id="49c91-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="49c91-118">والخيار الأول هو المفضل عند قيامك بإنشاء بيئة PowerApps صراحةً بغرض توفير Talent، وقد بدأت التنفيذ للتو، أو لم يكن لديك أي عمليات تكامل قائمة.</span><span class="sxs-lookup"><span data-stu-id="49c91-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="49c91-119">والخيار الثاني مناسب إذا كان لديك بيئة PowerApps محددة معبأة بالبيانات الغنية التي يتم جمعها في PowerApps والتدفقات.</span><span class="sxs-lookup"><span data-stu-id="49c91-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="49c91-120">قبل إزالة بيئة PowerApps، تأكد من عدم استخدامه لعمليات تكامل البيانات الغنية خارج نطاق Talent.</span><span class="sxs-lookup"><span data-stu-id="49c91-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="49c91-121">كما تجدر الإشارة إلى أنه لا يمكن إزالة بيئات PowerApps الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="49c91-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="49c91-122">لإزالة بيئة PowerApps بأكملها، بما في ذلك Talent والتطبيقات والتدفقات المرتبطة:</span><span class="sxs-lookup"><span data-stu-id="49c91-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="49c91-123">انتقل إلى [مركز إدارة PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="49c91-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="49c91-124">حدد **بيئات**.</span><span class="sxs-lookup"><span data-stu-id="49c91-124">Select **Environments**.</span></span>
3. <span data-ttu-id="49c91-125">حدد البيئة المُراد إزالتها.</span><span class="sxs-lookup"><span data-stu-id="49c91-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="49c91-126">حدد **حذف** وقم بتأكيد القرار.</span><span class="sxs-lookup"><span data-stu-id="49c91-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="49c91-127">انتظر حتى تكتمل عملية الحذف.</span><span class="sxs-lookup"><span data-stu-id="49c91-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="49c91-128">قم بتسجيل الدخول إلى [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (‏LCS‏) باستخدام الحساب الذي استخدمته للاشتراك في Talent.</span><span class="sxs-lookup"><span data-stu-id="49c91-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="49c91-129">حدد "مشروع Talent" الذي يحتوي على البيئة.</span><span class="sxs-lookup"><span data-stu-id="49c91-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="49c91-130">في مشروع LCS، حدد تجانب **"إدارة تطبيق Talent**.</span><span class="sxs-lookup"><span data-stu-id="49c91-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="49c91-131">حدد المثيل المراد إزالته.</span><span class="sxs-lookup"><span data-stu-id="49c91-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="49c91-132">حدد **إزالة مثيل** وقم بتأكيد قرارك.</span><span class="sxs-lookup"><span data-stu-id="49c91-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="49c91-133">لإزالة بيئة Talent من بيئة PowerApps موجودة، أكمل الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="49c91-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="49c91-134">لاحظ أن الحاجة إلى تضمين الدعم والاتصال بفريق عمليات تطوير Talent مؤقتة إلى أن يتم تمكين هذه الميزة في LCS مباشرةً.</span><span class="sxs-lookup"><span data-stu-id="49c91-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="49c91-135">اتصل بدعم لبدء طلب إزالة.</span><span class="sxs-lookup"><span data-stu-id="49c91-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="49c91-136">سيبدأ فريق الدعم طلب إزالة مع فريق عمليات تطوير Talent.</span><span class="sxs-lookup"><span data-stu-id="49c91-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="49c91-137">تابع بعد ظهور كلمة لك تفيد بأنه تمت إزالة البيئة.</span><span class="sxs-lookup"><span data-stu-id="49c91-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="49c91-138">قم بتسجيل الدخول إلى LCS باستخدام الحساب الذي استخدمته للاشتراك في Talent.</span><span class="sxs-lookup"><span data-stu-id="49c91-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="49c91-139">حدد "مشروع Talent" الذي يحتوي على البيئة.</span><span class="sxs-lookup"><span data-stu-id="49c91-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="49c91-140">في مشروع LCS، حدد تجانب **"إدارة تطبيق Talent**.</span><span class="sxs-lookup"><span data-stu-id="49c91-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="49c91-141">حدد المثيل الذي ترغب في إزالته، والذي يجب تمييزه بحالة النشر **فشل**.</span><span class="sxs-lookup"><span data-stu-id="49c91-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="49c91-142">حدد **إزالة مثيل** وقم بتأكيد قرارك.</span><span class="sxs-lookup"><span data-stu-id="49c91-142">Select **Remove instance** and confirm your decision.</span></span> 

