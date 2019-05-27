---
title: إنشاء تقويم وإنشاء أوقات عمل
description: وتصف التقويمات القدرة وأوقات العمل لموارد العمليات.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba4bd51d2102b3036307f34ab46f94f83df4f461
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510118"
---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="44d6f-103">إنشاء تقويم وإنشاء أوقات عمل</span><span class="sxs-lookup"><span data-stu-id="44d6f-103">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44d6f-104">وتصف التقويمات القدرة وأوقات العمل لموارد العمليات.</span><span class="sxs-lookup"><span data-stu-id="44d6f-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="44d6f-105">سيساعدك هذا الإجراء في تعريف تقويم عمل استناداً لأحد قوالب أوقات العمل.</span><span class="sxs-lookup"><span data-stu-id="44d6f-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="44d6f-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="44d6f-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="44d6f-107">انتقل إلى كافة مساحات العمل > إدارة دورة حياة الموارد.</span><span class="sxs-lookup"><span data-stu-id="44d6f-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="44d6f-108">انقر فوق "التقويمات".</span><span class="sxs-lookup"><span data-stu-id="44d6f-108">Click Calendars.</span></span>
3. <span data-ttu-id="44d6f-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="44d6f-109">Click New.</span></span>
4. <span data-ttu-id="44d6f-110">في الحقل "التقويم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44d6f-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="44d6f-111">هذا هو معرف التقويم الذي يستخدم كمرجع عند تعيين التقويمات، كمورد عمليات أو مجموعة موارد.</span><span class="sxs-lookup"><span data-stu-id="44d6f-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="44d6f-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44d6f-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="44d6f-113">في الحقل "يوم العمل القياسي بالساعات"، أدخل رقماً.</span><span class="sxs-lookup"><span data-stu-id="44d6f-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="44d6f-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="44d6f-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="44d6f-115">انقر فوق "أوقات العمل".</span><span class="sxs-lookup"><span data-stu-id="44d6f-115">Click Working times.</span></span>
9. <span data-ttu-id="44d6f-116">انقر فوق "تكوين أوقات العمل".</span><span class="sxs-lookup"><span data-stu-id="44d6f-116">Click Compose working times.</span></span>
    * <span data-ttu-id="44d6f-117">قم بإنشاء ساعات العمل لكل يوم في الفترة التي تريد أن تتمكن بها من جدولة العمل.</span><span class="sxs-lookup"><span data-stu-id="44d6f-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="44d6f-118">مع مرور الوقت، يمكنك إنشاء أوقات العمل لفترات إضافية.</span><span class="sxs-lookup"><span data-stu-id="44d6f-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="44d6f-119">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="44d6f-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="44d6f-120">هذا هو اليوم الأول الذي يجب فتح هذا التقويم به.</span><span class="sxs-lookup"><span data-stu-id="44d6f-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="44d6f-121">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="44d6f-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="44d6f-122">هذا هو اليوم الأول الأخير الذي يجب فتح هذا التقويم به.</span><span class="sxs-lookup"><span data-stu-id="44d6f-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="44d6f-123">في الحقل "قالب أوقات العمل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="44d6f-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="44d6f-124">يحدد قالب وقت العمل ساعات العمل لكل يوم من أيام الأسبوع.</span><span class="sxs-lookup"><span data-stu-id="44d6f-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="44d6f-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="44d6f-125">Click OK.</span></span>
14. <span data-ttu-id="44d6f-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44d6f-126">Close the page.</span></span>

