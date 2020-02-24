---
title: إدارة الوقت والحضور في Retail
description: يصف هذا الموضوع السيناريوهات المعتمدة لإدارة الوقت والحضور في Dynamics 365 Commerce.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
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
ms.openlocfilehash: cca5e3232450e75f931a621b278c134129fc745c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021506"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="841d1-103">إدارة الوقت والحضور في Retail</span><span class="sxs-lookup"><span data-stu-id="841d1-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="841d1-104">يصف هذا الموضوع السيناريوهات المعتمدة لإدارة الوقت والحضور في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="841d1-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="841d1-105">إدارة إعداد العمال وجدولتهم</span><span class="sxs-lookup"><span data-stu-id="841d1-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="841d1-106">التكوين الأولي</span><span class="sxs-lookup"><span data-stu-id="841d1-106">Initial configuration</span></span>

- <span data-ttu-id="841d1-107">قم بتشغيل معالج التكوين.</span><span class="sxs-lookup"><span data-stu-id="841d1-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="841d1-108">قم بتسجيل العاملين كعمال التسجيل الزمني.</span><span class="sxs-lookup"><span data-stu-id="841d1-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="841d1-109">تخطيط جداول العامل</span><span class="sxs-lookup"><span data-stu-id="841d1-109">Plan worker schedules</span></span>

