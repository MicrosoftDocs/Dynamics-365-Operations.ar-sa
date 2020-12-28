---
title: إدارة التقييمات والمراجعات
description: يشرح هذا الموضوع كيفية إدارة التقييمات والمراجعات في أداة إنشاء مواقع Microsoft Dynamics 365 Commerce .
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 3fc88bc5a5868dce7c0539bf3f0ddc5b751e7b75
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409914"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="2ceea-103">إدارة التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="2ceea-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2ceea-104">يشرح هذا الموضوع كيفية إدارة التقييمات والمراجعات في أداة إنشاء مواقع Microsoft Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="2ceea-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="2ceea-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="2ceea-105">Overview</span></span>

<span data-ttu-id="2ceea-106">Dynamics 365 Commerce يستخدم Microsoft Azure Cognitive Service للإشراف تلقائيًا على مرجعة النصوص عن طريق تنقيح الكلمات البذيئة.</span><span class="sxs-lookup"><span data-stu-id="2ceea-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="2ceea-107">بالاضافه إلى ذلك، يمكن للمشرفين استخدام أدة إنشاء مواقع Dynamics 365 Commerce لتنفيذ المهام اليدوية التالية:</span><span class="sxs-lookup"><span data-stu-id="2ceea-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="2ceea-108">الإشراف على المراجعات بالاستجابة لها أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="2ceea-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="2ceea-109">حذف مراجعات العميل عند طلب العميل.</span><span class="sxs-lookup"><span data-stu-id="2ceea-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="2ceea-110">الاستيراد المجمع لبيانات التقييمات والمراجعات لكافة المنتجات في قالب Microsoft Power BI ، حتى يمكن تحليل اتجاهات التقييمات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="2ceea-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="2ceea-111">قراءة مراجعة</span><span class="sxs-lookup"><span data-stu-id="2ceea-111">Read a review</span></span> 

<span data-ttu-id="2ceea-112">لقراءة مراجعة في أداة إنشاء موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2ceea-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2ceea-113">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> الإشراف**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="2ceea-114">استخدم حقل البحث في الجانب الأيمن العلوي من الصفحة لتصفية المراجعات التي يتم عرضها حسب معرف المنتج أو اسم المنتج أو نص المراجعة.</span><span class="sxs-lookup"><span data-stu-id="2ceea-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="2ceea-115">تتيح لك عوامل التصفية الإضافية تقييد المراجعات حسب الفترة أو التقييم أو القناة أو حاله الاختصاص (الاستبعاد أو الاستجابة أو إبلاغ عنها).</span><span class="sxs-lookup"><span data-stu-id="2ceea-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![الصفحة الرئيسية للإشراف](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="2ceea-117">الاستجابة إلى مراجعة</span><span class="sxs-lookup"><span data-stu-id="2ceea-117">Respond to a review</span></span> 

<span data-ttu-id="2ceea-118">أحيانا، يعبر العملاء الذين اشتروا منتجًا عن رضاهم أو استياءهم ، أو لا يفهمون كيفية استخدام المنتج.</span><span class="sxs-lookup"><span data-stu-id="2ceea-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="2ceea-119">وكمشرف، يمكنك نشر استجابة لمراجعة ما.</span><span class="sxs-lookup"><span data-stu-id="2ceea-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="2ceea-120">تظهر هذه الاستجابة مع المراجعة على الموقع.</span><span class="sxs-lookup"><span data-stu-id="2ceea-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="2ceea-121">للرد على مراجعة في أداة إنشاء موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2ceea-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2ceea-122">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> الإشراف**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="2ceea-123">ابحث عن المراجعة التي تتطلب استجابة وحددها.</span><span class="sxs-lookup"><span data-stu-id="2ceea-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="2ceea-124">في جزء الخصائص الموجود على اليسار، حدد **إضافة استجابة**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="2ceea-125">أدخل نص الاستجابة والاسم الذي يجب أن يظهر للمستجيب.</span><span class="sxs-lookup"><span data-stu-id="2ceea-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="2ceea-126">اسم المستجيب الافتراضي هو **المشرف**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="2ceea-127">عند الانتهاء، حدد **نشر الاستجابة**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-127">When you've finished, select **Post response**.</span></span>

