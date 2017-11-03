---
title: "وقت التجزئة والحضور"
description: "يصف هذا الموضوع السيناريوهات المعتمدة لإدارة الوقت والحضور في Microsoft Dynamics 365 for Retail."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d5672579c1e2d51e4b6494a1e86e3606c09a93a2
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="retail-time-and-attendance"></a><span data-ttu-id="0a541-103">وقت البيع بالتجزئة والحضور</span><span class="sxs-lookup"><span data-stu-id="0a541-103">Retail time and attendance</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="0a541-104">يصف هذا الموضوع السيناريوهات المعتمدة لإدارة الوقت والحضور في Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="0a541-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span> 

<a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="0a541-105">إدارة إعداد العمال وجدولتهم</span><span class="sxs-lookup"><span data-stu-id="0a541-105">Manage worker setup and scheduling</span></span>
----------------------------------

### <a name="initial-configuration"></a><span data-ttu-id="0a541-106">التكوين الأولي</span><span class="sxs-lookup"><span data-stu-id="0a541-106">Initial configuration</span></span>

-   <span data-ttu-id="0a541-107">قم بتشغيل معالج التكوين.</span><span class="sxs-lookup"><span data-stu-id="0a541-107">Run the configuration wizard.</span></span>
-   <span data-ttu-id="0a541-108">قم بتسجيل العاملين كعمال التسجيل الزمني.</span><span class="sxs-lookup"><span data-stu-id="0a541-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="0a541-109">تخطيط جداول العامل</span><span class="sxs-lookup"><span data-stu-id="0a541-109">Plan worker schedules</span></span>

-   <span data-ttu-id="0a541-110">قم بتطبيق ملفات التعريف باستخدام مخطط العمل.</span><span class="sxs-lookup"><span data-stu-id="0a541-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="0a541-111">لمزيد من المعلومات، راجع <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span><span class="sxs-lookup"><span data-stu-id="0a541-111">For more information, see <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span></span>

<span data-ttu-id="0a541-112">لمزيد من المعلومات حول خطوات التكوين، راجع <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span><span class="sxs-lookup"><span data-stu-id="0a541-112">For information about the configuration steps, see <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="0a541-113">تكوين خاص بالبيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="0a541-113">Retail-specific configuration</span></span>

-   <span data-ttu-id="0a541-114">قم بتمكين ملف تعريف الوظيفة ساعة الوقت للعاملين الذين تريد تمكين تسجيلات الوقت لديهم.</span><span class="sxs-lookup"><span data-stu-id="0a541-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="0a541-115">انقر فوق **ملفات تعريف وظيفة نقطة البيع** &gt; **الوظائف** &gt; **تسجيلات وقت نقطة البيع** &gt; **تمكين تسجيلات الوقت**.</span><span class="sxs-lookup"><span data-stu-id="0a541-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
-   <span data-ttu-id="0a541-116">قم بتكوين مجموعات أذونات نقطة البيع (POS) لتمكين إذن عرض إدخالات ساعة الوقت.</span><span class="sxs-lookup"><span data-stu-id="0a541-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="0a541-117">يسمح هذا الإذن للمستخدم عرض التسجيلات ساعة الوقت للعاملين الآخرين في المتجر (ومن أي متجر آخر يقترن بالمستخدم، خلال "دفتر العناوين").</span><span class="sxs-lookup"><span data-stu-id="0a541-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="0a541-118">قد تريد تمكين هذا الإذن لدور مدير لكن ليس دور الصراف.</span><span class="sxs-lookup"><span data-stu-id="0a541-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="0a541-119">انقر فوق **مجموعات أذونات نقطة البيع** &gt; **عرض إدخالات ساعة الوقت**.</span><span class="sxs-lookup"><span data-stu-id="0a541-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="0a541-120">تسجيل الوقت</span><span class="sxs-lookup"><span data-stu-id="0a541-120">Register time</span></span>
### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="0a541-121">تسجيلات وقت الصراف وغير الصراف</span><span class="sxs-lookup"><span data-stu-id="0a541-121">Cashier and non-cashier time registrations</span></span>

