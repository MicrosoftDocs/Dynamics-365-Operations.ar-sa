---
title: صفحات إدارة الحساب والوحدات النمطية
description: يُغطي هذا الموضوع صفحات إدارة الحساب والوحدات النمطية في Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885799"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="7a407-103">صفحات إدارة الحساب والوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="7a407-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7a407-104">يُغطي هذا الموضوع صفحات إدارة الحساب والوحدات النمطية في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7a407-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7a407-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="7a407-105">Overview</span></span>

<span data-ttu-id="7a407-106">تُشير إدارة الحساب إلى مجموعة من الصفحات المستخدمة لإدارة المعلومات ذات الصلة بحساب المستخدم في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7a407-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="7a407-107">تتضمن صفحات إدارة الحساب الصفحة المنتقل إليها لإدارة الحساب وصفحة ملف تعريف المستخدم وصفحة عنوان المستخدم وصفحة محفوظات الطلب وصفحة تفاصيل الطلب وصفحة الولاء وصفحة الأمنيات.</span><span class="sxs-lookup"><span data-stu-id="7a407-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="7a407-108">الصفحة المنتقل إليها لإدارة الحسابات</span><span class="sxs-lookup"><span data-stu-id="7a407-108">Account management landing page</span></span>

<span data-ttu-id="7a407-109">تستخدم الصفحة المنتقل إليها في إدارة الحساب الوحدات النمطية التالية:</span><span class="sxs-lookup"><span data-stu-id="7a407-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="7a407-110">**وضع المحتوى** - تُمثل هذه الوحدة النمطية وحدة نمطية للحاوية تحتفظ بكافة الوحدات النمطية في الصفحة المنتقل إليها لإدارة الحساب.</span><span class="sxs-lookup"><span data-stu-id="7a407-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="7a407-111">**عنصر رسالة ترحيب الحساب** - تستخدم هذه الوحدة النمطية لتوفير رسالة ترحيب في صفحة إدارة الحساب.</span><span class="sxs-lookup"><span data-stu-id="7a407-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="7a407-112">وهي تتضمن الخصائص للعنوان ولحجم التجانب.</span><span class="sxs-lookup"><span data-stu-id="7a407-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="7a407-113">تُحدد خاصية **حجم التجانب** عرض الوحدة النمطية في الوحدة النمطية لوضع المحتوى.</span><span class="sxs-lookup"><span data-stu-id="7a407-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="7a407-114">تتراوح القيم من **1** وحتى **12**، حيث تمثل **12** العرض الكامل لحاوية وضع المحتوى.</span><span class="sxs-lookup"><span data-stu-id="7a407-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="7a407-115">**صنف وضع أمر الحساب** - تستخدم هذه الوحدة النمطية لتوفير ملخص لعدد الأوامر التي تم وضعها بواسطة حساب المستخدم.</span><span class="sxs-lookup"><span data-stu-id="7a407-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="7a407-116">وهي تتضمن الخصائص للعنوان ولحجم التجانب وارتباط "عرض التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="7a407-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7a407-117">ويجب أن يتم تكوين ارتباط "عرض التفاصيل" لإعادة التوجيه إلى صفحات محفوظات الأمر.</span><span class="sxs-lookup"><span data-stu-id="7a407-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="7a407-118">**عنصر وضع ملف تعريف الحساب** - تستخدم هذه الوحدة النمطية لتوفير ملخص لملف تعريف المستخدم.</span><span class="sxs-lookup"><span data-stu-id="7a407-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="7a407-119">وهي تتضمن الخصائص للعنوان ولحجم التجانب وارتباط "عرض التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="7a407-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7a407-120">ويجب أن يتم تكوين ارتباط "عرض التفاصيل" لإعادة التوجيه إلى صفحة ملف تعريف المستخدم.</span><span class="sxs-lookup"><span data-stu-id="7a407-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="7a407-121">**عنصر أمنيات الحساب** - تستخدم هذه الوحدة النمطية لتوفير ملخص للعناصر الموجودة في قائمة أمنيات العميل.</span><span class="sxs-lookup"><span data-stu-id="7a407-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="7a407-122">على سبيل المثال، قد يذكر، "لديك 10 عناصر في قائمة الأمنيات الخاصة بك."</span><span class="sxs-lookup"><span data-stu-id="7a407-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="7a407-123">وهي تتضمن الخصائص للعنوان ولحجم التجانب وارتباط "عرض التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="7a407-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7a407-124">ويجب أن يتم تكوين ارتباط "عرض التفاصيل" لإعادة التوجيه إلى صفحة قائمة الأمنيات.</span><span class="sxs-lookup"><span data-stu-id="7a407-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="7a407-125">**عنصر عنوان الحساب** - تستخدم هذه الوحدة النمطية لتوفير ملخص لعناوين المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="7a407-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="7a407-126">على سبيل المثال، قد يذكر، "لديك عنوانين تمت إضافتهم إلى حسابك."</span><span class="sxs-lookup"><span data-stu-id="7a407-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="7a407-127">وهي تتضمن الخصائص للعنوان ولحجم التجانب وارتباط "عرض التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="7a407-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7a407-128">ويجب أن يتم تكوين ارتباط "عرض التفاصيل" لإعادة التوجيه إلى صفحة ملف العنوان.</span><span class="sxs-lookup"><span data-stu-id="7a407-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="7a407-129">**عنصر ولاء الحساب** - تستخدم هذه الوحدة النمطية لعرض وربط معلومات برنامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="7a407-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="7a407-130">وهي تتضمن الخصائص للعنوان ولحجم التجانب وارتباط "عرض التفاصيل"، وارتباط "كن عضوًا".</span><span class="sxs-lookup"><span data-stu-id="7a407-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="7a407-131">ويجب أن يتم تكوين ارتباط "عرض التفاصيل" لإعادة التوجيه إلى صفحة الولاء.</span><span class="sxs-lookup"><span data-stu-id="7a407-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="7a407-132">ويجب أن يتم تكوين ارتباط "كن عضوًا" لإعادة التوجيه إلى صفحة يُمكن للمستخدمين الانضمام إلى برنامج الولاء من خلالها.</span><span class="sxs-lookup"><span data-stu-id="7a407-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="7a407-133">صفحة سجل الأمر</span><span class="sxs-lookup"><span data-stu-id="7a407-133">Order history page</span></span>

