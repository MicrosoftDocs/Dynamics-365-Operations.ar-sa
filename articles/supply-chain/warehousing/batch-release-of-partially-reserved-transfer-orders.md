---
title: "إصدار دُفعة أوامر التحويل المحجوزة جزئيًا"
description: "يصف هذا الموضوع كيفية إعداد وتطبيق إصدار الدُفعة لأوامر التحويل المحجوزة جزئيًا‬ من جهاز محمول."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 614bce43e486667a894e77cbf03f3a18f9d5d68a
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="85057-103">إصدار دُفعة أوامر التحويل المحجوزة جزئيًا</span><span class="sxs-lookup"><span data-stu-id="85057-103">Batch release of partially reserved transfer orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85057-104">تسمح لك وظيفة إصدار الدُفعة لأوامر التحويل المحجوزة جزئيًا‬ بإصدار أوامر التحويل بشكل جزئي إلى مستودع باستخدام وظيفة دُفعية.</span><span class="sxs-lookup"><span data-stu-id="85057-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="85057-105">بما أنه يمكنك إصدار كمية جزئية، لست بحاجة إلى انتظار توفر كمية الأمر بكاملها في المستودع قبل إصدار الأمر.</span><span class="sxs-lookup"><span data-stu-id="85057-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="85057-106">يعتبر إصدار الأوامر إلى المستودع بمثابة عملية متقدمة لإدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="85057-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="85057-107">تتضمن هذه العملية أنشطة، مثل الانتقاء والتعبئة والشحن، يستطيع عامل المستودع تنفيذها باستخدام جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="85057-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="85057-108">أين يتم التطبيق</span><span class="sxs-lookup"><span data-stu-id="85057-108">Where it applies</span></span>

<span data-ttu-id="85057-109">لهذه الوظيفة، يتم إصدار أوامر التحويل إلى مستودع باستخدام وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="85057-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="85057-110">تعتبر هذه الوظيفة مفيدة إذا لم يكن لديك مخزون كاف في المستودع، ولكنك مع ذلك تريد تحويل الأصناف من مخزن إلى آخر.</span><span class="sxs-lookup"><span data-stu-id="85057-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="85057-111">كيف يتم إعدادها</span><span class="sxs-lookup"><span data-stu-id="85057-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="85057-112">تعيين معايير التنفيذ لأوامر المبيعات وأوامر التحويل</span><span class="sxs-lookup"><span data-stu-id="85057-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="85057-113">قبل إصدار أمر ما جزئيًا إلى مستودع في دُفعة، يجب تلبية معايير التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="85057-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="85057-114">تتحدد معايير التنفيذ هذه بواسطة سياسة التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="85057-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="85057-115">وتتحدد سياسات التنفيذ لأوامر المبيعات وأوامر التحويل على مستوى الشركة.</span><span class="sxs-lookup"><span data-stu-id="85057-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="85057-116">وفقًا لإعداد سياسة التنفيذ، سيتم قبول إصدار الأوامر في دُفعة أو رفضها.</span><span class="sxs-lookup"><span data-stu-id="85057-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="85057-117">بعد ذلك، تتم معالجة الأوامر وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="85057-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="85057-118">لإنشاء سياسات التنفيذ لأوامر التحويل وأوامر المبيعات، انقر فوق **إدارة المستودعات** \> **الإعداد** \> **إصدار إلى المستودع** \> **سياسة التنفيذ**، ثم قم بإنشاء سياسة تنفيذ بإدخال اسم ووصف.</span><span class="sxs-lookup"><span data-stu-id="85057-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="85057-119">لتعيين معدل تنفيذ، ونوع قيمة، والرسالة التي تظهر في حالة انتهاك سياسة التنفيذ، انقر فوق **إدارة المستودعات** \> **الإعداد** \> **إصدار إلى المستودع‬** \> **سياسة التنفيذ**، ثم عيّن الحقول **معدل التنفيذ‬** و**نوع القيمة‬** و**رسالة انتهاك التنفيذ‬‬**.</span><span class="sxs-lookup"><span data-stu-id="85057-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="85057-120">تعيين سياسات التنفيذ لأوامر المبيعات وأوامر التحويل</span><span class="sxs-lookup"><span data-stu-id="85057-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="85057-121">لتعيين سياسات التنفيذ لأوامر التحويل، انقر فوق **إدارة المخزون** \> **الإعداد** \> **محددات إدارة المستودعات والمخزون‬** \> **أوامر التحويل** \> **إدارة المستودعات**، ثم حدد سياسة التنفيذ لأوامر التحويل.</span><span class="sxs-lookup"><span data-stu-id="85057-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="85057-122">لتعيين سياسات التنفيذ لأوامر المبيعات، انقر فوق **الحسابات المدينة** \> **Setup** \> **محددات الحسابات المدينة‬** \> **إدارة المستودعات**، ثم حدد سياسة التنفيذ لأوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="85057-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="85057-123">السماح بالإصدار في دُفعة وتحديد الكمية التي يجب أن إصدارها في دُفعة</span><span class="sxs-lookup"><span data-stu-id="85057-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="85057-124">يتم استخدام وظيفة دُفعية لإصدار الأوامر إلى مستودع في دُفعة.</span><span class="sxs-lookup"><span data-stu-id="85057-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="85057-125">يتم تعيين المحددات التي تميز الأوامر التي يجب تشغيلها في وظيفة دُفعية على الوظيفة الدُفعية بحد ذاتها.</span><span class="sxs-lookup"><span data-stu-id="85057-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="85057-126">تعين محددة **الكمية** ما إذا كان يجب إصدار الكمية الكاملة أو الكمية المحجوزة فعليًا في الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="85057-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="85057-127">تحدد المحددة **السماح بإصدار الأوامر الصادرة جزئيًا‬** ما إذا كان يجب قبول الأوامر في الدُفعة أو رفضها في تم إصدارها جزئيًا في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="85057-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="85057-128">لتعيين محددات **الكمية** و**السماح بإصدار الأوامر الصادرة جزئيًا‬** لأوامر التحويل، انقر فوق **إدارة المستودعات** \> **إصدار إلى المستودع‬** \> **إصدار أوامر التحويل تلقائيًا‬**.</span><span class="sxs-lookup"><span data-stu-id="85057-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="85057-129">لتعيين محددات **الكمية** و**السماح بإصدار الأوامر الصادرة جزئيًا‬** لأوامر المبيعات، انقر فوق **إدارة المستودعات** \> **إصدار إلى المستودع‬** \> **إصدار أوامر المبيعات تلقائيًا‬**.</span><span class="sxs-lookup"><span data-stu-id="85057-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>

