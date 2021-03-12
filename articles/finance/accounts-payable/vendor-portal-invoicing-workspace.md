---
title: مساحة عمل فوترة تعاون المورد
description: يشرح هذا الموضوع كيفية عرض فواتير المورد وإرسال الفواتير من مساحة عمل فوترة تعاون المورد.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 30e9012845838a4d1df5f1308740b356a64433e9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993153"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="ba7c4-103">مساحة عمل فوترة تعاون المورد</span><span class="sxs-lookup"><span data-stu-id="ba7c4-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba7c4-104">يشرح هذا الموضوع كيفية عرض فواتير المورد وإرسال الفواتير من مساحة عمل فوترة تعاون المورد.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="ba7c4-105">يمكن استخدام مساحة عمل **فوترة تعاون المورد**‬ لعرض معلومات حول فواتير المورد وتقديم الفواتير إلى النظام باستخدام قدرات سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="ba7c4-106">مساحة عمل فوترة تعاون المورد</span><span class="sxs-lookup"><span data-stu-id="ba7c4-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="ba7c4-107">لوحات الملخص</span><span class="sxs-lookup"><span data-stu-id="ba7c4-107">Summary tiles</span></span>

<span data-ttu-id="ba7c4-108">توفر لك لوحات **الملخص** نظرة عامة على فواتير المورد المحدد.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="ba7c4-109">ويمكنك عرض الفواتير حسب حالتها.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="ba7c4-110">لم يتم إرسال الفواتير المسودة إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="ba7c4-111">الفواتير المرسلة وغير المعتمدة‬ هي تلك التي أرسلها المورد، ولكن لم يتم ترحيلها في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="ba7c4-112">الفواتير المعتمدة وغير المدفوعة هي تلك التي تم ترحيلها، ولكن لم يتم دفعها حتى الآن بشكل كامل.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="ba7c4-113">الفواتير المدفوعة هي تلك التي تم دفعها بشكل كامل في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="ba7c4-114">يؤدي النقر فوق لوحة إلى فتح طريقة عرض تمت تصفيتها **لقائمة الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="ba7c4-115">القوائم الجدولية</span><span class="sxs-lookup"><span data-stu-id="ba7c4-115">Tabular lists</span></span>

<span data-ttu-id="ba7c4-116">في مقطع **القوائم الجدولية**، يتم تقسيم حالة الفوترة بطريقة مماثلة لتقسيمها في لوحات الملخص: مسودة ومرسلة وغير معتمدة.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="ba7c4-117">عندما تكون الفاتورة في الحالة "مسودة"، يمكن إرساها إلى سير العمل أو يمكن حذفها.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="ba7c4-118">‏‫تُعد القائمة الجدولية خيارًا للبحث عن الفواتير.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="ba7c4-119">ويمكنك إجراء التصفية أثناء البحث، للسماح بإجراء عمليات بحث أسرع.‬</span><span class="sxs-lookup"><span data-stu-id="ba7c4-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="ba7c4-120">صفحة قائمة كافة فواتير المورد</span><span class="sxs-lookup"><span data-stu-id="ba7c4-120">All vendor invoices list page</span></span>

<span data-ttu-id="ba7c4-121">‏‫يمكنك عرض كافة فواتير المورد المرحلة وغير المرحلة في صفحة قائمة **فواتير تعاون المورد‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="ba7c4-122">ويمكنك استخدام صفحة القائمة هذه لعرض حالة دفع الفواتير.‬</span><span class="sxs-lookup"><span data-stu-id="ba7c4-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="ba7c4-123">تتضمن حالات الدفع: غير مرحل‬ وغير مدفوع ومدفوع جزئيًا‬ ومدفوع بالكامل‬.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="ba7c4-124">إنشاء فاتورة جديدة من أمر شراء</span><span class="sxs-lookup"><span data-stu-id="ba7c4-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="ba7c4-125">يمكنك إنشاء فاتورة مورد جديدة عن طريق تحديد الإجراء **جديد** في مساحة العمل **فوترة تعاون المورد**.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="ba7c4-126">يجب على المورد توفير رقم أمر الشراء ورقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="ba7c4-127">بشكل افتراضي، سوف تظهر كافة بنود أمر الشراء الخاص بالمورد على الفاتورة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="ba7c4-128">ويمكن تحرير معلومات الكمية والتكلفة قبل تقديم فاتورة المورد إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="ba7c4-129">يمكنك إرفاق الملفات والصور والملاحظات وعناوين URL بالفاتورة قبل إرسالها.</span><span class="sxs-lookup"><span data-stu-id="ba7c4-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="ba7c4-130">لمزيد من المعلومات، راجع [‬‏‫تعاون المورّدين مع موردين خارجيين](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="ba7c4-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>



