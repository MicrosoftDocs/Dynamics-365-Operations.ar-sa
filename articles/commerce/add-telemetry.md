---
title: إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام
description: يصف هذا الموضوع كيفيه إضافة التعليمات البرمجية لبرنامج نصي من جانب العميل إلى صفحات موقعك لدعم مجموعة تتبع الاستخدام من جانب العميل.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914529"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="07a1c-103">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="07a1c-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="07a1c-104">يصف هذا الموضوع كيفيه إضافة التعليمات البرمجية لبرنامج نصي من جانب العميل إلى صفحات موقعك لدعم مجموعة تتبع الاستخدام من جانب العميل.</span><span class="sxs-lookup"><span data-stu-id="07a1c-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="07a1c-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="07a1c-105">Overview</span></span>

<span data-ttu-id="07a1c-106">تُعد تحليلات الويب أداة أساسية عندما ترغب في فهم كيفية تفاعل عملائك مع موقعك واتخاذ قرارات من شأنها أن تساعد في تحسين التجربة لتحقيق أقصى قدر من التحويل.</span><span class="sxs-lookup"><span data-stu-id="07a1c-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="07a1c-107">تتوفر العديد من حزم تحليلات الويب لمساعدتك في تحقيق هذه الأهداف، مثل Google Analytics وClicky وMoz Analytics وKISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="07a1c-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="07a1c-108">تتطلب معظم حزم تحليلات الويب أن تضيف التعليمات البرمجية لبرنامج نصي في عنصر **\<العنوان\>** من HTML لجميع صفحات موقعك.</span><span class="sxs-lookup"><span data-stu-id="07a1c-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="07a1c-109">تنطبق الإرشادات الواردة في هذا الموضوع أيضًا على الوظائف المخصصة الأخرى من جانب العميل التي لا يوفرها Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="07a1c-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="07a1c-110">إنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي</span><span class="sxs-lookup"><span data-stu-id="07a1c-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="07a1c-111">بعد إنشاء جزء من التعليمات البرمجية الخاصة بالبرنامج النصي، يمكن إعادة استخدامه في جميع الصفحات على موقعك.</span><span class="sxs-lookup"><span data-stu-id="07a1c-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="07a1c-112">انتقل إلى **أجزاء \> جزء صفحة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="07a1c-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="07a1c-113">حدد **البرنامج النصي الخارجي**، وأدخل اسمًا للجزء ،ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="07a1c-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="07a1c-114">في التدرج الهرمي للجزء، حدد الوحدة النمطية التابعة لـ **حاقن البرنامج النصي** للجزء الذي أنشأته للتو.</span><span class="sxs-lookup"><span data-stu-id="07a1c-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="07a1c-115">في جزء الخصائص على اليمين، أضف البرنامج النصي الخاص بك من جانب العميل، واضبط خيارات التكوين الأخرى حسب الطلب.</span><span class="sxs-lookup"><span data-stu-id="07a1c-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="07a1c-116">أضف الجزء إلى القوالب</span><span class="sxs-lookup"><span data-stu-id="07a1c-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="07a1c-117">انتقل إلى **القوالب**، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.</span><span class="sxs-lookup"><span data-stu-id="07a1c-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="07a1c-118">في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .</span><span class="sxs-lookup"><span data-stu-id="07a1c-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="07a1c-119">حدد زر علامة الحذف (**...**) لفتحة **عنوان HTML** ، ثم حدد **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="07a1c-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="07a1c-120">حدد الجزء الذي قمت بإنشاءه للتعليمات البرمجية لبرنامجك النصي.</span><span class="sxs-lookup"><span data-stu-id="07a1c-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="07a1c-121">قم بحفظ القالب وإيداعه.</span><span class="sxs-lookup"><span data-stu-id="07a1c-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="07a1c-122">بعد الانتهاء، يجب عليك نشر الجزء والقالب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="07a1c-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="07a1c-123">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="07a1c-123">Additional resources</span></span>

[<span data-ttu-id="07a1c-124">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="07a1c-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="07a1c-125">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="07a1c-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="07a1c-126">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="07a1c-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="07a1c-127">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="07a1c-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="07a1c-128">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="07a1c-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="07a1c-129">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="07a1c-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="07a1c-130">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="07a1c-130">Add languages to your site</span></span>](add-languages-to-site.md)
