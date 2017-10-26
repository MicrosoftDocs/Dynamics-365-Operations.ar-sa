--- 
title: "تصميم نموذج البيانات الخاص بالمجال للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على نموذج بيانات لمستندات الدفع الإلكتروني."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fadc5bc54654faf9e91e0831bdd0ff087cea3164
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a><span data-ttu-id="0018b-103">تصميم نموذج البيانات الخاص بالمجال للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="0018b-103">Design a domain-specific data model for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0018b-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على نموذج بيانات لمستندات الدفع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="0018b-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="0018b-105">سيتم استخدام نموذج البيانات هذا لاحقًا كمصدر بيانات عند إنشاء تنسيق مستندات الدفع.</span><span class="sxs-lookup"><span data-stu-id="0018b-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="0018b-106">في هذا المثال، ستقوم بإنشاء تكوين لشركة عينة، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة كتكوينات ER المشتركة بين الشركات.</span><span class="sxs-lookup"><span data-stu-id="0018b-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="0018b-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="0018b-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="0018b-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="0018b-109">حدد موفر التكوين للشركة النموذجية، ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="0018b-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="0018b-110">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="0018b-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="0018b-111">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="0018b-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="0018b-112">ستقوم بإنشاء تكوين يحتوي على نموذج بيانات لمستندات الدفع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="0018b-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="0018b-113">سيتم استخدام نموذج البيانات هذا لاحقًا كمصدر بيانات عند إنشاء تنسيق مستندات الدفع.</span><span class="sxs-lookup"><span data-stu-id="0018b-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="0018b-114">إنشاء تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="0018b-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="0018b-115">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="0018b-116">في الحقل "الاسم"، اكتب "المدفوعات (نموذج مبسط)".</span><span class="sxs-lookup"><span data-stu-id="0018b-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="0018b-117">المدفوعات (نموذج مبسط)</span><span class="sxs-lookup"><span data-stu-id="0018b-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="0018b-118">في حقل "الوصف"، اكتب "تكوين نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="0018b-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="0018b-119">تكوين نموذج الدفع</span><span class="sxs-lookup"><span data-stu-id="0018b-119">Payment model configuration</span></span>  
    * <span data-ttu-id="0018b-120">يتم تلقائيًا إدخال موفر التكوين النشط هنا.</span><span class="sxs-lookup"><span data-stu-id="0018b-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="0018b-121">سيكون هذا الموفر قادرًا على المحافظة على هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="0018b-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="0018b-122">باستطاعة موفرين آخرين استخدام هذا التكوين، ولكن لن يكون باستطاعتهم المحافظة عليه.</span><span class="sxs-lookup"><span data-stu-id="0018b-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="0018b-123">انقر فوق الزر "إنشاء تكوين" لإكمال مهمة إنشاء التكوين</span><span class="sxs-lookup"><span data-stu-id="0018b-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="0018b-124">إنشاء نموذج بيانات</span><span class="sxs-lookup"><span data-stu-id="0018b-124">Create a data model</span></span>
    * <span data-ttu-id="0018b-125">إنك تقوم بإنشاء نموذج بيانات جديد للتكوين المحدد.</span><span class="sxs-lookup"><span data-stu-id="0018b-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="0018b-126">سيكون إصدار التكوين بالحالة "مسودة".</span><span class="sxs-lookup"><span data-stu-id="0018b-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="0018b-127">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="0018b-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="0018b-128">تعريف بنية طرف مشاركة في عملية الدفع</span><span class="sxs-lookup"><span data-stu-id="0018b-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="0018b-129">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0018b-130">في حقل "الاسم"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="0018b-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="0018b-131">الطرف</span><span class="sxs-lookup"><span data-stu-id="0018b-131">Party</span></span>  
