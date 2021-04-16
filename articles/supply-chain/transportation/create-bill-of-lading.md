---
title: إنشاء بوليصة شحن
description: يصف هذا الموضوع كيفية إنشاء بوليصة شحن عند استخدام عمليات إدارة المستودعات.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a14d971475c71e6a02957acfa0c6e6494c4638fc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807622"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="53b91-103">إنشاء بوليصة شحن</span><span class="sxs-lookup"><span data-stu-id="53b91-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53b91-104">يصف هذا الموضوع كيفية إنشاء بوليصة شحن عند استخدام عمليات إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="53b91-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="53b91-105">إن بوليصة الشحن عبارة عن وثيقة قانونية بين الشركة التي تقوم بشحن الأصناف والناقل.</span><span class="sxs-lookup"><span data-stu-id="53b91-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="53b91-106">تصحب هذه الوثيقة الأصناف المشحونة، وتعمل بمثابة إيصال الشحن عندما يتم تسليم الأصناف في الوجهة.</span><span class="sxs-lookup"><span data-stu-id="53b91-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="53b91-107">إذا كنت تستخدم إدارة المستودعات، فهناك طريقتان لإنشاء بوليصة الشحن:</span><span class="sxs-lookup"><span data-stu-id="53b91-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="53b91-108">إنشاء التقرير يدويًا، باستخدام صفحة **بوليصة الشحن**.</span><span class="sxs-lookup"><span data-stu-id="53b91-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="53b91-109">إنشاء التقرير من **منضدة عمل تخطيط الحِمل‬**.</span><span class="sxs-lookup"><span data-stu-id="53b91-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="53b91-110">إذا قمت بإنشاء بوليصة الشحن من **منضدة عمل تخطيط الحِمل‬**، فيجب أن تكون حالة الحِمل‬‏‎ **مشحون‬.**</span><span class="sxs-lookup"><span data-stu-id="53b91-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="53b91-111">‏‫إذا كان هناك أكثر من شحنة في الحِمل‬‏‎، فسيتم إنشاء بوليصة شحن لكل شحنة.</span><span class="sxs-lookup"><span data-stu-id="53b91-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="53b91-112">بعد إنشاء بوليصة الشحن، يمكنك إجراء تغييرات عليها في صفحة **بوليصة الشحن**.</span><span class="sxs-lookup"><span data-stu-id="53b91-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="53b91-113">بوليصة الشحن الرئيسية</span><span class="sxs-lookup"><span data-stu-id="53b91-113">Master bill of lading</span></span>
<span data-ttu-id="53b91-114">عند وجود أكثر من شحنة واحد في الحمل، يمكنك إنشاء بوليصة شحن رئيسية.</span><span class="sxs-lookup"><span data-stu-id="53b91-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="53b91-115">تتضمن بوليصة الشحن هذه نفس التخطيط والمعلومات كما في بوليصة الشحن العادية، ولكنها تحتوي على المحتوى الملخص لجميع الشحنات.</span><span class="sxs-lookup"><span data-stu-id="53b91-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="53b91-116">إذا تم تعيين الخيار **إنشاء بوليصة شحن رئيسية عند وجود أكثر من شحن واحد على حمل عمل‬** إلى **نعم** في صفحة **محددات إدارة النقل**، فسيتم إنشاء بوليصة شحن رئيسية تلقائيًا إذا أنشأت بوليصة شحن من **منضدة عمل تخطيط الحِمل‬**، وهناك أكثر من شحنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="53b91-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="53b91-117">يمكنك أيضًا الحصول على قائمة بوالص الشحن‬ بالنقر فوق **المعلومات ذات الصلة** &gt; **بوليصة الشحن**.</span><span class="sxs-lookup"><span data-stu-id="53b91-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="53b91-118">إذا كنت تقوم بإنشاء بوالص الشحن يدويًا، فيمكنك إنشاء بوليصة شحن رئيسية في صفحة **بوليصة الشحن**.</span><span class="sxs-lookup"><span data-stu-id="53b91-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]