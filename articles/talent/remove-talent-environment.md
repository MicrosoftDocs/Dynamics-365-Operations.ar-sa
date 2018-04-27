---
title: "إزالة بيئة Talent"
description: "يوضح لك هذا الموضوع عملية إزالة محرك أقراص اختبار أو بيئة إنتاج جديدة لـ Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d1870c84d4d5e7402bae44d192ce7587c2f67fe7
ms.openlocfilehash: 0e7748b079b1cd5c069917d46e05cd281ea6aa01
ms.contentlocale: ar-sa
ms.lasthandoff: 04/05/2018

---
# <a name="remove-a-talent-environment"></a><span data-ttu-id="1b65a-103">إزالة بيئة Talent</span><span class="sxs-lookup"><span data-stu-id="1b65a-103">Remove a Talent environment</span></span>

<span data-ttu-id="1b65a-104">يوضح لك هذا الموضوع عملية إزالة محرك أقراص اختبار أو بيئة إنتاج جديدة لـ Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="1b65a-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="1b65a-105">إزالة بيئة محرك أقراص اختبار</span><span class="sxs-lookup"><span data-stu-id="1b65a-105">Removing a test drive environment</span></span>

<span data-ttu-id="1b65a-106">يتم توفير محركات أقراص اختبارات Talent باستخدام سياسة انتهاء صلاحية مدتها 60 يومًا.</span><span class="sxs-lookup"><span data-stu-id="1b65a-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="1b65a-107">ومع ذلك، يتوفر لمالكي بيئات محركات أقراص الاختبار خيار إنهاء الخدمة التجريبية الخاصة بها بواسطة إكمال الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="1b65a-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="1b65a-108">انتقل إلى [مركز إدارة PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="1b65a-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="1b65a-109">حدد **بيئات**.</span><span class="sxs-lookup"><span data-stu-id="1b65a-109">Select **Environments**.</span></span>
3. <span data-ttu-id="1b65a-110">حدد بيئة محرك أقراص الاختبار الذي يحتوي على نمط تسمية مشابه لما يلي: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="1b65a-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="1b65a-111">حدد **حذف** وقم بتأكيد القرار.</span><span class="sxs-lookup"><span data-stu-id="1b65a-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="1b65a-112">ستتم إزالة بيئة محرك أقراص الاختبار الموجودة.</span><span class="sxs-lookup"><span data-stu-id="1b65a-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="1b65a-113">عندما تتم إزالتها، يمكنك تسجيل الاشتراك في بيئة محرك أقراص اختبار جديدة.</span><span class="sxs-lookup"><span data-stu-id="1b65a-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="1b65a-114">إزالة بيئة إنتاج</span><span class="sxs-lookup"><span data-stu-id="1b65a-114">Removing a production environment</span></span>

<span data-ttu-id="1b65a-115">يفترض هذا الموضوع أنك قمت بشراء Talent من خلال اتفاقية هندسة مؤسسة (EA) أو موفر حلول مجموعة (CSP).</span><span class="sxs-lookup"><span data-stu-id="1b65a-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="1b65a-116">نظرًا لأن هناك بيئة Talent واحدة "مشمولة" ضمن بيئة PowerApps واحدة، هناك خياران ينبغي أخذهما بعين الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="1b65a-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="1b65a-117">الخيار الأول يتضمن إزالة بيئة PowerApps بالكامل، والثاني يتضمن إزالة Talent فقط.</span><span class="sxs-lookup"><span data-stu-id="1b65a-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="1b65a-118">والخيار الأول هو المفضل عند قيامك بإنشاء بيئة PowerApps صراحةً بغرض توفير Talent، وقد بدأت التنفيذ للتو، أو لم يكن لديك أي عمليات تكامل قائمة.</span><span class="sxs-lookup"><span data-stu-id="1b65a-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="1b65a-119">والخيار الثاني مناسب إذا كان لديك بيئة PowerApps محددة معبأة بالبيانات الغنية التي يتم جمعها في PowerApps والتدفقات.</span><span class="sxs-lookup"><span data-stu-id="1b65a-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="1b65a-120">قبل إزالة بيئة PowerApps، تأكد من عدم استخدامه لعمليات تكامل البيانات الغنية خارج نطاق Talent.</span><span class="sxs-lookup"><span data-stu-id="1b65a-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="1b65a-121">كما تجدر الإشارة إلى أنه لا يمكن إزالة بيئات PowerApps الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="1b65a-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="1b65a-122">لإزالة بيئة PowerApps بأكملها، بما في ذلك Talent والتطبيقات والتدفقات المرتبطة:</span><span class="sxs-lookup"><span data-stu-id="1b65a-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="1b65a-123">انتقل إلى [مركز إدارة PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="1b65a-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="1b65a-124">حدد **بيئات**.</span><span class="sxs-lookup"><span data-stu-id="1b65a-124">Select **Environments**.</span></span>
3. <span data-ttu-id="1b65a-125">حدد البيئة المُراد إزالتها.</span><span class="sxs-lookup"><span data-stu-id="1b65a-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="1b65a-126">حدد **حذف** وقم بتأكيد القرار.</span><span class="sxs-lookup"><span data-stu-id="1b65a-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="1b65a-127">انتظر حتى تكتمل عملية الحذف.</span><span class="sxs-lookup"><span data-stu-id="1b65a-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="1b65a-128">قم بتسجيل الدخول إلى [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (‏LCS‏) باستخدام الحساب الذي استخدمته للاشتراك في Talent.</span><span class="sxs-lookup"><span data-stu-id="1b65a-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="1b65a-129">حدد "مشروع Talent" الذي يحتوي على البيئة.</span><span class="sxs-lookup"><span data-stu-id="1b65a-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="1b65a-130">في مشروع LCS، حدد تجانب **"إدارة تطبيق Talent**.</span><span class="sxs-lookup"><span data-stu-id="1b65a-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="1b65a-131">حدد المثيل المراد إزالته.</span><span class="sxs-lookup"><span data-stu-id="1b65a-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="1b65a-132">حدد **إزالة مثيل** وقم بتأكيد قرارك.</span><span class="sxs-lookup"><span data-stu-id="1b65a-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="1b65a-133">لإزالة بيئة Talent من بيئة PowerApps موجودة، أكمل الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="1b65a-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="1b65a-134">لاحظ أن الحاجة إلى تضمين الدعم والاتصال بفريق عمليات تطوير Talent مؤقتة إلى أن يتم تمكين هذه الميزة في LCS مباشرةً.</span><span class="sxs-lookup"><span data-stu-id="1b65a-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="1b65a-135">اتصل بدعم لبدء طلب إزالة.</span><span class="sxs-lookup"><span data-stu-id="1b65a-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="1b65a-136">سيبدأ فريق الدعم طلب إزالة مع فريق عمليات تطوير Talent.</span><span class="sxs-lookup"><span data-stu-id="1b65a-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="1b65a-137">تابع بعد ظهور كلمة لك تفيد بأنه تمت إزالة البيئة.</span><span class="sxs-lookup"><span data-stu-id="1b65a-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="1b65a-138">قم بتسجيل الدخول إلى LCS باستخدام الحساب الذي استخدمته للاشتراك في Talent.</span><span class="sxs-lookup"><span data-stu-id="1b65a-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="1b65a-139">حدد "مشروع Talent" الذي يحتوي على البيئة.</span><span class="sxs-lookup"><span data-stu-id="1b65a-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="1b65a-140">في مشروع LCS، حدد تجانب **"إدارة تطبيق Talent**.</span><span class="sxs-lookup"><span data-stu-id="1b65a-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="1b65a-141">حدد المثيل الذي ترغب في إزالته، والذي يجب تمييزه بحالة النشر **فشل**.</span><span class="sxs-lookup"><span data-stu-id="1b65a-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="1b65a-142">حدد **إزالة مثيل** وقم بتأكيد قرارك.</span><span class="sxs-lookup"><span data-stu-id="1b65a-142">Select **Remove instance** and confirm your decision.</span></span> 


