---
title: حساب وتعديل ضريبة المبيعات في فاتورة المورّد
description: يشرح هذا الموضوع كيفية ضبط ضريبة المبيعات على فاتورة مورد في Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2f3521f7bc56659fc6f7a6d47f581ddbfea16523
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139957"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="7ad60-103">حساب وتعديل ضريبة المبيعات في فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="7ad60-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ad60-104">يشرح هذا الموضوع كيفية ضبط ضريبة المبيعات على فاتورة مورّد.</span><span class="sxs-lookup"><span data-stu-id="7ad60-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="7ad60-105">إذا كان المستند المصدر الأصلي يعرض مبالغ ضريبة مختلفة كما تم حسابها، فيمكنك تعديل هذه المبالغ قبل الترحيل.</span><span class="sxs-lookup"><span data-stu-id="7ad60-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="7ad60-106">تستخدم هذه المهمة شركة بيانات العرض التوضيحي DEMF.</span><span class="sxs-lookup"><span data-stu-id="7ad60-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="7ad60-107">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > الفواتير > دفتر يومية الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="7ad60-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="7ad60-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7ad60-108">Select **New**.</span></span>
3. <span data-ttu-id="7ad60-109">في حقل **الاسم** للصف الجديد، حدد خيارًا في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="7ad60-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="7ad60-110">في جزء الإجراءات، حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="7ad60-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="7ad60-111">في حقل **الحساب**، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="7ad60-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="7ad60-112">في حقل **الفاتورة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7ad60-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="7ad60-113">في الحقل **دائن**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7ad60-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="7ad60-114">في الحقل **حساب مقابل**، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="7ad60-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="7ad60-115">حدد **ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="7ad60-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="7ad60-116">في حقل، **المبلغ الإجمالي الفعلي لضريبة المبيعات**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7ad60-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="7ad60-117">على علامة التبويب **تسوية**، يمكن تعديل مبالغ ضريبة المبيعات حسب كل كود ضريبة مبيعات.</span><span class="sxs-lookup"><span data-stu-id="7ad60-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="7ad60-118">حدد **إعادة تعيين القيمة الفعلية من المبالغ المحسوبة**.</span><span class="sxs-lookup"><span data-stu-id="7ad60-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="7ad60-119">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7ad60-119">Select **OK**.</span></span>
14. <span data-ttu-id="7ad60-120">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="7ad60-120">Select **Save**.</span></span>

