---
title: إعداد دفاتر التأجير
description: يصف هذا الموضوع المعلومات التي يتم الاحتفاظ بها في دفاتر عقد الإيجار. تحتوي دفاتر عقد الإيجار على نهج المحاسبة التي تحدد كيفية حساب الإيجار في النظام.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440146"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="1818e-104">إعداد دفاتر التأجير</span><span class="sxs-lookup"><span data-stu-id="1818e-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1818e-105">تحتوي دفاتر عقد الإيجار على نهج المحاسبة التي تحدد كيفية حساب الإيجار في النظام.</span><span class="sxs-lookup"><span data-stu-id="1818e-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="1818e-106">بالإضافة إلى المحاسبة الأساسية النقدية، يدعم تأجير الأصول المعايير التالية:</span><span class="sxs-lookup"><span data-stu-id="1818e-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="1818e-107">مبادئ المحاسبة مقبولة بشكل عام في الولايات المتحدة (US GAAP)</span><span class="sxs-lookup"><span data-stu-id="1818e-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="1818e-108">موضوع صياغة مقاييس المحاسبة 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="1818e-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="1818e-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="1818e-109">ASC 840</span></span>
- <span data-ttu-id="1818e-110">مقاييس Financial Reporting الدولية 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="1818e-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="1818e-111">مقاييس المحاسبة الدولية 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="1818e-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="1818e-112">لإنشاء دفتر عقد إيجار، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="1818e-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="1818e-113">انتقل إلى **تأجير الأصول \> الضبط \> دفاتر عقد الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="1818e-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="1818e-114">حدد **جديد** لإضافة دفتر.</span><span class="sxs-lookup"><span data-stu-id="1818e-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="1818e-115">قم بتعيين الحقول التالية.</span><span class="sxs-lookup"><span data-stu-id="1818e-115">Set the following fields.</span></span>

    | <span data-ttu-id="1818e-116">الاسم</span><span class="sxs-lookup"><span data-stu-id="1818e-116">Name</span></span>                                     | <span data-ttu-id="1818e-117">الوصف</span><span class="sxs-lookup"><span data-stu-id="1818e-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="1818e-118">طبقة الترحيل</span><span class="sxs-lookup"><span data-stu-id="1818e-118">Posting layer</span></span>                            | <span data-ttu-id="1818e-119">حدد طبقة الترحيل المطلوب استخدامها.</span><span class="sxs-lookup"><span data-stu-id="1818e-119">Select the posting layer to use.</span></span> <span data-ttu-id="1818e-120">يتم إعداد كل دفتر مرفق بعقد إيجار لطبقة ترحيل محددة.</span><span class="sxs-lookup"><span data-stu-id="1818e-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="1818e-121">لكل طبقة ترحيل أغراض ترحيل مختلفة.</span><span class="sxs-lookup"><span data-stu-id="1818e-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="1818e-122">نوع عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="1818e-122">Lease type</span></span>                               | <span data-ttu-id="1818e-123">حدد ما إذا كان يجب تصنيف عقد الإيجار تلقائيًا أم لا، أو ما إذا كان ينبغي تحديده مسبقًا كعقد تمويلي أو تشغيلي.</span><span class="sxs-lookup"><span data-stu-id="1818e-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="1818e-124">الإطار المحاسبي</span><span class="sxs-lookup"><span data-stu-id="1818e-124">Accounting framework</span></span>                     | <span data-ttu-id="1818e-125">حدد إطار العمل المرتبط بالدفتر.</span><span class="sxs-lookup"><span data-stu-id="1818e-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="1818e-126">إعداد فترة الإيجار/العمر الإنتاجي</span><span class="sxs-lookup"><span data-stu-id="1818e-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="1818e-127">سيقوم النظام بتصنيف عقد الإيجار كتمويلي في حالة تعيين نوع عقد الإيجار على **تلقائي**، وإذا كان العمر الإنتاجي للأصل أكبر من أو يساوي النسبة المئوية المحددة في هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="1818e-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="1818e-128">إعداد القيمة الحالية / القيمة العادلة للأصل</span><span class="sxs-lookup"><span data-stu-id="1818e-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="1818e-129">أدخل رقمًا صحيحًا لتحديد الحد الذي سيحدد نوع عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="1818e-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="1818e-130">إذا كانت القيمة الحالية في الحد الأدنى المستقبلي لدفعات عقد الإيجار أكبر من القيمة المحددة من قبل إعداد الدفتر، وإذا تم تعيين تصنيف عقد إيجار الدفتر على تلقائي، سيقوم النظام بتصنيف عقد الإيجار كعقد إيجار تمويلي.</span><span class="sxs-lookup"><span data-stu-id="1818e-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="1818e-131">الحد قصير الأجل</span><span class="sxs-lookup"><span data-stu-id="1818e-131">Short-term threshold</span></span>                     | <span data-ttu-id="1818e-132">أدخل عدد الشهور لاستخدامها كحد لإيجارات قصيرة الأجل.</span><span class="sxs-lookup"><span data-stu-id="1818e-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="1818e-133">وإذا كانت فترة الإيجار أقل من أو تساوي عدد الشهور التي يتم إدخالها هنا، سيقوم النظام بتصنيف عقد الإيجار كإيجار قصير الأجل وسيتم تطبيق معاملة الإيجار المؤجل.</span><span class="sxs-lookup"><span data-stu-id="1818e-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="1818e-134">حد القيمة المنخفضة</span><span class="sxs-lookup"><span data-stu-id="1818e-134">Low value threshold</span></span>                      | <span data-ttu-id="1818e-135">أدخل مبلغ لاستخدامه كحد لعقود إيجار أصول منخفضة القيمة.</span><span class="sxs-lookup"><span data-stu-id="1818e-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="1818e-136">وإذا كانت القيمة العادلة للأصل أقل من أو تساوي القيمة يتم إدخالها هنا، سيقوم النظام بتصنيف عقد الإيجار كعقد إيجار أصول منخفضة القيمة وسيتم تطبيق معاملة الإيجار المؤجل.</span><span class="sxs-lookup"><span data-stu-id="1818e-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="1818e-137">دفع للمورّد</span><span class="sxs-lookup"><span data-stu-id="1818e-137">Pay to vendor</span></span>                            | <span data-ttu-id="1818e-138">قم بتعيين هذا الخيار إلى **نعم** للسماح بترحيل دفعات الإيجار، كفاتورة، إلى حساب المورد الذي يتم تحديده في كل عقد إيجار.</span><span class="sxs-lookup"><span data-stu-id="1818e-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="1818e-139">عند ترحيل دفعات الإيجار، ستتم إضافة حساب المورد.</span><span class="sxs-lookup"><span data-stu-id="1818e-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="1818e-140">إذا تم تعيين هذا الخيار إلى **لا**، فإنه ستتم إضافة الحساب الذي يتم تحديده لنوع ترحيل **دفعات الإيجار** على الصفحة **معلمات ترحيل عقد الإيجار** بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="1818e-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
