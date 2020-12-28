---
title: جدولة أمر العمل في تاريخ ووقت محددين
description: يوضح هذا الموضوع كيفية جدولة أمر عمل في تاريخ ووقت محددين في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e81ea13a3463965c6e4785dac32f536d2e94a7ba
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421270"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="c40cf-103">جدولة أمر العمل في تاريخ ووقت محددين</span><span class="sxs-lookup"><span data-stu-id="c40cf-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c40cf-104">إذا كان من الضروري جدولة أحد أوامر العمل في تاريخ‏‎ *و* وقت محددين، فيمكنك تجاوز عمليه الجدولة القياسية في إدارة الأصول وإنشاء جدول معين لأمر العمل.</span><span class="sxs-lookup"><span data-stu-id="c40cf-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="c40cf-105">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="c40cf-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c40cf-106">في قائمة أمر العمل، انقر فوق معرف أمر العمل في عمود **أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="c40cf-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="c40cf-107">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="c40cf-107">Click **Edit**.</span></span>

4. <span data-ttu-id="c40cf-108">على علامة التبويب السريعة **رأس أمر العمل**، أدخل تواريخ وأوقات البدء والانتهاء في الحقلين **البدء المتوقع** و **الانتهاء المتوقع**.</span><span class="sxs-lookup"><span data-stu-id="c40cf-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

    ![الشكل 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="c40cf-110">على علامة التبويب السريعة **عام**، انقر فوق **جدول** لاستخدام عملية الجدولة القياسية، أو انقر فوق **إرسال** لتعين أمر العمل إلى عامل معين.</span><span class="sxs-lookup"><span data-stu-id="c40cf-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to assign the work order to a specific worker.</span></span>

6. <span data-ttu-id="c40cf-111">من أجل تجاوز حجوزات القدرة الإنتاجية الحالية لضمان جدولة أمر العمل في الفترة المتوقعة، قم بإجراء التحديدات كما هو موضح في الشكل أدناه في مربع الحوار **جدولة أمر العمل** > القسم **قدرة محدودة‬**.</span><span class="sxs-lookup"><span data-stu-id="c40cf-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="c40cf-112">وهذا يعني أن عملية الجدولة ستتجاهل حجوزات القدرة الإنتاجية الحالية نظرًا لضرورة بدء أمر العمل في وقت البدء المتوقع.</span><span class="sxs-lookup"><span data-stu-id="c40cf-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

    ![الشكل 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="c40cf-114">انقر فوق **موافق** لبدء الجدولة.</span><span class="sxs-lookup"><span data-stu-id="c40cf-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="c40cf-115">إذا أدت عملية الجدولة إلى الحصول على حجوزات مزدوجة، فسترى رسالة على الشاشة، ويمكنك ضبط أوامر العمل ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="c40cf-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="c40cf-116">من أجل جدولة عامل صيانة لأمر العمل، يجب أن يكون عامل الصاينة هذا متوفرًا في وقت وتاريخ البدء المتوقعين.</span><span class="sxs-lookup"><span data-stu-id="c40cf-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="c40cf-117">يتم إعداد توافر العاملين في [تقويم العمل](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span><span class="sxs-lookup"><span data-stu-id="c40cf-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 

