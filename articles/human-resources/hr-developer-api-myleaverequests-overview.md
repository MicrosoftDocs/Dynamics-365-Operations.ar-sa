---
title: نظره عامة على MyLeaveRequests
description: يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417041"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="3e986-103">نظره عامة على MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="3e986-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="3e986-104">يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.</span><span class="sxs-lookup"><span data-stu-id="3e986-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="3e986-105">مفتاح</span><span class="sxs-lookup"><span data-stu-id="3e986-105">Key</span></span>

  | <span data-ttu-id="3e986-106">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="3e986-106">Property Name</span></span> | <span data-ttu-id="3e986-107">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="3e986-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="3e986-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="3e986-108">dataAreaId</span></span>    | <span data-ttu-id="3e986-109">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3e986-109">String</span></span>    |
  | <span data-ttu-id="3e986-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="3e986-110">RequestId</span></span>     | <span data-ttu-id="3e986-111">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3e986-111">String</span></span>    |
  | <span data-ttu-id="3e986-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="3e986-112">LeaveType</span></span>     | <span data-ttu-id="3e986-113">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3e986-113">String</span></span>    |
  | <span data-ttu-id="3e986-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="3e986-114">LeaveDate</span></span>     | <span data-ttu-id="3e986-115">التاريخ</span><span class="sxs-lookup"><span data-stu-id="3e986-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="3e986-116">خصائص</span><span class="sxs-lookup"><span data-stu-id="3e986-116">Properties</span></span>

  | <span data-ttu-id="3e986-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="3e986-117">Property Name</span></span>     | <span data-ttu-id="3e986-118">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="3e986-118">Data Type</span></span> | <span data-ttu-id="3e986-119">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3e986-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="3e986-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="3e986-120">dataAreaId</span></span>        | <span data-ttu-id="3e986-121">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3e986-121">String</span></span>    | <span data-ttu-id="3e986-122">س</span><span class="sxs-lookup"><span data-stu-id="3e986-122">X</span></span>        |
  | <span data-ttu-id="3e986-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="3e986-123">RequestId</span></span>         | <span data-ttu-id="3e986-124">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3e986-124">String</span></span>    | <span data-ttu-id="3e986-125">س</span><span class="sxs-lookup"><span data-stu-id="3e986-125">X</span></span>        |
  | <span data-ttu-id="3e986-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="3e986-126">LeaveType</span></span>         | <span data-ttu-id="3e986-127">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3e986-127">String</span></span>    | <span data-ttu-id="3e986-128">س</span><span class="sxs-lookup"><span data-stu-id="3e986-128">X</span></span>        |
  | <span data-ttu-id="3e986-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="3e986-129">LeaveDate</span></span>         | <span data-ttu-id="3e986-130">التاريخ</span><span class="sxs-lookup"><span data-stu-id="3e986-130">Date</span></span>      | <span data-ttu-id="3e986-131">س</span><span class="sxs-lookup"><span data-stu-id="3e986-131">X</span></span>        |
  | <span data-ttu-id="3e986-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="3e986-132">ReasonCodeId</span></span>      | <span data-ttu-id="3e986-133">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3e986-133">String</span></span>    |          |
  | <span data-ttu-id="3e986-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="3e986-134">PersonnelNumber</span></span>   | <span data-ttu-id="3e986-135">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3e986-135">String</span></span>    | <span data-ttu-id="3e986-136">س</span><span class="sxs-lookup"><span data-stu-id="3e986-136">X</span></span>        |
  | <span data-ttu-id="3e986-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="3e986-137">RequestDate</span></span>       | <span data-ttu-id="3e986-138">التاريخ</span><span class="sxs-lookup"><span data-stu-id="3e986-138">Date</span></span>      | <span data-ttu-id="3e986-139">س</span><span class="sxs-lookup"><span data-stu-id="3e986-139">X</span></span>        |
  | <span data-ttu-id="3e986-140">تعليق</span><span class="sxs-lookup"><span data-stu-id="3e986-140">Comment</span></span>           | <span data-ttu-id="3e986-141">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3e986-141">String</span></span>    |          |
  | <span data-ttu-id="3e986-142">الحالة</span><span class="sxs-lookup"><span data-stu-id="3e986-142">Status</span></span>            | <span data-ttu-id="3e986-143">تعداد</span><span class="sxs-lookup"><span data-stu-id="3e986-143">Enum</span></span>      | <span data-ttu-id="3e986-144">س</span><span class="sxs-lookup"><span data-stu-id="3e986-144">X</span></span>        |
  | <span data-ttu-id="3e986-145">‏‏المقدار</span><span class="sxs-lookup"><span data-stu-id="3e986-145">Amount</span></span>            | <span data-ttu-id="3e986-146">حقيقي</span><span class="sxs-lookup"><span data-stu-id="3e986-146">Real</span></span>      |          |
  | <span data-ttu-id="3e986-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="3e986-147">HalfDayDefinition</span></span> | <span data-ttu-id="3e986-148">تعداد</span><span class="sxs-lookup"><span data-stu-id="3e986-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="3e986-149">إجراءات</span><span class="sxs-lookup"><span data-stu-id="3e986-149">Actions</span></span>

 | <span data-ttu-id="3e986-150">اسم الإجراء</span><span class="sxs-lookup"><span data-stu-id="3e986-150">Action Name</span></span>                               | <span data-ttu-id="3e986-151">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="3e986-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="3e986-152">إرسال</span><span class="sxs-lookup"><span data-stu-id="3e986-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="3e986-153">أرسل الطلب لمعالجته من خلال سير العمل.</span><span class="sxs-lookup"><span data-stu-id="3e986-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3e986-154">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="3e986-154">See also</span></span>

- [<span data-ttu-id="3e986-155">إرسال طلب إجازة إلى سير العمل</span><span class="sxs-lookup"><span data-stu-id="3e986-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="3e986-156">المصادقة</span><span class="sxs-lookup"><span data-stu-id="3e986-156">Authentication</span></span>](hr-developer-api-authentication.md)