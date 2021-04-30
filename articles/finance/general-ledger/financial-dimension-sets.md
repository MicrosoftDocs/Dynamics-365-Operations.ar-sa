---
title: مجموعات الأبعاد المالية
description: يصف هذا الموضوع مجموعات الأبعاد المالية ويوفر بعض التلميحات لتحسين استخدامها.
author: yukonpeegs
manager: AnnBe
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b719d8eb868cb1722b470be4443d01181078ce21
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864402"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="6540e-103">مجموعات الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="6540e-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6540e-104">يصف هذا الموضوع مجموعات الأبعاد المالية ويوفر بعض التلميحات لتحسين استخدامها.</span><span class="sxs-lookup"><span data-stu-id="6540e-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="6540e-105">تعد مجموعة الأبعاد بمثابة قائمة تتضمن الأبعاد المالية التي يمكن استخدامها لتلخيص بيانات دفتر الأستاذ العام بطريقه معرّفة من قبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="6540e-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="6540e-106">الاستخدام الأساسي لمجموعات الأبعاد هو تحديد ميزان المراجعة.</span><span class="sxs-lookup"><span data-stu-id="6540e-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="6540e-107">مجموعه الأبعاد القياسية الوحيدة هي مجموعه الأبعاد التي تحتوي على الحساب الرئيسي فقط.</span><span class="sxs-lookup"><span data-stu-id="6540e-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="6540e-108">يمكنك استخدام الصفحة **مجموعات الأبعاد المالية** لإنشاء مجموعات الأبعاد المالية وإدارتها.</span><span class="sxs-lookup"><span data-stu-id="6540e-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="6540e-109">أرصدة مجموعات الأبعاد</span><span class="sxs-lookup"><span data-stu-id="6540e-109">Dimension set balances</span></span>

<span data-ttu-id="6540e-110">بإمكان مجموعة الأبعاد أن تتضمن أرصدة تعتمد على أبعادها المالية.</span><span class="sxs-lookup"><span data-stu-id="6540e-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="6540e-111">توجد الأرصدة في دفتر الأستاذ العام وتعتمد على تعريف مجموعة الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="6540e-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="6540e-112">يتم تلخيص الأرصدة من بيانات دفتر الأستاذ العام للمساعدة في تحسين الأداء عند استردادها (على سبيل المثال، عند إنشاء ميزان المراجعة).</span><span class="sxs-lookup"><span data-stu-id="6540e-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="6540e-113">إنشاء أرصدة</span><span class="sxs-lookup"><span data-stu-id="6540e-113">Create balances</span></span>

<span data-ttu-id="6540e-114">استخدم الزر **إنشاء أرصدة** لتهيئة الأرصدة لمجموعة أبعاد ليس لديها أرصدة في الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="6540e-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="6540e-115">نوصي بالحد من عدد مجموعات الأبعاد التي لديها أرصدة، وذلك لأن تحديثات الرصيد تؤثر على كافة أنشطة ترحيل دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="6540e-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="6540e-116">تحديث الأرصدة</span><span class="sxs-lookup"><span data-stu-id="6540e-116">Update balances</span></span>

<span data-ttu-id="6540e-117">استخدم الزر **تحديث الأرصدة** لتضمين آخر نشاط ترحيل لدفتر الأستاذ العام في الأرصدة.</span><span class="sxs-lookup"><span data-stu-id="6540e-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="6540e-118">تعد تحديثات الأرصدة عمليات خفيفة.</span><span class="sxs-lookup"><span data-stu-id="6540e-118">Balance updates are light operations.</span></span> <span data-ttu-id="6540e-119">يجب عليها أن تقوم فقط بترحيل نشاط ترحيل دفتر الأستاذ العام الذي حدث مند آخر تحديث.</span><span class="sxs-lookup"><span data-stu-id="6540e-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="6540e-120">يؤدي عرض ميزان المراجعة إلى فرض تحديث، للتأكد من أن الأرصدة المعروضة هي أرصدة حالية.</span><span class="sxs-lookup"><span data-stu-id="6540e-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="6540e-121">يمكنك استخدام وظيفة دفعية متكررة بحيث تتم تحديثات مجموعات الأبعاد المستخدمة بشكل متكرر بطريقة أسرع.</span><span class="sxs-lookup"><span data-stu-id="6540e-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="6540e-122">وبهذه الطريقة، فأنت تساعد على تقليل الوقت الذي يجب علي المستخدمين فيه انتظار ميزان المراجعة.</span><span class="sxs-lookup"><span data-stu-id="6540e-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="6540e-123">إعادة إنشاء الأرصدة</span><span class="sxs-lookup"><span data-stu-id="6540e-123">Rebuild balances</span></span>

<span data-ttu-id="6540e-124">استخدم الزر **إعادة إنشاء الأرصدة** لإعادة إنشاء الأرصدة‏‎ من البداية.</span><span class="sxs-lookup"><span data-stu-id="6540e-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="6540e-125">وبهذه الطريقة، فأنت تساعد على التأكد من أنها تطابق البيانات في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="6540e-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="6540e-126">تتطلب إعادة بناء الأرصدة الكثير من المعالجة ومن غير المفترض أن تكون مطلوبة عادةً.</span><span class="sxs-lookup"><span data-stu-id="6540e-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="6540e-127">إذا كان لديك سيناريو يتطلب إعادة بناء الأرصدة بانتظام، فمن الأفضل أن تتصل بدعم العملاء.</span><span class="sxs-lookup"><span data-stu-id="6540e-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="6540e-128">بإمكان قسم دعم العملاء أن يساعدك في تحديد سبب عدم تطابق الأرصدة مع البيانات الموجودة في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="6540e-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="6540e-129">مسح الأرصدة</span><span class="sxs-lookup"><span data-stu-id="6540e-129">Clear balances</span></span>

<span data-ttu-id="6540e-130">استخدم الزر **مسح الأرصدة** لإزالة الأرصدة وإيقاف أي تحديثات لاحقة.</span><span class="sxs-lookup"><span data-stu-id="6540e-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="6540e-131">ولن يعود لمجموعة الأبعاد أي تأثير على أنشطة ترحيل دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="6540e-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="6540e-132">لمزيد من المعلومات، راجع [الأبعاد المالية‬](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="6540e-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
