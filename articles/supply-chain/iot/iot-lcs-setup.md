---
title: تثبيت الوظيفة الإضافية لذكاء IoT في LCS
description: يشرح هذه الموضوع تثبيت الوظيفة الإضافية لذكاء IoT في Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386481"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="60907-103">تثبيت الوظيفة الإضافية لذكاء IoT في LCS</span><span class="sxs-lookup"><span data-stu-id="60907-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60907-104">يشرح هذه الموضوع تثبيت الوظيفة الإضافية لذكاء IoT في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="60907-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="60907-105">قبل أن تتمكن من تثبيت الوظيفة الإضافية، يجب [إنشاء موارد Azure](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="60907-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="60907-106">إعداد بيئة LCS</span><span class="sxs-lookup"><span data-stu-id="60907-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="60907-107">افتح LCS، وانتقل إلى بيئة Microsoft Dynamics 365 Supply Chain Management الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="60907-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="60907-108">قم بالتمرير إلى قسم **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="60907-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="60907-109">حدد **تثبيت وظيفة إضافية جديدة** لإظهار قائمة بالوظائف الإضافية التي تم تمكينها للبيئة.</span><span class="sxs-lookup"><span data-stu-id="60907-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="60907-110">في مربع الحوار **تحديد وظيفة إضافية للتثبيت**، حدد **ذكاء IoT**.</span><span class="sxs-lookup"><span data-stu-id="60907-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="60907-111">في مربع الحوار **إعداد وظيفة إضافية**، قم بتوفير تفاصيل مركز IoT وذاكرة تخزين Redis المؤقتة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="60907-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="60907-112">يمكنك العثور على القيم المطلوبة في المخزن الرئيسي الذي قمت بإنشائه في [إنشاء موارد Azure](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="60907-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="60907-113">**معرف المستأجر** – في مدخل Azure، انتقل إلى المخزن الرئيسي، ثم في جزء التنقل الأيسر، حدد **نظرة عامة**، ثم انسخ قيمة **معرف الدليل**.</span><span class="sxs-lookup"><span data-stu-id="60907-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="60907-114">قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="60907-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="60907-115">**عنوان URI للمخزن الرئيسي لنقطة النهاية المتوافقة مع مركز أحداث IoT** – انتقل إلى المفتاح الرئيسي، ثم في جزء التنقل الأيسر، حدد **نظرة عامة**، وانسخ قيمة **اسم DNS**.</span><span class="sxs-lookup"><span data-stu-id="60907-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="60907-116">قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="60907-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="60907-117">**اسم سر نقطة النهاية المتوافقة مع مركز أحداث IoT** – انتقل إلى المخزن الرئيسي، ثم حدد جزء التنقل الأيسر، وحدد **الأسرار**، وانسخ اسم السر الذي سيتم فيه تخزين سلسلة اتصال مركز الأحداث لـ مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="60907-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="60907-118">قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="60907-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="60907-119">**عنوان URI للمخزن الرئيسي لذاكرة تخزين Redis المؤقتة** – انتقل إلى المفتاح الرئيسي، ثم في جزء التنقل الأيسر، حدد **نظرة عامة**، وانسخ قيمة **اسم DNS**.</span><span class="sxs-lookup"><span data-stu-id="60907-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="60907-120">قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="60907-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="60907-121">**اسم سر نقطة النهاية ذاكرة تخزين Redis المؤقتة** – انتقل إلى المخزن الرئيسي، ثم حدد جزء التنقل الأيسر، وحدد **الأسرار**، وانسخ اسم السر الذي سيتم فيه تخزين سلسلة الاتصال لذاكرة تخزين Redis المؤقتة.</span><span class="sxs-lookup"><span data-stu-id="60907-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="60907-122">قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="60907-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="60907-123">حدد خانة الاختيار لقبول البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="60907-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="60907-124">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="60907-124">Select **Install**.</span></span>
8. <span data-ttu-id="60907-125">يظهر مربع رسالة ينص على أنه "تم بنجاح تشغيل الوظيفة الإضافية للتثبيت."</span><span class="sxs-lookup"><span data-stu-id="60907-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="60907-126">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="60907-126">Select **OK**.</span></span>

<span data-ttu-id="60907-127">اكتمل الآن إعداد LCS.</span><span class="sxs-lookup"><span data-stu-id="60907-127">LCS setup is now completed.</span></span> <span data-ttu-id="60907-128">الخطوة التالية هي [إعداد السيناريوهات](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="60907-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="60907-129">إلغاء تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="60907-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="60907-130">في Supply Chain Management، [قم بتعطيل السيناريوهات](iot-scenario-setup.md#how-to-disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="60907-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="60907-131">في LCS، انتقل إلى تفاصيل بيئة Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="60907-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="60907-132">قم بالتمرير إلى قسم **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="60907-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="60907-133">حدد **إلغاء التثبيت** للوظيفة الإضافية لذكاء IoT.</span><span class="sxs-lookup"><span data-stu-id="60907-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
