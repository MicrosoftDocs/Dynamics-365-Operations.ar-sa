---
title: إزالة مثيل
description: ''
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
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007911"
---
# <a name="remove-an-instance"></a><span data-ttu-id="a55be-102">إزالة مثيل</span><span class="sxs-lookup"><span data-stu-id="a55be-102">Remove an instance</span></span>

<span data-ttu-id="a55be-103">ينقلك هذا المقال عبر عملية إزالة بيئة إنتاج أو بيئة إصدار تجريبي جديدة لتطبيق Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a55be-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="a55be-104">إزالة بيئة محرك أقراص اختبار</span><span class="sxs-lookup"><span data-stu-id="a55be-104">Remove a test drive environment</span></span>

<span data-ttu-id="a55be-105">يتم توفير محركات أقراص اختبارات Human Resources باستخدام سياسة انتهاء صلاحية مدتها 60 يومًا.</span><span class="sxs-lookup"><span data-stu-id="a55be-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="a55be-106">ومع ذلك، يتوفر لمالكي بيئات محركات أقراص الاختبار خيار إنهاء الخدمة التجريبية الخاصة بها بواسطة إكمال الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a55be-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="a55be-107">الانتقال إلى مركز إدارة [Power Apps ](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a55be-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="a55be-108">حدد **بيئات**.</span><span class="sxs-lookup"><span data-stu-id="a55be-108">Select **Environments**.</span></span>
3. <span data-ttu-id="a55be-109">حدد بيئة الإصدار التجريبي، ذات نمط تسمية مماثل للنمط التالي: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="a55be-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="a55be-110">حدد **حذف** وقم بتأكيد القرار.</span><span class="sxs-lookup"><span data-stu-id="a55be-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="a55be-111">ستتم إزالة بيئة محرك أقراص الاختبار الموجودة.</span><span class="sxs-lookup"><span data-stu-id="a55be-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="a55be-112">عندما تتم إزالتها، يمكنك تسجيل الاشتراك في بيئة محرك أقراص اختبار جديدة.</span><span class="sxs-lookup"><span data-stu-id="a55be-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="a55be-113">إزالة بيئة إنتاج</span><span class="sxs-lookup"><span data-stu-id="a55be-113">Remove a production environment</span></span>

<span data-ttu-id="a55be-114">يفترض هذا المقال أنك قمت بشراء Human Resources من خلال اتفاقية هندسة مؤسسة (EA) أو موفر حلول مجموعة (CSP).</span><span class="sxs-lookup"><span data-stu-id="a55be-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="a55be-115">نظرًا لأن هناك بيئة Human Resources واحدة مشمولة ضمن بيئة Power Apps واحدة، هناك خياران ينبغي أخذهما بعين الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="a55be-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="a55be-116">الخيار الأول يتضمن إزالة بيئة Power Apps بالكامل، والثاني يتضمن إزالة Human Resources فقط.</span><span class="sxs-lookup"><span data-stu-id="a55be-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="a55be-117">والخيار الأول هو المفضل عند قيامك بإنشاء بيئة Power Apps صراحةً بغرض توفير Human Resources، وقد بدأت التنفيذ للتو، أو لم يكن لديك أي عمليات تكامل قائمة.</span><span class="sxs-lookup"><span data-stu-id="a55be-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="a55be-118">والخيار الثاني مناسب إذا كان لديك بيئة Power Apps محددة معبأة بالبيانات الغنية التي يتم جمعها في Power Apps وPower Automate.</span><span class="sxs-lookup"><span data-stu-id="a55be-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="a55be-119">قبل إزالة بيئة Power Apps، تأكد من عدم استخدامه لعمليات تكامل البيانات الغنية خارج نطاق Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a55be-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="a55be-120">كما تجدر الإشارة إلى أنه لا يمكن إزالة بيئات Power Apps الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="a55be-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="a55be-121">لإزالة بيئة Power Apps بأكملها، بما في ذلك Human Resources والتطبيقات والتدفقات المرتبطة:</span><span class="sxs-lookup"><span data-stu-id="a55be-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="a55be-122">الانتقال إلى مركز إدارة [Power Apps ](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a55be-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="a55be-123">حدد **بيئات**.</span><span class="sxs-lookup"><span data-stu-id="a55be-123">Select **Environments**.</span></span>
3. <span data-ttu-id="a55be-124">حدد البيئة المُراد إزالتها.</span><span class="sxs-lookup"><span data-stu-id="a55be-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="a55be-125">حدد **حذف** وقم بتأكيد القرار.</span><span class="sxs-lookup"><span data-stu-id="a55be-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="a55be-126">انتظر حتى تكتمل عملية الحذف.</span><span class="sxs-lookup"><span data-stu-id="a55be-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="a55be-127">قم بتسجيل الدخول إلى [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (‏LCS‏) باستخدام الحساب الذي استخدمته للاشتراك في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a55be-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="a55be-128">حدد مشروع Human Resources الذي يحتوي على البيئة.</span><span class="sxs-lookup"><span data-stu-id="a55be-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="a55be-129">في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="a55be-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="a55be-130">حدد المثيل المراد إزالته.</span><span class="sxs-lookup"><span data-stu-id="a55be-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="a55be-131">حدد **إزالة مثيل** وقم بتأكيد قرارك.</span><span class="sxs-lookup"><span data-stu-id="a55be-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="a55be-132">لإزالة بيئة Human Resources من بيئة Power Apps موجودة، أكمل الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a55be-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="a55be-133">لاحظ أن الحاجة إلى تضمين الدعم والاتصال بفريق عمليات تطوير Human Resources مؤقتة إلى أن يتم تمكين هذه الميزة في LCS مباشرةً.</span><span class="sxs-lookup"><span data-stu-id="a55be-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="a55be-134">اتصل بدعم لبدء طلب إزالة.</span><span class="sxs-lookup"><span data-stu-id="a55be-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="a55be-135">سيبدأ فريق الدعم طلب إزالة مع فريق عمليات تطوير Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a55be-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="a55be-136">تابع بعد ظهور كلمة لك تفيد بأنه تمت إزالة البيئة.</span><span class="sxs-lookup"><span data-stu-id="a55be-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="a55be-137">قم بتسجيل الدخول إلى LCS باستخدام الحساب الذي استخدمته للاشتراك في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a55be-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="a55be-138">حدد مشروع Human Resources الذي يحتوي على البيئة.</span><span class="sxs-lookup"><span data-stu-id="a55be-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="a55be-139">في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="a55be-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="a55be-140">حدد المثيل الذي ترغب في إزالته، والذي يجب تمييزه بحالة النشر **فشل**.</span><span class="sxs-lookup"><span data-stu-id="a55be-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="a55be-141">حدد **إزالة مثيل** وقم بتأكيد قرارك.</span><span class="sxs-lookup"><span data-stu-id="a55be-141">Select **Remove instance** and confirm your decision.</span></span> 
