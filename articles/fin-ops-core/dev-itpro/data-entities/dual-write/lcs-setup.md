---
title: إعداد الكتابة المزدوجة من Lifecycle Services
description: يوضح هذا الموضوع كيفيه اعداد اتصال ثنائي الكتابة من Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e51b4ef1e309e5f89dc82a3776b88c505dc6593d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748531"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="55be2-103">إعداد الكتابة المزدوجة من Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="55be2-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="55be2-104">يشرح هذا الموضوع كيفية إعداد اتصال كتابة مزدوجة بين بيئة Finance and Operations جديدة وبيئة Dataverse جديدة من Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="55be2-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="55be2-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="55be2-105">Prerequisites</span></span>

<span data-ttu-id="55be2-106">يجب أن تكون مسؤولاً لإعداد اتصال كتابة مزدوجة.</span><span class="sxs-lookup"><span data-stu-id="55be2-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="55be2-107">يجب أن يكون لديك حق الوصول إلى المستأجر.</span><span class="sxs-lookup"><span data-stu-id="55be2-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="55be2-108">يجب أن تكون مسؤولاً في بيئات Finance and Operations وبيئات Dataverse.</span><span class="sxs-lookup"><span data-stu-id="55be2-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="55be2-109">إعداد اتصال كتابة مزدوجة</span><span class="sxs-lookup"><span data-stu-id="55be2-109">Set up a dual-write connection</span></span>

<span data-ttu-id="55be2-110">اتبع هذه الخطوات لإعداد اتصال الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="55be2-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="55be2-111">في LCS، انتقل إلى المشروع..</span><span class="sxs-lookup"><span data-stu-id="55be2-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="55be2-112">حدد **تكوين** لنشر بيئة جديدة.</span><span class="sxs-lookup"><span data-stu-id="55be2-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="55be2-113">حدد الإصدار.</span><span class="sxs-lookup"><span data-stu-id="55be2-113">Select the version.</span></span> 
4. <span data-ttu-id="55be2-114">حدد المخطط.</span><span class="sxs-lookup"><span data-stu-id="55be2-114">Select the topology.</span></span> <span data-ttu-id="55be2-115">إذا توفر مخطط واحد فقط، فسيتم تحديده بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="55be2-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="55be2-116">أكمل الخطوات الأولى في معالج **إعدادات النشر**.</span><span class="sxs-lookup"><span data-stu-id="55be2-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="55be2-117">على علامة التبويب **Dataverse**، اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="55be2-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="55be2-118">إذا تم تزويد بيئة Dataverse للمستأجر، فيمكنك تحديدها.</span><span class="sxs-lookup"><span data-stu-id="55be2-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="55be2-119">عيّن الخيار **تكوين Dataverse** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="55be2-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="55be2-120">في عمود **البيئات المتوفرة**، حدد البيئة التي تريد دمجها مع بيانات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="55be2-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="55be2-121">تتضمن القائمة كافة البيئات حيث تملك امتيازات إدارية.</span><span class="sxs-lookup"><span data-stu-id="55be2-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="55be2-122">حدد خانة الاختيار **أوافق** للإشارة إلى موافقتك على الأحكام والشروط.</span><span class="sxs-lookup"><span data-stu-id="55be2-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![علامة التبويب Dataverse عند تزويد بيئة Dataverse للمستأجر](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="55be2-124">إذا لم تتوفر بيئة Dataverse لدى المستأجر، فسيتم تزويد بيئة.</span><span class="sxs-lookup"><span data-stu-id="55be2-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="55be2-125">عيّن الخيار **تكوين Dataverse** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="55be2-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="55be2-126">أدخل اسمًا لبيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="55be2-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="55be2-127">حدد المنطقة لنشر البيئة فيها.</span><span class="sxs-lookup"><span data-stu-id="55be2-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="55be2-128">حدد لغة البيئة وعملتها الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="55be2-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="55be2-129">لا يمكنك تغيير اللغة والعملة لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="55be2-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="55be2-130">حدد خانة الاختيار **أوافق** للإشارة إلى موافقتك على الأحكام والشروط.</span><span class="sxs-lookup"><span data-stu-id="55be2-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![علامة التبويب Dataverse عندما لا تتوفر بيئة Dataverse لدى المستأجر](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="55be2-132">أكمل الخطوات المتبقية في معالج **إعدادات النشر**.</span><span class="sxs-lookup"><span data-stu-id="55be2-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="55be2-133">بعد ان تصبح حالة البيئة **منشورة**، افتح صفحة تفاصيل البيئة.</span><span class="sxs-lookup"><span data-stu-id="55be2-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="55be2-134">يعرض القسم **دمج Power Platform** أسماء بيئة Finance and Operations وبيئة Dataverse المرتبطتين.</span><span class="sxs-lookup"><span data-stu-id="55be2-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![قسم التكامل Power Platform](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="55be2-136">يجب أن يقوم مسؤول بيئة Finance and Operations بتسجيل الدخول إلى LCS وتحديد **ارتباط إلى CDS للتطبيقات** لإكمال الارتباط.</span><span class="sxs-lookup"><span data-stu-id="55be2-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="55be2-137">تعرض صفحة تفاصيل البيئة معلومات الاتصال بالمسؤول.</span><span class="sxs-lookup"><span data-stu-id="55be2-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="55be2-138">بعد إكمال الارتباط، يتم تحديث الحالة إلى **إكمال ربط البيئة بنجاح**.</span><span class="sxs-lookup"><span data-stu-id="55be2-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="55be2-139">لفتح مساحة عمل **تكامل البيانات** في بيئة Finance and Operations والتحكم في القوالب المتوفرة، حدد **ارتباط إلى CDS للتطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="55be2-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![الزر "ارتباط إلى CDS للتطبيقات" في قسم دمج Power Platform](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="55be2-141">لا يمكنك إلغاء ارتباط البيئات باستخدام LCS.</span><span class="sxs-lookup"><span data-stu-id="55be2-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="55be2-142">لإلغاء ارتباط بيئة، افتح مساحة عمل **تكامل البيانات** في بيئة Finance and Operations، ثم حدد **إلغاء الارتباط**.</span><span class="sxs-lookup"><span data-stu-id="55be2-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]