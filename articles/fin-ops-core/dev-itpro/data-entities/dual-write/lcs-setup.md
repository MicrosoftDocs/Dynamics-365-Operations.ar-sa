---
title: إعداد الكتابة المزدوجة من Lifecycle Services
description: يشرح هذا الموضوع كيفية إعداد اتصال كتابة مزدوجة بين بيئة Finance and Operations جديدة وبيئة Common Data Service جديدة من Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f49eba1748861af6ee3353a6c58005ee84ccae23
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998098"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="97505-103">إعداد الكتابة المزدوجة من Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="97505-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="97505-104">يشرح هذا الموضوع كيفية إعداد اتصال كتابة مزدوجة بين بيئة Finance and Operations جديدة وبيئة Common Data Service جديدة من Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="97505-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Common Data Service environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="97505-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="97505-105">Prerequisites</span></span>

<span data-ttu-id="97505-106">يجب أن تكون مسؤولاً لإعداد اتصال كتابة مزدوجة.</span><span class="sxs-lookup"><span data-stu-id="97505-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="97505-107">يجب أن يكون لديك حق الوصول إلى المستأجر.</span><span class="sxs-lookup"><span data-stu-id="97505-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="97505-108">يجب أن تكون مسؤولاً في بيئات Finance and Operations وبيئات Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="97505-108">You must be an admin in both Finance and Operations environments and Common Data Service environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="97505-109">إعداد اتصال كتابة مزدوجة</span><span class="sxs-lookup"><span data-stu-id="97505-109">Set up a dual-write connection</span></span>

<span data-ttu-id="97505-110">اتبع هذه الخطوات لإعداد اتصال الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="97505-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="97505-111">في LCS، انتقل إلى المشروع..</span><span class="sxs-lookup"><span data-stu-id="97505-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="97505-112">حدد **تكوين** لنشر بيئة جديدة.</span><span class="sxs-lookup"><span data-stu-id="97505-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="97505-113">حدد الإصدار.</span><span class="sxs-lookup"><span data-stu-id="97505-113">Select the version.</span></span> 
4. <span data-ttu-id="97505-114">حدد المخطط.</span><span class="sxs-lookup"><span data-stu-id="97505-114">Select the topology.</span></span> <span data-ttu-id="97505-115">إذا توفر مخطط واحد فقط، فسيتم تحديده بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="97505-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="97505-116">أكمل الخطوات الأولى في معالج **إعدادات النشر**.</span><span class="sxs-lookup"><span data-stu-id="97505-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="97505-117">على علامة التبويب **Common Data Service** ، اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="97505-117">On the **Common Data Service** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="97505-118">إذا تم تزويد بيئة Common Data Service للمستأجر، فيمكنك تحديدها.</span><span class="sxs-lookup"><span data-stu-id="97505-118">If a Common Data Service environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="97505-119">عيّن الخيار **تكوين Common Data Service** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="97505-119">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="97505-120">في حقل **البيئات المتوفرة** ، حدد البيئة التي تريد دمجها مع بيانات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="97505-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="97505-121">تتضمن القائمة كافة البيئات حيث تملك امتيازات إدارية.</span><span class="sxs-lookup"><span data-stu-id="97505-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="97505-122">حدد خانة الاختيار **أوافق** للإشارة إلى موافقتك على الأحكام والشروط.</span><span class="sxs-lookup"><span data-stu-id="97505-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![علامة التبويب Common Data Service عند تزويد بيئة Common Data Service للمستأجر](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="97505-124">إذا لم تتوفر بيئة Common Data Service لدى المستأجر، فسيتم تزويد بيئة.</span><span class="sxs-lookup"><span data-stu-id="97505-124">If your tenant doesn't already have a Common Data Service environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="97505-125">عيّن الخيار **تكوين Common Data Service** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="97505-125">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="97505-126">أدخل اسمًا لبيئة Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="97505-126">Enter a name for the Common Data Service environment.</span></span>
        3. <span data-ttu-id="97505-127">حدد المنطقة لنشر البيئة فيها.</span><span class="sxs-lookup"><span data-stu-id="97505-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="97505-128">حدد لغة البيئة وعملتها الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="97505-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="97505-129">لا يمكنك تغيير اللغة والعملة لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="97505-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="97505-130">حدد خانة الاختيار **أوافق** للإشارة إلى موافقتك على الأحكام والشروط.</span><span class="sxs-lookup"><span data-stu-id="97505-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![علامة التبويب Common Data Service عندما لا تتوفر بيئة Common Data Service لدى المستأجر](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="97505-132">أكمل الخطوات المتبقية في معالج **إعدادات النشر**.</span><span class="sxs-lookup"><span data-stu-id="97505-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="97505-133">بعد ان تصبح حالة البيئة **منشورة** ، افتح صفحة تفاصيل البيئة.</span><span class="sxs-lookup"><span data-stu-id="97505-133">After the environment has a status of **Deployed** , open the environment details page.</span></span> <span data-ttu-id="97505-134">يعرض القسم **معلومات بيئة Common Data Service** أسماء بيئة Finance and Operations وبيئة Common Data Service المرتبطتين.</span><span class="sxs-lookup"><span data-stu-id="97505-134">The **Common Data Service environment information** section shows the names of the Finance and Operations environment and the Common Data Service environment that are linked.</span></span>

    ![قسم معلومات بيئة Common Data Service](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="97505-136">يجب أن يقوم مسؤول بيئة Finance and Operations بتسجيل الدخول إلى LCS وتحديد **ارتباط إلى CDS للتطبيقات** لإكمال الارتباط.</span><span class="sxs-lookup"><span data-stu-id="97505-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="97505-137">تعرض صفحة تفاصيل البيئة معلومات الاتصال بالمسؤول.</span><span class="sxs-lookup"><span data-stu-id="97505-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="97505-138">بعد إكمال الارتباط، يتم تحديث الحالة إلى **إكمال ربط البيئة بنجاح**.</span><span class="sxs-lookup"><span data-stu-id="97505-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="97505-139">لفتح مساحة عمل **تكامل البيانات** في بيئة Finance and Operations والتحكم في القوالب المتوفرة، حدد **ارتباط إلى CDS للتطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="97505-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![الزر "ارتباط إلى CDS للتطبيقات" في قسم معلومات بيئة Common Data Service](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="97505-141">لا يمكنك إلغاء ارتباط البيئات باستخدام LCS.</span><span class="sxs-lookup"><span data-stu-id="97505-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="97505-142">لإلغاء ارتباط بيئة، افتح مساحة عمل **تكامل البيانات** في بيئة Finance and Operations، ثم حدد **إلغاء الارتباط**.</span><span class="sxs-lookup"><span data-stu-id="97505-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>
