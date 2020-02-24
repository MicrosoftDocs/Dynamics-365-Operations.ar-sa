---
title: تكوين بيئة معاينة Dynamics 365 Commerce
description: يشرح هذا الموضوع كيفية تكوين الميزات الاختيارية لبيئة معاينة Microsoft Dynamics 365 Commerce بعد توفيرها.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.openlocfilehash: 12d3a86698e9250f5d1645de51e0749c8d929f75
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024696"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="615af-103">تكوين بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="615af-103">Configure a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="615af-104">يشرح هذا الموضوع كيفية تكوين الميزات الاختيارية لبيئة معاينة Microsoft Dynamics 365 Commerce بعد توفيرها.</span><span class="sxs-lookup"><span data-stu-id="615af-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="615af-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="615af-105">Overview</span></span>

<span data-ttu-id="615af-106">أكمل الإجراءات في هذا الموضوع فقط بعد توفير بيئة معاينة التجارة.</span><span class="sxs-lookup"><span data-stu-id="615af-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="615af-107">للحصول على معلومات حول كيفية توفير بيئة معاينة التجارة، راجع [توفير بيئة معاينة التجارة](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="615af-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="615af-108">بعد توفير بيئة معاينة التجارة الشاملة الخاصة بك، يجب إكمال خطوات تكوين ما بعد التوفير الإضافية قبل أن تتمكن من البدء في تقييم البيئة.</span><span class="sxs-lookup"><span data-stu-id="615af-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="615af-109">لإكمال هذه الخطوات، يجب عليك استخدام Microsoft Dynamics Lifecycle Services (LCS) و Dynamics 365 Commerce، و Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="615af-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="615af-110">قبل البدء</span><span class="sxs-lookup"><span data-stu-id="615af-110">Before you start</span></span>

