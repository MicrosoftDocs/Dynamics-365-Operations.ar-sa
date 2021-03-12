---
title: مراقبة وإدارة ذكاء IoT
description: يوضح هذا الموضوع كيفية مراقبة وإدارة ذكاء IoT.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7082f9e7640e8ef1b2873a954327b61a440e8ad0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999996"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="07301-103">مراقبة وإدارة ذكاء IoT</span><span class="sxs-lookup"><span data-stu-id="07301-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07301-104">يوضح هذا الموضوع كيفية مراقبة وإدارة ذكاء IoT.</span><span class="sxs-lookup"><span data-stu-id="07301-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="07301-105">مراقبة السيناريوهات في Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="07301-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="07301-106">يمكنك مراقبة معالجة ذكاء IoT من عدة أماكن:</span><span class="sxs-lookup"><span data-stu-id="07301-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="07301-107">**الوحدات \> التحكم في الإنتاج \> الاستفسارات والتقارير \> ذكاء IoT \> الإخطارات** – عرض قائمة بالإخطارات التي لم يتم حلها.</span><span class="sxs-lookup"><span data-stu-id="07301-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="07301-108">**الوحدات \> التحكم في الإنتاج \> الاستفسارات والتقارير \> ذكاء IoT \> الإخطارات المغلقة** – عرض قائمة بالإخطارات التي يتم حلها أو تجاهلها.</span><span class="sxs-lookup"><span data-stu-id="07301-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="07301-109">**الوحدات \> التحكم في الإنتاج \> الاستعلامات والتقارير \> ذكاء IoT \> المفاتيح القياسية** – عرض المفاتيح القياسية لجداول السلاسل الزمنية لـ **حالة المورد**.</span><span class="sxs-lookup"><span data-stu-id="07301-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="07301-110">**الوحدات \> التحكم في الإنتاج \> تنفيذ التصنيع \> حالة المورد** – تتبع مقاييس خاصة باستخدام مربع حوار **التكوين**.</span><span class="sxs-lookup"><span data-stu-id="07301-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="07301-111">في حالة اكتشاف أحد السيناريوهات لاستثناء، يتم عرض إخطار يوضع تفاصيل الاستثناء.</span><span class="sxs-lookup"><span data-stu-id="07301-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="07301-112">**مساحات العمل \> إدارة طابق الإنتاج \> الإخطارات** – عرض قائمة بالإخطارات التي لم يتم حلها.</span><span class="sxs-lookup"><span data-stu-id="07301-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="07301-113">تعديل سيناريو ذكاء IoT قيد التشغيل</span><span class="sxs-lookup"><span data-stu-id="07301-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="07301-114">عندما يكون السيناريو قيد التشغيل، يمكنك إجراء هذه التغييرات:</span><span class="sxs-lookup"><span data-stu-id="07301-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="07301-115">إضافة تعريفات جديدة لمخطط المستشعرات.</span><span class="sxs-lookup"><span data-stu-id="07301-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="07301-116">تحديد حدد قيم بيانات إشارة جديدة.</span><span class="sxs-lookup"><span data-stu-id="07301-116">Select new signal data values.</span></span>
+ <span data-ttu-id="07301-117">إلغاء تحديد قيم بيانات الإشارة الموجودة.</span><span class="sxs-lookup"><span data-stu-id="07301-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="07301-118">إضافة قيم بيانات إشارة جديدة وتعيينها.</span><span class="sxs-lookup"><span data-stu-id="07301-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="07301-119">تحديث قيم الحد.</span><span class="sxs-lookup"><span data-stu-id="07301-119">Update threshold values.</span></span>

<span data-ttu-id="07301-120">عندما يكون السيناريو قيد التشغيل، يحظر إجراء هذه التغييرات:</span><span class="sxs-lookup"><span data-stu-id="07301-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="07301-121">حذف أو تعديل أي تعريفات للمخططات التي يتم استهلاكها حاليًا بواسطة سيناريو ممكن.</span><span class="sxs-lookup"><span data-stu-id="07301-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="07301-122">تغيير مسارات المخططات المحددة الخاصة بالسيناريو الممكن.</span><span class="sxs-lookup"><span data-stu-id="07301-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="07301-123">خيارات المحاكاة</span><span class="sxs-lookup"><span data-stu-id="07301-123">Simulation options</span></span>

<span data-ttu-id="07301-124">يمكنك محاكاة إشارات جهاز المصنع.</span><span class="sxs-lookup"><span data-stu-id="07301-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="07301-125">لمزيد من المعلومات، راجع هذه الموضوعات:</span><span class="sxs-lookup"><span data-stu-id="07301-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="07301-126">توصيل IoT DevKit AZ3166 بمركز Azure IoT</span><span class="sxs-lookup"><span data-stu-id="07301-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="07301-127">توصيل وحدة محاكاة Raspberry Pi على الإنترنت بمركز Azure IoT (Node.js)</span><span class="sxs-lookup"><span data-stu-id="07301-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="07301-128">نظرة عامة حول مسرع حل محاكاة الأجهزة</span><span class="sxs-lookup"><span data-stu-id="07301-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
