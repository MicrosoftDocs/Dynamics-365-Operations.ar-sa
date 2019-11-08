---
title: تعقب المصادر لملفات التعريف واستمارات التقديم الخاصة بالمرشحين
description: يوفر هذا الموضوع معلومات حول تعقب المصدر لملفات تعريف المرشحين واستمارات التقديم الخاصة بهم.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 5b368e97a716cd1ce4f668c2a97326877a2d3dff
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551877"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a><span data-ttu-id="72bfa-103">تعقب المصادر لملفات التعريف واستمارات التقديم الخاصة بالمرشحين</span><span class="sxs-lookup"><span data-stu-id="72bfa-103">Track sources for candidate profiles and applications</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="72bfa-104">تتوفر الوظيفة المذكورة في هذا الموضوع كجزء من إصدار مراجعة المعاينة.</span><span class="sxs-lookup"><span data-stu-id="72bfa-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="72bfa-105">المحتوى والوظيفة عرضة للتغيير.</span><span class="sxs-lookup"><span data-stu-id="72bfa-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="72bfa-106">لاستخدام هذه الميزة، اطلب من مسؤول تمكينها باستخدام **إعدادات المسؤول** في Attract.</span><span class="sxs-lookup"><span data-stu-id="72bfa-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="72bfa-107">سيوفر إصدار مستقبلي لك تقارير تعقب المصدر.</span><span class="sxs-lookup"><span data-stu-id="72bfa-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="72bfa-108">للحصول على مزيد من المعلومات، راجع [الوصول إلى ميزات المعاينة في Talent‬](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="72bfa-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="72bfa-109">عندما يقدم المرشحون طلبات الحصول على الوظيفة، يقوم Attract بشكل تلقائي بتعقب استمارات تقديم هؤلاء المرشحين، ويوفر لك معلومات قيّمة لمساعدتك في توجيه الجهود التي تبذلها في مجال التعيين.</span><span class="sxs-lookup"><span data-stu-id="72bfa-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="72bfa-110">بإمكان مسؤولي التعيين ومدراء التوظيف أيضًا تحديد مصدر استمارة التقديم أثناء إضافة مرشح إلى مجموعة وظائف أو مجموعة مواهب.‬</span><span class="sxs-lookup"><span data-stu-id="72bfa-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="72bfa-111">يمكنك عرض مصدر استمارة التقديم في نشاط استمارة التقديم ضمن علامة التبويب **النشاط**، وكذلك الأمر في سجل التوظيف ضمن **ملف التعريف** في مجموعات المواهب.=</span><span class="sxs-lookup"><span data-stu-id="72bfa-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="72bfa-112">يمكنك العثور على مصدر ملف تعريف المرشح في تفاصيل المرشح ضمن علامة التبويب **ملف التعريف** في مجموعات استمارات التقديم والمواهب.</span><span class="sxs-lookup"><span data-stu-id="72bfa-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="72bfa-113">يمكنك العثور على قوالب العملية في [المكون الإضافي "التوظيف الشامل"](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="72bfa-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="72bfa-114">المصادر المكوّنة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="72bfa-114">Pre-configured sources</span></span>

<span data-ttu-id="72bfa-115">تحتوي قائمة المصادر الافتراضية على مصادر استمارات التقديم الشائعة.</span><span class="sxs-lookup"><span data-stu-id="72bfa-115">The default source list contains common application sources.</span></span> <span data-ttu-id="72bfa-116">تتضمن بعض أنواع المصادر، مثل **لوحة الوظائف** و**الشبكة الاجتماعية** تفاصيل مصادر إضافية.</span><span class="sxs-lookup"><span data-stu-id="72bfa-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="72bfa-117">على سبيل المثال، تتضمن **الشبكة الاجتماعية** Facebook وTwitter.</span><span class="sxs-lookup"><span data-stu-id="72bfa-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="72bfa-118">يسمح لك نوع المصدر**إحالة‬** بتحديد موظف داخلي كمحيل.</span><span class="sxs-lookup"><span data-stu-id="72bfa-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="72bfa-119">تتضمن قائمة المصادر الافتراضية المصادر التالية المعرفة مسبقًا:</span><span class="sxs-lookup"><span data-stu-id="72bfa-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="72bfa-120">موقع وظائف Attract</span><span class="sxs-lookup"><span data-stu-id="72bfa-120">Attract career site</span></span>

-   <span data-ttu-id="72bfa-121">الوكالة</span><span class="sxs-lookup"><span data-stu-id="72bfa-121">Agency</span></span>

-   <span data-ttu-id="72bfa-122">معرض الوظائف</span><span class="sxs-lookup"><span data-stu-id="72bfa-122">Career Fair</span></span>

-   <span data-ttu-id="72bfa-123">تسويق الشركة</span><span class="sxs-lookup"><span data-stu-id="72bfa-123">Company Marketing</span></span>

-   <span data-ttu-id="72bfa-124">المؤتمرات والمعارض التجارية</span><span class="sxs-lookup"><span data-stu-id="72bfa-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="72bfa-125">النقابات المهنية</span><span class="sxs-lookup"><span data-stu-id="72bfa-125">Professional Association</span></span>

-   <span data-ttu-id="72bfa-126">لوحة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="72bfa-126">Job board</span></span>

    -   <span data-ttu-id="72bfa-127">Indeed</span><span class="sxs-lookup"><span data-stu-id="72bfa-127">Indeed</span></span>

    -   <span data-ttu-id="72bfa-128">Seek</span><span class="sxs-lookup"><span data-stu-id="72bfa-128">Seek</span></span>

    -   <span data-ttu-id="72bfa-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="72bfa-129">CareerBuilder</span></span>

    -   <span data-ttu-id="72bfa-130">Google Jobs</span><span class="sxs-lookup"><span data-stu-id="72bfa-130">Google Jobs</span></span>

    -   <span data-ttu-id="72bfa-131">Xing</span><span class="sxs-lookup"><span data-stu-id="72bfa-131">Xing</span></span>

    -   <span data-ttu-id="72bfa-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="72bfa-132">Glassdoor</span></span>

    -   <span data-ttu-id="72bfa-133">Monster Jobs</span><span class="sxs-lookup"><span data-stu-id="72bfa-133">Monster Jobs</span></span>

-   <span data-ttu-id="72bfa-134">المجلات والمنشورات</span><span class="sxs-lookup"><span data-stu-id="72bfa-134">Magazines & Publications</span></span>

-   <span data-ttu-id="72bfa-135">الشبكة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="72bfa-135">Social Network</span></span>

    -   <span data-ttu-id="72bfa-136">Facebook</span><span class="sxs-lookup"><span data-stu-id="72bfa-136">Facebook</span></span>

    -   <span data-ttu-id="72bfa-137">Twitter</span><span class="sxs-lookup"><span data-stu-id="72bfa-137">Twitter</span></span>

-   <span data-ttu-id="72bfa-138">التوظيف في الجامعة</span><span class="sxs-lookup"><span data-stu-id="72bfa-138">University Recruiting</span></span>

-   <span data-ttu-id="72bfa-139">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="72bfa-139">LinkedIn</span></span>

-   <span data-ttu-id="72bfa-140">الإعلانات المبوبة</span><span class="sxs-lookup"><span data-stu-id="72bfa-140">Classifieds</span></span>

-   <span data-ttu-id="72bfa-141">إحالة</span><span class="sxs-lookup"><span data-stu-id="72bfa-141">Referral</span></span>

-   <span data-ttu-id="72bfa-142">مُضاف من قِبل مسؤول التعيين</span><span class="sxs-lookup"><span data-stu-id="72bfa-142">Added by Recruiter</span></span>

-   <span data-ttu-id="72bfa-143">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="72bfa-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="72bfa-144">تخصيص قائمة المصادر</span><span class="sxs-lookup"><span data-stu-id="72bfa-144">Customize the source list</span></span> 

<span data-ttu-id="72bfa-145">يمكنك توسيع قائمة المصادر بحيث تتضمن مصادر استمارات تقديم إضافية.</span><span class="sxs-lookup"><span data-stu-id="72bfa-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="72bfa-146">لتخصيص هذه القائمة، اتبع الإرشادات الموجودة في [توسيع مجموعات الخيارات في Attract‬](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span><span class="sxs-lookup"><span data-stu-id="72bfa-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="72bfa-147">حرر الكيان **TalentSource‎** بحيث يتضمن مصادر إضافية.</span><span class="sxs-lookup"><span data-stu-id="72bfa-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="72bfa-148">لتجنب التأثير السلبي على واجهة المستخدم (UI)، لا تعمل على تحرير أو حذف قيم تعداد (وليس أسماء) **TalentCategory** لما يلي:</span><span class="sxs-lookup"><span data-stu-id="72bfa-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="72bfa-149">**إحالة**</span><span class="sxs-lookup"><span data-stu-id="72bfa-149">**Referral**</span></span>
- <span data-ttu-id="72bfa-150">**LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="72bfa-150">**LinkedIn**</span></span>
- <span data-ttu-id="72bfa-151">**‏‏غير ذلك**</span><span class="sxs-lookup"><span data-stu-id="72bfa-151">**Other**</span></span>

<span data-ttu-id="72bfa-152">بدلاً من ذلك، يمكنك توسيع تعداد **TalentSource** لإضافة أنواع أخرى من المصادر.</span><span class="sxs-lookup"><span data-stu-id="72bfa-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>
