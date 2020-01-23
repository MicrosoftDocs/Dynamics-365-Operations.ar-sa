---
title: ما الجديد أو المتغير في Dynamics 365 Talent - Core HR‏ (11 يناير 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899164"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a><span data-ttu-id="25c51-103">ما الجديد أو المتغير في Dynamics 365 Talent - Core HR‏ (11 يناير 2019)</span><span class="sxs-lookup"><span data-stu-id="25c51-103">What's new or changed in Dynamics 365 Talent - Core HR (January 11, 2019)</span></span>

<span data-ttu-id="25c51-104">**الإصدار 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="25c51-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="25c51-105">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Core HR.</span><span class="sxs-lookup"><span data-stu-id="25c51-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="25c51-106">التغييرات</span><span class="sxs-lookup"><span data-stu-id="25c51-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="25c51-107">التحقق من صحة طلبات الإجازة عن طريق التنبؤ بالرصيد المتوفر</span><span class="sxs-lookup"><span data-stu-id="25c51-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="25c51-108">تسمح التغييرات التي تم إدخالها في هذا الإصدار للموظفين بالمطالبة بوقت إجازة مستقبلي من دون طرحه من رصيدهم الحالي.</span><span class="sxs-lookup"><span data-stu-id="25c51-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="25c51-109">سيتم استخدام مهام سير العمل القياسية لأي طلبات مستقبلية يتم تقديمها.</span><span class="sxs-lookup"><span data-stu-id="25c51-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="25c51-110">للحصول على مزيد من المعلومات، اقرأ [الإجازة المستحقة بناءً على ساعات العمل](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="25c51-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="25c51-111">عرض رصيد الإجازات المتوقع في خدمة الموظف الذاتية والأشخاص</span><span class="sxs-lookup"><span data-stu-id="25c51-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="25c51-112">تسمح هذه الميزة بعرض أرصدة فترات الإجازات المستقبلية من قِبل قسم الموارد البشرية والمدراء والموظفين.</span><span class="sxs-lookup"><span data-stu-id="25c51-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="25c51-113">بإمكان الموظفين عرض الأرصدة المستقبلية في مساحة عمل **خدمة الموظف الذاتية‬**، ويستطيع قسم الموارد البشرية الوصول إلى نفس المعلومات باستخدام مساحة عمل **الأشخاص**.</span><span class="sxs-lookup"><span data-stu-id="25c51-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="25c51-114">الإخطارات المتعلقة بأرصدة الإجازات المتغيرة</span><span class="sxs-lookup"><span data-stu-id="25c51-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="25c51-115">سوف تعرض أرصدة الإجازات الرصيد الحالي للموظفين.</span><span class="sxs-lookup"><span data-stu-id="25c51-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="25c51-116">وتتوفر الأرصدة المستقبلية على مساحتي العمل **خدمة الموظف الذاتية‬** و**الأشخاص** عن طريق إدخال "اعتبارًا من تاريخ" لحساب الرصيد المتوقع.</span><span class="sxs-lookup"><span data-stu-id="25c51-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="25c51-117">تمت إضافة التنقل لعرض الأرصدة المتوقعة في النواحي التالية:</span><span class="sxs-lookup"><span data-stu-id="25c51-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="25c51-118">بطاقة **زمن التوقف** على مساحة عمل **خدمة الموظف الذاتية‬**.</span><span class="sxs-lookup"><span data-stu-id="25c51-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="25c51-119">بطاقة عمل **الإجازة والغياب** على مساحة عمل **الخدمة الذاتية للمدير‬**.</span><span class="sxs-lookup"><span data-stu-id="25c51-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="25c51-120">صفحة **الإجازة والغياب** على مساحة عمل **الأشخاص**.</span><span class="sxs-lookup"><span data-stu-id="25c51-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="25c51-121">السماح بالأرقام العشرية لخطط التعويض المتغير (خطط نقدية)</span><span class="sxs-lookup"><span data-stu-id="25c51-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="25c51-122">تتميز الآن المكافآت والخطط النقدية المتغيرة بمرونة إضافية للمبالغ وتجاوزات للقيم ذات المبالغ العشرية.</span><span class="sxs-lookup"><span data-stu-id="25c51-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="25c51-123">يتعذر تغيير التواريخ في عمليات التسجيل في التعويض المتغير بعد حفظ الخطة</span><span class="sxs-lookup"><span data-stu-id="25c51-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="25c51-124">يسمح هذا التغيير بتحديث تاريخ انتهاء الخطة (ممددة أو منتهية صلاحيته) بعد حفظ الخطة.</span><span class="sxs-lookup"><span data-stu-id="25c51-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="25c51-125">لا يزال باستطاعتك تنشيط الخطط أو إلغاء تنشيطها بشكل مستقل عن تاريخي البدء والانتهاء.</span><span class="sxs-lookup"><span data-stu-id="25c51-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="25c51-126">تتوفر معلومات المرتبات عند تعيين دور أمان مسؤول المرتبات</span><span class="sxs-lookup"><span data-stu-id="25c51-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="25c51-127">تم تحديث دور مسؤول المرتبات بحيث يتمكن من الوصول إلى معلومات المرتبات أثناء عملية الطلب.</span><span class="sxs-lookup"><span data-stu-id="25c51-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="25c51-128">فشل خدمة الموظف الذاتية | التدرج الهرمي للمناصب في التنقل وصولاً إلى العقدة الأصلية</span><span class="sxs-lookup"><span data-stu-id="25c51-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="25c51-129">تم إدخال تغييرات للتخلص من خطأ كان يحدث عند إضافة التدرج الهرمي للمناصب إلى مساحات عمل جديدة والتنقل في البنية التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="25c51-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="25c51-130">رسالة تحقق من الصحة جديدة عند استخدام التسلسل الرقمي للموظفين</span><span class="sxs-lookup"><span data-stu-id="25c51-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="25c51-131">تم إجراء تغيير لتوضيح المشكلة التي تظهر عند تعيين موظف ويكون رقم الموظف التالي قيد الاستخدام.</span><span class="sxs-lookup"><span data-stu-id="25c51-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="25c51-132">تحديد مساحة عمل خدمة الموظف الذاتية‬ المحددة كصفحة بدء تشغيل أولي</span><span class="sxs-lookup"><span data-stu-id="25c51-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="25c51-133">عند تحديد مساحة عمل **خدمة الموظف الذاتية‬** كصفحة بدء تشغيل أولي لأحد المستخدمين، ولم يتم تعيين دور الموظف لهذا المستخدم، سيعيد النظام توجيه المستخدم إلى لوحة المعلومات افتراضية.</span><span class="sxs-lookup"><span data-stu-id="25c51-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="25c51-134">كود سبب الإنهاء‬ يحدّث سجل تعيين المنصب‬</span><span class="sxs-lookup"><span data-stu-id="25c51-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="25c51-135">سيحدّث كود سبب الإنهاء‬ الآن سجل تعيين المنصب‬ عند إنهاء عمل أحد الموظفين وإنهاء المنصب.</span><span class="sxs-lookup"><span data-stu-id="25c51-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
