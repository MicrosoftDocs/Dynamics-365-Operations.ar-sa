---
title: إنشاء وترحيل فواتير النص الحر المكررة
description: يتم استخدام الفواتير المتكررة لفوترة العملاء بشكل منتظم لنفس المبلغ.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysLookupMultiSelectGrid, CustRecurrenceInvoiceGroup, CustFreeInvoice, CustRecurrenceInvoiceTotals
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3b31dbf296a06ea6253a8ae71bfea6193a1e03e
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138013"
---
# <a name="generate-and-post-recurring-free-text-invoices"></a><span data-ttu-id="fce9f-103">إنشاء وترحيل فواتير النص الحر المكررة</span><span class="sxs-lookup"><span data-stu-id="fce9f-103">Generate and post recurring free text invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fce9f-104">يتم استخدام الفواتير المتكررة لفوترة العملاء بشكل منتظم لنفس المبلغ.</span><span class="sxs-lookup"><span data-stu-id="fce9f-104">Recurring invoices are used to invoice customers regularly for the same amount.</span></span> <span data-ttu-id="fce9f-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="fce9f-105">This recording uses the USMF demo company.</span></span> <span data-ttu-id="fce9f-106">التسجيل مخصص للشخص المسؤول عن إدارة فواتير الحسابات المدينة ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="fce9f-106">The recording is intended for the person responsible for managing and processing A/R invoices.</span></span>


## <a name="generate-recurring-invoices"></a><span data-ttu-id="fce9f-107">إنشاء فواتير دورية</span><span class="sxs-lookup"><span data-stu-id="fce9f-107">Generate recurring invoices</span></span>

## <a name="post-recurring-invoices"></a><span data-ttu-id="fce9f-108">ترحيل الفواتير المتكررة</span><span class="sxs-lookup"><span data-stu-id="fce9f-108">Post recurring invoices</span></span>
1. <span data-ttu-id="fce9f-109">انتقل إلى الحسابات المدينة > الفواتير > الفواتير المتكررة‬ > ترحيل الفواتير المتكررة‬‬‬.</span><span class="sxs-lookup"><span data-stu-id="fce9f-109">Go to Accounts receivable > Invoices > Recurring invoices > Post recurring invoices.</span></span>
    * <span data-ttu-id="fce9f-110">استخدم هذه الصفحة لعرض وطباعة الفواتير المتكررة التي تم إنشاؤها بالفعل.</span><span class="sxs-lookup"><span data-stu-id="fce9f-110">Use this page to view and print recurring invoices that have already been generated.</span></span>  
2. <span data-ttu-id="fce9f-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fce9f-111">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fce9f-112">حدد مجموعة الفواتير المتكررة.</span><span class="sxs-lookup"><span data-stu-id="fce9f-112">Select the recurring invoice group.</span></span>  
3. <span data-ttu-id="fce9f-113">انقر فوق "الإجماليات".</span><span class="sxs-lookup"><span data-stu-id="fce9f-113">Click Totals.</span></span>
    * <span data-ttu-id="fce9f-114">تحقق من إجمالي مجموعة الفواتير المتكررة.</span><span class="sxs-lookup"><span data-stu-id="fce9f-114">Verify totals for the recurring invoice group.</span></span>  
4. <span data-ttu-id="fce9f-115">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="fce9f-115">Click Close.</span></span>
    * <span data-ttu-id="fce9f-116">يمثل كل بند أدناه فاتورة متكررة ذات نص حر.</span><span class="sxs-lookup"><span data-stu-id="fce9f-116">Each line below is a recurring free text invoice.</span></span> <span data-ttu-id="fce9f-117">يمكنك تحديد بند والنقر فوق الزر "تفاصيل" لعرض تفاصيل فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="fce9f-117">You can select a line and click 'Details' button to view free text invoice details.</span></span>  
5. <span data-ttu-id="fce9f-118">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="fce9f-118">Click Validate.</span></span>
    * <span data-ttu-id="fce9f-119">تحقق من أن الفواتير المحددة لا تحتوي على أخطاء، ولكن من دون ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="fce9f-119">Verify that the selected invoices do not have errors, but do not post the invoices.</span></span>  
6. <span data-ttu-id="fce9f-120">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="fce9f-120">Click Post.</span></span>
    * <span data-ttu-id="fce9f-121">رحّل الفواتير المحددة.</span><span class="sxs-lookup"><span data-stu-id="fce9f-121">Post the selected invoices.</span></span>  
