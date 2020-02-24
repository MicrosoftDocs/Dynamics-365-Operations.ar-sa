---
title: إدارة التقييمات والمراجعات
description: يوضح هذا الموضوع كيفية إدارة التقييمات والمراجعات باستخدام أداة الإشراف على تقييمات ومراجعات Microsoft Dynamics 365 Commerce .
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
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
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027232"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="33383-103">إدارة التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="33383-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33383-104">يوضح هذا الموضوع كيفية إدارة التقييمات والمراجعات باستخدام أداة الإشراف على تقييمات ومراجعات Microsoft Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="33383-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="33383-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="33383-105">Overview</span></span>

<span data-ttu-id="33383-106">Dynamics 365 Commerce يستخدم Microsoft Azure Cognitive Service للإشراف تلقائيًا على مرجعة النصوص عن طريق تنقيح الكلمات البذيئة.</span><span class="sxs-lookup"><span data-stu-id="33383-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="33383-107">بالإضافة إلى ذلك، يمكن للمشرفين استخدام أداه التقييمات والمراجعات للمهام اليدوية التالية:</span><span class="sxs-lookup"><span data-stu-id="33383-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="33383-108">الإشراف على المراجعات بالاستجابة لها أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="33383-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="33383-109">حذف مراجعات العميل عند طلب العميل.</span><span class="sxs-lookup"><span data-stu-id="33383-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="33383-110">الاستيراد المجمع لبيانات التقييمات والمراجعات لكافة المنتجات في قالب Microsoft Power BI ، حتى يمكن تحليل اتجاهات التقييمات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="33383-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="33383-111">الوصول إلى ميزات الإشراف على التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="33383-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="33383-112">للوصول إلى ميزات الإشراف على التقييمات والمراجعات في أداة إدارة موقع التجارة الإلكترونية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="33383-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="33383-113">سجل الدخول إلى [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="33383-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="33383-114">افتح المشروع الذي يحتوي علي البيئة التي ترغب في تهيئة التجارة الإلكترونية فيها.</span><span class="sxs-lookup"><span data-stu-id="33383-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="33383-115">في قسم **البيئات** ، حدد البيئة.</span><span class="sxs-lookup"><span data-stu-id="33383-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="33383-116">ضمن **ميزات البيئة**، حدد **إدارة البيع بالتجزئة**</span><span class="sxs-lookup"><span data-stu-id="33383-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="33383-117">في علامة التبويب **التجارة الإلكترونية** ضمن **الارتباطات**، حدد **أداة إدارة موقع التجارة الإكترونية**.</span><span class="sxs-lookup"><span data-stu-id="33383-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="33383-118">قراءة مراجعة</span><span class="sxs-lookup"><span data-stu-id="33383-118">Read a review</span></span> 

1. <span data-ttu-id="33383-119">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> الإشراف**.</span><span class="sxs-lookup"><span data-stu-id="33383-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="33383-120">استخدم حقل البحث في الجانب الأيمن العلوي من الصفحة لتصفية المراجعات التي يتم عرضها حسب معرف المنتج أو اسم المنتج أو نص المراجعة.</span><span class="sxs-lookup"><span data-stu-id="33383-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="33383-121">تتيح لك عوامل التصفية الإضافية تقييد المراجعات حسب الفترة أو التقييم أو القناة أو حاله الاختصاص (الاستبعاد أو الاستجابة أو إبلاغ عنها).</span><span class="sxs-lookup"><span data-stu-id="33383-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![الصفحة الرئيسية للإشراف](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="33383-123">الاستجابة إلى مراجعة</span><span class="sxs-lookup"><span data-stu-id="33383-123">Respond to a review</span></span> 

