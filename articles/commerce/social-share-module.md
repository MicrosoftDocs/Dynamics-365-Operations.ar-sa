---
title: الوحدة النمطية للمشاركة الاجتماعية
description: يتناول هذا الموضوع الوحدات النمطية للمشاركة الاجتماعية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0a5ad1f4a9bb317e128ad14f21a4e6c48cab8a72
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985526"
---
# <a name="social-share-module"></a><span data-ttu-id="34f13-103">الوحدة النمطية للمشاركة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="34f13-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="34f13-104">يتناول هذا الموضوع الوحدات النمطية للمشاركة الاجتماعية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="34f13-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="34f13-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="34f13-105">Overview</span></span>

<span data-ttu-id="34f13-106">تسمح الوحدات النمطية للمشاركة الاجتماعية للمستخدمين بمشاركة عناوين URL لصفحات موقع التجارة الإلكترونية على وسائل التواصل الاجتماعي مثل Facebook وTwitter وPinterest وLinkedIn.</span><span class="sxs-lookup"><span data-stu-id="34f13-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="34f13-107">يمكن أيضًا مشاركة عناوين URL لصفحات الموقع عبر البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="34f13-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="34f13-108">وتستخدم عادة الوحدات النمطية للمشاركة الاجتماعية في صفحات تفاصيل المنتج (PDP) لمساعدة المستخدمين على مشاركة معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="34f13-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="34f13-109">كل وحدة نمطية للمشاركة الاجتماعية هي حاوية للوحدات النمطية لعناصر المشاركة الاجتماعية.</span><span class="sxs-lookup"><span data-stu-id="34f13-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="34f13-110">يمكن تكوين كل وحدة نمطية لعنصر المشاركة الاجتماعية للإشارة إلى موقع وسائط اجتماعية محدد.</span><span class="sxs-lookup"><span data-stu-id="34f13-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="34f13-111">التكامل مع Facebook وTwitter وPinterest وLinkedIn والبريد الإلكتروني مدعوم على الفور..</span><span class="sxs-lookup"><span data-stu-id="34f13-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="34f13-112">عندما يقوم مستخدم الموقع بتحديد رمز وسائل تواصل اجتماعي، يتم تشغيل HTML iframe لموقع وسائل التواصل الاجتماعي المناظرة.</span><span class="sxs-lookup"><span data-stu-id="34f13-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="34f13-113">داخل iframe، يمكن للمستخدم تسجيل الدخول وترحيل محتوى الصفحة التي كانوا يستعرضونها.</span><span class="sxs-lookup"><span data-stu-id="34f13-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="34f13-114">قد يتعقب كل نظام وسائل تواصل اجتماعي ملفات تعريف الارتباط، لذا تتطلب هذه الوحدة النمطية من المستخدمين قبول رسالة إعلام الموافقة على ملفات تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="34f13-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="34f13-115">عند عدم قبول الموافقة على ملفات تعريف الارتباط، سيتم إخفاء الوحدة النمطية في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="34f13-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="34f13-116">لمزيد من المعلومات، راجع [التوافق مع ملف تعريف الارتباط](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="34f13-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="34f13-117">يلقى الرسم التوضيحي التالي الضوء على مثال لوحدة نمطية للمشاركة الاجتماعية المستخدمة في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="34f13-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![مثال عن وحدة نمطية للمشاركة الاجتماعية](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="34f13-119">خصائص الوحدة النمطية للمشاركة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="34f13-119">Social share module properties</span></span>

| <span data-ttu-id="34f13-120">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="34f13-120">Property name</span></span>             | <span data-ttu-id="34f13-121">قيمة</span><span class="sxs-lookup"><span data-stu-id="34f13-121">Value</span></span>                 | <span data-ttu-id="34f13-122">الوصف</span><span class="sxs-lookup"><span data-stu-id="34f13-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="34f13-123">التسمية التوضيحية</span><span class="sxs-lookup"><span data-stu-id="34f13-123">Caption</span></span>                  | <span data-ttu-id="34f13-124">النص</span><span class="sxs-lookup"><span data-stu-id="34f13-124">Text</span></span> | <span data-ttu-id="34f13-125">تحدد هذه الخاصية التسمية التوضيحية للوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="34f13-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="34f13-126">الاتجاه</span><span class="sxs-lookup"><span data-stu-id="34f13-126">Orientation</span></span> | <span data-ttu-id="34f13-127">**أفقي** أو **عمودي**</span><span class="sxs-lookup"><span data-stu-id="34f13-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="34f13-128">تحدد هذه الخاصية اتجاه التخطيط لعناصر وسائل التواصل الاجتماعي.</span><span class="sxs-lookup"><span data-stu-id="34f13-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="34f13-129">خصائص الوحدة النمطية لعنصر المشاركة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="34f13-129">Social share item module properties</span></span>
| <span data-ttu-id="34f13-130">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="34f13-130">Property name</span></span>             | <span data-ttu-id="34f13-131">قيمة</span><span class="sxs-lookup"><span data-stu-id="34f13-131">Value</span></span>                 | <span data-ttu-id="34f13-132">الوصف</span><span class="sxs-lookup"><span data-stu-id="34f13-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="34f13-133">وسائل التواصل الاجتماعي</span><span class="sxs-lookup"><span data-stu-id="34f13-133">Social media</span></span>              | <span data-ttu-id="34f13-134">**Facebook**، **Twitter**، **Pinterest**، **LinkedIn**، **البريد**</span><span class="sxs-lookup"><span data-stu-id="34f13-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="34f13-135">قائمة منسدلة تتضمن قائمة بالأنظمة الأساسية لوسائل التواصل الاجتماعي.</span><span class="sxs-lookup"><span data-stu-id="34f13-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="34f13-136">أيقونة</span><span class="sxs-lookup"><span data-stu-id="34f13-136">Icon</span></span> |<span data-ttu-id="34f13-137">صورة</span><span class="sxs-lookup"><span data-stu-id="34f13-137">Image</span></span>    | <span data-ttu-id="34f13-138">ستكون هذه الصورة التي سيتم عرضها لوسائل التواصل الاجتماعي المناظرة.</span><span class="sxs-lookup"><span data-stu-id="34f13-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="34f13-139">من المستحسن الرجوع إلى SDK النظام الأساسي لوسائل التواصل الاجتماعي للاطلاع على الصفحة التي ننصح باستخدامها لكل نظام أساسي.</span><span class="sxs-lookup"><span data-stu-id="34f13-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="34f13-140">إضافة وحدة نمطية للمشاركة الاجتماعية إلى الوحدة النمطية لمربع الشراء</span><span class="sxs-lookup"><span data-stu-id="34f13-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="34f13-141">لإضافة وحدة نمطية للمشاركة الاجتماعية إلى الوحدة النمطية لمربع الشراء، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="34f13-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="34f13-142">في موقع Fabrikam، حدد **الصفحات**، ثم حدد الصفحة **DefaultPDP** لفتح صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="34f13-142">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="34f13-143">في فتحة **مربع الشراء (مطلوب)‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="34f13-143">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="34f13-144">في مربع الحوار **إضافة وحدة**، حدد وحدة **المشاركة الاجتماعية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="34f13-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="34f13-145">في فتحة **المشاركة الاجتماعية‬‬‏‫** حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="34f13-145">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="34f13-146">في مربع الحوار **إضافة وحدة**، حدد وحدة **SocialShare‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="34f13-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="34f13-147">في الجزء خصائص من وحدة **SocialShare**، ضمن **الاتجاه**، حدد **أفقي**.</span><span class="sxs-lookup"><span data-stu-id="34f13-147">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="34f13-148">أضف تسمية توضيحية حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="34f13-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="34f13-149">في فتحة **SocialShare‬‬‏‫** حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="34f13-149">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="34f13-150">في مربع الحوار **إضافة وحدة**، حدد وحدة **SocialShareItem‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="34f13-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="34f13-151">في الجزء خصائص من وحدة **SocialShareItem**، ضمن **وسائل التواصل الاجتماعي**، حدد **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="34f13-151">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="34f13-152">في الجزء خصائص من وحدة **SocialShareItem**، ضمن **الأيقونة**، حدد **+ إضافة صورة**.</span><span class="sxs-lookup"><span data-stu-id="34f13-152">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="34f13-153">في مربع الحوار **منتقي الوسائط**، حدد صورة شعار Facebook، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="34f13-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="34f13-154">في حال عدم وجود صورة شعار Facebook، حدد **تحميل عنصر وسائط جديد** لتحميل عنصر.</span><span class="sxs-lookup"><span data-stu-id="34f13-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="34f13-155">أضف وكوّن وحدات **SocialShareItem** إضافية حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="34f13-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="34f13-156">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="34f13-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="34f13-157">ستعرض الصفحة الوحدة النمطية للمشاركة الاجتماعية.</span><span class="sxs-lookup"><span data-stu-id="34f13-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="34f13-158">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="34f13-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34f13-159">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="34f13-159">Additional resources</span></span>

[<span data-ttu-id="34f13-160">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="34f13-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="34f13-161">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="34f13-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="34f13-162">توافق ملفات تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="34f13-162">Cookie compliance</span></span>](cookie-compliance.md)
