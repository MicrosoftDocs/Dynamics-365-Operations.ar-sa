---
title: استكشاف المشاكل وإصلاحها أثناء الإعداد الأولي
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح المشكلات التي قد تحدث أثناء الإعداد الأولي لتكامل الكتابة الثنائية بين تطبيقات Finance and OperationsوCommon Data Service.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 6fb71a17d767a1e84511743794d85523db25eba8
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997340"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="50a38-103">استكشاف المشاكل وإصلاحها أثناء الإعداد الأولي</span><span class="sxs-lookup"><span data-stu-id="50a38-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="50a38-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="50a38-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="50a38-105">على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات التي قد تحدث أثناء الإعداد الأولي لتكامل الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="50a38-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50a38-106">قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="50a38-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="50a38-107">يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="50a38-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a><span data-ttu-id="50a38-108">لا يمكنك ربط تطبيق Finance and Operations بـ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="50a38-108">You can't link a Finance and Operations app to Common Data Service</span></span>

<span data-ttu-id="50a38-109">**الدور المطلوب لتعيين الكتابة المزدوجة:** مسؤول النظام في تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="50a38-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="50a38-110">تحدث الأخطاء في صفحة **رابط الإعداد لـ Common Data Service** عادة بسبب وجود مشكلات الإعداد غير المكتمل أو المشكلات المتعلقة بالأذونات.</span><span class="sxs-lookup"><span data-stu-id="50a38-110">Errors on the **Setup link to Common Data Service** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="50a38-111">تأكد من نجاح عملية التحقق من الصحة الكاملة في صفحة **رابط الإعداد لـ Common Data Service** ، كما هو مبين في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="50a38-111">Make sure that the whole health check passes on the **Setup link to Common Data Service** page, as shown in the following illustration.</span></span> <span data-ttu-id="50a38-112">لا يمكنك ربط الكتابة الثنائية إلا إذا نجحت عملية التحقق من الصحة الكاملة.</span><span class="sxs-lookup"><span data-stu-id="50a38-112">You can't link dual-write unless the whole health check passes.</span></span>

![عملية التحقق من السلامة الناجحة](media/health_check.png)

<span data-ttu-id="50a38-114">يجب أن يكون لديك بيانات اعتماد مسؤول مستأجر Azure AD لربط بيئات Finance and Operations وCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="50a38-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Common Data Service environments.</span></span> <span data-ttu-id="50a38-115">بعد ربط البيئات، يمكن للمستخدمين تسجيل الدخول باستخدام بيانات اعتماد الحساب الخاص بهم وتحديث خريطة كيان موجودة.</span><span class="sxs-lookup"><span data-stu-id="50a38-115">After you link the environments, users can sign in by using their account credentials and update an existing entity map.</span></span>

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a><span data-ttu-id="50a38-116">حدث خطأ عند فتح الرابط المؤدي إلى صفحة Common Data Service</span><span class="sxs-lookup"><span data-stu-id="50a38-116">Error when you open the Link to Common Data Service page</span></span>

<span data-ttu-id="50a38-117">**بيانات الاعتماد المطلوبة لإصلاح المشكلة:** مسؤول مستأجر Azure AD</span><span class="sxs-lookup"><span data-stu-id="50a38-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="50a38-118">قد تظهر رسالة الخطأ التالية عندمت تفتح صفحة **الرابط لـ Common Data Service** في تطبيق Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="50a38-118">You might receive the following error message when you open the **Link to Common Data Service** page in a Finance and Operations app:</span></span>

