---
title: إنشاء قواعد متقدمة لدفاتر اليومية
description: يوضح هذا الإجراء إنشاء قواعد متقدمة لدفاتر اليومية.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e61ed731c4040e7351e20421f6cf217ae9a4641d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222349"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="10a90-103">إنشاء قواعد متقدمة لدفاتر اليومية</span><span class="sxs-lookup"><span data-stu-id="10a90-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10a90-104">يوضح هذا الإجراء إنشاء قواعد متقدمة لدفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="10a90-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="10a90-105">ويشمل هذا إعداد قيود التحكم في دفتر اليومية وترحيل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="10a90-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="10a90-106">ويستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="10a90-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="10a90-107">إعداد التحكم في دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="10a90-107">Set up journal control</span></span>
1. <span data-ttu-id="10a90-108">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > دفتر الأستاذ العام > إعداد دفتر اليومية > أسماء دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="10a90-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="10a90-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="10a90-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="10a90-110">انقر فوق **التحكم في دفتر اليومية‬‬** في **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="10a90-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="10a90-111">على علامة التبويب السريعة **ما هي أنواع الحسابات التي يمكن ترحيلها**، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="10a90-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="10a90-112">في الحقل **حسابات الشركة**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10a90-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="10a90-113">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="10a90-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="10a90-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10a90-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="10a90-115">على علامة التبويب السريعة **ما هي قيم الأجزاء الصالحة لدفتر اليومية هذا**، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="10a90-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="10a90-116">في الحقل **بنية الحساب**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10a90-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="10a90-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="10a90-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="10a90-118">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10a90-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="10a90-119">في الحقل **الشريحة**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10a90-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="10a90-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10a90-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="10a90-121">في الحقل **من القيمة**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10a90-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="10a90-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="10a90-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="10a90-123">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10a90-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="10a90-124">في الحقل **إلى القيمة‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10a90-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="10a90-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="10a90-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="10a90-126">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10a90-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="10a90-127">إعداد قيود الترحيل</span><span class="sxs-lookup"><span data-stu-id="10a90-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="10a90-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="10a90-128">Close the page.</span></span>
2. <span data-ttu-id="10a90-129">انقر فوق ‏‏**قيود الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="10a90-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="10a90-130">في الحقل **كيف تريد إعداد قيود الترحيل**، حدد "حسب مجموعة المستخدمين".</span><span class="sxs-lookup"><span data-stu-id="10a90-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="10a90-131">في الشجرة، قم بتحديد خانة الاختيار"المجموعة التي تريد السماح لها بالترحيل لاسم دفتر اليومية هذا."</span><span class="sxs-lookup"><span data-stu-id="10a90-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="10a90-132">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="10a90-132">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]