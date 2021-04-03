---
title: حالة طلب التعيين
description: يصف هذا الموضوع مجموعة خيارات حالة التعيين لـ Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464636"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="7bbcd-103">حالة طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="7bbcd-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7bbcd-104">يصف هذا الموضوع مجموعة خيارات حالة التعيين لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7bbcd-105">الاسم الفعلي: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="7bbcd-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="7bbcd-106">توفر قائمة التعداد هذه مجموعة الخيارات الخاصة بقيم الحالة لـ RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="7bbcd-107">قيمة</span><span class="sxs-lookup"><span data-stu-id="7bbcd-107">Value</span></span> | <span data-ttu-id="7bbcd-108">تسمية</span><span class="sxs-lookup"><span data-stu-id="7bbcd-108">Label</span></span> | <span data-ttu-id="7bbcd-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="7bbcd-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7bbcd-110">200000000</span><span class="sxs-lookup"><span data-stu-id="7bbcd-110">200000000</span></span> | <span data-ttu-id="7bbcd-111">مبدئي‬</span><span class="sxs-lookup"><span data-stu-id="7bbcd-111">Draft</span></span> | <span data-ttu-id="7bbcd-112">الطلب موجود في مسودة وهو غير جاهز للتوظيف النشط.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="7bbcd-113">200000001</span><span class="sxs-lookup"><span data-stu-id="7bbcd-113">200000001</span></span> | <span data-ttu-id="7bbcd-114">قيد المراجعة</span><span class="sxs-lookup"><span data-stu-id="7bbcd-114">In Review</span></span> | <span data-ttu-id="7bbcd-115">تم إرسال الطلب ويجري توجيهه للموافقة بواسطة سير العمل.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="7bbcd-116">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="7bbcd-117">200000002</span><span class="sxs-lookup"><span data-stu-id="7bbcd-117">200000002</span></span> | <span data-ttu-id="7bbcd-118">معلّق</span><span class="sxs-lookup"><span data-stu-id="7bbcd-118">Pending</span></span> | <span data-ttu-id="7bbcd-119">الطلب معلق لانتظار إجراء سير العمل.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-119">The request is pending workflow action.</span></span> <span data-ttu-id="7bbcd-120">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="7bbcd-121">200000003</span><span class="sxs-lookup"><span data-stu-id="7bbcd-121">200000003</span></span> | <span data-ttu-id="7bbcd-122">مُلغاة</span><span class="sxs-lookup"><span data-stu-id="7bbcd-122">Canceled</span></span> | <span data-ttu-id="7bbcd-123">تم إلغاء الطلب.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-123">The request has been canceled.</span></span> <span data-ttu-id="7bbcd-124">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="7bbcd-125">200000004</span><span class="sxs-lookup"><span data-stu-id="7bbcd-125">200000004</span></span> | <span data-ttu-id="7bbcd-126">مرفوض</span><span class="sxs-lookup"><span data-stu-id="7bbcd-126">Denied</span></span> | <span data-ttu-id="7bbcd-127">تم رفض الطلب.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-127">The request has been denied.</span></span> <span data-ttu-id="7bbcd-128">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="7bbcd-129">200000005</span><span class="sxs-lookup"><span data-stu-id="7bbcd-129">200000005</span></span> | <span data-ttu-id="7bbcd-130">نشط</span><span class="sxs-lookup"><span data-stu-id="7bbcd-130">Active</span></span> | <span data-ttu-id="7bbcd-131">تم إكمال أي سير عمل والموافقة عليه، والطلب جاهز لعملية التوظيف النشطة.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="7bbcd-132">200000006</span><span class="sxs-lookup"><span data-stu-id="7bbcd-132">200000006</span></span> | <span data-ttu-id="7bbcd-133">مكتمل</span><span class="sxs-lookup"><span data-stu-id="7bbcd-133">Closed</span></span> | <span data-ttu-id="7bbcd-134">تم إقفال طلب التعيين.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7bbcd-135">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="7bbcd-135">See also</span></span>

[<span data-ttu-id="7bbcd-136">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="7bbcd-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="7bbcd-137">مثال لاستعلام عن طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="7bbcd-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]