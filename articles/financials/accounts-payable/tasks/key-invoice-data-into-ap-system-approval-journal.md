---
title: بيانات الفاتورة الرئيسية في نظام الحسابات الدائنة باستخدام دفتر يومية الموافقة
description: يوضح دليل المهمة هذا كيفية استخدام سجل الفواتير لإنشاء فواتير ثم استخدام دفتر يومية الموافقة لتحديث حسابات المصروفات.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0faece510cc85fd86113d8b62d54b71f3014b1db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837026"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="a0200-103">بيانات الفاتورة الرئيسية في نظام الحسابات الدائنة باستخدام دفتر يومية الموافقة</span><span class="sxs-lookup"><span data-stu-id="a0200-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0200-104">يوضح دليل المهمة هذا كيفية استخدام سجل الفواتير لإنشاء فواتير ثم استخدام دفتر يومية الموافقة لتحديث حسابات المصروفات.</span><span class="sxs-lookup"><span data-stu-id="a0200-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="a0200-105">إنشاء فاتورة وترحيلها</span><span class="sxs-lookup"><span data-stu-id="a0200-105">Create and post and invoice</span></span>
1. <span data-ttu-id="a0200-106">انتقل إلى الحسابات الدائنة > الفواتير > سجل الفواتير.</span><span class="sxs-lookup"><span data-stu-id="a0200-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="a0200-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a0200-107">Click New.</span></span>
3. <span data-ttu-id="a0200-108">حدد اسم سجل الفواتير الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="a0200-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="a0200-109">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="a0200-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a0200-110">انقر فوق "البنود‬" لفتح السجل وإدخال بنود المصروفات.</span><span class="sxs-lookup"><span data-stu-id="a0200-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="a0200-111">حدد موردًا.</span><span class="sxs-lookup"><span data-stu-id="a0200-111">Select a vendor.</span></span> <span data-ttu-id="a0200-112">على سبيل المثال، أدخل أو حدد US-104</span><span class="sxs-lookup"><span data-stu-id="a0200-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="a0200-113">في الحقل "الفاتورة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a0200-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="a0200-114">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a0200-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="a0200-115">في الحقل "دائن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="a0200-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="a0200-116">في الحقل "تمت الموافقة بواسطة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="a0200-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="a0200-117">ميّز أحد المعتمِدين ثم انقر فوق "تحديد" لتحديده.</span><span class="sxs-lookup"><span data-stu-id="a0200-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="a0200-118">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="a0200-118">Click Post.</span></span>
13. <span data-ttu-id="a0200-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a0200-119">Close the page.</span></span>
14. <span data-ttu-id="a0200-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a0200-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="a0200-121">الموافقة على فاتورة</span><span class="sxs-lookup"><span data-stu-id="a0200-121">Approve an invoice</span></span>
1. <span data-ttu-id="a0200-122">انتقل إلى الحسابات الدائنة > الفواتير > الموافقة على الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="a0200-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="a0200-123">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a0200-123">Click New.</span></span>
3. <span data-ttu-id="a0200-124">حدد اسم دفتر يومية الموافقة على الفواتير الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="a0200-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="a0200-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="a0200-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a0200-126">انقر فوق "البنود" لعرض صفحة حيث يمكنك تحديد الفواتير التي تريد الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="a0200-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="a0200-127">حدد "البحث عن إيصالات" لعرض كافة الفواتير الجاهزة للموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="a0200-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="a0200-128">ضع علامة على الفاتورة التي قمت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="a0200-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="a0200-129">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="a0200-129">Click Select.</span></span>
    * <span data-ttu-id="a0200-130">يتم نقل الإيصالات التي حددتها أعلاه إلى هذه القائمة بعد تحديدها.</span><span class="sxs-lookup"><span data-stu-id="a0200-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="a0200-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a0200-131">Click OK.</span></span>
10. <span data-ttu-id="a0200-132">انقر فوق حقل "رقم الحساب" لإضافة حساب مصروفات للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="a0200-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="a0200-133">أدخل رقم حساب، واضغط على علامة جدولة للخروج من الحقل.</span><span class="sxs-lookup"><span data-stu-id="a0200-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="a0200-134">على سبيل المثال، أدخل 600120.</span><span class="sxs-lookup"><span data-stu-id="a0200-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="a0200-135">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="a0200-135">Click Post.</span></span>
13. <span data-ttu-id="a0200-136">انقر فوق "الإيصال" لعرض الإدخالات التي تم ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="a0200-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="a0200-137">يتم عكس حساب "الفاتورة المعلقة للموافقة" واستبداله بحساب المصروفات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="a0200-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

