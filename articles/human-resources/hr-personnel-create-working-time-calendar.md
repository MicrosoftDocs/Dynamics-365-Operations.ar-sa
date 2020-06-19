---
title: إنشاء تقويمات وإنشاء أوقات عمل
description: وتصف التقويمات القدرة وأوقات العمل لموارد العمليات. تشرح هذه المقالة كيفية تعريف تقويم عمل استنادًا إلى قالب وقت عمل.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f4960f895ac6a9e6284119a998af540523785ed
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430361"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="52113-104">إنشاء تقويمات وإنشاء أوقات عمل</span><span class="sxs-lookup"><span data-stu-id="52113-104">Create calendars and generate working times</span></span>



<span data-ttu-id="52113-105">وتصف التقويمات القدرة وأوقات العمل لموارد العمليات.</span><span class="sxs-lookup"><span data-stu-id="52113-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="52113-106">تشرح هذه المقالة كيفية تعريف تقويم عمل استنادًا إلى قالب وقت عمل.</span><span class="sxs-lookup"><span data-stu-id="52113-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="52113-107">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="52113-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="52113-108">في الصفحة الرئيسية، حدد **إدارة دورة حياة الموارد**.</span><span class="sxs-lookup"><span data-stu-id="52113-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="52113-109">حدد **التقويمات**.</span><span class="sxs-lookup"><span data-stu-id="52113-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="52113-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="52113-110">Select **New**.</span></span>
4. <span data-ttu-id="52113-111">في حقل **التقويم**، قم بتصنيف التقويم.</span><span class="sxs-lookup"><span data-stu-id="52113-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="52113-112">هذا هو معرف التقويم الذي يستخدم كمرجع عند تعيين التقويمات، كمورد عمليات أو مجموعة موارد.</span><span class="sxs-lookup"><span data-stu-id="52113-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="52113-113">في حقل **الاسم**، أدخل اسمًا للتقويم.</span><span class="sxs-lookup"><span data-stu-id="52113-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="52113-114">في الحقل **يوم العمل القياسي بالساعات**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="52113-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="52113-115">تأكد من تحديد الصف، ثم حدد **أوقات العمل** من جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="52113-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="52113-116">حدد **إنشاء أوقات العمل**.</span><span class="sxs-lookup"><span data-stu-id="52113-116">Select **Compose working times**.</span></span> <span data-ttu-id="52113-117">قم بإنشاء ساعات العمل لكل يوم في الفترة التي تريد أن تتمكن بها من جدولة العمل.</span><span class="sxs-lookup"><span data-stu-id="52113-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="52113-118">مع مرور الوقت، يمكنك إنشاء أوقات العمل لفترات إضافية.</span><span class="sxs-lookup"><span data-stu-id="52113-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="52113-119">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="52113-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="52113-120">هذا هو اليوم الأول الذي يجب فتح هذا التقويم به.</span><span class="sxs-lookup"><span data-stu-id="52113-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="52113-121">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="52113-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="52113-122">هذا هو اليوم الأول الأخير الذي يجب فتح هذا التقويم به.</span><span class="sxs-lookup"><span data-stu-id="52113-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="52113-123">في الحقل **قالب أوقات العمل**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="52113-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="52113-124">يحدد قالب وقت العمل ساعات العمل لكل يوم من أيام الأسبوع.</span><span class="sxs-lookup"><span data-stu-id="52113-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="52113-125">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="52113-125">Select **OK**.</span></span>
13. <span data-ttu-id="52113-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="52113-126">Close the page.</span></span>