<span data-ttu-id="33383-124">أحيانا، يعبر العملاء الذين اشتروا منتجًا عن رضاهم أو استياءهم ، أو لا يفهمون كيفية استخدام المنتج.</span><span class="sxs-lookup"><span data-stu-id="33383-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="33383-125">وكمشرف، يمكنك نشر استجابة لمراجعة ما.</span><span class="sxs-lookup"><span data-stu-id="33383-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="33383-126">تظهر هذه الاستجابة مع المراجعة على الموقع.</span><span class="sxs-lookup"><span data-stu-id="33383-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="33383-127">للاستجابة لمراجعة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="33383-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="33383-128">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> الإشراف**.</span><span class="sxs-lookup"><span data-stu-id="33383-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="33383-129">ابحث عن المراجعة التي تتطلب استجابة وحددها.</span><span class="sxs-lookup"><span data-stu-id="33383-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="33383-130">في جزء الخصائص الموجود على اليسار، حدد **إضافة استجابة**.</span><span class="sxs-lookup"><span data-stu-id="33383-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="33383-131">أدخل نص الاستجابة والاسم الذي يجب أن يظهر للمستجيب.</span><span class="sxs-lookup"><span data-stu-id="33383-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="33383-132">اسم المستجيب الافتراضي هو **المشرف**.</span><span class="sxs-lookup"><span data-stu-id="33383-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="33383-133">عند الانتهاء، حدد **نشر الاستجابة**.</span><span class="sxs-lookup"><span data-stu-id="33383-133">When you've finished, select **Post response**.</span></span>

