---
title: ملفات تعريف التقييم
description: يصف هذا الموضوع كيفية إعداد بيانات ملفات تعريف التصنيف.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb2b7a5edcee6e248798a6bee114c7da7ecb18a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973950"
---
# <a name="rating-profiles"></a><span data-ttu-id="be833-103">ملفات تعريف التقييم</span><span class="sxs-lookup"><span data-stu-id="be833-103">Rating profiles</span></span>

<span data-ttu-id="be833-104">يمثل ملف تعريف التقييم عقد التجهيز (لكن ليس عقدا قانونيا).</span><span class="sxs-lookup"><span data-stu-id="be833-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="be833-105">وهو يستخدم لتحديد تعريفات نقل الحمولات.</span><span class="sxs-lookup"><span data-stu-id="be833-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="be833-106">يعتبر كل ملف تعريف تقييم فريداً لشركة شحن.</span><span class="sxs-lookup"><span data-stu-id="be833-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="be833-107">في كل ملف تعريف، يتم إقران أسعار شركة الشحن بسجل أسعار رئيسي.</span><span class="sxs-lookup"><span data-stu-id="be833-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="be833-108">يحدد سجل الأسعار الرئيسي مهمة قاعدة الأسعار وقاعدة الأسعار.</span><span class="sxs-lookup"><span data-stu-id="be833-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="be833-109">تحدد قاعدة السعر سعر الناقل.</span><span class="sxs-lookup"><span data-stu-id="be833-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="be833-110">يمكنك إعداد ملف تعريف تقييم باستخدام صفحة عامة تعرض نظرة عامة على كافة ملفات تعريف التقييم الموجودة.</span><span class="sxs-lookup"><span data-stu-id="be833-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="be833-111">بدلاً من ذلك، يمكنك إعداد ملف تعريف تقييم مباشرة من شركة الشحن.</span><span class="sxs-lookup"><span data-stu-id="be833-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="be833-112">وفي كلتا الحالتين ، تكون المعلومات التي قمت باعدادها لملف تعريف التصنيف هي نفسها.</span><span class="sxs-lookup"><span data-stu-id="be833-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="be833-113">إنشاء ملف تعريف التقييم أو تحريره في صفحه ملفات تعريف التصنيف</span><span class="sxs-lookup"><span data-stu-id="be833-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="be833-114">في صفحه **ملفات تعريف التصنيف**، يمكنك مراجعه كافة ملفات تعريف التصنيف المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="be833-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="be833-115">يمكنك أيضا تحرير ملفات تعريف موجودة وإنشاء ملفات تعريف جديده.</span><span class="sxs-lookup"><span data-stu-id="be833-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="be833-116">انتقل إلى **إدارة النقل \> إعداد \> التقييم‬ \> السجل الرئيسي للأسعار**.</span><span class="sxs-lookup"><span data-stu-id="be833-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="be833-117">في جزء الاجراء، حدد **جديد** لأضافه ملف تعريف تقييم جديد إلى الشبكة ، أو حدد **تحرير** لتحرير ملف تعريف موجود.</span><span class="sxs-lookup"><span data-stu-id="be833-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="be833-118">في الصف الخاص بملف تعريف التقييم الجديد أو الموجود ، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="be833-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="be833-119">**ملف تعريف التصنيف** أدخل معرّفًا فريدًا (ID) ووصفًا لملف تعريف التقييم.</span><span class="sxs-lookup"><span data-stu-id="be833-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="be833-120">**الاسم** - أدخل اسمًا وصفيًا لملف تعريف التصنيف.</span><span class="sxs-lookup"><span data-stu-id="be833-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="be833-121">**شركه الشحن** - تحديد شركه شحن.</span><span class="sxs-lookup"><span data-stu-id="be833-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="be833-122">سيظهر أيضا ملف تعريف التقييم الذي تقوم باعداده في الصفحة **شركات الشحن** لشركه الشحن المحددة.</span><span class="sxs-lookup"><span data-stu-id="be833-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="be833-123">**الموقع** و **المستودع** - تحديد موقع ومستودع.</span><span class="sxs-lookup"><span data-stu-id="be833-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="be833-124">**محرك الأسعار** – تحديد محرك الأسعار لملف تعريف التصنيف.</span><span class="sxs-lookup"><span data-stu-id="be833-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="be833-125">**السجل الرئيسي للأسعار** – تحديد السجل الرئيسي للأسعار لملف تعريف التصنيف.</span><span class="sxs-lookup"><span data-stu-id="be833-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="be833-126">يمكنك استخدام سجل الأسعار الرئيسي لتعريف نوع قاعد السعر وقاعدة السعر.</span><span class="sxs-lookup"><span data-stu-id="be833-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="be833-127">لمزيد من المعلومات، راجع [إعداد السجلات الرئيسية اللأسعار‬‬‬‬](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="be833-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="be833-128">**محرك وقت تحديد عدد أيام النقل** – تحديد محرك الوقت الخاص بتحديد عدد أيام النقل لملف تعريف التقييم.</span><span class="sxs-lookup"><span data-stu-id="be833-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="be833-129">**مؤشر الوقود لشركة النقل** - تحديد مؤشر الوقود لشركة النقل لملف تعريف التقييم.</span><span class="sxs-lookup"><span data-stu-id="be833-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="be833-130">**تاريخ ووقت بدء السريان** و **تاريخ ووقت انتهاء السريان** - تحديد الفترة التي يجب ان يكون فيها ملف تعريف التصنيف نشطا.</span><span class="sxs-lookup"><span data-stu-id="be833-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="be833-131">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="be833-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="be833-132">إنشاء ملف تعريف التقييم مباشرة في صفحه شركات الشحن</span><span class="sxs-lookup"><span data-stu-id="be833-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="be833-133">انتقل إلى **إدارة النقل \> إعداد \> شركات النقل‬‬ \> شركات الشحن‬‬**.</span><span class="sxs-lookup"><span data-stu-id="be833-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="be833-134">حدد شركة شحن في القائمة.</span><span class="sxs-lookup"><span data-stu-id="be833-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="be833-135">في علامة التبويب السريعة **ملفات تعريف التصنيف**، حدد **جديد** لإنشاء ملف تعريف تقييم.</span><span class="sxs-lookup"><span data-stu-id="be833-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="be833-136">تتيح تعيين الحقول لملف تعريف التقييم الجديد.</span><span class="sxs-lookup"><span data-stu-id="be833-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="be833-137">تتوافق هذه الحقول مع الحقول الموجودة في صفحه **ملفات تعريف التصنيف**، كما هو موضح في القسم السابق من هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="be833-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="be833-138">ويتم أيضا عرض ملفات التعريف التي تم إنشاؤها في الصفحة **شركات الشحن** في صفحه **ملفات تعريف التصنيف**.</span><span class="sxs-lookup"><span data-stu-id="be833-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>
