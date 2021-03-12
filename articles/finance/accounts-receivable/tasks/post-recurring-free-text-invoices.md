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
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c89247c870ef3edcaaa30831efaef9b03a9bc166
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003196"
---
# <a name="generate-and-post-recurring-free-text-invoices"></a><span data-ttu-id="28d7c-103">إنشاء وترحيل فواتير النص الحر المكررة</span><span class="sxs-lookup"><span data-stu-id="28d7c-103">Generate and post recurring free text invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28d7c-104">يتم استخدام الفواتير المتكررة لفوترة العملاء بشكل منتظم لنفس المبلغ.</span><span class="sxs-lookup"><span data-stu-id="28d7c-104">Recurring invoices are used to invoice customers regularly for the same amount.</span></span> <span data-ttu-id="28d7c-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="28d7c-105">This recording uses the USMF demo company.</span></span> <span data-ttu-id="28d7c-106">التسجيل مخصص للشخص المسؤول عن إدارة فواتير الحسابات المدينة ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="28d7c-106">The recording is intended for the person responsible for managing and processing A/R invoices.</span></span>


## <a name="generate-recurring-invoices"></a><span data-ttu-id="28d7c-107">إنشاء فواتير دورية</span><span class="sxs-lookup"><span data-stu-id="28d7c-107">Generate recurring invoices</span></span>

## <a name="post-recurring-invoices"></a><span data-ttu-id="28d7c-108">ترحيل الفواتير المتكررة</span><span class="sxs-lookup"><span data-stu-id="28d7c-108">Post recurring invoices</span></span>
1. <span data-ttu-id="28d7c-109">انتقل إلى الحسابات المدينة > الفواتير > الفواتير المتكررة‬ > ترحيل الفواتير المتكررة‬‬‬.</span><span class="sxs-lookup"><span data-stu-id="28d7c-109">Go to Accounts receivable > Invoices > Recurring invoices > Post recurring invoices.</span></span>
    * <span data-ttu-id="28d7c-110">استخدم هذه الصفحة لعرض وطباعة الفواتير المتكررة التي تم إنشاؤها بالفعل.</span><span class="sxs-lookup"><span data-stu-id="28d7c-110">Use this page to view and print recurring invoices that have already been generated.</span></span>  
2. <span data-ttu-id="28d7c-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="28d7c-111">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="28d7c-112">حدد مجموعة الفواتير المتكررة.</span><span class="sxs-lookup"><span data-stu-id="28d7c-112">Select the recurring invoice group.</span></span>  
3. <span data-ttu-id="28d7c-113">انقر فوق "الإجماليات".</span><span class="sxs-lookup"><span data-stu-id="28d7c-113">Click Totals.</span></span>
    * <span data-ttu-id="28d7c-114">تحقق من إجمالي مجموعة الفواتير المتكررة.</span><span class="sxs-lookup"><span data-stu-id="28d7c-114">Verify totals for the recurring invoice group.</span></span>  
4. <span data-ttu-id="28d7c-115">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="28d7c-115">Click Close.</span></span>
    * <span data-ttu-id="28d7c-116">يمثل كل بند أدناه فاتورة متكررة ذات نص حر.</span><span class="sxs-lookup"><span data-stu-id="28d7c-116">Each line below is a recurring free text invoice.</span></span> <span data-ttu-id="28d7c-117">يمكنك تحديد بند والنقر فوق الزر "تفاصيل" لعرض تفاصيل فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="28d7c-117">You can select a line and click 'Details' button to view free text invoice details.</span></span>  
5. <span data-ttu-id="28d7c-118">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="28d7c-118">Click Validate.</span></span>
    * <span data-ttu-id="28d7c-119">تحقق من أن الفواتير المحددة لا تحتوي على أخطاء، ولكن من دون ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="28d7c-119">Verify that the selected invoices do not have errors, but do not post the invoices.</span></span>  
6. <span data-ttu-id="28d7c-120">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="28d7c-120">Click Post.</span></span>
    * <span data-ttu-id="28d7c-121">رحّل الفواتير المحددة.</span><span class="sxs-lookup"><span data-stu-id="28d7c-121">Post the selected invoices.</span></span>  

