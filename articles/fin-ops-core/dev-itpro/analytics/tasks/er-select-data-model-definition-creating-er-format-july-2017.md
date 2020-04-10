---
title: تحديد تعريفات نماذج البيانات عندما تنشئ التنسيقات
description: لإكمال الخطوات في هذا الإجراء، يجب أولاً إكمال الإجراء "التقارير الإلكترونية - إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 374c31b5ea9160fba773e82f658e8de05c67cab4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143236"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="2ec53-103">تحديد تعريفات نماذج البيانات عندما تنشئ التنسيقات</span><span class="sxs-lookup"><span data-stu-id="2ec53-103">Select data model definitions when you create formats</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ec53-104">لإكمال الخطوات في هذا الإجراء، يجب أولاً إكمال الإجراء "التقارير الإلكترونية - إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="2ec53-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="2ec53-105">يُظهر هذا الإجراء كيف يمكن تحديد العنصر الجذر للنموذج كتعريف نموذج بيانات لإدراج تنسيق التقارير الإلكترونية المصمم لإنشاء المستندات الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2ec53-105">This procedure shows how a model's root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="2ec53-106">في هذا الإجراء، ستقوم بإضافة تنسيق تقارير إلكترونية جديدة لشركة نموذجية، وهي Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="2ec53-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="2ec53-107">تم تخصيص هذا الإجراء للمستخدمين الذين تم تعيين دور مسؤول النظام أو مطور التقارير الإلكترونية لهم.</span><span class="sxs-lookup"><span data-stu-id="2ec53-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="2ec53-108">يمكن إتمام الخطوات باستخدام أي مجموعة بيانات.</span><span class="sxs-lookup"><span data-stu-id="2ec53-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="2ec53-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="2ec53-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="2ec53-110">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="2ec53-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="2ec53-111">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء، "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="2ec53-111">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="2ec53-112">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="2ec53-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="2ec53-113">إضافة تكوين نموذج بيانات جديد للتقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2ec53-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="2ec53-114">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="2ec53-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="2ec53-115">إننا نضيف تكوين نموذج جديد للتقارير الإلكترونية يحتوي على نموذج بيانات تم تصميمه لكي يتم استخدامه كمصدر بيانات لإنشاء التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2ec53-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="2ec53-116">في الحقل "الاسم"، اكتب "نموذج الدفع (وهمي)".</span><span class="sxs-lookup"><span data-stu-id="2ec53-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="2ec53-117">نموذج الدفع (وهمي)</span><span class="sxs-lookup"><span data-stu-id="2ec53-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="2ec53-118">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="2ec53-118">Click Create configuration.</span></span>
4. <span data-ttu-id="2ec53-119">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="2ec53-119">Click Designer.</span></span>
    * <span data-ttu-id="2ec53-120">افتح مصمم التقارير الإلكترونية لتحديد بنية نموذج البيانات لهذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="2ec53-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="2ec53-121">لنفترض أننا نصمم نموذج البيانات لمجال أعمال المدفوعات لدعم طريقتي دفع -تحويل الائتمان والخصم المباشر.</span><span class="sxs-lookup"><span data-stu-id="2ec53-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="2ec53-122">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="2ec53-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="2ec53-123">في الحقل "الاسم، اكتب "المدفوعات – تحويل الائتمان‬".</span><span class="sxs-lookup"><span data-stu-id="2ec53-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="2ec53-124">المدفوعات – تحويل الائتمان</span><span class="sxs-lookup"><span data-stu-id="2ec53-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="2ec53-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2ec53-125">Click Add.</span></span>
8. <span data-ttu-id="2ec53-126">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="2ec53-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="2ec53-127">في الحقل "عقدة جديدة كـ‬"، أدخل "جذر النموذج‬".</span><span class="sxs-lookup"><span data-stu-id="2ec53-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="2ec53-128">في الحقل "الاسم، اكتب "المدفوعات – الخصم المباشر‬".</span><span class="sxs-lookup"><span data-stu-id="2ec53-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="2ec53-129">المدفوعات – الخصم المباشر</span><span class="sxs-lookup"><span data-stu-id="2ec53-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="2ec53-130">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2ec53-130">Click Add.</span></span>
12. <span data-ttu-id="2ec53-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="2ec53-131">Click Save.</span></span>
13. <span data-ttu-id="2ec53-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ec53-132">Close the page.</span></span>
14. <span data-ttu-id="2ec53-133">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="2ec53-133">Click Change status.</span></span>
    * <span data-ttu-id="2ec53-134">أنجز إصدار المسودة للنموذج لجعله متاحًا في تعيينات وتنسيقات النموذج الجديد.</span><span class="sxs-lookup"><span data-stu-id="2ec53-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="2ec53-135">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="2ec53-135">Click Complete.</span></span>
