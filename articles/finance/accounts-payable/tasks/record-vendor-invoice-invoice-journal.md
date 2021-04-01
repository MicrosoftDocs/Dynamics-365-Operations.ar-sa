---
title: تسجيل فاتورة مورّد في دفتر يومية الفواتير
description: سيظهر دليل المهمة هذا كيفية تسجيل فواتير المورّدين غير المقترنة بأوامر الشراء.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a60a5959046ca9e953bac80aaeb382d07a267643
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227126"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="6f3b2-103">تسجيل فاتورة مورّد في دفتر يومية الفواتير</span><span class="sxs-lookup"><span data-stu-id="6f3b2-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f3b2-104">سيظهر دليل المهمة هذا كيفية تسجيل فواتير المورّدين غير المقترنة بأوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="6f3b2-105">تتضمن أمثلة هذا النوع من الفواتير مصروفات الإمدادات أو الخدمات.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="6f3b2-106">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="6f3b2-107">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات الدائنة > مساحات العمل > إدخال فاتورة المورّد‬**.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="6f3b2-108">انقر فوق **دفتر يومية الفاتورة الجديدة‬** في **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="6f3b2-109">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-109">Click **New**.</span></span>
4. <span data-ttu-id="6f3b2-110">في الحقل **الاسم**، أدخل اسم دفتر اليومية أو انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="6f3b2-111">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="6f3b2-112">في **جزء الإجراءات**، انقر فوق **البنود**.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="6f3b2-113">في الحقل **التاريخ**، أدخل تاريخ الترحيل الذي سيقوم بتحديث دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="6f3b2-114">في حقل **الحساب**، حدد **حساب المورّد**.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="6f3b2-115">في الحقل **الفاتورة**، أدخل رقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="6f3b2-116">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="6f3b2-117">في الحقل **دائن**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="6f3b2-118">في الحقل **حساب مقابل**، أدخل رقم الحساب أو انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="6f3b2-119">ستأتي **مجموعة ضريبة المبيعات** بشكل افتراضي من حساب المورّد.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="6f3b2-120">ستأتي **مجموعة ضرائب مبيعات الأصناف** بشكل افتراضي من الحساب الرئيسي المحدد في الحقل **حساب مقابل**.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="6f3b2-121">سيتم حساب **تاريخ الاستحقاق** استنادًا إلى شروط الدفع.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="6f3b2-122">سيأتي **الخصم النقدي** بشكل افتراضي من حساب المورّد.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="6f3b2-123">إذا كنت قد قمت بتمكين سير عمل دفتر يومية فاتورة المورد، انقر فوق **سير العمل > إرسال**.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="6f3b2-124">عندما يتم اعتماد الإرسال الخاص بك، سيكون التاريخ متقدمًا لأول يوم في الفترة المفتوحة التالية، إذا كان تاريخ ترحيل الحركة يقع في فترة قيد الانتظار أو مغلق لترحيل دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="6f3b2-125">انقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-125">Click **Post**.</span></span>
13. <span data-ttu-id="6f3b2-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6f3b2-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]