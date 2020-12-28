---
title: تكوين الأحداث الحياتية المستقبلية
description: يمكنك جدولة الأحداث الحياتية المستقبلية في Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78c65faa4ae0f428184700a912998e9dded026c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417065"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="83803-103">تكوين الأحداث الحياتية المستقبلية</span><span class="sxs-lookup"><span data-stu-id="83803-103">Configure future life events</span></span>

<span data-ttu-id="83803-104">يمكنك جدولة الأحداث الحياتية المستقبلية في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="83803-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="83803-105">في مساحة العمل **إدارة المزايا**، ضمن **إعداد**، حدد **الأحداث الحياتية المستقبلية**.</span><span class="sxs-lookup"><span data-stu-id="83803-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="83803-106">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="83803-106">Select **New**.</span></span>

3. <span data-ttu-id="83803-107">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="83803-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="83803-108">الحقل</span><span class="sxs-lookup"><span data-stu-id="83803-108">Field</span></span> | <span data-ttu-id="83803-109">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="83803-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="83803-110">تاريخ حدث الحياة</span><span class="sxs-lookup"><span data-stu-id="83803-110">Life event date</span></span> | <span data-ttu-id="83803-111">يقوم النظام بمعالجة كافة الأحداث الحياتية خلال فترة التسجيل التي تتم حتى هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="83803-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="83803-112">تم تسجيل حدث الحياة</span><span class="sxs-lookup"><span data-stu-id="83803-112">Life event logged</span></span> | <span data-ttu-id="83803-113">تاريخ ووقت تسجيل الحدث الحياتي.</span><span class="sxs-lookup"><span data-stu-id="83803-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="83803-114">نوع السجل</span><span class="sxs-lookup"><span data-stu-id="83803-114">Log type</span></span> | <span data-ttu-id="83803-115">يعرض ما إذا كان الإجراء واحدًا مما يلي:</span><span class="sxs-lookup"><span data-stu-id="83803-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="83803-116">- **تحديث** -تغيير في سجل موجود يتتبع الأحداث الحياتية</span><span class="sxs-lookup"><span data-stu-id="83803-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="83803-117">- **إدراج** -إنشاء سجل حدث حياتي جديد</span><span class="sxs-lookup"><span data-stu-id="83803-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="83803-118">معرف نوع حدث الحياة</span><span class="sxs-lookup"><span data-stu-id="83803-118">Life event type ID</span></span> | <span data-ttu-id="83803-119">المعرف الفريد لنوع الحدث الحياتي.</span><span class="sxs-lookup"><span data-stu-id="83803-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="83803-120">نوع حدث الحياة</span><span class="sxs-lookup"><span data-stu-id="83803-120">Life event type</span></span> | <span data-ttu-id="83803-121">حافز لتحديث تسجيل مزايا الموظف.</span><span class="sxs-lookup"><span data-stu-id="83803-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="83803-122">لمزيد من التفاصيل، راجع قسم مشغلات الحدث الحياتي.</span><span class="sxs-lookup"><span data-stu-id="83803-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="83803-123">الحالة</span><span class="sxs-lookup"><span data-stu-id="83803-123">Status</span></span> | <span data-ttu-id="83803-124">هل تمت معالجة الحدث الحياتي أم لا.</span><span class="sxs-lookup"><span data-stu-id="83803-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="83803-125">البند</span><span class="sxs-lookup"><span data-stu-id="83803-125">Line</span></span> | <span data-ttu-id="83803-126">رقم البند الخاص بالحدث الحياتي المستقبلي.</span><span class="sxs-lookup"><span data-stu-id="83803-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="83803-127">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="83803-127">Select **Save**.</span></span> 
