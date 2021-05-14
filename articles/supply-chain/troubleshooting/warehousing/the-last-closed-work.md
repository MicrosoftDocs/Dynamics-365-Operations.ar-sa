---
title: آخر بند عمل مقفل يجب أن يكون "وضع"
description: آخر بند عمل مقفل يجب أن يكون "وضع"
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
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924365"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="b527a-103">آخر بند عمل مقفل يجب أن يكون "وضع"</span><span class="sxs-lookup"><span data-stu-id="b527a-103">The last closed work line must be a put</span></span>

<span data-ttu-id="b527a-104">رمز الخطأ: WAX1285</span><span class="sxs-lookup"><span data-stu-id="b527a-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="b527a-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="b527a-105">Symptoms</span></span>

<span data-ttu-id="b527a-106">يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="b527a-106">The system shows the following error message:</span></span>

> <span data-ttu-id="b527a-107">آخر بند عمل مقفل يجب أن يكون "وضع".</span><span class="sxs-lookup"><span data-stu-id="b527a-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="b527a-108">السبب</span><span class="sxs-lookup"><span data-stu-id="b527a-108">Cause</span></span>

<span data-ttu-id="b527a-109">لا يمكن إلغاء العمل في حالته الحالية.</span><span class="sxs-lookup"><span data-stu-id="b527a-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="b527a-110">في بند العمل الأخير، تم تعيين حقل **حالة العمل** إلى *مقفل*، ولكن لم يتم تعيين **نوع العمل** إلى *وضع*.</span><span class="sxs-lookup"><span data-stu-id="b527a-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="b527a-111">الدقة</span><span class="sxs-lookup"><span data-stu-id="b527a-111">Resolution</span></span>

<span data-ttu-id="b527a-112">لإلغاء العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b527a-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="b527a-113">انتقل إلى **إدارة المستودع \> المهام الدورية \> تنظيف \> إلغاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="b527a-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="b527a-114">في حقل **معرف العمل**، حدد معرف العمل الذي ترغب في إلغائه.</span><span class="sxs-lookup"><span data-stu-id="b527a-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="b527a-115">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b527a-115">Select **OK**.</span></span>
1. <span data-ttu-id="b527a-116">حدد **نعم** لتأكيد رغبتك في إلغاء العمل.</span><span class="sxs-lookup"><span data-stu-id="b527a-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="b527a-117">لمزيد من المعلومات، راجع [إلغاء عمل المستودع لمعالجة الاستثناء](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="b527a-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
