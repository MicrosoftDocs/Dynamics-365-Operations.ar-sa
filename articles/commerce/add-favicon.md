---
title: إضافة أيقونة المفضلة
description: ‏‫يوضح هذا الموضوع كيفية إضافة أيقونة مفضلة إلى الموقع الخاص بك.‬
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 18e12cbe46650fcf024a56b6de9a8cb2903d2bf8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914553"
---
# <a name="add-a-favicon"></a><span data-ttu-id="fc39d-103">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="fc39d-103">Add a favicon</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fc39d-104">‏‫يوضح هذا الموضوع كيفية إضافة أيقونة مفضلة إلى الموقع الخاص بك.‬</span><span class="sxs-lookup"><span data-stu-id="fc39d-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="fc39d-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="fc39d-105">Overview</span></span>

<span data-ttu-id="fc39d-106">وأيقونة المفضلة هي ملف رسومي صغير يتم عرضة على علامة تبويب مستعرض ويب، في شريط العنوان، وفي محفوظات الاستعراض، وفي الإشارات المرجعية أو المفضلة، من بين أماكن أخرى.</span><span class="sxs-lookup"><span data-stu-id="fc39d-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="fc39d-107">نوصي أن تقوم بإضافة أيقونة المفضلة إلى موقعك، لأنها تعرض وتعزز علامتك التجارية، وتساعد في تمييز موقعك عن المواقع الأخرى التي يزورها عملائك.</span><span class="sxs-lookup"><span data-stu-id="fc39d-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="fc39d-108">على الرغم من أنه يُمكنك إضافة عدة أيقونات للمفضلة بأحجام مختلفة وأنواع ملفات إلى موقعك، ويوضح هذا الموضوع كيفية إضافة أيقونة مفضلة واحدة.</span><span class="sxs-lookup"><span data-stu-id="fc39d-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="fc39d-109">ولكن، يتم استخدام نفس العملية والموقع لإضافة أكثر من أيقونة المفضلة.</span><span class="sxs-lookup"><span data-stu-id="fc39d-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="fc39d-110">تحميل أيقونة المفضلة إلى مجموعة أصول الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="fc39d-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="fc39d-111">لتحميل أيقونة المفضلة إلى مجموعة أصول الموقع الخاص بك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="fc39d-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="fc39d-112">انتقل إلى **الأصول \> تحميل \> تحميل الأصول**.</span><span class="sxs-lookup"><span data-stu-id="fc39d-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="fc39d-113">ابحث عن أيقونة المفضلة في نظام ملفاتك المحلي وحددها.</span><span class="sxs-lookup"><span data-stu-id="fc39d-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="fc39d-114">ادخل تجانب، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc39d-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="fc39d-115">في جزء الخصائص الموجود على اليمين، انسخ عنوان URL العمومي لأيقونة المفضلة.</span><span class="sxs-lookup"><span data-stu-id="fc39d-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="fc39d-116">إذا لم تقم بتحديد خيار **نشر الأصول بعد التحميل** ، يجب عليك العودة إلى صفحة **الأصول** ، ونشر أيقونة المفضلة يدويًا في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="fc39d-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="fc39d-117">قم بإنشاء HTML لأيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="fc39d-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="fc39d-118">لإنشاء HTML لأيقونة المفضلة، استخدم جزء HTML التالي.</span><span class="sxs-lookup"><span data-stu-id="fc39d-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="fc39d-119">بالنسبة للسمة **href** ،استبدل **"عنوان URL\_العمومي\_لـ\_أيقونة المفضلة\_الخاصة بك"** بعنوان URL الذي قمت بنسخه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="fc39d-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="fc39d-120">إضافة HTML لأيقونة المفضلة إلى عنصر \<العنوان\> في الصفحات الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="fc39d-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="fc39d-121">لإضافة أيقونة المفضلة إلى موقعك، استخدم نفس الإجراء المستخدم لإضافة أي نوع من HTML أو البرنامج النصي إلى عنصر **\<العنوان\>** لصفحات موقعك.</span><span class="sxs-lookup"><span data-stu-id="fc39d-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc39d-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fc39d-122">Additional resources</span></span>

[<span data-ttu-id="fc39d-123">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="fc39d-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="fc39d-124">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="fc39d-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="fc39d-125">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="fc39d-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="fc39d-126">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="fc39d-126">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="fc39d-127">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="fc39d-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="fc39d-128">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="fc39d-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="fc39d-129">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="fc39d-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
