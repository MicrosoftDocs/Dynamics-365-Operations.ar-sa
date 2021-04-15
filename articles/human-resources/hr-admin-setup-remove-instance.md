---
title: إزالة مثيل
description: ينقلك هذا المقال عبر عملية إزالة بيئة إنتاج أو بيئة إصدار تجريبي جديدة لتطبيق Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 399c710b99c5721ff9867ce332b815bd362d6103
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795011"
---
# <a name="remove-an-instance"></a><span data-ttu-id="84f07-103">إزالة مثيل</span><span class="sxs-lookup"><span data-stu-id="84f07-103">Remove an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="84f07-104">ينقلك هذا المقال عبر عملية إزالة بيئة إنتاج أو بيئة إصدار تجريبي جديدة لتطبيق Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="84f07-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="84f07-105">إزالة بيئة محرك أقراص اختبار</span><span class="sxs-lookup"><span data-stu-id="84f07-105">Remove a test drive environment</span></span>

<span data-ttu-id="84f07-106">يتم توفير محركات أقراص اختبارات Human Resources باستخدام سياسة انتهاء صلاحية مدتها 60 يومًا.</span><span class="sxs-lookup"><span data-stu-id="84f07-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="84f07-107">ومع ذلك، يتوفر لمالكي بيئات محركات أقراص الاختبار خيار إنهاء الخدمة التجريبية الخاصة بها بواسطة إكمال الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="84f07-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="84f07-108">الانتقال إلى مركز إدارة [Power Apps ](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="84f07-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="84f07-109">حدد **بيئات**.</span><span class="sxs-lookup"><span data-stu-id="84f07-109">Select **Environments**.</span></span>
3. <span data-ttu-id="84f07-110">حدد بيئة الإصدار التجريبي، ذات نمط تسمية مماثل للنمط التالي: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="84f07-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="84f07-111">حدد **حذف** وقم بتأكيد القرار.</span><span class="sxs-lookup"><span data-stu-id="84f07-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="84f07-112">ستتم إزالة بيئة محرك أقراص الاختبار الموجودة.</span><span class="sxs-lookup"><span data-stu-id="84f07-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="84f07-113">عندما تتم إزالتها، يمكنك تسجيل الاشتراك في بيئة محرك أقراص اختبار جديدة.</span><span class="sxs-lookup"><span data-stu-id="84f07-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="84f07-114">إزالة بيئة إنتاج</span><span class="sxs-lookup"><span data-stu-id="84f07-114">Remove a production environment</span></span>

<span data-ttu-id="84f07-115">يفترض هذا المقال أنك قمت بشراء Human Resources من خلال اتفاقية هندسة مؤسسة (EA) أو موفر حلول مجموعة (CSP).</span><span class="sxs-lookup"><span data-stu-id="84f07-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="84f07-116">نظرًا لأن هناك بيئة Human Resources واحدة مشمولة ضمن بيئة Power Apps واحدة، هناك خياران ينبغي أخذهما بعين الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="84f07-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="84f07-117">الخيار الأول يتضمن إزالة بيئة Power Apps بالكامل، والثاني يتضمن إزالة Human Resources فقط.</span><span class="sxs-lookup"><span data-stu-id="84f07-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="84f07-118">والخيار الأول هو المفضل عند قيامك بإنشاء بيئة Power Apps صراحةً بغرض توفير Human Resources، وقد بدأت التنفيذ للتو، أو لم يكن لديك أي عمليات تكامل قائمة.</span><span class="sxs-lookup"><span data-stu-id="84f07-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="84f07-119">والخيار الثاني مناسب إذا كان لديك بيئة Power Apps محددة معبأة بالبيانات الغنية التي يتم جمعها في Power Apps وPower Automate.</span><span class="sxs-lookup"><span data-stu-id="84f07-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="84f07-120">قبل إزالة بيئة Power Apps، تأكد من عدم استخدامه لعمليات تكامل البيانات الغنية خارج نطاق Human Resources.</span><span class="sxs-lookup"><span data-stu-id="84f07-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="84f07-121">كما تجدر الإشارة إلى أنه لا يمكن إزالة بيئات Power Apps الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="84f07-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="84f07-122">لإزالة بيئة Power Apps بأكملها، بما في ذلك Human Resources والتطبيقات والتدفقات المرتبطة:</span><span class="sxs-lookup"><span data-stu-id="84f07-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="84f07-123">الانتقال إلى مركز إدارة [Power Apps ](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="84f07-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="84f07-124">حدد **بيئات**.</span><span class="sxs-lookup"><span data-stu-id="84f07-124">Select **Environments**.</span></span>
3. <span data-ttu-id="84f07-125">حدد البيئة المُراد إزالتها.</span><span class="sxs-lookup"><span data-stu-id="84f07-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="84f07-126">حدد **حذف** وقم بتأكيد القرار.</span><span class="sxs-lookup"><span data-stu-id="84f07-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="84f07-127">انتظر حتى تكتمل عملية الحذف.</span><span class="sxs-lookup"><span data-stu-id="84f07-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="84f07-128">قم بتسجيل الدخول إلى [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (‏LCS‏) باستخدام الحساب الذي استخدمته للاشتراك في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="84f07-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="84f07-129">حدد مشروع Human Resources الذي يحتوي على البيئة.</span><span class="sxs-lookup"><span data-stu-id="84f07-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="84f07-130">في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="84f07-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="84f07-131">حدد المثيل المراد إزالته.</span><span class="sxs-lookup"><span data-stu-id="84f07-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="84f07-132">حدد **إزالة مثيل** وقم بتأكيد قرارك.</span><span class="sxs-lookup"><span data-stu-id="84f07-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="84f07-133">لإزالة بيئة Human Resources من بيئة Power Apps موجودة، أكمل الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="84f07-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="84f07-134">لاحظ أن الحاجة إلى تضمين الدعم والاتصال بفريق عمليات تطوير Human Resources مؤقتة إلى أن يتم تمكين هذه الميزة في LCS مباشرةً.</span><span class="sxs-lookup"><span data-stu-id="84f07-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="84f07-135">اتصل بدعم لبدء طلب إزالة.</span><span class="sxs-lookup"><span data-stu-id="84f07-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="84f07-136">سيبدأ فريق الدعم طلب إزالة مع فريق عمليات تطوير Human Resources.</span><span class="sxs-lookup"><span data-stu-id="84f07-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="84f07-137">تابع بعد ظهور كلمة لك تفيد بأنه تمت إزالة البيئة.</span><span class="sxs-lookup"><span data-stu-id="84f07-137">Continue after you receive word that the environment has been removed.</span></span>
4. <span data-ttu-id="84f07-138">قم بتسجيل الدخول إلى LCS باستخدام الحساب الذي استخدمته للاشتراك في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="84f07-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="84f07-139">حدد مشروع Human Resources الذي يحتوي على البيئة.</span><span class="sxs-lookup"><span data-stu-id="84f07-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="84f07-140">في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="84f07-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="84f07-141">حدد المثيل الذي ترغب في إزالته، والذي يجب تمييزه بحالة النشر **محذوف**.</span><span class="sxs-lookup"><span data-stu-id="84f07-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Deleted**.</span></span>
8. <span data-ttu-id="84f07-142">حدد **إزالة مثيل** وقم بتأكيد قرارك.</span><span class="sxs-lookup"><span data-stu-id="84f07-142">Select **Remove instance** and confirm your decision.</span></span> 

## <a name="recover-a-soft-deleted-environment"></a><span data-ttu-id="84f07-143">استرداد بيئة محذوفة بشكل مبدئي</span><span class="sxs-lookup"><span data-stu-id="84f07-143">Recover a soft-deleted environment</span></span>

<span data-ttu-id="84f07-144">إذا قمت بحذف بيئة Power Apps من بيئة Human Resources المتصلة بها، ستكون حالة بيئة Human Resources في Lifecycle Services **محذوفة مبدئيًا** .</span><span class="sxs-lookup"><span data-stu-id="84f07-144">If you delete the Power Apps environment that your Human Resources environment is connected to, the status of the Human Resources environment in Lifecycle Services will be **Soft deleted**.</span></span> <span data-ttu-id="84f07-145">في هذه الحالة، سيتعذر على المستخدمين الاتصال بـ Human Resources.</span><span class="sxs-lookup"><span data-stu-id="84f07-145">In this case, users can't connect to Human Resources.</span></span>

<span data-ttu-id="84f07-146">لاستعاده البيئة:</span><span class="sxs-lookup"><span data-stu-id="84f07-146">To restore the environment:</span></span>

1. <span data-ttu-id="84f07-147">اتبع الإرشادات في [استرداد بيئة Power Apps](/power-platform/admin/recover-environment.md).</span><span class="sxs-lookup"><span data-stu-id="84f07-147">Follow the instructions in [Recover the Power Apps environment](/power-platform/admin/recover-environment.md).</span></span>

2. <span data-ttu-id="84f07-148">اتصل بالدعم لاستعاده بيئة Human Resources.</span><span class="sxs-lookup"><span data-stu-id="84f07-148">Contact Support to restore the Human Resources environment.</span></span> <span data-ttu-id="84f07-149">لمزيد من المعلومات، راجع [الحصول على الدعم](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="84f07-149">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

> [!Warning]
> <span data-ttu-id="84f07-150">يتم حفظ بيئات Power Apps لسبعة أيام فقط بعد الحذف.</span><span class="sxs-lookup"><span data-stu-id="84f07-150">Power Apps environments are only saved for seven days after deletion.</span></span> <span data-ttu-id="84f07-151">يجب استرداد البيئة خلال فترة السبعة أيام.</span><span class="sxs-lookup"><span data-stu-id="84f07-151">You must recover the environment within the seven day period.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]