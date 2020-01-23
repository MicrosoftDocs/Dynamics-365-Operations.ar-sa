---
title: استكشاف أخطاء التكامل وإصلاحها مع LinkedIn وMicrosoft Dynamics 365 Talent - Attract
description: يوضح هذا الموضوع كيفية استكشاف المشكلات وإصلاحها عند محاولة نشر الوظائف في LinkedIn من Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: ec095642f556b8d0087dd22f35097671a30047a6
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898493"
---
# <a name="troubleshoot-integration-with-linkedin-and-attract"></a><span data-ttu-id="2231c-103">استكشاف أخطاء التكامل وإصلاحها باستخدام LinkedIn وAttract</span><span class="sxs-lookup"><span data-stu-id="2231c-103">Troubleshoot integration with LinkedIn and Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2231c-104">استخدم المعلومات التالية للمساعدة في استكشاف وإصلاح المشاكل التي قد تواجهها عند محاولة نشر الوظائف في LinkedIn من Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="2231c-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="2231c-105">لا يمكنك تسجيل الدخول إلى LinkedIn من Attract</span><span class="sxs-lookup"><span data-stu-id="2231c-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="2231c-106">إذا واجهت مشكلة ما في تسجيل الدخول إلى LinkedIn من Attract، فجرب الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="2231c-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="2231c-107">تأكد من أن بيانات اعتماد LinkedIn التي أدخلتها في Attract صالحة وصحيحة.</span><span class="sxs-lookup"><span data-stu-id="2231c-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="2231c-108">إذا كانت بيانات الاعتماد صالحة وصحيحة، فاتصل بقسم [دعم LinkedIn](https://www.linkedin.com/help/linkedin).</span><span class="sxs-lookup"><span data-stu-id="2231c-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="2231c-109">إذا استمرت المشكلة، فاتصل بقسم [دعم Microsoft](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="2231c-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="2231c-110">لا تظهر عمليات نشر الوظائف من Attract في LinkedIn</span><span class="sxs-lookup"><span data-stu-id="2231c-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="2231c-111">إذا لم تظهر وظيفتك على LinkedIn بعد 24 ساعة، فحاول القيام بهذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="2231c-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="2231c-112">تأكد من تعيين معرّف شركتك في LinkedIn إلى صفحة شركتك في LinkedIn ومن إدخالها بشكل صحيح في مركز إدارة Attract.</span><span class="sxs-lookup"><span data-stu-id="2231c-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="2231c-113">لمزيد من المعلومات حول كيفية تغيير إعدادات LinkedIn في مركز الإدارة، راجع [إعداد التكامل مع LinkedIn لـ Microsoft Dynamics 365 Talent - Attract](attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="2231c-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract](attract-admin-linkedin.md).</span></span> <span data-ttu-id="2231c-114">لمزيد من المعلومات حول معرّفات الشركات في LinkedIn، راجع [ربط معرّف شركتك في LinkedIn بلوحة وظائف LinkedIn - الأسئلة المتداولة](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="2231c-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="2231c-115">تحقق من تفاصيل الوظيفة على LinkedIn للتأكد من إدخال عنوان كامل.</span><span class="sxs-lookup"><span data-stu-id="2231c-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="2231c-116">لنشر وظيفة بطريقة ناجحة، تحتاج LinkedIn على الأقل إلى مدينة وبلد أو منطقة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="2231c-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="2231c-117">تأكد من أن الوظيفة غير مكررة مع وظيفة أخرى تم نشرها في LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="2231c-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="2231c-118">لن تقوم LinkedIn بنشر وظائف مكررة أو إعلانات وظائف مميزة أو محدودة من LinkedIn من مصدر آخر.</span><span class="sxs-lookup"><span data-stu-id="2231c-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="2231c-119">تأكد من عدم قيام شخص آخر في شركتك بنشر الوظيفة يدويًا.</span><span class="sxs-lookup"><span data-stu-id="2231c-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="2231c-120">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="2231c-120">See also</span></span>

[<span data-ttu-id="2231c-121">الأسئلة المتداولة حول تكامل Attract مع LinkedIn</span><span class="sxs-lookup"><span data-stu-id="2231c-121">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="2231c-122">نشر الوظائف في LinkedIn من Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="2231c-122">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="2231c-123">بحث عن المرشحين باستخدام LinkedIn Recruiter في Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="2231c-123">Source candidates with LinkedIn Recruiter in Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="2231c-124">إنشاء الوظائف والموافقة عليها ونشرها في Attract</span><span class="sxs-lookup"><span data-stu-id="2231c-124">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="2231c-125">استكشاف أخطاء التكامل وإصلاحها مع LinkedIn وMicrosoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="2231c-125">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
