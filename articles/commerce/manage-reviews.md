---
title: إدارة التقييمات والمراجعات
description: يوضح هذا الموضوع كيفية إدارة التقييمات والمراجعات باستخدام أداة الإشراف على تقييمات ومراجعات Microsoft Dynamics 365 Commerce .
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698016"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="e39b2-103">إدارة التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="e39b2-103">Manage ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e39b2-104">يوضح هذا الموضوع كيفية إدارة التقييمات والمراجعات باستخدام أداة الإشراف على تقييمات ومراجعات Microsoft Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="e39b2-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="e39b2-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="e39b2-105">Overview</span></span>

<span data-ttu-id="e39b2-106">Dynamics 365 Commerce يستخدم Microsoft Azure Cognitive Service للإشراف تلقائيًا على مرجعة النصوص عن طريق تنقيح الكلمات البذيئة.</span><span class="sxs-lookup"><span data-stu-id="e39b2-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="e39b2-107">بالإضافة إلى ذلك، يمكن للمشرفين استخدام أداه التقييمات والمراجعات للمهام اليدوية التالية:</span><span class="sxs-lookup"><span data-stu-id="e39b2-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="e39b2-108">الإشراف على المراجعات بالاستجابة لها أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="e39b2-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="e39b2-109">حذف مراجعات العميل عند طلب العميل.</span><span class="sxs-lookup"><span data-stu-id="e39b2-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="e39b2-110">الاستيراد المجمع لبيانات التقييمات والمراجعات لكافة المنتجات في قالب Microsoft Power BI ، حتى يمكن تحليل اتجاهات التقييمات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="e39b2-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="e39b2-111">قراءة مراجعة</span><span class="sxs-lookup"><span data-stu-id="e39b2-111">Read a review</span></span> 

1. <span data-ttu-id="e39b2-112">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> الإشراف**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-112">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="e39b2-113">استخدم حقل البحث في الجانب الأيمن العلوي من الصفحة لتصفية المراجعات التي يتم عرضها حسب معرف المنتج أو اسم المنتج أو نص المراجعة.</span><span class="sxs-lookup"><span data-stu-id="e39b2-113">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="e39b2-114">تتيح لك عوامل التصفية الإضافية تقييد المراجعات حسب الفترة أو التقييم أو القناة أو حاله الاختصاص (الاستبعاد أو الاستجابة أو إبلاغ عنها).</span><span class="sxs-lookup"><span data-stu-id="e39b2-114">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![الصفحة الرئيسية للإشراف](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="e39b2-116">الاستجابة إلى مراجعة</span><span class="sxs-lookup"><span data-stu-id="e39b2-116">Respond to a review</span></span> 

<span data-ttu-id="e39b2-117">أحيانا، يعبر العملاء الذين اشتروا منتجًا عن رضاهم أو استياءهم ، أو لا يفهمون كيفية استخدام المنتج.</span><span class="sxs-lookup"><span data-stu-id="e39b2-117">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="e39b2-118">وكمشرف، يمكنك نشر استجابة لمراجعة ما.</span><span class="sxs-lookup"><span data-stu-id="e39b2-118">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="e39b2-119">تظهر هذه الاستجابة مع المراجعة على الموقع.</span><span class="sxs-lookup"><span data-stu-id="e39b2-119">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="e39b2-120">للاستجابة لمراجعة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e39b2-120">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="e39b2-121">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> الإشراف**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-121">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="e39b2-122">ابحث عن المراجعة التي تتطلب استجابة وحددها.</span><span class="sxs-lookup"><span data-stu-id="e39b2-122">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="e39b2-123">في جزء الخصائص الموجود على اليسار، حدد **إضافة استجابة**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-123">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="e39b2-124">أدخل نص الاستجابة والاسم الذي يجب أن يظهر للمستجيب.</span><span class="sxs-lookup"><span data-stu-id="e39b2-124">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="e39b2-125">اسم المستجيب الافتراضي هو **المشرف**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-125">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="e39b2-126">عند الانتهاء، حدد **نشر الاستجابة**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-126">When you've finished, select **Post response**.</span></span>

