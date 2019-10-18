---
title: تعيين أعضاء أبعاد عنصر التكلفة لمجموعة شائعة من أعضاء الأبعاد
description: من خلال تعيين أعضاء أبعاد عنصر تكلفة مختلفين إلى مجموعة مشتركة من أعضاء أبعاد عنصر تكلفة، ستقوم بدمج البيانات في تنسيق مشترك لأغراض التحليل.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: deb9b5aab9cd69270c78d4e1ea0e2a6cac6ac370
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176232"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="df5bc-103">تعيين أعضاء أبعاد عنصر التكلفة لمجموعة شائعة من أعضاء الأبعاد</span><span class="sxs-lookup"><span data-stu-id="df5bc-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df5bc-104">من خلال تعيين أعضاء أبعاد عنصر تكلفة مختلفين إلى مجموعة مشتركة من أعضاء أبعاد عنصر تكلفة، ستقوم بدمج البيانات في تنسيق مشترك لأغراض التحليل.</span><span class="sxs-lookup"><span data-stu-id="df5bc-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="df5bc-105">إذا كنت شركة عالمية تمتثل لمتطلبات المحاسبة القانونية، فقد تستخدم أدلة حسابات متعددة.</span><span class="sxs-lookup"><span data-stu-id="df5bc-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="df5bc-106">عندما تقوم باستيراد أعضاء أبعاد عنصر تكلفة من أدلة حسابات مختلفة، قد ينتهي بك الأمر بالحصول على مزيج حسابات.</span><span class="sxs-lookup"><span data-stu-id="df5bc-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="df5bc-107">ومع ذلك، فإن هذه الحسابات قد تكون مماثلة في الواقع من حيث طبيعتها، وقد تحتاج إلى تحليل وتوزيع التكاليف الخاصة بها باستخدام تنسيق مشترك.</span><span class="sxs-lookup"><span data-stu-id="df5bc-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="df5bc-108">تعيين أعضاء أبعاد عنصر التكلفة‬ إلى تنسيق مشترك</span><span class="sxs-lookup"><span data-stu-id="df5bc-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="df5bc-109">يوضح المثال التالي كيف يمكنك أنت، بصفتك مراقب التكاليف، إنشاء بُعد جديد لعنصر تكلفة في محاسبة التكاليف يقوم بتعيين أعضاء أبعاد عنصر التكلفة من بنية دليل الحسابات الأمريكي وبنية دليل الحسابات الفرنسي إلى مجموعة مشتركة من أعضاء أبعاد عنصر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="df5bc-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="df5bc-110">ويمكنك عندئذٍ استخدام المجموعة المشتركة من أعضاء أبعاد عنصر التكلفة لتحليل بيانات التكلفة من الكيانين القانونيين في دفتر أستاذ محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="df5bc-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="df5bc-111">المصدر: دليل الحسابات الأمريكي</span><span class="sxs-lookup"><span data-stu-id="df5bc-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="df5bc-112">المصدر: دليل الحسابات الفرنسي</span><span class="sxs-lookup"><span data-stu-id="df5bc-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="df5bc-113">مجموعة مشتركة جديدة من أعضاء أبعاد عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="df5bc-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="df5bc-114">استيراد أعضاء أبعاد عنصر التكلفة من دليل الحسابات الأمريكي</span><span class="sxs-lookup"><span data-stu-id="df5bc-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="df5bc-115">أعضاء أبعاد عنصر التكلفة المستوردون من دليل الحسابات الفرنسي</span><span class="sxs-lookup"><span data-stu-id="df5bc-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="df5bc-116">تعيين أعضاء أبعاد عنصر التكلفة الأمريكيين والفرنسيين إلى مجموعة مشتركة</span><span class="sxs-lookup"><span data-stu-id="df5bc-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="df5bc-117">5001: المبيعات</span><span class="sxs-lookup"><span data-stu-id="df5bc-117">5001: Sales</span></span>                                                           | <span data-ttu-id="df5bc-118">5001: المبيعات والإعلانات</span><span class="sxs-lookup"><span data-stu-id="df5bc-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="df5bc-119">5000: المبيعات والإعلانات</span><span class="sxs-lookup"><span data-stu-id="df5bc-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="df5bc-120">5030: الإعلانات</span><span class="sxs-lookup"><span data-stu-id="df5bc-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="df5bc-121">6390: شراء المخزون\*</span><span class="sxs-lookup"><span data-stu-id="df5bc-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="df5bc-122">7000: مصروفات التنظيف</span><span class="sxs-lookup"><span data-stu-id="df5bc-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="df5bc-123">7001: مصروفات التنظيف</span><span class="sxs-lookup"><span data-stu-id="df5bc-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="df5bc-124">7001: مصروفات السفر</span><span class="sxs-lookup"><span data-stu-id="df5bc-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="df5bc-125">7001: مصروفات السفر</span><span class="sxs-lookup"><span data-stu-id="df5bc-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="df5bc-126">\*لم يتم تعيين عضو بُعد عنصر التكلفة الفرنسي لشراء المخزون.</span><span class="sxs-lookup"><span data-stu-id="df5bc-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="df5bc-127">تحويل العملة</span><span class="sxs-lookup"><span data-stu-id="df5bc-127">Currency conversion</span></span>
<span data-ttu-id="df5bc-128">من المحتمل أن يكون قد تم إعداد أدلة الحسابات المختلفة التي تستخدمها لاستخدام عملات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="df5bc-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="df5bc-129">في هذه الحالة، تأكد من تحديد تحويل عملة، بحيث تتم معالجة بيانات التكلفة باستخدام العملة الصحيحة، كما هو محدد في دفتر أستاذ محاسبة التكاليف حيث يتم استخدام أعضاء أبعاد عنصر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="df5bc-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="df5bc-130">في المثال السابق، إذا تم استخدام الدولار الأمريكي (USD) في دفتر أستاذ محاسبة التكاليف، فيجب إنشاء تحويل عملة من الدولار إلى اليورو (EUR) لمعالجة الحركات لأعضاء أبعاد عنصر التكلفة المعينين.</span><span class="sxs-lookup"><span data-stu-id="df5bc-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="df5bc-131">تحديث التعيينات في أي وقت</span><span class="sxs-lookup"><span data-stu-id="df5bc-131">Update mappings at any time</span></span>
<span data-ttu-id="df5bc-132">يمكنك تحديث تعريفات التعيينات لبُعد عنصر تكلفة في أي وقت.</span><span class="sxs-lookup"><span data-stu-id="df5bc-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="df5bc-133">ولأن التعيينات غير محددة بتاريخ سريان، فسيتم تطبيق التغييرات في المرة التالية التي تقوم فيها بمعالجة حركات التكلفة أو تشغيل حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="df5bc-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>



