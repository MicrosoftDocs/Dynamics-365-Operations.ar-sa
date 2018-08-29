--- 
title: "تكوين وجهات ‏‫مخرجات التقارير الإلكترونية"
description: "يوضح هذا الإجراء كيفية الإعداد واستخدام وجهات مختلفة لمكونات إخراج التقارير الإلكترونية (ER)، مثل مجلد أو ملف."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 7c84464f426d6bedff092fd918fcabbc35600f3c
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="configure-destinations-for-electronic-reporting-er-output"></a><span data-ttu-id="85d2d-103">تكوين وجهات ‏‫مخرجات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="85d2d-103">Configure destinations for Electronic reporting (ER) output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85d2d-104">يوضح هذا الإجراء كيفية الإعداد واستخدام وجهات مختلفة لمكونات إخراج التقارير الإلكترونية (ER)، مثل مجلد أو ملف.</span><span class="sxs-lookup"><span data-stu-id="85d2d-104">This procedure demonstrates how to set up and use different destinations for Electronic reporting (ER) output components, such as a folder or a file.</span></span> <span data-ttu-id="85d2d-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF.</span><span class="sxs-lookup"><span data-stu-id="85d2d-105">The demo data company used to create this procedure is DEMF.</span></span> <span data-ttu-id="85d2d-106">تُعد ألمانيا بلد/منطقة العنوان الأساسي للكيان القانوني، على الرغم من ذلك، يمكنك استخدام أي كيان قانوني لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="85d2d-106">Germany is the country\region of the legal entity’s primary address, however you can use any legal entity for this procedure.</span></span> 

<span data-ttu-id="85d2d-107">التنسيق المستخدم في هذا المثال هو تحويل الائتمان ISO20022 (DE)، ولكن يمكنك استخدام أي تنسيق قمت باستيراده بالفعل.</span><span class="sxs-lookup"><span data-stu-id="85d2d-107">The format used in this example is ISO20022 Credit transfer, but you can use any format that you have already imported.</span></span> <span data-ttu-id="85d2d-108">لاحظ أن هذا الإجراء عبارة عن مثال لملف واحد وإعداد وجهة واحدة.</span><span class="sxs-lookup"><span data-stu-id="85d2d-108">Note, this procedure is an example of a single file and a single destination setup.</span></span> <span data-ttu-id="85d2d-109">يمكن العثور على مزيد من المعلومات حول إدارة وجهات التقارير الإلكترونية في تعليمات Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="85d2d-109">More information about Electronic reporting destination management can be found in the Dynamics 365 for Finance and Operations Help.</span></span>

1. <span data-ttu-id="85d2d-110">انتقل إلى إدارة المؤسسة > التقارير الإلكترونية > وجهة إعداد التقارير الإلكترونية‬.</span><span class="sxs-lookup"><span data-stu-id="85d2d-110">Go to Organization administration > Electronic reporting > Electronic reporting destination.</span></span>
2. <span data-ttu-id="85d2d-111">انقر فوق "جديد" لإنشاء مجموعة جديدة من وجهات لتنسيق.</span><span class="sxs-lookup"><span data-stu-id="85d2d-111">Click New to create a new set of destinations for a format.</span></span>
3. <span data-ttu-id="85d2d-112">في حقل "المرجع"، حدد التنسيق الذي تريد تكوين الوجهات له.</span><span class="sxs-lookup"><span data-stu-id="85d2d-112">In the Reference field, select a format for which you want to configure destinations.</span></span>
    * <span data-ttu-id="85d2d-113">إذا لم يكن لديك قيمة لتحددها، فهذا يعني أنك لم تقم باستيراد أي تكوينات تنسيق إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85d2d-113">If you don't have a value to select, it means that you have not imported any Electronic reporting format configurations.</span></span> <span data-ttu-id="85d2d-114">يجب استيراد تكوين تنسيق قبل إعداد الوجهات.</span><span class="sxs-lookup"><span data-stu-id="85d2d-114">You must import a format configuration before setting up destinations.</span></span>  