3. <span data-ttu-id="0018b-132">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-132">Click Add.</span></span>
4. <span data-ttu-id="0018b-133">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="0018b-134">في الحقل "الاسم"، اكتب "الاسم".</span><span class="sxs-lookup"><span data-stu-id="0018b-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="0018b-135">الاسم</span><span class="sxs-lookup"><span data-stu-id="0018b-135">Name</span></span>  
6. <span data-ttu-id="0018b-136">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="0018b-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="0018b-137">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-137">Click Add.</span></span>
8. <span data-ttu-id="0018b-138">في الحقل "بحث"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="0018b-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="0018b-139">الطرف</span><span class="sxs-lookup"><span data-stu-id="0018b-139">Party</span></span>  
9. <span data-ttu-id="0018b-140">انقر فوق "بحث عن السابق".</span><span class="sxs-lookup"><span data-stu-id="0018b-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="0018b-141">تعريف بنية البنك لهذا النموذج</span><span class="sxs-lookup"><span data-stu-id="0018b-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="0018b-142">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0018b-143">في الحقل "الاسم"، اكتب "الوكيل".</span><span class="sxs-lookup"><span data-stu-id="0018b-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="0018b-144">الوكيل</span><span class="sxs-lookup"><span data-stu-id="0018b-144">Agent</span></span>  
3. <span data-ttu-id="0018b-145">في الحقل "نوع الصنف"، حدد "سجل".</span><span class="sxs-lookup"><span data-stu-id="0018b-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="0018b-146">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-146">Click Add.</span></span>
5. <span data-ttu-id="0018b-147">في حقل "الوصف"، أدخل "مؤسسة مالية (على سبيل المثال، بنك) تخدم حسابًا للطرف (مدين/دائن)".</span><span class="sxs-lookup"><span data-stu-id="0018b-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="0018b-148">مؤسسة مالية (على سبيل المثال، بنك) تخدم حسابًا للطرف (مدين/دائن).</span><span class="sxs-lookup"><span data-stu-id="0018b-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="0018b-149">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="0018b-150">في الحقل "الاسم"، اكتب "الاسم".</span><span class="sxs-lookup"><span data-stu-id="0018b-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="0018b-151">الاسم</span><span class="sxs-lookup"><span data-stu-id="0018b-151">Name</span></span>  
8. <span data-ttu-id="0018b-152">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="0018b-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="0018b-153">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-153">Click Add.</span></span>
10. <span data-ttu-id="0018b-154">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="0018b-155">في الحقل "الاسم"، اكتب "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="0018b-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="0018b-156">تحويل إلكتروني</span><span class="sxs-lookup"><span data-stu-id="0018b-156">SWIFT</span></span>  
12. <span data-ttu-id="0018b-157">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-157">Click Add.</span></span>
13. <span data-ttu-id="0018b-158">في حقل "الوصف"، أدخل "كود تعريف البنك".</span><span class="sxs-lookup"><span data-stu-id="0018b-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="0018b-159">كود تعريف البنك.</span><span class="sxs-lookup"><span data-stu-id="0018b-159">Bank identification code</span></span>  
14. <span data-ttu-id="0018b-160">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="0018b-161">في الحقل "الاسم"، اكتب "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="0018b-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="0018b-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="0018b-162">RoutingNumber</span></span>  
16. <span data-ttu-id="0018b-163">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-163">Click Add.</span></span>
17. <span data-ttu-id="0018b-164">في حقل "الوصف"، أدخل "رقم التوجيه".</span><span class="sxs-lookup"><span data-stu-id="0018b-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="0018b-165">رقم التوجيه</span><span class="sxs-lookup"><span data-stu-id="0018b-165">Routing number</span></span>  
18. <span data-ttu-id="0018b-166">انقر فوق "بحث عن السابق".</span><span class="sxs-lookup"><span data-stu-id="0018b-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="0018b-167">تعريف بنية الحساب البنكي لهذا النموذج</span><span class="sxs-lookup"><span data-stu-id="0018b-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="0018b-168">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0018b-169">في الحقل "الاسم"، اكتب "الحساب".</span><span class="sxs-lookup"><span data-stu-id="0018b-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="0018b-170">الحساب</span><span class="sxs-lookup"><span data-stu-id="0018b-170">Account</span></span>  
3. <span data-ttu-id="0018b-171">في الحقل "نوع الصنف"، حدد "سجل".</span><span class="sxs-lookup"><span data-stu-id="0018b-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="0018b-172">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-172">Click Add.</span></span>
5. <span data-ttu-id="0018b-173">في حقل "الوصف"، أدخل "تعريف حساب الطرف في مؤسسة مالية (على سبيل المثال، بنك)".</span><span class="sxs-lookup"><span data-stu-id="0018b-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="0018b-174">تعريف حساب الطرف في مؤسسة مالية (على سبيل المثال، بنك).</span><span class="sxs-lookup"><span data-stu-id="0018b-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="0018b-175">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="0018b-176">في الحقل "الاسم"، اكتب "العملة".</span><span class="sxs-lookup"><span data-stu-id="0018b-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="0018b-177">العملة</span><span class="sxs-lookup"><span data-stu-id="0018b-177">Currency</span></span>  
8. <span data-ttu-id="0018b-178">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="0018b-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="0018b-179">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-179">Click Add.</span></span>
10. <span data-ttu-id="0018b-180">في حقل "الوصف"، أدخل "كود العملة".</span><span class="sxs-lookup"><span data-stu-id="0018b-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="0018b-181">كود العملة</span><span class="sxs-lookup"><span data-stu-id="0018b-181">Currency code</span></span>  
11. <span data-ttu-id="0018b-182">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="0018b-183">في الحقل "الاسم"، اكتب "الرقم".</span><span class="sxs-lookup"><span data-stu-id="0018b-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="0018b-184">العدد</span><span class="sxs-lookup"><span data-stu-id="0018b-184">Number</span></span>  
13. <span data-ttu-id="0018b-185">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-185">Click Add.</span></span>
14. <span data-ttu-id="0018b-186">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="0018b-187">في الحقل "الاسم، اكتب "IBAN".</span><span class="sxs-lookup"><span data-stu-id="0018b-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="0018b-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="0018b-188">IBAN</span></span>  
16. <span data-ttu-id="0018b-189">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-189">Click Add.</span></span>
17. <span data-ttu-id="0018b-190">في حقل "الوصف"، أدخل "رقم الحساب البنكي الدولي".</span><span class="sxs-lookup"><span data-stu-id="0018b-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="0018b-191">رقم الحساب البنكي الدولي</span><span class="sxs-lookup"><span data-stu-id="0018b-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="0018b-192">تعريف بنية رسالة الدفع لنوع دفع تحويل الائتمان</span><span class="sxs-lookup"><span data-stu-id="0018b-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="0018b-193">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0018b-194">في الحقل "عقدة جديدة كـ‬"، أدخل "جذر النموذج‬".</span><span class="sxs-lookup"><span data-stu-id="0018b-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="0018b-195">في الحقل "الاسم، اكتب "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="0018b-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="0018b-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="0018b-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="0018b-197">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-197">Click Add.</span></span>
5. <span data-ttu-id="0018b-198">في الحقل "بحث، اكتب "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="0018b-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="0018b-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="0018b-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="0018b-200">انقر فوق "بحث عن السابق".</span><span class="sxs-lookup"><span data-stu-id="0018b-200">Click Find previous.</span></span>
7. <span data-ttu-id="0018b-201">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="0018b-202">في الحقل "الاسم، اكتب "MessageIdentification".‬</span><span class="sxs-lookup"><span data-stu-id="0018b-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="0018b-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="0018b-203">MessageIdentification</span></span>  
9. <span data-ttu-id="0018b-204">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-204">Click Add.</span></span>
10. <span data-ttu-id="0018b-205">في حقل "الوصف"، أدخل "المرجع نقطة إلى نقطة المعين بواسطة الطرف مصدر التعليمات (والمرسل إلى الطرف التالي) لتعريف رسالة".</span><span class="sxs-lookup"><span data-stu-id="0018b-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="0018b-206">المرجع نقطة إلى نقطة المعين بواسطة الطرف مصدر التعليمات (والمرسل إلى الطرف التالي) لتعريف رسالة.</span><span class="sxs-lookup"><span data-stu-id="0018b-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="0018b-207">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="0018b-208">في الحقل "الاسم، اكتب "ProcessingDateTime".‬</span><span class="sxs-lookup"><span data-stu-id="0018b-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="0018b-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="0018b-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="0018b-210">في الحقل "نوع الصنف"، حدد "DateTime".</span><span class="sxs-lookup"><span data-stu-id="0018b-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="0018b-211">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-211">Click Add.</span></span>
15. <span data-ttu-id="0018b-212">في حقل "الوصف"، أدخل "تاريخ ووقت إنشاء رسالة الدفع".</span><span class="sxs-lookup"><span data-stu-id="0018b-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="0018b-213">تاريخ ووقت إنشاء رسالة الدفع.</span><span class="sxs-lookup"><span data-stu-id="0018b-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="0018b-214">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="0018b-215">تعريف بنية حركة الدفع لهذا النموذج.</span><span class="sxs-lookup"><span data-stu-id="0018b-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="0018b-216">في الحقل "الاسم، اكتب "دفعات".‬</span><span class="sxs-lookup"><span data-stu-id="0018b-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="0018b-217">المدفوعات</span><span class="sxs-lookup"><span data-stu-id="0018b-217">Payments</span></span>  
18. <span data-ttu-id="0018b-218">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="0018b-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="0018b-219">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-219">Click Add.</span></span>
20. <span data-ttu-id="0018b-220">في حقل "الوصف"، أدخل "‏‫بنود الدفع للرسالة الحالية‬".</span><span class="sxs-lookup"><span data-stu-id="0018b-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="0018b-221">بنود الدفع للرسالة الحالية</span><span class="sxs-lookup"><span data-stu-id="0018b-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="0018b-222">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="0018b-223">في الحقل "الاسم"، اكتب "الدائن".</span><span class="sxs-lookup"><span data-stu-id="0018b-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="0018b-224">الدائن</span><span class="sxs-lookup"><span data-stu-id="0018b-224">Creditor</span></span>  
23. <span data-ttu-id="0018b-225">في الحقل "نوع الصنف"، حدد "سجل".</span><span class="sxs-lookup"><span data-stu-id="0018b-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="0018b-226">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-226">Click Add.</span></span>
25. <span data-ttu-id="0018b-227">في حقل "الوصف"، اكتب "الطرف المستحق له المبلغ المالي".</span><span class="sxs-lookup"><span data-stu-id="0018b-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="0018b-228">الطرف المستحق له المبلغ المالي.</span><span class="sxs-lookup"><span data-stu-id="0018b-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="0018b-229">انقر فوق "تغيير مرجع الصنف".</span><span class="sxs-lookup"><span data-stu-id="0018b-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="0018b-230">في الحقل "بحث"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="0018b-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="0018b-231">الطرف</span><span class="sxs-lookup"><span data-stu-id="0018b-231">Party</span></span>  
28. <span data-ttu-id="0018b-232">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="0018b-232">Click Find next.</span></span>
29. <span data-ttu-id="0018b-233">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0018b-233">Click OK.</span></span>
30. <span data-ttu-id="0018b-234">في الحقل "بحث"، اكتب "دفعات".‬</span><span class="sxs-lookup"><span data-stu-id="0018b-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="0018b-235">المدفوعات</span><span class="sxs-lookup"><span data-stu-id="0018b-235">Payments</span></span>  
31. <span data-ttu-id="0018b-236">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="0018b-236">Click Find next.</span></span>
32. <span data-ttu-id="0018b-237">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="0018b-238">في الحقل "الاسم"، اكتب "المدين".</span><span class="sxs-lookup"><span data-stu-id="0018b-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="0018b-239">المدين</span><span class="sxs-lookup"><span data-stu-id="0018b-239">Debtor</span></span>  
34. <span data-ttu-id="0018b-240">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-240">Click Add.</span></span>
35. <span data-ttu-id="0018b-241">في حقل "الوصف"، اكتب "الطرف المدين بالمبلغ المالي للدائن (النهائي)‬".</span><span class="sxs-lookup"><span data-stu-id="0018b-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="0018b-242">الطرف المدين بالمبلغ المالي للدائن (النهائي).</span><span class="sxs-lookup"><span data-stu-id="0018b-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="0018b-243">انقر فوق "تغيير مرجع الصنف".</span><span class="sxs-lookup"><span data-stu-id="0018b-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="0018b-244">في الحقل "بحث"، اكتب "الطرف".</span><span class="sxs-lookup"><span data-stu-id="0018b-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="0018b-245">الطرف</span><span class="sxs-lookup"><span data-stu-id="0018b-245">Party</span></span>  
38. <span data-ttu-id="0018b-246">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="0018b-246">Click Find next.</span></span>
39. <span data-ttu-id="0018b-247">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0018b-247">Click OK.</span></span>
40. <span data-ttu-id="0018b-248">انقر فوق "بحث عن التالي".</span><span class="sxs-lookup"><span data-stu-id="0018b-248">Click Find next.</span></span>
41. <span data-ttu-id="0018b-249">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="0018b-250">في الحقل "الاسم"، اكتب "الوصف".</span><span class="sxs-lookup"><span data-stu-id="0018b-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="0018b-251">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="0018b-251">Description</span></span>  
43. <span data-ttu-id="0018b-252">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="0018b-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="0018b-253">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-253">Click Add.</span></span>
45. <span data-ttu-id="0018b-254">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="0018b-255">في الحقل "الاسم"، اكتب "العملة".</span><span class="sxs-lookup"><span data-stu-id="0018b-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="0018b-256">العملة</span><span class="sxs-lookup"><span data-stu-id="0018b-256">Currency</span></span>  
47. <span data-ttu-id="0018b-257">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-257">Click Add.</span></span>
48. <span data-ttu-id="0018b-258">في حقل "الوصف"، أدخل "كود العملة".</span><span class="sxs-lookup"><span data-stu-id="0018b-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="0018b-259">كود العملة</span><span class="sxs-lookup"><span data-stu-id="0018b-259">Currency code</span></span>  
49. <span data-ttu-id="0018b-260">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="0018b-261">في الحقل "الاسم"، أكتب "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="0018b-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="0018b-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="0018b-262">TransactionDate</span></span>  
51. <span data-ttu-id="0018b-263">في الحقل "نوع الصنف"، حدد "تاريخ".</span><span class="sxs-lookup"><span data-stu-id="0018b-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="0018b-264">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-264">Click Add.</span></span>
53. <span data-ttu-id="0018b-265">في حقل "الوصف"، أدخل "تاريخ الحركة".</span><span class="sxs-lookup"><span data-stu-id="0018b-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="0018b-266">تاريخ الحركة</span><span class="sxs-lookup"><span data-stu-id="0018b-266">Transaction date</span></span>  
54. <span data-ttu-id="0018b-267">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="0018b-268">في الحقل "الاسم"، اكتب "InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="0018b-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="0018b-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="0018b-269">InstructedAmount</span></span>  
56. <span data-ttu-id="0018b-270">في الحقل "نوع الصنف"، حدد "حقيقي".</span><span class="sxs-lookup"><span data-stu-id="0018b-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="0018b-271">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-271">Click Add.</span></span>
58. <span data-ttu-id="0018b-272">في حقل "الوصف"، اكتب "المبلغ المالي المطلوب تحويله بين المدين والدائن، قبل خصم الرسوم.‬</span><span class="sxs-lookup"><span data-stu-id="0018b-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="0018b-273">يجب التعبير عن المبلغ بالعملة كما طلبها الطرف البادئ".</span><span class="sxs-lookup"><span data-stu-id="0018b-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="0018b-274">المبلغ المالي المطلوب تحويله بين المدين والدائن، قبل خصم الرسوم.</span><span class="sxs-lookup"><span data-stu-id="0018b-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="0018b-275">يجب التعبير عن المبلغ بالعملة كما طلبها الطرف البادئ.</span><span class="sxs-lookup"><span data-stu-id="0018b-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="0018b-276">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0018b-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="0018b-277">في الحقل "الاسم، اكتب "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="0018b-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="0018b-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="0018b-278">End2EndID</span></span>  
61. <span data-ttu-id="0018b-279">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="0018b-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="0018b-280">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0018b-280">Click Add.</span></span>
63. <span data-ttu-id="0018b-281">في حقل "الوصف"، أدخل "الهوية الفريدة المعينة بواسطة الطرف البادئ.</span><span class="sxs-lookup"><span data-stu-id="0018b-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="0018b-282">يتم تمرير هذه الهوية، دون تغيير عبر سلسلة نهاية إلى نهاية بأكملها".</span><span class="sxs-lookup"><span data-stu-id="0018b-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="0018b-283">الهوية الفريدة المعينة بواسطة الطرف البادئ.</span><span class="sxs-lookup"><span data-stu-id="0018b-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="0018b-284">يتم تمرير هذه الهوية، دون تغيير عبر سلسلة نهاية إلى نهاية بأكملها.</span><span class="sxs-lookup"><span data-stu-id="0018b-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="0018b-285">في الحقل "الاسم"، اكتب "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="0018b-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="0018b-286">يتماشى اسم PaymentModel مع الواجهات المعرفة مسبقًا لنماذج الدفع.</span><span class="sxs-lookup"><span data-stu-id="0018b-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="0018b-287">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="0018b-287">Click Save.</span></span>
66. <span data-ttu-id="0018b-288">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0018b-288">Close the page.</span></span>

