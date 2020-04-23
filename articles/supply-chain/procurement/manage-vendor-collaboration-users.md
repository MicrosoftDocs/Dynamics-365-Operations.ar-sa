---
title: إدارة مستخدمي تعاون المورد‬
description: يصف هذا الموضوع كيف يمكنك طلب توفير مستخدمين جدد لتعاون الموردين، وكيفية إضافة جهات اتصال جديدة لتعاون الموردين.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8491fd7c5af015989d409391e3ac143d88b6ad92
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207153"
---
# <a name="manage-vendor-collaboration-users"></a><span data-ttu-id="9ceaa-103">إدارة مستخدمي تعاون المورد‬</span><span class="sxs-lookup"><span data-stu-id="9ceaa-103">Manage vendor collaboration users</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ceaa-104">يصف هذا الموضوع كيف يمكنك طلب توفير مستخدمين جدد لتعاون الموردين، وكيفية إضافة جهات اتصال جديدة لتعاون الموردين.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-104">This topic describes how you can request the provisioning of new vendor collaboration users, and how to add new vendor collaboration contacts.</span></span> 

<span data-ttu-id="9ceaa-105">تعرض واجهة تعاون المورّد في Dynamics 365 Supply Chain Management معلومات حول أوامر الشراء والفواتير وشحن الإدارة المصروفات‬ لمورّدين خارجيين.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-105">The vendor collaboration interface in Dynamics 365 Supply Chain Management exposes information about purchase orders, invoices, and consignment stock to external vendors.</span></span> <span data-ttu-id="9ceaa-106">يمكنك إنشاء جهات اتصال جديدة لتعاون المورد وطلب توفير مستخدمين جدد إذا كنت تعمل كمورد خارجي لديه دور الأمان **مسؤول المورد (خارجي)** أو أذونات مماثلة.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-106">You can create new vendor collaboration contacts and request that new users are provisioned if you're working as an external vendor with the **Vendor admin (external)** security role, or similar permissions.</span></span> <span data-ttu-id="9ceaa-107">ويمكنك أيضًا تنفيذ هذه المهام إذا كنت تعمل كأحد أخصائيي التدبير‬.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-107">You can also perform these tasks if you're working as a procurement professional.</span></span> <span data-ttu-id="9ceaa-108">في هذا الموضوع، يشير هذا الدور إلى أخصائي التدبير‬ الذين يعمل داخل الشركة التي تملك مثيل Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-108">In this topic, this role refers to a procurement professional who is working within the company that owns the instance of Supply Chain Management.</span></span> <span data-ttu-id="9ceaa-109">‏‫لمزيد من المعلومات حول كيفية استخدام تعاون المورد إذا كنت موردًا خارجيًا، راجع [تعاون الموردين مع العملاء](vendor-collaboration-work-customers-dynamics-365-operations.md).</span><span class="sxs-lookup"><span data-stu-id="9ceaa-109">For more information about how to use vendor collaboration if you're an external vendor, see [Vendor collaboration with customers](vendor-collaboration-work-customers-dynamics-365-operations.md).</span></span>  

