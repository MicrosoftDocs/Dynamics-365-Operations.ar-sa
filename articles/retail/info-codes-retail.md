---
title: "أكواد المعلومات"
description: "توفر هذه المقالة نظرة عامة حول أكواد المعلومات ومجموعات أكواد المعلومات وكيفية استخدامها."
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: ce7cdd22d10c98cef6bf7b2567f0c7b776e04483
ms.contentlocale: ar-sa
ms.lasthandoff: 06/29/2017



---

# <a name="info-codes"></a><span data-ttu-id="8858f-103">أكواد المعلومات</span><span class="sxs-lookup"><span data-stu-id="8858f-103">Info codes</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="8858f-104">توفر هذه المقالة نظرة عامة حول أكواد المعلومات ومجموعات أكواد المعلومات وكيفية استخدامها.</span><span class="sxs-lookup"><span data-stu-id="8858f-104">This article provides an overview about info codes, info code groups, and how to use them.</span></span>

<span data-ttu-id="8858f-105">توفر أكواد المعلومات طريقة لالتقاط البيانات بسجل نقطة بيع (POS).</span><span class="sxs-lookup"><span data-stu-id="8858f-105">Info codes provide a way for you to capture data at a point-of-sale (POS) register.</span></span> <span data-ttu-id="8858f-106">يمكن استخدام أكواد المعلومات لمطالبة الصراف بإدخال معلومات أثناء تنفيذ إجراءات مختلفة بنقطة البيع، مثل مبيعات الصنف أو مرتجعات الصنف أو تحديد العملاء.</span><span class="sxs-lookup"><span data-stu-id="8858f-106">You can use info codes to prompt the cashier to enter information during various actions at the POS, such as item sales, item returns, or selecting customers.</span></span> <span data-ttu-id="8858f-107">يمكن أن يقوم الصرافون بتحديد إدخال من قائمة أو إدخال كود أو رقم أو تاريخ أو نص.</span><span class="sxs-lookup"><span data-stu-id="8858f-107">Cashiers can select input from a list or enter it as a code, number, date, or text.</span></span> <span data-ttu-id="8858f-108">يمكن تعيين أكواد المعلومات لإجراءات متجر محددة مسبقًا أو لأصناف البيع بالتجزئة أو لأنواع طرق دفع أو لعملاء أو لأنشطة نقطة بيع محددة.</span><span class="sxs-lookup"><span data-stu-id="8858f-108">You can assign info codes to predefined store actions, retail items, payment methods, customers, or specific point-of-sale activities.</span></span> <span data-ttu-id="8858f-109">يمكنك استخدام أكواد المعلومات للقيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="8858f-109">You can use info codes to do the following:</span></span>
-   <span data-ttu-id="8858f-110">التقاط معلومات إضافية أثناء الحركة، مثل رقم رحلة أو سبب الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="8858f-110">Capture additional information at transaction time, such as a flight number or the reason for a return.</span></span>
-   <span data-ttu-id="8858f-111">مطالبة صراف السجل بتحديد سعر من قائمة أسعار منتجات محددة.</span><span class="sxs-lookup"><span data-stu-id="8858f-111">Prompt the register cashier to select from a list of prices for specific products.</span></span>
-   <span data-ttu-id="8858f-112">ربط كود فرعي بكود معلومات يطالب الصراف بإجراء إدخال عند تنفيذ نشاط محدد.</span><span class="sxs-lookup"><span data-stu-id="8858f-112">Link a subcode to an info code to prompt the cashier for input when performing a specific activity.</span></span> <span data-ttu-id="8858f-113">على سبيل المثال، عندما يقوم عميل بإرجاع منتج، يمكنك مطالبة الصراف بالاستعلام عن سبب إرجاع المنتج.</span><span class="sxs-lookup"><span data-stu-id="8858f-113">For example, when a customer returns a product, you can prompt the cashier to ask why the product is being returned.</span></span> <span data-ttu-id="8858f-114">ثم يمكنك استخدام الأكواد الفرعية لعرض قائمة بالأسباب التي يمكن أن يقوم الصراف بالاختيار من بينها.</span><span class="sxs-lookup"><span data-stu-id="8858f-114">Then you can use subcodes to display a list of reasons that the cashier can choose from.</span></span>
-   <span data-ttu-id="8858f-115">بيع منتج كبيع عادي أو كبيع بالخصم أو كمنتج مجاني.</span><span class="sxs-lookup"><span data-stu-id="8858f-115">Sell a product as a regular sale, discounted sale, or free product.</span></span>
-   <span data-ttu-id="8858f-116">يمكنك مطالبة الصراف بإدخال قيمة أو تحديد كود من قائمة الأكواد الفرعية عند قيامه بفتح درج السجل وعدم تنفيذ عملية مبيعات.</span><span class="sxs-lookup"><span data-stu-id="8858f-116">Prompt the cashier to enter a value or select from a list of subcodes when the register drawer is opened without performing a sales operation.</span></span>

