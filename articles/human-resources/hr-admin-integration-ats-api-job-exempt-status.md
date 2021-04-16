---
title: حالة الإعفاء من الوظيفة
description: يصف هذا الموضوع مجموعة خيارات حالة الإعفاء من الوظيفة لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798287"
---
# <a name="job-exempt-status"></a><span data-ttu-id="fddc9-103">حالة الإعفاء من الوظيفة</span><span class="sxs-lookup"><span data-stu-id="fddc9-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fddc9-104">يصف هذا الموضوع مجموعة خيارات حالة الإعفاء من الوظيفة لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fddc9-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="fddc9-105">الاسم الفعلي: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="fddc9-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="fddc9-106">تحدد قائمة التعداد هذه مجموعة خيارات لقيم حالة حالة الإعفاء من الوظيفة لـ FLSA.</span><span class="sxs-lookup"><span data-stu-id="fddc9-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="fddc9-107">يتم توفير ذلك في مجموعة خيارات cdm_jobexemptstatus الموجودة.</span><span class="sxs-lookup"><span data-stu-id="fddc9-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="fddc9-108">قيمة</span><span class="sxs-lookup"><span data-stu-id="fddc9-108">Value</span></span> | <span data-ttu-id="fddc9-109">تسمية</span><span class="sxs-lookup"><span data-stu-id="fddc9-109">Label</span></span> | <span data-ttu-id="fddc9-110">الوصف</span><span class="sxs-lookup"><span data-stu-id="fddc9-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fddc9-111">200000000</span><span class="sxs-lookup"><span data-stu-id="fddc9-111">200000000</span></span> | <span data-ttu-id="fddc9-112">إعفاء</span><span class="sxs-lookup"><span data-stu-id="fddc9-112">Exempt</span></span> | <span data-ttu-id="fddc9-113">تحتوي الوظيفة على حالة إعفاء استنادا إلى إرشادات FLSA.</span><span class="sxs-lookup"><span data-stu-id="fddc9-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="fddc9-114">200000001</span><span class="sxs-lookup"><span data-stu-id="fddc9-114">200000001</span></span> | <span data-ttu-id="fddc9-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="fddc9-115">NonExempt</span></span> | <span data-ttu-id="fddc9-116">تحتوي الوظيفة على حالة عدم إعفاء استنادا إلى إرشادات FLSA.</span><span class="sxs-lookup"><span data-stu-id="fddc9-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="fddc9-117">200000002</span><span class="sxs-lookup"><span data-stu-id="fddc9-117">200000002</span></span> | <span data-ttu-id="fddc9-118">لا ينطبق</span><span class="sxs-lookup"><span data-stu-id="fddc9-118">Does Not Apply</span></span> | <span data-ttu-id="fddc9-119">لا تنطبق إرشادات حالة FLSA على الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="fddc9-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="fddc9-120">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="fddc9-120">See also</span></span>

[<span data-ttu-id="fddc9-121">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="fddc9-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="fddc9-122">مثال لاستعلام عن طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="fddc9-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]