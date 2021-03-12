---
title: الدفاتر المشتقة
description: توفر هذه المقالة نظرة عامة على وظيفة الدفاتر المشتقة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 911bb476a696facfad9dec177261821724d2bfe0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994905"
---
# <a name="derived-books"></a><span data-ttu-id="ac533-103">الدفاتر المشتقة</span><span class="sxs-lookup"><span data-stu-id="ac533-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac533-104">توفر هذه المقالة نظرة عامة على وظيفة الدفاتر المشتقة.</span><span class="sxs-lookup"><span data-stu-id="ac533-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="ac533-105">‏‫الغرض من الدفاتر المشتقة هو تبسيط ترحيل حركات دفتر الأصول الثابتة التي تم تخطيطها للفواصل الزمنية العادية.</span><span class="sxs-lookup"><span data-stu-id="ac533-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="ac533-106">يمكنك اختيار دفتر واحد كدفتر أساسي.‬</span><span class="sxs-lookup"><span data-stu-id="ac533-106">You choose one book as the primary book.</span></span> <span data-ttu-id="ac533-107">يكون هذا عادةً الكتاب المستخدم للإهلاك المحاسبي.</span><span class="sxs-lookup"><span data-stu-id="ac533-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="ac533-108">وتقوم فيما بعد بإرفاقه بدفاتر أخرى التي تم إعدادها لترحيل الحركات في الفواصل الزمنية نفسها كالدفتر الأساسي.</span><span class="sxs-lookup"><span data-stu-id="ac533-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="ac533-109">يتم غالبًا إعداد دفاتر إهلاك كدفاتر مشتقة.</span><span class="sxs-lookup"><span data-stu-id="ac533-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="ac533-110">وتعتبر الحركات الأكثر شيوعًا التي يجب إعدادها لترحيل الدفاتر المشتقة عمليات الاستحواذ وتسويات الاستحواذ وعمليات التخلص.</span><span class="sxs-lookup"><span data-stu-id="ac533-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="ac533-111">مثال</span><span class="sxs-lookup"><span data-stu-id="ac533-111">Example</span></span>

<span data-ttu-id="ac533-112">تم إعداد الدفتر "ب" والدفتر "ج" كدفاتر مشتقة للدفتر "أ" لنوع حركة الاستحواذ.</span><span class="sxs-lookup"><span data-stu-id="ac533-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="ac533-113">في الدفتر "أ"، أدخل حركة الاستحواذ للأصل 123 بقيمة 1.500.00.</span><span class="sxs-lookup"><span data-stu-id="ac533-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="ac533-114">عندما يتم ترحيل الحركة، يتم إنشاء حركة استحواذ ويتم ترحيلها في الأصل 123 للدفتر "ب" وفي الأصل 123 لنموذج للدفتر "ج" بقيمة 1.500.00.</span><span class="sxs-lookup"><span data-stu-id="ac533-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="ac533-115">عندما تقوم بإعداد حركات الدفتر الأساسي لترحيلها في دفتر يومية الأصل الثابت، يمكنك أيضًا عرض حركات دفاتر الإهلاك المشتقة وتعديلها.</span><span class="sxs-lookup"><span data-stu-id="ac533-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="ac533-116">وإذا قمت بإعداد حركات الدفتر الأساسي في دفتر يومية آخر، فلن تظهر حركات القيمة المشتقة.</span><span class="sxs-lookup"><span data-stu-id="ac533-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="ac533-117">ومع ذلك، يتم ترحيلها إلى الحسابات المناسبة وطبقات الترحيل عند ترحيل حركات الدفتر الأساسي.</span><span class="sxs-lookup"><span data-stu-id="ac533-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="ac533-118">فيما يتعلق بالدفاتر التي يتم إعدادها لترحيل الحركات عند فواصل زمنية غير الفواصل الزمنية للدفتر الأساسي، يجب إرفاقها بالأصل الثابت كدفاتر منفصلة وليس كدفاتر مشتقة.</span><span class="sxs-lookup"><span data-stu-id="ac533-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="ac533-119">لمزيد من المعلومات، راجع [‏‫الترحيل باستخدام الدفاتر المشتقة](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="ac533-119">For more information, see [Post with derived books](post-derived-value-models.md).</span></span>



