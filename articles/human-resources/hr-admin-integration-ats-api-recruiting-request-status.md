---
title: حالة طلب التعيين
description: يصف هذا الموضوع مجموعة خيارات حالة التعيين لـ Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059174"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="0b550-103">حالة طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="0b550-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0b550-104">يصف هذا الموضوع مجموعة خيارات حالة التعيين لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0b550-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0b550-105">الاسم الفعلي: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="0b550-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="0b550-106">توفر قائمة التعداد هذه مجموعة الخيارات الخاصة بقيم الحالة لـ RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="0b550-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="0b550-107">قيمة</span><span class="sxs-lookup"><span data-stu-id="0b550-107">Value</span></span> | <span data-ttu-id="0b550-108">تسمية</span><span class="sxs-lookup"><span data-stu-id="0b550-108">Label</span></span> | <span data-ttu-id="0b550-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="0b550-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0b550-110">200000000</span><span class="sxs-lookup"><span data-stu-id="0b550-110">200000000</span></span> | <span data-ttu-id="0b550-111">مبدئي‬</span><span class="sxs-lookup"><span data-stu-id="0b550-111">Draft</span></span> | <span data-ttu-id="0b550-112">الطلب موجود في مسودة وهو غير جاهز للتوظيف النشط.</span><span class="sxs-lookup"><span data-stu-id="0b550-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="0b550-113">200000001</span><span class="sxs-lookup"><span data-stu-id="0b550-113">200000001</span></span> | <span data-ttu-id="0b550-114">قيد المراجعة</span><span class="sxs-lookup"><span data-stu-id="0b550-114">In Review</span></span> | <span data-ttu-id="0b550-115">تم إرسال الطلب ويجري توجيهه للموافقة بواسطة سير العمل.</span><span class="sxs-lookup"><span data-stu-id="0b550-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="0b550-116">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="0b550-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="0b550-117">200000002</span><span class="sxs-lookup"><span data-stu-id="0b550-117">200000002</span></span> | <span data-ttu-id="0b550-118">معلّق</span><span class="sxs-lookup"><span data-stu-id="0b550-118">Pending</span></span> | <span data-ttu-id="0b550-119">الطلب معلق لانتظار إجراء سير العمل.</span><span class="sxs-lookup"><span data-stu-id="0b550-119">The request is pending workflow action.</span></span> <span data-ttu-id="0b550-120">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="0b550-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="0b550-121">200000003</span><span class="sxs-lookup"><span data-stu-id="0b550-121">200000003</span></span> | <span data-ttu-id="0b550-122">مُلغاة</span><span class="sxs-lookup"><span data-stu-id="0b550-122">Canceled</span></span> | <span data-ttu-id="0b550-123">تم إلغاء الطلب.</span><span class="sxs-lookup"><span data-stu-id="0b550-123">The request has been canceled.</span></span> <span data-ttu-id="0b550-124">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="0b550-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="0b550-125">200000004</span><span class="sxs-lookup"><span data-stu-id="0b550-125">200000004</span></span> | <span data-ttu-id="0b550-126">مرفوض</span><span class="sxs-lookup"><span data-stu-id="0b550-126">Denied</span></span> | <span data-ttu-id="0b550-127">تم رفض الطلب.</span><span class="sxs-lookup"><span data-stu-id="0b550-127">The request has been denied.</span></span> <span data-ttu-id="0b550-128">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="0b550-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="0b550-129">200000005</span><span class="sxs-lookup"><span data-stu-id="0b550-129">200000005</span></span> | <span data-ttu-id="0b550-130">نشط</span><span class="sxs-lookup"><span data-stu-id="0b550-130">Active</span></span> | <span data-ttu-id="0b550-131">تم إكمال أي سير عمل والموافقة عليه، والطلب جاهز لعملية التوظيف النشطة.</span><span class="sxs-lookup"><span data-stu-id="0b550-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="0b550-132">200000006</span><span class="sxs-lookup"><span data-stu-id="0b550-132">200000006</span></span> | <span data-ttu-id="0b550-133">مكتمل</span><span class="sxs-lookup"><span data-stu-id="0b550-133">Closed</span></span> | <span data-ttu-id="0b550-134">تم إقفال طلب التعيين.</span><span class="sxs-lookup"><span data-stu-id="0b550-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0b550-135">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="0b550-135">See also</span></span>

[<span data-ttu-id="0b550-136">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="0b550-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="0b550-137">مثال لاستعلام عن طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="0b550-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]