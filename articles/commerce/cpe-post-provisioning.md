---
title: تكوين بيئة تقييم Dynamics 365 Commerce
description: يوضح هذا الموضوع كيفية تكوين بيئة تقييم Microsoft Dynamics 365 Commerce بعد توفيرها.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e80830a1cb0864c7eef19857b91e36ad27cdef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795849"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="94778-103">تكوين بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="94778-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94778-104">يوضح هذا الموضوع كيفية تكوين بيئة تقييم Microsoft Dynamics 365 Commerce بعد توفيرها.</span><span class="sxs-lookup"><span data-stu-id="94778-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="94778-105">لا تستكمل الإجراءات في هذا الموضوع إلا بعد توفير بيئة تقييم Commerce.</span><span class="sxs-lookup"><span data-stu-id="94778-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="94778-106">للحصول على معلومات حول كيفية توفير بيئة تقييم Commerce، راجع [توفير بيئة تقييم Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="94778-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="94778-107">بعد توفير بيئة تقييم Commerce الشاملة لديك، يجب إكمال خطوات تكوين ما بعد التوفير الإضافية قبل أن تتمكن من البدء في تقييم البيئة.</span><span class="sxs-lookup"><span data-stu-id="94778-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="94778-108">لإكمال هذه الخطوات، يجب عليك استخدام Microsoft Dynamics Lifecycle Services (LCS) وDynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="94778-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="94778-109">قبل البدء</span><span class="sxs-lookup"><span data-stu-id="94778-109">Before you start</span></span>

