---
title: دفتر أستاذ محاسبة المخزون العالمي
description: يصف هذا الموضوع دفاتر الأستاذ لمحاسبة المخزون العالمي، والتي يتم تعريفها بواسطة مجموعة من العملة والتقويم والقواعد والارتباط بكيان قانوني.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273106"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="8bdea-103">دفتر أستاذ محاسبة المخزون العالمي</span><span class="sxs-lookup"><span data-stu-id="8bdea-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="8bdea-104">محاسبة المخزون العلمي لديها مجموعة خاصة بها من دفاتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="8bdea-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="8bdea-105">في كل مرة تتم فيها معالجة حركة متعلقة بالمخزون لكيان قانوني ذي صلة، يمكن للنظام حساب تلك الحركة في أي عدد من دفاتر الأستاذ لمحاسبة المخزون العالمي، كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="8bdea-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="8bdea-106">دفتر الأستاذ العام عبارة عن سجل مقاييس الدائن والمدين.</span><span class="sxs-lookup"><span data-stu-id="8bdea-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="8bdea-107">وتصنف هذه المقاييس باستخدام عناصر التكلفة وحسابات دفتر الأستاذ الفرعي.</span><span class="sxs-lookup"><span data-stu-id="8bdea-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="8bdea-108">يتم تحديد دفتر الأستاذ لمحاسبة المخزون العالمي حسب تعريفه للعملة والتقويم والقواعد والارتباط بكيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="8bdea-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="8bdea-109">لإعداد دفاتر الأستاذ لمحاسبة المخزون العالمي، انتقل إلى **محاسبة المخزون العالمي \> الإعداد \> دفاتر أستاذ محاسبة المخزون العالمي**.</span><span class="sxs-lookup"><span data-stu-id="8bdea-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="8bdea-110">بالنسبة لكل دفتر أستاذ، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="8bdea-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="8bdea-111">**الاسم** - أدخل اسم دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="8bdea-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="8bdea-112">**الوصف**، أدخل وصفًا لدفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="8bdea-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="8bdea-113">**التقويم المالي** – حدد التقويم المالي لدفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="8bdea-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="8bdea-114">**نوع سعر الصرف والعملة** – استخدم الحقول الموجودة في علامة التبويب السريعة هذه لتحديد عملة المحاسبة التي يستخدمها دفتر الأستاذ ونوع سعر الصرف.</span><span class="sxs-lookup"><span data-stu-id="8bdea-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="8bdea-115">يمكن أن تختلف العملة التي تحددها عن العملة التي يستخدمها الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="8bdea-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="8bdea-116">في محاسبة المخزون العالمي، يمكن للمستخدمين تعريف دفاتر الأستاذ للتكاليف حسب تتطلب.</span><span class="sxs-lookup"><span data-stu-id="8bdea-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="8bdea-117">تدعم محاسبة المخزون العالمية محاسبة المخزون بعملات متعددة وفي تقييمات متعددة.</span><span class="sxs-lookup"><span data-stu-id="8bdea-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="8bdea-118">قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="8bdea-118">Set the following fields:</span></span>

    - <span data-ttu-id="8bdea-119">**العملة** – حدد عملة التكاليف التي يتم الاحتفاظ بالقيم المرتبطة بالمخزون بها.</span><span class="sxs-lookup"><span data-stu-id="8bdea-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="8bdea-120">وتشمل هذه القيم قيمة المخزون وتكلفة البضائع المبيعة والمخزون بالطريق وجميع أنواع التباين.</span><span class="sxs-lookup"><span data-stu-id="8bdea-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="8bdea-121">**نوع سعر الصرف** – حدد سعر الصرف الذي يجب أن يستخدمه النظام لتحويل مبلغ الحركة بعملة الحركة والتكلفة القياسية للأصناف إلى عملة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="8bdea-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="8bdea-122">**اسم القاعدة** – حدد قاعدة.</span><span class="sxs-lookup"><span data-stu-id="8bdea-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="8bdea-123">القاعدة عبارة عن مجموعة من السياسات التي تحدد كيفية حساب التكاليف في دفتر الأستاذ هذا.</span><span class="sxs-lookup"><span data-stu-id="8bdea-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="8bdea-124">**الكيان القانوني** – سيقوم دفتر الأستاذ بحساب المستندات التي يتم ترحيلها إلى الكيان القانوني المحدد.</span><span class="sxs-lookup"><span data-stu-id="8bdea-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="8bdea-125">**التهيئة** – حدد ما إذا كان يجب معالجة حركات المخزون التي تم إنشاؤها قبل إنشاء دفتر الأستاذ وفقًا للعملة والقاعدة في دفتر الأستاذ أم لا.</span><span class="sxs-lookup"><span data-stu-id="8bdea-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="8bdea-126">حدد إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="8bdea-126">Select one of the following values:</span></span>

    - <span data-ttu-id="8bdea-127">**منشَّط** – يجب أن يعالج دفتر الأستاذ الحركات التي تم إنشاؤها قبل إنشاء دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="8bdea-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="8bdea-128">**غير منشَّط** – يجب أن يعالج دفتر الأستاذ الحركات التي يتم إنشاؤها بعد إنشاء دفتر الأستاذ فقط.</span><span class="sxs-lookup"><span data-stu-id="8bdea-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8bdea-129">**لن** تتمكن من العودة وتعيين هذا الحقل بعد إدخال مستندات جديدة.</span><span class="sxs-lookup"><span data-stu-id="8bdea-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="8bdea-130">**الحالة** – يقوم النظام تلقائيًا بتعيين حالة دفاتر الأستاذ التي تم إنشاؤها حديثًا إلى *إعداد*.</span><span class="sxs-lookup"><span data-stu-id="8bdea-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
