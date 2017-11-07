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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ebbf3c72b4c34cba95ecd2fb3ce506af393acc34
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="retail-time-and-attendance"></a>وقت البيع بالتجزئة والحضور

[!include[banner](includes/banner.md)]


يصف هذا الموضوع السيناريوهات المعتمدة لإدارة الوقت والحضور في Microsoft Dynamics 365 for Retail. 

<a name="manage-worker-setup-and-scheduling"></a>إدارة إعداد العمال وجدولتهم
----------------------------------

### <a name="initial-configuration"></a>التكوين الأولي

-   قم بتشغيل معالج التكوين.
-   قم بتسجيل العاملين كعمال التسجيل الزمني.

### <a name="plan-worker-schedules"></a>تخطيط جداول العامل

-   قم بتطبيق ملفات التعريف باستخدام مخطط العمل. لمزيد من المعلومات، راجع <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

لمزيد من المعلومات حول خطوات التكوين، راجع <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>تكوين خاص بالبيع بالتجزئة

-   قم بتمكين ملف تعريف الوظيفة ساعة الوقت للعاملين الذين تريد تمكين تسجيلات الوقت لديهم. انقر فوق **ملفات تعريف وظيفة نقطة البيع** &gt; **الوظائف** &gt; **تسجيلات وقت نقطة البيع** &gt; **تمكين تسجيلات الوقت**.
-   قم بتكوين مجموعات أذونات نقطة البيع (POS) لتمكين إذن عرض إدخالات ساعة الوقت. يسمح هذا الإذن للمستخدم عرض التسجيلات ساعة الوقت للعاملين الآخرين في المتجر (ومن أي متجر آخر يقترن بالمستخدم، خلال "دفتر العناوين"). قد تريد تمكين هذا الإذن لدور مدير لكن ليس دور الصراف. انقر فوق **مجموعات أذونات نقطة البيع** &gt; **عرض إدخالات ساعة الوقت**.

## <a name="register-time"></a>تسجيل الوقت
### <a name="cashier-and-non-cashier-time-registrations"></a>تسجيلات وقت الصراف وغير الصراف

-   في نقطة التشغيل:
    -   عمليات بدء العمل:
        -   تسجيل الدخول باستخدام عملية غير مرتبطة بدرج أو وردية جديدة.
        -   حدد عملية ساعة الوقت.
        -   تحديد عملية مرغوبة:
            -   بدء العمل
            -   راحة من العمل
            -   راحة لتناول الغذاء
            -   إنهاء العمل

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>الحالة الحالية</th>
    <th>العمليات المتاحة</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>بدء العمل</td>
    <td><ul>
    <li>راحة من العمل</li>
    <li>راحة لتناول الغذاء</li>
    <li>إنهاء العمل</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>راحة من العمل</td>
    <td>بدء العمل</td>
    </tr>
    <tr class="odd">
    <td>راحة لتناول الغذاء</td>
    <td>بدء العمل</td>
    </tr>
    <tr class="even">
    <td>إنهاء العمل</td>
    <td>بدء العمل</td>
    </tr>
    </tbody>
    </table>

    [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)
-   اعرض رسالة التأكيد، وتحقق من صحة وقت النشاط الحالي.
-   دفتر التسجيل:
    -   انقر فوق **دفتر التسجيل** لعرض نشاط ساعة الوقت.
    -   استخدام عوامل تصفية الوقت لتحديد إطارات زمنية مختلفة.
    -   إذا كنت تعمل في مواقع متجر متعدد، فإنك سترى تسجيلات الوقت الخاصة بك من كافة المتاجر حيث قمت بتسجيل الوقت. يمكنك استخدام عامل تصفية المتجر لعرض تسجيلات وقت من متجر محدد.

<!-- -->

-   مناطق زمنية مختلفة:
    -   إذا قمت بعرض الوقت من موقع آخر (لسجل الصراف، أو باستخدام **عرض إدخالات ساعة الوقت** لسيناريو مدير)، وهذا الموقع موجود في منطقة زمنية مختلفة، يتم تحويل السجلات الزمنية التي تراها إلى المنطقة الزمنية المحلية. ‏‫على سبيل المثال، إنك مدير لمتجرين وواحد في ولاية أريزونا والآخر في نيفادا. يسجل الصراف بدء العمل في الساعة 9:00 ص في أريزونا.‬ في تلك اللحظة، كان الوقت في نيفادا 8:00 ص ولذلك، إذا كنت في متجر نيفادا وتنظر إلى سجلات تسجيل الوقت، فإنه يتم وضع علامة تسجيل الوقت على الساعة 8 صباحًا.

## <a name="view-worker-time-registrations"></a>عرض تسجيلات الوقت للعمال
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>اعرض تسجيلات الوقت والتصفية حسب المتجر أو نوع النشاط

في نقطة التشغيل:

-   حدد **عرض إدخالات ساعة الوقت**.
-   إنك تراجع أنشطة تسجيل الوقت من جميع العمال الذين تم تعيينهم إلى المتاجر نفسها التي تم تعيينها لك.
-   يمكنك استخدام نوع النشاط وتخزين عوامل التصفية لتصفية تسجيلات الوقت.

## <a name="process-and-manage-time-registrations"></a>معالجة وإدارة تسجيلات الوقت
يتبع مستخدم Dynamics 365 for Retail سير العمل لحساب تسجيلات الوقت للرواتب والموافقة عليها ونقلها.

### <a name="primary-operations"></a>العمليات الأساسية

-   حساب
-   موافقة
-   إرسال للرواتب

### <a name="other-common-operations"></a>العمليات العامة الأخرى

-   انتهاء العمل المجمع
-   تسجيل الغياب

لمزيد من المعلومات حول كيفية معالجة تسجيلات الوقت والحضور، راجع <https://technet.microsoft.com/en-us/library/aa573180.aspx>.




