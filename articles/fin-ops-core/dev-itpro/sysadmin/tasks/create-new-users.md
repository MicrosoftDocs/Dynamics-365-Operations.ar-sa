---
title: إنشاء مستخدمين جدد
description: المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b994473b4535c255f87551a6d97e197516fc2a9c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745827"
---
# <a name="create-new-users"></a><span data-ttu-id="e0274-103">إنشاء مستخدمين جدد</span><span class="sxs-lookup"><span data-stu-id="e0274-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0274-104">قبل ان تتمكن من الوصول إلى Finance and Operations التطبيقات، يجب ان تتم اضافتك أولا إلى صفحه **المستخدمون** (**أداره النظام \> المستخدمون \> المستخدمون**).</span><span class="sxs-lookup"><span data-stu-id="e0274-104">Before you can access Finance and Operations apps, you must first be added to the **Users** page (**System administration \> Users \> Users**).</span></span> <span data-ttu-id="e0274-105">ويتضمن المستخدمون موظفين داخليين بمؤسسك، أو العملاء الخارجيين والموردون.</span><span class="sxs-lookup"><span data-stu-id="e0274-105">Users include internal employees of your organization, or external customers and vendors.</span></span> <span data-ttu-id="e0274-106">يمكن استيراد المستخدمين أو اضافتهم يدويا.</span><span class="sxs-lookup"><span data-stu-id="e0274-106">Users can be imported or added manually.</span></span> <span data-ttu-id="e0274-107">يجب ان يتم ترخيص كافة المستخدمين بشكل صحيح للاستخدام المتوافق.</span><span class="sxs-lookup"><span data-stu-id="e0274-107">All users must be correctly licensed for compliant use.</span></span>

