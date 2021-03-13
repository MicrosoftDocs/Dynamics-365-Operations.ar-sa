---
title: حالة الإعفاء من الوظيفة
description: يصف هذا الموضوع مجموعة خيارات حالة الإعفاء من الوظيفة لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125559"
---
# <a name="job-exempt-status"></a><span data-ttu-id="0c540-103">حالة الإعفاء من الوظيفة</span><span class="sxs-lookup"><span data-stu-id="0c540-103">Job exempt status</span></span>

<span data-ttu-id="0c540-104">يصف هذا الموضوع مجموعة خيارات حالة الإعفاء من الوظيفة لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c540-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0c540-105">الاسم الفعلي: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="0c540-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="0c540-106">تحدد قائمة التعداد هذه مجموعة خيارات لقيم حالة حالة الإعفاء من الوظيفة لـ FLSA.</span><span class="sxs-lookup"><span data-stu-id="0c540-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="0c540-107">يتم توفير ذلك في مجموعة خيارات cdm_jobexemptstatus الموجودة.</span><span class="sxs-lookup"><span data-stu-id="0c540-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="0c540-108">قيمة</span><span class="sxs-lookup"><span data-stu-id="0c540-108">Value</span></span> | <span data-ttu-id="0c540-109">تسمية</span><span class="sxs-lookup"><span data-stu-id="0c540-109">Label</span></span> | <span data-ttu-id="0c540-110">الوصف</span><span class="sxs-lookup"><span data-stu-id="0c540-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0c540-111">200000000</span><span class="sxs-lookup"><span data-stu-id="0c540-111">200000000</span></span> | <span data-ttu-id="0c540-112">إعفاء</span><span class="sxs-lookup"><span data-stu-id="0c540-112">Exempt</span></span> | <span data-ttu-id="0c540-113">تحتوي الوظيفة على حالة إعفاء استنادا إلى إرشادات FLSA.</span><span class="sxs-lookup"><span data-stu-id="0c540-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="0c540-114">200000001</span><span class="sxs-lookup"><span data-stu-id="0c540-114">200000001</span></span> | <span data-ttu-id="0c540-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="0c540-115">NonExempt</span></span> | <span data-ttu-id="0c540-116">تحتوي الوظيفة على حالة عدم إعفاء استنادا إلى إرشادات FLSA.</span><span class="sxs-lookup"><span data-stu-id="0c540-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="0c540-117">200000002</span><span class="sxs-lookup"><span data-stu-id="0c540-117">200000002</span></span> | <span data-ttu-id="0c540-118">لا ينطبق</span><span class="sxs-lookup"><span data-stu-id="0c540-118">Does Not Apply</span></span> | <span data-ttu-id="0c540-119">لا تنطبق إرشادات حالة FLSA على الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="0c540-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0c540-120">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="0c540-120">See also</span></span>

[<span data-ttu-id="0c540-121">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="0c540-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="0c540-122">مثال لاستعلام عن طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="0c540-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
