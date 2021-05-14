---
title: لا يمكن إلغاء العمل بسبب حالته
description: لا يمكن إلغاء العمل بسبب حالته
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924245"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="bb900-103">لا يمكن إلغاء العمل بسبب حالته</span><span class="sxs-lookup"><span data-stu-id="bb900-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="bb900-104">رمز الخطأ: WAX2190</span><span class="sxs-lookup"><span data-stu-id="bb900-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="bb900-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="bb900-105">Symptoms</span></span>

<span data-ttu-id="bb900-106">يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="bb900-106">The system shows the following error message:</span></span>

> <span data-ttu-id="bb900-107">لا يمكنك إلغاء العمل %1 لأن حالته %2.</span><span class="sxs-lookup"><span data-stu-id="bb900-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="bb900-108">السبب</span><span class="sxs-lookup"><span data-stu-id="bb900-108">Cause</span></span>

<span data-ttu-id="bb900-109">لا يمكن إلغاء العمل في حالته الحالية.</span><span class="sxs-lookup"><span data-stu-id="bb900-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="bb900-110">لا يحتوي رأس العمل أو بنود العمل على قيمة **حالة العمل** المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="bb900-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="bb900-111">لم يتم تعيين حقل **حالة العمل** في رأس العمل إلى *مفتوح* أو *قيد التقدم*.</span><span class="sxs-lookup"><span data-stu-id="bb900-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="bb900-112">الدقة</span><span class="sxs-lookup"><span data-stu-id="bb900-112">Resolution</span></span>

<span data-ttu-id="bb900-113">لإلغاء العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="bb900-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="bb900-114">انتقل إلى **إدارة المستودع \> المهام الدورية \> تنظيف \> إلغاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="bb900-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="bb900-115">في حقل **معرف العمل**، حدد معرف العمل الذي ترغب في إلغائه.</span><span class="sxs-lookup"><span data-stu-id="bb900-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="bb900-116">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bb900-116">Select **OK**.</span></span>
1. <span data-ttu-id="bb900-117">حدد **نعم** لتأكيد رغبتك في إلغاء العمل.</span><span class="sxs-lookup"><span data-stu-id="bb900-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="bb900-118">لمزيد من المعلومات، راجع [إلغاء عمل المستودع لمعالجة الاستثناء](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="bb900-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
