---
title: نموذج البيانات الخاص بمجال تصميم الإبلاغ الإلكتروني
description: تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على نموذج بيانات لمستندات الدفع الإلكتروني.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe08b30977b8515ffd8d0acc1fd8f4b3085de93
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026076"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="718c3-103">نموذج البيانات الخاص بمجال تصميم الإبلاغ الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="718c3-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="718c3-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على نموذج بيانات لمستندات الدفع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="718c3-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="718c3-105">سيتم استخدام نموذج البيانات هذا لاحقًا كمصدر بيانات عند إنشاء تنسيق مستندات الدفع.</span><span class="sxs-lookup"><span data-stu-id="718c3-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="718c3-106">في هذا المثال، ستقوم بإنشاء تكوين لشركة عينة، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة كتكوينات ER المشتركة بين الشركات.</span><span class="sxs-lookup"><span data-stu-id="718c3-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="718c3-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="718c3-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="718c3-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="718c3-109">حدد موفر التكوين للشركة النموذجية، ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="718c3-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="718c3-110">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="718c3-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="718c3-111">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="718c3-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="718c3-112">ستقوم بإنشاء تكوين يحتوي على نموذج بيانات لمستندات الدفع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="718c3-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="718c3-113">سيتم استخدام نموذج البيانات هذا لاحقًا كمصدر بيانات عند إنشاء تنسيق مستندات الدفع.</span><span class="sxs-lookup"><span data-stu-id="718c3-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="718c3-114">إنشاء تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="718c3-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="718c3-115">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="718c3-116">في الحقل "الاسم"، اكتب "المدفوعات (نموذج مبسط)".</span><span class="sxs-lookup"><span data-stu-id="718c3-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="718c3-117">المدفوعات (نموذج مبسط)</span><span class="sxs-lookup"><span data-stu-id="718c3-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="718c3-118">في حقل "الوصف"، اكتب "تكوين نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="718c3-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="718c3-119">تكوين نموذج الدفع</span><span class="sxs-lookup"><span data-stu-id="718c3-119">Payment model configuration</span></span>  
    * <span data-ttu-id="718c3-120">يتم تلقائيًا إدخال موفر التكوين النشط هنا.</span><span class="sxs-lookup"><span data-stu-id="718c3-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="718c3-121">سيكون هذا الموفر قادرًا على المحافظة على هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="718c3-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="718c3-122">باستطاعة موفرين آخرين استخدام هذا التكوين، ولكن لن يكون باستطاعتهم المحافظة عليه.</span><span class="sxs-lookup"><span data-stu-id="718c3-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="718c3-123">انقر فوق الزر "إنشاء تكوين" لإكمال مهمة إنشاء التكوين</span><span class="sxs-lookup"><span data-stu-id="718c3-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="718c3-124">إنشاء نموذج بيانات</span><span class="sxs-lookup"><span data-stu-id="718c3-124">Create a data model</span></span>