1. <span data-ttu-id="94778-110">سجل الدخول إلى [مدخل LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="94778-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="94778-111">انتقل إلى المشروع.</span><span class="sxs-lookup"><span data-stu-id="94778-111">Go to your project.</span></span>
1. <span data-ttu-id="94778-112">في القائمة العلوية، حدد **البيئات المستضافة على السحابة**.</span><span class="sxs-lookup"><span data-stu-id="94778-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="94778-113">حدد البيئة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="94778-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="94778-114">حدد **تسجيل الدخول إلى البيئة** من معلومات البيئة الموجودة على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="94778-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="94778-115">سيتم إرسالك إلى مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="94778-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="94778-116">تأكد من تحديد الكيان القانوني **USRT** في الزاوية العلوية اليمنى.</span><span class="sxs-lookup"><span data-stu-id="94778-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="94778-117">وخلال أنشطة ما بعد التوفير في مركز Commerce الرئيسي، تأكد من تحديد كيان **USRT** القانوني دائمًا.</span><span class="sxs-lookup"><span data-stu-id="94778-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="94778-118">تكوين نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="94778-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="94778-119">إقران العامل بهويتك</span><span class="sxs-lookup"><span data-stu-id="94778-119">Associate a worker with your identity</span></span>

<span data-ttu-id="94778-120">لإقران عامل بهويتك، اتبع الخطوات التالية في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="94778-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="94778-121">باستخدام القائمة الموجودة على الجانب الأيسر للانتقال إلى **الوحدات النمطية \> Retail وcommerce \> الموظفون \> العاملون**.</span><span class="sxs-lookup"><span data-stu-id="94778-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="94778-122">في القائمة، قم بالبحث عن السجل التالي: **000713 - Andrew Collette‬‏‫**‬‏‫ وحدده.‬</span><span class="sxs-lookup"><span data-stu-id="94778-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="94778-123">في جزء الإجراءات، حدد **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="94778-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="94778-124">حدد **الإقران بهوية موجودة**.</span><span class="sxs-lookup"><span data-stu-id="94778-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="94778-125">في حقل **البريد الإلكتروني** إلى يمين **‏‫البحث باستخدام البريد الإلكتروني‬**، أدخل عنوان بريدك الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="94778-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="94778-126">حدد **بحث**.</span><span class="sxs-lookup"><span data-stu-id="94778-126">Select **Search**.</span></span>
1. <span data-ttu-id="94778-127">حدد السجل الذي يتضمن اسمك.</span><span class="sxs-lookup"><span data-stu-id="94778-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="94778-128">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="94778-128">Select **OK**.</span></span>
1. <span data-ttu-id="94778-129">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="94778-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="94778-130">تنشيط نقطة بيع مجموعة النظراء</span><span class="sxs-lookup"><span data-stu-id="94778-130">Activate Cloud POS</span></span>

<span data-ttu-id="94778-131">لتنشيط ‏‫نقطة البيع السحابية، اتبع هذه الخطوات في LCS.</span><span class="sxs-lookup"><span data-stu-id="94778-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="94778-132">في القائمة العلوية، حدد **البيئات المستضافة على السحابة**.</span><span class="sxs-lookup"><span data-stu-id="94778-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="94778-133">حدد البيئة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="94778-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="94778-134">حدد **تسجيل الدخول إلى نقطة البيع السحابية** من معلومات البيئة الموجودة على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="94778-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="94778-135">حدد **التالي** لفتح مربع الحوار **‏‫قبل البدء‬**.</span><span class="sxs-lookup"><span data-stu-id="94778-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="94778-136">اترك حقل **عنوان URL الخادم** كما هو.</span><span class="sxs-lookup"><span data-stu-id="94778-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="94778-137">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="94778-137">Select **Next**.</span></span>
1. <span data-ttu-id="94778-138">تسجيل الدخول باستخدام حساب Microsoft Azure Active Directory (Azure AD) .</span><span class="sxs-lookup"><span data-stu-id="94778-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="94778-139">ضمن **اسم المتجر**، حدد **سان فرانسيسكو**، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="94778-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="94778-140">ضمن **‏‫السجل والجهاز‬**، حدد **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="94778-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="94778-141">حدد **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="94778-141">Select **Activate**.</span></span> <span data-ttu-id="94778-142">لقد قمت بتسجيل الخروج وانتقلت إلى صفحة تسجيل الدخول إلى نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="94778-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="94778-143">يمكنك الآن تسجيل الدخول إلى ‏‫تجربة ‏‫نقطة بيع المجموعة‬‬ باستخدام معرف العامل **000713** وكلمة المرور **123**.</span><span class="sxs-lookup"><span data-stu-id="94778-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="94778-144">قم بإعداد موقعك في التجارة</span><span class="sxs-lookup"><span data-stu-id="94778-144">Set up your site in Commerce</span></span>

<span data-ttu-id="94778-145">للبدء في إعداد موقع التقييم في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="94778-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="94778-146">سجِّل الدخول إلى منشئ موقع Commerce باستخدام عنوان URL الذي قمت بتدوينه عندما قمت بتهيئة التجارة الإلكترونية أثناء التوفير (راجع [تهيئة التجارة الإلكترونية](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="94778-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="94778-147">حدد موقع **‏‫شركة الاتحاد للتصنيع‬** لفتح مربع حوار إعداد الموقع.</span><span class="sxs-lookup"><span data-stu-id="94778-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="94778-148">حدد المجال الذي قمت بإدخاله عند تهيئة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="94778-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="94778-149">حدد **متجر ‏‫شركة الاتحاد للتصنيع‬ الموسّع على الإنترنت** كقناة افتراضية.</span><span class="sxs-lookup"><span data-stu-id="94778-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="94778-150">(تأكد من تحديد المتجر **الموسع** على الإنترنت.)</span><span class="sxs-lookup"><span data-stu-id="94778-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="94778-151">حدد **en-us** بصفتها اللغة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="94778-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="94778-152">اترك قيمه حقل **المسار** كما هو.</span><span class="sxs-lookup"><span data-stu-id="94778-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="94778-153">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="94778-153">Select **OK**.</span></span> <span data-ttu-id="94778-154">تظهر قائمة الصفحات على الموقع.</span><span class="sxs-lookup"><span data-stu-id="94778-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="94778-155">تمكين الوظائف</span><span class="sxs-lookup"><span data-stu-id="94778-155">Enable jobs</span></span>

<span data-ttu-id="94778-156">لتمكين الوظائف في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="94778-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="94778-157">تسجيل الدخول إلى البيئة (HQ).</span><span class="sxs-lookup"><span data-stu-id="94778-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="94778-158">باستخدام القائمة الموجودة علي الجانب الأيسر ، انتقل إلى **Retail وcommerce \> الاستعلامات والتقارير \> الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="94778-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="94778-159">يجب إكمال الخطوات المتبقية من هذا الإجراء لكل من الوظائف التالية:</span><span class="sxs-lookup"><span data-stu-id="94778-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="94778-160">معالجة إخطار البريد الإلكتروني للبيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="94778-160">Process retail order email notification</span></span>
    * <span data-ttu-id="94778-161">توفر المنتجات</span><span class="sxs-lookup"><span data-stu-id="94778-161">Product availability</span></span>
    * <span data-ttu-id="94778-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="94778-162">P-0001</span></span>
    * <span data-ttu-id="94778-163">مزامنة وظيفة الأوامر</span><span class="sxs-lookup"><span data-stu-id="94778-163">Synchronize orders job</span></span>

1. <span data-ttu-id="94778-164">استخدم عامل التصفية السريع للبحث عن الوظيفة باستخدام الاسم.</span><span class="sxs-lookup"><span data-stu-id="94778-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="94778-165">إذا كانت حالة الوظيفة **‏‫قيد التنفيذ‬**، فاتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="94778-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="94778-166">حدد السجل.</span><span class="sxs-lookup"><span data-stu-id="94778-166">Select the record.</span></span>
    1. <span data-ttu-id="94778-167">في جزء الإجراءات، انقر فوق علامة التبويب **وظيفة دفعية** ، حدد **حالة التغيير**.</span><span class="sxs-lookup"><span data-stu-id="94778-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="94778-168">حدد **إلغاء**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="94778-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="94778-169">يمكنك أيضًا تعيين فترة التكرار إلى دقيقة واحدة (1) للوظائف التالية اختياريًا:</span><span class="sxs-lookup"><span data-stu-id="94778-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="94778-170">معالجة وظيفة إخطار البريد الإلكتروني لأمر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="94778-170">Process retail order email notification job</span></span>
* <span data-ttu-id="94778-171">الوظيفة P-0001</span><span class="sxs-lookup"><span data-stu-id="94778-171">P-0001 job</span></span>
* <span data-ttu-id="94778-172">مزامنة وظيفة الأوامر</span><span class="sxs-lookup"><span data-stu-id="94778-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="94778-173">تشغيل مزامنة البيانات بالكامل</span><span class="sxs-lookup"><span data-stu-id="94778-173">Run full data synchronization</span></span>

<span data-ttu-id="94778-174">لتشغيل مزامنة البيانات الكاملة في Commerce، اتبع الخطوات التالية في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="94778-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="94778-175">باستخدام القائمة الموجودة على اليسار، للانتقال إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة‬ \> ‏‫إعداد المراكز الرئيسية \> مجدول التجارة \> ‏‫قاعدة بيانات القناة‬**.</span><span class="sxs-lookup"><span data-stu-id="94778-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="94778-176">حدد القناة بالاسم **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="94778-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="94778-177">في جزء الإجراءات، حدد **مزامنة البيانات بالكامل**.</span><span class="sxs-lookup"><span data-stu-id="94778-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="94778-178">أدخل **9999** لجدول لتوزيع.</span><span class="sxs-lookup"><span data-stu-id="94778-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="94778-179">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="94778-179">Select **OK**.</span></span>
1. <span data-ttu-id="94778-180">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="94778-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="94778-181">اختبار معلومات بطاقة الائتمان لإجراء عمليات شراء تجريبية</span><span class="sxs-lookup"><span data-stu-id="94778-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="94778-182">لإجراء حركات الاختبار على الموقع، يمكنك استخدام معلومات بطاقة ائتمان التجريبية التالية:</span><span class="sxs-lookup"><span data-stu-id="94778-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="94778-183">**رقم البطاقة:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="94778-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="94778-184">**تاريخ انتهاء الصلاحية:** 10/20</span><span class="sxs-lookup"><span data-stu-id="94778-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="94778-185">**‏‫كود قيمة التحقق من البطاقة (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="94778-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94778-186">لا تحاول أبدا، تحت أي ظرف من الظروف، استخدام معلومات بطاقة الائتمان الفعلية في موقع الاختبار.</span><span class="sxs-lookup"><span data-stu-id="94778-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="94778-187">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="94778-187">Next steps</span></span>

<span data-ttu-id="94778-188">بعد الانتهاء من خطوات التوفير والتكوين، يمكنك بدء استخدام بيئة التقييم.</span><span class="sxs-lookup"><span data-stu-id="94778-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="94778-189">استخدم عنوان URL لمنشئ مواقع Commerce للانتقال إلى تجربة التأليف.</span><span class="sxs-lookup"><span data-stu-id="94778-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="94778-190">استخدم عنوان URL لموقع Commerce للانتقال إلى تجربة موقع عميل البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="94778-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="94778-191">لتكوين الميزات الاختيارية لبيئة تقييم Commerce، راجع [تكوين الميزات الاختيارية لبيئة تقييم Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="94778-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94778-192">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="94778-192">Additional resources</span></span>

[<span data-ttu-id="94778-193">نظرة عامة على بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="94778-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="94778-194">توفير بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="94778-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="94778-195">تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="94778-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="94778-196">تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="94778-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="94778-197">الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="94778-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="94778-198">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="94778-198">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="94778-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="94778-199">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="94778-200">مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="94778-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="94778-201">موقع ويب Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="94778-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