-   <span data-ttu-id="0a541-122">في نقطة التشغيل:</span><span class="sxs-lookup"><span data-stu-id="0a541-122">On POS:</span></span>
    -   <span data-ttu-id="0a541-123">عمليات بدء العمل:</span><span class="sxs-lookup"><span data-stu-id="0a541-123">Clock-in operations:</span></span>
        -   <span data-ttu-id="0a541-124">تسجيل الدخول باستخدام عملية غير مرتبطة بدرج أو وردية جديدة.</span><span class="sxs-lookup"><span data-stu-id="0a541-124">Log on with a non-drawer operation or New shift.</span></span>
        -   <span data-ttu-id="0a541-125">حدد عملية ساعة الوقت.</span><span class="sxs-lookup"><span data-stu-id="0a541-125">Select a Time Clock operation.</span></span>
        -   <span data-ttu-id="0a541-126">تحديد عملية مرغوبة:</span><span class="sxs-lookup"><span data-stu-id="0a541-126">Select a desired operation:</span></span>
            -   <span data-ttu-id="0a541-127">بدء العمل</span><span class="sxs-lookup"><span data-stu-id="0a541-127">Clock-in</span></span>
            -   <span data-ttu-id="0a541-128">راحة من العمل</span><span class="sxs-lookup"><span data-stu-id="0a541-128">Break for Work</span></span>
            -   <span data-ttu-id="0a541-129">راحة لتناول الغذاء</span><span class="sxs-lookup"><span data-stu-id="0a541-129">Break for Lunch</span></span>
            -   <span data-ttu-id="0a541-130">إنهاء العمل</span><span class="sxs-lookup"><span data-stu-id="0a541-130">Clock-out</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="0a541-131">الحالة الحالية</span><span class="sxs-lookup"><span data-stu-id="0a541-131">Current state</span></span></th>
    <th><span data-ttu-id="0a541-132">العمليات المتاحة</span><span class="sxs-lookup"><span data-stu-id="0a541-132">Available operations</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="0a541-133">بدء العمل</span><span class="sxs-lookup"><span data-stu-id="0a541-133">Clock-in</span></span></td>
    <td><ul>
    <li><span data-ttu-id="0a541-134">راحة من العمل</span><span class="sxs-lookup"><span data-stu-id="0a541-134">Break for Work</span></span></li>
    <li><span data-ttu-id="0a541-135">راحة لتناول الغذاء</span><span class="sxs-lookup"><span data-stu-id="0a541-135">Break for Lunch</span></span></li>
    <li><span data-ttu-id="0a541-136">إنهاء العمل</span><span class="sxs-lookup"><span data-stu-id="0a541-136">Clock-out</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="0a541-137">راحة من العمل</span><span class="sxs-lookup"><span data-stu-id="0a541-137">Break for Work</span></span></td>
    <td><span data-ttu-id="0a541-138">بدء العمل</span><span class="sxs-lookup"><span data-stu-id="0a541-138">Clock-in</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="0a541-139">راحة لتناول الغذاء</span><span class="sxs-lookup"><span data-stu-id="0a541-139">Break for Lunch</span></span></td>
    <td><span data-ttu-id="0a541-140">بدء العمل</span><span class="sxs-lookup"><span data-stu-id="0a541-140">Clock-in</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="0a541-141">إنهاء العمل</span><span class="sxs-lookup"><span data-stu-id="0a541-141">Clock-out</span></span></td>
    <td><span data-ttu-id="0a541-142">بدء العمل</span><span class="sxs-lookup"><span data-stu-id="0a541-142">Clock-in</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="0a541-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="0a541-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>
-   <span data-ttu-id="0a541-144">اعرض رسالة التأكيد، وتحقق من صحة وقت النشاط الحالي.</span><span class="sxs-lookup"><span data-stu-id="0a541-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
-   <span data-ttu-id="0a541-145">دفتر التسجيل:</span><span class="sxs-lookup"><span data-stu-id="0a541-145">Logbook:</span></span>
    -   <span data-ttu-id="0a541-146">انقر فوق **دفتر التسجيل** لعرض نشاط ساعة الوقت.</span><span class="sxs-lookup"><span data-stu-id="0a541-146">Click **Logbook** to view time clock activity.</span></span>
    -   <span data-ttu-id="0a541-147">استخدام عوامل تصفية الوقت لتحديد إطارات زمنية مختلفة.</span><span class="sxs-lookup"><span data-stu-id="0a541-147">Use time filters to select different time windows.</span></span>
    -   <span data-ttu-id="0a541-148">إذا كنت تعمل في مواقع متجر متعدد، فإنك سترى تسجيلات الوقت الخاصة بك من كافة المتاجر حيث قمت بتسجيل الوقت.</span><span class="sxs-lookup"><span data-stu-id="0a541-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="0a541-149">يمكنك استخدام عامل تصفية المتجر لعرض تسجيلات وقت من متجر محدد.</span><span class="sxs-lookup"><span data-stu-id="0a541-149">You can use the store filter to view time registrations from a selected store.</span></span>

<!-- -->

