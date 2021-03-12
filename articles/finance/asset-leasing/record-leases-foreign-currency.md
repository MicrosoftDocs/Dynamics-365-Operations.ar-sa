---
title: تسجيل عقود الإيجار بالعملات الأجنبية
description: يوضح هذا الموضوع كيفية تسجيل عقود الإيجارات بعملات مختلفة عن عملة المحاسبة أو عملة التقارير.
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
ms.openlocfilehash: 7f70442450cc1c814ae23e41a1feb3a63f2aade8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992879"
---
# <a name="record-leases-in-foreign-currencies"></a><span data-ttu-id="6d57e-103">تسجيل عقود الإيجار بالعملات الأجنبية</span><span class="sxs-lookup"><span data-stu-id="6d57e-103">Record leases in foreign currencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d57e-104">يتم إنشاء حسابات إيجار الأصول لعقود الإيجار بعملات مختلفة عن عملة المحاسبة أو عملة التقارير في الصفحة **إعداد دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-104">Asset leasing accounts for leases that are in currencies other than the accounting currency or the reporting currency are established on the **Ledger setup** page.</span></span> <span data-ttu-id="6d57e-105">يجب إدخال كافة عقود الإيجار بعملة الحركة الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="6d57e-105">All leases should be entered in their transaction currency.</span></span> <span data-ttu-id="6d57e-106">بمعني آخر، يجب إدخالها بالعملة المحددة في عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="6d57e-106">In other words, they should be entered in the currency that is specified in the lease contract.</span></span> <span data-ttu-id="6d57e-107">يوضح هذا الموضوع كيفية تسجيل عقود الإيجارات بعملات مختلفة عن عملة المحاسبة أو عملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="6d57e-107">This topic explains how to record leases in currencies other than the accounting or reporting currency.</span></span>

<span data-ttu-id="6d57e-108">إذا قمت بإدخال عقد إيجار بعملة أجنبية، فإنه سيتم إهلاك حق استخدام الأصل بعملة المحاسبة وعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="6d57e-108">If you enter a lease in a foreign currency, the right-of-use (ROU) asset is depreciated in both the accounting currency and the reporting currency.</span></span> <span data-ttu-id="6d57e-109">يتم تكوين هذه العملات في الصفحة **إعداد دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-109">These currencies are configured on the **Ledger setup** page.</span></span> <span data-ttu-id="6d57e-110">يستخدم هذا السلوك أيضًا في الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="6d57e-110">This behavior is also used in Fixed assets.</span></span> <span data-ttu-id="6d57e-111">عند إنشاء عقد إيجار بعملة أجنبية، حدد عملة الحركة في الحقل **العملة**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-111">When you create a lease in a foreign currency, select the transaction currency in the **Currency** field.</span></span>

<span data-ttu-id="6d57e-112">يعتبر سعر صرف عملة المحاسبة هو القيمة الافتراضية في الحقل **سعر صرف عملة المحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-112">The exchange rate of the accounting currency is the default value in **Accounting currency exchange rate** field.</span></span> <span data-ttu-id="6d57e-113">يعتبر سعر صرف عملة التقارير هو القيمة الافتراضية في الحقل **سعر صرف عملة التقارير**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-113">The exchange rate of the reporting currency is the default value in the **Reporting currency exchange rate** field.</span></span> <span data-ttu-id="6d57e-114">وكانت أسعار الصرف مؤثرة على تاريخ تاريخ بدء عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="6d57e-114">These exchange rates were effective on the commencement date of the lease.</span></span> <span data-ttu-id="6d57e-115">يوجد الحقل **سعر الصرف بعملة المحاسبة** والحقل **سعر صرف عملة التقارير** في علامة التبويب السريعة **المعلومات المالية والتقارير لسعر الصرف**، في الصفحة **تفاصيل الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-115">The **Accounting currency exchange rate** and **Reporting currency exchange rate** fields, are in the **Financial and reporting exchange information** FastTab, on the **Lease details** page.</span></span>

