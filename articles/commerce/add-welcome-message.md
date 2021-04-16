---
title: إضافة رسالة ترحيب
description: يصف هذا الموضوع كيفية إضافة رسالة ترحيب إلى موقع Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797373"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="25cb2-103">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="25cb2-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="25cb2-104">يصف هذا الموضوع كيفية إضافة رسالة ترحيب إلى موقع Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="25cb2-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="25cb2-105">يمكن لرسالة الترحيب على موقع التجارة الإلكترونية الخاص بك أن تبلغ الزائرين بالمبيعات الجارية أو تحديثات الموقع أو توافر المجموعات الموسمية.</span><span class="sxs-lookup"><span data-stu-id="25cb2-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="25cb2-106">يتم تعيين رسالة الترحيب باستخدام الوحدة النمطية للتنبيه.</span><span class="sxs-lookup"><span data-stu-id="25cb2-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="25cb2-107">يجب إضافة الوحدة النمطية للتنبيه إلى فتحة **رسائل الخطأ / المعلومات** في جزء العنوان.</span><span class="sxs-lookup"><span data-stu-id="25cb2-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="25cb2-108">تتيح لك الوحدة النمطية للتنبيه تحديد النص المعروض ولون النص والمحاذاة.</span><span class="sxs-lookup"><span data-stu-id="25cb2-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="25cb2-109">كما يتيح لك تحديد ما إذا كان بإمكان زوار الموقع رفض الرسالة.</span><span class="sxs-lookup"><span data-stu-id="25cb2-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="25cb2-110">عند إضافة رسالة ترحيب إلى جزء العنوان المشترك، فسوف يتم عرضها في كل صفحة تستخدم القالب حيث يتم استخدام جزء العنوان المشترك هذا.</span><span class="sxs-lookup"><span data-stu-id="25cb2-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="25cb2-111">لإضافة رسالة ترحيب إلى موقعك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="25cb2-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="25cb2-112">في منشئ مواقع Commerce، انتقل إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="25cb2-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="25cb2-113">حدد **أجزاء**.</span><span class="sxs-lookup"><span data-stu-id="25cb2-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="25cb2-114">حدد جزء العنوان لإضافة الرسالة إليه.</span><span class="sxs-lookup"><span data-stu-id="25cb2-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="25cb2-115">في شجرة المخطط التفصيلي، قم بتوسيع **رسائل الخطأ / المعلومات**.</span><span class="sxs-lookup"><span data-stu-id="25cb2-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="25cb2-116">حدد الوحدة النمطية للتنبيه، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="25cb2-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="25cb2-117">إذا كانت وحدة التنبيه غير موجودة بعد، فحدد أولا زر علامة الحذف (**...**) بجوار **الخطأ/رسائل المعلومات**، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="25cb2-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="25cb2-118">في جزء الخصائص الموجود علي اليمين، ضمن علامة التبويب **بيانات** ،حدد **إضافة مصدر بيانات**، ثم حدد **المحتوي**.</span><span class="sxs-lookup"><span data-stu-id="25cb2-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="25cb2-119">في الحقل **إدخال النص** ، ادخل نص رسالة الترحيب.</span><span class="sxs-lookup"><span data-stu-id="25cb2-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="25cb2-120">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع جزء الرأس، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="25cb2-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="25cb2-121">سوف تظهر رسالة الترحيب الآن في الجزء العلوي من كل صفحة موقع تستخدم جزء العنوان المحدد.</span><span class="sxs-lookup"><span data-stu-id="25cb2-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25cb2-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="25cb2-122">Additional resources</span></span>

[<span data-ttu-id="25cb2-123">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="25cb2-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="25cb2-124">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="25cb2-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="25cb2-125">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="25cb2-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="25cb2-126">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="25cb2-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="25cb2-127">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="25cb2-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="25cb2-128">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="25cb2-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="25cb2-129">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="25cb2-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