<span data-ttu-id="9ceaa-110">لمزيد من المعلومات حول كيفية استخدام تعاون المورد إذا كنت أخصائي تدبير، راجع [‬‏‫تعاون الموردين مع الموردين الخارجيين‬‏‫](vendor-collaboration-work-external-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="9ceaa-110">For more information about how to use vendor collaboration if you're a procurement professional, see [Vendor collaboration with external vendors](vendor-collaboration-work-external-vendors.md).</span></span>

## <a name="add-new-vendor-collaboration-contacts"></a><span data-ttu-id="9ceaa-111">إضافة جهات اتصال جديدة لتعاون المورد</span><span class="sxs-lookup"><span data-stu-id="9ceaa-111">Add new vendor collaboration contacts</span></span>
<span data-ttu-id="9ceaa-112">إذا كنت تريد منح حق الوصول إلى تعاون المورد، فيجب إضافته أولاً إضافته كجهة اتصال لتعاون المورد.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-112">If you want someone to have access to vendor collaboration they first have to be added as a vendor collaboration contact.</span></span> <span data-ttu-id="9ceaa-113">قد تحتاج أيضًا إلى إضافة جهات اتصال للموظفين الموجودين في الشركة الذين لن يستخدموا تعاون المورد.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-113">You may also want to add contacts for employees in your company who won't use vendor collaboration.</span></span> <span data-ttu-id="9ceaa-114">على سبيل المثال، قد يكون هؤلاء نقطة اتصال لأنواع أخرى من المعلومات المتعلقة بالتدبير.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-114">For example, they could be the point of contact for other kinds of procurement information.</span></span> <span data-ttu-id="9ceaa-115">تتم إضافة جهات الاتصال الجديدة على صفحة **‎كافة جهات الاتصال**، والتي يتم الوصول إليها من **تعاون المورد** &gt; قائمة **جهات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-115">New contacts are added on the **All contacts** page, which is accessed from the **Vendor collaboration** &gt; **Contacts** menu.</span></span> <span data-ttu-id="9ceaa-116">لإضافة جهة اتصال جديدة</span><span class="sxs-lookup"><span data-stu-id="9ceaa-116">To add a new contact:</span></span>

1.  <span data-ttu-id="9ceaa-117">انقر فوق **جديد.**</span><span class="sxs-lookup"><span data-stu-id="9ceaa-117">Click **New.**</span></span>
2.  <span data-ttu-id="9ceaa-118">أدخل تفاصيل الشخص الذي تعتبره جهة اتصال.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-118">Enter the contact person details.</span></span>
3.  <span data-ttu-id="9ceaa-119">اختر الكيان القانوني الذي يمثله هذا الشخص في شركتك، والكيان القانوني الذي سيعمل معه في الشركة التي سوف يتعاون معها.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-119">Choose which legal entity they're representing in your company, and which legal entity they'll work with in the company that they'll collaborate with.</span></span> <span data-ttu-id="9ceaa-120">يمكنك القيام بذلك عن طريق تحديد الزوج **الكيان القانوني في شركتي**/**الكيان القانوني في شركة العميل‎‏**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-120">You do this by selecting a **Legal entity in my company**/**Legal entity in customer company** pair.</span></span>
4.  <span data-ttu-id="9ceaa-121">انقر فوق **إنشاء.**</span><span class="sxs-lookup"><span data-stu-id="9ceaa-121">Click **Create.**</span></span>

<span data-ttu-id="9ceaa-122">إذا أردت حذف جهة اتصال، فمن الممكن فقط حذف تلك التي قمت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-122">If you want to delete a contact, it's only possible to delete the ones that you've created.</span></span>

## <a name="vendor-collaboration-user-requests"></a><span data-ttu-id="9ceaa-123">طلبات مستخدم تعاون المورد</span><span class="sxs-lookup"><span data-stu-id="9ceaa-123">Vendor collaboration user requests</span></span>
<span data-ttu-id="9ceaa-124">يمكن رفع طلبات مستخدم تعاون المورد من قِبل أخصائي تدبير أو مسؤول مورد خارجي.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-124">Vendor collaboration user requests can be raised by a procurement professional, or by an external vendor administrator.</span></span>

-   <span data-ttu-id="9ceaa-125">إذا كنت موردًا خارجيًا، فيمكنك إرسال الطلبات من صفحة **كافة جهات الاتصال** ضمن الوحدة النمطية **تعاون المورد**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-125">If you're an external vendor, you submit requests from the **All contacts** page within the **Vendor collaboration** module.</span></span>
-   <span data-ttu-id="9ceaa-126">إذا كنت أخصائي تدبير، فيمكنك إرسال الطلبات من صفحة **عرض جهات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-126">If you're a procurement professional, you submit requests from the **View contacts** page.</span></span> <span data-ttu-id="9ceaa-127">لإجراء ذلك، في سجل المورد، في مقطع **الإعداد‏‎** في جزء الإجراءات، حدد **جهات الاتصال** &gt; **عرض جهات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-127">To do this, on the vendor record, in the **Setup** section in the Action pane, select **Contacts** &gt; **View contacts**.</span></span>

<span data-ttu-id="9ceaa-128">يمكنك تقديم طلب توفير مستخدم أو إلغاء تنشيط مستخدم أو تعديل أدوار الأمان.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-128">You can make a request to provision a user, to inactivate a user, or to modify security roles.</span></span> <span data-ttu-id="9ceaa-129">إذا كنت مسؤول مورد خارجي، فيجب أن تكون مسجلاً كشخص يعتبر جهة اتصال لحسابات المورد التي تريد تقديم طلبات مستخدم لها، ويجب أن يتوفر لديك حق الوصول إلى واجهة تعاون المورد لحسابات المورد هذه.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-129">If you're an external vendor administrator, you must be registered as a contact person for the vendor accounts that you want to make user requests for, and you must have access to the vendor collaboration interface for those vendor accounts.</span></span>  

<span data-ttu-id="9ceaa-130">يُضاف الطلب عند إرساله إلى قائمة **طلبات مستخدم تعاون المورد‬** في الوحدة النمطية **تعاون المورد**، وإلى قائمة **طلب مستخدم تعاون المورد‬** في الوحدة النمطية **التدبير وتحديد الموارد** (يتعذر على المستخدمين الخارجيين الوصول إلى الوحدة النمطية "التدبير وتحديد الموارد").</span><span class="sxs-lookup"><span data-stu-id="9ceaa-130">When a request is submitted it is added to the **Vendor collaboration user requests** list in the **Vendor collaboration** module, and to the **Vendor collaboration user request** list in the **Procurement and sourcing** module (the Procurement and sourcing module is not accessible to external users).</span></span>

### <a name="provision-a-user"></a><span data-ttu-id="9ceaa-131">توفير مستخدم</span><span class="sxs-lookup"><span data-stu-id="9ceaa-131">Provision a user</span></span>

<span data-ttu-id="9ceaa-132">قبل أن تتمكن من طلب توفير مستخدم جديد، يجب إعداد ذلك الشخص كجهة اتصال لحساب مورد واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-132">Before you can request that a new user is provisioned, that person must be set up as a contact for one or more vendor accounts.</span></span> <span data-ttu-id="9ceaa-133">لإنشاء طلب لمستخدم تعاون مورد جديد:</span><span class="sxs-lookup"><span data-stu-id="9ceaa-133">To create a request for a new vendor collaboration user:</span></span>

1. <span data-ttu-id="9ceaa-134">في صفحة **كافة جهات الاتصال**، انقر فوق **توفير مستخدم مورد**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-134">On the **All contacts** page, click **Provision vendor user**.</span></span>
2. <span data-ttu-id="9ceaa-135">أدخل عنوان بريد إلكتروني للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-135">Enter an email address for the user.</span></span> <span data-ttu-id="9ceaa-136">سوف يُستخدم هذا النواع بواسطة المستخدم لتسجيل الدخول إلى Supply Chain Management. </span><span class="sxs-lookup"><span data-stu-id="9ceaa-136">This address will be used by the user to sign in to Supply Chain Management.</span></span> <span data-ttu-id="9ceaa-137">إذا كان عنوان البريد الإلكتروني ينتمي إلى مجال مسجل كمستأجر مع Microsoft Azure, فيجب أن يكون عنوان البريد الإلكتروني هذا حسابًا موجودًا في Azure Active Directory (AAD) لكي تكتمل عملية التوفير بنجاح.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-137">If the email address belongs to a domain registered as a tenant with Microsoft Azure, then the email address has to be an existing Azure Active Directory (AAD) account in order for the provisioning process to complete successfully.</span></span> <span data-ttu-id="9ceaa-138">أما في حال عدم انتماء عنوان البريد الإلكتروني إلى مجال مسجّل مع Microsoft Azure، فسيتم إنشاء حساب AAD كجزء من عملية التوفير وسيتلقى المستخدم الجديد دعوة بالبريد.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-138">If the email address does not belong to a domain registered with Microsoft Azure, an AAD account will be created as part of the provisioning process and the new user will receive an invitation mail.</span></span> <span data-ttu-id="9ceaa-139">لا يمكن استخدام عناوين البريد الإلكتروني للمستهلك التي تتضمن مجالات مثل @hotmail.com‏ أو ‎@gmail.com أو ‎@comcast.net لتسجيل مستخدم.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-139">Consumer email addresses with domains such as @hotmail.com, @gmail.com, or @comcast.net cannot be used to register a  user.</span></span>
3. <span data-ttu-id="9ceaa-140">عيّن الخيار **السماح بالوصول إلى تعاون المورد‬‬** إلى **نعم** لجميع الكيانات القانونية التي يحتاج المستخدم للوصول إلى.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-140">Set the **Vendor collaboration access allowed** option to **Yes** for all the legal entities that the user needs access to.</span></span>
4. <span data-ttu-id="9ceaa-141">في المقطع **تعيين أدوار المستخدم**، حدد خانة الاختيار **بتعيين** لأدوار الأمان التي يجب أن تكون لدى المستخدم الجديد.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-141">In the **Assign user roles** section, select the **Assign** check box for the security roles that the new user should have.</span></span>
5. <span data-ttu-id="9ceaa-142">انقر فوق **تقديم**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-142">Click **Submit**.</span></span>

<span data-ttu-id="9ceaa-143">عند إرسال طلب مستخدم مورد، يتم تعيين الحقل **السماح بالوصول إلى تعاون المورد** إلى **نعم** لحساب المورد المحدد ويبدأ تشغيل سير عمل طلب المستخدم.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-143">When the vendor user request is submitted, the **Vendor collaboration access allowed** field is set to **Yes** for the selected vendor account and a user request workflow is started.</span></span> <span data-ttu-id="9ceaa-144">كجزء من سير العمل، يتم إنشاء مستخدم جديد، ويتم تعيين أدوار الأمان.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-144">As part of the workflow, a new user is created, and security roles are assigned.</span></span> <span data-ttu-id="9ceaa-145">علاوةً على ذلك، يتم تنشيط خدمة Azure B2B التي تبدأ التفاعل مع مدخل Azure وتقوم بإقران حساب AAD جديد أو موجود بحساب مستخدم Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-145">In addition, an Azure B2B service is activated which initiates interaction with Azure portal and associates a new or existing AAD account with the Supply Chain Management user account.</span></span> <span data-ttu-id="9ceaa-146">للحصول على مزيد من المعلومات، راجع [ما هو تعاون Azure AD B2B?](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).</span><span class="sxs-lookup"><span data-stu-id="9ceaa-146">For more information, see [What is Azure AD B2B collaboration?](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).</span></span>

### <a name="inactivate-a-user"></a><span data-ttu-id="9ceaa-147">إلغاء تنشيط مستخدم</span><span class="sxs-lookup"><span data-stu-id="9ceaa-147">Inactivate a user</span></span>

<span data-ttu-id="9ceaa-148">هناك طريقتان لإزالة الوصول إلى تعاون المورد لمستخدم:</span><span class="sxs-lookup"><span data-stu-id="9ceaa-148">There are two ways to remove access to vendor collaboration for a user:</span></span>

-   <span data-ttu-id="9ceaa-149">في صفحة **جهات الاتصال** للمورد، قم بتعيين الخيار **السماح بالوصول إلى تعاون المورد** إلى **لا** لجهة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-149">On the **Contacts** page for the vendor, set the **Vendor collaboration access allowed** option to **No** for the contact.</span></span> <span data-ttu-id="9ceaa-150">يمكن إجراء ذلك بشكل فردي لكل كيان قانوني يكون الشخص جهة اتصال له.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-150">This can be done individually per legal entity that the person is a contact for.</span></span> <span data-ttu-id="9ceaa-151">يمكن استخدام هذا الخيار فقط من قِبل أخصائي التدبير.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-151">This option can only be used by procurement professionals.</span></span>
-   <span data-ttu-id="9ceaa-152">قم إلغاء تنشيط حساب المستخدم بالكامل، عن طريق إرسال طلب **إلغاء تنشيط مستخدم مورّد‬**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-152">Inactivate the entire user account, by submitting an **Inactivate vendor user** request.</span></span>

<span data-ttu-id="9ceaa-153">لطلب إلغاء تنشيط مستخدم:</span><span class="sxs-lookup"><span data-stu-id="9ceaa-153">To request that a user is inactivated:</span></span>

1.  <span data-ttu-id="9ceaa-154">في صفحة **كافة جهات الاتصال**، انقر فوق **‎إلغاء تنشيط** **مستخدم مورّد**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-154">On the **All contacts** page, click **Inactivate** **vendor user**.</span></span>
2.  <span data-ttu-id="9ceaa-155">اكتب تعليقًا في الحقل **مبررات الأعمال**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-155">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="9ceaa-156">انقر فوق **تقديم**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-156">Click **Submit**.</span></span>

### <a name="modify-security-roles"></a><span data-ttu-id="9ceaa-157">تعديل أدوار الأمان</span><span class="sxs-lookup"><span data-stu-id="9ceaa-157">Modify security roles</span></span>

<span data-ttu-id="9ceaa-158">تعد صفحة **الاحتفاظ بأدوار المستخدمين المورّدين** هي نفسها الصفحة **توفير مستخدم مورد** باستثناء أنه يمكن تحرير قائمة أدوار الأمان.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-158">The **Maintain vendor user roles** page is the same as the **Provision vendor user** page except that the list of security roles can be edited.</span></span>  

<span data-ttu-id="9ceaa-159">لطلب تعديل أدوار الأمان لمستخدم:</span><span class="sxs-lookup"><span data-stu-id="9ceaa-159">To request that the security roles are modified for a user:</span></span>

1.  <span data-ttu-id="9ceaa-160">في صفحة **كافة جهات الاتصال**، انقر فوق **الاحتفاظ** **بأدوار المستخدمين المورّدين**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-160">On the **All contacts** page, click **Maintain** **vendor user roles**.</span></span>
2.  <span data-ttu-id="9ceaa-161">اكتب تعليقًا في الحقل **مبررات الأعمال**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-161">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="9ceaa-162">في المقطع **الاحتفاظ بأدوار المستخدمين**، حدد أدوار الأمان التي تريد تعيينها أو قم بإلغاء تحديد تلك التي تريد إزالتها.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-162">In the **Maintain user roles** section, select the security roles that you want to assign, or clear the ones that you want to remove.</span></span>
4.  <span data-ttu-id="9ceaa-163">انقر فوق **تقديم‏‎**.</span><span class="sxs-lookup"><span data-stu-id="9ceaa-163">Click **Submit**.</span></span>




