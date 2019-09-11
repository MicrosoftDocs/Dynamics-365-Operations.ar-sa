---
title: إضافة خطأ إلى أمر عمل
description: يوضح هذا الموضوع كيفية إضافة تسجيلات أخطاء إلى أوامر العمل في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875488"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="33370-103">إضافة خطأ إلى أمر عمل</span><span class="sxs-lookup"><span data-stu-id="33370-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="33370-104">يمكنك إضافة أخطاء تم إعدادها في مصمم الأخطاء إلى أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="33370-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="33370-105">يجب ان يحتوي الأصل المحدد في أمر العمل على أنواع أصول تتضمن سجل خطأ أو أكثر يرتبط بها.</span><span class="sxs-lookup"><span data-stu-id="33370-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="33370-106">اقرأ المزيد حول الإعداد في القسم [إدارة الأخطاء](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="33370-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="33370-107">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="33370-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="33370-108">في القائمة، حدد أمر العمل الذي ترغب في إجراء تسجيل خطأ عليه، وانقر فوق **أخطاء الأصول‬‬**.</span><span class="sxs-lookup"><span data-stu-id="33370-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="33370-109">على علامة التبويب السريعة **الأعراض**، انقر فوق **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="33370-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="33370-110">يتم إدراج رقم خطأ متسلسل في حقل **الخطأ** بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="33370-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="33370-111">حدد العَرَض المناسب في حقل **العَرَض**.</span><span class="sxs-lookup"><span data-stu-id="33370-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="33370-112">حدد **منطقة الخطأ** و**نوع الخطأ‏‎**.</span><span class="sxs-lookup"><span data-stu-id="33370-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="33370-113">في حقل **تاريخ الخطأ**، يتم إدراج التاريخ الحالي بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="33370-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="33370-114">يمكنك تحديد تاريخ آخر، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="33370-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="33370-115">على علامة التبويب السريعة **أسباب العَرَض المحدد**، أضف بندًا يصف سبب المشكلة.</span><span class="sxs-lookup"><span data-stu-id="33370-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="33370-116">على علامة التبويب السريعة **علاجات العَرَض المحدد**، أضف بندًا يصف حلاً محتملاً للمشكلة.</span><span class="sxs-lookup"><span data-stu-id="33370-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="33370-117">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="33370-117">Click **Save**.</span></span>

![الشكل 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="33370-119">عرض أخطاء الأصول</span><span class="sxs-lookup"><span data-stu-id="33370-119">View asset faults</span></span>

<span data-ttu-id="33370-120">في القائمة **أخطاء الأصول**، يمكنك الحصول على نظرة عامة على جميع الأخطاء المسجلة على الأصول.</span><span class="sxs-lookup"><span data-stu-id="33370-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="33370-121">انقر فوق **إدارة الأصول** > **استعلامات‬** > **خطأ الأصل** > **أخطا الأصول‏‎** لفتح القائمة.</span><span class="sxs-lookup"><span data-stu-id="33370-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="33370-122">طباعة تقارير أخطاء الأصول</span><span class="sxs-lookup"><span data-stu-id="33370-122">Print asset fault report</span></span>

<span data-ttu-id="33370-123">من صفحة قائمة **كل الأصول**، يمكنك طباعة تقرير أخطاء الأصول الذي يعرض جميع تسجيلات الأخطاء بالإضافة إلى نظرة عامة رسومية لإحصاءات الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="33370-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="33370-124">انقر فوق **إدارة الأصول** > **عام** > **الأصول** > **كل الأصول**.</span><span class="sxs-lookup"><span data-stu-id="33370-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="33370-125">في قائمة **الأصول**، حدد الأصل الذي تريد طباعة تقرير الأخطاء له.</span><span class="sxs-lookup"><span data-stu-id="33370-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="33370-126">على علامة التبويب **عام** > **قسم التقارير**، انقر فوق **خطأ الأصل**.</span><span class="sxs-lookup"><span data-stu-id="33370-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="33370-127">أدخل فترة معينة، أو حدد نوع الخطأ.</span><span class="sxs-lookup"><span data-stu-id="33370-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="33370-128">انقر فوق **موافق** لطباعة التقرير.</span><span class="sxs-lookup"><span data-stu-id="33370-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="33370-129">يمكنك أيضًا طباعة تقرير الأخطاء لعدد كبير من الأصول أو أنواع الأصول عن طريق النقر فوق **إدارة الأصول** > **التقارير** > **الأصول‏‎** > **خطأ الأصل**.</span><span class="sxs-lookup"><span data-stu-id="33370-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

