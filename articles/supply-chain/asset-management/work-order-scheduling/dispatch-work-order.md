---
title: إرسال أمر العمل
description: يوضح هذا الموضوع كيفية إرسال أمر عمل في إدارة الأصول.
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
ms.openlocfilehash: 3412b447876d5cd0b16bdbfc0a30ae1afa3e33c0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215299"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="e3bb5-103">إرسال أمر العمل</span><span class="sxs-lookup"><span data-stu-id="e3bb5-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e3bb5-104">يمكنك جدولة أمر عمل واحد أو مهام أوامر عمل إلى عامل واحد باستخدام الوظيفة **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="e3bb5-105">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e3bb5-106">حدد أمر العمل في القائمة.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="e3bb5-107">في علامة التبويب **عام**، انقر فوق **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="e3bb5-108">في مربع الحوار **جدولة أمر العمل** ، حدد العامل في حقل **العامل** .</span><span class="sxs-lookup"><span data-stu-id="e3bb5-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="e3bb5-109">في حقل **جدولة الساعات**، يمكنك إدخال ساعات العمل المتوقعة في حال كانت ساعات العمل المتوقعة تختلف عن الساعات المتنبأ بها.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="e3bb5-110">في حقل **البداية المجدولة**، يمكنك تحرير تاريخ ووقت البدء إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="e3bb5-111">إذا كان من الضروري أن تأخذ عملية الجدولة في الاعتبار القيود على القدرة الإنتاجية فيما يتعلق بالموارد المجدولة مسبقًا لمهام أخرى، فمن ثم تأكد من تعيين أزرار التبديل **الأصل**، و **الأداة**، و **العامل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="e3bb5-112">إذا أردت الاطلاع على معلومات مفصلة حول عملية الجدولة، حدد **نعم** على زر التبديل **مطولّ‬** .</span><span class="sxs-lookup"><span data-stu-id="e3bb5-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="e3bb5-113">وهذا يعني أن معلومات تفصيلية حول الدرجات المحسوبة على أمر العمل سوف تظهر في سجل المعلومات.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="e3bb5-114">حدد **نعم** في زر التبديل **تجاهل الجدولة** لتجاهل الأيام المغلقة في التقويم (ينطبق ذلك على الأصل والعامل والأدوات).</span><span class="sxs-lookup"><span data-stu-id="e3bb5-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="e3bb5-115">حدد **نعم** في زر التبديل **تجاهل التنفيذ المجدول** لتجاهل القيود التي قد يكون تم تحديدها في أمر العمل فيما يتعلق بالجدولة.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="e3bb5-116">راجع قسم [التنفيذ المجدول](../setup-for-work-orders/scheduled-execution.md) للحصول على معلومات حول إعداد التنفيذ المجدول.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="e3bb5-117">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-117">Click **OK**.</span></span> <span data-ttu-id="e3bb5-118">يتم تحديث حالة دورة حياة أمر العمل تلقائيًا إلى حالة دورة الحياة **المجدولة** المحددة في **إدارة الأصول** > **الإعداد** > **أوامر العمل** > **نماذج دورة الحياة**.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="e3bb5-119">يعرض الشكل المبين أدناه مثالاً حول تحديدات الإرسال في مربع الحوار **جدولة أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![الشكل 1](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="e3bb5-121">إذا كنت ترغب في حذف الجدولة في أمر العمل، يتم إجراء ذلك عن طريق تحديد أمر العمل في **كافة أوامر العمل**، والنقر فوق **حذف الجدولة** في علامة التبويب **عام** . تذكر تحديث أمر العمل يدويًا حالة دورة حياة أمر العمل إذا قمت بحذف الجدولة.</span><span class="sxs-lookup"><span data-stu-id="e3bb5-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

