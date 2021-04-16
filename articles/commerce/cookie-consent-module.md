---
title: الوحدة النمطية للموافقة على ملف تعريف الارتباط
description: يتناول هذا الموضوع الوحدات النمطية للموافقة على ملف تعريف الارتباط ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2f0118b197f465113bb894e3e57b3e682e04ef36
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795993"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="6fac3-103">الوحدة النمطية للموافقة على ملف تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="6fac3-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6fac3-104">يتناول هذا الموضوع الوحدات النمطية للموافقة على ملف تعريف الارتباط ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6fac3-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6fac3-105">تطالب الوحدة النمطية للموافقة على ملف تعريف الارتباط المستخدمين بتوفير موافقة صريحة على السماح بملفات تعريف الارتباط لأي ميزة أو وحدة نمطية تتعقب ملفات تعريف ارتباط المستعرض.</span><span class="sxs-lookup"><span data-stu-id="6fac3-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="6fac3-106">تكون الموافقة مطلوبة في المرة الأولى التي يقوم فيها مستخدم موقع باستعراض موقع في جلسة عمل مستعرض جديدة.</span><span class="sxs-lookup"><span data-stu-id="6fac3-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="6fac3-107">عند تلقي الموافقة، يتم تعقبها ولن تتم مطالبة مستخدم الموقع بإعطاء الموافقة مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="6fac3-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="6fac3-108">لمزيد من المعلومات، راجع [التوافق مع ملف تعريف الارتباط](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="6fac3-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="6fac3-109">إذا لم يتم استلام الموافقة على ملفات تعريف الارتباط من مستخدم الموقع، لن تظهر على الصفحة أي ميزات أو وحدات نمطية تتطلب الموافقة على ملفات تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="6fac3-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="6fac3-110">على سبيل المثال، تتطلب الوحدة النمطية للسداد مع الخروج والوحدة النمطية للمشاركة الاجتماعية وميزة المتجر المفضل الموافقة على ملفات تعريف الارتباط ولن تظهر إذا لم يتم استلام موافقة مستخدم الموقع.</span><span class="sxs-lookup"><span data-stu-id="6fac3-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="6fac3-111">يمكن تكوين الوحدة النمطية للموافقة على ملف تعريف الارتباط على جزء رأس الصفحة بحيث يمكن تنفيذها عند تحميل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6fac3-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="6fac3-112">يجب أن تتضمن الوحدة النمطية للموافقة على ملف تعريف الارتباط رسالة واضحة تُعلم مستخدم الوقع عن استخدام ملفات تعريف الارتباط في الموقع ويجب أن توفر ارتباطًا غلى صفحة خصوصية الموقع.</span><span class="sxs-lookup"><span data-stu-id="6fac3-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="6fac3-113">يبين الرسم التوضيحي التالي مثالاً على رسالة الموافقة على ملفات تعريف الارتباط مع ارتباط إلى صفحة سياسة خصوصية الموقع يظهر على رأس صفحة الموقع.</span><span class="sxs-lookup"><span data-stu-id="6fac3-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="6fac3-114">![مثال عن وحدة نمطية للموافقة على ملف تعريف الارتباط](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="6fac3-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="6fac3-115">خصائص الوحدة النمطية للموافقة على ملف تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="6fac3-115">Cookie consent module properties</span></span>

| <span data-ttu-id="6fac3-116">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="6fac3-116">Property name</span></span>             | <span data-ttu-id="6fac3-117">قيمة</span><span class="sxs-lookup"><span data-stu-id="6fac3-117">Value</span></span>                 | <span data-ttu-id="6fac3-118">الوصف</span><span class="sxs-lookup"><span data-stu-id="6fac3-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="6fac3-119">نص منسق</span><span class="sxs-lookup"><span data-stu-id="6fac3-119">Rich Text</span></span>                  | <span data-ttu-id="6fac3-120">نص منسق</span><span class="sxs-lookup"><span data-stu-id="6fac3-120">Rich Text</span></span> | <span data-ttu-id="6fac3-121">تحديد اعلام نص منسق لمستخدمي الموقع يفيد بأن الموقع يستخدم ملفات تعريف ارتباط المستعرض وأنه يتعين على المستخدمين قبول استخدام ملفات تعريف الارتباط كي يعمل الموقع بشكل تام.</span><span class="sxs-lookup"><span data-stu-id="6fac3-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="6fac3-122">الارتباطات</span><span class="sxs-lookup"><span data-stu-id="6fac3-122">Links</span></span> | <span data-ttu-id="6fac3-123">URL</span><span class="sxs-lookup"><span data-stu-id="6fac3-123">URL</span></span> | <span data-ttu-id="6fac3-124">يمكن إضافة ارتباط واحد أو أكثر إلى صفحة خصوصية الموقع التي تصف أنواع ملفات تعريف الارتباط التي يتم تعقبها على الموقع.</span><span class="sxs-lookup"><span data-stu-id="6fac3-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="6fac3-125">إضافة وحدة نمطية للموافقة على ملف تعريف الارتباط إلى صفحات الموقع</span><span class="sxs-lookup"><span data-stu-id="6fac3-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="6fac3-126">لإضافة وحدة نمطية للموافقة على ملف تعريف الارتباط لعدة صفحات في الموقع بكفاءة، يمكن إضافتها إلى جزء رأس الصفحة المشتركة.</span><span class="sxs-lookup"><span data-stu-id="6fac3-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="6fac3-127">بعد إضافة جزء الرأس إلى جميع صفحات الموقع، سيظهر إعلام بالموافقة على ملفات تعريف الارتباط بشكل تلقائي في المرة الأولى التي ينتقل فيها المستخدم إلى أي صفحة في الموقع.</span><span class="sxs-lookup"><span data-stu-id="6fac3-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="6fac3-128">لمزيد من المعلومات حول أجزاء الرأس والوحدات النمطية، راجع [الوحدة النمطية للرأس](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="6fac3-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fac3-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6fac3-129">Additional resources</span></span>

[<span data-ttu-id="6fac3-130">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="6fac3-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6fac3-131">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="6fac3-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="6fac3-132">توافق ملفات تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="6fac3-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]