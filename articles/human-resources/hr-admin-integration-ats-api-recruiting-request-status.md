---
title: حالة طلب التعيين
description: يصف هذا الموضوع مجموعة خيارات حالة التعيين لـ Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 888fbc511bffbecd837c929049006266191da5ba
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5806032"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="c033e-103">حالة طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="c033e-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c033e-104">يصف هذا الموضوع مجموعة خيارات حالة التعيين لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c033e-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c033e-105">الاسم الفعلي: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="c033e-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="c033e-106">توفر قائمة التعداد هذه مجموعة الخيارات الخاصة بقيم الحالة لـ RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="c033e-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="c033e-107">قيمة</span><span class="sxs-lookup"><span data-stu-id="c033e-107">Value</span></span> | <span data-ttu-id="c033e-108">تسمية</span><span class="sxs-lookup"><span data-stu-id="c033e-108">Label</span></span> | <span data-ttu-id="c033e-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="c033e-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c033e-110">200000000</span><span class="sxs-lookup"><span data-stu-id="c033e-110">200000000</span></span> | <span data-ttu-id="c033e-111">مبدئي‬</span><span class="sxs-lookup"><span data-stu-id="c033e-111">Draft</span></span> | <span data-ttu-id="c033e-112">الطلب موجود في مسودة وهو غير جاهز للتوظيف النشط.</span><span class="sxs-lookup"><span data-stu-id="c033e-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="c033e-113">200000001</span><span class="sxs-lookup"><span data-stu-id="c033e-113">200000001</span></span> | <span data-ttu-id="c033e-114">قيد المراجعة</span><span class="sxs-lookup"><span data-stu-id="c033e-114">In Review</span></span> | <span data-ttu-id="c033e-115">تم إرسال الطلب ويجري توجيهه للموافقة بواسطة سير العمل.</span><span class="sxs-lookup"><span data-stu-id="c033e-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="c033e-116">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="c033e-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c033e-117">200000002</span><span class="sxs-lookup"><span data-stu-id="c033e-117">200000002</span></span> | <span data-ttu-id="c033e-118">معلّق</span><span class="sxs-lookup"><span data-stu-id="c033e-118">Pending</span></span> | <span data-ttu-id="c033e-119">الطلب معلق لانتظار إجراء سير العمل.</span><span class="sxs-lookup"><span data-stu-id="c033e-119">The request is pending workflow action.</span></span> <span data-ttu-id="c033e-120">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="c033e-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c033e-121">200000003</span><span class="sxs-lookup"><span data-stu-id="c033e-121">200000003</span></span> | <span data-ttu-id="c033e-122">مُلغاة</span><span class="sxs-lookup"><span data-stu-id="c033e-122">Canceled</span></span> | <span data-ttu-id="c033e-123">تم إلغاء الطلب.</span><span class="sxs-lookup"><span data-stu-id="c033e-123">The request has been canceled.</span></span> <span data-ttu-id="c033e-124">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="c033e-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c033e-125">200000004</span><span class="sxs-lookup"><span data-stu-id="c033e-125">200000004</span></span> | <span data-ttu-id="c033e-126">مرفوض</span><span class="sxs-lookup"><span data-stu-id="c033e-126">Denied</span></span> | <span data-ttu-id="c033e-127">تم رفض الطلب.</span><span class="sxs-lookup"><span data-stu-id="c033e-127">The request has been denied.</span></span> <span data-ttu-id="c033e-128">متوفر فقط عند تمكين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="c033e-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c033e-129">200000005</span><span class="sxs-lookup"><span data-stu-id="c033e-129">200000005</span></span> | <span data-ttu-id="c033e-130">نشط</span><span class="sxs-lookup"><span data-stu-id="c033e-130">Active</span></span> | <span data-ttu-id="c033e-131">تم إكمال أي سير عمل والموافقة عليه، والطلب جاهز لعملية التوظيف النشطة.</span><span class="sxs-lookup"><span data-stu-id="c033e-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="c033e-132">200000006</span><span class="sxs-lookup"><span data-stu-id="c033e-132">200000006</span></span> | <span data-ttu-id="c033e-133">مكتمل</span><span class="sxs-lookup"><span data-stu-id="c033e-133">Closed</span></span> | <span data-ttu-id="c033e-134">تم إقفال طلب التعيين.</span><span class="sxs-lookup"><span data-stu-id="c033e-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c033e-135">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="c033e-135">See also</span></span>

[<span data-ttu-id="c033e-136">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="c033e-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="c033e-137">مثال لاستعلام عن طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="c033e-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]