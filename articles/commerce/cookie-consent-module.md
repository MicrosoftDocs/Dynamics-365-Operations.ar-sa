---
title: الوحدة النمطية للموافقة على ملف تعريف الارتباط
description: يتناول هذا الموضوع الوحدات النمطية للموافقة على ملف تعريف الارتباط ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 60ce530575841c22355e4a14e8b0bbec6c0e35ab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409791"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="bfa37-103">الوحدة النمطية للموافقة على ملف تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="bfa37-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bfa37-104">يتناول هذا الموضوع الوحدات النمطية للموافقة على ملف تعريف الارتباط ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bfa37-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bfa37-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="bfa37-105">Overview</span></span>

<span data-ttu-id="bfa37-106">تطالب الوحدة النمطية للموافقة على ملف تعريف الارتباط المستخدمين بتوفير موافقة صريحة على السماح بملفات تعريف الارتباط لأي ميزة أو وحدة نمطية تتعقب ملفات تعريف ارتباط المستعرض.</span><span class="sxs-lookup"><span data-stu-id="bfa37-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="bfa37-107">تكون الموافقة مطلوبة في المرة الأولى التي يقوم فيها مستخدم موقع باستعراض موقع في جلسة عمل مستعرض جديدة.</span><span class="sxs-lookup"><span data-stu-id="bfa37-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="bfa37-108">عند تلقي الموافقة، يتم تعقبها ولن تتم مطالبة مستخدم الموقع بإعطاء الموافقة مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="bfa37-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="bfa37-109">لمزيد من المعلومات، راجع [التوافق مع ملف تعريف الارتباط](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="bfa37-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="bfa37-110">إذا لم يتم استلام الموافقة على ملفات تعريف الارتباط من مستخدم الموقع، لن تظهر على الصفحة أي ميزات أو وحدات نمطية تتطلب الموافقة على ملفات تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="bfa37-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="bfa37-111">على سبيل المثال، تتطلب الوحدة النمطية للسداد مع الخروج والوحدة النمطية للمشاركة الاجتماعية وميزة المتجر المفضل الموافقة على ملفات تعريف الارتباط ولن تظهر إذا لم يتم استلام موافقة مستخدم الموقع.</span><span class="sxs-lookup"><span data-stu-id="bfa37-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="bfa37-112">يمكن تكوين الوحدة النمطية للموافقة على ملف تعريف الارتباط على جزء رأس الصفحة بحيث يمكن تنفيذها عند تحميل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bfa37-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="bfa37-113">يجب أن تتضمن الوحدة النمطية للموافقة على ملف تعريف الارتباط رسالة واضحة تُعلم مستخدم الوقع عن استخدام ملفات تعريف الارتباط في الموقع ويجب أن توفر ارتباطًا غلى صفحة خصوصية الموقع.</span><span class="sxs-lookup"><span data-stu-id="bfa37-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="bfa37-114">يبين الرسم التوضيحي التالي مثالاً على رسالة الموافقة على ملفات تعريف الارتباط مع ارتباط إلى صفحة سياسة خصوصية الموقع يظهر على رأس صفحة الموقع.</span><span class="sxs-lookup"><span data-stu-id="bfa37-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="bfa37-115">![مثال عن وحدة نمطية للموافقة على ملف تعريف الارتباط](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="bfa37-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="bfa37-116">خصائص الوحدة النمطية للموافقة على ملف تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="bfa37-116">Cookie consent module properties</span></span>

| <span data-ttu-id="bfa37-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="bfa37-117">Property name</span></span>             | <span data-ttu-id="bfa37-118">قيمة</span><span class="sxs-lookup"><span data-stu-id="bfa37-118">Value</span></span>                 | <span data-ttu-id="bfa37-119">الوصف</span><span class="sxs-lookup"><span data-stu-id="bfa37-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="bfa37-120">نص منسق</span><span class="sxs-lookup"><span data-stu-id="bfa37-120">Rich Text</span></span>                  | <span data-ttu-id="bfa37-121">نص منسق</span><span class="sxs-lookup"><span data-stu-id="bfa37-121">Rich Text</span></span> | <span data-ttu-id="bfa37-122">تحديد اعلام نص منسق لمستخدمي الموقع يفيد بأن الموقع يستخدم ملفات تعريف ارتباط المستعرض وأنه يتعين على المستخدمين قبول استخدام ملفات تعريف الارتباط كي يعمل الموقع بشكل تام.</span><span class="sxs-lookup"><span data-stu-id="bfa37-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="bfa37-123">الارتباطات</span><span class="sxs-lookup"><span data-stu-id="bfa37-123">Links</span></span> | <span data-ttu-id="bfa37-124">URL</span><span class="sxs-lookup"><span data-stu-id="bfa37-124">URL</span></span> | <span data-ttu-id="bfa37-125">يمكن إضافة ارتباط واحد أو أكثر إلى صفحة خصوصية الموقع التي تصف أنواع ملفات تعريف الارتباط التي يتم تعقبها على الموقع.</span><span class="sxs-lookup"><span data-stu-id="bfa37-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="bfa37-126">إضافة وحدة نمطية للموافقة على ملف تعريف الارتباط إلى صفحات الموقع</span><span class="sxs-lookup"><span data-stu-id="bfa37-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="bfa37-127">لإضافة وحدة نمطية للموافقة على ملف تعريف الارتباط لعدة صفحات في الموقع بكفاءة، يمكن إضافتها إلى جزء رأس الصفحة المشتركة.</span><span class="sxs-lookup"><span data-stu-id="bfa37-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="bfa37-128">بعد إضافة جزء الرأس إلى جميع صفحات الموقع، سيظهر إعلام بالموافقة على ملفات تعريف الارتباط بشكل تلقائي في المرة الأولى التي ينتقل فيها المستخدم إلى أي صفحة في الموقع.</span><span class="sxs-lookup"><span data-stu-id="bfa37-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="bfa37-129">لمزيد من المعلومات حول أجزاء الرأس والوحدات النمطية، راجع [الوحدة النمطية للرأس](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="bfa37-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bfa37-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="bfa37-130">Additional resources</span></span>

[<span data-ttu-id="bfa37-131">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="bfa37-131">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bfa37-132">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="bfa37-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="bfa37-133">توافق ملفات تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="bfa37-133">Cookie compliance</span></span>](cookie-compliance.md)
