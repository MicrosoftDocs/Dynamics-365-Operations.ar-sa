---
title: نموذج البيانات الخاص بمجال تصميم الإبلاغ الإلكتروني
description: يصف هذا الموضوع كيفيه إنشاء تكوين اعداد التقارير الكترونيه الجديد (ER) الذي يحتوي علي نموذج بيانات لمستندات الدفع الكترونيه.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351c5a6624f7ee912c507a9f74324f4c8f61166b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755024"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="68cc5-103">نموذج البيانات الخاص بمجال تصميم الإبلاغ الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="68cc5-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="68cc5-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على نموذج بيانات لمستندات الدفع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="68cc5-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="68cc5-105">سيتم استخدام نموذج البيانات هذا لاحقًا كمصدر بيانات عند إنشاء تنسيق مستندات الدفع.</span><span class="sxs-lookup"><span data-stu-id="68cc5-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="68cc5-106">في هذا المثال، ستقوم بإنشاء تكوين لشركة عينة، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة كتكوينات ER المشتركة بين الشركات.</span><span class="sxs-lookup"><span data-stu-id="68cc5-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="68cc5-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="68cc5-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="68cc5-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="68cc5-109">حدد موفر التكوين للشركة النموذجية، ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="68cc5-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="68cc5-110">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="68cc5-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="68cc5-111">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="68cc5-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="68cc5-112">ستقوم بإنشاء تكوين يحتوي على نموذج بيانات لمستندات الدفع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="68cc5-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="68cc5-113">سيتم استخدام نموذج البيانات هذا لاحقًا كمصدر بيانات عند إنشاء تنسيق مستندات الدفع.</span><span class="sxs-lookup"><span data-stu-id="68cc5-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="68cc5-114">إنشاء تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="68cc5-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="68cc5-115">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="68cc5-116">في الحقل "الاسم"، اكتب "المدفوعات (نموذج مبسط)".</span><span class="sxs-lookup"><span data-stu-id="68cc5-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="68cc5-117">في حقل "الوصف"، اكتب "تكوين نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="68cc5-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="68cc5-118">يتم تلقائيًا إدخال موفر التكوين النشط هنا.</span><span class="sxs-lookup"><span data-stu-id="68cc5-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="68cc5-119">سيكون هذا الموفر قادرًا على المحافظة على هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="68cc5-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="68cc5-120">باستطاعة موفرين آخرين استخدام هذا التكوين، ولكن لن يكون باستطاعتهم المحافظة عليه.</span><span class="sxs-lookup"><span data-stu-id="68cc5-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="68cc5-121">انقر فوق الزر "إنشاء تكوين" لإكمال مهمة إنشاء التكوين</span><span class="sxs-lookup"><span data-stu-id="68cc5-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="68cc5-122">إنشاء نموذج بيانات</span><span class="sxs-lookup"><span data-stu-id="68cc5-122">Create a data model</span></span>
<span data-ttu-id="68cc5-123">إنك تقوم بإنشاء نموذج بيانات جديد للتكوين المحدد.</span><span class="sxs-lookup"><span data-stu-id="68cc5-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="68cc5-124">سيكون إصدار التكوين بالحالة "مسودة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="68cc5-125">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="68cc5-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="68cc5-126">تعريف بنية طرف مشاركة في عملية الدفع</span><span class="sxs-lookup"><span data-stu-id="68cc5-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="68cc5-127">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="68cc5-128">في حقل "الاسم"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="68cc5-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="68cc5-129">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-129">Click Add.</span></span>
4. <span data-ttu-id="68cc5-130">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="68cc5-131">في الحقل "الاسم"، اكتب "الاسم".</span><span class="sxs-lookup"><span data-stu-id="68cc5-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="68cc5-132">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="68cc5-133">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-133">Click Add.</span></span>
8. <span data-ttu-id="68cc5-134">في الحقل "بحث"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="68cc5-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="68cc5-135">انقر فوق "بحث عن السابق".</span><span class="sxs-lookup"><span data-stu-id="68cc5-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="68cc5-136">تعريف بنية البنك لهذا النموذج</span><span class="sxs-lookup"><span data-stu-id="68cc5-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="68cc5-137">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="68cc5-138">في الحقل "الاسم"، اكتب "الوكيل".</span><span class="sxs-lookup"><span data-stu-id="68cc5-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="68cc5-139">في الحقل "نوع الصنف"، حدد "سجل".</span><span class="sxs-lookup"><span data-stu-id="68cc5-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="68cc5-140">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-140">Click Add.</span></span>
5. <span data-ttu-id="68cc5-141">في حقل "الوصف"، أدخل "مؤسسة مالية (على سبيل المثال، بنك) تخدم حسابًا للطرف (مدين/دائن)".</span><span class="sxs-lookup"><span data-stu-id="68cc5-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="68cc5-142">مؤسسة مالية (على سبيل المثال، بنك) تخدم حسابًا للطرف (مدين/دائن).</span><span class="sxs-lookup"><span data-stu-id="68cc5-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="68cc5-143">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="68cc5-144">في الحقل "الاسم"، اكتب "الاسم".</span><span class="sxs-lookup"><span data-stu-id="68cc5-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="68cc5-145">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="68cc5-146">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-146">Click Add.</span></span>
10. <span data-ttu-id="68cc5-147">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="68cc5-148">في الحقل "الاسم"، اكتب "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="68cc5-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="68cc5-149">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-149">Click Add.</span></span>
13. <span data-ttu-id="68cc5-150">في حقل "الوصف"، أدخل "كود تعريف البنك".</span><span class="sxs-lookup"><span data-stu-id="68cc5-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="68cc5-151">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="68cc5-152">في الحقل "الاسم"، اكتب "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="68cc5-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="68cc5-153">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-153">Click Add.</span></span>
17. <span data-ttu-id="68cc5-154">في حقل "الوصف"، أدخل "رقم التوجيه".</span><span class="sxs-lookup"><span data-stu-id="68cc5-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="68cc5-155">انقر فوق "بحث عن السابق".</span><span class="sxs-lookup"><span data-stu-id="68cc5-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="68cc5-156">تعريف بنية الحساب البنكي لهذا النموذج</span><span class="sxs-lookup"><span data-stu-id="68cc5-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="68cc5-157">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="68cc5-158">في الحقل "الاسم"، اكتب "الحساب".</span><span class="sxs-lookup"><span data-stu-id="68cc5-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="68cc5-159">في الحقل "نوع الصنف"، حدد "سجل".</span><span class="sxs-lookup"><span data-stu-id="68cc5-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="68cc5-160">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-160">Click Add.</span></span>
5. <span data-ttu-id="68cc5-161">في حقل "الوصف"، أدخل "تعريف حساب الطرف في مؤسسة مالية (على سبيل المثال، بنك)".</span><span class="sxs-lookup"><span data-stu-id="68cc5-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="68cc5-162">تعريف حساب الطرف في مؤسسة مالية (على سبيل المثال، بنك).</span><span class="sxs-lookup"><span data-stu-id="68cc5-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="68cc5-163">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="68cc5-164">في الحقل "الاسم"، اكتب "العملة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="68cc5-165">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="68cc5-166">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-166">Click Add.</span></span>
10. <span data-ttu-id="68cc5-167">في حقل "الوصف"، أدخل "كود العملة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="68cc5-168">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="68cc5-169">في الحقل "الاسم"، اكتب "الرقم".</span><span class="sxs-lookup"><span data-stu-id="68cc5-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="68cc5-170">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-170">Click Add.</span></span>
14. <span data-ttu-id="68cc5-171">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="68cc5-172">في الحقل "الاسم، اكتب "IBAN".</span><span class="sxs-lookup"><span data-stu-id="68cc5-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="68cc5-173">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-173">Click Add.</span></span>
17. <span data-ttu-id="68cc5-174">في حقل "الوصف"، أدخل "رقم الحساب البنكي الدولي".</span><span class="sxs-lookup"><span data-stu-id="68cc5-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="68cc5-175">تعريف بنية رسالة الدفع لنوع دفع تحويل الائتمان</span><span class="sxs-lookup"><span data-stu-id="68cc5-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="68cc5-176">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="68cc5-177">في الحقل "عقدة جديدة كـ‬"، أدخل "جذر النموذج‬".</span><span class="sxs-lookup"><span data-stu-id="68cc5-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="68cc5-178">في الحقل "الاسم، اكتب "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="68cc5-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="68cc5-179">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-179">Click Add.</span></span>
5. <span data-ttu-id="68cc5-180">في الحقل "بحث، اكتب "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="68cc5-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="68cc5-181">انقر فوق "بحث عن السابق".</span><span class="sxs-lookup"><span data-stu-id="68cc5-181">Click Find previous.</span></span>
7. <span data-ttu-id="68cc5-182">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="68cc5-183">في الحقل "الاسم، اكتب "MessageIdentification".‬</span><span class="sxs-lookup"><span data-stu-id="68cc5-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="68cc5-184">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-184">Click Add.</span></span>
10. <span data-ttu-id="68cc5-185">في حقل "الوصف"، أدخل "المرجع نقطة إلى نقطة المعين بواسطة الطرف مصدر التعليمات (والمرسل إلى الطرف التالي) لتعريف رسالة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="68cc5-186">المرجع نقطة إلى نقطة المعين بواسطة الطرف مصدر التعليمات (والمرسل إلى الطرف التالي) لتعريف رسالة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="68cc5-187">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="68cc5-188">في الحقل "الاسم، اكتب "ProcessingDateTime".‬</span><span class="sxs-lookup"><span data-stu-id="68cc5-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="68cc5-189">في الحقل "نوع الصنف"، حدد "DateTime".</span><span class="sxs-lookup"><span data-stu-id="68cc5-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="68cc5-190">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-190">Click Add.</span></span>
15. <span data-ttu-id="68cc5-191">في حقل "الوصف"، أدخل "تاريخ ووقت إنشاء رسالة الدفع".</span><span class="sxs-lookup"><span data-stu-id="68cc5-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="68cc5-192">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="68cc5-193">تعريف بنية حركة الدفع لهذا النموذج.</span><span class="sxs-lookup"><span data-stu-id="68cc5-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="68cc5-194">في الحقل "الاسم، اكتب "دفعات".‬</span><span class="sxs-lookup"><span data-stu-id="68cc5-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="68cc5-195">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="68cc5-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="68cc5-196">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-196">Click Add.</span></span>
20. <span data-ttu-id="68cc5-197">في حقل "الوصف"، أدخل "‏‫بنود الدفع للرسالة الحالية‬".</span><span class="sxs-lookup"><span data-stu-id="68cc5-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="68cc5-198">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="68cc5-199">في الحقل "الاسم"، اكتب "الدائن".</span><span class="sxs-lookup"><span data-stu-id="68cc5-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="68cc5-200">في الحقل "نوع الصنف"، حدد "سجل".</span><span class="sxs-lookup"><span data-stu-id="68cc5-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="68cc5-201">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-201">Click Add.</span></span>
25. <span data-ttu-id="68cc5-202">في حقل "الوصف"، اكتب "الطرف المستحق له المبلغ المالي".</span><span class="sxs-lookup"><span data-stu-id="68cc5-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="68cc5-203">انقر فوق "تغيير مرجع الصنف".</span><span class="sxs-lookup"><span data-stu-id="68cc5-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="68cc5-204">في الحقل "بحث"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="68cc5-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="68cc5-205">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="68cc5-205">Click Find next.</span></span>
29. <span data-ttu-id="68cc5-206">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="68cc5-206">Click OK.</span></span>
30. <span data-ttu-id="68cc5-207">في الحقل "بحث"، اكتب "دفعات".‬</span><span class="sxs-lookup"><span data-stu-id="68cc5-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="68cc5-208">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="68cc5-208">Click Find next.</span></span>
32. <span data-ttu-id="68cc5-209">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="68cc5-210">في الحقل "الاسم"، اكتب "المدين".</span><span class="sxs-lookup"><span data-stu-id="68cc5-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="68cc5-211">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-211">Click Add.</span></span>
35. <span data-ttu-id="68cc5-212">في حقل "الوصف"، اكتب "الطرف المدين بالمبلغ المالي للدائن (النهائي)‬".</span><span class="sxs-lookup"><span data-stu-id="68cc5-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="68cc5-213">انقر فوق "تغيير مرجع الصنف".</span><span class="sxs-lookup"><span data-stu-id="68cc5-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="68cc5-214">في الحقل "بحث"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="68cc5-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="68cc5-215">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="68cc5-215">Click Find next.</span></span>
39. <span data-ttu-id="68cc5-216">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="68cc5-216">Click OK.</span></span>
40. <span data-ttu-id="68cc5-217">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="68cc5-217">Click Find next.</span></span>
41. <span data-ttu-id="68cc5-218">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="68cc5-219">في الحقل "الاسم"، اكتب "الوصف".</span><span class="sxs-lookup"><span data-stu-id="68cc5-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="68cc5-220">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="68cc5-221">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-221">Click Add.</span></span>
45. <span data-ttu-id="68cc5-222">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="68cc5-223">في الحقل "الاسم"، اكتب "العملة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="68cc5-224">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-224">Click Add.</span></span>
48. <span data-ttu-id="68cc5-225">في حقل "الوصف"، أدخل "كود العملة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="68cc5-226">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="68cc5-227">في الحقل "الاسم"، أكتب "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="68cc5-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="68cc5-228">في الحقل "نوع الصنف"، حدد "تاريخ".</span><span class="sxs-lookup"><span data-stu-id="68cc5-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="68cc5-229">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-229">Click Add.</span></span>
53. <span data-ttu-id="68cc5-230">في حقل "الوصف"، أدخل "تاريخ الحركة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="68cc5-231">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="68cc5-232">في الحقل "الاسم"، اكتب "InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="68cc5-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="68cc5-233">في الحقل "نوع الصنف"، حدد "حقيقي".</span><span class="sxs-lookup"><span data-stu-id="68cc5-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="68cc5-234">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-234">Click Add.</span></span>
58. <span data-ttu-id="68cc5-235">في حقل "الوصف"، اكتب "المبلغ المالي المطلوب تحويله بين المدين والدائن، قبل خصم الرسوم.‬</span><span class="sxs-lookup"><span data-stu-id="68cc5-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="68cc5-236">يجب التعبير عن المبلغ بالعملة كما طلبها الطرف البادئ".</span><span class="sxs-lookup"><span data-stu-id="68cc5-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="68cc5-237">المبلغ المالي المطلوب تحويله بين المدين والدائن، قبل خصم الرسوم.</span><span class="sxs-lookup"><span data-stu-id="68cc5-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="68cc5-238">يجب التعبير عن المبلغ بالعملة كما طلبها الطرف البادئ.</span><span class="sxs-lookup"><span data-stu-id="68cc5-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="68cc5-239">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="68cc5-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="68cc5-240">في الحقل "الاسم، اكتب "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="68cc5-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="68cc5-241">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="68cc5-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="68cc5-242">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-242">Click Add.</span></span>
63. <span data-ttu-id="68cc5-243">في حقل "الوصف"، أدخل "الهوية الفريدة المعينة بواسطة الطرف البادئ.</span><span class="sxs-lookup"><span data-stu-id="68cc5-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="68cc5-244">يتم تمرير هذه الهوية، دون تغيير عبر سلسلة نهاية إلى نهاية بأكملها".</span><span class="sxs-lookup"><span data-stu-id="68cc5-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="68cc5-245">في الحقل "الاسم"، اكتب "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="68cc5-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="68cc5-246">يتماشى اسم PaymentModel مع الواجهات المعرفة مسبقًا لنماذج الدفع.</span><span class="sxs-lookup"><span data-stu-id="68cc5-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="68cc5-247">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="68cc5-247">Click Save.</span></span>
66. <span data-ttu-id="68cc5-248">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="68cc5-248">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]