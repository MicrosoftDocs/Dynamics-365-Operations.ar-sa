---
title: إعداد الكتابة المزدوجة من Lifecycle Services
description: يوضح هذا الموضوع كيفيه اعداد اتصال ثنائي الكتابة من Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103559"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="94f1b-103">إعداد الكتابة المزدوجة من Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="94f1b-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="94f1b-104">يوضح هذا الموضوع كيفية تمكين الكتابة المزدوجة من Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="94f1b-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="94f1b-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="94f1b-105">Prerequisites</span></span>

<span data-ttu-id="94f1b-106">يجب إكمال تكامل Power Platform كما هو موضح في الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="94f1b-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="94f1b-107">Power Platform التكامل - التمكين أثناء نشر البيئة</span><span class="sxs-lookup"><span data-stu-id="94f1b-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="94f1b-108">Power Platform التكامل - الإعداد بعد نشر البيئة</span><span class="sxs-lookup"><span data-stu-id="94f1b-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="94f1b-109">إعداد الكتابة المزدوجة لبيئات Dataverse الجديدة</span><span class="sxs-lookup"><span data-stu-id="94f1b-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="94f1b-110">اتبع هذه الخطوات لإعداد الكتابة المزدوجة من الصفحة **تفاصيل بيئة** LCS:</span><span class="sxs-lookup"><span data-stu-id="94f1b-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="94f1b-111">في الصفحة **تفاصيل البيئة**، قم بتوسيع القسم **تكامل Power Platform**.</span><span class="sxs-lookup"><span data-stu-id="94f1b-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="94f1b-112">حدد الزر **تطبيق الكتابة المزدوجة**.</span><span class="sxs-lookup"><span data-stu-id="94f1b-112">Select the **Dual-write application** button.</span></span>

    ![تكامل Power Platform](media/powerplat_integration_step2.png)

3. <span data-ttu-id="94f1b-114">راجع البنود والشروط، ثم حدد **تكوين**.</span><span class="sxs-lookup"><span data-stu-id="94f1b-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="94f1b-115">حدد **موافق** للمتابعة.</span><span class="sxs-lookup"><span data-stu-id="94f1b-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="94f1b-116">يمكنك مراقبة التقدم عن طريق تحديث صفحة تفاصيل البيئة بشكل دوري.</span><span class="sxs-lookup"><span data-stu-id="94f1b-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="94f1b-117">يستغرق الإعداد عادة 30 دقيقة أو أقل.</span><span class="sxs-lookup"><span data-stu-id="94f1b-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="94f1b-118">عند اكتمال الإعداد، تقوم رسالة بإعلامك في حالة نجاح العملية أو إذا فشلت.</span><span class="sxs-lookup"><span data-stu-id="94f1b-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="94f1b-119">وفي حالة فشل الإعداد، يتم عرض رسالة خطأ مرتبطة.</span><span class="sxs-lookup"><span data-stu-id="94f1b-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="94f1b-120">يجب إصلاح أية أخطاء قبل الانتقال إلى الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="94f1b-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="94f1b-121">حدد **ارتباط إلى بيئة Power Platform** لإنشاء ارتباط بين Dataverse وقواعد البيانات الحالية الخاصة بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="94f1b-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="94f1b-122">يستغرق هذا عادة أقل من 5 دقائق.</span><span class="sxs-lookup"><span data-stu-id="94f1b-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="الربط ببيئة Power Platform ":::

8. <span data-ttu-id="94f1b-124">عند اكتمال الارتباط، يتم عرض ارتباط تشعبي.</span><span class="sxs-lookup"><span data-stu-id="94f1b-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="94f1b-125">استخدم الارتباط لتسجيل الدخول إلى منطقة إدارة الكتابة المزدوجة في البيئة Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="94f1b-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="94f1b-126">ومن هناك، يمكنك إعداد تعيينات الكيانات.</span><span class="sxs-lookup"><span data-stu-id="94f1b-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="94f1b-127">إعداد الكتابة المزدوجة لبيئة Dataverse موجودة</span><span class="sxs-lookup"><span data-stu-id="94f1b-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="94f1b-128">لإعداد الكتابة الزدوجة لبيئة Dataverse موجودة، يجب عليك إنشاء [بطاقة دعم Microsoft](../../lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="94f1b-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="94f1b-129">يجب أن تتضمن التذكرة:</span><span class="sxs-lookup"><span data-stu-id="94f1b-129">The ticket must include:</span></span>

+ <span data-ttu-id="94f1b-130">معرف بيئة Finance and Operations الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="94f1b-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="94f1b-131">اسم البيئة الخاصة بك من Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="94f1b-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="94f1b-132">معرف مؤسسة Dataverse أو معرف بيئة Power Platform من مركز مسؤول Power Platform.</span><span class="sxs-lookup"><span data-stu-id="94f1b-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="94f1b-133">في البطاقة الخاصة بك، اطلب أن يكون المُعرف هو المثيل المستخدم لتكامل Power Platform.</span><span class="sxs-lookup"><span data-stu-id="94f1b-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="94f1b-134">لا يمكنك إلغاء ارتباط البيئات باستخدام LCS.</span><span class="sxs-lookup"><span data-stu-id="94f1b-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="94f1b-135">لإلغاء ارتباط بيئة، افتح مساحة عمل **تكامل البيانات** في بيئة Finance and Operations، ثم حدد **إلغاء الارتباط**.</span><span class="sxs-lookup"><span data-stu-id="94f1b-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
