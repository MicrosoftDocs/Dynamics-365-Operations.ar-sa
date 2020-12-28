---
title: إنشاء حساب مورد
description: يوضح هذا الإجراء كيفية إنشاء حساب مورد، وإضافة عنوان ومعلومات الاتصال.
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd8cd2bb7b03c0415a5c5656f0e3ffada961973e
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4421798"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="7eae4-103">إنشاء حساب مورد</span><span class="sxs-lookup"><span data-stu-id="7eae4-103">Create a vendor account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7eae4-104">يوضح هذا الإجراء كيفية إنشاء حساب مورد، وإضافة عنوان ومعلومات الاتصال.</span><span class="sxs-lookup"><span data-stu-id="7eae4-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="7eae4-105">ولا يوضح الإجراء كيفية ملء جميع الحقول لأغراض المشتريات والأغراض المالية.</span><span class="sxs-lookup"><span data-stu-id="7eae4-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="7eae4-106">للتعرف على مزيد من المعلومات حول هذه الحقول، الرجاء قراءة أوصاف الحقول.</span><span class="sxs-lookup"><span data-stu-id="7eae4-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="7eae4-107">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="7eae4-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="7eae4-108">يتم إنشاء حسابات الموردين عادة بواسطة عاملين محترفين أو عاملي الحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="7eae4-109">إنشاء حساب مورد</span><span class="sxs-lookup"><span data-stu-id="7eae4-109">Create a vendor account</span></span>
1. <span data-ttu-id="7eae4-110">انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد > المورّدون‬ > كافة المورّدين‬**.</span><span class="sxs-lookup"><span data-stu-id="7eae4-110">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="7eae4-111">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7eae4-111">Click **New**.</span></span>
3. <span data-ttu-id="7eae4-112">في حقل **حساب المورّد**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-112">In the **Vendor account** field, type a value.</span></span>
    - <span data-ttu-id="7eae4-113">قد يتم ملء القيمة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="7eae4-113">The value may be populated automatically.</span></span> <span data-ttu-id="7eae4-114">وإذا حدث ذلك، يمكنك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-114">If so, you can skip this step.</span></span>  
    - <span data-ttu-id="7eae4-115">يمكنك إنشاء حسابات موردين لشخص أو مؤسسة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="7eae4-116">سيؤثر هذا الحقول المتاحة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-116">This will affect which fields are available.</span></span> <span data-ttu-id="7eae4-117">في هذا المثال، سنقوم بإنشاء حساب مورد لمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-117">In this example, we'll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="7eae4-118">في الحقل **الاسم** أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7eae4-118">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="7eae4-119">إذا كان المورد طرفًا مسجلاً بالفعل في النظام الخاص بك، يمكنك استخدام ميزة الإفلات وتحديده في هذا الحقل وسيرث حساب المورد الجديد في العنوان ومعلومات جهة الاتصال المسجلة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="7eae4-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that's already registered.</span></span>
5. <span data-ttu-id="7eae4-120">في الحقل **مجموعة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7eae4-120">In the **Group** field, enter or select a value.</span></span> <span data-ttu-id="7eae4-121">يتم استخدام مجموعة الموردين لمجموعة الموردين التي تشترك في أي من المعلمات التالية: شروط الدفع وفترة التسوية وترحيل المخزون إلى حسابات دفتر الأستاذ بما في ذلك مجموعة ضرائب المبيعات أو حسابات دفتر الأستاذ الافتراضية أو رموز تصفية المنتجات أو تكوين التنبؤ بالتوريد.</span><span class="sxs-lookup"><span data-stu-id="7eae4-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment, settle period, inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>
6. <span data-ttu-id="7eae4-122">في الحقل **عدد الموظفين**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7eae4-122">In the **Number of employees** field, enter a number.</span></span>
7. <span data-ttu-id="7eae4-123">في الحقل **رقم المؤسسة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-123">In the **Organization number** field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="7eae4-124">إضافة عنوان</span><span class="sxs-lookup"><span data-stu-id="7eae4-124">Add an address</span></span>
1. <span data-ttu-id="7eae4-125">وسّع القسم **عناوين**.</span><span class="sxs-lookup"><span data-stu-id="7eae4-125">Expand the **Addresses** section.</span></span>
2. <span data-ttu-id="7eae4-126">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="7eae4-126">Click **Add**.</span></span>
3. <span data-ttu-id="7eae4-127">في الحقل **الغرض**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7eae4-127">In the **Purpose** field, enter or select a value.</span></span> <span data-ttu-id="7eae4-128">بإمكانك تحديد غرض واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="7eae4-128">You can select one or more purposes.</span></span> <span data-ttu-id="7eae4-129">تستخدم هذه الأغراض لتحديد العنوان الصحيح لغرض معين.</span><span class="sxs-lookup"><span data-stu-id="7eae4-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="7eae4-130">على سبيل المثال، إذا كان الغرض هو "الفاتورة" فسيتم استخدام عنوانها عند إرسال الفواتير.</span><span class="sxs-lookup"><span data-stu-id="7eae4-130">For example, if the purpose is "Invoice" that address will be used when you send invoices.</span></span>
4. <span data-ttu-id="7eae4-131">في الحقل **الاسم أو الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-131">In the **Name or description** field, type a value.</span></span>
5. <span data-ttu-id="7eae4-132">في الحقل **البلد/المنطقة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7eae4-132">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="7eae4-133">أدخل تفاصيل العنوان.</span><span class="sxs-lookup"><span data-stu-id="7eae4-133">Enter the address details.</span></span> <span data-ttu-id="7eae4-134">سيحدد البلد/المنطقة التي قمت بتحديدها الحقول التي يتم تقديمك من خلالها، بما يوافق تنسيق العنوان للبلد/المنطقة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span> 
6. <span data-ttu-id="7eae4-135">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7eae4-135">Click **OK**.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="7eae4-136">إضافة معلومات جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="7eae4-136">Add contact information</span></span>
1. <span data-ttu-id="7eae4-137">وسّع قسم **معلومات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="7eae4-137">Expand the **Contact information** section.</span></span>
2. <span data-ttu-id="7eae4-138">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="7eae4-138">Click **Add**.</span></span>
3. <span data-ttu-id="7eae4-139">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-139">In the **Description** field, type a value.</span></span>
4. <span data-ttu-id="7eae4-140">في الحقل **النوع**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="7eae4-140">In the **Type** field, select an option.</span></span>
5. <span data-ttu-id="7eae4-141">في الحقل **‏‫رقم/عنوان جهة الاتصال**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-141">In the **Contact number/address** field, type a value.</span></span> <span data-ttu-id="7eae4-142">يمكنك تحديد خانة الاختيار الأساسية إذا كانت هذه هي جهة الاتصال الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="7eae4-142">You can select the Primary check box if this is the primary contact.</span></span>  
6. <span data-ttu-id="7eae4-143">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="7eae4-143">Click **Save**.</span></span>
7. <span data-ttu-id="7eae4-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-144">Close the page.</span></span>
8. <span data-ttu-id="7eae4-145">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7eae4-145">Close the page.</span></span>

