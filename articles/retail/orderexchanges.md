---
title: تكوين ومعالجة عملية استبدال في أمر إرجاع
description: يشرح هذا الموضوع كيفية تكوين عملية استبدال في أمر إرجاع في Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "301851"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="bd414-103">تكوين ومعالجة عملية استبدال في أمر إرجاع</span><span class="sxs-lookup"><span data-stu-id="bd414-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bd414-104">في الإصدارات السابقة من Microsoft Dynamics 365 for Retail، كانت معالجة المرتجعات في مقابل أوامر العملاء تتم باستخدام مستند أمر الإرجاع في Retail Headquarters.</span><span class="sxs-lookup"><span data-stu-id="bd414-104">In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail headquarters.</span></span> <span data-ttu-id="bd414-105">ومع ذلك، يمكن استخدام مستند أمر الإرجاع لمعالجة المنتجات المرتجعة فقط.</span><span class="sxs-lookup"><span data-stu-id="bd414-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="bd414-106">يُشار إلى المنتجات المرتجعة بكمية سالبة في بنود أمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="bd414-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="bd414-107">وبطريقة مغايرة، يُشار إلى المبيعات بكمية موجبة.</span><span class="sxs-lookup"><span data-stu-id="bd414-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="bd414-108">ومع ذلك، لا يدعم مستند أمر الإرجاع الكميات الموجبة.</span><span class="sxs-lookup"><span data-stu-id="bd414-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="bd414-109">وبسبب هذا القيد، لم تدعم الإصدارات السابقة من Retail السيناريوهات حيث كانت عمليات الاستبدال تتم فقط باستخدام مستند أمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="bd414-109">Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="bd414-110">ومع ذلك، تمت إضافة وظيفة لدعم السيناريوهات حيث تتم عمليات الاستبدال على الأوامر المرتجعة.</span><span class="sxs-lookup"><span data-stu-id="bd414-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="bd414-111">يستخدم Retail الآن مستند أمر المبيعات بدلاً من مستند أمر الإرجاع لمعالجة هذه الأنواع من الحركات.</span><span class="sxs-lookup"><span data-stu-id="bd414-111">Retail now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a><span data-ttu-id="bd414-112">تكوين Retail لدعم عمليات الاستبدال على أوامر الإرجاع</span><span class="sxs-lookup"><span data-stu-id="bd414-112">Configure Retail to support exchanges on return orders</span></span>

<span data-ttu-id="bd414-113">اتبع هذه الخطوات لتكوين النظام لدعم عمليات الاستبدال على أوامر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="bd414-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="bd414-114">انتقل إلى **البيع بالتجزئة \> إعداد Headquarters \> المعلمات \> معلمات Retail**.</span><span class="sxs-lookup"><span data-stu-id="bd414-114">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="bd414-115">على علامة التبويب السريعة **أوامر العملاء‬**، عيّن الخيار **معالجة أوامر الإرجاع كأوامر مبيعات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="bd414-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="bd414-116">شغّل وظيفة **جدول توزيع التكوين العمومي** (**1110**).</span><span class="sxs-lookup"><span data-stu-id="bd414-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="bd414-117">إجراء عملية استبدال</span><span class="sxs-lookup"><span data-stu-id="bd414-117">Make an exchange</span></span>

<span data-ttu-id="bd414-118">بعد أن يتم تكوين النظام كما ورد في المقطع السابق، سيحدد مستخدم نقطة البيع (POS) أمر مبيعات أو فاتورة مبيعات لمعالجة عملية إرجاع، كما هو الحال في إصدارات Retail السابقة.</span><span class="sxs-lookup"><span data-stu-id="bd414-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</span></span> <span data-ttu-id="bd414-119">ومع ذلك، بعد إضافة الأصناف المرتجعة إلى سلة التسوق، سيتمكن المستخدم من إضافة بنود مبيعات جديدة إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="bd414-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="bd414-120">بالنسبة إلى بنود المبيعات الجديدة هذه، يجب على المستخدم تحديد كافة السمات المطلوبة لمعالجة بند في أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="bd414-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="bd414-121">تتضمن هذه السمات أسلوب التسليم وموقع التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="bd414-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="bd414-122">سيكون الدفع المستحق للحركة عبارة عن قيمة صافية لبنود أمر الإرجاع وبنود أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="bd414-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="bd414-123">عند تقديم الدفع للحركة، سيتم ترحيل أمر الإرجاع كمستند أمر مبيعات في Retail Headquarters، وسيقوم النظام بفوترة بنود الإرجاع على الفور.</span><span class="sxs-lookup"><span data-stu-id="bd414-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="bd414-124">لتوفير رؤية أفضل لمختلف المبالغ في سلة التسوق، تمت إضافة ثلاثة حقول مبالغ جديدة إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="bd414-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="bd414-125">ويمكنك استخدام مصمم الشاشة لجعل كافة هذه الحقول الجديدة متوفرة في واجهة مستخدم (UI) نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="bd414-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="bd414-126">**‏‫تم استخدام الإيداع‬** – مبلغ الإيداع المطبق على حركة عندما يقوم المستخدم بانتقاء أمر العميل‬.</span><span class="sxs-lookup"><span data-stu-id="bd414-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="bd414-127">إذا لم يكن هناك أي مبلغ تجاوز الإيداع، وإذا تم تكوين إيداع بنسبة 10 بالمئة، سيكون المبلغ في هذا الحقل 90 بالمئة من المبلغ الإجمالي لأمر العميل.</span><span class="sxs-lookup"><span data-stu-id="bd414-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="bd414-128">**تنفيذ المبلغ** – المبلغ الإجمالي للبنود حيث تم تعيين وضع التسليم إلى **تنفيذ** عندما تم إنشاء أمر العميل أو تحريره، أو خلال استبدال أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="bd414-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="bd414-129">يتضمن المبلغ الموجود في هذا الحقل الضرائب والمصاريف.</span><span class="sxs-lookup"><span data-stu-id="bd414-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="bd414-130">**المبلغ المرتجع‬** – المبلغ الإجمالي للبنود ذات الكميات السالبة أثناء استبدال أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="bd414-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="bd414-131">يتضمن المبلغ الموجود في هذا الحقل الضرائب والمصاريف.</span><span class="sxs-lookup"><span data-stu-id="bd414-131">The amount in this field includes taxes and charges.</span></span>
