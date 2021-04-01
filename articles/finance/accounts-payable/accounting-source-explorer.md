---
title: مستكشف مصدر المحاسبة
description: توفر هذه المقالة معلومات حول مستكشف مصدر المحاسبة، الذي يمكنك استخدامه لإجراء تحليل مفصل للمعلومات المصدر خلف الإدخالات المحاسبية‬ في دفتر الأستاذ العام.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: roschlom
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f92781a8e1400206f91f91c46c319b928e0010c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250712"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="59ffa-103">مستكشف مصدر المحاسبة</span><span class="sxs-lookup"><span data-stu-id="59ffa-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59ffa-104">توفر هذه المقالة معلومات حول مستكشف مصدر المحاسبة، الذي يمكنك استخدامه لإجراء تحليل مفصل للمعلومات المصدر خلف الإدخالات المحاسبية‬ في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="59ffa-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="59ffa-105">مستكشف مصدر المحاسبة هو صفحة جديدة تعرض معلومات المصدر.</span><span class="sxs-lookup"><span data-stu-id="59ffa-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="59ffa-106">‏‫ويمكنك استخدام مستكشف مصدر المحاسبة كأداة مستقلة أو لتحليل التفاصيل بما يتجاوز إدخالات المحاسبة في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="59ffa-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="59ffa-107">‏‫على سبيل المثال، يمكنك استخدام مستكشف مصدر المحاسبة للحصول على معلومات المصدر الأكثر تفصيلاً للاطلاع على رصيد في ميزان المراجعة أو حركة إيصال.‬</span><span class="sxs-lookup"><span data-stu-id="59ffa-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="59ffa-108">يمكنك عندئذٍ استخدام ميزة التصدير إلى MS Excel لتقسيم وتجزئة المعلومات بشكل أكبر في Microsoft Excel (على سبيل المثال، في PivotTable أو تقرير PivotTable).</span><span class="sxs-lookup"><span data-stu-id="59ffa-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="59ffa-109">يعرض مستكشف مصدر المحاسبة دائماً نفس المبلغ الإجمالي لكل حساب دفتر أستاذ مثلما يعرضه دفتر الأستاذ العام (على سبيل المثال، في ميزان المراجعة).</span><span class="sxs-lookup"><span data-stu-id="59ffa-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="59ffa-110">وكما هو الحال في ميزان المراجعة، يمكنك عرض الشرائح في أعمدة منفصلة.</span><span class="sxs-lookup"><span data-stu-id="59ffa-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="59ffa-111">وما عليك سوى تحديد مجموعة الأبعاد المالية المناسبة.</span><span class="sxs-lookup"><span data-stu-id="59ffa-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="59ffa-112">ويمكنك استخدام المعلمات لتحديد فترة تاريخ للتحليل.</span><span class="sxs-lookup"><span data-stu-id="59ffa-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="59ffa-113">كما تشبه هذه الوظيفة الوظيفة الموجودة في ميزان المراجعة.</span><span class="sxs-lookup"><span data-stu-id="59ffa-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="59ffa-114">‏‫وبالنسبة لكافة المستندات التي تستخدم إطار عمل المستند المصدر، يعرض مستكشف مصدر المحاسبة معلومات إضافية، استناداً إلى التوزيعات المحاسبية، وإن أمكن، توزيعات محاسبة المشروع.</span><span class="sxs-lookup"><span data-stu-id="59ffa-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="59ffa-115">وتتضمن هذه المعلومات نوع المبلغ النقدي، والمشروع، والنشاط، والفئة، وخاصية البند.</span><span class="sxs-lookup"><span data-stu-id="59ffa-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="59ffa-116">فيما يلي بعض الأمثلة على التحليل الذي يمكنك القيام به:</span><span class="sxs-lookup"><span data-stu-id="59ffa-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="59ffa-117">الفروق بين أوامر الشراء وفواتير المورد، لأن كل فرق يتمثل بنوع مبلغ مالي، مثل فرق التكلفة</span><span class="sxs-lookup"><span data-stu-id="59ffa-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="59ffa-118">الساعات المدفوعة مقابل الساعات غير المدفوعة والمصروفات لكل مشروع، ووحدة أعمال، والحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="59ffa-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="59ffa-119">بالنسبة للمستندات المصدر استخدام مفهوم معرفات مرجع المستند المصدر، يعرض مستكشف مصدر المحاسبة مزيدًا من التفاصيل، مثل العميل والمورد، والعامل، والمنتج، والكمية، ونص الوحدة، والأوصاف.</span><span class="sxs-lookup"><span data-stu-id="59ffa-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="59ffa-120">فيما يلي بعض الأمثلة على التحليل الذي يمكنك القيام به:</span><span class="sxs-lookup"><span data-stu-id="59ffa-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="59ffa-121">مصروفات الفندق لكل وحدة أعمال والعلامة التجارية للفندق لفترة مالية، استناداً إلى تقارير المصروفات</span><span class="sxs-lookup"><span data-stu-id="59ffa-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="59ffa-122">الخصومات لكل مورد ومنتج وإدارة</span><span class="sxs-lookup"><span data-stu-id="59ffa-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="59ffa-123">بالنسبة لهذه المستندات، يمكنك أيضًا التنقل إلى المستند المصدر الفعلي من مستكشف مصدر المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="59ffa-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]