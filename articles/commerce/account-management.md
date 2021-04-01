---
title: صفحات والوحدات النمطية لإدارة الحساب
description: يُغطي هذا الموضوع صفحات إدارة الحساب والوحدات النمطية في Microsoft Dynamics 365 Commerce.
author: v-chgri
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206621"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="fb82c-103">صفحات والوحدات النمطية لإدارة الحساب</span><span class="sxs-lookup"><span data-stu-id="fb82c-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fb82c-104">يُغطي هذا الموضوع صفحات إدارة الحساب والوحدات النمطية في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fb82c-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fb82c-105">تُشير إدارة الحساب إلى مجموعة من الصفحات المستخدمة لإدارة المعلومات ذات الصلة بحساب المستخدم في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fb82c-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="fb82c-106">تتضمن صفحات إدارة الحساب الصفحة المنتقل إليها لإدارة الحساب وصفحة ملف تعريف المستخدم وصفحة عنوان المستخدم وصفحة محفوظات الطلب وصفحة تفاصيل الطلب وصفحة الولاء وصفحة الأمنيات.</span><span class="sxs-lookup"><span data-stu-id="fb82c-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="fb82c-107">الصفحة المنتقل إليها لإدارة الحسابات</span><span class="sxs-lookup"><span data-stu-id="fb82c-107">Account management landing page</span></span>

<span data-ttu-id="fb82c-108">تستخدم الصفحة المنتقل إليها في إدارة الحساب الوحدات النمطية التالية:</span><span class="sxs-lookup"><span data-stu-id="fb82c-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="fb82c-109">**الحاوية** - يجب وضع كافة الوحدات النمطية للصفحة المنتقل إليها لإدارة الحسابات في حاوية واحدة..</span><span class="sxs-lookup"><span data-stu-id="fb82c-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="fb82c-110">**لوحة رسالة ترحيب الحساب** - تستخدم هذه الوحدة النمطية لتوفير رسالة ترحيب في صفحة إدارة الحساب.</span><span class="sxs-lookup"><span data-stu-id="fb82c-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="fb82c-111">وهي تتضمن خصائص للعنوان.</span><span class="sxs-lookup"><span data-stu-id="fb82c-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="fb82c-112">**لوحة الحساب العامة** - يمكن استخدام هذه الوحدة النمطية لتوفير عناوين وارتباطات إلى صفحات إدارة الحسابات، مثل صفحات "محفوظات الأوامر" أو "ملف تعريفي".</span><span class="sxs-lookup"><span data-stu-id="fb82c-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="fb82c-113">يمكن استخدام الوحدة النمطية للوحة العامة لتكوين لوحة لأي صفحة.</span><span class="sxs-lookup"><span data-stu-id="fb82c-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="fb82c-114">في Fabrikam، يتم استخدام هذه الوحدة النمطية لارتباطات صفحات "محفوظات الأوامر" و"ملف تعريفي" في الصفحة المنتقل إليها لإدارة الحسابات.</span><span class="sxs-lookup"><span data-stu-id="fb82c-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="fb82c-115">**لوحة قائمة أمنيات الحساب** - تستخدم هذه الوحدة النمطية لتوفير ملخص للعناصر الموجودة في قائمة أمنيات العميل.</span><span class="sxs-lookup"><span data-stu-id="fb82c-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="fb82c-116">على سبيل المثال، قد يذكر، "لديك 10 عناصر في قائمة الأمنيات الخاصة بك."</span><span class="sxs-lookup"><span data-stu-id="fb82c-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="fb82c-117">وهي تتضمن خصائص للعنوان وارتباط "عرض التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="fb82c-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="fb82c-118">ويجب أن يتم تكوين ارتباط "عرض التفاصيل" لإعادة التوجيه إلى صفحة قائمة الأمنيات.</span><span class="sxs-lookup"><span data-stu-id="fb82c-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="fb82c-119">**لوحة عنوان الحساب** - تستخدم هذه الوحدة النمطية لتوفير ملخص لعناوين المستخدم.</span><span class="sxs-lookup"><span data-stu-id="fb82c-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="fb82c-120">على سبيل المثال، قد يذكر، "لديك عنوانين تمت إضافتهم إلى حسابك."</span><span class="sxs-lookup"><span data-stu-id="fb82c-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="fb82c-121">وهي تتضمن خصائص للعنوان وارتباط "عرض التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="fb82c-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="fb82c-122">ويجب أن يتم تكوين ارتباط "عرض التفاصيل" لإعادة التوجيه إلى صفحة ملف العنوان.</span><span class="sxs-lookup"><span data-stu-id="fb82c-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="fb82c-123">**لوحة ولاء الحساب** - تستخدم هذه الوحدة النمطية لعرض وربط معلومات برنامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="fb82c-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="fb82c-124">تحتوي هذه اللوحة على حالتين: حالة تعرض للارتباطات للانضمام إلى برنامج الولاء إذا لم يكن المستخدم من أعضاء البرنامج.</span><span class="sxs-lookup"><span data-stu-id="fb82c-124">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="fb82c-125">وتعرض الحالة الأخرى ارتباطات لعرض صفحة تفاصيل الولاء عندما يكون المستخدم من أعضاء البرنامج.</span><span class="sxs-lookup"><span data-stu-id="fb82c-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="fb82c-126">تتضمن الخصائص ارتباط "التسجيل" وارتباط "عرض الولاء".</span><span class="sxs-lookup"><span data-stu-id="fb82c-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="fb82c-127">ويجب أن يتم تكوين ارتباط "عرض الولاء" لإعادة التوجيه إلى صفحة الولاء.</span><span class="sxs-lookup"><span data-stu-id="fb82c-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="fb82c-128">ويجب أن يتم تكوين ارتباط "التسجيل" لإعادة التوجيه إلى صفحة يُمكن للمستخدمين الانضمام إلى برنامج الولاء من خلالها.</span><span class="sxs-lookup"><span data-stu-id="fb82c-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="fb82c-129">صفحة سجل الأمر</span><span class="sxs-lookup"><span data-stu-id="fb82c-129">Order history page</span></span>

