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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125944"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="e1ecd-103">حالة طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="e1ecd-103">Recruiting request status</span></span>

<span data-ttu-id="e1ecd-104">يصف هذا الموضوع مجموعة خيارات حالة التعيين لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e1ecd-105">الاسم الفعلي: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="e1ecd-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="e1ecd-106">توفر قائمة التعداد هذه مجموعة الخيارات الخاصة بقيم الحالة لـ RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="e1ecd-107">قيمة</span><span class="sxs-lookup"><span data-stu-id="e1ecd-107">Value</span></span> | <span data-ttu-id="e1ecd-108">تسمية</span><span class="sxs-lookup"><span data-stu-id="e1ecd-108">Label</span></span> | <span data-ttu-id="e1ecd-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="e1ecd-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e1ecd-110">200000000</span><span class="sxs-lookup"><span data-stu-id="e1ecd-110">200000000</span></span> | <span data-ttu-id="e1ecd-111">مبدئي‬</span><span class="sxs-lookup"><span data-stu-id="e1ecd-111">Draft</span></span> | <span data-ttu-id="e1ecd-112">الطلب موجود في مسودة وهو غير جاهز للتوظيف النشط.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="e1ecd-113">200000001</span><span class="sxs-lookup"><span data-stu-id="e1ecd-113">200000001</span></span> | <span data-ttu-id="e1ecd-114">قيد المراجعة</span><span class="sxs-lookup"><span data-stu-id="e1ecd-114">In Review</span></span> | <span data-ttu-id="e1ecd-115">تم إرسال الطلب ويجري توجيهه للموافقة بواسطة سير العمل.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="e1ecd-116">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e1ecd-117">200000002</span><span class="sxs-lookup"><span data-stu-id="e1ecd-117">200000002</span></span> | <span data-ttu-id="e1ecd-118">معلّق</span><span class="sxs-lookup"><span data-stu-id="e1ecd-118">Pending</span></span> | <span data-ttu-id="e1ecd-119">الطلب معلق لانتظار إجراء سير العمل.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-119">The request is pending workflow action.</span></span> <span data-ttu-id="e1ecd-120">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e1ecd-121">200000003</span><span class="sxs-lookup"><span data-stu-id="e1ecd-121">200000003</span></span> | <span data-ttu-id="e1ecd-122">مُلغاة</span><span class="sxs-lookup"><span data-stu-id="e1ecd-122">Canceled</span></span> | <span data-ttu-id="e1ecd-123">تم إلغاء الطلب.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-123">The request has been canceled.</span></span> <span data-ttu-id="e1ecd-124">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e1ecd-125">200000004</span><span class="sxs-lookup"><span data-stu-id="e1ecd-125">200000004</span></span> | <span data-ttu-id="e1ecd-126">مرفوض</span><span class="sxs-lookup"><span data-stu-id="e1ecd-126">Denied</span></span> | <span data-ttu-id="e1ecd-127">تم رفض الطلب.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-127">The request has been denied.</span></span> <span data-ttu-id="e1ecd-128">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e1ecd-129">200000005</span><span class="sxs-lookup"><span data-stu-id="e1ecd-129">200000005</span></span> | <span data-ttu-id="e1ecd-130">نشط</span><span class="sxs-lookup"><span data-stu-id="e1ecd-130">Active</span></span> | <span data-ttu-id="e1ecd-131">تم إكمال أي سير عمل والموافقة عليه، والطلب جاهز لعملية التوظيف النشطة.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="e1ecd-132">200000006</span><span class="sxs-lookup"><span data-stu-id="e1ecd-132">200000006</span></span> | <span data-ttu-id="e1ecd-133">مكتمل</span><span class="sxs-lookup"><span data-stu-id="e1ecd-133">Closed</span></span> | <span data-ttu-id="e1ecd-134">تم إقفال طلب التعيين.</span><span class="sxs-lookup"><span data-stu-id="e1ecd-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e1ecd-135">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="e1ecd-135">See also</span></span>

[<span data-ttu-id="e1ecd-136">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="e1ecd-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e1ecd-137">مثال لاستعلام عن طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="e1ecd-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
