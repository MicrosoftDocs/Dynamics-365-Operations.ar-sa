---
title: يظل العمل محظورًا
description: يظل العمل محظورًا
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924120"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="75a10-103">يظل العمل محظورًا</span><span class="sxs-lookup"><span data-stu-id="75a10-103">Work remains blocked</span></span>

<span data-ttu-id="75a10-104">رمز الخطأ: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="75a10-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="75a10-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="75a10-105">Symptoms</span></span>

<span data-ttu-id="75a10-106">يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="75a10-106">The system shows the following error message:</span></span>

> <span data-ttu-id="75a10-107">يبقى العمل %1 محظورًا لأن حالة الموجة المرتبطة %2 هي %3.</span><span class="sxs-lookup"><span data-stu-id="75a10-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="75a10-108">السبب</span><span class="sxs-lookup"><span data-stu-id="75a10-108">Cause</span></span>

<span data-ttu-id="75a10-109">تتم معالجة العمل حاليًا على موجة ولا يمكن إلغاء حظره، كما يتضح من أحد الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="75a10-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="75a10-110">في علامة التبويب **أسباب الحظر**، تم تعيين حقل **سبب حظر العمل** لواحد أو أكثر من البنود إلى *موجة المعالجة*.</span><span class="sxs-lookup"><span data-stu-id="75a10-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="75a10-111">عند تحديد **موجة** في مجموعة **المعلومات ذات الصلة** في علامة التبويب **ذات الصلة** في جزء الإجراءات، ويتم تعيين حقل **حالة الموجة** إلى *معالجة*.</span><span class="sxs-lookup"><span data-stu-id="75a10-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="75a10-112">الدقة</span><span class="sxs-lookup"><span data-stu-id="75a10-112">Resolution</span></span>

<span data-ttu-id="75a10-113">في جزء الإجراءات، في علامة التبويب **المعلومات ذات الصلة**، في مجموعة **المعلومات ذات الصلة**، حدد **موجة**.</span><span class="sxs-lookup"><span data-stu-id="75a10-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="75a10-114">وبعد ذلك في صفحة **الموجات**، في جزء الإجراءات، في علامة التبويب **موجة**، في مجموعة **الموجة**، حدد **تنظيف بيانات الموجة**.</span><span class="sxs-lookup"><span data-stu-id="75a10-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="75a10-115">حل بديل</span><span class="sxs-lookup"><span data-stu-id="75a10-115">Workaround</span></span>

<span data-ttu-id="75a10-116">إذا لم تؤد الخطوات السابقة إلى حل المشكلة، فيمكنك إلغاء العمل باتباع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="75a10-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="75a10-117">انتقل إلى **إدارة المستودع \> المهام الدورية \> تنظيف \> إلغاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="75a10-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="75a10-118">في حقل **معرف العمل**، حدد معرف العمل الذي تريد إلغاؤه، والذي يحتوي حاليًا على قيمة **حالة العمل** التي تكون *مفتوح* أو *قيد التقدم* أو *تم الإلغاء* أو *تم التجميع* أو *مغلق*.</span><span class="sxs-lookup"><span data-stu-id="75a10-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="75a10-119">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="75a10-119">Select **OK**.</span></span>
1. <span data-ttu-id="75a10-120">حدد **نعم** لتأكيد رغبتك في إلغاء العمل.</span><span class="sxs-lookup"><span data-stu-id="75a10-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="75a10-121">لمزيد من المعلومات، راجع [إلغاء عمل المستودع لمعالجة الاستثناء](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="75a10-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
