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
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092027"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="f9b13-103">نظره عامة على MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="f9b13-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="f9b13-104">يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.</span><span class="sxs-lookup"><span data-stu-id="f9b13-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="f9b13-105">مفتاح</span><span class="sxs-lookup"><span data-stu-id="f9b13-105">Key</span></span>

  | <span data-ttu-id="f9b13-106">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="f9b13-106">Property Name</span></span> | <span data-ttu-id="f9b13-107">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="f9b13-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="f9b13-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="f9b13-108">dataAreaId</span></span>    | <span data-ttu-id="f9b13-109">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f9b13-109">String</span></span>    |
  | <span data-ttu-id="f9b13-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="f9b13-110">RequestId</span></span>     | <span data-ttu-id="f9b13-111">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f9b13-111">String</span></span>    |
  | <span data-ttu-id="f9b13-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="f9b13-112">LeaveType</span></span>     | <span data-ttu-id="f9b13-113">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f9b13-113">String</span></span>    |
  | <span data-ttu-id="f9b13-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="f9b13-114">LeaveDate</span></span>     | <span data-ttu-id="f9b13-115">التاريخ</span><span class="sxs-lookup"><span data-stu-id="f9b13-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="f9b13-116">خصائص</span><span class="sxs-lookup"><span data-stu-id="f9b13-116">Properties</span></span>

  | <span data-ttu-id="f9b13-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="f9b13-117">Property Name</span></span>     | <span data-ttu-id="f9b13-118">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="f9b13-118">Data Type</span></span> | <span data-ttu-id="f9b13-119">مطلوب</span><span class="sxs-lookup"><span data-stu-id="f9b13-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="f9b13-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="f9b13-120">dataAreaId</span></span>        | <span data-ttu-id="f9b13-121">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f9b13-121">String</span></span>    | <span data-ttu-id="f9b13-122">س</span><span class="sxs-lookup"><span data-stu-id="f9b13-122">X</span></span>        |
  | <span data-ttu-id="f9b13-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="f9b13-123">RequestId</span></span>         | <span data-ttu-id="f9b13-124">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f9b13-124">String</span></span>    | <span data-ttu-id="f9b13-125">س</span><span class="sxs-lookup"><span data-stu-id="f9b13-125">X</span></span>        |
  | <span data-ttu-id="f9b13-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="f9b13-126">LeaveType</span></span>         | <span data-ttu-id="f9b13-127">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f9b13-127">String</span></span>    | <span data-ttu-id="f9b13-128">س</span><span class="sxs-lookup"><span data-stu-id="f9b13-128">X</span></span>        |
  | <span data-ttu-id="f9b13-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="f9b13-129">LeaveDate</span></span>         | <span data-ttu-id="f9b13-130">التاريخ</span><span class="sxs-lookup"><span data-stu-id="f9b13-130">Date</span></span>      | <span data-ttu-id="f9b13-131">س</span><span class="sxs-lookup"><span data-stu-id="f9b13-131">X</span></span>        |
  | <span data-ttu-id="f9b13-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="f9b13-132">ReasonCodeId</span></span>      | <span data-ttu-id="f9b13-133">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f9b13-133">String</span></span>    |          |
  | <span data-ttu-id="f9b13-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="f9b13-134">PersonnelNumber</span></span>   | <span data-ttu-id="f9b13-135">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f9b13-135">String</span></span>    | <span data-ttu-id="f9b13-136">س</span><span class="sxs-lookup"><span data-stu-id="f9b13-136">X</span></span>        |
  | <span data-ttu-id="f9b13-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="f9b13-137">RequestDate</span></span>       | <span data-ttu-id="f9b13-138">التاريخ</span><span class="sxs-lookup"><span data-stu-id="f9b13-138">Date</span></span>      | <span data-ttu-id="f9b13-139">س</span><span class="sxs-lookup"><span data-stu-id="f9b13-139">X</span></span>        |
  | <span data-ttu-id="f9b13-140">تعليق</span><span class="sxs-lookup"><span data-stu-id="f9b13-140">Comment</span></span>           | <span data-ttu-id="f9b13-141">سلسلة</span><span class="sxs-lookup"><span data-stu-id="f9b13-141">String</span></span>    |          |
  | <span data-ttu-id="f9b13-142">الحالة</span><span class="sxs-lookup"><span data-stu-id="f9b13-142">Status</span></span>            | <span data-ttu-id="f9b13-143">تعداد</span><span class="sxs-lookup"><span data-stu-id="f9b13-143">Enum</span></span>      | <span data-ttu-id="f9b13-144">س</span><span class="sxs-lookup"><span data-stu-id="f9b13-144">X</span></span>        |
  | <span data-ttu-id="f9b13-145">‏‏المقدار</span><span class="sxs-lookup"><span data-stu-id="f9b13-145">Amount</span></span>            | <span data-ttu-id="f9b13-146">حقيقي</span><span class="sxs-lookup"><span data-stu-id="f9b13-146">Real</span></span>      |          |
  | <span data-ttu-id="f9b13-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="f9b13-147">HalfDayDefinition</span></span> | <span data-ttu-id="f9b13-148">تعداد</span><span class="sxs-lookup"><span data-stu-id="f9b13-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="f9b13-149">إجراءات</span><span class="sxs-lookup"><span data-stu-id="f9b13-149">Actions</span></span>

 | <span data-ttu-id="f9b13-150">اسم الإجراء</span><span class="sxs-lookup"><span data-stu-id="f9b13-150">Action Name</span></span>                               | <span data-ttu-id="f9b13-151">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="f9b13-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="f9b13-152">إرسال</span><span class="sxs-lookup"><span data-stu-id="f9b13-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="f9b13-153">أرسل الطلب لمعالجته من خلال سير العمل.</span><span class="sxs-lookup"><span data-stu-id="f9b13-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f9b13-154">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="f9b13-154">See also</span></span>

- [<span data-ttu-id="f9b13-155">إرسال طلب إجازة إلى سير العمل</span><span class="sxs-lookup"><span data-stu-id="f9b13-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="f9b13-156">المصادقة</span><span class="sxs-lookup"><span data-stu-id="f9b13-156">Authentication</span></span>](hr-developer-api-authentication.md)