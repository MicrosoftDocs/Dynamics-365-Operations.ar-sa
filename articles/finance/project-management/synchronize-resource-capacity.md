---
title: مزامنة سعة الموارد‬
description: يوفر هذا الموضوع معلومات حول كيفية مزامنة سعة الموارد عبر التقويمات والمشاريع.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760462"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="ffeff-103">مزامنة سعة الموارد‬</span><span class="sxs-lookup"><span data-stu-id="ffeff-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffeff-104">تساعد عمليات مزامنة الموارد على ضمان انتشار معلومات التقويم والتقويم الأساسي في جدولة موارد المشروع.</span><span class="sxs-lookup"><span data-stu-id="ffeff-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="ffeff-105">إذا تغيّر التقويم، فإن العمليات تجري التحديثات المطلوبة على جدولة موارد المشروع.</span><span class="sxs-lookup"><span data-stu-id="ffeff-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="ffeff-106">تساعد العمليات أيضًا على تحسين الأداء، نظرًا لمزامنة معلومات مورد التقويم بشكل مسبق.</span><span class="sxs-lookup"><span data-stu-id="ffeff-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="ffeff-107">ونتيجة لذلك، تحدث عمليات تحديث معلومات جدولة الموارد بشكل أسرع.</span><span class="sxs-lookup"><span data-stu-id="ffeff-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="ffeff-108">نحن نوصي بجدولة العمليات كدفعة بدلاً من جدولتها كل واحدة على حدة.</span><span class="sxs-lookup"><span data-stu-id="ffeff-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="ffeff-109">وإلا، فهناك خطر بأن ينسى أحدهم التواريخ الضمنية عند حدوث آخر عملية مزامنة للمعلومات.</span><span class="sxs-lookup"><span data-stu-id="ffeff-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="ffeff-110">إذا لم يتم استخدام التواريخ الضمنية، فقد تحدث ثغرات أثناء مزامنة التاريخ.</span><span class="sxs-lookup"><span data-stu-id="ffeff-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![مزامنة التقويم](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="ffeff-112">مزامنة عمليات تجميع قدرة المورد</span><span class="sxs-lookup"><span data-stu-id="ffeff-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="ffeff-113">تم تصميم عملية المزامنة لمزامنة كافة معلومات تقويم المورد.</span><span class="sxs-lookup"><span data-stu-id="ffeff-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="ffeff-114">تتضمن هذه المعلومات معلومات التقويم الأساسي حول أي تغييرات تحصل في جدول قدرة تقويم مورد المشروع.</span><span class="sxs-lookup"><span data-stu-id="ffeff-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="ffeff-115">إذا تمت إضافة موارد جديدة في المشروع، فإن المزامنة تساعد على ضمان توفر معلومات التقويم المحدثة.</span><span class="sxs-lookup"><span data-stu-id="ffeff-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="ffeff-116">يمكن إجراء هذه المزامنة في أي وقت.</span><span class="sxs-lookup"><span data-stu-id="ffeff-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="ffeff-117">إننا نوصي باستخدام دفعة.</span><span class="sxs-lookup"><span data-stu-id="ffeff-117">We recommend that you use a batch.</span></span> <span data-ttu-id="ffeff-118">تتوفر الخيارات أثناء مزامنة عمليات حجز القدرة الإنتاجية.</span><span class="sxs-lookup"><span data-stu-id="ffeff-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="ffeff-119">حدد **إدارة المشروع‬ والمحاسبة‬** &gt; **دوري** &gt; **مزامنة القدرة** &gt; **مزامنة عمليات تجميع قدرة المورد**.</span><span class="sxs-lookup"><span data-stu-id="ffeff-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="ffeff-120">عيّن الخيارات في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="ffeff-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="ffeff-121">خيار</span><span class="sxs-lookup"><span data-stu-id="ffeff-121">Option</span></span>      | <span data-ttu-id="ffeff-122">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="ffeff-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="ffeff-123">كود الفترة</span><span class="sxs-lookup"><span data-stu-id="ffeff-123">Period code</span></span> | <span data-ttu-id="ffeff-124">بشكل اختياري، حدد كود الفاصل الزمني لدفتر الأستاذ العام لتعيين تواريخ البدء والانتهاء لمزامنة عمليات تجميع قدرة المورد‬.</span><span class="sxs-lookup"><span data-stu-id="ffeff-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="ffeff-125">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="ffeff-125">Start date</span></span>  | <span data-ttu-id="ffeff-126">أدخل تاريخ البدء لمزامنة عمليات تجميع قدرة المورد‬.</span><span class="sxs-lookup"><span data-stu-id="ffeff-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="ffeff-127">تاريخ الإنهاء</span><span class="sxs-lookup"><span data-stu-id="ffeff-127">End date</span></span>    | <span data-ttu-id="ffeff-128">أدخل تاريخ الانتهاء لمزامنة عمليات تجميع قدرة المورد‬.</span><span class="sxs-lookup"><span data-stu-id="ffeff-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="ffeff-129">[![عملية المزامنة](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="ffeff-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