4. <span data-ttu-id="85d2d-115">انقر فوق "جديد" لإنشاء وجهة ملف جديدة.</span><span class="sxs-lookup"><span data-stu-id="85d2d-115">Click New to create a new file destination.</span></span>
    * <span data-ttu-id="85d2d-116">لاحظ أنه يمكنك إنشاء وجهة ملف واحد لكل مكون مخرجات من التنسيق نفسه، مثل مجلد أو ملف.</span><span class="sxs-lookup"><span data-stu-id="85d2d-116">Note, you can create one file destination for each output component of the same format, such as a folder or a file.</span></span> <span data-ttu-id="85d2d-117">ستكون قادرًا على تمكين الوجهات وتعطيلها بشكل منفصل في الإعدادات.</span><span class="sxs-lookup"><span data-stu-id="85d2d-117">You will be able to enable and disable destinations separately in the settings.</span></span>  
5. <span data-ttu-id="85d2d-118">في الحقل "الاسم"، أدخل اسم المستخدم المألوف لمكون المخرجات.</span><span class="sxs-lookup"><span data-stu-id="85d2d-118">In the Name field, enter the user-friendly name of output component.</span></span>
    * <span data-ttu-id="85d2d-119">نوصي باستخدام أسماء ذات معنى، مثل "ملف الدفع" أو "التحكم في التقرير".</span><span class="sxs-lookup"><span data-stu-id="85d2d-119">We recommend that you use meaningful names, such as "Payment file" or "Control report".</span></span> <span data-ttu-id="85d2d-120">سيتم تقديم هذه الأسماء للمستخدمين في وقت تشغيل التكوين جنبًا إلى جنب مع إعدادات الوجهة.</span><span class="sxs-lookup"><span data-stu-id="85d2d-120">These names will be presented to users at configuration runtime along with the destination settings.</span></span>  
6. <span data-ttu-id="85d2d-121">في اسم "الملف"، حدد الملف أو المجلد الخاص بالتنسيق.</span><span class="sxs-lookup"><span data-stu-id="85d2d-121">In the File name, select a file or folder that is specific to the format.</span></span>
7. <span data-ttu-id="85d2d-122">انقر فوق "إعدادات".</span><span class="sxs-lookup"><span data-stu-id="85d2d-122">Click Settings.</span></span>
8. <span data-ttu-id="85d2d-123">حدد "نعم" في الحقل "تمكين".</span><span class="sxs-lookup"><span data-stu-id="85d2d-123">Select Yes in the Enabled field.</span></span>
    * <span data-ttu-id="85d2d-124">تعمل خانة الاختيار "تمكين" على كل علامة تبويب وتعطل كل جهة بشكل منفصل.</span><span class="sxs-lookup"><span data-stu-id="85d2d-124">The Enabled check box on each tab enables and disables each destination separately.</span></span> <span data-ttu-id="85d2d-125">في هذا المثال، ستقوم بتمكين إرسال ملف إخراج إلى متلقي بريد عند إنشاء الملف.</span><span class="sxs-lookup"><span data-stu-id="85d2d-125">In this example, you'll enable sending an output file to a mail recipient when the file is generated.</span></span>  
9. <span data-ttu-id="85d2d-126">انقر فوق "تحرير" لإعداد مستلمي البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="85d2d-126">Click Edit, to set up email recipients.</span></span>
10. <span data-ttu-id="85d2d-127">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="85d2d-127">Click Add.</span></span>
11. <span data-ttu-id="85d2d-128">انقر فوق "بريد إلكتروني خاص بإدارة الطباعة‬".</span><span class="sxs-lookup"><span data-stu-id="85d2d-128">Click Print Management email.</span></span>
12. <span data-ttu-id="85d2d-129">في الحقل "مصدر البريد الإلكتروني"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="85d2d-129">In the Email source  field, select an option.</span></span>
    * <span data-ttu-id="85d2d-130">يمكنك تحديد أنواع مصادر بريد إلكتروني مختلفة، مثل نوع المورّد أو العميل.</span><span class="sxs-lookup"><span data-stu-id="85d2d-130">You can select different email source types, such as a customer or a vendor type.</span></span> <span data-ttu-id="85d2d-131">يحدد هذا نوع الوسيطة التي سيتم إرجاعها بواسطة معادلة حساب البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="85d2d-131">This defines the type of argument that will be returned by the Email source account formula.</span></span> <span data-ttu-id="85d2d-132">تُعد معادلة حساب البريد الإلكتروني, الموضحة في خطوة تالية، المكان حيث سيتم ربط مصدر البريد إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="85d2d-132">The Email source account formula, described in a following step, is the place where you bind an email source.</span></span> <span data-ttu-id="85d2d-133">حدد المود إذا كانت المعادلة ستعود على حساب المورد.</span><span class="sxs-lookup"><span data-stu-id="85d2d-133">Select Vendor if your formula will return a vendor account.</span></span> <span data-ttu-id="85d2d-134">استخدم المورد إذا كنت تستخدم مثال تكوين نقل ائتمان ISO 20022.</span><span class="sxs-lookup"><span data-stu-id="85d2d-134">Use Vendor if you are using the ISO 20022 Credit Transfer configuration example.</span></span>  