![الاستجابة إلى أحد المراجعات](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="33383-135">استبعاد مراجعة</span><span class="sxs-lookup"><span data-stu-id="33383-135">Take down a review</span></span> 

<span data-ttu-id="33383-136">في بعض الأحيان، يكون لدى شركة ما المبرر الذي يكفل للمشرفين استبعاد مراجعات العملاء.</span><span class="sxs-lookup"><span data-stu-id="33383-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="33383-137">لاستبعاد مراجعة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="33383-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="33383-138">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> الإشراف**.</span><span class="sxs-lookup"><span data-stu-id="33383-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="33383-139">ابحث عن المراجعة التي يجب استبعادها وحددها.</span><span class="sxs-lookup"><span data-stu-id="33383-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="33383-140">في جزء الخصائص الموجود علي اليسار، حدد سبب الاستبعاد، ثم حدد **استبعاد**.</span><span class="sxs-lookup"><span data-stu-id="33383-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="33383-141">حذف مراجعات العميل عند طلب العميل</span><span class="sxs-lookup"><span data-stu-id="33383-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="33383-142">في بعض الأحيان، يرغب العملاء في حذف تقييماتهم ومراجعاتهم نهائيًا من موقع ويب خاص بالتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="33383-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="33383-143">يمكن للمشرف الذي يتلقى طلبات إزالة من أحد العملاء إزالة بيانات العميل باستخدام ميزة "حذف مراجعة".</span><span class="sxs-lookup"><span data-stu-id="33383-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="33383-144">للبحث عن بيانات عميل وحذفها، يطلب المشرف عنوان البريد الإلكتروني الذي استخدمه العميل لتسجيل الدخول وتدوين مراجعات.</span><span class="sxs-lookup"><span data-stu-id="33383-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="33383-145">للبحث عن بيانات العميل وحذفها، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="33383-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="33383-146">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> حذف**.</span><span class="sxs-lookup"><span data-stu-id="33383-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="33383-147">في حقل **بحث عن المستخدمين باستخدام عنوان البريد الإلكتروني**، أدخل عنوان البريد الإلكتروني للعميل، ثم حدد **بحث**.</span><span class="sxs-lookup"><span data-stu-id="33383-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="33383-148">إذا كان لدى العميل أي نشاط مراجعة (على سبيل المثال، إرسال مراجعات، أو التصويت على الفائدة من مراجعات عميل آخر، أو تعليقات حول مراجعة عميل آخر)، يتم عرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="33383-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="33383-149">يوجد زر **حذف** لكل عنصر.</span><span class="sxs-lookup"><span data-stu-id="33383-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="33383-150">بالنسبة لكل عنصر يجب حذفه، حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="33383-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="33383-151">عند المطالبة بالتاكيد، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="33383-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![حذف بيانات العميل](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="33383-153">قد يستغرق الإجراء سبعة أيام حتى يتم إزالة البيانات تمامًا من النظام.</span><span class="sxs-lookup"><span data-stu-id="33383-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="33383-154">يجب على المشرفين أن يعلموا العملاء بشأن هذا التأخير.</span><span class="sxs-lookup"><span data-stu-id="33383-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="33383-155">إذا قام العملاء بتغيير أسمائهم في إعدادات الحساب الخاصة بهم، فقد تظهر عناصر متعددة في نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="33383-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="33383-156">في هذه الحالة، لحذف بيانات العميل بشكل كامل، يجب على المشرف أن يحدد **حذف** لكل عنصر.</span><span class="sxs-lookup"><span data-stu-id="33383-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="33383-157">تنزيل بيانات التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="33383-157">Download ratings and reviews data</span></span>

<span data-ttu-id="33383-158">تتيح أداة الإشراف على التقييمات والمراجعات للمشرفين إمكانية استيراد بيانات التقييمات والمراجعات مجمّعة، بحيث يمكنهم تحليل الاتجاهات.</span><span class="sxs-lookup"><span data-stu-id="33383-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="33383-159">يتوفر قالب Power BI يتضمن القياسات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="33383-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="33383-160">يمكن للمشرفين استخدام هذا القالب للاتصال بالبيانات المستوردة المجمّعة وعرض لوحة معلومات.</span><span class="sxs-lookup"><span data-stu-id="33383-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="33383-161">ولا يلزمهم إنشاء لوحة معلومات مخصصة.</span><span class="sxs-lookup"><span data-stu-id="33383-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="33383-162">كما يمكن للمشرفين تخصيص قالب Power BI لتلبية احتياجاتهم المحددة.</span><span class="sxs-lookup"><span data-stu-id="33383-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="33383-163">لتحميل بيانات التقييمات والمراجعات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="33383-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="33383-164">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> ‏‫إعداد التقارير‬‬**.</span><span class="sxs-lookup"><span data-stu-id="33383-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="33383-165">حدد **تنزيل بيانات المراجعات** لتنزيل بيانات التقييمات والمراجعات بشكل مجمع بتنسيق قيم مفصولة بفواصل (CSV).</span><span class="sxs-lookup"><span data-stu-id="33383-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="33383-166">عرض اتجاهات التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="33383-166">View ratings and reviews trends</span></span>

<span data-ttu-id="33383-167">يمكن أن يقوم المشرفون بتنزيل قالب Power BI بحيث يمكنهم عرض الاتجاهات في لوحة معلومات.</span><span class="sxs-lookup"><span data-stu-id="33383-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="33383-168">لعرض اتجاهات التقييمات والمراجعات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="33383-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="33383-169">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> ‏‫إعداد التقارير‬‬**.</span><span class="sxs-lookup"><span data-stu-id="33383-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="33383-170">حدد **قالب PowerBI** لتنزيل القالب.</span><span class="sxs-lookup"><span data-stu-id="33383-170">Select **PowerBI template** to download the template.</span></span>

    ![تنزيل قالب Power BI](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="33383-172">افتح القالب الذي تم تنزيله باستخدام تطبيق Power BI.</span><span class="sxs-lookup"><span data-stu-id="33383-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="33383-173">قم بإغلاق مربع الحوار **الوصول إلى محتوى الويب** الذي يظهر، ثم أغلق رسالة الخطأ "تحديث" التي تظهر.</span><span class="sxs-lookup"><span data-stu-id="33383-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="33383-174">انتقل إلى **الصفحة الرئيسية**، وحدد **تحرير الاستعلامات**، ثم حدد **إعدادات مصدر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="33383-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="33383-175">في مربع حوار **إعدادات مصدر البيانات**، حدد **تغيير المصدر**.</span><span class="sxs-lookup"><span data-stu-id="33383-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="33383-176">في حقل **URL**، أدخل مسار بيانات المراجعات التي قمت بتنزيلها في الإجراء السابق (على سبيل المثال، **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="33383-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![حقل URL في مربع حوار القيم المفصولة بفواصل](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="33383-178">حدد **موافق**، ثم حدد **‏‫تطبيق التغييرات‬**.</span><span class="sxs-lookup"><span data-stu-id="33383-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="33383-179">سيستغرق تطبيق التغييرات علي مصدر البيانات دقيقة إلى دقيقتين.</span><span class="sxs-lookup"><span data-stu-id="33383-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="33383-180">حدد **ورقة الاتجاهات** لعرض اتجاهات التقييمات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="33383-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![اتجاهات التقييمات والمراجعات](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="33383-182">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="33383-182">Additional resources</span></span>

[<span data-ttu-id="33383-183">نظرة عامة على التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="33383-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="33383-184">الموافقة على استخدام التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="33383-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="33383-185">تكوين التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="33383-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="33383-186">مزامنة تقييمات المنتجات في Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="33383-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
