---
title: تسجيل إدخالات دفتر اليومية المرّحلة في دفتر يومية
description: يوضح هذه الإجراء كيفية تسجيل إدخالات دفتر اليومية المرحلة في دفتر اليومية.
author: aprilolson
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5028db1db2359a54d565fc299c9a3353a4cf8297
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826144"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="7e38d-103">تسجيل إدخالات دفتر اليومية المرّحلة في دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="7e38d-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e38d-104">يوضح هذه الإجراء كيفية تسجيل إدخالات دفتر اليومية المرحلة في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="7e38d-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="7e38d-105">ويستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="7e38d-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="7e38d-106">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > دفتر الأستاذ العام > إعداد دفتر الأستاذ > محددات دفتر الأستاذ العام**‬.</span><span class="sxs-lookup"><span data-stu-id="7e38d-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="7e38d-107">يمكن تعيين الحقل **دفتر يومية دفتر الأستاذ الموسع** إلى "نعم" أو "لا".</span><span class="sxs-lookup"><span data-stu-id="7e38d-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="7e38d-108">إذا تم تعيينه إلى "نعم"، فستكون مخرجات التقرير مختلفة.</span><span class="sxs-lookup"><span data-stu-id="7e38d-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="7e38d-109">حدد ما إذا كان يمكن إقفال الفترة إذا لم يتم تشغيل عملية التسجيل في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="7e38d-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="7e38d-110">إذا تم تعيين هذا الخيار إلى "نعم"، فلا يمكن إقفال الفترة إلا بعد إتمام عملية التسجيل في دفتر اليومية لتلك الفترة.</span><span class="sxs-lookup"><span data-stu-id="7e38d-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="7e38d-111">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7e38d-111">Close the page.</span></span>
5. <span data-ttu-id="7e38d-112">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > دفتر الأستاذ العام > مهام دورية‬ > تسجيل دفتر اليومية‬**.</span><span class="sxs-lookup"><span data-stu-id="7e38d-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="7e38d-113">انقر فوق **تصفية**.</span><span class="sxs-lookup"><span data-stu-id="7e38d-113">Click **Filter**.</span></span>
7. <span data-ttu-id="7e38d-114">قم بتمييز الصف الذي يحتوي على معايير التصفية التي تريد تعريفها.</span><span class="sxs-lookup"><span data-stu-id="7e38d-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="7e38d-115">في الحقل **المعايير‬**، أدخل معايير التصفية أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7e38d-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="7e38d-116">انقر فوق **موافق** لإغلاق صفحة عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="7e38d-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="7e38d-117">انقر فوق **موافق** لبدء عملية التسجيل في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="7e38d-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="7e38d-118">سيتم إنشاء تقرير بعد اكتمال العملية.</span><span class="sxs-lookup"><span data-stu-id="7e38d-118">A report will be generated after the process is complete.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]