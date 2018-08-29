---
title: "إعداد تسجيل الدخول الموسع لكل من MPOS وCloud POS"
description: "يتناول هذا الموضوع الخيارات الخاصة بإعداد تسجيل الدخول الموسع لنقاط بيع المجموعة ونقاط البيع الحديثة للبيع بالتجزئة (MPOS)."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 4e3f8042871e5e423b559bb0e0dae0006af00194
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a><span data-ttu-id="7ba4d-103">إعداد تسجيل الدخول الموسع لكل من MPOS وCloud POS</span><span class="sxs-lookup"><span data-stu-id="7ba4d-103">Set up extended logon functionality for MPOS and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7ba4d-104">يتناول هذا الموضوع الخيارات الخاصة بإعداد تسجيل الدخول الموسع لنقاط بيع المجموعة ونقاط البيع الحديثة للبيع بالتجزئة (MPOS).</span><span class="sxs-lookup"><span data-stu-id="7ba4d-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

## <a name="setting-up-extended-logon"></a><span data-ttu-id="7ba4d-105">إعداد تسجيل الدخول الموسع</span><span class="sxs-lookup"><span data-stu-id="7ba4d-105">Setting up extended logon</span></span>

<span data-ttu-id="7ba4d-106">يمكنك العثور على إعداد أقنعة الرمز الشريطي في **البيع بالتجزئة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع‬** &gt; **ملفات تعريف نقطة البيع‬** &gt; **ملفات تعريف الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-106">You can find the setup for bar code masks at **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="7ba4d-107">تتضمن علامة التبويب السريعة **الوظائف** الخيارات التالية المتعلقة بتسجيل دخول موسع.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="7ba4d-108">تسجيل دخول الكود الشريطي للفريق</span><span class="sxs-lookup"><span data-stu-id="7ba4d-108">Staff bar code logon</span></span>

<span data-ttu-id="7ba4d-109">عند تمكين خيار **تسجيل دخول الرمز الشريطي للموظفين**، يستطيع العاملون الذين لديهم تسجيل دخول موسع معين إلى بيانات اعتماد نقطة البيع (POS) تسجيل الدخول باستخدام رمز شريطي.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="7ba4d-110">يتطلب تسجيل دخول الكود الشريطي للفريق وجود كلمة مرور</span><span class="sxs-lookup"><span data-stu-id="7ba4d-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="7ba4d-111">عندما يتم تمكين خيار **يتطلب تسجيل دخول الرمز الشريطي للموظفين كلمة مرور**، يحدد تسجيل دخول الرمز الشريطي للموظفين العامل الذي يتم تعيينه لتسجيل دخول موسع يتم تقديمه فقط.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="7ba4d-112">لا يزال يجب على العمال إدخال كلمة المرور عند تمكين هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="7ba4d-113">تسجيل دخول بطاقة الفريق</span><span class="sxs-lookup"><span data-stu-id="7ba4d-113">Staff card logon</span></span>

<span data-ttu-id="7ba4d-114">عند تمكين خيار **تسجيل دخول بطاقة الموظفين**، يستطيع العاملون الذين لديهم تسجيل دخول موسع معين إلى بيانات اعتماد نقطة البيع تسجيل الدخول باستخدام شريط مغناطيسي.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="7ba4d-115">يتطلب تسجيل دخول بطاقة الفريق وجود كلمة مرور</span><span class="sxs-lookup"><span data-stu-id="7ba4d-115">Staff card logon requires password</span></span>

<span data-ttu-id="7ba4d-116">عندما يتم تمكين خيار **يتطلب تسجيل دخول بطاقة الموظفين كلمة مرور**، يحدد تسجيل بطاقة الموظفين العامل الذي يتم تعيينه لتسجيل دخول موسع يتم تقديمه فقط.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="7ba4d-117">لا يزال يجب على العمال إدخال كلمة المرور عند تمكين هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-117">Workers must still enter their password when this option is enabled.</span></span>

## <a name="assigning-an-extended-logon"></a><span data-ttu-id="7ba4d-118">تعيين تسجيل دخول موسع</span><span class="sxs-lookup"><span data-stu-id="7ba4d-118">Assigning an extended logon</span></span>

<span data-ttu-id="7ba4d-119">بشكل افتراضي، يستطيع المديرون فقط تعيين تسجيل الدخول الموسع للعاملين.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="7ba4d-120">‏‫لتعيين تسجيل الدخول الموسع، انتقل إلى **‬‏‫تسجيل دخول موسع** ‬‏‫في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="7ba4d-121"> ثم ابحث عن عامل عن طريق إدخال معرف المشغل الخاص به أو بها في حقل البحث.‬</span><span class="sxs-lookup"><span data-stu-id="7ba4d-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="7ba4d-122">حدد العامل، ثم انقر فوق **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="7ba4d-123">في الصفحة التالية، اسحب تسجيل الدخول الموسع أو امسحه لتعيين العامل.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="7ba4d-124">إذا تمت قراءة السحب أو المسح بنجاح، يصبح الزر **موافق**متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="7ba4d-125">انقر فوق **موافق** لحفظ تسجيل الدخول الموسع لهذا العامل.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-125">Click **OK** to save the extended logon for that worker.</span></span>

## <a name="deleting-an-extended-logon"></a><span data-ttu-id="7ba4d-126">حذف تسجيل دخول موسع</span><span class="sxs-lookup"><span data-stu-id="7ba4d-126">Deleting an extended logon</span></span>

<span data-ttu-id="7ba4d-127">لحذف تسجيل الدخول الموسع الذي يتم تعيينه لعامل، ابحث عن العامل باستخدام عملية **تسجيل الدخول الموسع**.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="7ba4d-128">حدد العامل، ثم انقر فوق **إلغاء التعيين**.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="7ba4d-129">تتم إزالة كافة بيانات اعتماد تسجيل الدخول الموسع التي تقترن بهذا العامل.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-129">All extended logon credentials that are associated with that worker are removed.</span></span>

## <a name="extending-extended-logon"></a><span data-ttu-id="7ba4d-130">توسيع تسجيل الدخول الموسع</span><span class="sxs-lookup"><span data-stu-id="7ba4d-130">Extending extended logon</span></span>

<span data-ttu-id="7ba4d-131">يمكن توسيع خدمة تسجيل الدخول لدعم أجهزة تسجيل الدخول الموسع الإضافي، مثل ماسحات الكمبيوتر الكفي.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="7ba4d-132">لمزيد من المعلومات، راجع وثائق قابلية التوسعة لنقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-132">For more information, see the POS extensibility documentation.</span></span>

## <a name="using-extended-logon"></a><span data-ttu-id="7ba4d-133">استخدام تسجيل الدخول الموسع</span><span class="sxs-lookup"><span data-stu-id="7ba4d-133">Using extended logon</span></span>

<span data-ttu-id="7ba4d-134">عندما يتم تكوين تسجيل الدخول الموسع، وقام عامل بتعيين الرمز الشريطي أو الشريط المغناطيسي، يجب على العامل أن يقوم بتمرير البطاقة أو مسحها بينما يتم عرض صفحة تسجيل دخول نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="7ba4d-135">إذا كانت كلمة مرور مطلوبة أيضًا قبل إمكانية متابعة تسجيل الدخول، فإنه تتم مطالبة العامل بإدخال كلمة المرور الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>




