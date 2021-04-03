---
title: نظره عامة على MyLeaveRequests
description: يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465500"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="3c62a-103">نظره عامة على MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="3c62a-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3c62a-104">يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.</span><span class="sxs-lookup"><span data-stu-id="3c62a-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="3c62a-105">مفتاح</span><span class="sxs-lookup"><span data-stu-id="3c62a-105">Key</span></span>

  | <span data-ttu-id="3c62a-106">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="3c62a-106">Property Name</span></span> | <span data-ttu-id="3c62a-107">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="3c62a-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="3c62a-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="3c62a-108">dataAreaId</span></span>    | <span data-ttu-id="3c62a-109">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3c62a-109">String</span></span>    |
  | <span data-ttu-id="3c62a-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="3c62a-110">RequestId</span></span>     | <span data-ttu-id="3c62a-111">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3c62a-111">String</span></span>    |
  | <span data-ttu-id="3c62a-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="3c62a-112">LeaveType</span></span>     | <span data-ttu-id="3c62a-113">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3c62a-113">String</span></span>    |
  | <span data-ttu-id="3c62a-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="3c62a-114">LeaveDate</span></span>     | <span data-ttu-id="3c62a-115">التاريخ</span><span class="sxs-lookup"><span data-stu-id="3c62a-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="3c62a-116">خصائص</span><span class="sxs-lookup"><span data-stu-id="3c62a-116">Properties</span></span>

  | <span data-ttu-id="3c62a-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="3c62a-117">Property Name</span></span>     | <span data-ttu-id="3c62a-118">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="3c62a-118">Data Type</span></span> | <span data-ttu-id="3c62a-119">مطلوب</span><span class="sxs-lookup"><span data-stu-id="3c62a-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="3c62a-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="3c62a-120">dataAreaId</span></span>        | <span data-ttu-id="3c62a-121">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3c62a-121">String</span></span>    | <span data-ttu-id="3c62a-122">س</span><span class="sxs-lookup"><span data-stu-id="3c62a-122">X</span></span>        |
  | <span data-ttu-id="3c62a-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="3c62a-123">RequestId</span></span>         | <span data-ttu-id="3c62a-124">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3c62a-124">String</span></span>    | <span data-ttu-id="3c62a-125">س</span><span class="sxs-lookup"><span data-stu-id="3c62a-125">X</span></span>        |
  | <span data-ttu-id="3c62a-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="3c62a-126">LeaveType</span></span>         | <span data-ttu-id="3c62a-127">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3c62a-127">String</span></span>    | <span data-ttu-id="3c62a-128">س</span><span class="sxs-lookup"><span data-stu-id="3c62a-128">X</span></span>        |
  | <span data-ttu-id="3c62a-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="3c62a-129">LeaveDate</span></span>         | <span data-ttu-id="3c62a-130">التاريخ</span><span class="sxs-lookup"><span data-stu-id="3c62a-130">Date</span></span>      | <span data-ttu-id="3c62a-131">س</span><span class="sxs-lookup"><span data-stu-id="3c62a-131">X</span></span>        |
  | <span data-ttu-id="3c62a-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="3c62a-132">ReasonCodeId</span></span>      | <span data-ttu-id="3c62a-133">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3c62a-133">String</span></span>    |          |
  | <span data-ttu-id="3c62a-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="3c62a-134">PersonnelNumber</span></span>   | <span data-ttu-id="3c62a-135">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3c62a-135">String</span></span>    | <span data-ttu-id="3c62a-136">س</span><span class="sxs-lookup"><span data-stu-id="3c62a-136">X</span></span>        |
  | <span data-ttu-id="3c62a-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="3c62a-137">RequestDate</span></span>       | <span data-ttu-id="3c62a-138">التاريخ</span><span class="sxs-lookup"><span data-stu-id="3c62a-138">Date</span></span>      | <span data-ttu-id="3c62a-139">س</span><span class="sxs-lookup"><span data-stu-id="3c62a-139">X</span></span>        |
  | <span data-ttu-id="3c62a-140">تعليق</span><span class="sxs-lookup"><span data-stu-id="3c62a-140">Comment</span></span>           | <span data-ttu-id="3c62a-141">سلسلة</span><span class="sxs-lookup"><span data-stu-id="3c62a-141">String</span></span>    |          |
  | <span data-ttu-id="3c62a-142">الحالة</span><span class="sxs-lookup"><span data-stu-id="3c62a-142">Status</span></span>            | <span data-ttu-id="3c62a-143">تعداد</span><span class="sxs-lookup"><span data-stu-id="3c62a-143">Enum</span></span>      | <span data-ttu-id="3c62a-144">س</span><span class="sxs-lookup"><span data-stu-id="3c62a-144">X</span></span>        |
  | <span data-ttu-id="3c62a-145">‏‏المقدار</span><span class="sxs-lookup"><span data-stu-id="3c62a-145">Amount</span></span>            | <span data-ttu-id="3c62a-146">حقيقي</span><span class="sxs-lookup"><span data-stu-id="3c62a-146">Real</span></span>      |          |
  | <span data-ttu-id="3c62a-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="3c62a-147">HalfDayDefinition</span></span> | <span data-ttu-id="3c62a-148">تعداد</span><span class="sxs-lookup"><span data-stu-id="3c62a-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="3c62a-149">إجراءات</span><span class="sxs-lookup"><span data-stu-id="3c62a-149">Actions</span></span>

 | <span data-ttu-id="3c62a-150">اسم الإجراء</span><span class="sxs-lookup"><span data-stu-id="3c62a-150">Action Name</span></span>                               | <span data-ttu-id="3c62a-151">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="3c62a-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="3c62a-152">إرسال</span><span class="sxs-lookup"><span data-stu-id="3c62a-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="3c62a-153">أرسل الطلب لمعالجته من خلال سير العمل.</span><span class="sxs-lookup"><span data-stu-id="3c62a-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3c62a-154">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="3c62a-154">See also</span></span>

- [<span data-ttu-id="3c62a-155">إرسال طلب إجازة إلى سير العمل</span><span class="sxs-lookup"><span data-stu-id="3c62a-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="3c62a-156">المصادقة</span><span class="sxs-lookup"><span data-stu-id="3c62a-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]