![الاستجابة إلى أحد المراجعات](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="2ceea-129">استبعاد مراجعة</span><span class="sxs-lookup"><span data-stu-id="2ceea-129">Take down a review</span></span> 

<span data-ttu-id="2ceea-130">في بعض الأحيان، يكون لدى شركة ما المبرر الذي يكفل للمشرفين استبعاد مراجعات العملاء.</span><span class="sxs-lookup"><span data-stu-id="2ceea-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="2ceea-131">لاستبعاد مراجعة في أداة إنشاء موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2ceea-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2ceea-132">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> الإشراف**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="2ceea-133">ابحث عن المراجعة التي يجب استبعادها وحددها.</span><span class="sxs-lookup"><span data-stu-id="2ceea-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="2ceea-134">في جزء الخصائص الموجود علي اليسار، حدد سبب الاستبعاد، ثم حدد **استبعاد مراجعة**، ثم حدد **استبعاد**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="2ceea-135">حذف مراجعات العميل عند طلب العميل</span><span class="sxs-lookup"><span data-stu-id="2ceea-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="2ceea-136">في بعض الأحيان، يرغب العملاء في حذف تقييماتهم ومراجعاتهم نهائيًا من موقع ويب خاص بالتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2ceea-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="2ceea-137">يمكن للمشرف الذي يتلقى طلبات إزالة من أحد العملاء إزالة بيانات العميل باستخدام ميزة "حذف مراجعة".</span><span class="sxs-lookup"><span data-stu-id="2ceea-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="2ceea-138">للبحث عن بيانات عميل وحذفها، يطلب المشرف عنوان البريد الإلكتروني الذي استخدمه العميل لتسجيل الدخول وتدوين مراجعات.</span><span class="sxs-lookup"><span data-stu-id="2ceea-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="2ceea-139">للبحث عن بيانات العميل في أداة إنشاء موقع Commerce وحذفها، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2ceea-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2ceea-140">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> حذف**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="2ceea-141">في مربع **بحث عن المستخدمين باستخدام عنوان البريد الإلكتروني**، أدخل عنوان البريد الإلكتروني للعميل، ثم حدد **بحث**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="2ceea-142">إذا كان لدى العميل أي نشاط مراجعة (على سبيل المثال، إرسال مراجعات، أو التصويت على الفائدة من مراجعات عميل آخر، أو تعليقات حول مراجعة عميل آخر)، يتم عرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="2ceea-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="2ceea-143">يوجد زر **حذف** لكل عنصر.</span><span class="sxs-lookup"><span data-stu-id="2ceea-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="2ceea-144">بالنسبة لكل عنصر يجب حذفه، حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="2ceea-145">عند المطالبة بالتاكيد، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![حذف بيانات العميل](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="2ceea-147">قد يستغرق الإجراء سبعة أيام حتى يتم إزالة البيانات تمامًا من النظام.</span><span class="sxs-lookup"><span data-stu-id="2ceea-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="2ceea-148">يجب على المشرفين أن يعلموا العملاء بشأن هذا التأخير.</span><span class="sxs-lookup"><span data-stu-id="2ceea-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="2ceea-149">إذا قام العملاء بتغيير أسمائهم في إعدادات الحساب الخاصة بهم، فقد تظهر عناصر متعددة في نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="2ceea-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="2ceea-150">في هذه الحالة، لحذف بيانات العميل بشكل كامل، يجب على المشرف أن يحدد **حذف** لكل عنصر.</span><span class="sxs-lookup"><span data-stu-id="2ceea-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="2ceea-151">تنزيل بيانات التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="2ceea-151">Download ratings and reviews data</span></span>

<span data-ttu-id="2ceea-152">تتيح أداة إنشاء موقع Commerce على التقييمات والمراجعات للمشرفين إمكانية استيراد بيانات التقييمات والمراجعات مجمّعة، بحيث يمكنهم تحليل الاتجاهات.</span><span class="sxs-lookup"><span data-stu-id="2ceea-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="2ceea-153">يتوفر قالب Power BI يتضمن القياسات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="2ceea-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="2ceea-154">يمكن للمشرفين استخدام هذا القالب للاتصال بالبيانات المستوردة المجمّعة وعرض لوحة معلومات.</span><span class="sxs-lookup"><span data-stu-id="2ceea-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="2ceea-155">ولا يلزمهم إنشاء لوحة معلومات مخصصة.</span><span class="sxs-lookup"><span data-stu-id="2ceea-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="2ceea-156">كما يمكن للمشرفين تخصيص قالب Power BI لتلبية احتياجاتهم المحددة.</span><span class="sxs-lookup"><span data-stu-id="2ceea-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="2ceea-157">لتنزيل التقييمات والمراجعات في أداة إنشاء موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2ceea-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2ceea-158">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> ‏‫إعداد التقارير‬‬**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="2ceea-159">حدد **تنزيل بيانات المراجعة** لتنزيل بيانات التقييمات والمراجعات بشكل مجمع بتنسيق قيم مفصولة بفواصل (CSV).</span><span class="sxs-lookup"><span data-stu-id="2ceea-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="2ceea-160">عرض اتجاهات التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="2ceea-160">View ratings and reviews trends</span></span>

<span data-ttu-id="2ceea-161">يمكن أن يقوم المشرفون بتنزيل قالب Power BI بحيث يمكنهم عرض الاتجاهات في لوحة معلومات.</span><span class="sxs-lookup"><span data-stu-id="2ceea-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="2ceea-162">لعرض اتجاهات التقييمات والمراجعات في أداة إنشاء موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2ceea-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2ceea-163">انتقل إلى **الصفحة الرئيسية‬ \> المراجعات \> ‏‫إعداد التقارير‬‬**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="2ceea-164">حدد **قالب PowerBI** لتنزيل القالب.</span><span class="sxs-lookup"><span data-stu-id="2ceea-164">Select **PowerBI template** to download the template.</span></span>

    ![تنزيل قالب Power BI](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="2ceea-166">افتح القالب الذي تم تنزيله باستخدام تطبيق Power BI.</span><span class="sxs-lookup"><span data-stu-id="2ceea-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="2ceea-167">قم بإغلاق مربع الحوار **الوصول إلى محتوى الويب** الذي يظهر، ثم أغلق رسالة الخطأ "تحديث" التي تظهر.</span><span class="sxs-lookup"><span data-stu-id="2ceea-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="2ceea-168">انتقل إلى **الصفحة الرئيسية**، وحدد **تحرير الاستعلامات**، ثم حدد **إعدادات مصدر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="2ceea-169">في مربع حوار **إعدادات مصدر البيانات**، حدد **تغيير المصدر**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="2ceea-170">في حقل **URL**، أدخل مسار بيانات المراجعات التي قمت بتنزيلها في الإجراء السابق (على سبيل المثال، **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="2ceea-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![حقل URL في مربع حوار القيم المفصولة بفواصل](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="2ceea-172">حدد **موافق**، ثم حدد **‏‫تطبيق التغييرات‬**.</span><span class="sxs-lookup"><span data-stu-id="2ceea-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="2ceea-173">سيستغرق تطبيق التغييرات علي مصدر البيانات دقيقة إلى دقيقتين.</span><span class="sxs-lookup"><span data-stu-id="2ceea-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="2ceea-174">حدد **ورقة الاتجاهات** لعرض اتجاهات التقييمات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="2ceea-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![اتجاهات التقييمات والمراجعات](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="2ceea-176">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2ceea-176">Additional resources</span></span>

[<span data-ttu-id="2ceea-177">نظرة عامة على التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="2ceea-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="2ceea-178">الموافقة على استخدام التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="2ceea-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="2ceea-179">تكوين التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="2ceea-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="2ceea-180">مزامنة تقييمات المنتجات في Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="2ceea-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
