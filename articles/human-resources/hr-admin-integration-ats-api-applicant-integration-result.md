---
title: نتيجة تكامل مقدم الطلب
description: يصف هذا الموضوع مجموعة خيارات نتيجة تكامل مقدم الطلب لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467543"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="0d4bd-103">نتيجة تكامل مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="0d4bd-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0d4bd-104">يصف هذا الموضوع مجموعة خيارات نتيجة تكامل مقدم الطلب لـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0d4bd-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0d4bd-105">الاسم الفعلي: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="0d4bd-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="0d4bd-106">يوفر هذا التعداد الحالة لسجل مرشح.</span><span class="sxs-lookup"><span data-stu-id="0d4bd-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="0d4bd-107">قيمة</span><span class="sxs-lookup"><span data-stu-id="0d4bd-107">Value</span></span> | <span data-ttu-id="0d4bd-108">تسمية</span><span class="sxs-lookup"><span data-stu-id="0d4bd-108">Label</span></span> | <span data-ttu-id="0d4bd-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="0d4bd-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0d4bd-110">200000000</span><span class="sxs-lookup"><span data-stu-id="0d4bd-110">200000000</span></span> | <span data-ttu-id="0d4bd-111">لم تتم المعالجة</span><span class="sxs-lookup"><span data-stu-id="0d4bd-111">Not processed</span></span> | <span data-ttu-id="0d4bd-112">لا يزال المرشح تحت الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="0d4bd-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="0d4bd-113">200000001</span><span class="sxs-lookup"><span data-stu-id="0d4bd-113">200000001</span></span> | <span data-ttu-id="0d4bd-114">تم التوظيف</span><span class="sxs-lookup"><span data-stu-id="0d4bd-114">Hired</span></span> | <span data-ttu-id="0d4bd-115">تم توظيف المرشح.</span><span class="sxs-lookup"><span data-stu-id="0d4bd-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="0d4bd-116">200000002</span><span class="sxs-lookup"><span data-stu-id="0d4bd-116">200000002</span></span> | <span data-ttu-id="0d4bd-117">لم يتم توظيفه</span><span class="sxs-lookup"><span data-stu-id="0d4bd-117">Not hired</span></span> | <span data-ttu-id="0d4bd-118">تم اتخاذ قرار بعدم توظيف المرشح.</span><span class="sxs-lookup"><span data-stu-id="0d4bd-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="0d4bd-119">200000003</span><span class="sxs-lookup"><span data-stu-id="0d4bd-119">200000003</span></span> | <span data-ttu-id="0d4bd-120">مستبعد</span><span class="sxs-lookup"><span data-stu-id="0d4bd-120">Dismissed</span></span> | <span data-ttu-id="0d4bd-121">تم استبعاد المرشح من الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="0d4bd-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0d4bd-122">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="0d4bd-122">See also</span></span>

[<span data-ttu-id="0d4bd-123">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="0d4bd-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="0d4bd-124">مثال الاستعلام عن مرشح مراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="0d4bd-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]