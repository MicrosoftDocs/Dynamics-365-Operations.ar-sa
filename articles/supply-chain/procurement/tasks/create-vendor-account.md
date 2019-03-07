---
title: إنشاء حساب مورد
description: يوضح هذا الإجراء كيفية إنشاء حساب مورد، وإضافة عنوان ومعلومات الاتصال.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22c7a1a2b7468f00aa25a67a2c5f62b088e2fe7c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "360131"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="e4849-103">إنشاء حساب مورد</span><span class="sxs-lookup"><span data-stu-id="e4849-103">Create a vendor account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4849-104">يوضح هذا الإجراء كيفية إنشاء حساب مورد، وإضافة عنوان ومعلومات الاتصال.</span><span class="sxs-lookup"><span data-stu-id="e4849-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="e4849-105">ولا يوضح الإجراء كيفية ملء جميع الحقول لأغراض المشتريات والأغراض المالية.</span><span class="sxs-lookup"><span data-stu-id="e4849-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="e4849-106">للتعرف على مزيد من المعلومات حول هذه الحقول، الرجاء قراءة أوصاف الحقول.</span><span class="sxs-lookup"><span data-stu-id="e4849-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="e4849-107">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e4849-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="e4849-108">يتم إنشاء حسابات الموردين عادة بواسطة عاملين محترفين أو عاملي الحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="e4849-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="e4849-109">إنشاء حساب مورد</span><span class="sxs-lookup"><span data-stu-id="e4849-109">Create a vendor account</span></span>
1. <span data-ttu-id="e4849-110">انتقل إلى ‏‫التدبير والتوريد > الموردون > جميع الموردين.</span><span class="sxs-lookup"><span data-stu-id="e4849-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="e4849-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e4849-111">Click New.</span></span>
3. <span data-ttu-id="e4849-112">في الحقل "حساب المورّد‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e4849-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="e4849-113">قد يتم ملء القيمة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="e4849-113">The value may be populated automatically.</span></span> <span data-ttu-id="e4849-114">وإذا حدث ذلك، يمكنك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="e4849-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="e4849-115">يمكنك إنشاء حسابات موردين لشخص أو مؤسسة.</span><span class="sxs-lookup"><span data-stu-id="e4849-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="e4849-116">سيؤثر هذا الحقول المتاحة.</span><span class="sxs-lookup"><span data-stu-id="e4849-116">This will affect which fields are available.</span></span> <span data-ttu-id="e4849-117">في هذا المثال، سنقوم بإنشاء حساب مورد لمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="e4849-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="e4849-118">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e4849-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="e4849-119">إذا كان المورد طرفًا مسجلاً بالفعل في النظام الخاص بك، يمكنك استخدام ميزة الإفلات وتحديده في هذا الحقل وسيرث حساب المورد الجديد في العنوان ومعلومات جهة الاتصال المسجلة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="e4849-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="e4849-120">في الحقل "مجموعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e4849-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="e4849-121">يتم استخدام مجموعة الموردين لمجموعة الموردين التي تشترك في أي من المعلمات التالية: شروط الدفع وفترة التسوية وترحيل المخزون إلى حسابات دفتر الأستاذ بما في ذلك مجموعة ضرائب المبيعات أو حسابات دفتر الأستاذ الافتراضية أو رموز تصفية المنتجات أو تكوين التنبؤ بالتوريد.</span><span class="sxs-lookup"><span data-stu-id="e4849-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="e4849-122">في الحقل "عدد الموظفين"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e4849-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="e4849-123">في الحقل "رقم المؤسسة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e4849-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="e4849-124">إضافة عنوان</span><span class="sxs-lookup"><span data-stu-id="e4849-124">Add an address</span></span>
1. <span data-ttu-id="e4849-125">وسّع المقطع "عناوين".</span><span class="sxs-lookup"><span data-stu-id="e4849-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="e4849-126">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e4849-126">Click Add.</span></span>
3. <span data-ttu-id="e4849-127">في الحقل "الغرض"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e4849-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="e4849-128">بإمكانك تحديد غرض واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="e4849-128">You can select one or more purposes.</span></span> <span data-ttu-id="e4849-129">تستخدم هذه الأغراض لتحديد العنوان الصحيح لغرض معين.</span><span class="sxs-lookup"><span data-stu-id="e4849-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="e4849-130">على سبيل المثال، إذا كان الغرض هو "الفاتورة" فسيتم استخدام عنوانها عند إرسال الفواتير.</span><span class="sxs-lookup"><span data-stu-id="e4849-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="e4849-131">في الحقل "الاسم أو الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e4849-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="e4849-132">في الحقل "البلد/المنطقة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e4849-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="e4849-133">أدخل تفاصيل العنوان.</span><span class="sxs-lookup"><span data-stu-id="e4849-133">Enter the address details.</span></span> <span data-ttu-id="e4849-134">سيحدد البلد/المنطقة التي قمت بتحديدها الحقول التي يتم تقديمك من خلالها، بما يوافق تنسيق العنوان للبلد/المنطقة.</span><span class="sxs-lookup"><span data-stu-id="e4849-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="e4849-135">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e4849-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="e4849-136">إضافة معلومات جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="e4849-136">Add contact information</span></span>
1. <span data-ttu-id="e4849-137">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e4849-137">Click Add.</span></span>
2. <span data-ttu-id="e4849-138">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e4849-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="e4849-139">في الحقل "النوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="e4849-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="e4849-140">في الحقل "‏‫رقم/عنوان جهة الاتصال‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e4849-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="e4849-141">يمكنك تحديد خانة الاختيار الأساسية إذا كانت هذه هي جهة الاتصال الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="e4849-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="e4849-142">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e4849-142">Click Save.</span></span>
6. <span data-ttu-id="e4849-143">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e4849-143">Close the page.</span></span>
7. <span data-ttu-id="e4849-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e4849-144">Close the page.</span></span>

