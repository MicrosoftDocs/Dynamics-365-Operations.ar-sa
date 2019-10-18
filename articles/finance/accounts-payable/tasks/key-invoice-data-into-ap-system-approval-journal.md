---
title: بيانات الفاتورة الرئيسية في الحسابات الدائنة باستخدام ‏‫دفتر يومية الموافقة
description: يشرح هذا الموضوع كيفية استخدام سجل الفواتير لإنشاء فواتير ثم استخدام دفتر يومية الموافقة لتحديث حسابات المصروفات.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: fb690769a33f88e63ab8f54cec69a5e927fd324c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176290"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="f2378-103">بيانات الفاتورة الرئيسية في الحسابات الدائنة باستخدام ‏‫دفتر يومية الموافقة</span><span class="sxs-lookup"><span data-stu-id="f2378-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2378-104">يشرح هذا الموضوع كيفية استخدام سجل الفواتير لإنشاء فواتير ثم استخدام دفتر يومية الموافقة لتحديث حسابات المصروفات.</span><span class="sxs-lookup"><span data-stu-id="f2378-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="f2378-105">إنشاء فاتورة وترحيلها</span><span class="sxs-lookup"><span data-stu-id="f2378-105">Create and post and invoice</span></span>
1. <span data-ttu-id="f2378-106">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > الفواتير > سجل الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="f2378-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="f2378-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f2378-107">Select **New**.</span></span>
3. <span data-ttu-id="f2378-108">حدد اسم سجل الفواتير الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="f2378-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="f2378-109">حدد **البنود‬** لفتح السجل وإدخال بنود المصروفات.</span><span class="sxs-lookup"><span data-stu-id="f2378-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="f2378-110">حدد موردًا.</span><span class="sxs-lookup"><span data-stu-id="f2378-110">Select a vendor.</span></span> <span data-ttu-id="f2378-111">على سبيل المثال، أدخل أو حدد `US-104`.</span><span class="sxs-lookup"><span data-stu-id="f2378-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="f2378-112">في حقل **الفاتورة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f2378-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="f2378-113">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f2378-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="f2378-114">في الحقل **دائن**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f2378-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="f2378-115">في الحقل **معتمد بواسطة**، حدد معتمدًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="f2378-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="f2378-116">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="f2378-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="f2378-117">الموافقة على فاتورة</span><span class="sxs-lookup"><span data-stu-id="f2378-117">Approve an invoice</span></span>
1. <span data-ttu-id="f2378-118">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > الفواتير > الموافقة على الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="f2378-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="f2378-119">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f2378-119">Select **New**.</span></span>
3. <span data-ttu-id="f2378-120">حدد اسم دفتر يومية الموافقة على الفواتير الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="f2378-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="f2378-121">حدد **البنود** لعرض صفحة حيث يمكنك تحديد الفواتير التي تريد الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="f2378-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="f2378-122">حدد **البحث عن إيصالات** لعرض كافة الفواتير الجاهزة للموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="f2378-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="f2378-123">ضع علامة على الفاتورة التي قمت بإنشائها، ثم انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="f2378-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="f2378-124">يتم نقل الإيصالات التي حددتها أعلاه إلى هذه القائمة بعد تحديدها.</span><span class="sxs-lookup"><span data-stu-id="f2378-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="f2378-125">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f2378-125">Select **OK**.</span></span>
8. <span data-ttu-id="f2378-126">حدد حقل **رقم الحساب** لإضافة حساب مصروفات للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="f2378-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="f2378-127">أدخل رقم حساب، واضغط على علامة جدولة للخروج من الحقل.</span><span class="sxs-lookup"><span data-stu-id="f2378-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="f2378-128">على سبيل المثال، أدخل `600120`.</span><span class="sxs-lookup"><span data-stu-id="f2378-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="f2378-129">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="f2378-129">Select **Post**.</span></span>
11. <span data-ttu-id="f2378-130">حدد **الإيصال** لعرض الإدخالات التي تم ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="f2378-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="f2378-131">يتم عكس حساب "الفاتورة المعلقة للموافقة" واستبداله بحساب المصروفات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="f2378-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

