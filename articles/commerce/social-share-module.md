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
ms.openlocfilehash: 0e7f30686894f9cf92257e99d95cc8b00f76f899
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234307"
---
# <a name="social-share-module"></a><span data-ttu-id="f10ba-103">الوحدة النمطية للمشاركة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="f10ba-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f10ba-104">يتناول هذا الموضوع الوحدات النمطية للمشاركة الاجتماعية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f10ba-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f10ba-105">تسمح الوحدات النمطية للمشاركة الاجتماعية للمستخدمين بمشاركة عناوين URL لصفحات موقع التجارة الإلكترونية على وسائل التواصل الاجتماعي مثل Facebook وTwitter وPinterest وLinkedIn.</span><span class="sxs-lookup"><span data-stu-id="f10ba-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="f10ba-106">يمكن أيضًا مشاركة عناوين URL لصفحات الموقع عبر البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="f10ba-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="f10ba-107">وتستخدم عادة الوحدات النمطية للمشاركة الاجتماعية في صفحات تفاصيل المنتج (PDP) لمساعدة المستخدمين على مشاركة معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="f10ba-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="f10ba-108">كل وحدة نمطية للمشاركة الاجتماعية هي حاوية للوحدات النمطية لعناصر المشاركة الاجتماعية.</span><span class="sxs-lookup"><span data-stu-id="f10ba-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="f10ba-109">يمكن تكوين كل وحدة نمطية لعنصر المشاركة الاجتماعية للإشارة إلى موقع وسائط اجتماعية محدد.</span><span class="sxs-lookup"><span data-stu-id="f10ba-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="f10ba-110">التكامل مع Facebook وTwitter وPinterest وLinkedIn والبريد الإلكتروني مدعوم على الفور..</span><span class="sxs-lookup"><span data-stu-id="f10ba-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="f10ba-111">عندما يقوم مستخدم الموقع بتحديد رمز وسائل تواصل اجتماعي، يتم تشغيل HTML iframe لموقع وسائل التواصل الاجتماعي المناظرة.</span><span class="sxs-lookup"><span data-stu-id="f10ba-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="f10ba-112">داخل iframe، يمكن للمستخدم تسجيل الدخول وترحيل محتوى الصفحة التي كانوا يستعرضونها.</span><span class="sxs-lookup"><span data-stu-id="f10ba-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="f10ba-113">قد يتعقب كل نظام وسائل تواصل اجتماعي ملفات تعريف الارتباط، لذا تتطلب هذه الوحدة النمطية من المستخدمين قبول رسالة إعلام الموافقة على ملفات تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="f10ba-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="f10ba-114">عند عدم قبول الموافقة على ملفات تعريف الارتباط، سيتم إخفاء الوحدة النمطية في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f10ba-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="f10ba-115">لمزيد من المعلومات، راجع [التوافق مع ملف تعريف الارتباط](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="f10ba-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="f10ba-116">يلقى الرسم التوضيحي التالي الضوء على مثال لوحدة نمطية للمشاركة الاجتماعية المستخدمة في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="f10ba-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![مثال عن وحدة نمطية للمشاركة الاجتماعية](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="f10ba-118">خصائص الوحدة النمطية للمشاركة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="f10ba-118">Social share module properties</span></span>

