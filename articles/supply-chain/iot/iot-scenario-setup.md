---
title: إعداد سيناريو لذكاء IoT
description: يوضح هذا الموضوع كيفية تكوين سيناريوهات لذكاء IoT في Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 91deb080121d50794e6ff6fe79f9ca876b76deb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005242"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="e8540-103">إعداد سيناريو لذكاء IoT</span><span class="sxs-lookup"><span data-stu-id="e8540-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8540-104">يوضح هذا الموضوع كيفية تكوين سيناريوهات لذكاء IoT في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e8540-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e8540-105">قبل إعداد السيناريوهات، يجب [إعداد Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="e8540-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="e8540-106">في هذا الموضوع، ستقوم بتكوين سيناريو **وقت تعطل المعدات** لإنشاء إخطاء في Supply Chain Management عند تعطل أحد الأجهزة.</span><span class="sxs-lookup"><span data-stu-id="e8540-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="e8540-107">يبين هذا الموضوع أيضًا كيفية تكوين سيناريو **جودة المنتج** بحيث يتم إنشاء اخطار إذا كانت سمة أحد الأصناف خارج نطاق محدد، وكيفية تكوين سيناريو‏‎ **تأخيرات الإنتاج** بحيث يتم إنشاء اخطار إذا كان صافي الإنتاج أقل من قيمة الحد.</span><span class="sxs-lookup"><span data-stu-id="e8540-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="e8540-108">تكوين سيناريو تعطل المعدات في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e8540-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="e8540-109">يقوم سيناريو **وقت تعطل المعدات** بتعيين إشارة **خروج الجزء** إلى حد التنبيه الخاص بالجهاز.</span><span class="sxs-lookup"><span data-stu-id="e8540-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="e8540-110">وتجري مراقبة الجهاز فقط عندما يكون محددًا للسيناريو وعندما يكون معينًا إلى وضع **التشغيل** في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e8540-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="e8540-111">إذا تجاوز الوقت منذ آخر مرت تم فيها استلام إشارة **خروج الجزء** من الجهاز حد التنبيه، عندها يتم تشغيل إخطار **الجهاز معطل**.</span><span class="sxs-lookup"><span data-stu-id="e8540-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="e8540-112">إذا كان الجهاز لا يزال قيد التشغيل، يتم تشغيل إخطار **الجهاز قيد التشغيل** عند تلقي إشارة **خروج الجزء** التالية.</span><span class="sxs-lookup"><span data-stu-id="e8540-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="e8540-113">إذا ظل الجهاز معطلاً لمدة تزيد عن 30 دقيقة، يتم تشغيل إخطار **الجهاز معطل** جديد.</span><span class="sxs-lookup"><span data-stu-id="e8540-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="e8540-114">يتضمن سيناريو **وقت تعطل المعدات** التبعيات التالية:</span><span class="sxs-lookup"><span data-stu-id="e8540-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="e8540-115">يمكن تشغيل تنبيه فقط إذا كان أمر الإنتاج قيد التشغيل على جهاز تم تعيينه.</span><span class="sxs-lookup"><span data-stu-id="e8540-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="e8540-116">يجب إرسال إشارة تمثل إشارة **خروج الجزء** للجهاز المعين إلى مركز IoT، ويجب تضمين اسم خاصية فريد.</span><span class="sxs-lookup"><span data-stu-id="e8540-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="e8540-117">يجب أن تكون خاصية **الطابع الزمني** UNIX، حيث يتم التعبير عن القيمة بالمللي ثانية، موجودة في رسالة مركز Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e8540-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="e8540-118">لتكوين السيناريو، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e8540-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="e8540-119">سجل دخولك إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e8540-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="e8540-120">قم بتمكين علامة ميزة ذكاء IoT.</span><span class="sxs-lookup"><span data-stu-id="e8540-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="e8540-121">لمزيد من المعلومات، راجع [‏‫نظرة عامة على إدارة الميزات](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="e8540-121">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
3. <span data-ttu-id="e8540-122">تكوين المقاييس.</span><span class="sxs-lookup"><span data-stu-id="e8540-122">Configure the metrics.</span></span> <span data-ttu-id="e8540-123">لمزيد من المعلومات، راجع [كيفية تكوين المقاييس](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="e8540-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="e8540-124">انتقل إلى **التحكم بالإنتاج \> الإعداد \> ذكاء IoT \> إدارة السيناريوهات‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="e8540-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="e8540-125">على اللوحة **وقت تعطل المعدات**، حدد **تكوين** لفتح معالج التكوين.</span><span class="sxs-lookup"><span data-stu-id="e8540-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="e8540-126">الصفحة الأولى في المعالج هي صفحة **تعريف مخطط مستشعر المعدات**.</span><span class="sxs-lookup"><span data-stu-id="e8540-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="e8540-127">في هذه الصفحة، هدفك هو إعداد المخطط في Supply Chain Management بحيث يتطابق مع تنسيق JavaScript Object Notation (JSON) لرسائل مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="e8540-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="e8540-128">يمكن تعريف العديد من مخططات الرسائل.</span><span class="sxs-lookup"><span data-stu-id="e8540-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="e8540-129">لمزيد من المعلومات، راجع [تنسيقات المخطط لرسائل مركز IoT](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="e8540-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="e8540-130">في هذا المثال، تحتوي حمولة الرسائل على مجموعة من الرسائل بهذا التنسيق.</span><span class="sxs-lookup"><span data-stu-id="e8540-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

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

7. <span data-ttu-id="e8540-131">أضف سطرًا إلى الجدول، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e8540-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="e8540-132">قم بتعيين حقل **اسم المخطط** إلى **المعرف**.</span><span class="sxs-lookup"><span data-stu-id="e8540-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="e8540-133">قم بتعيين حقل **مسار المخطط** إلى **/payload\[\*\]/id**.</span><span class="sxs-lookup"><span data-stu-id="e8540-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="e8540-134">قم بعيين حقل **الوصف** إلى **معرف الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="e8540-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="e8540-135">أضف سطرًا آخر إلى الجدول، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e8540-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="e8540-136">قم بتعيين حقل **اسم المخطط** إلى **الطابع الزمني**.</span><span class="sxs-lookup"><span data-stu-id="e8540-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="e8540-137">قم بتعيين حقل **مسار المخطط** إلى **/payload\[\*\]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="e8540-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="e8540-138">قم بتعيين حقل **الوصف** إلى **الطابع الزمني للرسالة**.</span><span class="sxs-lookup"><span data-stu-id="e8540-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="e8540-139">أضف سطرًا آخر إلى الجدول، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e8540-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="e8540-140">قم بتعيين حقل **اسم المخطط** إلى **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="e8540-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="e8540-141">قم بتعيين حقل **مسار المخطط** إلى **/payload\[\*\]/value**.</span><span class="sxs-lookup"><span data-stu-id="e8540-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="e8540-142">قم بتعيين حقل **الوصف** إلى **قيمة الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="e8540-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e8540-143">لا حاجة إلى تعريف كافة الخصائص في الرسالة.</span><span class="sxs-lookup"><span data-stu-id="e8540-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="e8540-144">يمكنك تعريف الخصائص التي تحتاج إليها فقط.</span><span class="sxs-lookup"><span data-stu-id="e8540-144">Define only the properties that you require.</span></span> <span data-ttu-id="e8540-145">في الخطوات السابقة، لم تقم بإنشاء صف **الطابع الزمني الجذر‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="e8540-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="e8540-146">مسار **الطابع الزمني الجذر** يجب أن يكون **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="e8540-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="e8540-147">حدد **التالي** للانتقال إلى صفحة **خريطة مخططات مستشعرات المعدات**.</span><span class="sxs-lookup"><span data-stu-id="e8540-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="e8540-148">في صف **معرف مورد المعدات** في حقل **اسم المخطط** حدد **المعرف**.</span><span class="sxs-lookup"><span data-stu-id="e8540-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="e8540-149">في الصف **وقت UTC**، في حقل **اسم المخطط** حدد **الطابع الزمني**.</span><span class="sxs-lookup"><span data-stu-id="e8540-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="e8540-150">في صف **الإشارة الناتجة عن الصف**، في حقل **اسم المخطط** حدد **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="e8540-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="e8540-151">حدد **التالي** للانتقال إلى صفحة **تكوين معرف مورد المعدات**.</span><span class="sxs-lookup"><span data-stu-id="e8540-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="e8540-152">اتبع هذه الخطوات لتعيين تعيين القيم في رسالة مركز IoT إلى موارد Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="e8540-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="e8540-153">في الجدول **قيم بيانات الإشارات**، أضف صفًا جديدًا.</span><span class="sxs-lookup"><span data-stu-id="e8540-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="e8540-154">في حقل **القيمة**، أدخل **IoTInt.Machine1225.PartOut**.</span><span class="sxs-lookup"><span data-stu-id="e8540-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="e8540-155">تأتي هذه القيمة من خاصية **معرف** JSON إلى رسالة مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="e8540-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="e8540-156">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e8540-156">Select **Save**.</span></span>
    3. <span data-ttu-id="e8540-157">في جدول **تعيين سجل الأعمال**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e8540-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="e8540-158">يتم تلقائيًا ملء قيمة افتراضية للحقل **نوع سجل الأعمال**، ولا تحتاج إلى تغييرها.</span><span class="sxs-lookup"><span data-stu-id="e8540-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="e8540-159">في حقل **سجل الأعمال**، حدد مورد جهاز Supply Chain Management الذي يتم إرسال قيمة الإشارة منه.</span><span class="sxs-lookup"><span data-stu-id="e8540-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="e8540-160">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e8540-160">Select **Save**.</span></span>
    6. <span data-ttu-id="e8540-161">كرر هذه الخطوات لإضافة تعيين سجل أعمال جديد لـ **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="e8540-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="e8540-162">يمكنك تعيين قيم بيانات متعددة الإشارات لسجل مفرد في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e8540-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="e8540-163">استخدم عمود **المحدد** لتحديد الأجهزة التي تريد معالجتها.</span><span class="sxs-lookup"><span data-stu-id="e8540-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="e8540-164">لا حاجة إلى تعريف جميع قيم الإشارات، ولا حاجة إلى تحديد جميع الأجهزة.</span><span class="sxs-lookup"><span data-stu-id="e8540-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="e8540-165">حدد **التالي** للانتقال إلى صفحة **تكوين الإشارات الناتجة عن الجزء**.</span><span class="sxs-lookup"><span data-stu-id="e8540-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="e8540-166">في جدول **قيم بيانات الإشارات**، أضف صفًا، وعيّن حقل **القيمة** على **صحيح**.</span><span class="sxs-lookup"><span data-stu-id="e8540-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="e8540-167">تأتي هذه القيمة من خاصية **قيمة** JSON إلى رسالة مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="e8540-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="e8540-168">يمكنك إضافة العديد من القيم التي تحتاج إليها للسيناريو.</span><span class="sxs-lookup"><span data-stu-id="e8540-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="e8540-169">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e8540-169">Select **Save**.</span></span>
20. <span data-ttu-id="e8540-170">حدد **التالي** للانتقال إلى صفحة **حد تعطل المعدات**.</span><span class="sxs-lookup"><span data-stu-id="e8540-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="e8540-171">الأجهزة المدرجة هي الأجهزة التي تم تعيينها سابقًا إلى قيم الإشارة.</span><span class="sxs-lookup"><span data-stu-id="e8540-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="e8540-172">في هذه الصفحة، عليك تعيين حد لمعرفة ما إذا كان الجهاز معطلاً أم لا.</span><span class="sxs-lookup"><span data-stu-id="e8540-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="e8540-173">على سبيل المثال، إذا قمت بتعيين الحد إلى **10**، فستقوم Supply Chain Management بإنشاء إخطار إذا لم يكن يتم تلقي إشارة **خروج الجزء** من الجهاز لمدة 10 دقائق.</span><span class="sxs-lookup"><span data-stu-id="e8540-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="e8540-174">حدد **التالي** للانتقال إلى صفحة **تمكين السيناريو**.</span><span class="sxs-lookup"><span data-stu-id="e8540-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="e8540-175">عيّن الخيار لتمكين السيناريو.</span><span class="sxs-lookup"><span data-stu-id="e8540-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="e8540-176">حدد **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="e8540-176">Select **Finish**.</span></span>

<span data-ttu-id="e8540-177">تم الآن إكمال إعداد السيناريو.</span><span class="sxs-lookup"><span data-stu-id="e8540-177">The scenario setup is now completed.</span></span> <span data-ttu-id="e8540-178">سيبدأ ذكاء IoT تلقائيا معالجة رسائل مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="e8540-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="e8540-179">تكوين سيناريو جودة المنتج في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e8540-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="e8540-180">يقوم سيناريو **جودة المنتج** بإنشاء إخطار إذا كان هناك سمة لأحد الأصناف خارج النطاق المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8540-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="e8540-181">على سبيل المثال، يرسل المستشعر وزن كل صنف إلى مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="e8540-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="e8540-182">إذا كان أحد وزن أحد الأصناف ثقيلاً جدًا أو خفيفًا جدًا، فسيتم إنشاء إخطار في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e8540-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="e8540-183">يتضمن سيناريو **جودة المنتج** التبعيات التالية:</span><span class="sxs-lookup"><span data-stu-id="e8540-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="e8540-184">يمكن تشغيل تنبيه فقط إذا كان أمر الإنتاج يعمل على جهاز معين وينتج منتجًا لديه سمة دًفعة معينة.</span><span class="sxs-lookup"><span data-stu-id="e8540-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="e8540-185">يجب إرسال إشارة تمثل سمة الدُفعة إلى مركز IoT، ويجب تضمين اسم خاصية فريد.</span><span class="sxs-lookup"><span data-stu-id="e8540-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="e8540-186">يجب أن تكون خاصية **الطابع الزمني** UNIX، حيث يتم التعبير عن القيمة بالمللي ثانية، موجودة في رسالة مركز Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e8540-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="e8540-187">تكوين سيناريو تأخيرات الإنتاج في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e8540-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="e8540-188">يقوم سيناريو **تأخيرات الإنتاج** بإنشاء إخطار إذا كان صافي الإنتاج أقل من قيمة الحد.</span><span class="sxs-lookup"><span data-stu-id="e8540-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="e8540-189">في هذا السيناريو، يتم إرسال إشارة **خروج الجزء** إلى مركز IoT لكل صنف تم إنتاجه.</span><span class="sxs-lookup"><span data-stu-id="e8540-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="e8540-190">في Supply Chain Management، يتم حساب تأخير الأمر استنادًا إلى مقدار الوقت المجدول لتشغيل أمر الإنتاج، وعدد الأصناف التي يجب إنتاجها، ومقدار الوقت الذي تم خلاله تشغيل المهمة ، وعدد إشارات **خروج الجزء** التي تم استلامها.</span><span class="sxs-lookup"><span data-stu-id="e8540-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="e8540-191">يتم إنشاء إخطار بالتأخير إذا كان عدد إشارات **خروج الجزء** للمهمة أقل من قيمة الحد.</span><span class="sxs-lookup"><span data-stu-id="e8540-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="e8540-192">يتضمن سيناريو **تأخيرات الإنتاج** التبعيات التالية:</span><span class="sxs-lookup"><span data-stu-id="e8540-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="e8540-193">يمكن تشغيل تنبيه فقط إذا كان أمر الإنتاج قيد التشغيل على جهاز تم تعيينه.</span><span class="sxs-lookup"><span data-stu-id="e8540-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="e8540-194">يجب إرسال إشارة تمثل إشارة **خروج الجزء** للجهاز المعين إلى مركز Azure IoT، ويجب تضمين اسم خاصية فريد.</span><span class="sxs-lookup"><span data-stu-id="e8540-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="e8540-195">يجب أن تكون خاصية **الطابع الزمني** UNIX، حيث يتم التعبير عن القيمة بالمللي ثانية، موجودة في رسالة مركز Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e8540-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="e8540-196">تعطيل سيناريو</span><span class="sxs-lookup"><span data-stu-id="e8540-196">Disable a scenario</span></span>

<span data-ttu-id="e8540-197">اتبع هذه الخطوات لتعطيل سيناريو.</span><span class="sxs-lookup"><span data-stu-id="e8540-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="e8540-198">في Supply Chain Management، انتقل إلى **التحكم بالإنتاج \> الإعداد \> ذكاء IoT \> إدارة السيناريو**.</span><span class="sxs-lookup"><span data-stu-id="e8540-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="e8540-199">في لوحة السيناريو، حدد **تكوين**.</span><span class="sxs-lookup"><span data-stu-id="e8540-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="e8540-200">حدد **التالي** للانتقال إلى صفحة المعالج الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="e8540-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="e8540-201">عيّن خيار تعطيل السيناريو.</span><span class="sxs-lookup"><span data-stu-id="e8540-201">Set the option to disable the scenario.</span></span>
