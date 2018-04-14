---
title: "حل الاختلافات أثناء مطابقة إجماليات الفواتير"
description: "يمكنك استخدام مطابقة إجماليات الفواتير للمساعدة على التأكد من أن مبالغ الفواتير الإجمالية لا تحيد عن المبالغ المتوقعة بما يزيد على فرق مقبول."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 091185b7c3c10fa177a3d0c9338ae7950c2f6f47
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="c836d-103">حل الاختلافات أثناء مطابقة إجماليات الفواتير</span><span class="sxs-lookup"><span data-stu-id="c836d-103">Resolve discrepancies during invoice totals matching</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="c836d-104">يتمثل نوع واحد من التحقق من صحة مطابقة الفواتير في مطابقة إجماليات الفواتير.</span><span class="sxs-lookup"><span data-stu-id="c836d-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="c836d-105">ولتحديد أن النظام يجب عليه تنفيذ مطابقة إجماليات الفواتير، في صفحة **معلمات الحسابات الدائنة**، في علامة التبويب **التحقق من صحة الفواتير**، قم بتعيين خيار **مطابقة إجماليات الفواتير** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c836d-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="c836d-106">يمكنك استخدام مطابقة إجماليات الفواتير للمساعدة على التأكد من أن مبالغ الفواتير الإجمالية لا تحيد عن المبالغ المتوقعة بما يزيد على فرق مقبول.</span><span class="sxs-lookup"><span data-stu-id="c836d-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="c836d-107">وتتم مقارنة ستة إجماليات في صفحة **تفاصيل مطابقة إجماليات الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="c836d-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="c836d-108">وإذا انحرف أي إجمالي من الإجماليات عن إجمالي أمر الشراء المقابل المتوقع، فإنه يتم وضع علامة لاختلاف المطابقة.</span><span class="sxs-lookup"><span data-stu-id="c836d-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="c836d-109">ولمراجعة الفاتورة المشتملة على اختلاف مطابقة الإجماليات، في مساحة عمل **إدخال فاتورة مورد**، انقر فوق تجانب **الفواتير المعلقة**.</span><span class="sxs-lookup"><span data-stu-id="c836d-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="c836d-110">وبعد ذلك، في جزء الإجراءات، في علامة التبويب **مراجعة**، انقر فوق **تفاصيل المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="c836d-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="c836d-111">وإذا تم الكشف عن اختلافات في المطابقة، تظهر رموز تحذير بجوار مبلغ الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c836d-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="c836d-112">ويمكنك عرض المزيد من التفاصيل حول الإجماليات بعرض تفاصيل مطابقة إجماليات الفواتير.</span><span class="sxs-lookup"><span data-stu-id="c836d-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="c836d-113">وبعد تحديد اختلاف، قد تحتاج إلى الاتصال بالمورّد إذا كنت تعتقد أن المعلومات الموجودة في الفاتورة غير صحيحة.</span><span class="sxs-lookup"><span data-stu-id="c836d-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="c836d-114">ووفقًا لما ستتفق عليه مع المورّد، يمكنك القيام بأيٍ من الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="c836d-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="c836d-115">قبول الاختلاف في السعر وترحيل الفاتورة التي تشتمل على اختلافات المطابقة.</span><span class="sxs-lookup"><span data-stu-id="c836d-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="c836d-116">ويمكن إعداد النظام لتتطلب الموافقة قبل أن يمكنه الترحيل إذا كانت هناك اختلافات في المطابقة.</span><span class="sxs-lookup"><span data-stu-id="c836d-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="c836d-117">وفي هذه الحالة، يجب عليك الموافقة على اختلاف المطابقة ويمكنك إدخال تعليق موافقة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="c836d-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="c836d-118">وبعد ذلك، يمكنك اختيار ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c836d-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="c836d-119">قم بتعديل مبلغ الفاتورة إلى المبلغ المتوقع وترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c836d-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="c836d-120">اطلب ائتمانًا كاملاً، فاتورة مصححة جديدة من المورد.</span><span class="sxs-lookup"><span data-stu-id="c836d-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="c836d-121">للحصول على مزيد من المعلومات، راجع [حل الاستثناءات‏‎ أو البحث عنها](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="c836d-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



