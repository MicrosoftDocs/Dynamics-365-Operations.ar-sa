---
title: تقرير مواصفات ضريبة المبيعات حسب حركة دفتر الأستاذ
description: يوضح هذا الموضوع كيفية استخدام ‏‫تقرير مواصفات ضريبة المبيعات حسب حركة دفتر الأستاذ‬ لعرض وطباعة معلومات حول حركات دفتر الأستاذ التي يتم حساب ضريبة المبيعات لها.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1c36d9f8fb81a0a7e7a6de3db48cebdcf9d13b2d
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/14/2019
ms.locfileid: "2591184"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="f2a7f-103">تقرير مواصفات ضريبة المبيعات حسب حركة دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="f2a7f-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2a7f-104">يوضح هذا الموضوع كيفية استخدام ‏‫تقرير **مواصفات ضريبة المبيعات حسب حركة دفتر الأستاذ**‬ لعرض وطباعة معلومات حول حركات دفتر الأستاذ التي يتم حساب ضريبة المبيعات لها.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="f2a7f-105">الحسابات الضريبية مقابل الحسابات غير الضريبية</span><span class="sxs-lookup"><span data-stu-id="f2a7f-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="f2a7f-106">يعرض تقرير **‏‫مواصفات ضريبة المبيعات حسب حركة دفتر الأستاذ‬** حركات الضريبة لكل من الحسابات الضريبة والحسابات غير الضريبية.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="f2a7f-107">يتم تصنيف هذه الحسابات بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="f2a7f-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="f2a7f-108">**حساب ضريبي** – يعتبر الحساب حسابًا ضريبيًا عند ترحيل حركة ضريبية، وعندما يكون الحساب الرئيسي في بند دفتر اليومية **ضريبة المبيعات** حساب ضريبة، مثل حساب ضريبة مبيعات مستحقة الدفع أو حساب ضريبة مبيعات مستحقه القبض.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="f2a7f-109">**حساب غير ضريبي** – يعتبر الحساب حسابًا غير ضريبي عند ترحيل حركة ضريبية، وعندما يكون الحساب الرئيسي في الحركة الأساسية هو حساب غير ضريبي، مثل حساب إيرادات أو حساب مصروفات.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="f2a7f-110">بالنسبة للحسابات الضريبية تعرض الأعمدة **الأصل** و **‏‫ضريبة المبيعات مستحقة القبض‬** و **‏‫ضريبة المبيعات مستحقة الدفع** في التقرير **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="f2a7f-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="f2a7f-111">بالنسبة للحسابات غير الضريبية، تعرض هذه الأعمدة المبالغ.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="f2a7f-112">تصفية البيانات المعروضة في التقرير</span><span class="sxs-lookup"><span data-stu-id="f2a7f-112">Filtering the data on the report</span></span>

<span data-ttu-id="f2a7f-113">عند إنشاء التقرير، تظهر الحقول الافتراضية التالية.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="f2a7f-114">يمكنك استخدام هذه الحقول لتصفية البيانات التي ستظهر في التقرير.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="f2a7f-115">الحقل</span><span class="sxs-lookup"><span data-stu-id="f2a7f-115">Field</span></span>                      | <span data-ttu-id="f2a7f-116">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="f2a7f-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="f2a7f-117">التاريخ</span><span class="sxs-lookup"><span data-stu-id="f2a7f-117">Date</span></span>                       | <span data-ttu-id="f2a7f-118">استخدم الحقول الموجودة في القسمين **من** و **إلى** لتحديد نطاق تاريخ لحركات الضرائب.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="f2a7f-119">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="f2a7f-119">Main account</span></span>               | <span data-ttu-id="f2a7f-120">استخدم الحقول الموجودة في القسمين **من** و **إلى** لتحديد نطاق الحساب الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="f2a7f-121">كود ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="f2a7f-121">Sales tax code</span></span>             | <span data-ttu-id="f2a7f-122">استخدم الحقول الموجودة في القسمين **من** و **إلى** لتحديد نطاق أكواد ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="f2a7f-123">التجميع</span><span class="sxs-lookup"><span data-stu-id="f2a7f-123">Grouping</span></span>                   | <span data-ttu-id="f2a7f-124">حدد ما إذا كان يجب تجميع التقرير حسب حساب دفتر الأستاذ أو كود ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="f2a7f-125">الإجمالي الفرعي حسب كود ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="f2a7f-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="f2a7f-126">قم بتعيين هذا الخيار إلى **نعم** لإظهار الإجماليات الفرعية بواسطة كود ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="f2a7f-127">الإجماليات فقط</span><span class="sxs-lookup"><span data-stu-id="f2a7f-127">Totals only</span></span>                | <span data-ttu-id="f2a7f-128">قم بتعيين هذا الخيار إلى **نعم** لإظهار الإجماليات فقط.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="f2a7f-129">الحسابات الرئيسية فقط</span><span class="sxs-lookup"><span data-stu-id="f2a7f-129">Main accounts only</span></span>         | <span data-ttu-id="f2a7f-130">قم بتعيين هذا الخيار إلى **نعم** لتضمين الحسابات الرئيسية فقط في التقرير.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="f2a7f-131">إظهار الحسابات غير الضريبية فقط في التقرير</span><span class="sxs-lookup"><span data-stu-id="f2a7f-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="f2a7f-132">لإظهار الحسابات غير الضريبية فقط في التقرير، قم باعداد شرط عامل تصفية، مثل العلامة النجمية (\*)، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="f2a7f-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![تقرير يوضح الحسابات غير الضريبية](media/taxspecperledgertrans.png)
