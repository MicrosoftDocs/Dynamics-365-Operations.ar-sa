---
title: تكوين ومعالجة عملية استبدال في أمر إرجاع
description: يشرح هذا الموضوع كيفية تكوين عملية استبدال في أمر إرجاع في Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 60d58e4194481c875c5ff3f08fc3f8e12a87caa0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972722"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="be36b-103">تكوين ومعالجة عملية استبدال في أمر إرجاع</span><span class="sxs-lookup"><span data-stu-id="be36b-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="be36b-104">في الإصدارات السابقة من Dynamics 365 Commerce، كانت معالجة المرتجعات في مقابل أوامر العملاء تتم باستخدام مستند أمر الإرجاع في Headquarters.</span><span class="sxs-lookup"><span data-stu-id="be36b-104">In previous versions of Dynamics 365 Commerce, returns against customer orders were processed by using the return order document in Headquarters.</span></span> <span data-ttu-id="be36b-105">ومع ذلك، يمكن استخدام مستند أمر الإرجاع لمعالجة المنتجات المرتجعة فقط.</span><span class="sxs-lookup"><span data-stu-id="be36b-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="be36b-106">يُشار إلى المنتجات المرتجعة بكمية سالبة في بنود أمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="be36b-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="be36b-107">وبطريقة مغايرة، يُشار إلى المبيعات بكمية موجبة.</span><span class="sxs-lookup"><span data-stu-id="be36b-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="be36b-108">ومع ذلك، لا يدعم مستند أمر الإرجاع الكميات الموجبة.</span><span class="sxs-lookup"><span data-stu-id="be36b-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="be36b-109">وبسبب هذا القيد، لم تدعم الإصدارات السابقة من التطبيق السيناريوهات حيث كانت عمليات الاستبدال تتم فقط باستخدام مستند أمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="be36b-109">Because of this limitation, previous versions of the app didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="be36b-110">ومع ذلك، تمت إضافة وظيفة لدعم السيناريوهات حيث تتم عمليات الاستبدال على الأوامر المرتجعة.</span><span class="sxs-lookup"><span data-stu-id="be36b-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="be36b-111">يستخدم Commerce الآن مستند أمر المبيعات بدلاً من مستند أمر الإرجاع لمعالجة هذه الأنواع من الحركات.</span><span class="sxs-lookup"><span data-stu-id="be36b-111">Commerce now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a><span data-ttu-id="be36b-112">تكوين Commerce لدعم عمليات الاستبدال على أوامر الإرجاع</span><span class="sxs-lookup"><span data-stu-id="be36b-112">Configure Commerce to support exchanges on return orders</span></span>

<span data-ttu-id="be36b-113">اتبع هذه الخطوات لتكوين النظام لدعم عمليات الاستبدال على أوامر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="be36b-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="be36b-114">انتقل إلى **Retail وCommerce \> إعداد Headquarters \> المعلمات \> معلمات Commerce**.</span><span class="sxs-lookup"><span data-stu-id="be36b-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="be36b-115">على علامة التبويب السريعة **أوامر العملاء‬**، عيّن الخيار **معالجة أوامر الإرجاع كأوامر مبيعات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="be36b-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="be36b-116">شغّل وظيفة **جدول توزيع التكوين العمومي** (**1110**).</span><span class="sxs-lookup"><span data-stu-id="be36b-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="be36b-117">إجراء عملية استبدال</span><span class="sxs-lookup"><span data-stu-id="be36b-117">Make an exchange</span></span>

<span data-ttu-id="be36b-118">بعد أن يتم تكوين النظام كما ورد في المقطع السابق، سيحدد مستخدم نقطة البيع (POS) أمر مبيعات أو فاتورة مبيعات لمعالجة عملية إرجاع، كما هو الحال في إصدارات سابقة من التطبيق.</span><span class="sxs-lookup"><span data-stu-id="be36b-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of the app.</span></span> <span data-ttu-id="be36b-119">ومع ذلك، بعد إضافة الأصناف المرتجعة إلى سلة التسوق، سيتمكن المستخدم من إضافة بنود مبيعات جديدة إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="be36b-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="be36b-120">بالنسبة إلى بنود المبيعات الجديدة هذه، يجب على المستخدم تحديد كافة السمات المطلوبة لمعالجة بند في أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="be36b-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="be36b-121">تتضمن هذه السمات أسلوب التسليم وموقع التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="be36b-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="be36b-122">سيكون الدفع المستحق للحركة عبارة عن قيمة صافية لبنود أمر الإرجاع وبنود أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="be36b-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="be36b-123">عند تقديم الدفع للحركة، سيتم ترحيل أمر الإرجاع كمستند أمر مبيعات في Headquarters، وسيقوم النظام بفوترة بنود الإرجاع على الفور.</span><span class="sxs-lookup"><span data-stu-id="be36b-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="be36b-124">لتوفير رؤية أفضل لمختلف المبالغ في سلة التسوق، تمت إضافة ثلاثة حقول مبالغ جديدة إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="be36b-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="be36b-125">ويمكنك استخدام مصمم الشاشة لجعل كافة هذه الحقول الجديدة متوفرة في واجهة مستخدم (UI) نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="be36b-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="be36b-126">**‏‫تم استخدام الإيداع‬** – مبلغ الإيداع المطبق على حركة عندما يقوم المستخدم بانتقاء أمر العميل‬.</span><span class="sxs-lookup"><span data-stu-id="be36b-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="be36b-127">إذا لم يكن هناك أي مبلغ تجاوز الإيداع، وإذا تم تكوين إيداع بنسبة 10 بالمئة، سيكون المبلغ في هذا الحقل 90 بالمئة من المبلغ الإجمالي لأمر العميل.</span><span class="sxs-lookup"><span data-stu-id="be36b-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="be36b-128">**تنفيذ المبلغ** – المبلغ الإجمالي للبنود حيث تم تعيين وضع التسليم إلى **تنفيذ** عندما تم إنشاء أمر العميل أو تحريره، أو خلال استبدال أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="be36b-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="be36b-129">يتضمن المبلغ الموجود في هذا الحقل الضرائب والمصاريف.</span><span class="sxs-lookup"><span data-stu-id="be36b-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="be36b-130">**المبلغ المرتجع‬** – المبلغ الإجمالي للبنود ذات الكميات السالبة أثناء استبدال أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="be36b-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="be36b-131">يتضمن المبلغ الموجود في هذا الحقل الضرائب والمصاريف.</span><span class="sxs-lookup"><span data-stu-id="be36b-131">The amount in this field includes taxes and charges.</span></span>
