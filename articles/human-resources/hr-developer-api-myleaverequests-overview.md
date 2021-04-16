---
title: نظره عامة على MyLeaveRequests
description: يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803623"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="f50c0-103">نظره عامة على MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="f50c0-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f50c0-104">يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.</span><span class="sxs-lookup"><span data-stu-id="f50c0-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="f50c0-105">مفتاح</span><span class="sxs-lookup"><span data-stu-id="f50c0-105">Key</span></span>

  | <span data-ttu-id="f50c0-106">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="f50c0-106">Property Name</span></span> | <span data-ttu-id="f50c0-107">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="f50c0-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="f50c0-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="f50c0-108">dataAreaId</span></span>    | <span data-ttu-id="f50c0-109">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f50c0-109">String</span></span>    |
  | <span data-ttu-id="f50c0-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="f50c0-110">RequestId</span></span>     | <span data-ttu-id="f50c0-111">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f50c0-111">String</span></span>    |
  | <span data-ttu-id="f50c0-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="f50c0-112">LeaveType</span></span>     | <span data-ttu-id="f50c0-113">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f50c0-113">String</span></span>    |
  | <span data-ttu-id="f50c0-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="f50c0-114">LeaveDate</span></span>     | <span data-ttu-id="f50c0-115">التاريخ</span><span class="sxs-lookup"><span data-stu-id="f50c0-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="f50c0-116">خصائص</span><span class="sxs-lookup"><span data-stu-id="f50c0-116">Properties</span></span>

  | <span data-ttu-id="f50c0-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="f50c0-117">Property Name</span></span>     | <span data-ttu-id="f50c0-118">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="f50c0-118">Data Type</span></span> | <span data-ttu-id="f50c0-119">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f50c0-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="f50c0-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="f50c0-120">dataAreaId</span></span>        | <span data-ttu-id="f50c0-121">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f50c0-121">String</span></span>    | <span data-ttu-id="f50c0-122">س</span><span class="sxs-lookup"><span data-stu-id="f50c0-122">X</span></span>        |
  | <span data-ttu-id="f50c0-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="f50c0-123">RequestId</span></span>         | <span data-ttu-id="f50c0-124">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f50c0-124">String</span></span>    | <span data-ttu-id="f50c0-125">س</span><span class="sxs-lookup"><span data-stu-id="f50c0-125">X</span></span>        |
  | <span data-ttu-id="f50c0-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="f50c0-126">LeaveType</span></span>         | <span data-ttu-id="f50c0-127">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f50c0-127">String</span></span>    | <span data-ttu-id="f50c0-128">س</span><span class="sxs-lookup"><span data-stu-id="f50c0-128">X</span></span>        |
  | <span data-ttu-id="f50c0-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="f50c0-129">LeaveDate</span></span>         | <span data-ttu-id="f50c0-130">التاريخ</span><span class="sxs-lookup"><span data-stu-id="f50c0-130">Date</span></span>      | <span data-ttu-id="f50c0-131">س</span><span class="sxs-lookup"><span data-stu-id="f50c0-131">X</span></span>        |
  | <span data-ttu-id="f50c0-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="f50c0-132">ReasonCodeId</span></span>      | <span data-ttu-id="f50c0-133">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f50c0-133">String</span></span>    |          |
  | <span data-ttu-id="f50c0-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="f50c0-134">PersonnelNumber</span></span>   | <span data-ttu-id="f50c0-135">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f50c0-135">String</span></span>    | <span data-ttu-id="f50c0-136">س</span><span class="sxs-lookup"><span data-stu-id="f50c0-136">X</span></span>        |
  | <span data-ttu-id="f50c0-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="f50c0-137">RequestDate</span></span>       | <span data-ttu-id="f50c0-138">التاريخ</span><span class="sxs-lookup"><span data-stu-id="f50c0-138">Date</span></span>      | <span data-ttu-id="f50c0-139">س</span><span class="sxs-lookup"><span data-stu-id="f50c0-139">X</span></span>        |
  | <span data-ttu-id="f50c0-140">تعليق</span><span class="sxs-lookup"><span data-stu-id="f50c0-140">Comment</span></span>           | <span data-ttu-id="f50c0-141">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f50c0-141">String</span></span>    |          |
  | <span data-ttu-id="f50c0-142">الحالة</span><span class="sxs-lookup"><span data-stu-id="f50c0-142">Status</span></span>            | <span data-ttu-id="f50c0-143">تعداد</span><span class="sxs-lookup"><span data-stu-id="f50c0-143">Enum</span></span>      | <span data-ttu-id="f50c0-144">س</span><span class="sxs-lookup"><span data-stu-id="f50c0-144">X</span></span>        |
  | <span data-ttu-id="f50c0-145">‏‏المقدار</span><span class="sxs-lookup"><span data-stu-id="f50c0-145">Amount</span></span>            | <span data-ttu-id="f50c0-146">حقيقي</span><span class="sxs-lookup"><span data-stu-id="f50c0-146">Real</span></span>      |          |
  | <span data-ttu-id="f50c0-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="f50c0-147">HalfDayDefinition</span></span> | <span data-ttu-id="f50c0-148">تعداد</span><span class="sxs-lookup"><span data-stu-id="f50c0-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="f50c0-149">إجراءات</span><span class="sxs-lookup"><span data-stu-id="f50c0-149">Actions</span></span>

 | <span data-ttu-id="f50c0-150">اسم الإجراء</span><span class="sxs-lookup"><span data-stu-id="f50c0-150">Action Name</span></span>                               | <span data-ttu-id="f50c0-151">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="f50c0-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="f50c0-152">إرسال</span><span class="sxs-lookup"><span data-stu-id="f50c0-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="f50c0-153">أرسل الطلب لمعالجته من خلال سير العمل.</span><span class="sxs-lookup"><span data-stu-id="f50c0-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f50c0-154">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="f50c0-154">See also</span></span>

- [<span data-ttu-id="f50c0-155">إرسال طلب إجازة إلى سير العمل</span><span class="sxs-lookup"><span data-stu-id="f50c0-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="f50c0-156">المصادقة</span><span class="sxs-lookup"><span data-stu-id="f50c0-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]