![الاستجابة إلى أحد المراجعات](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="e39b2-128">استبعاد مراجعة</span><span class="sxs-lookup"><span data-stu-id="e39b2-128">Take down a review</span></span> 

<span data-ttu-id="e39b2-129">في بعض الأحيان، يكون لدى شركة ما المبرر الذي يكفل للمشرفين استبعاد مراجعات العملاء.</span><span class="sxs-lookup"><span data-stu-id="e39b2-129">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="e39b2-130">لاستبعاد مراجعة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e39b2-130">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="e39b2-131">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> الإشراف**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-131">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="e39b2-132">ابحث عن المراجعة التي يجب استبعادها وحددها.</span><span class="sxs-lookup"><span data-stu-id="e39b2-132">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="e39b2-133">في جزء الخصائص الموجود علي اليسار، حدد سبب الاستبعاد، ثم حدد **استبعاد**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-133">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="e39b2-134">حذف مراجعات العميل عند طلب العميل</span><span class="sxs-lookup"><span data-stu-id="e39b2-134">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="e39b2-135">في بعض الأحيان، يرغب العملاء في حذف تقييماتهم ومراجعاتهم نهائيًا من موقع ويب خاص بالتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e39b2-135">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="e39b2-136">يمكن للمشرف الذي يتلقى طلبات إزالة من أحد العملاء إزالة بيانات العميل باستخدام ميزة "حذف مراجعة".</span><span class="sxs-lookup"><span data-stu-id="e39b2-136">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="e39b2-137">للبحث عن بيانات عميل وحذفها، يطلب المشرف عنوان البريد الإلكتروني الذي استخدمه العميل لتسجيل الدخول وتدوين مراجعات.</span><span class="sxs-lookup"><span data-stu-id="e39b2-137">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="e39b2-138">للبحث عن بيانات العميل وحذفها، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e39b2-138">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="e39b2-139">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> حذف**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-139">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="e39b2-140">في حقل **بحث عن المستخدمين باستخدام عنوان البريد الإلكتروني**، أدخل عنوان البريد الإلكتروني للعميل، ثم حدد **بحث**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-140">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="e39b2-141">إذا كان لدى العميل أي نشاط مراجعة (على سبيل المثال، إرسال مراجعات، أو التصويت على الفائدة من مراجعات عميل آخر، أو تعليقات حول مراجعة عميل آخر)، يتم عرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="e39b2-141">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="e39b2-142">يوجد زر **حذف** لكل عنصر.</span><span class="sxs-lookup"><span data-stu-id="e39b2-142">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="e39b2-143">بالنسبة لكل عنصر يجب حذفه، حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-143">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="e39b2-144">عند المطالبة بالتاكيد، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-144">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![حذف بيانات العميل](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="e39b2-146">قد يستغرق الإجراء سبعة أيام حتى يتم إزالة البيانات تمامًا من النظام.</span><span class="sxs-lookup"><span data-stu-id="e39b2-146">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="e39b2-147">يجب على المشرفين أن يعلموا العملاء بشأن هذا التأخير.</span><span class="sxs-lookup"><span data-stu-id="e39b2-147">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="e39b2-148">إذا قام العملاء بتغيير أسمائهم في إعدادات الحساب الخاصة بهم، فقد تظهر عناصر متعددة في نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="e39b2-148">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="e39b2-149">في هذه الحالة، لحذف بيانات العميل بشكل كامل، يجب على المشرف أن يحدد **حذف** لكل عنصر.</span><span class="sxs-lookup"><span data-stu-id="e39b2-149">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="e39b2-150">تنزيل بيانات التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="e39b2-150">Download ratings and reviews data</span></span>

<span data-ttu-id="e39b2-151">تتيح أداة الإشراف على التقييمات والمراجعات للمشرفين إمكانية استيراد بيانات التقييمات والمراجعات مجمّعة، بحيث يمكنهم تحليل الاتجاهات.</span><span class="sxs-lookup"><span data-stu-id="e39b2-151">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="e39b2-152">يتوفر قالب Power BI يتضمن القياسات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="e39b2-152">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="e39b2-153">يمكن للمشرفين استخدام هذا القالب للاتصال بالبيانات المستوردة المجمّعة وعرض لوحة معلومات.</span><span class="sxs-lookup"><span data-stu-id="e39b2-153">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="e39b2-154">ولا يلزمهم إنشاء لوحة معلومات مخصصة.</span><span class="sxs-lookup"><span data-stu-id="e39b2-154">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="e39b2-155">كما يمكن للمشرفين تخصيص قالب Power BI لتلبية احتياجاتهم المحددة.</span><span class="sxs-lookup"><span data-stu-id="e39b2-155">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="e39b2-156">لتحميل بيانات التقييمات والمراجعات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e39b2-156">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="e39b2-157">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> ‏‫إعداد التقارير‬‬**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-157">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="e39b2-158">حدد **تنزيل بيانات المراجعات** لتنزيل بيانات التقييمات والمراجعات بشكل مجمع بتنسيق قيم مفصولة بفواصل (CSV).</span><span class="sxs-lookup"><span data-stu-id="e39b2-158">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="e39b2-159">عرض اتجاهات التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="e39b2-159">View ratings and reviews trends</span></span>

<span data-ttu-id="e39b2-160">يمكن أن يقوم المشرفون بتنزيل قالب Power BI بحيث يمكنهم عرض الاتجاهات في لوحة معلومات.</span><span class="sxs-lookup"><span data-stu-id="e39b2-160">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="e39b2-161">لعرض اتجاهات التقييمات والمراجعات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e39b2-161">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="e39b2-162">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> ‏‫إعداد التقارير‬‬**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-162">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="e39b2-163">حدد **قالب PowerBI** لتنزيل القالب.</span><span class="sxs-lookup"><span data-stu-id="e39b2-163">Select **PowerBI template** to download the template.</span></span>

    ![تنزيل قالب Power BI](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="e39b2-165">افتح القالب الذي تم تنزيله باستخدام تطبيق Power BI.</span><span class="sxs-lookup"><span data-stu-id="e39b2-165">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="e39b2-166">قم بإغلاق مربع الحوار **الوصول إلى محتوى الويب** الذي يظهر، ثم أغلق رسالة الخطأ "تحديث" التي تظهر.</span><span class="sxs-lookup"><span data-stu-id="e39b2-166">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="e39b2-167">انتقل إلى **الصفحة الرئيسية**، وحدد **تحرير الاستعلامات**، ثم حدد **إعدادات مصدر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-167">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="e39b2-168">في مربع حوار **إعدادات مصدر البيانات**، حدد **تغيير المصدر**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-168">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="e39b2-169">في حقل **URL**، أدخل مسار بيانات المراجعات التي قمت بتنزيلها في الإجراء السابق (على سبيل المثال، **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="e39b2-169">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![حقل URL في مربع حوار القيم المفصولة بفواصل](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="e39b2-171">حدد **موافق**، ثم حدد **‏‫تطبيق التغييرات‬**.</span><span class="sxs-lookup"><span data-stu-id="e39b2-171">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="e39b2-172">سيستغرق تطبيق التغييرات علي مصدر البيانات دقيقة إلى دقيقتين.</span><span class="sxs-lookup"><span data-stu-id="e39b2-172">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="e39b2-173">حدد **ورقة الاتجاهات** لعرض اتجاهات التقييمات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="e39b2-173">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![اتجاهات التقييمات والمراجعات](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="e39b2-175">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e39b2-175">Additional resources</span></span>

[<span data-ttu-id="e39b2-176">نظرة عامة على التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="e39b2-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="e39b2-177">الموافقة على استخدام التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="e39b2-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="e39b2-178">تكوين التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="e39b2-178">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="e39b2-179">مزامنة تقييمات المنتجات في Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="e39b2-179">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
