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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03313d875d23489b3293376dd94f808c73a4bd15
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439775"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="186d9-103">حساب وتعديل ضريبة المبيعات في فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="186d9-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="186d9-104">يشرح هذا الموضوع كيفية ضبط ضريبة المبيعات على فاتورة مورّد.</span><span class="sxs-lookup"><span data-stu-id="186d9-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="186d9-105">إذا كان المستند المصدر الأصلي يعرض مبالغ ضريبة مختلفة كما تم حسابها، فيمكنك تعديل هذه المبالغ قبل الترحيل.</span><span class="sxs-lookup"><span data-stu-id="186d9-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="186d9-106">تستخدم هذه المهمة شركة بيانات العرض التوضيحي DEMF.</span><span class="sxs-lookup"><span data-stu-id="186d9-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="186d9-107">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > الفواتير > دفتر يومية الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="186d9-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="186d9-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="186d9-108">Select **New**.</span></span>
3. <span data-ttu-id="186d9-109">في حقل **الاسم** للصف الجديد، حدد خيارًا في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="186d9-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="186d9-110">في جزء الإجراءات، حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="186d9-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="186d9-111">في حقل **الحساب**، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="186d9-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="186d9-112">في حقل **الفاتورة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="186d9-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="186d9-113">في الحقل **دائن**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="186d9-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="186d9-114">في الحقل **حساب مقابل**، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="186d9-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="186d9-115">حدد **ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="186d9-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="186d9-116">في حقل، **المبلغ الإجمالي الفعلي لضريبة المبيعات**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="186d9-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="186d9-117">على علامة التبويب **تسوية**، يمكن تعديل مبالغ ضريبة المبيعات حسب كل كود ضريبة مبيعات.</span><span class="sxs-lookup"><span data-stu-id="186d9-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="186d9-118">حدد **إعادة تعيين القيمة الفعلية من المبالغ المحسوبة**.</span><span class="sxs-lookup"><span data-stu-id="186d9-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="186d9-119">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="186d9-119">Select **OK**.</span></span>
14. <span data-ttu-id="186d9-120">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="186d9-120">Select **Save**.</span></span>