- <span data-ttu-id="841d1-110">قم بتطبيق ملفات التعريف باستخدام مخطط العمل.</span><span class="sxs-lookup"><span data-stu-id="841d1-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="841d1-111">لمزيد من المعلومات، راجع [تطبيق ملفات التعريف باستخدام مخطط العمل‬](https://technet.microsoft.com/library/aa551234.aspx).</span><span class="sxs-lookup"><span data-stu-id="841d1-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="841d1-112">لمزيد من المعلومات حول خطوات التكوين، راجع [إعداد الوقت والحضور](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="841d1-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="841d1-113">التكوين الخاص بـ Commerce</span><span class="sxs-lookup"><span data-stu-id="841d1-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="841d1-114">قم بتمكين ملف تعريف الوظيفة ساعة الوقت للعاملين الذين تريد تمكين تسجيلات الوقت لديهم.</span><span class="sxs-lookup"><span data-stu-id="841d1-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="841d1-115">انقر فوق **ملفات تعريف وظيفة نقطة البيع** &gt; **الوظائف** &gt; **تسجيلات وقت نقطة البيع** &gt; **تمكين تسجيلات الوقت**.</span><span class="sxs-lookup"><span data-stu-id="841d1-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="841d1-116">قم بتكوين مجموعات أذونات نقطة البيع (POS) لتمكين إذن عرض إدخالات ساعة الوقت.</span><span class="sxs-lookup"><span data-stu-id="841d1-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="841d1-117">يسمح هذا الإذن للمستخدم عرض التسجيلات ساعة الوقت للعاملين الآخرين في المتجر (ومن أي متجر آخر يقترن بالمستخدم، خلال "دفتر العناوين").</span><span class="sxs-lookup"><span data-stu-id="841d1-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="841d1-118">قد تريد تمكين هذا الإذن لدور مدير لكن ليس دور الصراف.</span><span class="sxs-lookup"><span data-stu-id="841d1-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="841d1-119">انقر فوق **مجموعات أذونات نقطة البيع** &gt; **عرض إدخالات ساعة الوقت**.</span><span class="sxs-lookup"><span data-stu-id="841d1-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="841d1-120">تسجيل الوقت</span><span class="sxs-lookup"><span data-stu-id="841d1-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="841d1-121">تسجيلات وقت الصراف وغير الصراف</span><span class="sxs-lookup"><span data-stu-id="841d1-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="841d1-122">في نقطة التشغيل:</span><span class="sxs-lookup"><span data-stu-id="841d1-122">On POS:</span></span>

    - <span data-ttu-id="841d1-123">عمليات بدء العمل:</span><span class="sxs-lookup"><span data-stu-id="841d1-123">Clock-in operations:</span></span>

        - <span data-ttu-id="841d1-124">تسجيل الدخول باستخدام عملية غير مرتبطة بدرج أو وردية جديدة.</span><span class="sxs-lookup"><span data-stu-id="841d1-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="841d1-125">حدد عملية ساعة الوقت.</span><span class="sxs-lookup"><span data-stu-id="841d1-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="841d1-126">تحديد عملية مرغوبة:</span><span class="sxs-lookup"><span data-stu-id="841d1-126">Select a desired operation:</span></span>

            - <span data-ttu-id="841d1-127">بدء العمل</span><span class="sxs-lookup"><span data-stu-id="841d1-127">Clock-in</span></span>
            - <span data-ttu-id="841d1-128">راحة من العمل</span><span class="sxs-lookup"><span data-stu-id="841d1-128">Break for Work</span></span>
            - <span data-ttu-id="841d1-129">راحة لتناول الغذاء</span><span class="sxs-lookup"><span data-stu-id="841d1-129">Break for Lunch</span></span>
            - <span data-ttu-id="841d1-130">إنهاء العمل</span><span class="sxs-lookup"><span data-stu-id="841d1-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="841d1-131">الحالة الحالية</span><span class="sxs-lookup"><span data-stu-id="841d1-131">Current state</span></span></th>
        <th><span data-ttu-id="841d1-132">العمليات المتاحة</span><span class="sxs-lookup"><span data-stu-id="841d1-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="841d1-133">بدء العمل</span><span class="sxs-lookup"><span data-stu-id="841d1-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="841d1-134">راحة من العمل</span><span class="sxs-lookup"><span data-stu-id="841d1-134">Break for Work</span></span></li>
        <li><span data-ttu-id="841d1-135">راحة لتناول الغذاء</span><span class="sxs-lookup"><span data-stu-id="841d1-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="841d1-136">إنهاء العمل</span><span class="sxs-lookup"><span data-stu-id="841d1-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="841d1-137">راحة من العمل</span><span class="sxs-lookup"><span data-stu-id="841d1-137">Break for Work</span></span></td>
        <td><span data-ttu-id="841d1-138">بدء العمل</span><span class="sxs-lookup"><span data-stu-id="841d1-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="841d1-139">راحة لتناول الغذاء</span><span class="sxs-lookup"><span data-stu-id="841d1-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="841d1-140">بدء العمل</span><span class="sxs-lookup"><span data-stu-id="841d1-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="841d1-141">إنهاء العمل</span><span class="sxs-lookup"><span data-stu-id="841d1-141">Clock-out</span></span></td>
        <td><span data-ttu-id="841d1-142">بدء العمل</span><span class="sxs-lookup"><span data-stu-id="841d1-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="841d1-143">[![حالات ساعة الوقت](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="841d1-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="841d1-144">اعرض رسالة التأكيد، وتحقق من صحة وقت النشاط الحالي.</span><span class="sxs-lookup"><span data-stu-id="841d1-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="841d1-145">دفتر التسجيل:</span><span class="sxs-lookup"><span data-stu-id="841d1-145">Logbook:</span></span>

    - <span data-ttu-id="841d1-146">انقر فوق **دفتر التسجيل** لعرض نشاط ساعة الوقت.</span><span class="sxs-lookup"><span data-stu-id="841d1-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="841d1-147">استخدام عوامل تصفية الوقت لتحديد إطارات زمنية مختلفة.</span><span class="sxs-lookup"><span data-stu-id="841d1-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="841d1-148">إذا كنت تعمل في مواقع متجر متعدد، فإنك سترى تسجيلات الوقت الخاصة بك من كافة المتاجر حيث قمت بتسجيل الوقت.</span><span class="sxs-lookup"><span data-stu-id="841d1-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="841d1-149">يمكنك استخدام عامل تصفية المتجر لعرض تسجيلات وقت من متجر محدد.</span><span class="sxs-lookup"><span data-stu-id="841d1-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="841d1-150">مناطق زمنية مختلفة:</span><span class="sxs-lookup"><span data-stu-id="841d1-150">Different time zones:</span></span>

    - <span data-ttu-id="841d1-151">إذا قمت بعرض الوقت من موقع آخر (لسجل الصراف، أو باستخدام **عرض إدخالات ساعة الوقت** لسيناريو مدير)، وهذا الموقع موجود في منطقة زمنية مختلفة، يتم تحويل السجلات الزمنية التي تراها إلى المنطقة الزمنية المحلية.</span><span class="sxs-lookup"><span data-stu-id="841d1-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="841d1-152">‏‫على سبيل المثال، إنك مدير لمتجرين وواحد في ولاية أريزونا والآخر في نيفادا.</span><span class="sxs-lookup"><span data-stu-id="841d1-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="841d1-153">يسجل الصراف بدء العمل في الساعة 9:00 ص</span><span class="sxs-lookup"><span data-stu-id="841d1-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="841d1-154">في أريزونا.‬</span><span class="sxs-lookup"><span data-stu-id="841d1-154">in Arizona.</span></span> <span data-ttu-id="841d1-155">في تلك اللحظة، كان الوقت في نيفادا 8:00 ص</span><span class="sxs-lookup"><span data-stu-id="841d1-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="841d1-156">ولذلك، إذا كنت في متجر نيفادا وتنظر إلى سجلات تسجيل الوقت، فإنه يتم وضع علامة تسجيل الوقت على الساعة 8 صباحًا.</span><span class="sxs-lookup"><span data-stu-id="841d1-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="841d1-157">عرض تسجيلات الوقت للعمال</span><span class="sxs-lookup"><span data-stu-id="841d1-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="841d1-158">اعرض تسجيلات الوقت والتصفية حسب المتجر أو نوع النشاط</span><span class="sxs-lookup"><span data-stu-id="841d1-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="841d1-159">في نقطة التشغيل:</span><span class="sxs-lookup"><span data-stu-id="841d1-159">On POS:</span></span>

- <span data-ttu-id="841d1-160">حدد **عرض إدخالات ساعة الوقت**.</span><span class="sxs-lookup"><span data-stu-id="841d1-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="841d1-161">إنك تراجع أنشطة تسجيل الوقت من جميع العمال الذين تم تعيينهم إلى المتاجر نفسها التي تم تعيينها لك.</span><span class="sxs-lookup"><span data-stu-id="841d1-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="841d1-162">يمكنك استخدام نوع النشاط وتخزين عوامل التصفية لتصفية تسجيلات الوقت.</span><span class="sxs-lookup"><span data-stu-id="841d1-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="841d1-163">معالجة وإدارة تسجيلات الوقت</span><span class="sxs-lookup"><span data-stu-id="841d1-163">Process and manage time registrations</span></span>

<span data-ttu-id="841d1-164">يتبع مستخدم Commerce سير العمل لحساب تسجيلات الوقت للرواتب والموافقة عليها ونقلها.</span><span class="sxs-lookup"><span data-stu-id="841d1-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="841d1-165">العمليات الأساسية</span><span class="sxs-lookup"><span data-stu-id="841d1-165">Primary operations</span></span>

- <span data-ttu-id="841d1-166">حساب</span><span class="sxs-lookup"><span data-stu-id="841d1-166">Calculate</span></span>
- <span data-ttu-id="841d1-167">موافقة</span><span class="sxs-lookup"><span data-stu-id="841d1-167">Approve</span></span>
- <span data-ttu-id="841d1-168">إرسال للمرتبات</span><span class="sxs-lookup"><span data-stu-id="841d1-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="841d1-169">العمليات العامة الأخرى</span><span class="sxs-lookup"><span data-stu-id="841d1-169">Other common operations</span></span>

- <span data-ttu-id="841d1-170">انتهاء العمل المجمع</span><span class="sxs-lookup"><span data-stu-id="841d1-170">Bulk Clock-out</span></span>
- <span data-ttu-id="841d1-171">تسجيل الغياب</span><span class="sxs-lookup"><span data-stu-id="841d1-171">Register Absence</span></span>

<span data-ttu-id="841d1-172">للحصول على مزيد من المعلومات حول كيفية معالجة تسجيلات الوقت والحضور، راجع [معالجة تسجيلات الوقت والحضور](https://technet.microsoft.com/library/aa573180.aspx).</span><span class="sxs-lookup"><span data-stu-id="841d1-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>
