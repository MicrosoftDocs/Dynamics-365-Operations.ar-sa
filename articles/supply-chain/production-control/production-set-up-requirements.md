---
title: "متطلبات إعداد الإنتاج"
description: "توفر هذه المقالة معلومات حول متطلبات الإعداد قبل بدء العمل بواسطة التحكم بالإنتاج‬."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47fe11168ad2ddea2a7033eda8d8bd8220efea32
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="production-setup-requirements"></a><span data-ttu-id="ef960-103">متطلبات إعداد الإنتاج</span><span class="sxs-lookup"><span data-stu-id="ef960-103">Production setup requirements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ef960-104">توفر هذه المقالة معلومات حول متطلبات الإعداد قبل بدء العمل بواسطة التحكم بالإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="ef960-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="ef960-105">يتم دمج التحكم في الإنتاج في الميزات الموجودة في الوحدات النمطية الأخرى.</span><span class="sxs-lookup"><span data-stu-id="ef960-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="ef960-106">ويتيح هذا الترابط لك تغيير أوامر الإنتاج وضمان تحديثها تلقائيًا في كافة العمليات والعمليات الحسابية الأخرى المرتبطة في النظام.</span><span class="sxs-lookup"><span data-stu-id="ef960-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="ef960-107">ويتم سرد عمليات الإعداد التالية في الأمر الذي يجب أن تُكملها فيه.</span><span class="sxs-lookup"><span data-stu-id="ef960-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="ef960-108">إعداد الخط الأساسي المطلوب في الوحدات النمطية الأخرى</span><span class="sxs-lookup"><span data-stu-id="ef960-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="ef960-109">يجب إعداد المعلومات في الوحدات الأخرى قبل العمل مع التحكم في الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ef960-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="ef960-110">يتضمن هذا الإعداد المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="ef960-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="ef960-111">إعداد معلومات الشركة العامة.</span><span class="sxs-lookup"><span data-stu-id="ef960-111">Set up general company information.</span></span>
-   <span data-ttu-id="ef960-112">إعداد دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="ef960-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="ef960-113">تحديد مجموعات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ef960-113">Define item groups.</span></span>
-   <span data-ttu-id="ef960-114">إعداد حسابات دفتر الأستاذ لمجموعات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ef960-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="ef960-115">إعداد جدول صنف المخزون في إدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="ef960-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="ef960-116">إنشاء قائمة مكونات الصنف وإصداراتها في إدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="ef960-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="ef960-117">التقويم المطلوب وإعداد الموارد</span><span class="sxs-lookup"><span data-stu-id="ef960-117">Required calendar and resource setup</span></span>
<span data-ttu-id="ef960-118">قبل قيامك باستخدام التحكم في الإنتاج، افتح إدارة المؤسسة، وقم بإنشاء وتحديد التقويم وموارد العمليات بالترتيب التالي:</span><span class="sxs-lookup"><span data-stu-id="ef960-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="ef960-119">**قالب مواعيد العمل** – إعداد قوالب فترة العمل لتحديد الفترات المتوفرة لجدولة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ef960-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="ef960-120">**التقويمات** – إعداد تقويمات فترة العمل لتحديد الأيام المتوفرة من السنة لجدولة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ef960-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="ef960-121">**مجموعات الموارد** – إعداد مجموعات الموارد لتجميع موارد العمليات بحيث يمكنك الحصول على نظرة عامة على أي قدرة مجانية عند تشغيل الجدولة.</span><span class="sxs-lookup"><span data-stu-id="ef960-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="ef960-122">ولا يلزم إعداد مجموعات الموارد قبل إعداد موارد العمليات.</span><span class="sxs-lookup"><span data-stu-id="ef960-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="ef960-123">ومع ذلك، نوصي بفهم كيفية تجميع الموارد عند إعداد التحكم في الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ef960-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="ef960-124">**الموارد** – إعداد موارد العمليات لتحديد الموارد التي يتم استخدامها لاستكمال عملية الإنتاج والتخطيط القدرة.</span><span class="sxs-lookup"><span data-stu-id="ef960-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="ef960-125">إعداد محددات الإنتاج المطلوبة</span><span class="sxs-lookup"><span data-stu-id="ef960-125">Required production parameters setup</span></span>
<span data-ttu-id="ef960-126">**معلمات التحكم في الإنتاج** – إعداد معلمات الإنتاج الأساسية لتحديد الكيفية التي يُجري بها ويعالج النظام أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ef960-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="ef960-127">حدد كيفية إنشاء أوامر الإنتاج وتقديرها وجدولتها واستهلاكها.</span><span class="sxs-lookup"><span data-stu-id="ef960-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="ef960-128">كما يمكنك تحديد نوع الملاحظات التي تريدها وطريقة إجراء محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="ef960-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="ef960-129">تعريف اسم دفتر اليومية المطلوب</span><span class="sxs-lookup"><span data-stu-id="ef960-129">Required journal name identification</span></span>
<span data-ttu-id="ef960-130">**أسماء دفاتر يومية الإنتاج** – تحديد أسماء دفاتر يومية الإنتاج التي يتم استخدامها لتسجيل الحركات وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="ef960-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="ef960-131">الإعداد في حالة استخدام العمليات</span><span class="sxs-lookup"><span data-stu-id="ef960-131">Setup if you use operations</span></span>
<span data-ttu-id="ef960-132">تُمثل العمليات الأنشطة الخاصة التي تتم لإصدار المنتج المنتهي.</span><span class="sxs-lookup"><span data-stu-id="ef960-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="ef960-133">**ملاحظة:** يجب معرفة أنواع الأنشطة المطلوبة لإنتاج الصنف الخاص بك، وترتيب وأولويات تلك الأنشطة.</span><span class="sxs-lookup"><span data-stu-id="ef960-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="ef960-134">كما يجب عليك معرفة الموارد التي يقومون بها، وعددها.</span><span class="sxs-lookup"><span data-stu-id="ef960-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="ef960-135">**العمليات** – إعداد العمليات لتقديم المهام التي يجب استكمالها لإنتاج الصنف المنتهي.</span><span class="sxs-lookup"><span data-stu-id="ef960-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="ef960-136">**العلاقات** – إعداد علاقات العملية لإنشاء الخواص التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="ef960-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="ef960-137">لتحديد علاقات العملية، انقر فوق **العلاقات** في صفحة **العمليات**.</span><span class="sxs-lookup"><span data-stu-id="ef960-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="ef960-138">الإعداد في حالة استخدام المسارات</span><span class="sxs-lookup"><span data-stu-id="ef960-138">Setup if you use routes</span></span>
<span data-ttu-id="ef960-139">إذا كنت تعمل باستخدام المسارات، فإنه يجب عليك تحديد العمليات لكل مسار إنتاج تقوم بإعداده.</span><span class="sxs-lookup"><span data-stu-id="ef960-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="ef960-140">تُمثل المسارات المسار الذي يسلكه الصنف من عملية لأخرى بدءًا من بداية عملية الإنتاج إلى النهاية.</span><span class="sxs-lookup"><span data-stu-id="ef960-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="ef960-141">**فئات التكلفة** – إعداد فئات التكلفة لتحديد التكلفة حسب كل ساعة للعمليات الخاصة وفترات الإعداد.</span><span class="sxs-lookup"><span data-stu-id="ef960-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="ef960-142">**مجموعات التكاليف** – إعداد مجموعات التكلفة لإنشاء أنواع التكلفة المختلفة وإعدادها.</span><span class="sxs-lookup"><span data-stu-id="ef960-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="ef960-143">**مجموعات المسارات** – إعداد مجموعات المسار لتحديد المحددات التي تتعلق بمجموعات المسارات.</span><span class="sxs-lookup"><span data-stu-id="ef960-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="ef960-144">يجب عليك إعداد مجموعات المسارات قبل تمكنك من إنشاء مسارات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ef960-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="ef960-145">**المسارات** – إعداد مسارات الإنتاج وتحديد الإعدادات الافتراضية للتحكم في الجدولة وتكاليف وأسعار عمليات المسارات وتقرير التحكم في التقدم.</span><span class="sxs-lookup"><span data-stu-id="ef960-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="ef960-146">**المسارات** – إعداد إصدارات المسار لتمكين متغيرات الصنف في الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ef960-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="ef960-147">الإعدادات الاختيارية المتقدمة</span><span class="sxs-lookup"><span data-stu-id="ef960-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="ef960-148">**مجموعات الإنتاج** – إعداد مجموعات الإنتاج لإنشاء علاقات بين أمر الإنتاج وحسابات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="ef960-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="ef960-149">يتم استخدام حسابات دفتر الأستاذ لترحيل أو تجميع الأوامر للتقارير.</span><span class="sxs-lookup"><span data-stu-id="ef960-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="ef960-150">**أوعية الإنتاج** – إنشاء أوعية أوامر الإنتاج لتجميع أوامر الإنتاج حتى تتمكن من معالجة أوامر الإنتاج العاجلة أو حذف مجموعات الأوامر وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="ef960-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="ef960-151">**الخصائص** – تحديد الخصائص لإنشاء السمات الخاصة التي يمكنك تعيينها للموارد الخاصة بك للتحكم في ترتيب عمليات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ef960-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="ef960-152">يتم توصيل هذه السمات بقالب فترة العمل.</span><span class="sxs-lookup"><span data-stu-id="ef960-152">These attributes are connected to the working time template.</span></span>





