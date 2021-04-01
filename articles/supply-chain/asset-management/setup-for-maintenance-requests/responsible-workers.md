---
title: عاملو الصيانة المسؤولون
description: يشرح هذا الموضوع كيفية إعداد عاملي الصيانة المسؤولين في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad6b1757952fb0e5b970f82f75d99919a7f0745e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261155"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="a12e4-103">عاملو الصيانة المسؤولون</span><span class="sxs-lookup"><span data-stu-id="a12e4-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a12e4-104">بإمكان عاملي الصيانة المسؤولين أن يكونوا مرتبطي بأنواع الأصول والأصول ومواقع العمل وفئات نوع مهمة الصيانة وأنواع مهام الصيانة ومتغيرات نوع مهام الصيانة والوظائف التي تحتاج إلى تدريبات معينة.</span><span class="sxs-lookup"><span data-stu-id="a12e4-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="a12e4-105">ويمكن استخدامهم لتنفيذ أوامر العمل وطلبات الصيانة للإشارة إلى تفضيل حول عاملي الصيانة الذين ينبغي أن يكونوا مسؤولين عن أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="a12e4-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="a12e4-106">(ومع ذلك، فإن عاملي الصيانة هؤلاء ليسوا بالضرورة العاملين نفسهم الذين من المقرر أن يقوموا بتنفيذ أمر العمل.) استخدام هذه الوظيفة اختياري.</span><span class="sxs-lookup"><span data-stu-id="a12e4-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="a12e4-107">على سبيل المثال، يمكن استخدامها لتحديد العاملين المسؤولين أو مجموعات العاملين لأنواع عمل أو نواحٍ عمل محددة.</span><span class="sxs-lookup"><span data-stu-id="a12e4-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="a12e4-108">أثناء دورة حياة أمر العمل أو دورة حياة طلب الصيانة، يمكن تغيير عاملي الصيانة المسؤولين أو تحديثهم.</span><span class="sxs-lookup"><span data-stu-id="a12e4-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="a12e4-109">وقد يرتبط هذا التغيير أو التحديث، على سبيل المثال، بتغيير في حالة دورة حياة طلب الصيانة أو حالة دورة حياة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="a12e4-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="a12e4-110">الإعداد على صفحة **عاملو الصيانة المسؤولون** *غير* مستخدم أثناء جدولة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="a12e4-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="a12e4-111">في إدارة الأصول، يمكنك أيضًا‏‎ إعداد عاملي الصيانة *المفضلين* الذين قد يتم تخصيصهم إلى أوامر العمل أثناء جدولة أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="a12e4-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="a12e4-112">قبل أن تتمكن من إعداد عاملي الصيانة المسؤولين، يجب إعداد العاملين ومجموعات عاملي الصيانة التي يجب أن تكون متاحة للاختيار.</span><span class="sxs-lookup"><span data-stu-id="a12e4-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="a12e4-113">للحصول على معلومات حول كيفيه إعداد العاملين ومجموعات عاملي الصيانة، راجع [عاملو الصيانة ومجموعات عاملي الصيانة‬](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="a12e4-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="a12e4-114">إعداد عمال الصيانة المسؤولين</span><span class="sxs-lookup"><span data-stu-id="a12e4-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="a12e4-115">حدد **إدارة الأصول** \> **الإعداد** \> **العاملون** \> **عاملو الصيانة المسؤولون**.</span><span class="sxs-lookup"><span data-stu-id="a12e4-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="a12e4-116">حدد **جديد** لإنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="a12e4-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="a12e4-117">أولاً قم بإنشاء عامل صيانة مسؤول افتراضي أو إعداد مجموعة عاملي صيانة مسؤولين حيث تقوم بتعيين حقل **مجموعة عاملي صيانة مسؤولين** و/أو **عامل مسؤول** فقط.</span><span class="sxs-lookup"><span data-stu-id="a12e4-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="a12e4-118">اترك الحقول المتبقية فارغة.</span><span class="sxs-lookup"><span data-stu-id="a12e4-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="a12e4-119">سيتم استخدام هذا الإعداد الافتراضي أثناء جدولة أمر العمل إذا لم تطابق تركيبة أخرى أكثر تحديداً محتويات أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="a12e4-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a12e4-120">أثناء إنشاء طلب صيانة، عندما يتم توفير عامل صيانة مسؤول أو مجموعة عاملي صيانة مسؤولين للتحديد على الصفحة **جميع طلبات الصيانة**، تمر إدارة الأصول على كافة سجلات عاملي الصيانة المسؤولين للتحقق من وجود تطابق محتمل.</span><span class="sxs-lookup"><span data-stu-id="a12e4-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="a12e4-121">وهي تتحقق دائمًا من المجموعة الأكثر تحديدًا أولاً.</span><span class="sxs-lookup"><span data-stu-id="a12e4-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="a12e4-122">وبعبارة أخرى، تقوم إدارة الأصول أولاً بالتحقق من أي تطابق في حقل **التجارة** .</span><span class="sxs-lookup"><span data-stu-id="a12e4-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="a12e4-123">إذا لم يتم العثور على تطابق، فهي تتحقق من وجود تطابق لحقل **متغير نوع مهمة الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="a12e4-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="a12e4-124">إذا لم يتم العثور على تطابق، فهي تتحقق من وجود تطابق لحقل **نوع مهمة الصيانة**، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="a12e4-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="a12e4-125">كما ترون في تخطيط الصفحة، وهذا السلوك يعني أنه، للعثور على التركيبة الأكثر تحديدًا، تتحقق إدارة الأصول من كل سجل من اليمين إلى اليسار بحثًا عن تطابق (أولا **التجارة**، ثم **متغير نوع مهمة الصيانة**، ثم **نوع مهمة الصيانة**، ثم **فئة نوع مهمة الصيانة**، ثم **موقع العمل**، ثم **الأصل**، وأخيرًا **نوع الأصل**).</span><span class="sxs-lookup"><span data-stu-id="a12e4-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="a12e4-126">إذا لم يتم العثور على تطابق، يتم استخدام السجل الافتراضي الذي لا يحتوي على تحديدات في هذه الحقول السبعة.</span><span class="sxs-lookup"><span data-stu-id="a12e4-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="a12e4-127">يبين الرسم التوضيحي التالي مثالاً لصفحة **عاملو الصيانة المسؤولون**.</span><span class="sxs-lookup"><span data-stu-id="a12e4-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![صفحة عاملي الصيانة المسؤولين](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]