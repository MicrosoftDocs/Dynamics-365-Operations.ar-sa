---
title: نتيجة تكامل مقدم الطلب
description: يصف هذا الموضوع مجموعة خيارات نتيجة تكامل مقدم الطلب لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: e8e41fe485cc70a668d4610ce6eabba5cd16ac86
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795107"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="110f7-103">نتيجة تكامل مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="110f7-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="110f7-104">يصف هذا الموضوع مجموعة خيارات نتيجة تكامل مقدم الطلب لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="110f7-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="110f7-105">الاسم الفعلي: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="110f7-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="110f7-106">يوفر هذا التعداد الحالة لسجل مرشح.</span><span class="sxs-lookup"><span data-stu-id="110f7-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="110f7-107">قيمة</span><span class="sxs-lookup"><span data-stu-id="110f7-107">Value</span></span> | <span data-ttu-id="110f7-108">تسمية</span><span class="sxs-lookup"><span data-stu-id="110f7-108">Label</span></span> | <span data-ttu-id="110f7-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="110f7-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="110f7-110">200000000</span><span class="sxs-lookup"><span data-stu-id="110f7-110">200000000</span></span> | <span data-ttu-id="110f7-111">لم تتم المعالجة</span><span class="sxs-lookup"><span data-stu-id="110f7-111">Not processed</span></span> | <span data-ttu-id="110f7-112">لا يزال المرشح تحت الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="110f7-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="110f7-113">200000001</span><span class="sxs-lookup"><span data-stu-id="110f7-113">200000001</span></span> | <span data-ttu-id="110f7-114">تم التوظيف</span><span class="sxs-lookup"><span data-stu-id="110f7-114">Hired</span></span> | <span data-ttu-id="110f7-115">تم توظيف المرشح.</span><span class="sxs-lookup"><span data-stu-id="110f7-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="110f7-116">200000002</span><span class="sxs-lookup"><span data-stu-id="110f7-116">200000002</span></span> | <span data-ttu-id="110f7-117">لم يتم توظيفه</span><span class="sxs-lookup"><span data-stu-id="110f7-117">Not hired</span></span> | <span data-ttu-id="110f7-118">تم اتخاذ قرار بعدم توظيف المرشح.</span><span class="sxs-lookup"><span data-stu-id="110f7-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="110f7-119">200000003</span><span class="sxs-lookup"><span data-stu-id="110f7-119">200000003</span></span> | <span data-ttu-id="110f7-120">مستبعد</span><span class="sxs-lookup"><span data-stu-id="110f7-120">Dismissed</span></span> | <span data-ttu-id="110f7-121">تم استبعاد المرشح من الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="110f7-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="110f7-122">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="110f7-122">See also</span></span>

[<span data-ttu-id="110f7-123">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="110f7-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="110f7-124">مثال الاستعلام عن مرشح مراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="110f7-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]