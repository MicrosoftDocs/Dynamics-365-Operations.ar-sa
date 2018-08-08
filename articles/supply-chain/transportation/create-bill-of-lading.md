---
title: "إنشاء بوليصة شحن"
description: "يصف هذا الموضوع كيفية إنشاء بوليصة شحن عند استخدام عمليات إدارة المستودعات."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 8d5caed5553ad1c7aec5db83591024129aab1264
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-bill-of-lading"></a><span data-ttu-id="cd914-103">إنشاء بوليصة شحن</span><span class="sxs-lookup"><span data-stu-id="cd914-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd914-104">يصف هذا الموضوع كيفية إنشاء بوليصة شحن عند استخدام عمليات إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="cd914-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="cd914-105">إن بوليصة الشحن عبارة عن وثيقة قانونية بين الشركة التي تقوم بشحن الأصناف والناقل.</span><span class="sxs-lookup"><span data-stu-id="cd914-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="cd914-106">تصحب هذه الوثيقة الأصناف المشحونة، وتعمل بمثابة إيصال الشحن عندما يتم تسليم الأصناف في الوجهة.</span><span class="sxs-lookup"><span data-stu-id="cd914-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="cd914-107">إذا كنت تستخدم إدارة المستودعات، فهناك طريقتان لإنشاء بوليصة الشحن:</span><span class="sxs-lookup"><span data-stu-id="cd914-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="cd914-108">إنشاء التقرير يدويًا، باستخدام صفحة **بوليصة الشحن**.</span><span class="sxs-lookup"><span data-stu-id="cd914-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="cd914-109">إنشاء التقرير من **منضدة عمل تخطيط الحِمل‬**.</span><span class="sxs-lookup"><span data-stu-id="cd914-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="cd914-110">إذا قمت بإنشاء بوليصة الشحن من **منضدة عمل تخطيط الحِمل‬**، فيجب أن تكون حالة الحِمل‬‏‎ **مشحون‬.**</span><span class="sxs-lookup"><span data-stu-id="cd914-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="cd914-111">‏‫إذا كان هناك أكثر من شحنة في الحِمل‬‏‎، فسيتم إنشاء بوليصة شحن لكل شحنة.</span><span class="sxs-lookup"><span data-stu-id="cd914-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="cd914-112">بعد إنشاء بوليصة الشحن، يمكنك إجراء تغييرات عليها في صفحة **بوليصة الشحن**.</span><span class="sxs-lookup"><span data-stu-id="cd914-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="cd914-113">بوليصة الشحن الرئيسية</span><span class="sxs-lookup"><span data-stu-id="cd914-113">Master bill of lading</span></span>
<span data-ttu-id="cd914-114">عند وجود أكثر من شحنة واحد في الحمل، يمكنك إنشاء بوليصة شحن رئيسية.</span><span class="sxs-lookup"><span data-stu-id="cd914-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="cd914-115">تتضمن بوليصة الشحن هذه نفس التخطيط والمعلومات كما في بوليصة الشحن العادية، ولكنها تحتوي على المحتوى الملخص لجميع الشحنات.</span><span class="sxs-lookup"><span data-stu-id="cd914-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="cd914-116">إذا تم تعيين الخيار **إنشاء بوليصة شحن رئيسية عند وجود أكثر من شحن واحد على حمل عمل‬** إلى **نعم** في صفحة **محددات إدارة النقل**، فسيتم إنشاء بوليصة شحن رئيسية تلقائيًا إذا أنشأت بوليصة شحن من **منضدة عمل تخطيط الحِمل‬**، وهناك أكثر من شحنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="cd914-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="cd914-117">يمكنك أيضًا الحصول على قائمة بوالص الشحن‬ بالنقر فوق **المعلومات ذات الصلة** &gt; **بوليصة الشحن**.</span><span class="sxs-lookup"><span data-stu-id="cd914-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="cd914-118">إذا كنت تقوم بإنشاء بوالص الشحن يدويًا، فيمكنك إنشاء بوليصة شحن رئيسية في صفحة **بوليصة الشحن**.</span><span class="sxs-lookup"><span data-stu-id="cd914-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>