1. <span data-ttu-id="615af-111">سجل الدخول إلى [مدخل LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="615af-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="615af-112">انتقل إلى المشروع.</span><span class="sxs-lookup"><span data-stu-id="615af-112">Go to your project.</span></span>
1. <span data-ttu-id="615af-113">في القائمة العلوية، حدد **البيئات المستضافة على السحابة**.</span><span class="sxs-lookup"><span data-stu-id="615af-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="615af-114">حدد البيئة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="615af-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="615af-115">حدد **كل التفاصيل** من معلومات البيئة الموجودة على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="615af-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="615af-116">حدد **تسجيل الدخول** لفتح قائمة، وحدد **تسجيل الدخول إلى البيئة**.</span><span class="sxs-lookup"><span data-stu-id="615af-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="615af-117">تأكد من تحديد الكيان القانوني **USRT** في الزاوية العلوية اليمنى.</span><span class="sxs-lookup"><span data-stu-id="615af-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="615af-118">تكوين نقطة البيع في LCS</span><span class="sxs-lookup"><span data-stu-id="615af-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="615af-119">إقران العامل بهويتك</span><span class="sxs-lookup"><span data-stu-id="615af-119">Associate a worker with your identity</span></span>

<span data-ttu-id="615af-120">لإقران عامل بهويتك في LCS، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="615af-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="615af-121">باستخدام القائمة الموجودة على الجانب الأيسر للانتقال إلى **الوحدات النمطية \> ‏‫‏‫البيع بالتجزئة \> الموظفون \> العاملون**.</span><span class="sxs-lookup"><span data-stu-id="615af-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="615af-122">في القائمة، قم بالبحث عن السجل التالي: **000713 - Andrew Collette‬‏‫**‬‏‫ وحدده.‬</span><span class="sxs-lookup"><span data-stu-id="615af-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="615af-123">في جزء الإجراءات، حدد **البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="615af-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="615af-124">حدد **الإقران بهوية موجودة**.</span><span class="sxs-lookup"><span data-stu-id="615af-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="615af-125">في حقل **البريد الإلكتروني** إلى يمين **‏‫البحث باستخدام البريد الإلكتروني‬**، أدخل عنوان بريدك الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="615af-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="615af-126">حدد **بحث**.</span><span class="sxs-lookup"><span data-stu-id="615af-126">Select **Search**.</span></span>
1. <span data-ttu-id="615af-127">حدد السجل الذي يتضمن اسمك.</span><span class="sxs-lookup"><span data-stu-id="615af-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="615af-128">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="615af-128">Select **OK**.</span></span>
1. <span data-ttu-id="615af-129">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="615af-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="615af-130">تنشيط نقطة بيع مجموعة النظراء</span><span class="sxs-lookup"><span data-stu-id="615af-130">Activate Cloud POS</span></span>

<span data-ttu-id="615af-131">لتنشيط ‏‫نقطة بيع المجموعة في LCS، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="615af-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="615af-132">في القائمة العلوية، حدد **البيئات المستضافة على السحابة**.</span><span class="sxs-lookup"><span data-stu-id="615af-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="615af-133">حدد البيئة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="615af-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="615af-134">حدد **كل التفاصيل** من معلومات البيئة الموجودة على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="615af-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="615af-135">حدد **تسجيل الدخول** لفتح أحدي القوائم، ثم حدد **تسجيل الدخول إلى ‏‫نقطة بيع المجموعة** لفتح نقطه البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="615af-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="615af-136">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="615af-136">Select **Next**.</span></span>
1. <span data-ttu-id="615af-137">تسجيل الدخول باستخدام حساب Microsoft Azure Active Directory (Azure AD) .</span><span class="sxs-lookup"><span data-stu-id="615af-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="615af-138">ضمن **اسم المخزن**، حدد **سان فرانسيسكو**.</span><span class="sxs-lookup"><span data-stu-id="615af-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="615af-139">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="615af-139">Select **Next**.</span></span>
1. <span data-ttu-id="615af-140">ضمن **‏‫السجل والجهاز‬**، حدد **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="615af-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="615af-141">حدد **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="615af-141">Select **Activate**.</span></span> <span data-ttu-id="615af-142">لقد قمت بتسجيل الخروج وانتقلت إلى صفحة تسجيل الدخول إلى نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="615af-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="615af-143">يمكنك الآن تسجيل الدخول إلى ‏‫تجربة ‏‫نقطة بيع المجموعة‬‬ باستخدام معرف العامل **000713** وكلمة المرور **123**.</span><span class="sxs-lookup"><span data-stu-id="615af-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="615af-144">قم بإعداد موقعك في التجارة</span><span class="sxs-lookup"><span data-stu-id="615af-144">Set up your site in Commerce</span></span>

<span data-ttu-id="615af-145">للبدء في إعداد موقع المعاينة في التجارة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="615af-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="615af-146">قم بتسجيل الدخول إلى أداة إدارة موقع التجارة باستخدام عنوان URL الذي قمت بتدوينه عندما قمت بتهيئة التجارة الإلكترونية أثناء التزويد (راجع [تهيئة التجارة الإلكترونية](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="615af-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="615af-147">حدد موقع **‏‫شركة الاتحاد للتصنيع‬** لفتح مربع حوار إعداد الموقع.</span><span class="sxs-lookup"><span data-stu-id="615af-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="615af-148">حدد المجال الذي قمت بإدخاله عند تهيئة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="615af-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="615af-149">حدد **متجر ‏‫شركة الاتحاد للتصنيع‬ الموسّع على الإنترنت** كقناة افتراضية.</span><span class="sxs-lookup"><span data-stu-id="615af-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="615af-150">(تأكد من تحديد المتجر **الموسع** على الإنترنت.)</span><span class="sxs-lookup"><span data-stu-id="615af-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="615af-151">حدد **en-us** بصفتها اللغة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="615af-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="615af-152">اترك قيمه حقل **المسار** كما هو.</span><span class="sxs-lookup"><span data-stu-id="615af-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="615af-153">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="615af-153">Select **OK**.</span></span> <span data-ttu-id="615af-154">تظهر قائمة الصفحات على الموقع.</span><span class="sxs-lookup"><span data-stu-id="615af-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="615af-155">تمكين الوظائف في البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="615af-155">Enable jobs in Retail</span></span>

<span data-ttu-id="615af-156">لتمكين الوظائف في البيع بالتجزئة ، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="615af-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="615af-157">تسجيل الدخول إلى البيئة (HQ).</span><span class="sxs-lookup"><span data-stu-id="615af-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="615af-158">باستخدام القائمة الموجودة علي الجانب الأيسر ، انتقل إلى **البيع بالتجزئة \> الاستعلامات والتقارير \> الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="615af-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="615af-159">يجب إكمال الخطوات المتبقية من هذا الإجراء لكل من الوظائف التالية:</span><span class="sxs-lookup"><span data-stu-id="615af-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="615af-160">معالجة إخطار البريد الإلكتروني للبيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="615af-160">Process retail order email notification</span></span>
    * <span data-ttu-id="615af-161">توفر المنتجات</span><span class="sxs-lookup"><span data-stu-id="615af-161">Product availability</span></span>
    * <span data-ttu-id="615af-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="615af-162">P-0001</span></span>
    * <span data-ttu-id="615af-163">مزامنة وظيفة الأوامر</span><span class="sxs-lookup"><span data-stu-id="615af-163">Synchronize orders job</span></span>

1. <span data-ttu-id="615af-164">استخدم عامل التصفية السريع للبحث عن الوظيفة باستخدام الاسم.</span><span class="sxs-lookup"><span data-stu-id="615af-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="615af-165">إذا كانت حالة الوظيفة **اقتطاع**، فاتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="615af-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="615af-166">حدد السجل.</span><span class="sxs-lookup"><span data-stu-id="615af-166">Select the record.</span></span>
    1. <span data-ttu-id="615af-167">في جزء الإجراءات، انقر فوق علامة التبويب **وظيفة دفعية** ، حدد **حالة التغيير**.</span><span class="sxs-lookup"><span data-stu-id="615af-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="615af-168">حدد **‏‫جارٍ الانتظار‬**، ثم قم بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="615af-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="615af-169">تشغيل مزامنة البيانات الكاملة في البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="615af-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="615af-170">لتشغيل مزامنة البيانات الكاملة في البيع بالتجزئة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="615af-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="615af-171">باستخدام القائمة الموجودة على اليسار، للانتقال إلى **الوحدات النمطية \> البيع بالتجزئة \> ‏‫إعداد المراكز الرئيسية \> مجدول Retail \> ‏‫قاعدة بيانات القناة‬**.</span><span class="sxs-lookup"><span data-stu-id="615af-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="615af-172">من القائمة الموجودة على اليسار، حدد القناة **الافتراضية** .</span><span class="sxs-lookup"><span data-stu-id="615af-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="615af-173">حدد القناة الأخرى المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="615af-173">Select the other available channel.</span></span> <span data-ttu-id="615af-174">تسمي هذه القناة **scxxxxxxxxx**.</span><span class="sxs-lookup"><span data-stu-id="615af-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="615af-175">في جزء الإجراءات، حدد **مزامنة البيانات بالكامل**.</span><span class="sxs-lookup"><span data-stu-id="615af-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="615af-176">أدخل **9999** لجدول لتوزيع.</span><span class="sxs-lookup"><span data-stu-id="615af-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="615af-177">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="615af-177">Select **OK**.</span></span>
1. <span data-ttu-id="615af-178">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="615af-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="615af-179">اختبار معلومات بطاقة الائتمان لإجراء عمليات شراء تجريبية</span><span class="sxs-lookup"><span data-stu-id="615af-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="615af-180">لإجراء حركات الاختبار على الموقع، يمكنك استخدام معلومات بطاقة ائتمان التجريبية التالية:</span><span class="sxs-lookup"><span data-stu-id="615af-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="615af-181">**رقم البطاقة:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="615af-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="615af-182">**تاريخ انتهاء الصلاحية:** 10/20</span><span class="sxs-lookup"><span data-stu-id="615af-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="615af-183">**‏‫كود قيمة التحقق من البطاقة (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="615af-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="615af-184">لا تحاول أبدا، تحت أي ظرف من الظروف، استخدام معلومات بطاقة الائتمان الفعلية في موقع الاختبار.</span><span class="sxs-lookup"><span data-stu-id="615af-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="615af-185">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="615af-185">Next steps</span></span>

<span data-ttu-id="615af-186">بعد الانتهاء من خطوات تشغيل الخدمة والتكون، تكون مستعدًا لتقييم بيئة المعاينة.</span><span class="sxs-lookup"><span data-stu-id="615af-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="615af-187">استخدم عنوان URL الخاص بأداة إدارة موقع التجارة للانتقال إلى تجربة التأليف.</span><span class="sxs-lookup"><span data-stu-id="615af-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="615af-188">استخدم عنوان URL لموقع التجارة للانتقال إلى تجربة موقع عميل البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="615af-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="615af-189">للحصول علي معلومات حول كيفية تكوين الميزات الاختيارية لبيئة معاينة التجارة، راجع [تكوين الميزات الاختيارية لبيئة معاينة التجارة](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="615af-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="615af-190">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="615af-190">Additional resources</span></span>

[<span data-ttu-id="615af-191">نظرة عامة على بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="615af-191">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="615af-192">تشغيل بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="615af-192">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="615af-193">تكوين ميزات اختيارية لبيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="615af-193">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="615af-194">الأسئلة المتداولة حول بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="615af-194">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="615af-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="615af-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="615af-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="615af-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="615af-197">مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="615af-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="615af-198">موقع ويب Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="615af-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