<span data-ttu-id="718c3-125">إنك تقوم بإنشاء نموذج بيانات جديد للتكوين المحدد.</span><span class="sxs-lookup"><span data-stu-id="718c3-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="718c3-126">سيكون إصدار التكوين بالحالة "مسودة".</span><span class="sxs-lookup"><span data-stu-id="718c3-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="718c3-127">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="718c3-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="718c3-128">تعريف بنية طرف مشاركة في عملية الدفع</span><span class="sxs-lookup"><span data-stu-id="718c3-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="718c3-129">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="718c3-130">في حقل "الاسم"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="718c3-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="718c3-131">الطرف</span><span class="sxs-lookup"><span data-stu-id="718c3-131">Party</span></span>  
3. <span data-ttu-id="718c3-132">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-132">Click Add.</span></span>
4. <span data-ttu-id="718c3-133">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="718c3-134">في الحقل "الاسم"، اكتب "الاسم".</span><span class="sxs-lookup"><span data-stu-id="718c3-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="718c3-135">الاسم</span><span class="sxs-lookup"><span data-stu-id="718c3-135">Name</span></span>  
6. <span data-ttu-id="718c3-136">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="718c3-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="718c3-137">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-137">Click Add.</span></span>
8. <span data-ttu-id="718c3-138">في الحقل "بحث"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="718c3-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="718c3-139">الطرف</span><span class="sxs-lookup"><span data-stu-id="718c3-139">Party</span></span>  
9. <span data-ttu-id="718c3-140">انقر فوق "بحث عن السابق".</span><span class="sxs-lookup"><span data-stu-id="718c3-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="718c3-141">تعريف بنية البنك لهذا النموذج</span><span class="sxs-lookup"><span data-stu-id="718c3-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="718c3-142">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="718c3-143">في الحقل "الاسم"، اكتب "الوكيل".</span><span class="sxs-lookup"><span data-stu-id="718c3-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="718c3-144">الوكيل</span><span class="sxs-lookup"><span data-stu-id="718c3-144">Agent</span></span>  
3. <span data-ttu-id="718c3-145">في الحقل "نوع الصنف"، حدد "سجل".</span><span class="sxs-lookup"><span data-stu-id="718c3-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="718c3-146">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-146">Click Add.</span></span>
5. <span data-ttu-id="718c3-147">في حقل "الوصف"، أدخل "مؤسسة مالية (على سبيل المثال، بنك) تخدم حسابًا للطرف (مدين/دائن)".</span><span class="sxs-lookup"><span data-stu-id="718c3-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="718c3-148">مؤسسة مالية (على سبيل المثال، بنك) تخدم حسابًا للطرف (مدين/دائن).</span><span class="sxs-lookup"><span data-stu-id="718c3-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="718c3-149">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="718c3-150">في الحقل "الاسم"، اكتب "الاسم".</span><span class="sxs-lookup"><span data-stu-id="718c3-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="718c3-151">الاسم</span><span class="sxs-lookup"><span data-stu-id="718c3-151">Name</span></span>  
8. <span data-ttu-id="718c3-152">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="718c3-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="718c3-153">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-153">Click Add.</span></span>
10. <span data-ttu-id="718c3-154">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="718c3-155">في الحقل "الاسم"، اكتب "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="718c3-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="718c3-156">تحويل إلكتروني</span><span class="sxs-lookup"><span data-stu-id="718c3-156">SWIFT</span></span>  
12. <span data-ttu-id="718c3-157">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-157">Click Add.</span></span>
13. <span data-ttu-id="718c3-158">في حقل "الوصف"، أدخل "كود تعريف البنك".</span><span class="sxs-lookup"><span data-stu-id="718c3-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="718c3-159">كود تعريف البنك.</span><span class="sxs-lookup"><span data-stu-id="718c3-159">Bank identification code</span></span>  
14. <span data-ttu-id="718c3-160">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="718c3-161">في الحقل "الاسم"، اكتب "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="718c3-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="718c3-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="718c3-162">RoutingNumber</span></span>  
16. <span data-ttu-id="718c3-163">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-163">Click Add.</span></span>
17. <span data-ttu-id="718c3-164">في حقل "الوصف"، أدخل "رقم التوجيه".</span><span class="sxs-lookup"><span data-stu-id="718c3-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="718c3-165">رقم التوجيه</span><span class="sxs-lookup"><span data-stu-id="718c3-165">Routing number</span></span>  
18. <span data-ttu-id="718c3-166">انقر فوق "بحث عن السابق".</span><span class="sxs-lookup"><span data-stu-id="718c3-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="718c3-167">تعريف بنية الحساب البنكي لهذا النموذج</span><span class="sxs-lookup"><span data-stu-id="718c3-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="718c3-168">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="718c3-169">في الحقل "الاسم"، اكتب "الحساب".</span><span class="sxs-lookup"><span data-stu-id="718c3-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="718c3-170">الحساب</span><span class="sxs-lookup"><span data-stu-id="718c3-170">Account</span></span>  
3. <span data-ttu-id="718c3-171">في الحقل "نوع الصنف"، حدد "سجل".</span><span class="sxs-lookup"><span data-stu-id="718c3-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="718c3-172">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-172">Click Add.</span></span>
5. <span data-ttu-id="718c3-173">في حقل "الوصف"، أدخل "تعريف حساب الطرف في مؤسسة مالية (على سبيل المثال، بنك)".</span><span class="sxs-lookup"><span data-stu-id="718c3-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="718c3-174">تعريف حساب الطرف في مؤسسة مالية (على سبيل المثال، بنك).</span><span class="sxs-lookup"><span data-stu-id="718c3-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="718c3-175">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="718c3-176">في الحقل "الاسم"، اكتب "العملة".</span><span class="sxs-lookup"><span data-stu-id="718c3-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="718c3-177">العملة</span><span class="sxs-lookup"><span data-stu-id="718c3-177">Currency</span></span>  
8. <span data-ttu-id="718c3-178">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="718c3-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="718c3-179">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-179">Click Add.</span></span>
10. <span data-ttu-id="718c3-180">في حقل "الوصف"، أدخل "كود العملة".</span><span class="sxs-lookup"><span data-stu-id="718c3-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="718c3-181">كود العملة</span><span class="sxs-lookup"><span data-stu-id="718c3-181">Currency code</span></span>  
11. <span data-ttu-id="718c3-182">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="718c3-183">في الحقل "الاسم"، اكتب "الرقم".</span><span class="sxs-lookup"><span data-stu-id="718c3-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="718c3-184">العدد</span><span class="sxs-lookup"><span data-stu-id="718c3-184">Number</span></span>  
13. <span data-ttu-id="718c3-185">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-185">Click Add.</span></span>
14. <span data-ttu-id="718c3-186">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="718c3-187">في الحقل "الاسم، اكتب "IBAN".</span><span class="sxs-lookup"><span data-stu-id="718c3-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="718c3-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="718c3-188">IBAN</span></span>  
16. <span data-ttu-id="718c3-189">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-189">Click Add.</span></span>
17. <span data-ttu-id="718c3-190">في حقل "الوصف"، أدخل "رقم الحساب البنكي الدولي".</span><span class="sxs-lookup"><span data-stu-id="718c3-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="718c3-191">رقم الحساب البنكي الدولي</span><span class="sxs-lookup"><span data-stu-id="718c3-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="718c3-192">تعريف بنية رسالة الدفع لنوع دفع تحويل الائتمان</span><span class="sxs-lookup"><span data-stu-id="718c3-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="718c3-193">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="718c3-194">في الحقل "عقدة جديدة كـ‬"، أدخل "جذر النموذج‬".</span><span class="sxs-lookup"><span data-stu-id="718c3-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="718c3-195">في الحقل "الاسم، اكتب "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="718c3-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="718c3-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="718c3-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="718c3-197">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-197">Click Add.</span></span>
5. <span data-ttu-id="718c3-198">في الحقل "بحث، اكتب "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="718c3-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="718c3-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="718c3-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="718c3-200">انقر فوق "بحث عن السابق".</span><span class="sxs-lookup"><span data-stu-id="718c3-200">Click Find previous.</span></span>
7. <span data-ttu-id="718c3-201">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="718c3-202">في الحقل "الاسم، اكتب "MessageIdentification".‬</span><span class="sxs-lookup"><span data-stu-id="718c3-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="718c3-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="718c3-203">MessageIdentification</span></span>  
9. <span data-ttu-id="718c3-204">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-204">Click Add.</span></span>
10. <span data-ttu-id="718c3-205">في حقل "الوصف"، أدخل "المرجع نقطة إلى نقطة المعين بواسطة الطرف مصدر التعليمات (والمرسل إلى الطرف التالي) لتعريف رسالة".</span><span class="sxs-lookup"><span data-stu-id="718c3-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="718c3-206">المرجع نقطة إلى نقطة المعين بواسطة الطرف مصدر التعليمات (والمرسل إلى الطرف التالي) لتعريف رسالة.</span><span class="sxs-lookup"><span data-stu-id="718c3-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="718c3-207">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="718c3-208">في الحقل "الاسم، اكتب "ProcessingDateTime".‬</span><span class="sxs-lookup"><span data-stu-id="718c3-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="718c3-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="718c3-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="718c3-210">في الحقل "نوع الصنف"، حدد "DateTime".</span><span class="sxs-lookup"><span data-stu-id="718c3-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="718c3-211">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-211">Click Add.</span></span>
15. <span data-ttu-id="718c3-212">في حقل "الوصف"، أدخل "تاريخ ووقت إنشاء رسالة الدفع".</span><span class="sxs-lookup"><span data-stu-id="718c3-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="718c3-213">تاريخ ووقت إنشاء رسالة الدفع.</span><span class="sxs-lookup"><span data-stu-id="718c3-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="718c3-214">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="718c3-215">تعريف بنية حركة الدفع لهذا النموذج.</span><span class="sxs-lookup"><span data-stu-id="718c3-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="718c3-216">في الحقل "الاسم، اكتب "دفعات".‬</span><span class="sxs-lookup"><span data-stu-id="718c3-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="718c3-217">المدفوعات</span><span class="sxs-lookup"><span data-stu-id="718c3-217">Payments</span></span>  
18. <span data-ttu-id="718c3-218">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="718c3-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="718c3-219">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-219">Click Add.</span></span>
20. <span data-ttu-id="718c3-220">في حقل "الوصف"، أدخل "‏‫بنود الدفع للرسالة الحالية‬".</span><span class="sxs-lookup"><span data-stu-id="718c3-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="718c3-221">بنود الدفع للرسالة الحالية</span><span class="sxs-lookup"><span data-stu-id="718c3-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="718c3-222">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="718c3-223">في الحقل "الاسم"، اكتب "الدائن".</span><span class="sxs-lookup"><span data-stu-id="718c3-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="718c3-224">الدائن</span><span class="sxs-lookup"><span data-stu-id="718c3-224">Creditor</span></span>  
23. <span data-ttu-id="718c3-225">في الحقل "نوع الصنف"، حدد "سجل".</span><span class="sxs-lookup"><span data-stu-id="718c3-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="718c3-226">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-226">Click Add.</span></span>
25. <span data-ttu-id="718c3-227">في حقل "الوصف"، اكتب "الطرف المستحق له المبلغ المالي".</span><span class="sxs-lookup"><span data-stu-id="718c3-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="718c3-228">الطرف المستحق له المبلغ المالي.</span><span class="sxs-lookup"><span data-stu-id="718c3-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="718c3-229">انقر فوق "تغيير مرجع الصنف".</span><span class="sxs-lookup"><span data-stu-id="718c3-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="718c3-230">في الحقل "بحث"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="718c3-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="718c3-231">الطرف</span><span class="sxs-lookup"><span data-stu-id="718c3-231">Party</span></span>  
28. <span data-ttu-id="718c3-232">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="718c3-232">Click Find next.</span></span>
29. <span data-ttu-id="718c3-233">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="718c3-233">Click OK.</span></span>
30. <span data-ttu-id="718c3-234">في الحقل "بحث"، اكتب "دفعات".‬</span><span class="sxs-lookup"><span data-stu-id="718c3-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="718c3-235">المدفوعات</span><span class="sxs-lookup"><span data-stu-id="718c3-235">Payments</span></span>  
31. <span data-ttu-id="718c3-236">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="718c3-236">Click Find next.</span></span>
32. <span data-ttu-id="718c3-237">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="718c3-238">في الحقل "الاسم"، اكتب "المدين".</span><span class="sxs-lookup"><span data-stu-id="718c3-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="718c3-239">المدين</span><span class="sxs-lookup"><span data-stu-id="718c3-239">Debtor</span></span>  
34. <span data-ttu-id="718c3-240">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-240">Click Add.</span></span>
35. <span data-ttu-id="718c3-241">في حقل "الوصف"، اكتب "الطرف المدين بالمبلغ المالي للدائن (النهائي)‬".</span><span class="sxs-lookup"><span data-stu-id="718c3-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="718c3-242">الطرف المدين بالمبلغ المالي للدائن (النهائي).</span><span class="sxs-lookup"><span data-stu-id="718c3-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="718c3-243">انقر فوق "تغيير مرجع الصنف".</span><span class="sxs-lookup"><span data-stu-id="718c3-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="718c3-244">في الحقل "بحث"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="718c3-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="718c3-245">الطرف</span><span class="sxs-lookup"><span data-stu-id="718c3-245">Party</span></span>  
38. <span data-ttu-id="718c3-246">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="718c3-246">Click Find next.</span></span>
39. <span data-ttu-id="718c3-247">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="718c3-247">Click OK.</span></span>
40. <span data-ttu-id="718c3-248">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="718c3-248">Click Find next.</span></span>
41. <span data-ttu-id="718c3-249">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="718c3-250">في الحقل "الاسم"، اكتب "الوصف".</span><span class="sxs-lookup"><span data-stu-id="718c3-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="718c3-251">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="718c3-251">Description</span></span>  
43. <span data-ttu-id="718c3-252">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="718c3-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="718c3-253">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-253">Click Add.</span></span>
45. <span data-ttu-id="718c3-254">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="718c3-255">في الحقل "الاسم"، اكتب "العملة".</span><span class="sxs-lookup"><span data-stu-id="718c3-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="718c3-256">العملة</span><span class="sxs-lookup"><span data-stu-id="718c3-256">Currency</span></span>  
47. <span data-ttu-id="718c3-257">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-257">Click Add.</span></span>
48. <span data-ttu-id="718c3-258">في حقل "الوصف"، أدخل "كود العملة".</span><span class="sxs-lookup"><span data-stu-id="718c3-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="718c3-259">كود العملة</span><span class="sxs-lookup"><span data-stu-id="718c3-259">Currency code</span></span>  
49. <span data-ttu-id="718c3-260">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="718c3-261">في الحقل "الاسم"، أكتب "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="718c3-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="718c3-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="718c3-262">TransactionDate</span></span>  
51. <span data-ttu-id="718c3-263">في الحقل "نوع الصنف"، حدد "تاريخ".</span><span class="sxs-lookup"><span data-stu-id="718c3-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="718c3-264">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-264">Click Add.</span></span>
53. <span data-ttu-id="718c3-265">في حقل "الوصف"، أدخل "تاريخ الحركة".</span><span class="sxs-lookup"><span data-stu-id="718c3-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="718c3-266">تاريخ الحركة</span><span class="sxs-lookup"><span data-stu-id="718c3-266">Transaction date</span></span>  
54. <span data-ttu-id="718c3-267">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="718c3-268">في الحقل "الاسم"، اكتب "InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="718c3-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="718c3-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="718c3-269">InstructedAmount</span></span>  
56. <span data-ttu-id="718c3-270">في الحقل "نوع الصنف"، حدد "حقيقي".</span><span class="sxs-lookup"><span data-stu-id="718c3-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="718c3-271">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-271">Click Add.</span></span>
58. <span data-ttu-id="718c3-272">في حقل "الوصف"، اكتب "المبلغ المالي المطلوب تحويله بين المدين والدائن، قبل خصم الرسوم.‬</span><span class="sxs-lookup"><span data-stu-id="718c3-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="718c3-273">يجب التعبير عن المبلغ بالعملة كما طلبها الطرف البادئ".</span><span class="sxs-lookup"><span data-stu-id="718c3-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="718c3-274">المبلغ المالي المطلوب تحويله بين المدين والدائن، قبل خصم الرسوم.</span><span class="sxs-lookup"><span data-stu-id="718c3-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="718c3-275">يجب التعبير عن المبلغ بالعملة كما طلبها الطرف البادئ.</span><span class="sxs-lookup"><span data-stu-id="718c3-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="718c3-276">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="718c3-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="718c3-277">في الحقل "الاسم، اكتب "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="718c3-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="718c3-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="718c3-278">End2EndID</span></span>  
61. <span data-ttu-id="718c3-279">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="718c3-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="718c3-280">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="718c3-280">Click Add.</span></span>
63. <span data-ttu-id="718c3-281">في حقل "الوصف"، أدخل "الهوية الفريدة المعينة بواسطة الطرف البادئ.</span><span class="sxs-lookup"><span data-stu-id="718c3-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="718c3-282">يتم تمرير هذه الهوية، دون تغيير عبر سلسلة نهاية إلى نهاية بأكملها".</span><span class="sxs-lookup"><span data-stu-id="718c3-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="718c3-283">الهوية الفريدة المعينة بواسطة الطرف البادئ.</span><span class="sxs-lookup"><span data-stu-id="718c3-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="718c3-284">يتم تمرير هذه الهوية، دون تغيير عبر سلسلة نهاية إلى نهاية بأكملها.</span><span class="sxs-lookup"><span data-stu-id="718c3-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="718c3-285">في الحقل "الاسم"، اكتب "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="718c3-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="718c3-286">يتماشى اسم PaymentModel مع الواجهات المعرفة مسبقًا لنماذج الدفع.</span><span class="sxs-lookup"><span data-stu-id="718c3-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="718c3-287">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="718c3-287">Click Save.</span></span>
66. <span data-ttu-id="718c3-288">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="718c3-288">Close the page.</span></span>

