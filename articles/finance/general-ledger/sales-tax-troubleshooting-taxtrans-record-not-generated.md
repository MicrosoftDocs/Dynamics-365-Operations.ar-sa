---
title: لم يتم إنشاء سجل TaxTrans
description: يوفر هذا الموضوع معلومات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد عندما لا يتم إنشاء سجل TaxTrans.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947589"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="e4f0c-103">لم يتم إنشاء سجل TaxTrans</span><span class="sxs-lookup"><span data-stu-id="e4f0c-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4f0c-104">إذا قمت بتحديد **ضريبة المبيعات المرحلة** لأحدي الحركات، ولكن كانت  **صفحه ضريبة المبيعات المرحلة** Yما لا تظهر إيه بنود ضريبة أو إذا كانت العلامة تفتقد لبند ضريبة، فربما لم يتم إنشاء سجل **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="e4f0c-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="e4f0c-105">[![صفحه ضريبة المبيعات المرحلة التي لا تحتوي علي أصناف بند](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="e4f0c-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="e4f0c-106">لاستكشاف هذه المشكلة وإصلاحها، اتبع الخطوات الواردة في الأقسام التالية عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="e4f0c-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="e4f0c-107">التحقق من ضريبة المبيعات قبل ترحيل الحركة</span><span class="sxs-lookup"><span data-stu-id="e4f0c-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="e4f0c-108">قبل ترحيل الحركة، في صفحة **ترحيل الفاتورة**، حدد **ضريبة المبيعات** للتحقق من الحساب.</span><span class="sxs-lookup"><span data-stu-id="e4f0c-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="e4f0c-109">[![زر ضريبة المبيعات علي صفحه ترحيل الفاتورة](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="e4f0c-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="e4f0c-110">في صفحة **حركات ضريبة المبيعات المؤقتة**، راجع نتيجة الحساب.</span><span class="sxs-lookup"><span data-stu-id="e4f0c-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="e4f0c-111">في حاله عدم حساب أي ضريبة، راجع [الضريبة التي لم يتم حسابها أو يكون مبلغ الضريبة صفرًا](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="e4f0c-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="e4f0c-112">البحث عن سجل TaxTrans في كافة ضرائب المبيعات المرحلة</span><span class="sxs-lookup"><span data-stu-id="e4f0c-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="e4f0c-113">انتقل إلى **الضريبة** \> **الاستعلامات والتقارير** \> **استعلامات ضريبة المبيعات** > **ضريبة المبيعات المرحلة**.</span><span class="sxs-lookup"><span data-stu-id="e4f0c-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="e4f0c-114">في عنوان عمود **الإيصال**، حدد رمز عامل التصفية للعثور على سجل **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="e4f0c-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="e4f0c-115">إذا وجدت سجلات ضريبة المبيعات التي تبحث عنها، فتحقق من التاريخ.</span><span class="sxs-lookup"><span data-stu-id="e4f0c-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="e4f0c-116">إذا كان التاريخ مختلفا عن تاريخ راس دفتر اليومية، قم بإنشاء طلب خدمه Microsoft للحصول علي دعم إضافي.</span><span class="sxs-lookup"><span data-stu-id="e4f0c-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="e4f0c-117">[![صفحة ضريبة المبيعات المرحّلة](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="e4f0c-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="e4f0c-118">تدقيق التصحيح لمراجعه التفاصيل</span><span class="sxs-lookup"><span data-stu-id="e4f0c-118">Debug to check details</span></span>

1. <span data-ttu-id="e4f0c-119">للحصول على معلومات حول كيفية التصحيح وتحديد ما إذا كان قد تم إنشاء **TmpTaxWorkTrans** و **TaxUncommitted** بشكل صحيح، راجع [قيمة الحقل في TaxTrans غير صحيحة](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="e4f0c-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="e4f0c-120">في حالة إنشاء **TaxTmpWorkTrans** أو **TaxUncommitted** بشكل صحيح، أضف نقطة توقف **TaxPost::SaveAndPost()** و **Tax::SaveAndPost** لتصحيح سبب عدم إدراج **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="e4f0c-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="e4f0c-121">[![نقاط التوقف المضافة في التعليمات البرمجية](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="e4f0c-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="e4f0c-122">[![نتائج نقاط التوقف المضافة](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="e4f0c-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="e4f0c-123">حدد ما إذا كان التخصيص موجودًا</span><span class="sxs-lookup"><span data-stu-id="e4f0c-123">Determine whether customization exists</span></span>

<span data-ttu-id="e4f0c-124">إذا كنت قد أكملت الخطوات الواردة في الأقسام السابقة ولكنك لم تجد أي مشكلة، فحدد ما إذا كان التخصيص موجودًا أم لا.</span><span class="sxs-lookup"><span data-stu-id="e4f0c-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="e4f0c-125">في حاله عدم وجود تخصيص، قم بإنشاء طلب خدمه Microsoft لمزيد من الدعم.</span><span class="sxs-lookup"><span data-stu-id="e4f0c-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
