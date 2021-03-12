---
title: إعداد برامج الاستمرارية لمراكز الاتصال
description: تصف هذه المقالة كيفية إعداد ‏‫برنامج الاستمرارية لمركز الاتصال.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 941685c9bad3b8f288e2acdf31bb25c7bcaa7cba
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969741"
---
# <a name="set-up-continuity-programs-for-call-centers"></a><span data-ttu-id="cd936-103">إعداد برامج الاستمرارية لمراكز الاتصال</span><span class="sxs-lookup"><span data-stu-id="cd936-103">Set up continuity programs for call centers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cd936-104">تصف هذه المقالة كيفية إعداد ‏‫برنامج الاستمرارية لمركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="cd936-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="cd936-105">في برنامج استمرارية، ويعرف أيضًا ببرنامج الأمر المتكرر، يتلقى العملاء شحنات المنتجات العادية وفقًا لجدول معرف مسبقاً.</span><span class="sxs-lookup"><span data-stu-id="cd936-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="cd936-106">يمكن أن يحتوي كل شحنة على منتج مختلف، كما في حالة نادي كتاب الشهر، أو يمكن إرسال المنتج نفسه مرارًا وتكرارًا.</span><span class="sxs-lookup"><span data-stu-id="cd936-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="cd936-107">ولإعداد برنامج استمرارية، يجب عليك إكمال المهام التالية.</span><span class="sxs-lookup"><span data-stu-id="cd936-107">To set up a continuity program, you must complete the following tasks.</span></span>

1. <span data-ttu-id="cd936-108">تعيين معلمات الاستمرارية في صفحة **معلمات مركز الاتصالات**.</span><span class="sxs-lookup"><span data-stu-id="cd936-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2. <span data-ttu-id="cd936-109"> أنشئ برنامج استمرارية والذي يحدد تفاصيل مثل جدول الدفع، توقيت الشحنات، وما إذا كانت الفوترة مقدمًا.</span><span class="sxs-lookup"><span data-stu-id="cd936-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="cd936-110">يجب أيضًا إضافة قائمة بالمنتجات التي يتضمنها برنامج الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="cd936-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="cd936-111">‏‫يتلقى كل منتج رقم معرف حدث يتم تعيينه بشكل تسلسلي، بدءاً من الرقم 1.</span><span class="sxs-lookup"><span data-stu-id="cd936-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="cd936-112">تحدد معرفات الحدث الترتيب الذي يتم به إرسال المنتجات به.</span><span class="sxs-lookup"><span data-stu-id="cd936-112">The event IDs determine the order that products are sent in.</span></span>

    - <span data-ttu-id="cd936-113">إذا تلقي العملاء منتجًا مختلفًا في كل شحنة، يتم إرسال المنتجات بترتيب متسلسل وفقًا لمعرفات الأحداث الخاصة بها، بدءاً من الحدث الحالي.</span><span class="sxs-lookup"><span data-stu-id="cd936-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    - <span data-ttu-id="cd936-114">إذا تلقي العملاء نفس المنتج في كل شحنة، تحتوي القائمة على منتج واحد ذو معرف حدث واحد.</span><span class="sxs-lookup"><span data-stu-id="cd936-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="cd936-115">يحدث نفس الحدث مرارًا وتكرارًا.</span><span class="sxs-lookup"><span data-stu-id="cd936-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="cd936-116">يمكنك تحديد عدد المرات التي يتكرر بها كل حدث.</span><span class="sxs-lookup"><span data-stu-id="cd936-116">You can specify how many times each event is repeated.</span></span>

3. <span data-ttu-id="cd936-117">‏‫أنشئ المنتج الأصل الذي يمثل برنامج الاستمرارية الذي قمت بإنشائه في المهمة 2.</span><span class="sxs-lookup"><span data-stu-id="cd936-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="cd936-118">وإذا قمت بإضافة هذا المنتج لأمر مبيعات، يتم فتح صفحة **الاستمرارية**.</span><span class="sxs-lookup"><span data-stu-id="cd936-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="cd936-119">يمكنك فيما بعد استخدام هذه الصفحة لإنشاء أمر الاستمراية الفعلي.</span><span class="sxs-lookup"><span data-stu-id="cd936-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="cd936-120">لا يحدد المنتج الأصل المنتجات الفردية التي يتلقاها العميل في كل شحنة.</span><span class="sxs-lookup"><span data-stu-id="cd936-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="cd936-121">بعد قيامك بإعداد برنامج استمرارية كما هو موضح أعلاه، يمكنك إنشاء أمر استمرارية لأحد العملاء.</span><span class="sxs-lookup"><span data-stu-id="cd936-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="cd936-122">وقد تحتاج إلى تنفيذ مهام الصيانة الإضافية التالية.</span><span class="sxs-lookup"><span data-stu-id="cd936-122">You might also have to perform the following additional maintenance tasks.</span></span>

- <span data-ttu-id="cd936-123">**تحديث فترة حدث الاستمرارية الحالية** – إعداد وظيفة الدفعة التي تُعلم النظام بفترة الحدث الحالية.</span><span class="sxs-lookup"><span data-stu-id="cd936-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
- <span data-ttu-id="cd936-124">**إنشاء أوامر استمرارية فرعية** – إنشاء أوامر الاستمرارية الفرعية من أمر الاستمرارية الأصلي.</span><span class="sxs-lookup"><span data-stu-id="cd936-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
- <span data-ttu-id="cd936-125">**معالجة مدفوعات الاستمرارية** – معالجة الفواتير ورسائل الإعلام الخاصة بالمدفوعات المرتبطة بأوامر المبيعات الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="cd936-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
- <span data-ttu-id="cd936-126">**توسيع بنود الاستمرارية** (عند اللزوم) – توسيع عدد المرات التي يمكن تكرارها حدثاً استمرارية.</span><span class="sxs-lookup"><span data-stu-id="cd936-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="cd936-127">ويمكن لتكرار الشحنات فيما بعد تجاوز الحد الذي تم تعيينه في حقل **حد تكرار الاستمرارية** في معلمات مركز الاتصالات.</span><span class="sxs-lookup"><span data-stu-id="cd936-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
- <span data-ttu-id="cd936-128">**تنفيذ عملية تحديث استمرارية** (عند اللزوم) – مزامنة التغييرات بين برنامج الاستمرارية وأوامر المبيعات الأصلية الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="cd936-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
- <span data-ttu-id="cd936-129">**إغلاق بنود وأوامر الاستمرارية الأصلية** – إغلاق أوامر الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="cd936-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>