16. <span data-ttu-id="2ec53-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2ec53-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="2ec53-137">بدء إدخال تكوين التنسيق الجديد للتقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2ec53-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="2ec53-138">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="2ec53-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="2ec53-139">في الحقل "جديد"، أدخل "التنسيق استنادًا إلى نموذج الدفع الخاص بنموذج البيانات (وهمي)".</span><span class="sxs-lookup"><span data-stu-id="2ec53-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="2ec53-140">في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2ec53-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="2ec53-141">لاحظ أن كافة عناصر الجذر في نموذج البيانات المحدد متاحة حاليًا للتحديد كتعريف نموذج بيانات.</span><span class="sxs-lookup"><span data-stu-id="2ec53-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="2ec53-142">يمكنك متابعة تصميم تنسيقك باستخدام أي من العناصر الجذر المطلوبة لنموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="2ec53-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="2ec53-143">لا يمنعك تعيين نموذج مفقود لعنصر الجذر المحدد من المتابعة.</span><span class="sxs-lookup"><span data-stu-id="2ec53-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="2ec53-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ec53-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="2ec53-145">إضافة تكوين تعيين نموذج جديد للتقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2ec53-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="2ec53-146">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="2ec53-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="2ec53-147">في الحقل "جديد"، أدخل "تعيين النموذج استنادًا إلى نموذج الدفع الخاص بنموذج البيانات (وهمي)".</span><span class="sxs-lookup"><span data-stu-id="2ec53-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="2ec53-148">في الحقل "الاسم"، اكتب "تعيينات نموذج الدفع (وهمية)‬".</span><span class="sxs-lookup"><span data-stu-id="2ec53-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="2ec53-149">تعيينات نموذج الدفع (وهمية)</span><span class="sxs-lookup"><span data-stu-id="2ec53-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="2ec53-150">في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2ec53-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="2ec53-151">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="2ec53-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="2ec53-152">تصميم تعيينات نموذج التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2ec53-152">Design ER model mappings</span></span>
1. <span data-ttu-id="2ec53-153">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="2ec53-153">Click Designer.</span></span>
    * <span data-ttu-id="2ec53-154">استخدم مصمم التقارير الإلكترونية لتحديد تعيينات النموذج للعناصر الجذر المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2ec53-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="2ec53-155">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="2ec53-155">Click Designer.</span></span>
    * <span data-ttu-id="2ec53-156">قم بمحاكاة إعداد تعيين النموذج المحدد للعنصر الجذر للنموذج المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ec53-156">Simulate setting of selected model mapping for the selected model's root item.</span></span>  
3. <span data-ttu-id="2ec53-157">في الشجرة، حدد "Dynamics 365 for Operations\سجلات الجدول".</span><span class="sxs-lookup"><span data-stu-id="2ec53-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="2ec53-158">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="2ec53-158">Click Add root.</span></span>
5. <span data-ttu-id="2ec53-159">في الحقل "الاسم"، اكتب "دفتر الأستاذ".</span><span class="sxs-lookup"><span data-stu-id="2ec53-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="2ec53-160">في الحقل "الجدول"، اكتب 'LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="2ec53-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="2ec53-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="2ec53-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="2ec53-162">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2ec53-162">Click OK.</span></span>
8. <span data-ttu-id="2ec53-163">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="2ec53-163">Click Save.</span></span>
9. <span data-ttu-id="2ec53-164">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ec53-164">Close the page.</span></span>
10. <span data-ttu-id="2ec53-165">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ec53-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="2ec53-166">بدء إدخال تكوين تنسيق آخر جديد للتقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2ec53-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="2ec53-167">في الشجرة، حدد "نموذج الدفع (وهمي)‬".</span><span class="sxs-lookup"><span data-stu-id="2ec53-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="2ec53-168">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="2ec53-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="2ec53-169">في الحقل "جديد"، أدخل "التنسيق استنادًا إلى نموذج الدفع الخاص بنموذج البيانات (وهمي)".</span><span class="sxs-lookup"><span data-stu-id="2ec53-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="2ec53-170">في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2ec53-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="2ec53-171">لاحظ أنه يتوفر الآن عنصر جذر واحد فقط لتعيينه إلى مصادر بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="2ec53-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="2ec53-172">عندما يتم تقديم تعيين نموذج واحد على الأقل، يمكن تحديد فقط العناصر الجذر للنموذج التي تم تعيينها إلى مصادر بيانات التطبيق كتعريف نموذج بينما تتم إضافة تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2ec53-172">When at least one model mapping is introduced, only the model's root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="2ec53-173">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ec53-173">Close the page.</span></span>