13. <span data-ttu-id="85d2d-135">انقر فوق الزر "ربط مصدر البريد الإلكتروني".</span><span class="sxs-lookup"><span data-stu-id="85d2d-135">Click Email source bind button.</span></span>
14. <span data-ttu-id="85d2d-136">في المعادلة، أدخل مرجعًا خاصًا بمستند إلى نوع طرف حددته في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="85d2d-136">In the Formula, enter a document-specific reference to a party type that you selected earlier.</span></span>
    * <span data-ttu-id="85d2d-137">بدلاً من الكتابة، يمكنك العثور على عقدة مصدر بيانات تمثل حساب الطرف، وانقر فوق الزر "إضافة مصدر البيانات" لتحديث المعادلة.</span><span class="sxs-lookup"><span data-stu-id="85d2d-137">Instead of typing, you can find a data source node that represents the party account, and click the Add data source button to update the formula.</span></span> <span data-ttu-id="85d2d-138">على سبيل المثال، إذا كنت تستخدم تكوين تحويل الائتمان ISO 20022، فإن العقدة التي تمثل حساب المورّد هي "$PaymentsForCoveringLetter". Creditor.Identification.SourceID.</span><span class="sxs-lookup"><span data-stu-id="85d2d-138">For example, if you use the ISO 20022 Credit Transfer configuration, the node representing a vendor account is '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID.</span></span> <span data-ttu-id="85d2d-139">وإلا، أدخل أي قيمة سلسلة، مثل "DE-001"، لحفظ المعادلة.</span><span class="sxs-lookup"><span data-stu-id="85d2d-139">Otherwise, enter any string value, such as "DE-001", to save a formula.</span></span>  
15. <span data-ttu-id="85d2d-140">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="85d2d-140">Click Save.</span></span>
16. <span data-ttu-id="85d2d-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="85d2d-141">Close the page.</span></span>
17. <span data-ttu-id="85d2d-142">انقر فوق "تحرير" لتكوين جهة الاتصال للطرف.</span><span class="sxs-lookup"><span data-stu-id="85d2d-142">Click Edit to configure contact details for the party.</span></span>
18. <span data-ttu-id="85d2d-143">حدد "نعم" في الحقل "جهة الاتصال الرئيسية‬".</span><span class="sxs-lookup"><span data-stu-id="85d2d-143">Select Yes in the Primary contact field.</span></span>
    * <span data-ttu-id="85d2d-144">يمكنك استخدام خيارات مختلفة للإشارة إلى نوع جهة الاتصال للطرف التي يجب استخدامها كعنوان بريد إلكتروني لهذه الوجهة.</span><span class="sxs-lookup"><span data-stu-id="85d2d-144">You may use different options to indicate what contact type of the party should be used as an email address for this destination.</span></span> <span data-ttu-id="85d2d-145">نحن نستخدم جهة الاتصال الرئيسية في هذا المثال.</span><span class="sxs-lookup"><span data-stu-id="85d2d-145">We use primary contact in this example.</span></span>  
19. <span data-ttu-id="85d2d-146">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="85d2d-146">Click OK.</span></span>
20. <span data-ttu-id="85d2d-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="85d2d-147">Click OK.</span></span>
21. <span data-ttu-id="85d2d-148">في الحقل "الموضوع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="85d2d-148">In the Subject field, type a value.</span></span>
22. <span data-ttu-id="85d2d-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="85d2d-149">Click OK.</span></span>


