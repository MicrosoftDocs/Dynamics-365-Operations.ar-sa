---
title: إضافة خطأ إلى أمر عمل
description: يوضح هذا الموضوع كيفية إضافة تسجيلات أخطاء إلى أوامر العمل في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 083ceca9605ad044c172ba7aa23739d170f8c301
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019294"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="eb658-103">إضافة خطأ إلى أمر العمل</span><span class="sxs-lookup"><span data-stu-id="eb658-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="eb658-104">يمكنك إضافة أخطاء تم إعدادها في مصمم الأخطاء إلى أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="eb658-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="eb658-105">ينبغي ربط سجل خطأ واحد أو أكثر بأنواع الأصول المستخدمة للأصل المحدد في أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="eb658-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="eb658-106">لمزيد من المعلومات حول كيفية الإعداد، راجع [إدارة الأخطاء‬](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="eb658-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="eb658-107">حدد **إدارة الأصول** > **مشترك** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="eb658-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="eb658-108">حدد أمر العمل لإجراء تسجيل خاطئ عليه، ثم في جزء الإجراء، ضمن علامة التبويب **أمر العمل** ، في مجموعة **الأصل** ، حدد **خطأ في الأصل**.</span><span class="sxs-lookup"><span data-stu-id="eb658-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="eb658-109">على علامة التبويب السريعة **الأعراض** ، حدد **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="eb658-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="eb658-110">يتم إدخال رقم خطأ متسلسل في حقل **الخطأ** بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="eb658-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="eb658-111">حدد العَرَض المناسب في حقل **عَرَض الخطأ‬‏‫** .</span><span class="sxs-lookup"><span data-stu-id="eb658-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="eb658-112">في الحقلين **منطقة الخطأ** و **نوع الخطأ** ، حدد القيم المناسبة.</span><span class="sxs-lookup"><span data-stu-id="eb658-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="eb658-113">في حقل **تاريخ الخطأ**، يتم إدراج التاريخ الحالي بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="eb658-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="eb658-114">يمكنك تحديد تاريخ مختلف كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="eb658-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="eb658-115">على علامة التبويب السريعة **أسباب العَرَض المحدد**، أضف سطرًا  يصف سبب المشكلة.</span><span class="sxs-lookup"><span data-stu-id="eb658-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="eb658-116">على علامة التبويب السريعة **علاجات العَرَض المحدد** ، أضف سطرًا يصف حلاً محتملاً للمشكلة.</span><span class="sxs-lookup"><span data-stu-id="eb658-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="eb658-117">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="eb658-117">Select **Save**.</span></span>

<span data-ttu-id="eb658-118">يبين الرسم التوضيحي أدناه مثالاً على تسجيل الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="eb658-118">The illustration below shows an example of a fault registration.</span></span>

![الشكل 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="eb658-120">عرض أخطاء الأصول</span><span class="sxs-lookup"><span data-stu-id="eb658-120">View asset faults</span></span>

<span data-ttu-id="eb658-121">في القائمة **أخطاء الأصول**، يمكنك الحصول على نظرة عامة على جميع الأخطاء المسجلة على الأصول.</span><span class="sxs-lookup"><span data-stu-id="eb658-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="eb658-122">في صفحة قائمة **أخطاء الأصل** ، يمكنك الحصول على نظرة عامة على جميع الأخطاء المسجلة على الأصول.</span><span class="sxs-lookup"><span data-stu-id="eb658-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="eb658-123">لفتح الصفحة، حدد **إدارة الأصول** > **استعلامات‬** > **خطأ الأصل** > **أخطاء الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="eb658-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="eb658-124">طباعة تقارير أخطاء الأصول</span><span class="sxs-lookup"><span data-stu-id="eb658-124">Print asset fault report</span></span>

<span data-ttu-id="eb658-125">من صفحة قائمة **كل الأصول** ، يمكنك طباعة تقرير أخطاء الأصل الذي يعرض جميع تسجيلات الأخطاء بالإضافة إلى نظرة عامة رسومية لإحصاءات الخطأ.</span><span class="sxs-lookup"><span data-stu-id="eb658-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="eb658-126">حدد **إدارة الأصول** > **مشترك** > **الأصول** > **كافة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="eb658-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="eb658-127">حدد الأصل لطباعة تقرير الخطأ له.</span><span class="sxs-lookup"><span data-stu-id="eb658-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="eb658-128">في جزء الإجراءات، على علامة التبويب **عام** ، في مجموعة **تقارير** ، حدد **خطأ الأصل**.</span><span class="sxs-lookup"><span data-stu-id="eb658-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="eb658-129">أدخل فترة معينة، أو حدد نوع الخطأ.</span><span class="sxs-lookup"><span data-stu-id="eb658-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="eb658-130">حدد **موافق** لطباعة التقرير.</span><span class="sxs-lookup"><span data-stu-id="eb658-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="eb658-131">لطباعة تقرير الأخطاء للعديد من الأصول أو أنواع الأصول، حدد **إدارة الأصول** > **التقارير** > **الأصول‏‎** > **خطأ الأصل**.</span><span class="sxs-lookup"><span data-stu-id="eb658-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

