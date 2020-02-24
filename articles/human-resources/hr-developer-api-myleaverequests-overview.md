---
title: نظره عامة على MyLeaveRequests
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007955"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="17761-102">نظره عامة على MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="17761-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="17761-103">يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.</span><span class="sxs-lookup"><span data-stu-id="17761-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="17761-104">مفتاح</span><span class="sxs-lookup"><span data-stu-id="17761-104">Key</span></span>

  | <span data-ttu-id="17761-105">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="17761-105">Property Name</span></span> | <span data-ttu-id="17761-106">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="17761-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="17761-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="17761-107">dataAreaId</span></span>    | <span data-ttu-id="17761-108">سلسلة</span><span class="sxs-lookup"><span data-stu-id="17761-108">String</span></span>    |
  | <span data-ttu-id="17761-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="17761-109">RequestId</span></span>     | <span data-ttu-id="17761-110">سلسلة</span><span class="sxs-lookup"><span data-stu-id="17761-110">String</span></span>    |
  | <span data-ttu-id="17761-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="17761-111">LeaveType</span></span>     | <span data-ttu-id="17761-112">سلسلة</span><span class="sxs-lookup"><span data-stu-id="17761-112">String</span></span>    |
  | <span data-ttu-id="17761-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="17761-113">LeaveDate</span></span>     | <span data-ttu-id="17761-114">التاريخ</span><span class="sxs-lookup"><span data-stu-id="17761-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="17761-115">خصائص</span><span class="sxs-lookup"><span data-stu-id="17761-115">Properties</span></span>

  | <span data-ttu-id="17761-116">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="17761-116">Property Name</span></span>     | <span data-ttu-id="17761-117">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="17761-117">Data Type</span></span> | <span data-ttu-id="17761-118">مطلوب</span><span class="sxs-lookup"><span data-stu-id="17761-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="17761-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="17761-119">dataAreaId</span></span>        | <span data-ttu-id="17761-120">سلسلة</span><span class="sxs-lookup"><span data-stu-id="17761-120">String</span></span>    | <span data-ttu-id="17761-121">س</span><span class="sxs-lookup"><span data-stu-id="17761-121">X</span></span>        |
  | <span data-ttu-id="17761-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="17761-122">RequestId</span></span>         | <span data-ttu-id="17761-123">سلسلة</span><span class="sxs-lookup"><span data-stu-id="17761-123">String</span></span>    | <span data-ttu-id="17761-124">س</span><span class="sxs-lookup"><span data-stu-id="17761-124">X</span></span>        |
  | <span data-ttu-id="17761-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="17761-125">LeaveType</span></span>         | <span data-ttu-id="17761-126">سلسلة</span><span class="sxs-lookup"><span data-stu-id="17761-126">String</span></span>    | <span data-ttu-id="17761-127">س</span><span class="sxs-lookup"><span data-stu-id="17761-127">X</span></span>        |
  | <span data-ttu-id="17761-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="17761-128">LeaveDate</span></span>         | <span data-ttu-id="17761-129">التاريخ</span><span class="sxs-lookup"><span data-stu-id="17761-129">Date</span></span>      | <span data-ttu-id="17761-130">س</span><span class="sxs-lookup"><span data-stu-id="17761-130">X</span></span>        |
  | <span data-ttu-id="17761-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="17761-131">ReasonCodeId</span></span>      | <span data-ttu-id="17761-132">سلسلة</span><span class="sxs-lookup"><span data-stu-id="17761-132">String</span></span>    |          |
  | <span data-ttu-id="17761-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="17761-133">PersonnelNumber</span></span>   | <span data-ttu-id="17761-134">سلسلة</span><span class="sxs-lookup"><span data-stu-id="17761-134">String</span></span>    | <span data-ttu-id="17761-135">س</span><span class="sxs-lookup"><span data-stu-id="17761-135">X</span></span>        |
  | <span data-ttu-id="17761-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="17761-136">RequestDate</span></span>       | <span data-ttu-id="17761-137">التاريخ</span><span class="sxs-lookup"><span data-stu-id="17761-137">Date</span></span>      | <span data-ttu-id="17761-138">س</span><span class="sxs-lookup"><span data-stu-id="17761-138">X</span></span>        |
  | <span data-ttu-id="17761-139">تعليق</span><span class="sxs-lookup"><span data-stu-id="17761-139">Comment</span></span>           | <span data-ttu-id="17761-140">سلسلة</span><span class="sxs-lookup"><span data-stu-id="17761-140">String</span></span>    |          |
  | <span data-ttu-id="17761-141">الحالة</span><span class="sxs-lookup"><span data-stu-id="17761-141">Status</span></span>            | <span data-ttu-id="17761-142">تعداد</span><span class="sxs-lookup"><span data-stu-id="17761-142">Enum</span></span>      | <span data-ttu-id="17761-143">س</span><span class="sxs-lookup"><span data-stu-id="17761-143">X</span></span>        |
  | <span data-ttu-id="17761-144">‏‏المقدار</span><span class="sxs-lookup"><span data-stu-id="17761-144">Amount</span></span>            | <span data-ttu-id="17761-145">حقيقي</span><span class="sxs-lookup"><span data-stu-id="17761-145">Real</span></span>      |          |
  | <span data-ttu-id="17761-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="17761-146">HalfDayDefinition</span></span> | <span data-ttu-id="17761-147">تعداد</span><span class="sxs-lookup"><span data-stu-id="17761-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="17761-148">إجراءات</span><span class="sxs-lookup"><span data-stu-id="17761-148">Actions</span></span>

 | <span data-ttu-id="17761-149">اسم الإجراء</span><span class="sxs-lookup"><span data-stu-id="17761-149">Action Name</span></span>                               | <span data-ttu-id="17761-150">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="17761-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="17761-151">إرسال</span><span class="sxs-lookup"><span data-stu-id="17761-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="17761-152">أرسل الطلب لمعالجته من خلال سير العمل.</span><span class="sxs-lookup"><span data-stu-id="17761-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="17761-153">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="17761-153">See also</span></span>

- [<span data-ttu-id="17761-154">إرسال طلب إجازة إلى سير العمل</span><span class="sxs-lookup"><span data-stu-id="17761-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="17761-155">المصادقة</span><span class="sxs-lookup"><span data-stu-id="17761-155">Authentication</span></span>](hr-developer-api-authentication.md)