---
title: تمكين مصادقة Azure Active Directory لتسجيل الدخول إلى نقطة البيع
description: يشرح هذا الموضوع كيفية تكوين تجربة تسجيل الدخول إلى نقطة البيع (POS) في Microsoft Dynamics 365 Commerce بحيث تستخدم مصادقة Azure Active Directory.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d6073a04814adf8237b4caa952b31b011f4b34bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982730"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="17670-103">تمكين مصادقة Azure Active Directory لتسجيل الدخول إلى نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="17670-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="17670-104">عدد كبير من العملاء ممن يستخدمون Microsoft Dynamics 365 Commerce يستخدمون أيضًا خدمات سحابية أخرى من Microsoft، وقد يستخدمون Azure Active Directory (Azure AD) لإدارة بيانات اعتماد المستخدم لهذه الخدمات.</span><span class="sxs-lookup"><span data-stu-id="17670-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="17670-105">وفي هذه الحالات، قد يرغب العملاء في استخدام حساب Azure AD نفسه عبر التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="17670-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="17670-106">يشرح هذا الموضوع كيفية تكوين تجربة تسجيل الدخول إلى نقطة البيع (POS) في Commerce لاستخدام مصادقة Azure AD.</span><span class="sxs-lookup"><span data-stu-id="17670-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="17670-107">تكوين مصادقة Azure AD</span><span class="sxs-lookup"><span data-stu-id="17670-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="17670-108">لجعل Azure AD متوفرًا كأسلوب مصادقة لتسجيل الدخول إلى نقطة البيع في متجر ما، يجب تكوين إعدادات ملف تعريف الوظائف الخاصة بالمتجر ثم تطبيق هذه الإعدادات على عملاء نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="17670-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="17670-109">لتكوين ملف تعريف الوظائف، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="17670-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="17670-110">انتقل إلى **Retail and Commerce** \> **إعداد القناة** \> **إعداد نقطة البيع** \> **ملفات تعريف نقاط البيع** \> **ملفات تعريف الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="17670-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="17670-111">حدد ملف تعريف الوظائف لتغييره.</span><span class="sxs-lookup"><span data-stu-id="17670-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="17670-112">على علامة التبويب السريعة **الوظائف**، في القسم **تسجيل دخول الموظفين إلى نقطة البيع**، قم بتغيير قيمة الحقل **أسلوب مصادقة تسجيل الدخول** من **معرف الموظف وكلمة المرور** إلى **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="17670-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="17670-113">بشكل افتراضي، تستخدم جميع ملفات تعريف الوظائف **معرف الموظف وكلمة المرور** كأسلوب مصادقة نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="17670-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="17670-114">وبالتالي، يجب تغيير قيمة حقل **أسلوب مصادقة تسجيل الدخول** إذا أردت استخدام Azure AD.</span><span class="sxs-lookup"><span data-stu-id="17670-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="17670-115">سيتأثر كل متجر للبيع بالتجزئة مرتبط بملف تعريف الوظائف المحددة بهذا التغيير.</span><span class="sxs-lookup"><span data-stu-id="17670-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="17670-116">لتطبيق الإعدادات على عملاء نقطة البيع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="17670-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="17670-117">انتقل إلى **Retail and Commerce** \> **تكنولوجيا معلومات البيع بالتجزئة والتجارة** \> **جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="17670-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="17670-118">شغّل جدول توزيع **1070** (**تكوين قناة**).</span><span class="sxs-lookup"><span data-stu-id="17670-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="17670-119">تتطلب مصادقة Azure AD اتصال إنترنت.</span><span class="sxs-lookup"><span data-stu-id="17670-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="17670-120">ولن تعمل عندما تكون نقطة البيع في وضع عدم الاتصال.</span><span class="sxs-lookup"><span data-stu-id="17670-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="17670-121">في الوقت الحالي، لا تدعم وظيفة **تجاوز المدير** لا تدعم Azure AD كأسلوب مصادقة.</span><span class="sxs-lookup"><span data-stu-id="17670-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="17670-122">يلزم وجود معرف عامل التشغيل وكلمة المرور حتى لو تم تكوين Azure AD كأسلوب مصادقة لتسجيل الدخول إلى نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="17670-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="17670-123">ربط حساب Azure AD بعامل</span><span class="sxs-lookup"><span data-stu-id="17670-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="17670-124">قبل أن يتمكن عامل المتجر من استخدم حساب Azure AD لتسجيل الدخول إلى تطبيق نقطة البيع، يجب ربط حساب Azure AD بهذا العامل.</span><span class="sxs-lookup"><span data-stu-id="17670-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="17670-125">لربط حساب Azure AD بعامل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="17670-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="17670-126">انتقل إلى **البيع بالتجزئة والتجار** \> **الموظفون** \> **العاملون**.</span><span class="sxs-lookup"><span data-stu-id="17670-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="17670-127">افتح صفحة تفاصيل العامل.</span><span class="sxs-lookup"><span data-stu-id="17670-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="17670-128">في جزء الإجراءات، في علامة تبويب **Commerce**، في مجموعة **الهوية الخارجية**، حدد **إقران هوية موجودة**.</span><span class="sxs-lookup"><span data-stu-id="17670-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="17670-129">في مربع الحوار **استخدام هوية خارجية موجودة**، حدد **البحث باستخدام البريد الإلكتروني**، وأدخل عنوان بريد إلكتروني في Azure AD، ثم حدد **بحث**.</span><span class="sxs-lookup"><span data-stu-id="17670-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="17670-130">حدد حساب Azure AD المرتجع، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="17670-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="17670-131">ستتم تعبئة حقول **الاسم المستعار** و **UPN** و **المعرف الفرعي الخارجي** على علامة تبويب **Commerce** في صفحة تفاصيل العامل.</span><span class="sxs-lookup"><span data-stu-id="17670-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="17670-132">بعد تحديث سجل العامل، علي سبيل المثال إذا تم إقران حساب Azure AD جديد أو تغيير كلمة مرور أو تحديث دفتر عناوين الموظفين، من المستحسن أن تقوم بتشغيل جدول التوزيع **1060** (**الموظفون**) لمزامنة معلومات الموظفين الأخيرة مع القناة.</span><span class="sxs-lookup"><span data-stu-id="17670-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="17670-133">وبهذه الطريقة، يمكن لتطبيق نقطة البيع إحضار البيانات الصحيحة لمصادقة المستخدم والتحقق من التخويل.</span><span class="sxs-lookup"><span data-stu-id="17670-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17670-134">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="17670-134">Additional resources</span></span>

[<span data-ttu-id="17670-135">إعداد وظيفة تسجيل الدخول الموسع لنقطة البيع الحديثة ونقطة البيع السحابية</span><span class="sxs-lookup"><span data-stu-id="17670-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="17670-136">إنشاء ملف تعريف وظائف البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="17670-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="17670-137"> تكوين عامل</span><span class="sxs-lookup"><span data-stu-id="17670-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
