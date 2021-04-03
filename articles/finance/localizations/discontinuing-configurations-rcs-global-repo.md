---
title: إيقاف التكوينات في المستودع العمومي لـ RCS
description: يوضح هذا الموضوع كيفية إيقاف التكوينات في المستودع العمومي لـ RCS.
author: JaneA07
manager: AnnBe
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 35d0af91161d898b09557a83913019609c71e836
ms.sourcegitcommit: e9d19f25e64cf4d1c1d07c8031a7081454a6f79e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/18/2021
ms.locfileid: "5474238"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="8610f-103">إيقاف التكوينات في المستودع العمومي لـ RCS</span><span class="sxs-lookup"><span data-stu-id="8610f-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8610f-104">يوضح هذا الموضوع كيفية إيقاف التكوين في المستودع العمومي لـ RCS.</span><span class="sxs-lookup"><span data-stu-id="8610f-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="8610f-105">سابقا، كان من الممكن فقط حذف التكوينات التي لم تعد مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="8610f-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="8610f-106">ومع ذلك يمكنك الآن وضع علامة على التكوين الذي تم إصداره باعتباره **موقوف** في المستودع العمومي لـ RCS.</span><span class="sxs-lookup"><span data-stu-id="8610f-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="8610f-107">باستخدام هذه الوظيفة، يمكنك أيضًا تنفيذ ما يلي:</span><span class="sxs-lookup"><span data-stu-id="8610f-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="8610f-108">توفير إخطارات مقدمة عند التخطيط لإيقاف أحد التكوينات.</span><span class="sxs-lookup"><span data-stu-id="8610f-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="8610f-109">تضمين التفاصيل القابلة للتطبيق حول التكوين البديل.</span><span class="sxs-lookup"><span data-stu-id="8610f-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="8610f-110">قم بتعيين تاريخ **مدعوم حتى** لتكوين محدد لإعلام المستخدم بمتى سيتم إيقافه.</span><span class="sxs-lookup"><span data-stu-id="8610f-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="8610f-111">عندما تقوم بإيقاف إصدار التكوين، يمكنك تحديد المعلومات الاختيارية التالية:</span><span class="sxs-lookup"><span data-stu-id="8610f-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="8610f-112">**تكوين البديل**</span><span class="sxs-lookup"><span data-stu-id="8610f-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="8610f-113">**إصدار التكوين البديل**</span><span class="sxs-lookup"><span data-stu-id="8610f-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="8610f-114">**ملاحظه نص حر**: استخدم هذا الحقل لتوفير ارتباطات أو مراجع الوثائق</span><span class="sxs-lookup"><span data-stu-id="8610f-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="8610f-115">**مدعوم حتى**: يوفر هذا الحقل التاريخ المقترح الذي سيتم مقابله دعم التكوين/الإصدار الحالي.</span><span class="sxs-lookup"><span data-stu-id="8610f-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="8610f-116">يجب تحديث هذا التاريخ يدويًا.</span><span class="sxs-lookup"><span data-stu-id="8610f-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="8610f-117">لإيقاف التكوين، أكمل الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8610f-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="8610f-118">حدد ما إذا كنت تريد إيقاف إصدار فردي أو كافة الإصدارات التي لها نفس الإعدادات في عملية واحدة وذلك بإعداد **كافة الإصدارات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="8610f-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="8610f-119">قم بتعيين معلمة **الإيقاف** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="8610f-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="8610f-120">حدد **موافق** لإيقاف التكوينات.</span><span class="sxs-lookup"><span data-stu-id="8610f-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="8610f-121">سيتم ملء حقل **تاريخ الإيقاف** عند حفظ التغييرات.</span><span class="sxs-lookup"><span data-stu-id="8610f-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![معلومات إيقاف تكوين](media/Discontinue-details-2.png)
  
<span data-ttu-id="8610f-123">يمكنك إعادة التكوين مرة أخرى إلى **مشترك** أو تعديل معلومات الإيقاف في أي وقت.</span><span class="sxs-lookup"><span data-stu-id="8610f-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="8610f-124">في حالة مشاركة تكوين، حدد تاريخ **مدعوم حتى** وكافة المعلومات الأخرى المرتبطة بالإيقاف للإشارة إلى خطط الإيقاف المستقبلية لك.</span><span class="sxs-lookup"><span data-stu-id="8610f-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="8610f-125">إذا كنت ترغب في مشاركة معلومات حول الإيقاف المخطط، قبل إيقاف التكوين الفعلي، فيمكن للمستخدم ملء كافة الحقول المتعلقة بالاستبدال مسبقًا لكن مع ترك المعلمة **إيقاف** معينة إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="8610f-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="8610f-126">الإيقاف لا يقيد العمليات التي يمكن إجراؤها على التكوينات.</span><span class="sxs-lookup"><span data-stu-id="8610f-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="8610f-127">يمكنك متابعة استيراد التكوينات أو تشغيلها أو اشتقاقها، تعتبر هذه الحقول معلوماتية.</span><span class="sxs-lookup"><span data-stu-id="8610f-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="8610f-128">يدعم Finance عرض هذه المعلومات بدءا من الإصدار 10.0.14</span><span class="sxs-lookup"><span data-stu-id="8610f-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="8610f-129">بدء من الإصدار 10.0.14، يدعم Dynamics 365 Finance عرض معلومات الإيقاف.</span><span class="sxs-lookup"><span data-stu-id="8610f-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="8610f-130">في صفحة **المستودع العمومي**، يمكنك عرض أحدث المعلومات المتعلقة بالإيقاف.</span><span class="sxs-lookup"><span data-stu-id="8610f-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="8610f-131">بشكل افتراضي، تتم تصفية التكوينات التي لم يتم وقفها.</span><span class="sxs-lookup"><span data-stu-id="8610f-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="8610f-132">تعرض صفحة **التكوينات المستوردة** (ERSolutionTable)، التكوينات التي تم إيقافها بالفعل عند استيرادها.</span><span class="sxs-lookup"><span data-stu-id="8610f-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="8610f-133">بالنسبة لتلك التكوينات التي لم يتم إيقافها بعد الاستيراد، يمكن مزامنة معلومات الإيقاف عن طريق تشغيل الوظيفة **تحديثات استيراد التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="8610f-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


