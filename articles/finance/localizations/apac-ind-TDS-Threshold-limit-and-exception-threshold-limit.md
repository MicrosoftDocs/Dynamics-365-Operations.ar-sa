---
title: الحد وحد استثنائي
description: يصف هذا الموضوع الحد والحدود الاستثنائية للضريبة المخصومة في المصدر (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1bf0d3a01ede559d288581d3b58b3777d0e608dc
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022992"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a><span data-ttu-id="90111-103">الحد وحد استثنائي</span><span class="sxs-lookup"><span data-stu-id="90111-103">Threshold limit and exception threshold limit</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90111-104">يصف هذا الموضوع الحد والحدود الاستثنائية للضريبة المخصومة في المصدر (TDS).</span><span class="sxs-lookup"><span data-stu-id="90111-104">This topic describes the threshold and exception limits for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="90111-105">يتم حساب TDS في الفواتير والمدفوعات دائمًا باعتبار الحد والحد الاستثنائي المحدد لمكونات الضريبة TDS في الصفحة **مكونات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="90111-105">The TDS on invoices and payments is always calculated considering the threshold limit and exception threshold limit defined for the TDS tax components on the **Withholding tax components** page.</span></span> <span data-ttu-id="90111-106">يتم إرفاق مكونات ضريبة TDS بأكواد ضريبة TDS، والتي يتم تضمينها في مجموعات ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="90111-106">The TDS tax components are attached to TDS tax codes, which are included in the TDS tax groups.</span></span> <span data-ttu-id="90111-107">يتم إرفاق مجموعات ضريبة TDS بالموردين والعملاء لحساب TDS على مستوى الفاتورة أو مستوى الدفع.</span><span class="sxs-lookup"><span data-stu-id="90111-107">The TDS tax groups are attached to vendors and customers to calculate TDS at the invoice-level or payment-level.</span></span>

<span data-ttu-id="90111-108">يتم حساب TDS إذا كان مبلغ الحركة أو الحركات التراكمية التي تم ترحيلها باستخدام مجموعة TDS محددة لمورد يتجاوز الحد المعين في الصفحة **مكونات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="90111-108">TDS is calculated if the amount for a transaction or the cumulative transactions posted with a specific TDS group for a vendor exceeds the threshold limit specified on the **Withholding tax components** page.</span></span> <span data-ttu-id="90111-109">لن يتم حساب TDS حتى يتجاوز مبلغ الحركة التراكمية الحد المعين.</span><span class="sxs-lookup"><span data-stu-id="90111-109">TDS will not be calculated until the cumulative transaction amount exceeds the specified threshold limit.</span></span>

<span data-ttu-id="90111-110">إذا تم تحديد الحد الاستثنائي بالإضافة إلى الحد لمكون TDS، يتم حساب TDS عندما يتجاوز مبلغ حركة معين الحد الاستثنائي حتى وإن لم يتجاوز مبلغ الحركة التراكمية الحد المعين.</span><span class="sxs-lookup"><span data-stu-id="90111-110">If an exception threshold limit is specified along with the threshold limit for a TDS component, TDS is calculated when a specific transaction amount exceeds the exception threshold limit even if the cumulative transaction amount does not exceed the specified threshold limit.</span></span>

### <a name="example"></a><span data-ttu-id="90111-111">مثال</span><span class="sxs-lookup"><span data-stu-id="90111-111">Example</span></span>
<span data-ttu-id="90111-112">يتم إعداد مكون الضريبة يسمى TDS وإرفاقه بمجموعة ضريبة TDS والتي تسمى المقاول.</span><span class="sxs-lookup"><span data-stu-id="90111-112">A tax component called TDS is set up and attached to the TDS tax group called Contractor.</span></span> <span data-ttu-id="90111-113">تم تحديد الحد على أنه 50.000 وتم تعريف الحد الاستثنائي على أنها 20.000 لمكون ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="90111-113">The threshold has been defined as 50,000 and exception threshold has been defined as 20,000 for TDS tax component.</span></span> <span data-ttu-id="90111-114">يتم تحديد مقاول مجموعة TDS كمجموعة TDS الافتراضية للمورد 1.</span><span class="sxs-lookup"><span data-stu-id="90111-114">The TDS group contractor is defined as the default TDS group for vendor 1.</span></span>

<span data-ttu-id="90111-115">يتم ترحيل فاتورة الشراء 001 لمورد 1 لـ 10000.</span><span class="sxs-lookup"><span data-stu-id="90111-115">A purchase invoice 001 is posted for vendor 1 for 10000.</span></span> <span data-ttu-id="90111-116">لم يتم حساب TDS للفاتورة نظرًا لعدم عبور مبلغ الفاتورة للحد أو الحد الاستثنائي.</span><span class="sxs-lookup"><span data-stu-id="90111-116">TDS is not calculated for the invoice because the invoice amount has not crossed the threshold limit or exception threshold limit.</span></span> <span data-ttu-id="90111-117">يتم ترحيل فاتورة الشراء 002 لمورد 1 لـ 25.000.</span><span class="sxs-lookup"><span data-stu-id="90111-117">A purchase invoice 002 is posted for vendor 1 for 25,000.</span></span> <span data-ttu-id="90111-118">لم يتم حساب TDS للفاتورة نظرًا لعدم تجاوز مبلغ الفاتورة للحد الاستثنائي.</span><span class="sxs-lookup"><span data-stu-id="90111-118">TDS is calculated for the invoice because the invoice amount has crossed the exception threshold limit.</span></span> <span data-ttu-id="90111-119">يتم ترحيل فاتورة الشراء 003 لمورد 1 لـ 20.000.</span><span class="sxs-lookup"><span data-stu-id="90111-119">A purchase invoice 003 is posted for Vendor 1 for 20,000.</span></span> <span data-ttu-id="90111-120">يتم حساب TDS للفاتورة نظرًا لأن مبلغ الفاتورة الإجمالي للفواتير الثلاثة التي يتم إصدارها للمورد قد تجاوز الحد.</span><span class="sxs-lookup"><span data-stu-id="90111-120">TDS is calculated for the invoice because the total invoice amount of the three invoices that are issued for the vendor has crossed the threshold limit.</span></span> <span data-ttu-id="90111-121">يتم حساب TDS في كافة الفواتير التي يتم إصدارها للمورد الذي لم يتم حساب TDS عليه في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="90111-121">TDS is calculated on all invoices that are issued for the vendor on which the TDS has not been calculated earlier.</span></span> <span data-ttu-id="90111-122">وبالتالي، يتم حساب TDS على 30.000، وهو مبلغ الفاتورة الإجمالي للفاتورتين 001 و 003.</span><span class="sxs-lookup"><span data-stu-id="90111-122">Therefore, TDS is calculated on 30,000, which is the total invoice amount of invoice 001 and 003.</span></span>

<span data-ttu-id="90111-123">لا يتم اعتبار الحد والحد الاستثنائي لحساب TDS إذا تم تحديد خانة الاختيار **حد الاطلاع** لأكواد ضريبة TDS في المجموعة TDS التي يتم إرفاقها بالحركة.</span><span class="sxs-lookup"><span data-stu-id="90111-123">The threshold limit and exception threshold limit are not considered for the TDS calculation if the **Overlook threshold** check box is selected for TDS tax codes in the TDS group that is attached to the transaction.</span></span> <span data-ttu-id="90111-124">لن يتم استخدام الحد في أكواد ضريبة TDS في المجموعة TDS التي تحتوي على خانة الاختيار **حد الاطلاع**.</span><span class="sxs-lookup"><span data-stu-id="90111-124">The threshold limit won't be used in the TDS tax codes in the TDS group that the **Overlook threshold** check box is for.</span></span>

<span data-ttu-id="90111-125">في حالة تحديد خانة الاختيار **حد الاطلاع** لمجموعة TDS محددة لبعض الفواتير، ولكن لم يتم تحديدها للفواتير الأخرى التي تم إنشاؤها لمورد/عميل محدد، فقد يتم وضع حساب TDS بدون الاطلاع على الحد الخاص ببعض الفواتير في الاعتبار المبلغ التراكمي في كافة الفواتير التي لم يتم حساب TDS فيها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="90111-125">If the **Overlook threshold** check box is selected for a specific TDS group for some invoices, but not selected for other invoices that were created for a specific vendor/customer, the calculation of TDS without overlooking the threshold limit for few invoices may take place considering the cumulative amount on all invoices on which TDS hasn't been calculated earlier.</span></span>

<span data-ttu-id="90111-126">على سبيل المثال، الحد هو 25000.</span><span class="sxs-lookup"><span data-stu-id="90111-126">For example, the threshold limit is 25000.</span></span> <span data-ttu-id="90111-127">يتم إنشاء الفواتير التالية للمورد أ.</span><span class="sxs-lookup"><span data-stu-id="90111-127">The following invoices are created for Vendor A.</span></span>

- <span data-ttu-id="90111-128">الفاتورة 1 – 2.000 – (لم يتم تحديد خانة الاختيار **حد الاطلاع**): لا يتم حساب TDS.</span><span class="sxs-lookup"><span data-stu-id="90111-128">Invoice 1 – 2,0000 – (**Overlook threshold** check box is not selected): TDS is not calculated.</span></span>

- <span data-ttu-id="90111-129">الفاتورة 2 – 4.000 – (يتم تحديد خانة الاختيار **حد الاطلاع**): يتم حساب TDS على 4.000.</span><span class="sxs-lookup"><span data-stu-id="90111-129">Invoice 2 – 4,000 – (**Overlook threshold** check box is selected): TDS is calculated on 4,000.</span></span>

- <span data-ttu-id="90111-130">الفاتورة 2 – 3.000-(لا يتم تحديد خانة الاختيار **حد الاطلاع**): يتم حساب TDS على أنه مبلغ الفاتورة التراكمي، أي ، 27.000 (20000 + 4000 + 3000) يتجاوز الحد.</span><span class="sxs-lookup"><span data-stu-id="90111-130">Invoice 2 – 3,000 – (**Overlook threshold** check box is not selected): TDS is calculated as the cumulative invoice amount, that is, 27,000 (20000+4000+3000) exceeded the threshold limit.</span></span> <span data-ttu-id="90111-131">يتم حساب TDS على المبلغ التراكمي للفواتير التي لم يتم احتساب TDS عليها في وقت سابق، أي، 23.000 (20000 + 3000).</span><span class="sxs-lookup"><span data-stu-id="90111-131">TDS is calculated on the cumulative amount of invoices on which the TDS has not been calculated earlier, that is, 23,000 (20000+3000).</span></span>
