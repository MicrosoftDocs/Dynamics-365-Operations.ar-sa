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
ms.openlocfilehash: 853791d5ffc1d92b9fbafa2acc13cd5543c38196
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275523"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="c0d0b-103">استكشاف المشاكل وإصلاحها مع وحدة الكتابة المزدوجة في تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c0d0b-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0d0b-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="c0d0b-105">على وجه التحديد، يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها في وحدة **الكتابة الثنائية** في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0d0b-106">قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c0d0b-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="c0d0b-107">يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="c0d0b-108">لا يمكنك تحميل وحدة الكتابة المزدوجة في تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c0d0b-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="c0d0b-109">إذا لم تتمكن من فتح صفحة **الكتابة الثنائية** بتحديد تجانب **الكتابة الثنائية** في مساحة عمل **إدارة البيانات**، فربما تكون خدمة تكامل البيانات معطلة.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="c0d0b-110">أنشئ تذكرة دعم لطلب إعادة تشغيل خدمة تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-map"></a><span data-ttu-id="c0d0b-111">حدث خطأ عند محاولة إنشاء تعيين كيان جديد</span><span class="sxs-lookup"><span data-stu-id="c0d0b-111">Error when you try to create a new entity map</span></span>

<span data-ttu-id="c0d0b-112">**بيانات الاعتماد المطلوبة لإصلاح المشكلة**: نفس المستخدم الذي قام بإعداد الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="c0d0b-113">قد تتلقى رسالة الخطأ التالية عند محاولة تكوين كيان جديد للكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="c0d0b-114">المستخدم الوحيد الذي يمكنه إنشاء خريطة هو المستخدم الذي قام بإعداد اتصال الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="c0d0b-115">*لا يشير رمز حالة الاستجابة إلى النجاح: 401 (غير مرخص)*</span><span class="sxs-lookup"><span data-stu-id="c0d0b-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="c0d0b-116">حدث خطأ عند فتح واجهة مستخدم الكتابة الثنائية</span><span class="sxs-lookup"><span data-stu-id="c0d0b-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="c0d0b-117">قد تتلقى رسالة الخطأ التالية عند محاولة الوصول إلى الكتابة الثنائية من مساحة عمل **إدارة البيانات**:</span><span class="sxs-lookup"><span data-stu-id="c0d0b-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="c0d0b-118">*login.microsoftonline.com رفض الاتصال.*</span><span class="sxs-lookup"><span data-stu-id="c0d0b-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="c0d0b-119">لإصلاح المشكلة، قم بتسجيل الدخول باستخدام إطار InPrivate في Microsoft Edge أو في إطار وضع التخفي في Chromium أو في إطار وضع التخفي في Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="c0d0b-120">يجب أيضا إلغاء حظر ملفات تعريف ارتباط الجهات الخارجية أو مسحها.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="c0d0b-121">حدث خطأ عند ربط البيئة للكتابة الثنائية أو إضافة تعيين كيان جديد</span><span class="sxs-lookup"><span data-stu-id="c0d0b-121">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="c0d0b-122">**الدور المطلوب لحل المشكلة:** مسؤول النظام في كل من تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="c0d0b-123">قد تواجه الخطأ التالي عند الارتباط بالمخططات أو إنشائها:</span><span class="sxs-lookup"><span data-stu-id="c0d0b-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="c0d0b-124">*لا يشير رمز حاله الاستجابة إلى النجاح: 403 (tokenexchange).<br>معرف جلسة العمل: \<معرف جلسة العمل\><br> معرف النشاط الجذر \<معرف النشاط الجذر الخاص بك\>*</span><span class="sxs-lookup"><span data-stu-id="c0d0b-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="c0d0b-125">يمكن أن يحدث هذا الخطأ إذا لم يكن لديك الأذونات الكافية للربط بين الكتابة الثنائية أو إنشاء المخططات.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="c0d0b-126">يمكن أن يحدث هذا الخطأ إذا تمت إعادة تعيين بيئة Common Data Service بدون إلغاء ربط الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-126">This error can also occur if the Common Data Service environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="c0d0b-127">يمكن لأي مستخدم يتمتع بدور مسؤول النظام في كل من تطبيقات Finance and Operations وCommon Data Service ربط البيئات.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-127">Any user with system administrator role in both Finance and Operations apps and Common Data Service can link the environments.</span></span> <span data-ttu-id="c0d0b-128">يمكن فقط للمستخدم الذي قام بإعداد اتصال الكتابة المزدوجة إضافة تعيينات لكيانات جديدة.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-128">Only the user who setup the dual-write connection can add new entity maps.</span></span> <span data-ttu-id="c0d0b-129">بعد الإعداد، يمكن لأي مستخدم يتمتع بدور مسؤول النظام مراقبة الحالة وتحرير التعيينات.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="c0d0b-130">حدث خطأ عند إيقاف تعيين الكيان</span><span class="sxs-lookup"><span data-stu-id="c0d0b-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="c0d0b-131">قد تظهر رسالة الخطأ التالية عندما تحاول إيقاف تعيينات الكيانات:</span><span class="sxs-lookup"><span data-stu-id="c0d0b-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="c0d0b-132">*\[ممنوع\]، \[{"status":403,"source":"","message":"خطأ من رمز التبديل المميز: غير مسموح للمستخدم بالوصول إلى dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]، أرجع الخادم البعيد خطأ: (403) ممنوع.*</span><span class="sxs-lookup"><span data-stu-id="c0d0b-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="c0d0b-133">يحدث هذا الخطأ عندما تكون بيئة Common Data Service المرتبطة غير متوفرة.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="c0d0b-134">لإصلاح المشكلة، أنشئ تذكرة لفريق تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="c0d0b-135">قم بإرفاق تتبع الشبكة حتى يتمكن فريق تكامل البيانات من وضع علامة على المخططات باعتبارها **ليست قيد التشغيل** في النهاية الخلفية.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-entity-mapping"></a><span data-ttu-id="c0d0b-136">حدث خطأ أثناء محاولة بدء تعيين كيان</span><span class="sxs-lookup"><span data-stu-id="c0d0b-136">Error while trying to start an entity mapping</span></span>

