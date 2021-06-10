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
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054946"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="8ea6c-103">نظره عامة على MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="8ea6c-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8ea6c-104">يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="8ea6c-105">مفتاح</span><span class="sxs-lookup"><span data-stu-id="8ea6c-105">Key</span></span>

  | <span data-ttu-id="8ea6c-106">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="8ea6c-106">Property Name</span></span> | <span data-ttu-id="8ea6c-107">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="8ea6c-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="8ea6c-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8ea6c-108">dataAreaId</span></span>    | <span data-ttu-id="8ea6c-109">سلسلة</span><span class="sxs-lookup"><span data-stu-id="8ea6c-109">String</span></span>    |
  | <span data-ttu-id="8ea6c-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="8ea6c-110">RequestId</span></span>     | <span data-ttu-id="8ea6c-111">سلسلة</span><span class="sxs-lookup"><span data-stu-id="8ea6c-111">String</span></span>    |
  | <span data-ttu-id="8ea6c-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="8ea6c-112">LeaveType</span></span>     | <span data-ttu-id="8ea6c-113">سلسلة</span><span class="sxs-lookup"><span data-stu-id="8ea6c-113">String</span></span>    |
  | <span data-ttu-id="8ea6c-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8ea6c-114">LeaveDate</span></span>     | <span data-ttu-id="8ea6c-115">التاريخ</span><span class="sxs-lookup"><span data-stu-id="8ea6c-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="8ea6c-116">خصائص</span><span class="sxs-lookup"><span data-stu-id="8ea6c-116">Properties</span></span>

  | <span data-ttu-id="8ea6c-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="8ea6c-117">Property Name</span></span>     | <span data-ttu-id="8ea6c-118">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="8ea6c-118">Data Type</span></span> | <span data-ttu-id="8ea6c-119">مطلوب</span><span class="sxs-lookup"><span data-stu-id="8ea6c-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="8ea6c-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8ea6c-120">dataAreaId</span></span>        | <span data-ttu-id="8ea6c-121">سلسلة</span><span class="sxs-lookup"><span data-stu-id="8ea6c-121">String</span></span>    | <span data-ttu-id="8ea6c-122">س</span><span class="sxs-lookup"><span data-stu-id="8ea6c-122">X</span></span>        |
  | <span data-ttu-id="8ea6c-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="8ea6c-123">RequestId</span></span>         | <span data-ttu-id="8ea6c-124">سلسلة</span><span class="sxs-lookup"><span data-stu-id="8ea6c-124">String</span></span>    | <span data-ttu-id="8ea6c-125">س</span><span class="sxs-lookup"><span data-stu-id="8ea6c-125">X</span></span>        |
  | <span data-ttu-id="8ea6c-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="8ea6c-126">LeaveType</span></span>         | <span data-ttu-id="8ea6c-127">سلسلة</span><span class="sxs-lookup"><span data-stu-id="8ea6c-127">String</span></span>    | <span data-ttu-id="8ea6c-128">س</span><span class="sxs-lookup"><span data-stu-id="8ea6c-128">X</span></span>        |
  | <span data-ttu-id="8ea6c-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8ea6c-129">LeaveDate</span></span>         | <span data-ttu-id="8ea6c-130">التاريخ</span><span class="sxs-lookup"><span data-stu-id="8ea6c-130">Date</span></span>      | <span data-ttu-id="8ea6c-131">س</span><span class="sxs-lookup"><span data-stu-id="8ea6c-131">X</span></span>        |
  | <span data-ttu-id="8ea6c-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="8ea6c-132">ReasonCodeId</span></span>      | <span data-ttu-id="8ea6c-133">سلسلة</span><span class="sxs-lookup"><span data-stu-id="8ea6c-133">String</span></span>    |          |
  | <span data-ttu-id="8ea6c-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="8ea6c-134">PersonnelNumber</span></span>   | <span data-ttu-id="8ea6c-135">سلسلة</span><span class="sxs-lookup"><span data-stu-id="8ea6c-135">String</span></span>    | <span data-ttu-id="8ea6c-136">س</span><span class="sxs-lookup"><span data-stu-id="8ea6c-136">X</span></span>        |
  | <span data-ttu-id="8ea6c-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="8ea6c-137">RequestDate</span></span>       | <span data-ttu-id="8ea6c-138">التاريخ</span><span class="sxs-lookup"><span data-stu-id="8ea6c-138">Date</span></span>      | <span data-ttu-id="8ea6c-139">س</span><span class="sxs-lookup"><span data-stu-id="8ea6c-139">X</span></span>        |
  | <span data-ttu-id="8ea6c-140">تعليق</span><span class="sxs-lookup"><span data-stu-id="8ea6c-140">Comment</span></span>           | <span data-ttu-id="8ea6c-141">سلسلة</span><span class="sxs-lookup"><span data-stu-id="8ea6c-141">String</span></span>    |          |
  | <span data-ttu-id="8ea6c-142">الحالة</span><span class="sxs-lookup"><span data-stu-id="8ea6c-142">Status</span></span>            | <span data-ttu-id="8ea6c-143">تعداد</span><span class="sxs-lookup"><span data-stu-id="8ea6c-143">Enum</span></span>      | <span data-ttu-id="8ea6c-144">س</span><span class="sxs-lookup"><span data-stu-id="8ea6c-144">X</span></span>        |
  | <span data-ttu-id="8ea6c-145">‏‏المقدار</span><span class="sxs-lookup"><span data-stu-id="8ea6c-145">Amount</span></span>            | <span data-ttu-id="8ea6c-146">حقيقي</span><span class="sxs-lookup"><span data-stu-id="8ea6c-146">Real</span></span>      |          |
  | <span data-ttu-id="8ea6c-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="8ea6c-147">HalfDayDefinition</span></span> | <span data-ttu-id="8ea6c-148">تعداد</span><span class="sxs-lookup"><span data-stu-id="8ea6c-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="8ea6c-149">إجراءات</span><span class="sxs-lookup"><span data-stu-id="8ea6c-149">Actions</span></span>

 | <span data-ttu-id="8ea6c-150">اسم الإجراء</span><span class="sxs-lookup"><span data-stu-id="8ea6c-150">Action Name</span></span>                               | <span data-ttu-id="8ea6c-151">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="8ea6c-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="8ea6c-152">إرسال</span><span class="sxs-lookup"><span data-stu-id="8ea6c-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="8ea6c-153">أرسل الطلب لمعالجته من خلال سير العمل.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8ea6c-154">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="8ea6c-154">See also</span></span>

- [<span data-ttu-id="8ea6c-155">إرسال طلب إجازة إلى سير العمل</span><span class="sxs-lookup"><span data-stu-id="8ea6c-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="8ea6c-156">المصادقة</span><span class="sxs-lookup"><span data-stu-id="8ea6c-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]