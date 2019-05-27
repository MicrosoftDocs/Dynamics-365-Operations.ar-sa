---
title: تكوين عامل باستخدام جهاز وظيفة محمول
description: يوضح هذا الإجراء كيفية تعيين الأدوار الصحيحة لحساب المستخدم للعامل، ثم قم بتمكين العامل للقيام بتسجيلات حالة العمل.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571348"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="dfc52-103">تكوين عامل باستخدام جهاز وظيفة محمول</span><span class="sxs-lookup"><span data-stu-id="dfc52-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dfc52-104">يوضح هذا الإجراء كيفية تعيين الأدوار الصحيحة لحساب المستخدم للعامل، ثم قم بتمكين العامل للقيام بتسجيلات حالة العمل.</span><span class="sxs-lookup"><span data-stu-id="dfc52-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="dfc52-105">تعيين أدوار لحساب المستخدم</span><span class="sxs-lookup"><span data-stu-id="dfc52-105">Assign roles to user account</span></span>
1. <span data-ttu-id="dfc52-106">انتقل إلى إدارة النظام > المستخدمين > المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="dfc52-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="dfc52-107">استخدم "عامل التصفية السريعة" لتصفية اسم عامل حيثما يكون حساب المستخدم مقترنًا بدور عامل تشغيل الجهاز.</span><span class="sxs-lookup"><span data-stu-id="dfc52-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="dfc52-108">في نموذج البيانات، سيكون الاسم شانون.</span><span class="sxs-lookup"><span data-stu-id="dfc52-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="dfc52-109">قم بتمييز سجل حساب المستخدم.</span><span class="sxs-lookup"><span data-stu-id="dfc52-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="dfc52-110">في القائمة، انقر فوق رابط "الاسم" في الصف المحدد لعرض التفاصيل الخاصة بحساب المستخدم.</span><span class="sxs-lookup"><span data-stu-id="dfc52-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="dfc52-111">في الشجرة، حدد "الأدوار/عامل تشغيل الجهاز".</span><span class="sxs-lookup"><span data-stu-id="dfc52-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="dfc52-112">أغلق صفحة تفاصيل حساب المستخدم.</span><span class="sxs-lookup"><span data-stu-id="dfc52-112">Close the user account details page.</span></span>
7. <span data-ttu-id="dfc52-113">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dfc52-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="dfc52-114">تكوين حساب عامل.</span><span class="sxs-lookup"><span data-stu-id="dfc52-114">Configure worker account.</span></span>
1. <span data-ttu-id="dfc52-115">انتقل إلى الموارد البشرية > العاملون > العاملون.</span><span class="sxs-lookup"><span data-stu-id="dfc52-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="dfc52-116">استخدم "عامل التصفية السريعة" لتصفية اسم عامل حيثما يكون حساب المستخدم مقترنًا بدور عامل تشغيل الجهاز.</span><span class="sxs-lookup"><span data-stu-id="dfc52-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="dfc52-117">في نموذج البيانات، سيكون الاسم شانون.</span><span class="sxs-lookup"><span data-stu-id="dfc52-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="dfc52-118">قم بتمييز سجل حساب المستخدم.</span><span class="sxs-lookup"><span data-stu-id="dfc52-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="dfc52-119">في القائمة، انقر فوق رابط "الاسم" في الصف المحدد لعرض التفاصيل الخاصة بحساب المستخدم.</span><span class="sxs-lookup"><span data-stu-id="dfc52-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="dfc52-120">انقر فوق علامة التبويب "التوظيف‬‬".</span><span class="sxs-lookup"><span data-stu-id="dfc52-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="dfc52-121">قم بتوسيع علامة التبويب السريعة تسجيل الوقت وانقر فوق تنشيط على وحدات التسجيل الطرفية.</span><span class="sxs-lookup"><span data-stu-id="dfc52-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="dfc52-122">انقر فوق تنشيط على وحدات التسجيل الطرفية‬.</span><span class="sxs-lookup"><span data-stu-id="dfc52-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="dfc52-123">في حقل "‏‫مجموعة الحساب‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dfc52-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="dfc52-124">في حقل "‏‫مجموعة الحساب الافتراضي‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dfc52-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="dfc52-125">في حقل "مجموعة الموافقة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dfc52-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="dfc52-126">في الحقل "ملف التعريف‬ القياسي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dfc52-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="dfc52-127">في حقل "مجموعة ملف التعريف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dfc52-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="dfc52-128">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="dfc52-128">Click OK.</span></span>
14. <span data-ttu-id="dfc52-129">انقر فوق تحرير لإدخال رقم شارة لعامل تسجيل الوقت الجديد.</span><span class="sxs-lookup"><span data-stu-id="dfc52-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="dfc52-130">في الحقل "معرف الشارة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dfc52-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="dfc52-131">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="dfc52-131">Click Save.</span></span>
17. <span data-ttu-id="dfc52-132">استخدم الاختصار SaveRecord.</span><span class="sxs-lookup"><span data-stu-id="dfc52-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="dfc52-133">قم بإغلاق صفحة التفاصيل العامل.</span><span class="sxs-lookup"><span data-stu-id="dfc52-133">Close the worker details page.</span></span>
19. <span data-ttu-id="dfc52-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dfc52-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="dfc52-135">تعيين عامل إلى مجموعة الأجهزة.</span><span class="sxs-lookup"><span data-stu-id="dfc52-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="dfc52-136">انتقل إلى التحكم بالإنتاج > الإعداد > ‏‫التنفيذ التصنيعي‬ > ‏‫تكوين بطاقة وظيفة للأجهزة.</span><span class="sxs-lookup"><span data-stu-id="dfc52-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="dfc52-137">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="dfc52-137">Click Add.</span></span>
3. <span data-ttu-id="dfc52-138">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="dfc52-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="dfc52-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="dfc52-139">Click OK.</span></span>
5. <span data-ttu-id="dfc52-140">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="dfc52-140">Click Edit.</span></span>
6. <span data-ttu-id="dfc52-141">في حقل وحدة الإنتاج، يمكنك تعيين عامل التصفية الافتراضي للعامل.</span><span class="sxs-lookup"><span data-stu-id="dfc52-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="dfc52-142">وهذا يضمن أن لا يتم عرض إلا وظائف الإنتاج لوحدة الإنتاج المحددة عند قيام العامل بتسجيل الدخول إلى الجهاز.</span><span class="sxs-lookup"><span data-stu-id="dfc52-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="dfc52-143">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dfc52-143">Close the page.</span></span>

