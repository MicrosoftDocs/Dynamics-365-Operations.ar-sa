---
title: إعداد مساحة العمل المحمولة للأصل
description: يوضح هذا الموضوع كيفيه اعداد Microsoft Dynamics 365 Supply Chain ManagementFinance and Operations وتطبيق الاجهزه المحمولة (Dynamics 365) لتشغيل مساحة عمل متنقلة لأداره الأصول يمكن للعاملين استخدامها لأداء مهام أداره الأصول.
author: johanhoffmann
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 54da27a022dcc800438b96224370228aa8eed261
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226137"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="10283-103">إعداد مساحة العمل المحمولة للأصل</span><span class="sxs-lookup"><span data-stu-id="10283-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10283-104">يوضح هذا الموضوع كيفيه اعداد Microsoft Dynamics 365 Supply Chain Management وتطبيق الاجهزه المحمولة Finance and Operations (Dynamics 365) لتشغيل مساحة عمل متنقلة **لأداره الأصول** يمكن للعاملين استخدامها لأداء مهام أداره الأصول.</span><span class="sxs-lookup"><span data-stu-id="10283-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="10283-105">اعداد مستخدمي عامل الصيانة في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="10283-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="10283-106">بالنسبة لكل مستخدم يتطلب الوصول إلى مساحة عمل الاجهزه المحمولة **لأداره الأصول**، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="10283-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="10283-107">في Supply Chain Management، انتقل إلى عمال العمل في **الموارد البشرية\>العمال**، وتاكد من وجود سجل عامل للمستخدم الذي ترغب في اعداده.</span><span class="sxs-lookup"><span data-stu-id="10283-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="10283-108">قم بإنشاء سجل جديد بالشكل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="10283-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="10283-109">انتقل إلى **أداره الأصول \> اعداد \> العاملون \> العاملون**، وتاكد من تعيين سجل العامل الذي قمت بتحديده (أو إنشاؤه) في الخطوة السابقة إلى سجل عامل صيانة.</span><span class="sxs-lookup"><span data-stu-id="10283-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="10283-110">قم بإنشاء سجل عامل صيانة جديد حسب الحاجة، وقم بتعيين الحقل **العامل** إلى السجل العامل من الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="10283-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="10283-111">انتقل إلى **أداره الأصول \> اعداد \> العاملون \> صيانة مجموعات العاملين**، وتاكد من تعيين سجل العامل الذي قمت بتحديده (أو إنشاؤه) في الخطوة السابقة إلى سجل عامل صيانة.</span><span class="sxs-lookup"><span data-stu-id="10283-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="10283-112">انتقل إلى **إدارة النظام \> المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="10283-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="10283-113">حدد المستخدم ذا صلة في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="10283-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="10283-114">في علامة التبويب السريعة **تفاصيل المستخدم**، قم بتعيين حقل **الشخص** إلى حساب العامل الذي ترغب في ربطه بحساب المستخدم الحالي.</span><span class="sxs-lookup"><span data-stu-id="10283-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="10283-115">يجب ان يكون حساب العامل هذا هو سجل العامل الذي قمت بتحديده (أو تم إنشاؤه) في الخطوة 1 ويتم تعيينه إلى سجل عامل صيانة في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="10283-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="10283-116">تنطبق أذونات المستخدمين وأدوار الأمان علي ميزات مساحة عمل الاجهزه المحمولة **لأداره الأصول** كما يتم تطبيقها علي ميزات واجهه مستخدم Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="10283-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="10283-117">التالي، يجب ان يكون لكل مستخدم تقوم باعداده للوصول إلى مساحة عمل الشركة المتنقلة **لأداره الأصول**، ادوار الأمان المطلوبة لتنفيذ العمليات المتشابهة مباشره في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="10283-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="10283-118">نشر مساحة العمل المحمولة للأصل</span><span class="sxs-lookup"><span data-stu-id="10283-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="10283-119">لجعل ميزات أداره الأصول Finance and Operations متاحه في تطبيق الاجهزه المحمولة (Dynamics 365)، يجب ان تقوم بنشر مساحة عمل الاجهزه المحمولة **لأداره الأصول**.</span><span class="sxs-lookup"><span data-stu-id="10283-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="10283-120">في Supply Chain Management، حدد زر **الإعدادات** (رمز الترس في الزاوية العليا اليسرى)، ثم حدد **تطبيق** الاجهزه المحمولة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="10283-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="10283-121">في مربع الحوار **أداره تطبيق الاجهزه المحمولة**، ابحث عن تجانب **أداره الأصول**.</span><span class="sxs-lookup"><span data-stu-id="10283-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="10283-122">إذا كان يحتوي علي النص "في بيانات التعريف-لم يتم نشره ، فلم يتم نشر مساحة العمل بعد.</span><span class="sxs-lookup"><span data-stu-id="10283-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="10283-123">إذا كان يحتوي علي النص "في نشر بيانات التعريف"، "مساحة العمل" التي تم نشرها بالفعل ويمكنك تخطي المتبقي من هذا الاجراء.</span><span class="sxs-lookup"><span data-stu-id="10283-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="10283-124">![مربع حوار أداره تطبيق الاجهزه المحمولة](media/mobile-workspaces.png "مربع حوار أداره تطبيق الاجهزه المحمولة")</span><span class="sxs-lookup"><span data-stu-id="10283-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="10283-125">حدد تجانب **أداره الأصول**، ثم حدد **النشر** في شريط الادوات.</span><span class="sxs-lookup"><span data-stu-id="10283-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="10283-126">بعد بضع ثوان، يجب ان تتلقي اعلاما يوضح انه قد تم نشر مساحة العمل بنجاح.</span><span class="sxs-lookup"><span data-stu-id="10283-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="10283-127">بالاضافه إلى ذلك، يجب ان يتغير النص الموجود في التجانب إلى "في نشر بيانات التعريف".</span><span class="sxs-lookup"><span data-stu-id="10283-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="10283-128">تثبيت Finance and Operations تطبيق الاجهزه المحمولة (Dynamics 365) واعداده</span><span class="sxs-lookup"><span data-stu-id="10283-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="10283-129">انتقل إلى أحد مخازن التطبيقات التالية لتثبيت **Finance and Operations تطبيق Microsoft (Dynamics 365)** علي جهازك المحمول:</span><span class="sxs-lookup"><span data-stu-id="10283-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="10283-130">لأجهزه Google Android</span><span class="sxs-lookup"><span data-stu-id="10283-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="10283-131">بالنسبة لأجهزه Apple iOS</span><span class="sxs-lookup"><span data-stu-id="10283-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="10283-132">افتح Finance and Operations تطبيق (Dynamics 365).</span><span class="sxs-lookup"><span data-stu-id="10283-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="10283-133">يجب ان تظهر صفحه تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="10283-133">The sign-in page should appear.</span></span> <span data-ttu-id="10283-134">في الحقل **تسجيل الدخول**، ادخل عنوان Url لـ Supply Chain Management، أو حدد عنوان url حديثا في القائمة **البيئات الاخيره**، ثم انقر فوق **الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="10283-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="10283-135">![صفحة تسجيل الدخول](media/mobile-app-sign-in.png "صفحة تسجيل الدخول")</span><span class="sxs-lookup"><span data-stu-id="10283-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="10283-136">إذا تمت مطالبتك بتاكيد الاتصال، حدد خانه الاختيار **أفهم**، ثم اضغط علي **اتصال**.</span><span class="sxs-lookup"><span data-stu-id="10283-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="10283-137">في الصفحة **اختر حسابا**، استخدم حساب Microsoft الخاص بك لتسجيل الدخول إلى تطبيق الاجهزه المحمولة.</span><span class="sxs-lookup"><span data-stu-id="10283-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="10283-138">تظهر الصفحة **مساحات العمل‬**.</span><span class="sxs-lookup"><span data-stu-id="10283-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="10283-139">وهو يسرد كل مساحة عمل متنقلة تم نشرها بواسطة مثيل Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="10283-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="10283-140">![قائمه بمساحات العمل](media/mobile-app-workspaces.png "قائمه بمساحات العمل")</span><span class="sxs-lookup"><span data-stu-id="10283-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="10283-141">إذا كان من الضروري تغيير الكيان القانوني (الشركة)، انقر فوق زر القائمة (الذي يشار اليه أحيانا بالهامبورجير أو الزر هامبورجير) في الزاوية العلوية اليسرى، ثم انقر فوق **تغيير الشركة**.</span><span class="sxs-lookup"><span data-stu-id="10283-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="10283-142">![تغيير الكيان القانوني.](media/mobile-app-change-comp.png "تغيير الكيان القانوني.")</span><span class="sxs-lookup"><span data-stu-id="10283-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="10283-143">في الصفحة **مساحات العمل**، حدد مساحة العمل التي ترغب في استخدامها لفتحها.</span><span class="sxs-lookup"><span data-stu-id="10283-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="10283-144">![مساحة العمل المحمولة للأصل](media/mobile-app-asset-workspace.png "مساحة العمل المحمولة للأصل")</span><span class="sxs-lookup"><span data-stu-id="10283-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="10283-145">استخدام مساحة العمل المحمولة للأصل</span><span class="sxs-lookup"><span data-stu-id="10283-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="10283-146">لمزيد من المعلومات حول كيفيه العمل مع مساحة عمل الاجهزه المحمولة **لأداره الأصول**، راجع [استخدام مساحة عمل الاجهزه المحمولة لأداره الأصول](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="10283-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="10283-147">لمزيد من المعلومات حول Finance and Operations تطبيق الاجهزه المحمولة (Dynamics 365)، راجع [الصفحة الرئيسية لتطبيق الاجهزه المحمولة](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="10283-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]