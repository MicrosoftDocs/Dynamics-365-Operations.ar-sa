---
title: إنشاء وتصدير دفعات المورّد باستخدام تنسيق الدفع ISO20022
description: يوضح هذا الإجراء كيفية إنشاء بنود الدفع في دفتر يومية دفع المورّد وإنشاء ملف دفع المورّد باستخدام مثال تحوي الائتمان ISO2022.
author: mrolecki
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18c7d0b6c5c6a7f598f4b94f4dcf02df498d74cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822695"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="1dfb6-103">إنشاء وتصدير دفعات المورّد باستخدام تنسيق الدفع ISO20022</span><span class="sxs-lookup"><span data-stu-id="1dfb6-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1dfb6-104">يوضح هذا الموضوع كيفية إنشاء بنود الدفع في دفتر يومية دفع المورّد وإنشاء ملف دفع المورّد باستخدام مثال تحويل الائتمان ISO2022.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="1dfb6-105">هذا هو الإجراء الخامس من ضمن الإجراءات الخمسة، هدفه توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="1dfb6-106">استخدم شركة بيانات العرض التوضيحي DEMF لإكمال هذا المثال.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="1dfb6-107">مثال</span><span class="sxs-lookup"><span data-stu-id="1dfb6-107">Example</span></span>

1.    <span data-ttu-id="1dfb6-108">انتقل إلى **الحسابات الدائنة > المدفوعات‬ > دفتر يومية المدفوعات‬**.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.    <span data-ttu-id="1dfb6-109">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-109">Click **New**.</span></span>
3.    <span data-ttu-id="1dfb6-110">في الحقل **الاسم** أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-110">In the **Name** field, enter or select a value.</span></span>
4.    <span data-ttu-id="1dfb6-111">انقر فوق **البنود > مقترح الدفع > إنشاء مقترح الدفع**.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.    <span data-ttu-id="1dfb6-112">وسّع القسم **السجلات المطلوب تضمينها**.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-112">Expand the **Records to include** section.</span></span>
6.    <span data-ttu-id="1dfb6-113">انقر فوق **تصفية**.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-113">Click **Filter**.</span></span>
7.    <span data-ttu-id="1dfb6-114">في القائمة، حدد صف **جدول المورّدين** وحقل **حساب المورّد**.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.    <span data-ttu-id="1dfb6-115">في الحقل **المعايير‬**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="1dfb6-116">يمكنك تطبيق أي معايير لتحديد حركات المورّد للدفع، لهذا لمثال استخدم DE-001 كحساب مورّد.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12.    <span data-ttu-id="1dfb6-117">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-117">Click **OK**.</span></span>
13.    <span data-ttu-id="1dfb6-118">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-118">Click **OK**.</span></span>
14.    <span data-ttu-id="1dfb6-119">انقر فوق **إنشاء مدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="1dfb6-120">أنشئ ملف دفع ISO20022.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-120">Generate an ISO20022 payment file.</span></span>
    1.    <span data-ttu-id="1dfb6-121">انقر فوق **إنشاء مدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-121">Click **Generate payments**.</span></span>
    2.    <span data-ttu-id="1dfb6-122">في الحقل **أسلوب الدفع**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.    <span data-ttu-id="1dfb6-123">في الحقل **اسم الملف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="1dfb6-124">بالنسبة إلى هذا المثال، نظراً للدفع باليورو، سيكون الملف الذي تم إنشاؤه متوافقًا مع SEPA.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="1dfb6-125">يمكن أيضًا استخدام تحويل الائتمان ISO20022 بالإضافة إلى تنسيقات دفع أخرى خاصة بالمورّد لإنشاء مدفوعات بعملات أخرى.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.    <span data-ttu-id="1dfb6-126">في الحقل **الحساب البنكي**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1dfb6-126">In the **Bank account** field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]