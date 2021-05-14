---
title: الموجة غير مؤهلة للتنظيف
description: الموجة غير مؤهلة للتنظيف
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924317"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="59be1-103">الموجة غير مؤهلة للتنظيف</span><span class="sxs-lookup"><span data-stu-id="59be1-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="59be1-104">رمز الخطأ: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="59be1-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="59be1-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="59be1-105">Symptoms</span></span>

<span data-ttu-id="59be1-106">يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="59be1-106">The system shows the following error message:</span></span>

> <span data-ttu-id="59be1-107">الموجة %1 غير صالحة للتنظيف.</span><span class="sxs-lookup"><span data-stu-id="59be1-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="59be1-108">لا يمكن تنظيف بيانات الموجة.</span><span class="sxs-lookup"><span data-stu-id="59be1-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="59be1-109">السبب</span><span class="sxs-lookup"><span data-stu-id="59be1-109">Cause</span></span>

<span data-ttu-id="59be1-110">تتم معالجة الموجة حاليًا، كما يتضح من أحد الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="59be1-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="59be1-111">يتم تعيين حقل **حالة الموجة** إلى *جارٍ التنفيذ*.</span><span class="sxs-lookup"><span data-stu-id="59be1-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="59be1-112">عند تحديد **وظيفة الدفعة** في مجموعة **الموجة** في علامة التبويب **الموجة** في جزء الإجراءات، لم يتم تعيين حقل **الحالة** إلى *منتهي* أو *خطأ* أو *ملغى*.</span><span class="sxs-lookup"><span data-stu-id="59be1-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="59be1-113">لذلك، يتم تشغيل وظيفة دفعية حاليًا.</span><span class="sxs-lookup"><span data-stu-id="59be1-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="59be1-114">الدقة</span><span class="sxs-lookup"><span data-stu-id="59be1-114">Resolution</span></span>

<span data-ttu-id="59be1-115">في جزء الإجراءات، في علامة التبويب **موجة**، في مجموعة **الموجة**، حدد **وظيفة الدفعة**، ثم اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="59be1-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="59be1-116">في حالة تعيين حقل **الحالة** إلى *جارٍ التنفيذ*: في جزء الإجراءات، في علامة التبويب **وظيفة الدفعة**، في مجموعة **وظيفة الدفعة**، حدد **عرض المهام**.</span><span class="sxs-lookup"><span data-stu-id="59be1-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="59be1-117">يمكنك متابعة التقدم عن طريق تحديث صفحة **مهام الدفعات**.</span><span class="sxs-lookup"><span data-stu-id="59be1-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="59be1-118">في حالة عدم تعيين حقل **الحالة** إلى *جارٍ التنفيذ*: في جزء الإجراءات، في علامة التبويب **وظيفة الدفعة**، في مجموعة **الوظائف**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="59be1-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="59be1-119">في حقل **تحديد حالة جديدة**، حدد *قيد الانتظار*.</span><span class="sxs-lookup"><span data-stu-id="59be1-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="59be1-120">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="59be1-120">Then select **OK**.</span></span>
