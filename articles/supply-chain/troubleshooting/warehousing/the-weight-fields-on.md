---
title: لا تتطابق حقول الوزن في خطوط التحميل مع حقول الوزن الموجودة على الحمل
description: لا تتطابق حقول الوزن في خطوط التحميل مع حقول الوزن الموجودة على الحمل
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924341"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="1f095-103">لا تتطابق حقول الوزن في خطوط التحميل مع حقول الوزن الموجودة على الحمل</span><span class="sxs-lookup"><span data-stu-id="1f095-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="1f095-104">رموز الأخطاء: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="1f095-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="1f095-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="1f095-105">Symptoms</span></span>

<span data-ttu-id="1f095-106">يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="1f095-106">The system shows the following error message:</span></span>

> <span data-ttu-id="1f095-107">لا تتطابق حقول الوزن في خطوط التحميل مع حقول الوزن الموجودة على الحمل %1.</span><span class="sxs-lookup"><span data-stu-id="1f095-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="1f095-108">قم بتشغيل فحص تناسق وزن حمل المستودع لإعادة حساب حقول الوزن.</span><span class="sxs-lookup"><span data-stu-id="1f095-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="1f095-109">السبب</span><span class="sxs-lookup"><span data-stu-id="1f095-109">Cause</span></span>

<span data-ttu-id="1f095-110">تم تعيين حقلي **الوزن الصافي** و **الوزن الفارغ** إلى *0* (صفر) في بند الحمل.</span><span class="sxs-lookup"><span data-stu-id="1f095-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="1f095-111">ومع ذلك، لم يتم تعيين حقول الوزن إلى *0* لقياسات الوزن على المنتج.</span><span class="sxs-lookup"><span data-stu-id="1f095-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="1f095-112">عندما لا يتم تعيين حقول الوزن على خط التحميل، فإن أي تصحيحات للكمية على خط التحميل قد تتسبب في حساب وزن غير صحيح للحمل.</span><span class="sxs-lookup"><span data-stu-id="1f095-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="1f095-113">قد تحدث هذه المشكلة إذا تم تغيير الأوزان على المنتج منذ إنشاء بند الحمل.</span><span class="sxs-lookup"><span data-stu-id="1f095-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="1f095-114">الدقة</span><span class="sxs-lookup"><span data-stu-id="1f095-114">Resolution</span></span>

<span data-ttu-id="1f095-115">بشكل افتراضي، عند إنشاء بند حمل، يتم إدخال حقول الوزن من المنتج عليه.</span><span class="sxs-lookup"><span data-stu-id="1f095-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="1f095-116">إذا كان الوزن صفرًا، فيمكنك إعادة حسابه باستخدام وظيفة *فحص اتساق وزن الحمولة للمستودع*.</span><span class="sxs-lookup"><span data-stu-id="1f095-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="1f095-117">انتقل إلى **إدارة النظام \> المهام الدورية \> قاعدة البيانات \> تدقيق التناسق**.</span><span class="sxs-lookup"><span data-stu-id="1f095-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="1f095-118">في مربع الحوار **التحقق من الاتساق**، قم بتعيين حقل **الوحدة** إلى *إدارة المستودعات*.</span><span class="sxs-lookup"><span data-stu-id="1f095-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="1f095-119">قم بتعيين حقل **تحقق/إصلاح** إلى *إصلاح الخطأ*.</span><span class="sxs-lookup"><span data-stu-id="1f095-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="1f095-120">في قائمة خانة الاختيار، حدد **فحص اتساق وزن حمولة المستودع**، وتأكد من تحديد صف خانة الاختيار هذا فقط.</span><span class="sxs-lookup"><span data-stu-id="1f095-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="1f095-121">في أعلى قائمة خانة الاختيار، حدد زر علامة القطع (**...**)، ثم حدد **الحوار** على القائمة.</span><span class="sxs-lookup"><span data-stu-id="1f095-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="1f095-122">في مربع الحوار **فحص اتساق وزن حمولة المستودع**، عيّن الحقول التالية لتحديد المعايير التي يجب تشغيل اختبار الاتساق لها:</span><span class="sxs-lookup"><span data-stu-id="1f095-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="1f095-123">**معرف الحمل:** حدد معرف الحمل.</span><span class="sxs-lookup"><span data-stu-id="1f095-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="1f095-124">اترك هذا فارغًا للتحقق من جميع معرفات الحمولات.</span><span class="sxs-lookup"><span data-stu-id="1f095-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="1f095-125">**رقم الصنف:** حدد رقم صنف.</span><span class="sxs-lookup"><span data-stu-id="1f095-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="1f095-126">اترك هذا فارغًا للتحقق من جميع الأصناف.</span><span class="sxs-lookup"><span data-stu-id="1f095-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="1f095-127">**إعادة حساب الوزن على الأحمال دائمًا:** قم بتعيين هذا الخيار إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="1f095-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="1f095-128">**السماح بالكتابة فوق الوزن على بنود الحمل:** قم بتعيين هذا الخيار إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="1f095-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="1f095-129">حدد **موافق** لإغلاق مربع الحوار **فحص اتساق وزن حمل المستودع**.</span><span class="sxs-lookup"><span data-stu-id="1f095-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="1f095-130">حدد زر علامة الحذف، ثم حدد **تنفيذ** على القائمة.</span><span class="sxs-lookup"><span data-stu-id="1f095-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="1f095-131">يتم إعادة حساب الوزن بناءً على المعايير التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="1f095-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="1f095-132">حدد ارتباط **تفاصيل الرسالة** لعرض نتيجة فحص الاتساق.</span><span class="sxs-lookup"><span data-stu-id="1f095-132">Select the **Message details** link to view the result of the consistency check.</span></span>
