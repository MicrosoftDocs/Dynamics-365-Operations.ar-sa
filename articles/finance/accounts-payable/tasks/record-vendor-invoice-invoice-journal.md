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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140365"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="ef909-103">تسجيل فاتورة مورّد في دفتر يومية الفواتير</span><span class="sxs-lookup"><span data-stu-id="ef909-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef909-104">سيظهر دليل المهمة هذا كيفية تسجيل فواتير المورّدين غير المقترنة بأوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="ef909-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="ef909-105">تتضمن أمثلة هذا النوع من الفواتير مصروفات الإمدادات أو الخدمات.</span><span class="sxs-lookup"><span data-stu-id="ef909-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="ef909-106">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="ef909-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="ef909-107">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات الدائنة > مساحات العمل > إدخال فاتورة المورّد‬**.</span><span class="sxs-lookup"><span data-stu-id="ef909-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="ef909-108">انقر فوق **دفتر يومية الفاتورة الجديدة‬** في **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="ef909-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="ef909-109">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ef909-109">Click **New**.</span></span>
4. <span data-ttu-id="ef909-110">في الحقل **الاسم**، أدخل اسم دفتر اليومية أو انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="ef909-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="ef909-111">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ef909-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="ef909-112">في **جزء الإجراءات**، انقر فوق **البنود**.</span><span class="sxs-lookup"><span data-stu-id="ef909-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="ef909-113">في الحقل **التاريخ**، أدخل تاريخ الترحيل الذي سيقوم بتحديث دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="ef909-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="ef909-114">في حقل **الحساب**، حدد **حساب المورّد**.</span><span class="sxs-lookup"><span data-stu-id="ef909-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="ef909-115">في الحقل **الفاتورة**، أدخل رقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="ef909-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="ef909-116">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ef909-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="ef909-117">في الحقل **دائن**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="ef909-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="ef909-118">في الحقل **حساب مقابل**، أدخل رقم الحساب أو انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="ef909-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="ef909-119">ستأتي **مجموعة ضريبة المبيعات** بشكل افتراضي من حساب المورّد.</span><span class="sxs-lookup"><span data-stu-id="ef909-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="ef909-120">ستأتي **مجموعة ضرائب مبيعات الأصناف** بشكل افتراضي من الحساب الرئيسي المحدد في الحقل **حساب مقابل**.</span><span class="sxs-lookup"><span data-stu-id="ef909-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="ef909-121">سيتم حساب **تاريخ الاستحقاق** استنادًا إلى شروط الدفع.</span><span class="sxs-lookup"><span data-stu-id="ef909-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="ef909-122">سيأتي **الخصم النقدي** بشكل افتراضي من حساب المورّد.</span><span class="sxs-lookup"><span data-stu-id="ef909-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="ef909-123">انقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="ef909-123">Click **Post**.</span></span>
13. <span data-ttu-id="ef909-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ef909-124">Close the page.</span></span>

