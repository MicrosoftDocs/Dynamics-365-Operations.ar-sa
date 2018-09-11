--- 
title: "تسجيل فاتورة مورّد في دفتر يومية الفواتير"
description: "سيظهر دليل المهمة هذا كيفية تسجيل فواتير المورّدين غير المقترنة بأوامر الشراء."
author: abruer
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 9109144feee2cb5c813e00a04e78e4291d7f3bfd
ms.contentlocale: ar-sa
ms.lasthandoff: 09/11/2018

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="acef7-103">تسجيل فاتورة مورّد في دفتر يومية الفواتير</span><span class="sxs-lookup"><span data-stu-id="acef7-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="acef7-104">سيظهر دليل المهمة هذا كيفية تسجيل فواتير المورّدين غير المقترنة بأوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="acef7-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="acef7-105">تتضمن أمثلة هذا النوع من الفواتير مصروفات الإمدادات أو الخدمات.</span><span class="sxs-lookup"><span data-stu-id="acef7-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="acef7-106">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="acef7-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="acef7-107">انتقل إلى الحسابات الدائنة > مساحات العمل > إدخال فاتورة المورّدين.</span><span class="sxs-lookup"><span data-stu-id="acef7-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="acef7-108">انقر فوق "دفتر يومية الفاتورة الجديدة".</span><span class="sxs-lookup"><span data-stu-id="acef7-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="acef7-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="acef7-109">Click New.</span></span>
4. <span data-ttu-id="acef7-110">في الحقل "الاسم"، أدخل اسم دفتر اليومية أو انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="acef7-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="acef7-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="acef7-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="acef7-112">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="acef7-112">Click Lines.</span></span>
    * <span data-ttu-id="acef7-113">في الحقل "التاريخ"، أدخل تاريخ الترحيل الذي سيقوم بتحديث دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="acef7-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="acef7-114">في حقل "الحساب"، حدد اسم المورّد.</span><span class="sxs-lookup"><span data-stu-id="acef7-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="acef7-115">في الحقل "الفاتورة"، أدخل رقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="acef7-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="acef7-116">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="acef7-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="acef7-117">في الحقل "دائن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="acef7-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="acef7-118">في الحقل "حساب مقابل"، أدخل رقم الحساب أو انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="acef7-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="acef7-119">ستأتي مجموعة ضريبة المبيعات بشكل افتراضي من حساب المورّد.</span><span class="sxs-lookup"><span data-stu-id="acef7-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="acef7-120">ستأتي مجموعة ضرائب مبيعات الأصناف بشكل افتراضي من الحساب الرئيسي المحدد في الحقل "حساب مقابل".</span><span class="sxs-lookup"><span data-stu-id="acef7-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="acef7-121">سيتم حساب "تاريخ الاستحقاق" استنادًا إلى شروط الدفع.</span><span class="sxs-lookup"><span data-stu-id="acef7-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="acef7-122">سيأتي الخصم النقدي بشكل افتراضي من حساب المورّد.</span><span class="sxs-lookup"><span data-stu-id="acef7-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="acef7-123">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="acef7-123">Click Post.</span></span>
13. <span data-ttu-id="acef7-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="acef7-124">Close the page.</span></span>


