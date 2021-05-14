---
title: لا يمكن إلغاء العمل لأنه محظور
description: لا يمكن إلغاء العمل لأنه محظور
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924269"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="e949f-103">لا يمكن إلغاء العمل لأنه محظور</span><span class="sxs-lookup"><span data-stu-id="e949f-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="e949f-104">رمز الخطأ: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="e949f-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="e949f-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="e949f-105">Symptoms</span></span>

<span data-ttu-id="e949f-106">يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="e949f-106">The system shows the following error message:</span></span>

> <span data-ttu-id="e949f-107">لا يمكن إلغاء العمل %1 لأنه محظور وفقًا لنوع السبب %2.</span><span class="sxs-lookup"><span data-stu-id="e949f-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="e949f-108">يجب إلغاء حظر العمل قبل أن يتم إلغاؤه.</span><span class="sxs-lookup"><span data-stu-id="e949f-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="e949f-109">السبب</span><span class="sxs-lookup"><span data-stu-id="e949f-109">Cause</span></span>

<span data-ttu-id="e949f-110">العمل محظور ولا يمكن إلغاؤه.</span><span class="sxs-lookup"><span data-stu-id="e949f-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="e949f-111">في صفحة **العمل**، في علامة التبويب **عام**، تم تعيين خيار **محظور** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="e949f-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="e949f-112">يشير هذا الإعداد إلى أن العمل محظور.</span><span class="sxs-lookup"><span data-stu-id="e949f-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="e949f-113">تعرض علامة التبويب **أسباب الحظر** سبب حظر العمل.</span><span class="sxs-lookup"><span data-stu-id="e949f-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="e949f-114">الدقة</span><span class="sxs-lookup"><span data-stu-id="e949f-114">Resolution</span></span>

<span data-ttu-id="e949f-115">لإلغاء حظر العمل، حدد علامة التبويب **أسباب الحظر**، ثم اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="e949f-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="e949f-116">في حالة تعيين حقل **سبب حظر العمل** إلى *سبب غير محدد*: في جزء الإجراءات، في علامة التبويب **العمل**، في مجموعة **العمل**، حدد **إلغاء حظر العمل**.</span><span class="sxs-lookup"><span data-stu-id="e949f-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="e949f-117">في حالة تعيين حقل **سبب حظر العمل** إلى *معالجة الموجة*: في جزء الإجراءات، في علامة التبويب **المعلومات ذات الصلة**، في مجموعة **المعلومات ذات الصلة**، حدد **الموجة**.</span><span class="sxs-lookup"><span data-stu-id="e949f-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="e949f-118">وبعد ذلك في صفحة **الموجات**، في جزء الإجراءات، في علامة التبويب **موجة**، في مجموعة **الموجة**، حدد **تنظيف بيانات الموجة**.</span><span class="sxs-lookup"><span data-stu-id="e949f-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="e949f-119">حل بديل</span><span class="sxs-lookup"><span data-stu-id="e949f-119">Workaround</span></span>

<span data-ttu-id="e949f-120">إذا لم تؤد الخطوات السابقة إلى حل المشكلة، فيمكنك إلغاء العمل باتباع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e949f-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="e949f-121">انتقل إلى **إدارة المستودع \> المهام الدورية \> تنظيف \> إلغاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="e949f-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="e949f-122">في حقل **معرف العمل**، حدد معرف العمل الذي تريد إلغاؤه، والذي يحتوي حاليًا على قيمة **حالة العمل** التي تكون *مفتوح* أو *قيد التقدم* أو *تم الإلغاء* أو *تم التجميع* أو *مغلق*.</span><span class="sxs-lookup"><span data-stu-id="e949f-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="e949f-123">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e949f-123">Select **OK**.</span></span>
1. <span data-ttu-id="e949f-124">حدد **نعم** لتأكيد رغبتك في إلغاء العمل.</span><span class="sxs-lookup"><span data-stu-id="e949f-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="e949f-125">لمزيد من المعلومات، راجع [إلغاء عمل المستودع لمعالجة الاستثناء](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="e949f-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