<span data-ttu-id="50a38-119">*لا يشير رمز حالة الاستجابة إلى النجاح: 404 (لم يتم العثور عليه).*</span><span class="sxs-lookup"><span data-stu-id="50a38-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="50a38-120">يحدث هذا الخطأ عند عدم إكمال خطوة الموافقة.</span><span class="sxs-lookup"><span data-stu-id="50a38-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="50a38-121">للتحقق مما إذا كان قد تم إكمال خطوه الموافقة، قم بتسجيل الدخول إلى portal.Azure.com باستخدام حساب مسؤول مستأجر Azure AD، وراجع ما إذا كان التطبيق التابع للجهة الخارجية الذي يحتوي على المعرف **33976c19-1db5-4c02-810e-c243db79efde** في قائمة Azure AD **تطبيقات المرسسات**.</span><span class="sxs-lookup"><span data-stu-id="50a38-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="50a38-122">وفي حالة عدم توفرها، يجب توفير موافقة للتطبيقات.</span><span class="sxs-lookup"><span data-stu-id="50a38-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="50a38-123">لتوفير الموافقة على التطبيق، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="50a38-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="50a38-124">افتح عنوان URL التالي باستخدام بيانات اعتماد المسؤول.</span><span class="sxs-lookup"><span data-stu-id="50a38-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="50a38-125">يجب أن تكون مطالبًا بالموافقة.</span><span class="sxs-lookup"><span data-stu-id="50a38-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="50a38-126">حدد **قبول** للإشارة إلى أنك تقوم بمنح موافقتك لتثبيت التطبيق الذي يشتمل على المعرف **33976c19-1db5-4c02-810e-c243db79efde** الموجود في المستأجر الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="50a38-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="50a38-127">هذا التطبيق مطلوب لربط Common Data Service وتطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50a38-127">This app is required to link Common Data Service and Finance and Operations apps.</span></span> <span data-ttu-id="50a38-128">إذا كانت لديك مشكلة في هذه الخطوة، فقم بفتح المستعرض في وضع التخفي (في Google Chrome) أو في وضع InPrivate (في Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="50a38-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="50a38-129">تحقق من إعداد بيانات الشركة وفرق الكتابة الثنائية بشكل صحيح أثناء الربط</span><span class="sxs-lookup"><span data-stu-id="50a38-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="50a38-130">ولضمان عمل الكتابة الثنائية بشكل صحيح، يتم إنشاء الشركات التي تقوم بتحديدها أثناء التكوين في بيئة Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="50a38-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Common Data Service environment.</span></span> <span data-ttu-id="50a38-131">وبشكل افتراضي، تكون هذه الشركات للقراءة فقط، ويتم تعيين الخاصية **IsDualWriteEnable** إلى **True**.</span><span class="sxs-lookup"><span data-stu-id="50a38-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="50a38-132">بالإضافة إلى ذلك، يتم إنشاء مالك وحدةه الأعمال المالكة والفريق الافتراضي وتضمين اسم الشركة.</span><span class="sxs-lookup"><span data-stu-id="50a38-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="50a38-133">قبل تمكين المخططات، تحقق من تحديد مالك الفريق الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="50a38-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="50a38-134">للبحث عن كيان **الشركات (CDM\_الشركة)** ، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="50a38-134">To find the **Companies (CDM\_Company)** entity, follow these steps.</span></span>

1. <span data-ttu-id="50a38-135">في التطبيق المستند إلى النموذج في Dynamics 365، حدد عامل التصفية في الركن العلوي الأيمن.</span><span class="sxs-lookup"><span data-stu-id="50a38-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="50a38-136">من القائمة المنسدلة، حدد **الشركة**.</span><span class="sxs-lookup"><span data-stu-id="50a38-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="50a38-137">حدد **تشغيل** لعرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="50a38-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="50a38-138">حدد الشركة التي تم ربطها عندما قمت بتكوين الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="50a38-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="50a38-139">تحقق من أن حقل **الفريق المالك الافتراضي** يشتمل على قيمة.</span><span class="sxs-lookup"><span data-stu-id="50a38-139">Verify that the **Default owning team** field has a value.</span></span> <span data-ttu-id="50a38-140">في التوضيح التالي، يتم تعيين حقل **الفريق المالك الافتراضي** إلى **الكتابة الثنائية لـ USMF**.</span><span class="sxs-lookup"><span data-stu-id="50a38-140">In the following illustration, the **Default owning team** field is set to **USMF Dual Write**.</span></span>

    ![التحقق من الفريق الافتراضي المالك](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="50a38-142">البحث عن الحد الخاص بعدد الكيانات القانونية أو الشركات التي يمكن ربطها للكتابة الثنائية</span><span class="sxs-lookup"><span data-stu-id="50a38-142">Find the limit on the number of legal entities or companies that can be linked for dual-write</span></span>

<span data-ttu-id="50a38-143">قد تظهر رسالة الخطأ التالية عندما تحاول تمكين المخططات:</span><span class="sxs-lookup"><span data-stu-id="50a38-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="50a38-144">*فشل الكتابة الثنائية - فشل تسجيل المكون الإضافي: \[(يتعذر الحصول على مخطط تقسيم لمشروع DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443eaللمشروع DWM--. يتجاوز الخطا الحد الأقصى للأقسام المسموح بها لتعيين DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\]، حدث خطأ واحد أو أكثر.*</span><span class="sxs-lookup"><span data-stu-id="50a38-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="50a38-145">الحد الحالي عند ربط البيئات هو تقريبًا 40 كيانًا قانونيًا.</span><span class="sxs-lookup"><span data-stu-id="50a38-145">The current limit when you link the environments is approximately 40 legal entities.</span></span> <span data-ttu-id="50a38-146">يحدث هذا الخطأ إذا حاولت تمكين المخططات وكان أكثر من 40 كيانًا قانونيًا مرتبطًا بين البيئات.</span><span class="sxs-lookup"><span data-stu-id="50a38-146">This error occurs if you try to enable maps, and more than 40 legal entities are linked between the environments.</span></span>