| <span data-ttu-id="f10ba-119">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="f10ba-119">Property name</span></span>             | <span data-ttu-id="f10ba-120">قيمة</span><span class="sxs-lookup"><span data-stu-id="f10ba-120">Value</span></span>                 | <span data-ttu-id="f10ba-121">الوصف</span><span class="sxs-lookup"><span data-stu-id="f10ba-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f10ba-122">التسمية التوضيحية</span><span class="sxs-lookup"><span data-stu-id="f10ba-122">Caption</span></span>                  | <span data-ttu-id="f10ba-123">النص</span><span class="sxs-lookup"><span data-stu-id="f10ba-123">Text</span></span> | <span data-ttu-id="f10ba-124">تحدد هذه الخاصية التسمية التوضيحية للوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="f10ba-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="f10ba-125">الاتجاه</span><span class="sxs-lookup"><span data-stu-id="f10ba-125">Orientation</span></span> | <span data-ttu-id="f10ba-126">**أفقي** أو **عمودي**</span><span class="sxs-lookup"><span data-stu-id="f10ba-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="f10ba-127">تحدد هذه الخاصية اتجاه التخطيط لعناصر وسائل التواصل الاجتماعي.</span><span class="sxs-lookup"><span data-stu-id="f10ba-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="f10ba-128">خصائص الوحدة النمطية لعنصر المشاركة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="f10ba-128">Social share item module properties</span></span>
| <span data-ttu-id="f10ba-129">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="f10ba-129">Property name</span></span>             | <span data-ttu-id="f10ba-130">قيمة</span><span class="sxs-lookup"><span data-stu-id="f10ba-130">Value</span></span>                 | <span data-ttu-id="f10ba-131">الوصف</span><span class="sxs-lookup"><span data-stu-id="f10ba-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f10ba-132">وسائل التواصل الاجتماعي</span><span class="sxs-lookup"><span data-stu-id="f10ba-132">Social media</span></span>              | <span data-ttu-id="f10ba-133">**Facebook**، **Twitter**، **Pinterest**، **LinkedIn**، **البريد**</span><span class="sxs-lookup"><span data-stu-id="f10ba-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="f10ba-134">قائمة منسدلة تتضمن قائمة بالأنظمة الأساسية لوسائل التواصل الاجتماعي.</span><span class="sxs-lookup"><span data-stu-id="f10ba-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="f10ba-135">أيقونة</span><span class="sxs-lookup"><span data-stu-id="f10ba-135">Icon</span></span> |<span data-ttu-id="f10ba-136">صورة</span><span class="sxs-lookup"><span data-stu-id="f10ba-136">Image</span></span>    | <span data-ttu-id="f10ba-137">ستكون هذه الصورة التي سيتم عرضها لوسائل التواصل الاجتماعي المناظرة.</span><span class="sxs-lookup"><span data-stu-id="f10ba-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="f10ba-138">من المستحسن الرجوع إلى SDK النظام الأساسي لوسائل التواصل الاجتماعي للاطلاع على الصفحة التي ننصح باستخدامها لكل نظام أساسي.</span><span class="sxs-lookup"><span data-stu-id="f10ba-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="f10ba-139">إضافة وحدة نمطية للمشاركة الاجتماعية إلى الوحدة النمطية لمربع الشراء</span><span class="sxs-lookup"><span data-stu-id="f10ba-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="f10ba-140">لإضافة وحدة نمطية للمشاركة الاجتماعية إلى الوحدة النمطية لمربع الشراء، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f10ba-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="f10ba-141">في موقع Fabrikam، حدد **الصفحات**، ثم حدد الصفحة **DefaultPDP** لفتح صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="f10ba-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="f10ba-142">في فتحة **مربع الشراء (مطلوب)‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="f10ba-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f10ba-143">في مربع الحوار **إضافة وحدة**، حدد وحدة **المشاركة الاجتماعية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f10ba-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f10ba-144">في فتحة **المشاركة الاجتماعية‬‬‏‫** حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="f10ba-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f10ba-145">في مربع الحوار **إضافة وحدة**، حدد وحدة **SocialShare‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f10ba-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f10ba-146">في الجزء خصائص من وحدة **SocialShare**، ضمن **الاتجاه**، حدد **أفقي**.</span><span class="sxs-lookup"><span data-stu-id="f10ba-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="f10ba-147">أضف تسمية توضيحية حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="f10ba-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="f10ba-148">في فتحة **SocialShare‬‬‏‫** حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="f10ba-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f10ba-149">في مربع الحوار **إضافة وحدة**، حدد وحدة **SocialShareItem‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f10ba-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f10ba-150">في الجزء خصائص من وحدة **SocialShareItem**، ضمن **وسائل التواصل الاجتماعي**، حدد **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="f10ba-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="f10ba-151">في الجزء خصائص من وحدة **SocialShareItem**، ضمن **الأيقونة**، حدد **+ إضافة صورة**.</span><span class="sxs-lookup"><span data-stu-id="f10ba-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="f10ba-152">في مربع الحوار **منتقي الوسائط**، حدد صورة شعار Facebook، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f10ba-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="f10ba-153">في حال عدم وجود صورة شعار Facebook، حدد **تحميل عنصر وسائط جديد** لتحميل عنصر.</span><span class="sxs-lookup"><span data-stu-id="f10ba-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="f10ba-154">أضف وكوّن وحدات **SocialShareItem** إضافية حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="f10ba-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="f10ba-155">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f10ba-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f10ba-156">ستعرض الصفحة الوحدة النمطية للمشاركة الاجتماعية.</span><span class="sxs-lookup"><span data-stu-id="f10ba-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="f10ba-157">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="f10ba-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f10ba-158">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f10ba-158">Additional resources</span></span>

[<span data-ttu-id="f10ba-159">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="f10ba-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f10ba-160">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="f10ba-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f10ba-161">توافق ملفات تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="f10ba-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]