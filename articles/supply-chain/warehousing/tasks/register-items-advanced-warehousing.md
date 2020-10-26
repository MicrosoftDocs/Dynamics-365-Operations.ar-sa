---
title: تسجيل أصناف لصنف ممكَّن للتخزين المتقدم باستخدام دفتر يومية وصول الصنف
description: يوضح هذا الإجراء كيفية تسجيل الأصناف باستخدام دفتر يومية وصول الصنف عند استخدام عمليات إدارة المستودع المتقدمة.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea8b5e03282aa21aa9dfa486b1deaced6af4601c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976914"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="ffdea-103">تسجيل أصناف لصنف ممكَّن للتخزين المتقدم باستخدام دفتر يومية وصول الصنف</span><span class="sxs-lookup"><span data-stu-id="ffdea-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffdea-104">يوضح هذا الإجراء كيفية تسجيل الأصناف باستخدام دفتر يومية وصول الصنف عند استخدام عمليات إدارة المستودع المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="ffdea-105">يتم ذلك عادة عن طريق موظف الاستقبال.</span><span class="sxs-lookup"><span data-stu-id="ffdea-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="ffdea-106">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="ffdea-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="ffdea-107">تحتاج للحصول على أمر شراء مؤكد ببند أمر شراء مفتوح قبل تشغيل هذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="ffdea-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="ffdea-108">يجب أن يكون الصنف في البند مخزّنًا، ويجب ألا يستخدم متغيرات المنتج وألا تكون له أبعاد تعقب.</span><span class="sxs-lookup"><span data-stu-id="ffdea-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="ffdea-109">يجب ربط الصنف بمجموعة أبعاد تخزين تم تمكين إدارة مستودع تخزين لها.</span><span class="sxs-lookup"><span data-stu-id="ffdea-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="ffdea-110">يجب تمكين المستودع الذي يتم استخدامه لعمليات إدارة المستودع ويجب أن يكون الموقع الذي تستخدمَه يتم التحكم به بواسطة لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="ffdea-110">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="ffdea-111">إذا كنت تستخدم USMF، يمكنك استخدام حساب الشركة 1001، والمستودع 51، والصنف M9200 لإنشاء أمر الشراء الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="ffdea-111">If you're using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="ffdea-112">قم بتدوين رقم أمر الشراء التي تقوم بإنشائه، وقد أيضًا بتدوين رقم الصنف والموقع الذي استخدمتَه لأمر الشراء الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="ffdea-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="ffdea-113">إنشاء رأس دفتر يومية وصول صنف</span><span class="sxs-lookup"><span data-stu-id="ffdea-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="ffdea-114">انتقل إلى "وصول الصنف".</span><span class="sxs-lookup"><span data-stu-id="ffdea-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="ffdea-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ffdea-115">Click New.</span></span>
3. <span data-ttu-id="ffdea-116">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="ffdea-117">إذا كنت تستخدم USMF، فيمكنك كتابة WHS.</span><span class="sxs-lookup"><span data-stu-id="ffdea-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="ffdea-118">أما إذا كنت تستخدم بيانات أخرى، فيجب أن تتوفر الخصائص التالية في دفتر اليومية الذي تختار اسمه: يجب تعيين "التحقق من موقع الانتقاء‬" إلى "لا" ويجب تعيين "إدارة العزل‬" إلى "لا".</span><span class="sxs-lookup"><span data-stu-id="ffdea-118">If you're using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="ffdea-119">في الحقل "الرقم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="ffdea-120">في الحقل "الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="ffdea-121">حدد الموقع الذي استخدمتَه لبند أمر الشراء الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="ffdea-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="ffdea-122">وسيعمل هذا الموقع كقيمة افتراضية تنطبق بشكل افتراضي على جميع البنود المضمنة في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="ffdea-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="ffdea-123">إذا استخدمتَ المستودع 51 في شركة USMF، فاختر الموقع 5.</span><span class="sxs-lookup"><span data-stu-id="ffdea-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="ffdea-124">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="ffdea-125">حدد مستودعًا صالحًا للموقع الذي قمتَ بتحديده.</span><span class="sxs-lookup"><span data-stu-id="ffdea-125">Select a valid warehouse for the site that you've selected.</span></span> <span data-ttu-id="ffdea-126">وسيعمل هذا الموقع كقيمة افتراضية تنطبق بشكل افتراضي على جميع البنود المضمنة في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="ffdea-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="ffdea-127">إذا كنت تستخدم القيم المثال في شركة USMF، فحدد 51.</span><span class="sxs-lookup"><span data-stu-id="ffdea-127">If you're using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="ffdea-128">في الحقل "الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="ffdea-129">حدد موقعًا صالحًا في المستودع الذي قمتَ بتحديده.</span><span class="sxs-lookup"><span data-stu-id="ffdea-129">Select a valid location in the warehouse that you've selected.</span></span> <span data-ttu-id="ffdea-130">يجب أن يكون الموقع مرتبطًا بملف تعريف يتم التحكم به بواسطة لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="ffdea-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="ffdea-131">وسيعمل هذا الموقع كقيمة افتراضية تنطبق بشكل افتراضي على جميع البنود المضمنة في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="ffdea-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="ffdea-132">إذا كنت تستخدم القيم المثال في USMF، فحدد مجمع-008.</span><span class="sxs-lookup"><span data-stu-id="ffdea-132">If you're using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="ffdea-133">انقر بزر الماوس الأيمن فوق سهم القائمة المنسدلة في الحقل "لوحة الترخيص"، ثم حدد "عرض التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="ffdea-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="ffdea-134">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ffdea-134">Click New.</span></span>
10. <span data-ttu-id="ffdea-135">في الحقل "‏لوحة الترخيص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="ffdea-136">قم بتدوين ملاحظة بالقيمة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="ffdea-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ffdea-137">Click Save.</span></span>
12. <span data-ttu-id="ffdea-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-138">Close the page.</span></span>
13. <span data-ttu-id="ffdea-139">في الحقل "‏لوحة الترخيص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="ffdea-140">أدخل قيمة لوحة الترخيص التي قمت بإنشائها للتو.</span><span class="sxs-lookup"><span data-stu-id="ffdea-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="ffdea-141">وسيعمل هذا الموقع كقيمة افتراضية تنطبق بشكل افتراضي على جميع البنود المضمنة في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="ffdea-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="ffdea-142">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ffdea-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="ffdea-143">إضافة بند</span><span class="sxs-lookup"><span data-stu-id="ffdea-143">Add a line</span></span>
1. <span data-ttu-id="ffdea-144">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="ffdea-144">Click Add line.</span></span>
2. <span data-ttu-id="ffdea-145">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="ffdea-146">أدخل رقم الصنف الذي استخدمتَه في بند أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="ffdea-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="ffdea-147">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="ffdea-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="ffdea-148">أدخل الكمية التي تريد تسجيلها.</span><span class="sxs-lookup"><span data-stu-id="ffdea-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="ffdea-149">يحدد الحقل "التاريخ" التاريخ الذي سيتم فيه تسجيل الكمية المتاحة من هذا الصنف في المخزون.</span><span class="sxs-lookup"><span data-stu-id="ffdea-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="ffdea-150">سيتم ملء معرف الشحنة بواسطة النظام إذا أمكن تعريفه بشكل فريد من المعلومات المقدمة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="ffdea-151">وإلا ستحتاجُ لإضافة هذا المعرف يدوياً.</span><span class="sxs-lookup"><span data-stu-id="ffdea-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="ffdea-152">هذا حقل إلزامي يربط هذا التسجيل ببند مستند مصدر محدد.</span><span class="sxs-lookup"><span data-stu-id="ffdea-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="ffdea-153">إكمال التسجيل</span><span class="sxs-lookup"><span data-stu-id="ffdea-153">Complete the registration</span></span>
1. <span data-ttu-id="ffdea-154">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="ffdea-154">Click Validate.</span></span>
    * <span data-ttu-id="ffdea-155">يتحقق هذا من دفتر اليومية الجاهز للترحيل.</span><span class="sxs-lookup"><span data-stu-id="ffdea-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="ffdea-156">إذا فشلت عملية التحقق، فستحتاجُ لتصحيح الأخطاء قبل أن تتمكن من ترحيل دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="ffdea-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="ffdea-157">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ffdea-157">Click OK.</span></span>
    * <span data-ttu-id="ffdea-158">بعد النقر فوق "موافق"، تحقق من الرسالة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="ffdea-159">من المفترض أن تظهر رسالة تفيد بأن دفتر اليومية صحيح.</span><span class="sxs-lookup"><span data-stu-id="ffdea-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="ffdea-160">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="ffdea-160">Click Post.</span></span>
4. <span data-ttu-id="ffdea-161">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ffdea-161">Click OK.</span></span>
    * <span data-ttu-id="ffdea-162">بعد النقر فوق "موافق"، تحقق من شريط الرسائل.</span><span class="sxs-lookup"><span data-stu-id="ffdea-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="ffdea-163">من المفترض أن تظهر رسالة تفيد باكتمال العملية.</span><span class="sxs-lookup"><span data-stu-id="ffdea-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="ffdea-164">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ffdea-164">Close the page.</span></span>