-   <span data-ttu-id="0a541-150">مناطق زمنية مختلفة:</span><span class="sxs-lookup"><span data-stu-id="0a541-150">Different time zones:</span></span>
    -   <span data-ttu-id="0a541-151">إذا قمت بعرض الوقت من موقع آخر (لسجل الصراف، أو باستخدام **عرض إدخالات ساعة الوقت** لسيناريو مدير)، وهذا الموقع موجود في منطقة زمنية مختلفة، يتم تحويل السجلات الزمنية التي تراها إلى المنطقة الزمنية المحلية.</span><span class="sxs-lookup"><span data-stu-id="0a541-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="0a541-152">‏‫على سبيل المثال، إنك مدير لمتجرين وواحد في ولاية أريزونا والآخر في نيفادا.</span><span class="sxs-lookup"><span data-stu-id="0a541-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="0a541-153">يسجل الصراف بدء العمل في الساعة 9:00 ص</span><span class="sxs-lookup"><span data-stu-id="0a541-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="0a541-154">في أريزونا.‬</span><span class="sxs-lookup"><span data-stu-id="0a541-154">in Arizona.</span></span> <span data-ttu-id="0a541-155">في تلك اللحظة، كان الوقت في نيفادا 8:00 ص</span><span class="sxs-lookup"><span data-stu-id="0a541-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="0a541-156">ولذلك، إذا كنت في متجر نيفادا وتنظر إلى سجلات تسجيل الوقت، فإنه يتم وضع علامة تسجيل الوقت على الساعة 8 صباحًا.</span><span class="sxs-lookup"><span data-stu-id="0a541-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="0a541-157">عرض تسجيلات الوقت للعمال</span><span class="sxs-lookup"><span data-stu-id="0a541-157">View worker time registrations</span></span>
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="0a541-158">اعرض تسجيلات الوقت والتصفية حسب المتجر أو نوع النشاط</span><span class="sxs-lookup"><span data-stu-id="0a541-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="0a541-159">في نقطة التشغيل:</span><span class="sxs-lookup"><span data-stu-id="0a541-159">On POS:</span></span>

-   <span data-ttu-id="0a541-160">حدد **عرض إدخالات ساعة الوقت**.</span><span class="sxs-lookup"><span data-stu-id="0a541-160">Select **View timeclock entries**.</span></span>
-   <span data-ttu-id="0a541-161">إنك تراجع أنشطة تسجيل الوقت من جميع العمال الذين تم تعيينهم إلى المتاجر نفسها التي تم تعيينها لك.</span><span class="sxs-lookup"><span data-stu-id="0a541-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
-   <span data-ttu-id="0a541-162">يمكنك استخدام نوع النشاط وتخزين عوامل التصفية لتصفية تسجيلات الوقت.</span><span class="sxs-lookup"><span data-stu-id="0a541-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="0a541-163">معالجة وإدارة تسجيلات الوقت</span><span class="sxs-lookup"><span data-stu-id="0a541-163">Process and manage time registrations</span></span>
<span data-ttu-id="0a541-164">يتبع مستخدم Dynamics 365 for Retail سير العمل لحساب تسجيلات الوقت للرواتب والموافقة عليها ونقلها.</span><span class="sxs-lookup"><span data-stu-id="0a541-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="0a541-165">العمليات الأساسية</span><span class="sxs-lookup"><span data-stu-id="0a541-165">Primary operations</span></span>

-   <span data-ttu-id="0a541-166">حساب</span><span class="sxs-lookup"><span data-stu-id="0a541-166">Calculate</span></span>
-   <span data-ttu-id="0a541-167">موافقة</span><span class="sxs-lookup"><span data-stu-id="0a541-167">Approve</span></span>
-   <span data-ttu-id="0a541-168">إرسال للرواتب</span><span class="sxs-lookup"><span data-stu-id="0a541-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="0a541-169">العمليات العامة الأخرى</span><span class="sxs-lookup"><span data-stu-id="0a541-169">Other common operations</span></span>

-   <span data-ttu-id="0a541-170">انتهاء العمل المجمع</span><span class="sxs-lookup"><span data-stu-id="0a541-170">Bulk Clock-out</span></span>
-   <span data-ttu-id="0a541-171">تسجيل الغياب</span><span class="sxs-lookup"><span data-stu-id="0a541-171">Register Absence</span></span>

<span data-ttu-id="0a541-172">لمزيد من المعلومات حول كيفية معالجة تسجيلات الوقت والحضور، راجع <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span><span class="sxs-lookup"><span data-stu-id="0a541-172">For more information about how to process time and attendance registrations, see <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span></span>