1. <span data-ttu-id="6d57e-116">حدد خانة الاختيار **السعر الثابت** لتجاوز سعر الصرف الذي تم إدخاله تلقائيًا، ثم أدخل السعر الجديد.</span><span class="sxs-lookup"><span data-stu-id="6d57e-116">Select the **Fixed rate** check box to override the exchange rate that was automatically entered, and then enter the new rate.</span></span>
2. <span data-ttu-id="6d57e-117">في الحقول الأخرى، أدخل المعلومات المطلوبة لعقد الإيجار، ثم حدد **إنشاء جداول**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-117">In the other fields, enter the information that is required for the lease, and then select **Create schedules**.</span></span>
3. <span data-ttu-id="6d57e-118">في الصفحة **تفاصيل عقد الإيجار** الجديدة، حدد **الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-118">On the new **Lease details** page, select **Books**.</span></span>
4. <span data-ttu-id="6d57e-119">في الصفحة **دفتر الإيجار**، في علامة التبويب **المعلومات المالية والتقارير لسعر الصرف**، تحقق من قيم الحقل **حق استخدام الأصل الأولي لعملة المحاسبة** والحقل **حق استخدام الأصل الأولي لعملة التقارير**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-119">On the **Lease book** page, on the **Financial and reporting exchange information** tab, verify the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span> <span data-ttu-id="6d57e-120">يعرض كل حقل من هذه الحقول رصيد حق استخدام الأصل بالعملة المطابقة.</span><span class="sxs-lookup"><span data-stu-id="6d57e-120">Each of these fields shows the translated ROU asset balance in the corresponding currency.</span></span> <span data-ttu-id="6d57e-121">يتم تحديث هذه الحقول كلما قمت بتغيير أية معلومات مالية.</span><span class="sxs-lookup"><span data-stu-id="6d57e-121">These fields are updated whenever you change any financial information.</span></span> <span data-ttu-id="6d57e-122">حدد **إنشاء جداول** قبل تأكيد جدول الدفع.</span><span class="sxs-lookup"><span data-stu-id="6d57e-122">Select **Create schedules** before you confirm the payment schedule.</span></span>

    <span data-ttu-id="6d57e-123">يعمل إدخال دفتر يومية التقييم الأولي على تسجيل حق استخدام الأصل الذي يستخدم أسعار صرف العملة المدرجة في عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="6d57e-123">The initial recognition journal entry records the ROU asset that uses the currency exchange rates that are listed on the lease.</span></span> <span data-ttu-id="6d57e-124">يتضمن إدخال دفتر اليومية قيم الحقل **حق استخدام الأصل الأولي بعملة المحاسبة** والحقل **حق استخدام الأصل الأولي بعملة التقارير**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-124">The journal entry also includes the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

## <a name="subsequent-measurement-for-foreign-currency-leases"></a><span data-ttu-id="6d57e-125">قياس لاحق لعقود الإيجار بالعملة الأجنبية</span><span class="sxs-lookup"><span data-stu-id="6d57e-125">Subsequent measurement for foreign currency leases</span></span>

<span data-ttu-id="6d57e-126">يعرض جدول الإهلاك مبالغ مصروفات الإهلاك المتوقعة بعملة التقارير وعملة المحاسبة وعملة الحركة.</span><span class="sxs-lookup"><span data-stu-id="6d57e-126">The depreciation schedule shows the expected depreciation expense amounts in the reporting currency, the accounting currency, and the transaction currency.</span></span>

<span data-ttu-id="6d57e-127">لعرض أرصدة حق استخدام الأصل ومبالغ الإهلاك إما بعملة التقارير أو عملة المحاسبة، افتح الصفحة **جدول إهلاك الأصول**، ثم حدد خانة الاختيار **عرض مبالغ بعملة المحاسبة** أو **عرض مبالغ بعملة التقارير**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-127">To view the ROU asset balances and depreciation amounts in either the reporting currency or the accounting currency, open the **Asset depreciation schedule** page, and select the **Show accounting currency amounts** or **Show reporting currency amounts** check box.</span></span>

<span data-ttu-id="6d57e-128">عند إنشاء إدخالات دفتر يومية مصروفات الإهلاك مقابل عقد الإيجار الذي يتعين تسميته بعملة أجنبية، يستخدم الإدخال أسعار الصرف المدرجة في عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="6d57e-128">When you create the depreciation expense journal entries against a lease that is denominated in a foreign currency, the entry uses the exchange rates that are listed on the lease.</span></span> <span data-ttu-id="6d57e-129">كذلك، يستخدم قيم الحقل **حق استخدام الأصل الأولي بعملة المحاسبة** والحقل **حق استخدام الأصل الأولي بعملة التقارير**.</span><span class="sxs-lookup"><span data-stu-id="6d57e-129">It also uses the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

<span data-ttu-id="6d57e-130">يمكن حساب مبلغ مصروفات الإهلاك النهائي باستخدام سعر صرف مختلف قليلاً، بحيث يتم إهلاك حق استخدام الأصل بالكامل بعملة المحاسبة وعملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="6d57e-130">The final depreciation expense amount can be calculated by using a slightly different exchange rate, so that the ROU asset is fully depreciated in both the accounting currency and the reporting currency.</span></span>

<span data-ttu-id="6d57e-131">إذا تم إعادة تصنيف عقد الإيجار على أنه **إيجار مؤجل**، يقوم النظام تلقائيًا بإزالة أسعار الصرف الخاصة بالعملات المحاسبة والتقارير، إذا تم تحديدها بالفعل.</span><span class="sxs-lookup"><span data-stu-id="6d57e-131">If the lease has been reclassified as **Deferred rent**, the system automatically clears the exchange rates of the accounting and reporting currencies, if they have already been defined.</span></span>
