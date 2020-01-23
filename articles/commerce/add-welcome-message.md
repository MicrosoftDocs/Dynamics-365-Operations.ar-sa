---
title: إضافة رسالة ترحيب
description: يصف هذا الموضوع كيفية إضافة رسالة ترحيب إلى موقع Microsoft Dynamics 365 Commerce .
author: psimolin
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e9deeeaf491b77700ba0833e429f05d376a4392
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914506"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="ee1e9-103">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="ee1e9-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ee1e9-104">يصف هذا الموضوع كيفية إضافة رسالة ترحيب إلى موقع Microsoft Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="ee1e9-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="ee1e9-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="ee1e9-105">Overview</span></span>

<span data-ttu-id="ee1e9-106">يمكن لرسالة الترحيب على موقع التجارة الإلكترونية الخاص بك أن تبلغ الزائرين بالمبيعات الجارية أو تحديثات الموقع أو توافر المجموعات الموسمية.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="ee1e9-107">يتم تعيين رسالة الترحيب باستخدام الوحدة النمطية للتنبيه.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="ee1e9-108">يجب إضافة الوحدة النمطية للتنبيه إلى فتحة **رسائل الخطأ / المعلومات** في جزء العنوان.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="ee1e9-109">تتيح لك الوحدة النمطية للتنبيه تحديد النص المعروض ولون النص والمحاذاة.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="ee1e9-110">كما يتيح لك تحديد ما إذا كان بإمكان زوار الموقع رفض الرسالة.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="ee1e9-111">عند إضافة رسالة ترحيب إلى جزء العنوان المشترك، فسوف يتم عرضها في كل صفحة تستخدم القالب حيث يتم استخدام جزء العنوان المشترك هذا.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="ee1e9-112">لإضافة رسالة ترحيب إلى موقعك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="ee1e9-113">في Dynamics 365 Commerce، انتقل إلى موقعك.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="ee1e9-114">حدد **أجزاء**.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="ee1e9-115">حدد جزء العنوان لإضافة الرسالة إليه.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="ee1e9-116">في شجرة المخطط التفصيلي، قم بتوسيع **رسائل الخطأ / المعلومات**.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="ee1e9-117">حدد الوحدة النمطية للتنبيه.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-117">Select the alert module.</span></span>

    <span data-ttu-id="ee1e9-118">إذا لم تكن الوحدة النمطية للتنبيه موجودة بعد، فحدد زر علامة الحذف (**...**) بجوار **رسائل الخطأ / المعلومات**، ثم حدد **إضافة الوحدة النمطية**.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="ee1e9-119">حدد الوحدة النمطية للتنبيه، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="ee1e9-120">في جزء الخصائص الموجود علي اليمين، ضمن علامة التبويب **بيانات** ،حدد **إضافة مصدر بيانات**، ثم حدد **المحتوي**.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="ee1e9-121">في الحقل **إدخال النص** ، ادخل نص رسالة الترحيب.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="ee1e9-122">قم بحفظ جزء العنوان، وإيداعه ونشره.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="ee1e9-123">سوف تظهر رسالة الترحيب الآن في الجزء العلوي من كل صفحة موقع تستخدم جزء العنوان المحدد.</span><span class="sxs-lookup"><span data-stu-id="ee1e9-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee1e9-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ee1e9-124">Additional resources</span></span>

[<span data-ttu-id="ee1e9-125">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="ee1e9-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="ee1e9-126">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="ee1e9-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="ee1e9-127">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="ee1e9-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="ee1e9-128">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="ee1e9-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="ee1e9-129">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="ee1e9-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="ee1e9-130">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="ee1e9-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="ee1e9-131">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="ee1e9-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

