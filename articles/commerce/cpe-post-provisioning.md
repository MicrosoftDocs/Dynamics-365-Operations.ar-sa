---
title: تكوين بيئة تقييم Dynamics 365 Commerce
description: يوضح هذا الموضوع كيفية تكوين بيئة تقييم Microsoft Dynamics 365 Commerce بعد توفيرها.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409785"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="4ce78-103">تكوين بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4ce78-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4ce78-104">يوضح هذا الموضوع كيفية تكوين بيئة تقييم Microsoft Dynamics 365 Commerce بعد توفيرها.</span><span class="sxs-lookup"><span data-stu-id="4ce78-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="4ce78-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="4ce78-105">Overview</span></span>

<span data-ttu-id="4ce78-106">لا تستكمل الإجراءات في هذا الموضوع إلا بعد توفير بيئة تقييم Commerce.</span><span class="sxs-lookup"><span data-stu-id="4ce78-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="4ce78-107">للحصول على معلومات حول كيفية توفير بيئة تقييم Commerce، راجع [توفير بيئة تقييم Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="4ce78-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="4ce78-108">بعد توفير بيئة تقييم Commerce الشاملة لديك، يجب إكمال خطوات تكوين ما بعد التوفير الإضافية قبل أن تتمكن من البدء في تقييم البيئة.</span><span class="sxs-lookup"><span data-stu-id="4ce78-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="4ce78-109">لإكمال هذه الخطوات، يجب عليك استخدام Microsoft Dynamics Lifecycle Services (LCS) وDynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4ce78-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="4ce78-110">قبل البدء</span><span class="sxs-lookup"><span data-stu-id="4ce78-110">Before you start</span></span>

