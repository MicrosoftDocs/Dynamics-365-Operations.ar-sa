---
title: حالة منصب طلب التعيين
description: يصف هذا الموضوع مجموعة خيارات حالة المنصب لطلب التعيين في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126040"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="b3e25-103">حالة منصب طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="b3e25-103">Recruiting request position status</span></span>

<span data-ttu-id="b3e25-104">يصف هذا الموضوع مجموعة خيارات حالة المنصب لطلب التعيين في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b3e25-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b3e25-105">الاسم الفعلي: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="b3e25-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="b3e25-106">توفر قائمة التعداد هذه مجموعة الخيارات لقيم الحالة لكل منصب خاص بطلب تعيين في الكيان RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="b3e25-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="b3e25-107">قيمة</span><span class="sxs-lookup"><span data-stu-id="b3e25-107">Value</span></span> | <span data-ttu-id="b3e25-108">تسمية</span><span class="sxs-lookup"><span data-stu-id="b3e25-108">Label</span></span> | <span data-ttu-id="b3e25-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="b3e25-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b3e25-110">200000000</span><span class="sxs-lookup"><span data-stu-id="b3e25-110">200000000</span></span> | <span data-ttu-id="b3e25-111">مفتوحة</span><span class="sxs-lookup"><span data-stu-id="b3e25-111">Open</span></span> | <span data-ttu-id="b3e25-112">المنصب في طلب التعيين مفتوح للتعيين.</span><span class="sxs-lookup"><span data-stu-id="b3e25-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="b3e25-113">هذا لا يشير إلى أنه لا يوجد تعيين لمنصب نشط حاليًا للمنصب.</span><span class="sxs-lookup"><span data-stu-id="b3e25-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="b3e25-114">قد يكون هناك موظف في المنصب وقت التوظيف.</span><span class="sxs-lookup"><span data-stu-id="b3e25-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="b3e25-115">يشير فقط إلى أن المنصب متوفر للتعيين في سياق طلب التعيين.</span><span class="sxs-lookup"><span data-stu-id="b3e25-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="b3e25-116">200000001</span><span class="sxs-lookup"><span data-stu-id="b3e25-116">200000001</span></span> | <span data-ttu-id="b3e25-117">مشغول‬</span><span class="sxs-lookup"><span data-stu-id="b3e25-117">Filled</span></span> | <span data-ttu-id="b3e25-118">تم تحديد عامل للتعيين في المنصب.</span><span class="sxs-lookup"><span data-stu-id="b3e25-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="b3e25-119">200000002</span><span class="sxs-lookup"><span data-stu-id="b3e25-119">200000002</span></span> | <span data-ttu-id="b3e25-120">مُلغاة</span><span class="sxs-lookup"><span data-stu-id="b3e25-120">Canceled</span></span> | <span data-ttu-id="b3e25-121">تم إلغاء الطلب الخاص بالتعيين لهذا المنصب.</span><span class="sxs-lookup"><span data-stu-id="b3e25-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b3e25-122">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="b3e25-122">See also</span></span>

[<span data-ttu-id="b3e25-123">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="b3e25-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="b3e25-124">مثال لاستعلام عن طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="b3e25-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