<span data-ttu-id="fb82c-130">تستخدم صفحة سجل الأمر الوحدة النمطية لسجل الأمر لعرض كافة الأوامر الحديثة التي قام المستخدم بوضعها.</span><span class="sxs-lookup"><span data-stu-id="fb82c-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="fb82c-131">صفحة تفاصيل الأمر</span><span class="sxs-lookup"><span data-stu-id="fb82c-131">Order details page</span></span>

<span data-ttu-id="fb82c-132">توفر صفحة تفاصيل الأمر معلومات مفصلة لكل أمر ويتم الوصول إليها من صفحة سجل الأمر.</span><span class="sxs-lookup"><span data-stu-id="fb82c-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="fb82c-133">وهي تستخدم الوحدة النمطية لتفاصيل الأمر، والتي تتطلب وجود مُعرف المبيعات أو مُعرف الحركة لاسترداد تفاصيل الأمر.</span><span class="sxs-lookup"><span data-stu-id="fb82c-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="fb82c-134">صفحة ملف تعريف المستخدم</span><span class="sxs-lookup"><span data-stu-id="fb82c-134">User profile page</span></span>

<span data-ttu-id="fb82c-135">تعرض صفحة ملف تعريف المستخدم تفاصيل حساب المستخدم، مثل اسم المستخدم وعنوان البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="fb82c-135">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="fb82c-136">وهي تستخدم تفاصيل ملف تعريف المستخدم ووحدات تحرير ملف تعريف المستخدم.</span><span class="sxs-lookup"><span data-stu-id="fb82c-136">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="fb82c-137">على الرغم من عدم إمكانية إزالة عنوان البريد الإلكتروني، إلا أنه يُمكن تحريره.</span><span class="sxs-lookup"><span data-stu-id="fb82c-137">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="fb82c-138">تظهر صفحة ملف تعريف المستخدم أيضًا تفضيلات المستخدم التي تُمكن المستخدم من تمكين أو تعطيل ميزات معينة، مثل تخصيص قوائم التوصيات.</span><span class="sxs-lookup"><span data-stu-id="fb82c-138">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="fb82c-139">صفحة عنوان المستخدم</span><span class="sxs-lookup"><span data-stu-id="fb82c-139">User address page</span></span>

<span data-ttu-id="fb82c-140">تعرض صفحة عنوان المستخدم قائمة العناوين المقترنة بحساب المستخدم.</span><span class="sxs-lookup"><span data-stu-id="fb82c-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="fb82c-141">قام المستخدم إما بتوفير هذه العناوين في أثناء السداد مع الخروج أو تمت إضافتهم مباشرة في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fb82c-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="fb82c-142">يتم استخدام الوحدة النمطية لعنوان المستخدم لإضافة العناوين وتحريرها وتعيين العنوان الرئيسي وعرض العناوين الموجودة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fb82c-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="fb82c-143">صفحة قائمة الأمنيات</span><span class="sxs-lookup"><span data-stu-id="fb82c-143">Wish list page</span></span>

<span data-ttu-id="fb82c-144">تعرض صفحة قائمة الأمنيات الأصناف التي تمت إضافتها إلى قائمة أمنيات العميل.</span><span class="sxs-lookup"><span data-stu-id="fb82c-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="fb82c-145">وهي تستخدم الوحدة النمطية للأمنيات لعرض أصناف الأمنيات.</span><span class="sxs-lookup"><span data-stu-id="fb82c-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="fb82c-146">صفحه الولاء</span><span class="sxs-lookup"><span data-stu-id="fb82c-146">Loyalty page</span></span>

<span data-ttu-id="fb82c-147">تُتيح صفحة الولاد للعملاء عرض تفاصيل ولائهم إذا كانوا أعضاء في برنامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="fb82c-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="fb82c-148">ويُمكنهم أيضًا عرض النقاط التي اكتسبوها واستردادها في الحركات الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="fb82c-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="fb82c-149">تستخدم الصفحة الوحدة النمطية لتفاصيل الولاء لإظهار تفاصيل الولاء.</span><span class="sxs-lookup"><span data-stu-id="fb82c-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="fb82c-150">للانضمام إلى برنامج الولاء، يمكن إنشاء صفحة تسويق باستخدام وحدة التسجيل في برنامج الولاء ووحدة شروط برنامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="fb82c-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="fb82c-151">إذا لم يكن المستخدم عضوًا في برنامج الولاء، فستقوم هذه الوحدات النمطية بتمكين المستخدم للتسجيل.</span><span class="sxs-lookup"><span data-stu-id="fb82c-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb82c-152">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fb82c-152">Additional resources</span></span>

[<span data-ttu-id="fb82c-153">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="fb82c-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fb82c-154">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="fb82c-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="fb82c-155">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="fb82c-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="fb82c-156">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="fb82c-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fb82c-157">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="fb82c-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fb82c-158">وحدة تأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="fb82c-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fb82c-159">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="fb82c-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="fb82c-160">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="fb82c-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]