1. <span data-ttu-id="4ce78-111">سجل الدخول إلى [مدخل LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="4ce78-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="4ce78-112">انتقل إلى المشروع.</span><span class="sxs-lookup"><span data-stu-id="4ce78-112">Go to your project.</span></span>
1. <span data-ttu-id="4ce78-113">في القائمة العلوية، حدد **البيئات المستضافة على السحابة**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="4ce78-114">حدد البيئة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="4ce78-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="4ce78-115">حدد **تسجيل الدخول إلى البيئة** من معلومات البيئة الموجودة على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="4ce78-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="4ce78-116">سيتم إرسالك إلى مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="4ce78-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="4ce78-117">تأكد من تحديد الكيان القانوني **USRT** في الزاوية العلوية اليمنى.</span><span class="sxs-lookup"><span data-stu-id="4ce78-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="4ce78-118">وخلال أنشطة ما بعد التوفير في مركز Commerce الرئيسي، تأكد من تحديد كيان **USRT** القانوني دائمًا.</span><span class="sxs-lookup"><span data-stu-id="4ce78-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="4ce78-119">تكوين نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="4ce78-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="4ce78-120">إقران العامل بهويتك</span><span class="sxs-lookup"><span data-stu-id="4ce78-120">Associate a worker with your identity</span></span>

<span data-ttu-id="4ce78-121">لإقران عامل بهويتك، اتبع الخطوات التالية في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="4ce78-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="4ce78-122">باستخدام القائمة الموجودة على الجانب الأيسر للانتقال إلى **الوحدات النمطية \> Retail وcommerce \> الموظفون \> العاملون**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="4ce78-123">في القائمة، قم بالبحث عن السجل التالي: **000713 - Andrew Collette‬‏‫**‬‏‫ وحدده.‬</span><span class="sxs-lookup"><span data-stu-id="4ce78-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="4ce78-124">في جزء الإجراءات، حدد **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="4ce78-125">حدد **الإقران بهوية موجودة**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="4ce78-126">في حقل **البريد الإلكتروني** إلى يمين **‏‫البحث باستخدام البريد الإلكتروني‬**، أدخل عنوان بريدك الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="4ce78-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="4ce78-127">حدد **بحث**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-127">Select **Search**.</span></span>
1. <span data-ttu-id="4ce78-128">حدد السجل الذي يتضمن اسمك.</span><span class="sxs-lookup"><span data-stu-id="4ce78-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="4ce78-129">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-129">Select **OK**.</span></span>
1. <span data-ttu-id="4ce78-130">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="4ce78-131">تنشيط نقطة بيع مجموعة النظراء</span><span class="sxs-lookup"><span data-stu-id="4ce78-131">Activate Cloud POS</span></span>

<span data-ttu-id="4ce78-132">لتنشيط ‏‫نقطة البيع السحابية، اتبع هذه الخطوات في LCS.</span><span class="sxs-lookup"><span data-stu-id="4ce78-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="4ce78-133">في القائمة العلوية، حدد **البيئات المستضافة على السحابة**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="4ce78-134">حدد البيئة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="4ce78-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="4ce78-135">حدد **تسجيل الدخول إلى نقطة البيع السحابية** من معلومات البيئة الموجودة على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="4ce78-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="4ce78-136">حدد **التالي** لفتح مربع الحوار **‏‫قبل البدء‬**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="4ce78-137">اترك حقل **عنوان URL الخادم** كما هو.</span><span class="sxs-lookup"><span data-stu-id="4ce78-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="4ce78-138">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-138">Select **Next**.</span></span>
1. <span data-ttu-id="4ce78-139">تسجيل الدخول باستخدام حساب Microsoft Azure Active Directory (Azure AD) .</span><span class="sxs-lookup"><span data-stu-id="4ce78-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="4ce78-140">ضمن **اسم المتجر**، حدد **سان فرانسيسكو**، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="4ce78-141">ضمن **‏‫السجل والجهاز‬**، حدد **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="4ce78-142">حدد **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-142">Select **Activate**.</span></span> <span data-ttu-id="4ce78-143">لقد قمت بتسجيل الخروج وانتقلت إلى صفحة تسجيل الدخول إلى نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="4ce78-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="4ce78-144">يمكنك الآن تسجيل الدخول إلى ‏‫تجربة ‏‫نقطة بيع المجموعة‬‬ باستخدام معرف العامل **000713** وكلمة المرور **123**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="4ce78-145">قم بإعداد موقعك في التجارة</span><span class="sxs-lookup"><span data-stu-id="4ce78-145">Set up your site in Commerce</span></span>

<span data-ttu-id="4ce78-146">للبدء في إعداد موقع التقييم في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="4ce78-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="4ce78-147">سجِّل الدخول إلى منشئ موقع Commerce باستخدام عنوان URL الذي قمت بتدوينه عندما قمت بتهيئة التجارة الإلكترونية أثناء التوفير (راجع [تهيئة التجارة الإلكترونية](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="4ce78-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="4ce78-148">حدد موقع **‏‫شركة الاتحاد للتصنيع‬** لفتح مربع حوار إعداد الموقع.</span><span class="sxs-lookup"><span data-stu-id="4ce78-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="4ce78-149">حدد المجال الذي قمت بإدخاله عند تهيئة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="4ce78-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="4ce78-150">حدد **متجر ‏‫شركة الاتحاد للتصنيع‬ الموسّع على الإنترنت** كقناة افتراضية.</span><span class="sxs-lookup"><span data-stu-id="4ce78-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="4ce78-151">(تأكد من تحديد المتجر **الموسع** على الإنترنت.)</span><span class="sxs-lookup"><span data-stu-id="4ce78-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="4ce78-152">حدد **en-us** بصفتها اللغة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="4ce78-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="4ce78-153">اترك قيمه حقل **المسار** كما هو.</span><span class="sxs-lookup"><span data-stu-id="4ce78-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="4ce78-154">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-154">Select **OK**.</span></span> <span data-ttu-id="4ce78-155">تظهر قائمة الصفحات على الموقع.</span><span class="sxs-lookup"><span data-stu-id="4ce78-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="4ce78-156">تمكين الوظائف</span><span class="sxs-lookup"><span data-stu-id="4ce78-156">Enable jobs</span></span>

<span data-ttu-id="4ce78-157">لتمكين الوظائف في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="4ce78-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="4ce78-158">تسجيل الدخول إلى البيئة (HQ).</span><span class="sxs-lookup"><span data-stu-id="4ce78-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="4ce78-159">باستخدام القائمة الموجودة علي الجانب الأيسر ، انتقل إلى **Retail وcommerce \> الاستعلامات والتقارير \> الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="4ce78-160">يجب إكمال الخطوات المتبقية من هذا الإجراء لكل من الوظائف التالية:</span><span class="sxs-lookup"><span data-stu-id="4ce78-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="4ce78-161">معالجة إخطار البريد الإلكتروني للبيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="4ce78-161">Process retail order email notification</span></span>
    * <span data-ttu-id="4ce78-162">توفر المنتجات</span><span class="sxs-lookup"><span data-stu-id="4ce78-162">Product availability</span></span>
    * <span data-ttu-id="4ce78-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="4ce78-163">P-0001</span></span>
    * <span data-ttu-id="4ce78-164">مزامنة وظيفة الأوامر</span><span class="sxs-lookup"><span data-stu-id="4ce78-164">Synchronize orders job</span></span>

1. <span data-ttu-id="4ce78-165">استخدم عامل التصفية السريع للبحث عن الوظيفة باستخدام الاسم.</span><span class="sxs-lookup"><span data-stu-id="4ce78-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="4ce78-166">إذا كانت حالة الوظيفة **‏‫قيد التنفيذ‬**، فاتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="4ce78-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="4ce78-167">حدد السجل.</span><span class="sxs-lookup"><span data-stu-id="4ce78-167">Select the record.</span></span>
    1. <span data-ttu-id="4ce78-168">في جزء الإجراءات، انقر فوق علامة التبويب **وظيفة دفعية** ، حدد **حالة التغيير**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="4ce78-169">حدد **إلغاء**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="4ce78-170">يمكنك أيضًا تعيين فترة التكرار إلى دقيقة واحدة (1) للوظائف التالية اختياريًا:</span><span class="sxs-lookup"><span data-stu-id="4ce78-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="4ce78-171">معالجة وظيفة إخطار البريد الإلكتروني لأمر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="4ce78-171">Process retail order email notification job</span></span>
* <span data-ttu-id="4ce78-172">الوظيفة P-0001</span><span class="sxs-lookup"><span data-stu-id="4ce78-172">P-0001 job</span></span>
* <span data-ttu-id="4ce78-173">مزامنة وظيفة الأوامر</span><span class="sxs-lookup"><span data-stu-id="4ce78-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="4ce78-174">تشغيل مزامنة البيانات بالكامل</span><span class="sxs-lookup"><span data-stu-id="4ce78-174">Run full data synchronization</span></span>

<span data-ttu-id="4ce78-175">لتشغيل مزامنة البيانات الكاملة في Commerce، اتبع الخطوات التالية في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="4ce78-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="4ce78-176">باستخدام القائمة الموجودة على اليسار، للانتقال إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة‬ \> ‏‫إعداد المراكز الرئيسية \> مجدول التجارة \> ‏‫قاعدة بيانات القناة‬**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="4ce78-177">حدد القناة بالاسم **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="4ce78-178">في جزء الإجراءات، حدد **مزامنة البيانات بالكامل**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="4ce78-179">أدخل **9999** لجدول لتوزيع.</span><span class="sxs-lookup"><span data-stu-id="4ce78-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="4ce78-180">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-180">Select **OK**.</span></span>
1. <span data-ttu-id="4ce78-181">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4ce78-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="4ce78-182">اختبار معلومات بطاقة الائتمان لإجراء عمليات شراء تجريبية</span><span class="sxs-lookup"><span data-stu-id="4ce78-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="4ce78-183">لإجراء حركات الاختبار على الموقع، يمكنك استخدام معلومات بطاقة ائتمان التجريبية التالية:</span><span class="sxs-lookup"><span data-stu-id="4ce78-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="4ce78-184">**رقم البطاقة:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="4ce78-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="4ce78-185">**تاريخ انتهاء الصلاحية:** 10/20</span><span class="sxs-lookup"><span data-stu-id="4ce78-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="4ce78-186">**‏‫كود قيمة التحقق من البطاقة (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="4ce78-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ce78-187">لا تحاول أبدا، تحت أي ظرف من الظروف، استخدام معلومات بطاقة الائتمان الفعلية في موقع الاختبار.</span><span class="sxs-lookup"><span data-stu-id="4ce78-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4ce78-188">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="4ce78-188">Next steps</span></span>

<span data-ttu-id="4ce78-189">بعد الانتهاء من خطوات التوفير والتكوين، يمكنك بدء استخدام بيئة التقييم.</span><span class="sxs-lookup"><span data-stu-id="4ce78-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="4ce78-190">استخدم عنوان URL لمنشئ مواقع Commerce للانتقال إلى تجربة التأليف.</span><span class="sxs-lookup"><span data-stu-id="4ce78-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="4ce78-191">استخدم عنوان URL لموقع Commerce للانتقال إلى تجربة موقع عميل البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="4ce78-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="4ce78-192">لتكوين الميزات الاختيارية لبيئة تقييم Commerce، راجع [تكوين الميزات الاختيارية لبيئة تقييم Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="4ce78-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ce78-193">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4ce78-193">Additional resources</span></span>

[<span data-ttu-id="4ce78-194">نظرة عامة على بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4ce78-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="4ce78-195">توفير بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4ce78-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="4ce78-196">تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4ce78-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="4ce78-197">تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4ce78-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="4ce78-198">الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4ce78-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="4ce78-199">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="4ce78-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="4ce78-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="4ce78-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="4ce78-201">مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4ce78-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="4ce78-202">موقع ويب Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4ce78-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
