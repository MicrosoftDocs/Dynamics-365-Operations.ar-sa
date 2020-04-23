---
title: تكوين عامل باستخدام جهاز وظيفة محمول
description: يشرح هذا الموضوع كيفية تعيين الأدوار الصحيحة إلى حساب المستخدم الخاص بأحد العاملين، ثم بتمكين العامل للقيام بتسجيلات صالة الإنتاج‬.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1086a88c341b95d6af03adc81c4e3e5d76adc69
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210193"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="42f30-103">تكوين عامل باستخدام جهاز وظيفة محمول</span><span class="sxs-lookup"><span data-stu-id="42f30-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42f30-104">يشرح هذا الموضوع كيفية تعيين الأدوار الصحيحة إلى حساب المستخدم الخاص بأحد العاملين، ثم بتمكين العامل للقيام بتسجيلات صالة الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="42f30-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="42f30-105">التحقق من تعيين دور معين للعامل</span><span class="sxs-lookup"><span data-stu-id="42f30-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="42f30-106">لهذا المثال، تحقق من تعيين دور عامل تشغيل الجهاز للمستخدم "SHANNON" قبل تكوين حساب العامل.</span><span class="sxs-lookup"><span data-stu-id="42f30-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="42f30-107">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة النظام > المستخدمون > المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="42f30-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="42f30-108">ابحث عن مستخدم في عامل التصفية السريع.</span><span class="sxs-lookup"><span data-stu-id="42f30-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="42f30-109">في هذا المثال، أدخل `shannon`.</span><span class="sxs-lookup"><span data-stu-id="42f30-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="42f30-110">حدد الارتباط في العمود‏‎ **معرف المستخدم** لحساب المستخدم الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="42f30-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="42f30-111">في شجرة **أدوار المستخدم**، حدد **الأدوار > عامل تشغيل الجهاز**.</span><span class="sxs-lookup"><span data-stu-id="42f30-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="42f30-112">أغلق الصفحتين **تفاصيل‏‎ المستخدم** و**المستخدمون** للعودة إلى الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="42f30-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="42f30-113">تكوين حساب العامل</span><span class="sxs-lookup"><span data-stu-id="42f30-113">Configure worker account</span></span>
1. <span data-ttu-id="42f30-114">انتقل إلى **جزء التنقل > الوحدات النمطية > الموارد‏‎ البشرية > العاملون > العاملون**.</span><span class="sxs-lookup"><span data-stu-id="42f30-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="42f30-115">ابحث عن مستخدم في عامل التصفية السريع.</span><span class="sxs-lookup"><span data-stu-id="42f30-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="42f30-116">في هذا المثال، أدخل `shannon`.</span><span class="sxs-lookup"><span data-stu-id="42f30-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="42f30-117">حدد الارتباط في العمود‏‎ **الاسم** لحساب المستخدم الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="42f30-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="42f30-118">حدد علامة‏‎ التبويب **تسجيل الوقت**.</span><span class="sxs-lookup"><span data-stu-id="42f30-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="42f30-119">حدد **التنشيط على وحدات التسجيل الطرفية‬**.</span><span class="sxs-lookup"><span data-stu-id="42f30-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="42f30-120">أدخل القيم أو حددها في الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="42f30-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="42f30-121">**مجموعة الحساب**</span><span class="sxs-lookup"><span data-stu-id="42f30-121">**Calculation group**</span></span>  
    - <span data-ttu-id="42f30-122">**مجموعة الحساب الافتراضية**</span><span class="sxs-lookup"><span data-stu-id="42f30-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="42f30-123">**مجموعة الموافقة**</span><span class="sxs-lookup"><span data-stu-id="42f30-123">**Approval group**</span></span>  
    - <span data-ttu-id="42f30-124">**ملف تعريف قياسي**</span><span class="sxs-lookup"><span data-stu-id="42f30-124">**Standard profile**</span></span>  
    - <span data-ttu-id="42f30-125">**مجموعة ملف التعريف**</span><span class="sxs-lookup"><span data-stu-id="42f30-125">**Profile group**</span></span>  

7. <span data-ttu-id="42f30-126">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="42f30-126">Select **OK**.</span></span>
8. <span data-ttu-id="42f30-127">حدد **تحرير** لإدخال رقم شارة لعامل تسجيل الوقت الجديد.</span><span class="sxs-lookup"><span data-stu-id="42f30-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="42f30-128">في حقل **معرف الشارة**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="42f30-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="42f30-129">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="42f30-129">Select **Save**.</span></span>
10. <span data-ttu-id="42f30-130">أغلق الصفحتين **تفاصيل العامل** و**العاملون**.</span><span class="sxs-lookup"><span data-stu-id="42f30-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="42f30-131">تعيين عامل إلى مجموعة أجهزة</span><span class="sxs-lookup"><span data-stu-id="42f30-131">Assign worker to device group</span></span>
1. <span data-ttu-id="42f30-132">انتقل إلى **التحكم بالإنتاج > الإعداد > ‏‫تنفيذ التصنيع‬ > ‏‫تكوين بطاقة وظيفة للأجهزة**.</span><span class="sxs-lookup"><span data-stu-id="42f30-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="42f30-133">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="42f30-133">Select **Add**.</span></span>
3. <span data-ttu-id="42f30-134">في القائمة، حدد العامل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="42f30-134">In the list, select the desired worker.</span></span> <span data-ttu-id="42f30-135">بالنسبة إلى هذا المثال، حدد **SHANNON‎**.</span><span class="sxs-lookup"><span data-stu-id="42f30-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="42f30-136">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="42f30-136">Select **OK**.</span></span>
5. <span data-ttu-id="42f30-137">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="42f30-137">Select **Edit**.</span></span>
6. <span data-ttu-id="42f30-138">في حقل **وحدة الإنتاج**، يمكنك تعيين عامل التصفية الافتراضي للعامل.</span><span class="sxs-lookup"><span data-stu-id="42f30-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="42f30-139">وهذا يضمن أن لا يتم عرض إلا وظائف الإنتاج لوحدة الإنتاج المحددة عند قيام العامل بتسجيل الدخول إلى الجهاز.</span><span class="sxs-lookup"><span data-stu-id="42f30-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="42f30-140">أدخل القيمة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="42f30-140">Enter the desired value.</span></span>
7. <span data-ttu-id="42f30-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="42f30-141">Close the page.</span></span>

