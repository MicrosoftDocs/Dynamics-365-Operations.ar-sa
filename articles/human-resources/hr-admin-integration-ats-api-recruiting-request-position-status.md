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
ms.openlocfilehash: 01e8aa5157d0ad1c01f996886e7845e49ab97603
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464708"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="eae22-103">حالة منصب طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="eae22-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eae22-104">يصف هذا الموضوع مجموعة خيارات حالة المنصب لطلب التعيين في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="eae22-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="eae22-105">الاسم الفعلي: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="eae22-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="eae22-106">توفر قائمة التعداد هذه مجموعة الخيارات لقيم الحالة لكل منصب خاص بطلب تعيين في الكيان RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="eae22-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="eae22-107">قيمة</span><span class="sxs-lookup"><span data-stu-id="eae22-107">Value</span></span> | <span data-ttu-id="eae22-108">تسمية</span><span class="sxs-lookup"><span data-stu-id="eae22-108">Label</span></span> | <span data-ttu-id="eae22-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="eae22-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="eae22-110">200000000</span><span class="sxs-lookup"><span data-stu-id="eae22-110">200000000</span></span> | <span data-ttu-id="eae22-111">مفتوحة</span><span class="sxs-lookup"><span data-stu-id="eae22-111">Open</span></span> | <span data-ttu-id="eae22-112">المنصب في طلب التعيين مفتوح للتعيين.</span><span class="sxs-lookup"><span data-stu-id="eae22-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="eae22-113">هذا لا يشير إلى أنه لا يوجد تعيين لمنصب نشط حاليًا للمنصب.</span><span class="sxs-lookup"><span data-stu-id="eae22-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="eae22-114">قد يكون هناك موظف في المنصب وقت التوظيف.</span><span class="sxs-lookup"><span data-stu-id="eae22-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="eae22-115">يشير فقط إلى أن المنصب متوفر للتعيين في سياق طلب التعيين.</span><span class="sxs-lookup"><span data-stu-id="eae22-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="eae22-116">200000001</span><span class="sxs-lookup"><span data-stu-id="eae22-116">200000001</span></span> | <span data-ttu-id="eae22-117">مشغول‬</span><span class="sxs-lookup"><span data-stu-id="eae22-117">Filled</span></span> | <span data-ttu-id="eae22-118">تم تحديد عامل للتعيين في المنصب.</span><span class="sxs-lookup"><span data-stu-id="eae22-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="eae22-119">200000002</span><span class="sxs-lookup"><span data-stu-id="eae22-119">200000002</span></span> | <span data-ttu-id="eae22-120">مُلغاة</span><span class="sxs-lookup"><span data-stu-id="eae22-120">Canceled</span></span> | <span data-ttu-id="eae22-121">تم إلغاء الطلب الخاص بالتعيين لهذا المنصب.</span><span class="sxs-lookup"><span data-stu-id="eae22-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="eae22-122">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="eae22-122">See also</span></span>

[<span data-ttu-id="eae22-123">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="eae22-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="eae22-124">مثال لاستعلام عن طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="eae22-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]