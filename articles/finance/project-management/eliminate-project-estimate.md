---
title: حذف تقدير مشروع
description: يوفر هذا الموضوع معلومات حول حذف تقدير المشروع بعد اكتماله.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410186"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="f1b1c-103">حذف تقدير مشروع</span><span class="sxs-lookup"><span data-stu-id="f1b1c-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1b1c-104">توفر تقديرات المشروع طريقة العرض المالية للعمل المقدّر والمجدول لأحد المشاريع.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="f1b1c-105">للعمل مع تقديرات المشروع، يجب إرفاق المشروع بمشروع تقديري‬.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="f1b1c-106">يستند المشروع التقديري دائمًا إلى مشروع موجود، ولكن بإمكان مشاريع متعددة أن تشير إلى مشروع تقديري واحد.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="f1b1c-107">يمكن إرفاق المشاريع الاستثمارية وثابتة السعر فقط بالمشاريع التقديرية، ويجب أن تنتمي هذه المشاريع إلى مجموعة المشاريع نفسها في المشروع التقديري.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="f1b1c-108">لحذف مشروع تقديري، يجب أن يكون مكتملاً.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="f1b1c-109">توضح الخطوات التالية كيفية حذف تقدير.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="f1b1c-110">انتقل إلى **إدارة المشاريع والمحاسبة** > **جميع المشاريع** وافتح المشروع.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="f1b1c-111">في علامة التبويب **إدارة**، حدد **التقديرات**، وفي صفحة **التقدير**، حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="f1b1c-112">في الصفحة **حذف التقدير** على علامة التبويب **عام**، قم بتعيين الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="f1b1c-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="f1b1c-113">**كود الفترة**: حدد كود الفترة لاختيار مشاريع التقدير المناسبة.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="f1b1c-114">**تاريخ التقدير**: حدد تاريخ التقدير المناسب لحذفه.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="f1b1c-115">**الإزالة مع وجود تحذيرات الأعمال تحت التنفيذ**: يمكنك تمكين هذا الخيار لتقديم إعلام عندما سيتم حذف تقدير مرتبط بالأعمال تحت التنفيذ (WIP).</span><span class="sxs-lookup"><span data-stu-id="f1b1c-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="f1b1c-116">لا يمكن متابعة عملية الحذف في حال وجود أي حركات غير تقديرية.، عند عدم تمكين هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="f1b1c-117">لا يتوفر هذا الخيار الا عند تطبيق الحذف على مشروع تقديري.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="f1b1c-118">وهو لا يتوفر إذا كنت تستخدم عمليات ترحيل دورية.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="f1b1c-119">يعمل هذا الإعداد مع الإعدادات الموجودة في علامة تبويب **التقدير** في صفحة **معلمات المشروع** في مجموعة الحقول **السماح بالاستبعاد عند وجود حركات لم يتم تقديرها**.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="f1b1c-120">**‏‏تعيين المرحلة على "منتهي"**: يمكنك بتمكين هذا الخيار لتعيين مرحلة المشروع التقديري إلى **منتهي** بعد تشغيل الحذف.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="f1b1c-121">**‏‏طباعة قائمة التقديرات**: حدد المعلومات المطلوب تضمينها عند ‏‏طباعة قائمة التقديرات.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="f1b1c-122">**إظهار سجل المعلومات** : يمكنك تمكين هذا الخيار لعرض سجل المعلومات.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="f1b1c-123">**تاريخ الترحيل**: اختر تاريخ ترحيل دفتر الأستاذ الخاص بالتقدير.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="f1b1c-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-124">Select **OK**.</span></span>
5. <span data-ttu-id="f1b1c-125">بعد اكتمال عملية الحذف، يظهر المشروع التقديري المحذوف مع قيمة سالبة.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="f1b1c-126">إذا لم تكن تنوي إزالة تقدير، فيمكنك تحديد التقدير المحذوف وتحديد **عكس عملية الاستبعاد**.</span><span class="sxs-lookup"><span data-stu-id="f1b1c-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
