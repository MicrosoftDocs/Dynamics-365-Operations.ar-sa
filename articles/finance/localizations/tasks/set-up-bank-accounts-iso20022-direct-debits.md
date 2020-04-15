---
title: إعداد العملاء والحسابات البنكية للعملاء للديون المباشرة ISO20022
description: تنقلك هذه المهمة عبر عملية إعداد حساب بنكي للعميل وتفويض خصم مباشر للعميل وهما مطلوبان لإنشاء ملف دفع العميل مثل الدين المباشر ISO20022.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b09d7d203f1bb58fad26a109962005affa6d307
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144897"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="57fb4-103">إعداد العملاء والحسابات البنكية للعملاء للديون المباشرة ISO20022</span><span class="sxs-lookup"><span data-stu-id="57fb4-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57fb4-104">تنقلك هذه المهمة عبر عملية إعداد حساب بنكي للعميل وتفويض خصم مباشر للعميل وهما مطلوبان لإنشاء ملف دفع العميل مثل الدين المباشر ISO20022.</span><span class="sxs-lookup"><span data-stu-id="57fb4-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="57fb4-105">بحسب تنسيقات دفع العميل التي تم إعدادها، فإن بعض المعلومات الإضافية، التي لم يتم تناولها في هذا الإجراء، قد تكون مطلوبة لعميل أو حساب بنكي للعميل.</span><span class="sxs-lookup"><span data-stu-id="57fb4-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="57fb4-106">تم إنشاء هذه المهمة باستخدام شركة بيانات العرض التوضيحي DEMF مع كيان قانوني عنوانه الرئيسي في ألمانيا.</span><span class="sxs-lookup"><span data-stu-id="57fb4-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="57fb4-107">هذا هو الإجراء الرابع من ضمن خمسة إجراءات هدفها توضيح عملية معالجة مدفوعات العميل باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57fb4-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="57fb4-108">إعداد حساب بنكي خاص بالعميل</span><span class="sxs-lookup"><span data-stu-id="57fb4-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="57fb4-109">انتقل إلى الحسابات المدينة > العملاء > كافة العملاء‬.</span><span class="sxs-lookup"><span data-stu-id="57fb4-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="57fb4-110">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="57fb4-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="57fb4-111">على سبيل المثال، قم بإجراء التصفية على حقل "الحساب" بقيمة "DE-010".</span><span class="sxs-lookup"><span data-stu-id="57fb4-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="57fb4-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="57fb4-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="57fb4-113">في جزء الإجراءات، انقر فوق "العميل".</span><span class="sxs-lookup"><span data-stu-id="57fb4-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="57fb4-114">انتقل إلى "الحسابات البنكية".</span><span class="sxs-lookup"><span data-stu-id="57fb4-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="57fb4-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="57fb4-115">Click New.</span></span>
7. <span data-ttu-id="57fb4-116">في الحقل "الحساب البنكي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="57fb4-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="57fb4-117">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="57fb4-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="57fb4-118">على سبيل المثال، أدخل "EUR bank".</span><span class="sxs-lookup"><span data-stu-id="57fb4-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="57fb4-119">في الحقل "مجموعات بنكية‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="57fb4-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="57fb4-120">في الحقل "IBAN‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="57fb4-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="57fb4-121">على سبيل المثال، أدخل "DE36200400000628808808".</span><span class="sxs-lookup"><span data-stu-id="57fb4-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="57fb4-122">في الحقل "كود التحويل الإلكتروني‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="57fb4-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="57fb4-123">على سبيل المثال، أدخل "COBADEFFXXX".</span><span class="sxs-lookup"><span data-stu-id="57fb4-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="57fb4-124">لاحظ أن SWIFT \ BIC غير إلزامي للعديد من تنسيقات الدفع، لكن من المستحسن أن يتم تسجيله لحساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="57fb4-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="57fb4-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="57fb4-125">Click Save.</span></span>
13. <span data-ttu-id="57fb4-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="57fb4-126">Close the page.</span></span>
14. <span data-ttu-id="57fb4-127">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="57fb4-127">Click Edit.</span></span>
15. <span data-ttu-id="57fb4-128">وسّع المقطع "القيم الافتراضية للدفع‬".</span><span class="sxs-lookup"><span data-stu-id="57fb4-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="57fb4-129">في الحقل "الحساب البنكي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="57fb4-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="57fb4-130">إضافة تفويض خصم مباشر</span><span class="sxs-lookup"><span data-stu-id="57fb4-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="57fb4-131">وسّع المقطع "تفويضات الخصم المباشر‬".</span><span class="sxs-lookup"><span data-stu-id="57fb4-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="57fb4-132">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="57fb4-132">Click Add.</span></span>
3. <span data-ttu-id="57fb4-133">في الحقل "‏‫الحساب البنكي للدائن‬‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="57fb4-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="57fb4-134">على سبيل المثال، حدد DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="57fb4-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="57fb4-135">في الحقل "تاريخ التوقيع"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="57fb4-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="57fb4-136">انقر فوق "نعم" لتأكيد تاريخ التحديث.</span><span class="sxs-lookup"><span data-stu-id="57fb4-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="57fb4-137">في الحقل "موقع التوقيع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="57fb4-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="57fb4-138">في الحقل "العدد المتوقع للمدفوعات‬‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="57fb4-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="57fb4-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="57fb4-139">Click OK.</span></span>
9. <span data-ttu-id="57fb4-140">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="57fb4-140">Click Save.</span></span>

