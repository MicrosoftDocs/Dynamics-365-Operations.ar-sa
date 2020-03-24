---
title: إدارة الميزات
description: يصف هذا الموضوع كيف يمكن لمسؤول تمكين الميزات المعاينة في Microsoft Dynamics 365 Talent، ويسرد الميزات التي يجري تمكينها حاليًا للمعاينة.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124786"
---
# <a name="manage-features"></a><span data-ttu-id="1b2e5-103">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="1b2e5-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b2e5-104">كجزء من عملية النشر المستمر لإمكانات إدارة رؤوس الأموال البشرية‬ (HCM) لـ Microsoft Dynamics 365 Human Resources، نحن نريد السماح للعملاء بتجربة الميزات الجديدة في أقرب وقت ممكن.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="1b2e5-105">يمكن للمسؤولين رؤية واستخدام ميزات المعاينة في البيئات الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="1b2e5-106">هذه الميزات جاهزاً تقريبا للتوفر العام وقد خضعت للاختبارات الشاملة.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="1b2e5-107">ونحن فقط نبحث عن جولة نهائية من ملاحظات العملاء والتحقق من الصحة قبل أن نقوم بشكل عام بتحرير الميزات.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="1b2e5-108">يصف هذا الموضوع كيف يمكنك تمكين الميزات المعاينة، ويسرد الميزات المتوفرة حاليا للمعاينة.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="1b2e5-109">سيتم تحديث هذه القائمة مع إصدار الميزات للتوفر العام ومع إصدار الميزات الجديدة للمعاينة.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="1b2e5-110">لا يتم إعطاء أي إعلام عندما يتم إصدار ميزات جديدة للمعاينة.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="1b2e5-111">سيبدأ المستخدمون فقط في رؤية الميزات.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-111">Users will just start to see the features.</span></span> <span data-ttu-id="1b2e5-112">لمزيد من المعلومات حول الميزات الجديدة في Talent، راجع [ما الجديد أو المتغير‬ في ملاحظات الإصدار لكلٍّ من Dynamics 365 Talent](./whats-new.md) و[Dynamics 365 وPower Platform](https://docs.microsoft.com/business-applications-release-notes).</span><span class="sxs-lookup"><span data-stu-id="1b2e5-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="1b2e5-113">تمكين أو تعطيل ميزات المعاينة</span><span class="sxs-lookup"><span data-stu-id="1b2e5-113">Enable or disable preview features</span></span>

<span data-ttu-id="1b2e5-114">للوصول إلى ميزات المعاينة، يجب عليك أولاً تمكينها في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="1b2e5-115">تمكين أو تعطيل ميزات المعاينة يكون خاصًا بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b2e5-116">عند قيامك بتشغيل إعداد **ميزات معاينة**، يجب تمكين ميزات المعاينة لكافة المستخدمين في المؤسسة الخاصة بك في هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="1b2e5-117">عند إيقاف هذا الإعداد، يمكنك تعطيل ميزات المعاينة وجعلها غير قابلة للوصول إلى المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="1b2e5-118">يكون دعم ميزات المعاينة محدودًا في Talent.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="1b2e5-119">كما أنها تستخدم القليل من إجراءات الخصوصية والأمان، ولا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لبرنامج Talent.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="1b2e5-120">يجب عدم استخدام ميزات المعاينة لمعالجة البيانات الشخصية (بمعنى، أية معلومات يمكن من خلالها التعرف عليك)، أو لمعالجة البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="1b2e5-121">Attract</span><span class="sxs-lookup"><span data-stu-id="1b2e5-121">Attract</span></span>

1. <span data-ttu-id="1b2e5-122">تسجيل الدخول إلى Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="1b2e5-123">في قائمة **الإعداد** (رمز الترس) في الزاوية العلوية اليسرى، حدد **مركز الإدارة**.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="1b2e5-124">في علامة التبويب **إدارة الميزات**، حدد الخيار بجانب **ميزات المعاينة** بحيث يتحول إلى الأزرق ويقول**تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![تمكين ميزات المعاينة في Attract](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="1b2e5-126">قم بتحديد أو إلغاء تحديد ميزات المعاينة الفردية.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="1b2e5-127">في حاله عدم القيام بأي اجراء، يتم تمكين جميع ميزات المعاينة المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="1b2e5-128">قم بتحديث المستعرض لبدء مشاهدة الميزات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="1b2e5-129">سيشاهد أي مستخدمين قاموا بتسجيل الدخول بالفعل الميزات في المرة التالية التي يقومون فيها بتسجيل الدخول أو يمكنهم تحديث المستعرض الخاص بهم لمشاهدة الميزات مباشرةً.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="1b2e5-130">قد تتطلب بعض ميزات المعاينة تكوينًا إضافيًا.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="1b2e5-131">اتبع الارتباطات المجاورة لميزة المعاينة لإكمال الإعداد لها.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="1b2e5-132">ملاحظات</span><span class="sxs-lookup"><span data-stu-id="1b2e5-132">Feedback</span></span>

<span data-ttu-id="1b2e5-133">نريد أن نسمع منك عن تجربتك مع أيٍّ من ميزات المعاينة هذه.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="1b2e5-134">ونحن نشجعك على نشر الملاحظات الخاصة بك بشكل منتظم على المواقع التالية أثناء استخدامك لهذه الميزات أو أية ميزات أخرى:</span><span class="sxs-lookup"><span data-stu-id="1b2e5-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="1b2e5-135">[المجتمع](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) -يعد هذا الموقع مصدرا رائعًا حيث يمكن للمستخدمين مناقشة حالات الاستخدام، وطرح الأسئلة، والحصول على تعليمات من المجتمع.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="1b2e5-136">أخبرنا عن الميزات التي ترغب في رؤيتها في المنتج، أو أخبرنا عن أي تغييرات تعتقد أننا يجب أن نجريها على الميزات الحالية.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="1b2e5-137">اقترح أفكارًا للمنتج على المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="1b2e5-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="1b2e5-138">أفكار Attract</span><span class="sxs-lookup"><span data-stu-id="1b2e5-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="1b2e5-139">أفكار Onboard</span><span class="sxs-lookup"><span data-stu-id="1b2e5-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="1b2e5-140">تأكد من عدم قيامك بتضمين البيانات الشخصية (أي معلومات يمكن التعرف منه عليك) في تقديمات مراجعة الملاحظات أو المنتج.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="1b2e5-141">قد يتم تحليل المعلومات التي تم تجميعها بشكل أكبر، ولا يتم استخدامها للرد على الطلبات بموجب قوانين الخصوصية القابلة للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="1b2e5-142">البيانات الشخصية التي يتم تجميعها بشكل منفصل عن هذه البرامج تخضع لـ [بيان خصوصية Microsoft ](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="1b2e5-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="1b2e5-143">قم بعمل إشارة مرجعية لهذا الموضوع، وراجعه باستمرار لتبقى مطلعًا على أحدث ميزات المعاينة الجديدة حين نقوم بإصدارها.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b2e5-144">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="1b2e5-144">See also</span></span>

- [<span data-ttu-id="1b2e5-145">تجريب أو شراء تطبيقات Talent</span><span class="sxs-lookup"><span data-stu-id="1b2e5-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="1b2e5-146">ما الجديد أو المتغير‬ في Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="1b2e5-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="1b2e5-147">خطط الإصدارات</span><span class="sxs-lookup"><span data-stu-id="1b2e5-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="1b2e5-148">الحصول على دعم لـ Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="1b2e5-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