## <a name="info-codes-group"></a><span data-ttu-id="8858f-117">مجموعة أكواد المعلومات</span><span class="sxs-lookup"><span data-stu-id="8858f-117">Info codes group</span></span>
<span data-ttu-id="8858f-118">في Dynamics 365 for Retail، يمكنك إنشاء مجموعات من أكواد المعلومات.‬</span><span class="sxs-lookup"><span data-stu-id="8858f-118">In Dynamics 365 for Retail, you can create groups of info codes.</span></span> <span data-ttu-id="8858f-119">تعمل مجموعات أكواد المعلومات على زيادة سهولة الاستخدام من خلال تمكين تحديد أكواد معلومات أقل ومن ثم استخدامهم بشكل أكثر تنوعًا.</span><span class="sxs-lookup"><span data-stu-id="8858f-119">Info code groups add flexibility by enabling you to define fewer info codes and then use them in more versatile ways.</span></span> <span data-ttu-id="8858f-120">يمكنك استخدام مجموعات أكواد المعلومات بالطرقتين التاليتين:</span><span class="sxs-lookup"><span data-stu-id="8858f-120">You can use info code groups in the following ways:</span></span>
-   <span data-ttu-id="8858f-121">تحديد عدد أقل من أكواد المعلومات وإعادة استخدامها بسهولة.</span><span class="sxs-lookup"><span data-stu-id="8858f-121">Define fewer info codes and easily re-use them.</span></span> <span data-ttu-id="8858f-122">لا يوجد لأكواد المعلومات المضمنة في مجموعات أكواد المعلومات تبعيات محددة مسبقًا بناءً على أكواد المعلومات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="8858f-122">Info codes that are included in info code groups have no predefined dependencies on other info codes.</span></span> <span data-ttu-id="8858f-123">يمكنك تضمين نفس كود المعلومات في عدة مجموعات أكواد معلومات واستخدام ترتيب الأولويات لوضع نفس أكواد المعلومات بترتيب منطقي في أي حالة بعينها.</span><span class="sxs-lookup"><span data-stu-id="8858f-123">You can include the same info code in multiple info code groups and then use prioritization to present the same info codes in the order that makes sense in any particular situation.</span></span>
-   <span data-ttu-id="8858f-124">ربط أكواد معلومات بمجموعات أكواد معلومات أو أكواد معلومات أخرى لجمع معلومات حول منتج أو حركة دون الحاجة إلى تحديد كود معلومات منفصل أو كود معلومات مرتبط لكل سيناريو.</span><span class="sxs-lookup"><span data-stu-id="8858f-124">Link info codes to other info codes or info code groups to gather information about a product or transaction without having to define a separate info code or linked info code for each scenario.</span></span>