<span data-ttu-id="e0274-108">للحصول علي معلومات حول كيفيه شراء Finance and Operationsالتطبيقات وترخيصها ، راجع [Microsoft Dynamics 365 دليل الترخيص](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="e0274-108">For information about how to buy and license for Finance and Operations apps, see [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span></span>

## <a name="assign-a-license-to-a-user"></a><span data-ttu-id="e0274-109">تعيين ترخيص إلى معرّف مستخدم</span><span class="sxs-lookup"><span data-stu-id="e0274-109">Assign a license to a user</span></span>
<span data-ttu-id="e0274-110">بإمكان مسؤولي النظام [تعيين تراخيص إلى المستخدمين](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) في [مركز إدارة Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="e0274-110">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a><span data-ttu-id="e0274-111">أضافه مستخدم خارجي في Azure AD وتعيين ترخيص</span><span class="sxs-lookup"><span data-stu-id="e0274-111">Add an external user in Azure AD and assign a license</span></span> 
<span data-ttu-id="e0274-112">يجب ان يتم تمثيل المستخدمين الخارجيين في دليل المستاجر الخاص بك ( Azure Active Directory ( Azure AD)) بحيث يمكن تعيين تراخيص لهم.</span><span class="sxs-lookup"><span data-stu-id="e0274-112">External users must be represented in your tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="e0274-113">يجب إضافة هؤلاء المستخدمين الخارجيين إلى المستأجر في Azure AD كمستخدمين ضيوف ثم تعيين التراخيص المناسبة لهم.</span><span class="sxs-lookup"><span data-stu-id="e0274-113">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="e0274-114">ومتطلبات Finance and Operations التطبيقات هي انه يجب علي شركه المستخدمين الضيف استخدام Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e0274-114">A requirement for Finance and Operations apps is that the guest user's company must use Azure AD.</span></span> <span data-ttu-id="e0274-115">لمزيد من المعلومات، راجع [إضافة مستخدمي تعاون B2B Azure Active Directory في مدخل Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="e0274-115">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="import-new-users-from-azure-ad"></a><span data-ttu-id="e0274-116">استيراد المستخدمين الجدد من Azure AD</span><span class="sxs-lookup"><span data-stu-id="e0274-116">Import new users from Azure AD</span></span> 
1. <span data-ttu-id="e0274-117">انتقل إلى **إدارة النظام** \> **المستخدمون** \> **المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="e0274-117">Go to **System administration** \> **User** \> **Users**.</span></span>
2. <span data-ttu-id="e0274-118">في جزء الإجراءات، حدد **استيراد المستخدمين‬**.</span><span class="sxs-lookup"><span data-stu-id="e0274-118">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="e0274-119">حدد المستخدمين المراد استيرادهم.</span><span class="sxs-lookup"><span data-stu-id="e0274-119">Select the users to be imported.</span></span> <span data-ttu-id="e0274-120">تتضمن القائمة Azure AD المستخدمين الذين لا يقومون حاليا بالمستخدمين في هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="e0274-120">The list includes Azure AD users that are currently not users in this environment.</span></span>
4. <span data-ttu-id="e0274-121">حدد **استيراد المستخدمين‬**.</span><span class="sxs-lookup"><span data-stu-id="e0274-121">Select **Import users**.</span></span>
5. <span data-ttu-id="e0274-122">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="e0274-122">Select **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="e0274-123">سيتم تعيين قيمه حقل **الشركة** استنادا إلى شركه جلسة العمل الحالية للمسؤول. وبعد الاستيراد، يجب تعيين الأدوار والمؤسسات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="e0274-123">The value for the **Company** field will be set based on the current session company for the admin. After import, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="e0274-124">لمزيد من المعلومات، راجع ‏‫[تعيين مستخدمين إلى أدوار أمان‬](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e0274-124">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="e0274-125">وبشكل مشروط، قد يطلب أيضا منك ربط المستخدم مع **شخص** وتحديث خيارات المستخدم مثل اللغة.</span><span class="sxs-lookup"><span data-stu-id="e0274-125">Conditionally, it might also be required to associate the user with a **Person** and to update user options such as language.</span></span>

## <a name="manually-add-a-new-user"></a><span data-ttu-id="e0274-126">إضافة مستخدم جديد يدويًا</span><span class="sxs-lookup"><span data-stu-id="e0274-126">Manually add a new user</span></span>
1. <span data-ttu-id="e0274-127">انتقل إلى **إدارة النظام** \> **المستخدمون‏‎** \> **المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="e0274-127">Go to **System administration** \> **Users** \> **Users**.</span></span>
2. <span data-ttu-id="e0274-128">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e0274-128">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="e0274-129">في الحقل **معرف المستخدم**، أدخل معرفًا فريدًا للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="e0274-129">In the **User ID** field, enter a unique identifier for the user.</span></span>   
4. <span data-ttu-id="e0274-130">في حقل **اسم المستخدم**، أدخل اسم المستخدم‏‎.</span><span class="sxs-lookup"><span data-stu-id="e0274-130">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="e0274-131">في الحقل **الموفر**:</span><span class="sxs-lookup"><span data-stu-id="e0274-131">In the **Provider** field:</span></span>
 - <span data-ttu-id="e0274-132">بالنسبة للمستخدمين الداخليين، استخدم القيمة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="e0274-132">For internal users, use the defaulted value.</span></span> <span data-ttu-id="e0274-133">علي سبيل المثال، Azure AD يبدا المستاجر الذي تقوم باستخدامهhttps://sts.windows.net/.</span><span class="sxs-lookup"><span data-stu-id="e0274-133">For example, your Azure AD tenant prefixed with https://sts.windows.net/.</span></span>  
 - <span data-ttu-id="e0274-134">بالنسبة لغير Azure AD المستخدمين، مثل حسابات الخدمة-2، ادخل قيمه نصيه أساسيه للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="e0274-134">For non-Azure AD users, such as Service-2-Service accounts, enter a basic text value.</span></span> <span data-ttu-id="e0274-135">على سبيل المثال، NA.</span><span class="sxs-lookup"><span data-stu-id="e0274-135">For example, NA.</span></span> <span data-ttu-id="e0274-136">وسوف تساعد هذه القيمة علي تجنب استدعاءات المصادقة غير الصحيحة التي قد تؤدي إلى حدوث أخطاء في حاله استخدام قيمه موفر هويه صالحه.</span><span class="sxs-lookup"><span data-stu-id="e0274-136">This value will help avoid incorrect authentication calls that might result in errors if a valid identity provider value is used.</span></span>  
 - <span data-ttu-id="e0274-137">بالنسبة للمستخدمين الخارجيين أو الضيف، أضف اسم المستاجر الخاص بهم Azure AD بعد https://sts.windows.net/.</span><span class="sxs-lookup"><span data-stu-id="e0274-137">For external or guest users, add their Azure AD tenant name after https://sts.windows.net/.</span></span>
6. <span data-ttu-id="e0274-138">ثم، في حقل **‏‫البريد الإلكتروني**، أدخل عنوان البريد الإلكتروني/اسم المستخدم المسؤول للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="e0274-138">In the **Email** field, enter the user's full Email/User Principle Name.</span></span>  
7. <span data-ttu-id="e0274-139">في الحقل **الشركة**، حدد شركه بدء التشغيل الافتراضية للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="e0274-139">In the **Company** field, select the default startup company for the user.</span></span> 
8. <span data-ttu-id="e0274-140">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e0274-140">Select **Save**.</span></span>

<span data-ttu-id="e0274-141">سيتم تحديث قيم موفر الهوية ومعرف تتبع الاستخدام استنادا إلى [استدعاء Microsoft رسم](https://docs.microsoft.com/graph/overview)، عند حفظ سجل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="e0274-141">The values for Identity provider and Telemetry ID will be updated based on a [Microsoft graph](https://docs.microsoft.com/graph/overview) call, when the user record is saved.</span></span> <span data-ttu-id="e0274-142">ويعتمد معرف تتبع الاستخدام علي معرف كائن المستخدم/معرف الأمان (SID) في Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e0274-142">The Telemetry ID is based on the user's Object ID/Security Identifier (SID) in Azure AD.</span></span>

> [!NOTE]
> <span data-ttu-id="e0274-143">بعد أضافه مستخدم، يجب تعيين الأدوار والمؤسسات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="e0274-143">After you add a user, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="e0274-144">لمزيد من المعلومات، راجع ‏‫[تعيين مستخدمين إلى أدوار أمان‬](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e0274-144">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="e0274-145">وبشكل مشروط، قد يطلب أيضا منك ربط **المستخدم** مع شخص وتحديث **خيارات المستخدم** مثل اللغة.</span><span class="sxs-lookup"><span data-stu-id="e0274-145">Conditionally, it might also be required to associate the user with a **Person** and to update **User options** such as language.</span></span>

## <a name="change-a-user-id"></a><span data-ttu-id="e0274-146">تغيير معرف مستخدم</span><span class="sxs-lookup"><span data-stu-id="e0274-146">Change a user ID</span></span>
<span data-ttu-id="e0274-147">لتغيير معرف مستخدم، يجب أعاده تسميه المفتاح في قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="e0274-147">To change a user ID, you must rename the key in the database.</span></span> <span data-ttu-id="e0274-148">عندما تقوم بتغيير معرف مستخدم باستخدام هذا الاجراء، يتم تعديل كافة إعدادات المستخدم ذات الصلة لاستخدام معرف المستخدم الجديد.</span><span class="sxs-lookup"><span data-stu-id="e0274-148">When you change a user ID by using this procedure, all related user settings are modified to use the new user ID.</span></span> <span data-ttu-id="e0274-149">علي سبيل المثال، يتم تحديث معلومات الاستخدام الموجودة في الجدول **SysLastValue** للاشاره إلى معرف المستخدم الجديد.</span><span class="sxs-lookup"><span data-stu-id="e0274-149">For example, the usage information in the **SysLastValue** table is updated to reference the new user ID.</span></span>

> [!NOTE]
> <span data-ttu-id="e0274-150">معرف المستخدم هو المفتاح الأساسي لجدول معلومات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="e0274-150">The user ID is the primary key of the user information table.</span></span> <span data-ttu-id="e0274-151">قد تتطلب أعاده تسميه المفتاح الأساسي بعض الوقت للمستخدمين الموجودين لأنه يتم أيضا تحديث كافة المراجع إلى المفتاح في قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="e0274-151">Renaming the primary key can take some time for existing users because all references to the key are also updated in the database.</span></span> 

1. <span data-ttu-id="e0274-152">انتقل إلى **إدارة النظام \> المستخدمون‏‎ \> المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="e0274-152">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="e0274-153">حدد مستخدما من القائمة وحدد **الخيارات\>معلومات سجل**.</span><span class="sxs-lookup"><span data-stu-id="e0274-153">Select a user in the list and select **Options\> Record info**.</span></span>
3. <span data-ttu-id="e0274-154">حدد **أعاده التسمية**.</span><span class="sxs-lookup"><span data-stu-id="e0274-154">Select **Rename**.</span></span>
4. <span data-ttu-id="e0274-155">أدخل اسمًا وقيمة فريدة لمعرف المستخدم، ثم حدد **موافق**</span><span class="sxs-lookup"><span data-stu-id="e0274-155">Enter a new and unique value for the User ID, and then select **OK**.</span></span> 
5. <span data-ttu-id="e0274-156">للتأكيد، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e0274-156">Select **Yes** to confirm.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0274-157">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e0274-157">Additional resources</span></span>

<span data-ttu-id="e0274-158">لمزيد من الخيارات لتنفيذ مستخدمي B2B، راجع [تصدير مستخدمي b2b إلى Azure AD](../implement-b2b.md).</span><span class="sxs-lookup"><span data-stu-id="e0274-158">For more options to implement B2B users, see [Export B2B users to Azure AD](../implement-b2b.md).</span></span>

<span data-ttu-id="e0274-159">للحصول علي معلومات حول حسابات النظام المكونة مسبقا، راجع [حسابات النظام المكونة](../pre-configured-system-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="e0274-159">For information about preconfigured system accounts, see [Preconfigured system accounts](../pre-configured-system-accounts.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]