<span data-ttu-id="7a407-134">تستخدم صفحة سجل الأمر الوحدة النمطية لسجل الأمر لعرض كافة الأوامر الحديثة التي قام المستخدم بوضعها.</span><span class="sxs-lookup"><span data-stu-id="7a407-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="7a407-135">صفحة تفاصيل الأمر</span><span class="sxs-lookup"><span data-stu-id="7a407-135">Order details page</span></span>

<span data-ttu-id="7a407-136">توفر صفحة تفاصيل الأمر معلومات مفصلة لكل أمر ويتم الوصول إليها من صفحة سجل الأمر.</span><span class="sxs-lookup"><span data-stu-id="7a407-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="7a407-137">وهي تستخدم الوحدة النمطية لتفاصيل الأمر، والتي تتطلب وجود مُعرف المبيعات أو مُعرف الحركة لاسترداد تفاصيل الأمر.</span><span class="sxs-lookup"><span data-stu-id="7a407-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="7a407-138">صفحة ملف تعريف المستخدم</span><span class="sxs-lookup"><span data-stu-id="7a407-138">User profile page</span></span>

<span data-ttu-id="7a407-139">تعرض صفحة ملف تعريف المستخدم تفاصيل حساب المستخدم، مثل اسم المستخدم وعنوان البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="7a407-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="7a407-140">فهو يستخدم الوحدة النمطية لملف تعريف المستخدم.</span><span class="sxs-lookup"><span data-stu-id="7a407-140">It uses the user profile module.</span></span> <span data-ttu-id="7a407-141">على الرغم من عدم إمكانية إزالة عنوان البريد الإلكتروني، إلا أنه يُمكن تحريره.</span><span class="sxs-lookup"><span data-stu-id="7a407-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="7a407-142">تظهر صفحة ملف تعريف المستخدم أيضًا تفضيلات المستخدم التي تُمكن المستخدم من الاختيار أو التعطيل من ميزات معينة مثل تخصيص قوائم التوصيات.</span><span class="sxs-lookup"><span data-stu-id="7a407-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="7a407-143">صفحة عنوان المستخدم</span><span class="sxs-lookup"><span data-stu-id="7a407-143">User address page</span></span>

<span data-ttu-id="7a407-144">تعرض صفحة عنوان المستخدم قائمة العناوين المقترنة بحساب المستخدم.</span><span class="sxs-lookup"><span data-stu-id="7a407-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="7a407-145">قام المستخدم إما بتوفير هذه العناوين في أثناء السداد مع الخروج أو تمت إضافتهم مباشرة في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7a407-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="7a407-146">يتم استخدام الوحدة النمطية لعنوان المستخدم لإضافة العناوين وتحريرها وتعيين العنوان الرئيسي وعرض العناوين الموجودة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7a407-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="7a407-147">صفحة قائمة الأمنيات</span><span class="sxs-lookup"><span data-stu-id="7a407-147">Wish list page</span></span>

<span data-ttu-id="7a407-148">تعرض صفحة قائمة الأمنيات الأصناف التي تمت إضافتها إلى قائمة أمنيات العميل.</span><span class="sxs-lookup"><span data-stu-id="7a407-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="7a407-149">وهي تستخدم الوحدة النمطية للأمنيات لعرض أصناف الأمنيات.</span><span class="sxs-lookup"><span data-stu-id="7a407-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="7a407-150">صفحه الولاء</span><span class="sxs-lookup"><span data-stu-id="7a407-150">Loyalty page</span></span>

<span data-ttu-id="7a407-151">تُتيح صفحة الولاد للعملاء الانضمام إلى برنامج الولاء أو، إذا كانوا أعضاء في برنامج الولاء بالفعل، عرض تفاصيل البرنامج الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="7a407-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="7a407-152">ويُمكنهم أيضًا عرض النقاط التي اكتسبوها واستردادها في الحركات الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="7a407-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a407-153">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7a407-153">Additional resources</span></span>

[<span data-ttu-id="7a407-154">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="7a407-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7a407-155">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="7a407-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7a407-156">الوحدة النمطية لمربع شراء</span><span class="sxs-lookup"><span data-stu-id="7a407-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7a407-157">الوحدة النمطية لسلة التسوق</span><span class="sxs-lookup"><span data-stu-id="7a407-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7a407-158">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="7a407-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7a407-159">وحدة تأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="7a407-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7a407-160">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="7a407-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7a407-161">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="7a407-161">Footer module</span></span>](author-footer-module.md)