## <a name="info-code-examples"></a><span data-ttu-id="8858f-125">أمثلة على رموز المعلومات</span><span class="sxs-lookup"><span data-stu-id="8858f-125">Info code examples</span></span>
<span data-ttu-id="8858f-126">**المثال 1: إعادة استخدام رموز المعلومات** يمكنك ربط أكواد المعلومات حتى عندما يتم تشغيل كود معلومات واحد، يتم تشغيل كود معلومات آخر بعده مباشرة.</span><span class="sxs-lookup"><span data-stu-id="8858f-126">**Example 1: Reuse info codes** You can link info codes so that when one info code is triggered, another info code is triggered immediately after it.</span></span> <span data-ttu-id="8858f-127">على سبيل المثال، عند بيع منتجات معينة، يمكنك مطالبة الصراف بسؤال العميل ما إذا كان يرغب في شراء بطاريات أو ضمان منتج أم لا.</span><span class="sxs-lookup"><span data-stu-id="8858f-127">For example, when you sell certain products, you can prompt the cashier to ask the customer if they want to purchase batteries and a product warranty.</span></span> <span data-ttu-id="8858f-128">أما فيما يتعلق بمنتجات أخرى، يمكنك مطالبة الصراف بسؤال العميل ما إذا كان يرغب في شراء بطاريات بالإضافة إلى الحصول على الرمز البريدي الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="8858f-128">For other products, you can prompt the cashier to ask the customer if they want to purchase batteries and collect their postal code.</span></span> <span data-ttu-id="8858f-129">إذا قمت بإنشاء أكواد معلومات مرتبطة لهذه السيناريوهات، يجب الإعداد لكل تغير بكود المعلومات حتى تتم مطالبة الصراف بالاستعلام عن المعلومات الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="8858f-129">If you create linked info codes for these scenarios, you must set up every variation of the info code so that the cashier is prompted to ask for the right information.</span></span> <span data-ttu-id="8858f-130">إذا كنت تستخدم مجموعات أكواد المعلومات، يمكن إعداد أكواد المعلومات الشائعة، مثل استعلام عن شراء بطاريات، مرة واحدة ثم إعادة استخدامها في عدة مجموعات أكواد معلومات.</span><span class="sxs-lookup"><span data-stu-id="8858f-130">If you use info code groups, common info codes, such as asking for batteries, can be set up once and then reused in multiple info code groups.</span></span> <span data-ttu-id="8858f-131">يمكنك أيضًا استخدام ترتيب الأولويات داخل مجموعات أكواد المعلومات لتحديد الترتيب الذي يتم عرض المطالبات به.</span><span class="sxs-lookup"><span data-stu-id="8858f-131">You can also use prioritization in the info code groups to identify the order in which the prompts are displayed.</span></span>


<span data-ttu-id="8858f-132">**المثال 2: ربط رموز المعلومات بمجمو عات رموز المعلومات** عند بيع بعض المنتجات، الأجهزة المحمولة على سبيل المثال، دائمًا ما تحتاج إلى الحصول على معلومات معينة، مثل رقم الهاتف ومعرف المعدات المتنقلة (MEID) والرقم المسلسل.</span><span class="sxs-lookup"><span data-stu-id="8858f-132">**Example 2: Link info codes to info code groups** When you sell certain products, for example mobile devices, you always want to collect a specific set of information, such as telephone number, mobile equipment identifier (MEID), and serial number.</span></span> <span data-ttu-id="8858f-133">كما تختلف المعلومات التي تحتاج إلى الحصول عليها باختلاف المنتج من كمبيوتر لوحي إلى هاتف محمول.</span><span class="sxs-lookup"><span data-stu-id="8858f-133">However, you also want to collect different information for a tablet versus a mobile phone.</span></span> <span data-ttu-id="8858f-134">يمكنك إعداد مجموعة أكواد معلومات تتضمن مطالبات برقم الهاتف ومعرف MEID والرقم المسلسل ثم ربط مجموعة أكواد المعلومات بكود معلومات واحد.</span><span class="sxs-lookup"><span data-stu-id="8858f-134">You can set up an info code group that includes prompts for the telephone number, MEID, and the serial number, and then link the info code group to an individual info code.</span></span> <span data-ttu-id="8858f-135">عند تشغيل كود المعلومات الخاص بالمنتج، يتم تشغيل مجموعة أكواد المعلومات التالية لتمكينك من الحصول على البيانات الشائعة دون الحاجة إلى تحديد مجموعات متعددة من أكواد المعلومات المرتبطة لكل جهاز.</span><span class="sxs-lookup"><span data-stu-id="8858f-135">When the product-specific info code is triggered, the info code group can be triggered next to enable you to collect the common data without having to define multiple sets of linked info codes for each device.</span></span>

 



