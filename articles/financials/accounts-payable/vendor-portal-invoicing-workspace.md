---
title: "مساحة عمل فوترة تعاون المورد"
description: "يشرح هذا الموضوع كيفية عرض فواتير المورد وإرسال الفواتير من مساحة عمل فوترة تعاون المورد."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 506dd06790f40fbba272811a59281add1a86b179
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="8c510-103">مساحة عمل فوترة تعاون المورد</span><span class="sxs-lookup"><span data-stu-id="8c510-103">Vendor collaboration invoicing workspace</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8c510-104">يشرح هذا الموضوع كيفية عرض فواتير المورد وإرسال الفواتير من مساحة عمل فوترة تعاون المورد.</span><span class="sxs-lookup"><span data-stu-id="8c510-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="8c510-105">يمكن استخدام مساحة عمل **فوترة تعاون المورد** لعرض معلومات حول فواتير المورد وتقديم الفواتير إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition باستخدام قدرات سير العمل.</span><span class="sxs-lookup"><span data-stu-id="8c510-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="8c510-106">مساحة عمل فوترة تعاون المورد</span><span class="sxs-lookup"><span data-stu-id="8c510-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="8c510-107">لوحات الملخص</span><span class="sxs-lookup"><span data-stu-id="8c510-107">Summary tiles</span></span>

<span data-ttu-id="8c510-108">توفر لك لوحات **الملخص** نظرة عامة على فواتير المورد المحدد.</span><span class="sxs-lookup"><span data-stu-id="8c510-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="8c510-109">ويمكنك عرض الفواتير حسب حالتها.</span><span class="sxs-lookup"><span data-stu-id="8c510-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="8c510-110">لم يتم إرسال الفواتير المسودة إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="8c510-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="8c510-111">الفواتير المرسلة وغير المعتمدة‬ هي تلك التي أرسلها المورد، ولكن لم يتم ترحيلها في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c510-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Finance and Operations.</span></span>
-   <span data-ttu-id="8c510-112">الفواتير المعتمدة وغير المدفوعة هي تلك التي تم ترحيلها في Finance and Operations، ولكن لم يتم دفعها حتى الآن بشكل كامل.</span><span class="sxs-lookup"><span data-stu-id="8c510-112">Approved, not paid invoices are those that have been posted in Finance and Operations, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="8c510-113">الفواتير المدفوعة هي تلك التي تم دفعها بشكل كامل في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c510-113">Paid invoices are those that have been fully paid in Finance and Operations.</span></span>

<span data-ttu-id="8c510-114">يؤدي النقر فوق لوحة إلى فتح طريقة عرض تمت تصفيتها **لقائمة الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="8c510-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>
### <a name="tabular-lists"></a><span data-ttu-id="8c510-115">القوائم الجدولية</span><span class="sxs-lookup"><span data-stu-id="8c510-115">Tabular lists</span></span>

<span data-ttu-id="8c510-116">في مقطع **القوائم الجدولية**، يتم تقسيم حالة الفوترة بطريقة مماثلة لتقسيمها في لوحات الملخص: مسودة ومرسلة وغير معتمدة.</span><span class="sxs-lookup"><span data-stu-id="8c510-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="8c510-117">عندما تكون الفاتورة في الحالة "مسودة"، يمكن إرساها إلى سير العمل أو يمكن حذفها.</span><span class="sxs-lookup"><span data-stu-id="8c510-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="8c510-118">‏‫تُعد القائمة الجدولية خيارًا للبحث عن الفواتير.</span><span class="sxs-lookup"><span data-stu-id="8c510-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="8c510-119">ويمكنك إجراء التصفية أثناء البحث، للسماح بإجراء عمليات بحث أسرع.‬</span><span class="sxs-lookup"><span data-stu-id="8c510-119">You can filter as you search, to allow for faster searches.</span></span>
<span data-ttu-id="8c510-120">صفحة قائمة كافة فواتير المورد</span><span class="sxs-lookup"><span data-stu-id="8c510-120">All vendor invoices list page</span></span>
-----------------------------

<span data-ttu-id="8c510-121">‏‫يمكنك عرض كافة فواتير المورد المرحلة وغير المرحلة في صفحة قائمة **فواتير تعاون المورد‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="8c510-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="8c510-122">ويمكنك استخدام صفحة القائمة هذه لعرض حالة دفع الفواتير.‬</span><span class="sxs-lookup"><span data-stu-id="8c510-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="8c510-123">تتضمن حالات الدفع: غير مرحل‬ وغير مدفوع ومدفوع جزئيًا‬ ومدفوع بالكامل‬.</span><span class="sxs-lookup"><span data-stu-id="8c510-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="8c510-124">إنشاء فاتورة جديدة من أمر شراء</span><span class="sxs-lookup"><span data-stu-id="8c510-124">Creating a new invoice from a purchase order</span></span>
--------------------------------------------

<span data-ttu-id="8c510-125">يمكنك إنشاء فاتورة مورد جديدة عن طريق تحديد الإجراء **جديد** في مساحة العمل **فوترة تعاون المورد**.</span><span class="sxs-lookup"><span data-stu-id="8c510-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="8c510-126">يجب على المورد توفير رقم أمر الشراء ورقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="8c510-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="8c510-127">بشكل افتراضي، سوف تظهر كافة بنود أمر الشراء الخاص بالمورد على الفاتورة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="8c510-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="8c510-128">ويمكن تحرير معلومات الكمية والتكلفة قبل تقديم فاتورة المورد إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="8c510-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="8c510-129">يمكنك إرفاق الملفات والصور والملاحظات وعناوين URL بالفاتورة قبل إرسالها.</span><span class="sxs-lookup"><span data-stu-id="8c510-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>



<span data-ttu-id="8c510-130">لمزيد من المعلومات، راجع [‬‏‫التعاون مع المورّدين باستخدام مدخل المورِّد‬‬‏‫](../../supply-chain/procurement/collaborate-vendors-vendor-portal.md)</span><span class="sxs-lookup"><span data-stu-id="8c510-130">For more information, see [Collaborating with vendors by using the Vendor portal](../../supply-chain/procurement/collaborate-vendors-vendor-portal.md)</span></span>




