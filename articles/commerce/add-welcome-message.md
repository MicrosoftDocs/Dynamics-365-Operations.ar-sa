---
title: إضافة رسالة ترحيب
description: يصف هذا الموضوع كيفية إضافة رسالة ترحيب إلى موقع Microsoft Dynamics 365 Commerce .
author: psimolin
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5910ab85b1b0b2df992a24ad3cf7a032e7b98ea9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980122"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="45240-103">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="45240-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="45240-104">يصف هذا الموضوع كيفية إضافة رسالة ترحيب إلى موقع Microsoft Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="45240-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="45240-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="45240-105">Overview</span></span>

<span data-ttu-id="45240-106">يمكن لرسالة الترحيب على موقع التجارة الإلكترونية الخاص بك أن تبلغ الزائرين بالمبيعات الجارية أو تحديثات الموقع أو توافر المجموعات الموسمية.</span><span class="sxs-lookup"><span data-stu-id="45240-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="45240-107">يتم تعيين رسالة الترحيب باستخدام الوحدة النمطية للتنبيه.</span><span class="sxs-lookup"><span data-stu-id="45240-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="45240-108">يجب إضافة الوحدة النمطية للتنبيه إلى فتحة **رسائل الخطأ / المعلومات** في جزء العنوان.</span><span class="sxs-lookup"><span data-stu-id="45240-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="45240-109">تتيح لك الوحدة النمطية للتنبيه تحديد النص المعروض ولون النص والمحاذاة.</span><span class="sxs-lookup"><span data-stu-id="45240-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="45240-110">كما يتيح لك تحديد ما إذا كان بإمكان زوار الموقع رفض الرسالة.</span><span class="sxs-lookup"><span data-stu-id="45240-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="45240-111">عند إضافة رسالة ترحيب إلى جزء العنوان المشترك، فسوف يتم عرضها في كل صفحة تستخدم القالب حيث يتم استخدام جزء العنوان المشترك هذا.</span><span class="sxs-lookup"><span data-stu-id="45240-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="45240-112">لإضافة رسالة ترحيب إلى موقعك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="45240-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="45240-113">في منشئ مواقع Commerce، انتقل إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="45240-113">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="45240-114">حدد **أجزاء**.</span><span class="sxs-lookup"><span data-stu-id="45240-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="45240-115">حدد جزء العنوان لإضافة الرسالة إليه.</span><span class="sxs-lookup"><span data-stu-id="45240-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="45240-116">في شجرة المخطط التفصيلي، قم بتوسيع **رسائل الخطأ / المعلومات**.</span><span class="sxs-lookup"><span data-stu-id="45240-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="45240-117">حدد الوحدة النمطية للتنبيه، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="45240-117">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="45240-118">إذا كانت وحدة التنبيه غير موجودة بعد، فحدد أولا زر علامة الحذف (**...**) بجوار **الخطأ/رسائل المعلومات**، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="45240-118">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="45240-119">في جزء الخصائص الموجود علي اليمين، ضمن علامة التبويب **بيانات** ،حدد **إضافة مصدر بيانات**، ثم حدد **المحتوي**.</span><span class="sxs-lookup"><span data-stu-id="45240-119">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="45240-120">في الحقل **إدخال النص** ، ادخل نص رسالة الترحيب.</span><span class="sxs-lookup"><span data-stu-id="45240-120">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="45240-121">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع جزء الرأس، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="45240-121">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="45240-122">سوف تظهر رسالة الترحيب الآن في الجزء العلوي من كل صفحة موقع تستخدم جزء العنوان المحدد.</span><span class="sxs-lookup"><span data-stu-id="45240-122">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45240-123">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="45240-123">Additional resources</span></span>

[<span data-ttu-id="45240-124">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="45240-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="45240-125">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="45240-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="45240-126">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="45240-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="45240-127">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="45240-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="45240-128">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="45240-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="45240-129">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="45240-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="45240-130">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="45240-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

