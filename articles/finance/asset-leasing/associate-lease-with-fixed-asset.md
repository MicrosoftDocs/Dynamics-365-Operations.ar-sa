---
title: إقران أصول ثابتة بعقد إيجار
description: يوضح الموضوع كيفية إقران أصل ثابت موجود بعقد إيجار جديد.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5c4f14d38b3cfc2c4d09cfeb5854204701250757
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260843"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="6f750-103">إقران أصول ثابتة بعقد إيجار</span><span class="sxs-lookup"><span data-stu-id="6f750-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f750-104">يوضح الموضوع كيفية إقران أصل ثابت موجود بعقد إيجار جديد.</span><span class="sxs-lookup"><span data-stu-id="6f750-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="6f750-105">عند إقران أصل ثابت بعقد إيجار، ستكون قيمة حق استخدام الأصل (ROU) الموجودة في التقييم الأولي هي تكلفة الاستحواذ للأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="6f750-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="6f750-106">قبل أن تتمكن من إقران أصل ثابت بعقد إيجار، فإنه يجب إنشاء سجل للأصل الثابت في الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="6f750-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="6f750-107">ثم، في الصفحة **ملخص عقد الإيجار**، فإنه يجب إنشاء عقد إيجار وربط الأصل بعقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="6f750-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="6f750-108">أضف عقد إيجار باتباع الخطوات الموجودة في [إضافة عقود إيجار أو نسخها](add-lease.md).</span><span class="sxs-lookup"><span data-stu-id="6f750-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="6f750-109">في الصفحة **إضافة عقد إيجار**، في الحقل **عدد الأصول الثابتة**، حدد الأصل الذي لم تستحوذ عليه بعد.</span><span class="sxs-lookup"><span data-stu-id="6f750-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="6f750-110">حدد **الدفاتر**، وقم بتأكيد جدول الدفع.</span><span class="sxs-lookup"><span data-stu-id="6f750-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="6f750-111">حدد **التقييم المبدئي**.</span><span class="sxs-lookup"><span data-stu-id="6f750-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="6f750-112">حدد **دفتر يومية تأجير الأصول**.</span><span class="sxs-lookup"><span data-stu-id="6f750-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="6f750-113">يعمل إدخال دفتر يومية التقييم المبدئي لعقد الإيجار على خصم الأصل الثابت للمبلغ الذي عادة ما يكون مدينًا لحساب أصل حق استخدام الأصل.</span><span class="sxs-lookup"><span data-stu-id="6f750-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="6f750-114">يمكنك الآن عرض نوع الحركة والدفتر الخاص بالأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="6f750-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="6f750-115">حدد **تفاصيل دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="6f750-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="6f750-116">حدد **البنود** لعرض البنود الفردية لإدخال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="6f750-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="6f750-117">حدد بند دفتر اليومية الذي يحتوي على الأصل، ثم حدد علامة التبويب **الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="6f750-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="6f750-118">تظهر علامة التبويب **الأصول الثابتة** نوع الحركة والدفتر.</span><span class="sxs-lookup"><span data-stu-id="6f750-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="6f750-119">افتراضيًا، يتم تعيين الحقل **نوع الحركة** على **الاستحواذ**، ويتم تعيين الحقل **دفتر اليومية** على الدفتر الحالي للأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="6f750-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="6f750-120">بعد أن تقوم بترحيل إدخال دفتر يومية التقييم المبدئي، تظهر الحركة كحركة الاستحواذ للأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="6f750-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="6f750-121">لعرض جدول الحركة، انتقل إلى **الأصول الثابتة \> الأصول الثابتة \> الأصول الثابتة**، حدد الأصل المناسب ثم حدد **التقييمات**.</span><span class="sxs-lookup"><span data-stu-id="6f750-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="6f750-122">يجب عليك رؤية أنه قد قام إدخال دفتر يومية التقييم المبدئي باكتساب الحركة للأصل الثابت المحدد.</span><span class="sxs-lookup"><span data-stu-id="6f750-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="6f750-123">يمكن الآن إهلاك الأصل الثابت من خلال استخدام وظيفة الإهلاك القياسي في الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="6f750-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="6f750-124">لمزيد من المعلومات حول الإهلاك، راجع [أساليب وقواعد الإهلاك](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="6f750-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6f750-125">في حالة إقران أصل ثابت بعقد إيجار، فإنه يتم تعطيل الزرين **إهلاك الأصل** و **انخفاض قيمة عقد الإيجار** في تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="6f750-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="6f750-126">يمكنك عرض الحركات الخاصة بإهلاك الأصل وخفض قيمة التأجير من الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="6f750-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="6f750-127">كذلك، يتم تعطيل الزر **حركات الأصول**، الذي يفتح نموذج استعلام.</span><span class="sxs-lookup"><span data-stu-id="6f750-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="6f750-128">يمكنك أيضًا فتح نموذج الاستعلام **حركات الأصول** في الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="6f750-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]