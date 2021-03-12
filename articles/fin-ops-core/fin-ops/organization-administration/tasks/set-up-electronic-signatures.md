---
title: إعداد التوقيعات الإلكترونية
description: استخدم هذا الإجراء لإعداد التواقيع الإلكترونية.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 314f48fcac32793c96466ee807d5685e596193b1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796648"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="b379b-103">إعداد التوقيعات الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b379b-103">Set up electronic signatures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b379b-104">استخدم هذا الإجراء لإعداد التواقيع الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b379b-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="b379b-105">ويؤكد التوقيع الإلكتروني هوية الشخص الذي يكون على وشك البدء في عملية حساب أو الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="b379b-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="b379b-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DAT.</span><span class="sxs-lookup"><span data-stu-id="b379b-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="b379b-107">تمكين مفتاح تكوين التوقيع الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="b379b-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="b379b-108">انتقل إلى إدارة النظام > الإعداد > تكوين الترخيص.</span><span class="sxs-lookup"><span data-stu-id="b379b-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="b379b-109">في الشجرة، قم بتوسيع ''الإدارة".</span><span class="sxs-lookup"><span data-stu-id="b379b-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="b379b-110">تحقق من تحديد خانة الاختيار "التوقيع الإلكتروني".</span><span class="sxs-lookup"><span data-stu-id="b379b-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="b379b-111">إذا لم يتم تحديد خانة الاختيار" التوقيع الإلكتروني"، يجب تمكين وضع الصيانة.</span><span class="sxs-lookup"><span data-stu-id="b379b-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="b379b-112">يمكن تمكين وضع الصيانة في هذه البيئة عن طريق تشغيل وظيفة الصيانة من Lifecycle Services أو باستخدام أداة Deployment.Setup محليًا.</span><span class="sxs-lookup"><span data-stu-id="b379b-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="b379b-113">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b379b-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="b379b-114">إعداد محددات التوقيع الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="b379b-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="b379b-115">انتقل إلى إدارة المؤسسة > الإعداد > التوقيع الإلكتروني > معلمات التوقيع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="b379b-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="b379b-116">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="b379b-116">Click Edit.</span></span>
3. <span data-ttu-id="b379b-117">في الحقل "إشعار"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b379b-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="b379b-118">أدخل الإشعار الذي سيتلقاه الموقعون عندما يكون التوقيع مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="b379b-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="b379b-119">يمكنك إدخال أي نص.</span><span class="sxs-lookup"><span data-stu-id="b379b-119">You can enter any text.</span></span> <span data-ttu-id="b379b-120">عادةً ما يقوم هذا النص بإخبار المستخدم بالمقصود بتوقيع مستند إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="b379b-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="b379b-121">إذا أردت إدخال نص الإشعار بلغات إضافية، فانقر فوق الزر "الترجمات".</span><span class="sxs-lookup"><span data-stu-id="b379b-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="b379b-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b379b-122">Click Save.</span></span>
5. <span data-ttu-id="b379b-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b379b-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="b379b-124">إعداد أكواد الأسباب للتوقيعات الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b379b-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="b379b-125">انتقل إلى إدارة المؤسسة > الإعداد > التوقيع الإلكتروني > رموز أسباب التوقيع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="b379b-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="b379b-126">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b379b-126">Click New.</span></span>
    * <span data-ttu-id="b379b-127">يجب عليك إعداد أكواد سبب قبل استخدام التوقيعات الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b379b-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="b379b-128">يعد كود السبب الصالح مطلوبًا عند توقيع مستند.</span><span class="sxs-lookup"><span data-stu-id="b379b-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="b379b-129">يقوم الموقع بتحديد كود سبب لتوضيح الغرض من التوقيع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="b379b-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="b379b-130">على سبيل المثال، يمكن استخدام كود السبب للغشارة إلى الاعتماد القانوني.</span><span class="sxs-lookup"><span data-stu-id="b379b-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="b379b-131">في الحقل "رمز السبب"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b379b-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="b379b-132">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b379b-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b379b-133">أدخل رموز الأسباب الإضافية، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="b379b-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="b379b-134">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b379b-134">Click Save.</span></span>
6. <span data-ttu-id="b379b-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b379b-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="b379b-136">طلب تواقيع إلكترونية لعمليات موجودة</span><span class="sxs-lookup"><span data-stu-id="b379b-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="b379b-137">انتقل إلى إدارة المؤسسة > الإعداد > التوقيع الإلكتروني > متطلبات التوقيع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="b379b-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="b379b-138">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b379b-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b379b-139">حدد عملية تتطلب تواقيع إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b379b-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="b379b-140">قم بتحديد خانة الاختيار "التوقيع" أو إلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="b379b-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="b379b-141">كرر هذه الخطوات لكل عملية تتطلب التواقيع الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b379b-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="b379b-142">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b379b-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="b379b-143">إنشاء متطلب مخصص للتواقيع الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b379b-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="b379b-144">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b379b-144">Click New.</span></span>
2. <span data-ttu-id="b379b-145">قم بتحديد خانة الاختيار "التوقيع" أو إلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="b379b-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="b379b-146">في الحقل "الاسم" أدخل اسمًا للعملية التي تتطلب تواقيع إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b379b-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="b379b-147">في الحقل "الجدول"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="b379b-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b379b-148">في القائمة، ابحث عن الجدول المخزنة فيه البيانات التي يجب توقيعها وحدده.</span><span class="sxs-lookup"><span data-stu-id="b379b-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="b379b-149">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b379b-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b379b-150">في الحقل "اسم الحقل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="b379b-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b379b-151">في القائمة، ابحث عن الحقل في الجدول المراد رصده وحدده.</span><span class="sxs-lookup"><span data-stu-id="b379b-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="b379b-152">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b379b-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b379b-153">حدد الوقت الذي يكون فيه التوقيع مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="b379b-153">Specify when a signature is required.</span></span>     <span data-ttu-id="b379b-154">حدد دائمًا إذا كان التوقيع مطلوبًا عند تغيير البيانات في الحقل.</span><span class="sxs-lookup"><span data-stu-id="b379b-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="b379b-155">حدد فقط إذا كان التوقيع مطلوبًا فقط بموجب شروط معينة.‬</span><span class="sxs-lookup"><span data-stu-id="b379b-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="b379b-156">إذا حددت "فقط"، فيجب عليك أن تحدد أيضًا أحد الخيارات التالية: "عند إدراج سجل" أو "عند تحديث سجل" أو "عند حذف سجل".‬</span><span class="sxs-lookup"><span data-stu-id="b379b-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="b379b-157">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b379b-157">Click Save.</span></span>
11. <span data-ttu-id="b379b-158">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b379b-158">Close the page.</span></span>

