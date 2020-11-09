---
title: إعداد أكواد الترتيب
description: ويركز هذا الإجراء على إعداد رمز الإرجاع الذي يمكن استخدامه على جهاز محمول لعملية استلام أمر الإرجاع.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d84699e8e4323792ac67b69236d264e33eeaf28
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017016"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="daf1b-103">إعداد أكواد الترتيب</span><span class="sxs-lookup"><span data-stu-id="daf1b-103">Set up dispositions codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="daf1b-104">ويركز هذا الإجراء على إعداد رمز الإرجاع الذي يمكن استخدامه على جهاز محمول لعملية استلام أمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="daf1b-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="daf1b-105">تمثل رموز الإرجاع مجموعة من القواعد التي يمكن استخدامها عند استلام الأصناف.</span><span class="sxs-lookup"><span data-stu-id="daf1b-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="daf1b-106">على سبيل المثال، عندما يستخدم مستخدم عمل جهازًا محمولاً لاستلام الأصناف التي تعرضت للتلف، يجب عليه فحص رمز الإرجاع للعناصر التالفة.</span><span class="sxs-lookup"><span data-stu-id="daf1b-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="daf1b-107">ويمكن تحديد كل من حالة المخزون للبضائع المستلمة وقالب العمل وتوجيه الموقع من رمز الإرجاع الممسوح ضوئياً.</span><span class="sxs-lookup"><span data-stu-id="daf1b-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="daf1b-108">بالنسبة لعملية استلام أمر الشراء وتقرير أمر الإنتاج بانتهاء العملية، يكون استخدام رمز إرجاع اختياريًا.</span><span class="sxs-lookup"><span data-stu-id="daf1b-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="daf1b-109">وبالنسبة لعملية استلام إرجاع أمر المبيعات، إذا كانت الأصناف مسجلة باستخدام جهاز محمول، فإن استخدام كود الترتيب يكون إلزاميًا.</span><span class="sxs-lookup"><span data-stu-id="daf1b-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="daf1b-110">تم إنشاء هذا الدليل باستخدام شركة بيانات العرض التقديمي USMF.</span><span class="sxs-lookup"><span data-stu-id="daf1b-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="daf1b-111">هذا الإجراء مخصص لمدير المستودعات.</span><span class="sxs-lookup"><span data-stu-id="daf1b-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="daf1b-112">انتقل إلى إدارة المستودعات > الإعداد > الجهاز المحمول > رموز الترتيب.</span><span class="sxs-lookup"><span data-stu-id="daf1b-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="daf1b-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="daf1b-113">Click New.</span></span>
    * <span data-ttu-id="daf1b-114">قم بإنشاء رمز إرجاع جديد لاستخدامه لعائدات العميل.</span><span class="sxs-lookup"><span data-stu-id="daf1b-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="daf1b-115">في الحقل "رمز الإرجاع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="daf1b-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="daf1b-116">في الحقل "حالة المخزون"، حدد حالة مخزون يوجد بها حظر مخزون.</span><span class="sxs-lookup"><span data-stu-id="daf1b-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="daf1b-117">إذا كنت تستخدم USMF، فحدد "حظر".</span><span class="sxs-lookup"><span data-stu-id="daf1b-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="daf1b-118">يمكنك إضافة حالة مخزون إلى رمز الإرجاع لتجاوز الحالة الافتراضية المفروضة على بنود الأمر.</span><span class="sxs-lookup"><span data-stu-id="daf1b-118">You can add an inventory status to the disposition code to override the default status that's on the order lines.</span></span>  
5. <span data-ttu-id="daf1b-119">في الحقل "قالب العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="daf1b-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="daf1b-120">اختياري: حدد رمز قالب عمل مرتبط بأمر إرجاع.</span><span class="sxs-lookup"><span data-stu-id="daf1b-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="daf1b-121">إذا لم تتوفر أية قيمة، سيُحل قالب العمل باستخدام القواعد القياسية التي تم تكوينها في نظامك.</span><span class="sxs-lookup"><span data-stu-id="daf1b-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="daf1b-122">وسيؤدي تحديد قالب عمل إلى الحد من العمليات التي يمكن استخدام رمز الإرجاع هذا معها.</span><span class="sxs-lookup"><span data-stu-id="daf1b-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="daf1b-123">على سبيل المثال، إذا كان رمز إرجاع له قالب عمل به أمر عمل من نوع أمر الشراء، فلن يمكن استخدام هذا الرمز لتسجيل الأصناف التي يُرجعها العملاء.</span><span class="sxs-lookup"><span data-stu-id="daf1b-123">For example, if a disposition code has a work template with a work order of type purchase order, it can't be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="daf1b-124">في الحقل "كود ترتيب الإرجاع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="daf1b-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="daf1b-125">يحدد رمز ترتيب الإرجاع ما تبقى من عملية أمر الإرجاع للأصناف المسجلة.</span><span class="sxs-lookup"><span data-stu-id="daf1b-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="daf1b-126">في هذا المثال، يجب أن يستلم العميل إشعارًا دائنًا.</span><span class="sxs-lookup"><span data-stu-id="daf1b-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="daf1b-127">قم بإضافة رمز ترتيب الإرجاع الذي يحتوي على إجراء اعتماد.</span><span class="sxs-lookup"><span data-stu-id="daf1b-127">Add a returns disposition code that contains an action Credit.</span></span>  

