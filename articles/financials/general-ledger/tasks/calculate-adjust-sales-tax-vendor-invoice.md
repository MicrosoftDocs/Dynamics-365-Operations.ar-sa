---
title: حساب وتعديل ضريبة المبيعات في فاتورة المورّد
description: إذا كان المستند المصدر الأصلي يعرض مبالغ ضريبة مختلفة كما تم حسابها، فيمكنك تعديل هذه المبالغ قبل الترحيل.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545161"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="89bb4-103">حساب وتعديل ضريبة المبيعات في فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="89bb4-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89bb4-104">إذا كان المستند المصدر الأصلي يعرض مبالغ ضريبة مختلفة كما تم حسابها، فيمكنك تعديل هذه المبالغ قبل الترحيل.</span><span class="sxs-lookup"><span data-stu-id="89bb4-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="89bb4-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي DEMF.</span><span class="sxs-lookup"><span data-stu-id="89bb4-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="89bb4-106">انتقل إلى الحسابات الدائنة > الفواتير > دفتر يومية الفواتير‬.</span><span class="sxs-lookup"><span data-stu-id="89bb4-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="89bb4-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="89bb4-107">Click New.</span></span>
3. <span data-ttu-id="89bb4-108">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="89bb4-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="89bb4-109">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="89bb4-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="89bb4-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="89bb4-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="89bb4-111">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="89bb4-111">Click Lines.</span></span>
7. <span data-ttu-id="89bb4-112">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="89bb4-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="89bb4-113">في حقل "الحساب"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="89bb4-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="89bb4-114">في الحقل "الفاتورة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="89bb4-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="89bb4-115">في الحقل "دائن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="89bb4-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="89bb4-116">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="89bb4-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="89bb4-117">انقر فوق "ضريبة المبيعات".</span><span class="sxs-lookup"><span data-stu-id="89bb4-117">Click Sales tax.</span></span>
13. <span data-ttu-id="89bb4-118">في الحقل "المبلغ الإجمالي الفعلي لضريبة المبيعات‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="89bb4-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="89bb4-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="89bb4-119">Click OK.</span></span>
15. <span data-ttu-id="89bb4-120">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="89bb4-120">Click Save.</span></span>
16. <span data-ttu-id="89bb4-121">انقر فوق "ضريبة المبيعات".</span><span class="sxs-lookup"><span data-stu-id="89bb4-121">Click Sales tax.</span></span>
17. <span data-ttu-id="89bb4-122">ضمن علامة التبويب "تسوية"، يمكن تعديل مبالغ ضريبة المبيعات لكل كل كود ضريبة مبيعات.</span><span class="sxs-lookup"><span data-stu-id="89bb4-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="89bb4-123">انقر فوق "إعادة تعيين القيمة الفعلية من المبالغ المحسوبة‬".</span><span class="sxs-lookup"><span data-stu-id="89bb4-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="89bb4-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="89bb4-124">Click OK.</span></span>
20. <span data-ttu-id="89bb4-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="89bb4-125">Click Save.</span></span>

