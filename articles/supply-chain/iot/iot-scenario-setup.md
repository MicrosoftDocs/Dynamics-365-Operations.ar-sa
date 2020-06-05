---
title: إعداد سيناريو لذكاء IoT
description: يوضح هذا الموضوع كيفية تكوين سيناريو في Supply Chain Management لذكاء IoT.
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
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386482"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="d9722-103">إعداد سيناريو لذكاء IoT</span><span class="sxs-lookup"><span data-stu-id="d9722-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9722-104">يوضح هذا الموضوع كيفية تكوين سيناريو في Supply Chain Management لذكاء IoT.</span><span class="sxs-lookup"><span data-stu-id="d9722-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="d9722-105">قبل أن تتمكن من إعداد السيناريوهات، يجب [إعداد LCS](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d9722-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="d9722-106">في هذا الموضوع، ستقوم بتكوين سيناريو **تعطل المعدات** لإنشاء إخطار في Supply Chain Management عند تعطل إحدى الماكينات.</span><span class="sxs-lookup"><span data-stu-id="d9722-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="d9722-107">تكوين سيناريو **تعطل المعدات** في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d9722-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="d9722-108">يقوم سيناريو **تعطل المعدات** بتعيين إشارة خروج الجزء إلى حد التنبيه الخاص بالماكينة.</span><span class="sxs-lookup"><span data-stu-id="d9722-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="d9722-109">وتجري مراقبة الماكينة فقط عندما تكون الماكينة محددة للسيناريو وتم تعيينها للتشغيل في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d9722-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="d9722-110">إذا كان الوقت منذ آخر مرت تم فيها استلام إشارة خروج الجزء للماكينة أكبر من حد التنبيه، عندها يتم تشغيل إخطار **الجهاز معطل**.</span><span class="sxs-lookup"><span data-stu-id="d9722-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="d9722-111">إذا كان الجهاز لا يزال قيد التشغيل، عند تلقي إشارة **خروج الجزء** التالية يتم تشغيل إخطار **الجهاز قيد التشغيل**.</span><span class="sxs-lookup"><span data-stu-id="d9722-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="d9722-112">إذا ظل الجهاز معطلا لمدة تزيد عن 30 دقيقة يتم تشغيل إخطار **الجهاز معطل** جديد.</span><span class="sxs-lookup"><span data-stu-id="d9722-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="d9722-113">يحتوي سيناريو **تعطل المعدات** على التبعيات التالية:</span><span class="sxs-lookup"><span data-stu-id="d9722-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="d9722-114">يجب أن يتم تشغيل أمر الإنتاج على ماكينة معينة لكي يتم تشغيل تنبيه.</span><span class="sxs-lookup"><span data-stu-id="d9722-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="d9722-115">يجب إرسال إشارة تمثل إشارة خروج الجزء للماكينة المعينة إلى مركز IoT باستخدام اسم خاصية فريد.</span><span class="sxs-lookup"><span data-stu-id="d9722-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="d9722-116">يجب أن تكون خاصية الطابع الزمني Unix بالملي ثانية موجودة في رسالة مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="d9722-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="d9722-117">لتكوين السيناريو، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="d9722-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="d9722-118">سجل الدخول إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d9722-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="d9722-119">قم بتمكين علامة ميزة ذكاء IoT.</span><span class="sxs-lookup"><span data-stu-id="d9722-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="d9722-120">لمزيد من المعلومات، راجع [‏‫نظرة عامة على إدارة الميزات](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d9722-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="d9722-121">تكوين المقاييس.</span><span class="sxs-lookup"><span data-stu-id="d9722-121">Configure the metrics.</span></span> <span data-ttu-id="d9722-122">لمزيد من المعلومات، راجع [كيفية تكوين المقاييس](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="d9722-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="d9722-123">انتقل إلى **التحكم في الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="d9722-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="d9722-124">انتقل إلى **الإعداد \> ذكاء IoT \> إدارة السيناريوهات**.</span><span class="sxs-lookup"><span data-stu-id="d9722-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="d9722-125">انقر فوق **تكوين** في تجانب **تعطل المعدات**.</span><span class="sxs-lookup"><span data-stu-id="d9722-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="d9722-126">يبدأ معالج التكوين مع صفحة **تعريف مخطط مستشعر المعدات**.</span><span class="sxs-lookup"><span data-stu-id="d9722-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="d9722-127">الهدف هنا هو إعداد المخطط في Supply Chain Management لمطابقة تنسيق JSON الخاص برسائل IoT.</span><span class="sxs-lookup"><span data-stu-id="d9722-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="d9722-128">يمكن تعريف العديد من مخططات الرسائل.</span><span class="sxs-lookup"><span data-stu-id="d9722-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="d9722-129">لمزيد من المعلومات، راجع [تنسيقات مخطط الرسائل لمركز IoT](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="d9722-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="d9722-130">في هذا المثال، تحتوي حمولة الرسائل على مجموعة من الرسائل بهذا التنسيق:</span><span class="sxs-lookup"><span data-stu-id="d9722-130">In this example, the message payload contains a batch of messages with this format:</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="d9722-131">إضافة صف إلى الجدول.</span><span class="sxs-lookup"><span data-stu-id="d9722-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="d9722-132">قم بتعيين **اسم المخطط** إلى **المعرف**.</span><span class="sxs-lookup"><span data-stu-id="d9722-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="d9722-133">قم بتعيين **مسار المخطط** إلى **/payload[\*]/id**.</span><span class="sxs-lookup"><span data-stu-id="d9722-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="d9722-134">قم بعيين **الوصف** إلى **معرف الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="d9722-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="d9722-135">إضافة صف إلى الجدول.</span><span class="sxs-lookup"><span data-stu-id="d9722-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="d9722-136">قم بتعيين **اسم المخطط** إلى **الطابع الزمني**.</span><span class="sxs-lookup"><span data-stu-id="d9722-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="d9722-137">قم بتعيين **مسار المخطط** إلى **/payload[\*]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="d9722-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="d9722-138">قم بتعيين**الوصف** إلى **الطابع الزمني للرسالة**.</span><span class="sxs-lookup"><span data-stu-id="d9722-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="d9722-139">إضافة صف إلى الجدول.</span><span class="sxs-lookup"><span data-stu-id="d9722-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="d9722-140">قم بتعيين **اسم المخطط** إلى **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="d9722-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="d9722-141">قم بتعيين **مسار المخطط** إلى **/payload[\*]/value**.</span><span class="sxs-lookup"><span data-stu-id="d9722-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="d9722-142">قم بتعيين **الوصف** إلى **قيمة الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="d9722-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="d9722-143">لا يلزمك تعريف كافة الخصائص في الرسالة، بل فقط التي تحتاج إليها.</span><span class="sxs-lookup"><span data-stu-id="d9722-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="d9722-144">في هذا المثال، لم تقم بإنشاء صف **للطابع الزمني الجذري**.</span><span class="sxs-lookup"><span data-stu-id="d9722-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="d9722-145">مسار **الطابع الزمني الجذر** سيكون **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="d9722-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="d9722-146">انقر فوق **التالي** للانتقال إلى صفحة **خريطة مخططات مستشعرات المعدات**.</span><span class="sxs-lookup"><span data-stu-id="d9722-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="d9722-147">في صف **معرف مورد المعدات** قم بتعيين **اسم المخطط** إلى **المعرف**.</span><span class="sxs-lookup"><span data-stu-id="d9722-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="d9722-148">يتم عرض القيم الصالحة في جدول منسدل.</span><span class="sxs-lookup"><span data-stu-id="d9722-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="d9722-149">في الصف الخاص **بوقت UTC** قم بتعيين **اسم المخطط** إلى **الطابع الزمني**.</span><span class="sxs-lookup"><span data-stu-id="d9722-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="d9722-150">يتم عرض القيم الصالحة في جدول منسدل.</span><span class="sxs-lookup"><span data-stu-id="d9722-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="d9722-151">في صف **الإشارة الناتجة عن الصف** قم بتعيين **اسم المخطط** إلى **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="d9722-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="d9722-152">يتم عرض القيم الصالحة في جدول منسدل.</span><span class="sxs-lookup"><span data-stu-id="d9722-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="d9722-153">انقر فوق **التالي** لصفحة **تكوين معرف مورد المعدات**.</span><span class="sxs-lookup"><span data-stu-id="d9722-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="d9722-154">في هذه الخطوة، ستقوم بتعيين قيم الرسائل لمركز IoT إلى موارد Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d9722-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="d9722-155">في جدول **قيم بيانات الإشارات**، أضف صفًا جديدًا، وأدخل **IoTInt.Machine1225.PartOut** في عمود **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="d9722-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="d9722-156">تأتي القيمة **IoTInt.Machine1225.PartOut** من خاصية **معرف** JSON في رسائل مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="d9722-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="d9722-157">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d9722-157">Click **Save**.</span></span>
    3. <span data-ttu-id="d9722-158">في جدول **تعيين سجل الأعمال**، انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d9722-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="d9722-159">يتم تلقائيًا ملء القيمة الافتراضية لـ **نوع سجل الأعمال**، ولا تحتاج إلى تغييرها.</span><span class="sxs-lookup"><span data-stu-id="d9722-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="d9722-160">في عمود **سجل الأعمال**، حدد مورد جهاز Supple Chain Managementالذي يتم إرسال قيمة الإشارة هذه منه.</span><span class="sxs-lookup"><span data-stu-id="d9722-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="d9722-161">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d9722-161">Click **Save**.</span></span>
    6. <span data-ttu-id="d9722-162">كرر هذه الخطوات، مع إضافة تعيين سجل أعمال جديد لـ **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="d9722-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="d9722-163">يمكنك تعيين قيم بيانات متعددة الإشارات لسجل مفرد في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d9722-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="d9722-164">استخدم عمود **المحدد** لاختيار الأجهزة التي تريد معالجتها.</span><span class="sxs-lookup"><span data-stu-id="d9722-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="d9722-165">ليس عليك تحديد كافة قيم الإشارات وليس عليك تحديد كافة الماكينات.</span><span class="sxs-lookup"><span data-stu-id="d9722-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="d9722-166">انقر فوق **التالي** للانتقال إلى صفحة **تكوين الإشارات الناتجة عن الجزء**.</span><span class="sxs-lookup"><span data-stu-id="d9722-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="d9722-167">في جدول **قيم بيانات الإشارات**، قم بإضافة صف، وقم بتعيين **القيمة** على **صحيح**.</span><span class="sxs-lookup"><span data-stu-id="d9722-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="d9722-168">تأتي القيمة **صحيح** من خاصية **قيمة** JSON في رسائل مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="d9722-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="d9722-169">يمكنك إضافة العديد من القيم التي تحتاج إليها للسيناريو الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d9722-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="d9722-170">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d9722-170">Click **Save**.</span></span>
20. <span data-ttu-id="d9722-171">انقر فوق **التالي** للانتقال إلى صفحة **حد تعطل المعدات**.</span><span class="sxs-lookup"><span data-stu-id="d9722-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="d9722-172">الماكينات المدرجة هي الماكينات التي تم تعيينها سابقًا إلى قيم الإشارة.</span><span class="sxs-lookup"><span data-stu-id="d9722-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="d9722-173">في هذه الخطوة، عليك تحديد الحد الخاص بمعرفة ما إذا كانت الماكينة معطلة أم لا.</span><span class="sxs-lookup"><span data-stu-id="d9722-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="d9722-174">على سبيل المثال، إذا قمت بتعيين الحد إلى 10، فان Supply Chain Management تقوم بإنشاء إخطار إذا لم يكن هناك رسالة خروج الجزء من الماكينة لمدة 10 دقائق.</span><span class="sxs-lookup"><span data-stu-id="d9722-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="d9722-175">انقر فوق **التالي** للانتقال إلى صفحة **تمكين السيناريو**.</span><span class="sxs-lookup"><span data-stu-id="d9722-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="d9722-176">قم بتبديل شريط التمرير لتمكين السيناريو.</span><span class="sxs-lookup"><span data-stu-id="d9722-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="d9722-177">انقر فوق **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="d9722-177">Click **Finish**.</span></span>

<span data-ttu-id="d9722-178">تم إكمال إعداد السيناريو.</span><span class="sxs-lookup"><span data-stu-id="d9722-178">The scenario setup is complete.</span></span> <span data-ttu-id="d9722-179">ستقوم ذكاء IoT تلقائيا ببدء معالجة رسائل مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="d9722-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="d9722-180">تكوين سيناريو **جودة المنتج** في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d9722-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="d9722-181">يقوم سيناريو **جودة المنتج** بإنشاء إخطار إذا كان هناك سمة لأحد الأصناف خارج النطاق المحدد.</span><span class="sxs-lookup"><span data-stu-id="d9722-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="d9722-182">على سبيل المثال، قد يرسل المستشعر وزن كل عنصر إلى مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="d9722-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="d9722-183">في Supply Chain Management، سيتم إنشاء إخطار إذا كان الصنف كبيرًا جدًا أو خفيفًا جدًا.</span><span class="sxs-lookup"><span data-stu-id="d9722-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="d9722-184">يتضمن السيناريو التبعيات التالية:</span><span class="sxs-lookup"><span data-stu-id="d9722-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="d9722-185">يجب تشغيل أمر الإنتاج على ماكينة معينة وإنتاج منتج باستخدام سمة دفعة معينة لكي يتم إطلاق التنبيه.</span><span class="sxs-lookup"><span data-stu-id="d9722-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="d9722-186">يجب إرسال إشارة تمثل سمة الدفعة إلى مركز IoT باستخدام اسم خاصية فريد.</span><span class="sxs-lookup"><span data-stu-id="d9722-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="d9722-187">يجب أن تكون خاصية الطابع الزمني Unix بالملي ثانية موجودة في رسالة مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="d9722-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="d9722-188">تكوين سيناريو **تأخيرات الإنتاج** في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d9722-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="d9722-189">يقوم سيناريو **تأخيرات الإنتاج** بإنشاء إخطار إذا كان صافي الإنتاج أقل من قيمة الحد.</span><span class="sxs-lookup"><span data-stu-id="d9722-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="d9722-190">في هذا السيناريو، يتم إرسال إشارة **خروج الجزء** إلى مركز IoT لكل صنف تم إنتاجه.</span><span class="sxs-lookup"><span data-stu-id="d9722-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="d9722-191">في Supply Chain Management ، يتم حساب تأخير الأمر استنادًا إلى مقدار المدة المقرر أن يستغرقها تشغيل أمر الإنتاج، وعدد الأصناف التي يجب إنتاجها، والمدة التي تم فيها تشغيل المهمة، وعدد إشارات **خروج الجزء** المستلمة.</span><span class="sxs-lookup"><span data-stu-id="d9722-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="d9722-192">سيتم إنشاء إخطار بالتأخير إذا كان عدد إشارات **خروج الجزء** للمهمة أقل من قيمة الحد للقيمة المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="d9722-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="d9722-193">يتضمن السيناريو التبعيات التالية:</span><span class="sxs-lookup"><span data-stu-id="d9722-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="d9722-194">يجب أن يتم تشغيل أمر الإنتاج على ماكينة معينة لكي يتم تشغيل تنبيه.</span><span class="sxs-lookup"><span data-stu-id="d9722-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="d9722-195">يجب إرسال إشارة تمثل إشارة خروج الجزء للماكينة المعينة إلى مركز IoT باستخدام اسم خاصية فريد.</span><span class="sxs-lookup"><span data-stu-id="d9722-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="d9722-196">يجب أن تكون خاصية الطابع الزمني Unix بالملي ثانية موجودة في رسالة مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="d9722-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="d9722-197">كيفية تعطيل سيناريو</span><span class="sxs-lookup"><span data-stu-id="d9722-197">How to disable a scenario</span></span>

<span data-ttu-id="d9722-198">اتبع هذه الخطوات لتعطيل سيناريو.</span><span class="sxs-lookup"><span data-stu-id="d9722-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="d9722-199">في Supply Chain Management، انتقل إلى **التحكم في الإنتاج \> الإعداد \> ذكاء IoT\>**.</span><span class="sxs-lookup"><span data-stu-id="d9722-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="d9722-200">انقر فوق **تكوين** في السيناريو.</span><span class="sxs-lookup"><span data-stu-id="d9722-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="d9722-201">انقر فوق **التالي** للوصول إلى آخر علامة تبويب للمعالج.</span><span class="sxs-lookup"><span data-stu-id="d9722-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="d9722-202">قم بتبديل شريط التمرير لتعطيل السيناريو.</span><span class="sxs-lookup"><span data-stu-id="d9722-202">Toggle the slider to disable the scenario.</span></span>
