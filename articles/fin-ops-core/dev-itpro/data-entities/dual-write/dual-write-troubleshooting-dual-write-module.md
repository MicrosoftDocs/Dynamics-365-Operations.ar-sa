---
title: استكشاف المشاكل وإصلاحها مع وحدة الكتابة المزدوجة في تطبيقات Finance and Operations
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح المشكلات ذات الصلة بوحدة الكتابة الثنائية في تطبيقات Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172750"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="10289-103">استكشاف المشاكل وإصلاحها مع وحدة الكتابة المزدوجة في تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="10289-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="10289-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="10289-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="10289-105">على وجه التحديد، يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها في وحدة **الكتابة الثنائية** في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10289-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10289-106">قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="10289-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="10289-107">يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="10289-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="10289-108">لا يمكنك تحميل وحدة الكتابة الثنائية في تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="10289-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="10289-109">إذا لم تتمكن من فتح صفحة **الكتابة الثنائية** بتحديد تجانب **الكتابة الثنائية** في مساحة عمل **إدارة البيانات**، فربما تكون خدمة تكامل البيانات معطلة.</span><span class="sxs-lookup"><span data-stu-id="10289-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="10289-110">أنشئ تذكرة دعم لطلب إعادة تشغيل خدمة تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="10289-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="10289-111">حدث خطأ عند محاولة إنشاء تعيين كيان جديد</span><span class="sxs-lookup"><span data-stu-id="10289-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="10289-112">**بيانات الاعتماد المطلوبة لإصلاح المشكلة:** مسؤول مستأجر Azure AD</span><span class="sxs-lookup"><span data-stu-id="10289-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="10289-113">قد تتلقى رسالة الخطأ التالية عند محاولة تكوين كيان جديد للكتابة الثنائية:</span><span class="sxs-lookup"><span data-stu-id="10289-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="10289-114">*لا يشير رمز حالة الاستجابة إلى النجاح: 401 (غير مرخص)*</span><span class="sxs-lookup"><span data-stu-id="10289-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="10289-115">يحدث هذا الخطأ نظرًا لأنه يمكن لمسؤول مستأجر Azure AD فقط إضافة تعيين كيان جديد.</span><span class="sxs-lookup"><span data-stu-id="10289-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="10289-116">لإصلاح هذه المشكلة، قم بتسجيل الدخول إلى تطبيق Finance and Operations كمستأجر مسؤول Azure AD.</span><span class="sxs-lookup"><span data-stu-id="10289-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="10289-117">كما يجب عليك الانتقال إلى موقع web.PowerApps.com وإعادة التحقق من اتصالك.</span><span class="sxs-lookup"><span data-stu-id="10289-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="10289-118">حدث خطأ عند فتح واجهة مستخدم الكتابة الثنائية</span><span class="sxs-lookup"><span data-stu-id="10289-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="10289-119">قد تتلقى رسالة الخطأ التالية عند محاولة الوصول إلى الكتابة الثنائية من مساحة عمل **إدارة البيانات**:</span><span class="sxs-lookup"><span data-stu-id="10289-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="10289-120">*login.microsoftonline.com رفض الاتصال.*</span><span class="sxs-lookup"><span data-stu-id="10289-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="10289-121">لإصلاح المشكلة، قم بتسجيل الدخول باستخدام إطار InPrivate في Microsoft Edge أو في إطار وضع التخفي في Chromium أو في إطار وضع التخفي في Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="10289-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="10289-122">يجب أيضا إلغاء حظر ملفات تعريف ارتباط الجهات الخارجية أو مسحها.</span><span class="sxs-lookup"><span data-stu-id="10289-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="10289-123">حدث خطأ عند ربط البيئة للكتابة الثنائية أو إضافة تعيين كيان جديد</span><span class="sxs-lookup"><span data-stu-id="10289-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="10289-124">**بيانات الاعتماد المطلوبة لإصلاح المشكلة:** مسؤول مستأجر Azure AD</span><span class="sxs-lookup"><span data-stu-id="10289-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="10289-125">قد تواجه الخطأ التالي عند الارتباط بالمخططات أو إنشائها:</span><span class="sxs-lookup"><span data-stu-id="10289-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="10289-126">*لا يشير رمز حاله الاستجابة إلى النجاح: 403 (tokenexchange).<br>معرف جلسة العمل: \<معرف جلسة العمل\><br> معرف النشاط الجذر \<معرف النشاط الجذر الخاص بك\>*</span><span class="sxs-lookup"><span data-stu-id="10289-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="10289-127">يمكن أن يحدث هذا الخطأ إذا لم يكن لديك الأذونات الكافية للربط بين الكتابة الثنائية أو إنشاء المخططات.</span><span class="sxs-lookup"><span data-stu-id="10289-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="10289-128">يجب عليك استخدام حساب مسؤول مستأجر Azure AD لربط البيئات وإضافة تعيينات جديدة للكيانات.</span><span class="sxs-lookup"><span data-stu-id="10289-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="10289-129">ولكن، بعد الإعداد، يمكنك استخدام حساب غير مسؤول لمراقبه الحالة وتحرير التعيينات.</span><span class="sxs-lookup"><span data-stu-id="10289-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="10289-130">حدث خطأ عند إيقاف تعيين الكيان</span><span class="sxs-lookup"><span data-stu-id="10289-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="10289-131">قد تظهر رسالة الخطأ التالية عندما تحاول إيقاف تعيينات الكيانات:</span><span class="sxs-lookup"><span data-stu-id="10289-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="10289-132">*\[ممنوع\]، \[{"status":403,"source":"","message":"خطأ من رمز التبديل المميز: غير مسموح للمستخدم بالوصول إلى dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]، أرجع الخادم البعيد خطأ: (403) ممنوع.*</span><span class="sxs-lookup"><span data-stu-id="10289-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="10289-133">يحدث هذا الخطأ عندما تكون بيئة Common Data Service المرتبطة غير متوفرة.</span><span class="sxs-lookup"><span data-stu-id="10289-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="10289-134">لإصلاح المشكلة، أنشئ تذكرة لفريق تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="10289-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="10289-135">قم بإرفاق تتبع الشبكة حتى يتمكن فريق تكامل البيانات من وضع علامة على المخططات باعتبارها **ليست قيد التشغيل** في النهاية الخلفية.</span><span class="sxs-lookup"><span data-stu-id="10289-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