<span data-ttu-id="c0d0b-137">قد تتلقي خطأ مثل التالي عند محاولة تعيين تلك الحالة من التعيين إلى **قيد التشغيل:**</span><span class="sxs-lookup"><span data-stu-id="c0d0b-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="c0d0b-138">*تعذر إكمال مزامنة البيانات الأولية. خطأ: فشل في الكتابة المزدوجة - فشل تسجيل المكون الإضافي: تعذر إنشاء بيانات تعريف لبحث الكتابة المزدوجة. خطأ لم يتم تعيين مرجع كائن إلى مثيل كائن.*</span><span class="sxs-lookup"><span data-stu-id="c0d0b-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="c0d0b-139">يعتمد إصلاح هذا الخطأ على سبب الخطأ:</span><span class="sxs-lookup"><span data-stu-id="c0d0b-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="c0d0b-140">إذا كان التعيين يتضمن تعيينات تابعة، فتأكد من تمكين التعيينات التابعة لتعيين هذا الكيان.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this entity mapping.</span></span>
+ <span data-ttu-id="c0d0b-141">قد يكون التعيين مفتقدًا لحقول المصدر أو الوجهة.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="c0d0b-142">في حالة فقدان حقل في تطبيق Finance and Operations، اتبع الخطوات الموجودة في القسم [مشكلة فقدان حقول الكيان في التعيينات](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="c0d0b-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="c0d0b-143">في حالة فقدان حقل في Common Data Service، عندئذ انقر فوق **تحديث الكيانات** على التعيين بحيث يتم ملء الحقول تلقائيًا إلى التعيين.</span><span class="sxs-lookup"><span data-stu-id="c0d0b-143">If a field in Common Data Service is missing, then click **Refresh entities** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
