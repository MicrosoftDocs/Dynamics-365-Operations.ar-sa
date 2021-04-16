---
title: تثبيت الوظيفة الإضافية لذكاء IoT في LCS
description: يشرح هذه الموضوع تثبيت الوظيفة الإضافية لذكاء IoT في Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d1cc9a7535be05a3e466c27e53047d694cf0160
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826433"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="a033f-103">تثبيت الوظيفة الإضافية لذكاء IoT في LCS</span><span class="sxs-lookup"><span data-stu-id="a033f-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a033f-104">يشرح هذه الموضوع تثبيت الوظيفة الإضافية لذكاء IoT في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a033f-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a033f-105">لاحظ أنه لا يمكن تثبيت الوظائف الإضافية على بيئة عرض/تجريبية.</span><span class="sxs-lookup"><span data-stu-id="a033f-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="a033f-106">قبل أن تتمكن من تثبيت الوظيفة الإضافية، يجب [إنشاء موارد Azure](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a033f-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="a033f-107">إعداد بيئة LCS</span><span class="sxs-lookup"><span data-stu-id="a033f-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="a033f-108">افتح LCS، وانتقل إلى بيئة Microsoft Dynamics 365 Supply Chain Management الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a033f-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="a033f-109">قم بالتمرير إلى قسم **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="a033f-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="a033f-110">حدد **تثبيت وظيفة إضافية جديدة** لإظهار قائمة بالوظائف الإضافية التي تم تمكينها للبيئة.</span><span class="sxs-lookup"><span data-stu-id="a033f-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="a033f-111">في مربع الحوار **تحديد وظيفة إضافية للتثبيت**، حدد **ذكاء IoT**.</span><span class="sxs-lookup"><span data-stu-id="a033f-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="a033f-112">في مربع الحوار **إعداد وظيفة إضافية**، قم بتوفير تفاصيل مركز IoT وذاكرة تخزين Redis المؤقتة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a033f-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="a033f-113">يمكنك العثور على القيم المطلوبة في المخزن الرئيسي الذي قمت بإنشائه في [إنشاء موارد Azure](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a033f-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="a033f-114">**معرف المستأجر** – في مدخل Azure، انتقل إلى المخزن الرئيسي، ثم في جزء التنقل الأيسر، حدد **نظرة عامة**، ثم انسخ قيمة **معرف الدليل**.</span><span class="sxs-lookup"><span data-stu-id="a033f-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="a033f-115">قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="a033f-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="a033f-116">**عنوان URI للمخزن الرئيسي لنقطة النهاية المتوافقة مع مركز أحداث IoT** – انتقل إلى المفتاح الرئيسي، ثم في جزء التنقل الأيسر، حدد **نظرة عامة**، وانسخ قيمة **اسم DNS**.</span><span class="sxs-lookup"><span data-stu-id="a033f-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="a033f-117">قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="a033f-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="a033f-118">**اسم سر نقطة النهاية المتوافقة مع مركز أحداث IoT** – انتقل إلى المخزن الرئيسي، ثم حدد جزء التنقل الأيسر، وحدد **الأسرار**، وانسخ اسم السر الذي سيتم فيه تخزين سلسلة اتصال مركز الأحداث لـ مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="a033f-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="a033f-119">قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="a033f-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="a033f-120">**عنوان URI للمخزن الرئيسي لذاكرة تخزين Redis المؤقتة** – انتقل إلى المفتاح الرئيسي، ثم في جزء التنقل الأيسر، حدد **نظرة عامة**، وانسخ قيمة **اسم DNS**.</span><span class="sxs-lookup"><span data-stu-id="a033f-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="a033f-121">قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="a033f-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="a033f-122">**اسم سر نقطة النهاية ذاكرة تخزين Redis المؤقتة** – انتقل إلى المخزن الرئيسي، ثم حدد جزء التنقل الأيسر، وحدد **الأسرار**، وانسخ اسم السر الذي سيتم فيه تخزين سلسلة الاتصال لذاكرة تخزين Redis المؤقتة.</span><span class="sxs-lookup"><span data-stu-id="a033f-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="a033f-123">قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="a033f-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="a033f-124">حدد خانة الاختيار لقبول البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="a033f-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="a033f-125">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="a033f-125">Select **Install**.</span></span>
8. <span data-ttu-id="a033f-126">يظهر مربع رسالة ينص على أنه "تم بنجاح تشغيل الوظيفة الإضافية للتثبيت."</span><span class="sxs-lookup"><span data-stu-id="a033f-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="a033f-127">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a033f-127">Select **OK**.</span></span>

<span data-ttu-id="a033f-128">اكتمل الآن إعداد LCS.</span><span class="sxs-lookup"><span data-stu-id="a033f-128">LCS setup is now completed.</span></span> <span data-ttu-id="a033f-129">الخطوة التالية هي [إعداد السيناريوهات](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a033f-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="a033f-130">إلغاء تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="a033f-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="a033f-131">في Supply Chain Management، [قم بتعطيل السيناريوهات](iot-scenario-setup.md#disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="a033f-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="a033f-132">في LCS، انتقل إلى تفاصيل بيئة Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a033f-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="a033f-133">قم بالتمرير إلى قسم **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="a033f-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="a033f-134">حدد **إلغاء التثبيت** للوظيفة الإضافية لذكاء IoT.</span><span class="sxs-lookup"><span data-stu-id="a033f-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]