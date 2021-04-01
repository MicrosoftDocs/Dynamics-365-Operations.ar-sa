---
title: إضافة مهمة سابقة إلى نشاط تدفق الإنتاج
description: في إصدار تدفق الإنتاج، يجب أن تكون كافة الأنشطة متسلسلة.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d76ec6ac928228011f42355bebd553576bcfd275
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255435"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="60c83-103">إضافة مهمة سابقة إلى نشاط تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="60c83-103">Add a predecessor to a production flow activity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60c83-104">في إصدار تدفق الإنتاج، يجب أن تكون كافة الأنشطة متسلسلة.</span><span class="sxs-lookup"><span data-stu-id="60c83-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="60c83-105">بإمكان نشاط واحد أن يتضمن عدة مهام سابقة أو لاحقة.</span><span class="sxs-lookup"><span data-stu-id="60c83-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="60c83-106">يوضح هذا الإجراء كيفية إقران مهمة سابقة بنشاط.</span><span class="sxs-lookup"><span data-stu-id="60c83-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="60c83-107">لتنفيذ هذه المهمة، إنك تحتاج إلى تدفق إنتاج لديه إصدار "مسودة" مع نشاطين على الأقل يمكن توصيلهما.</span><span class="sxs-lookup"><span data-stu-id="60c83-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="60c83-108">لمعرفة المزيد، اقرأ المستند التقنين "تدفقات الإنتاج والأنشطة في lean manufacturing".</span><span class="sxs-lookup"><span data-stu-id="60c83-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="60c83-109">البحث عن تدفق الإنتاج والإصدار</span><span class="sxs-lookup"><span data-stu-id="60c83-109">Find the production flow and version</span></span>
1. <span data-ttu-id="60c83-110">انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="60c83-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="60c83-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="60c83-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="60c83-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="60c83-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="60c83-113">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="60c83-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="60c83-114">انقر فوق "الأنشطة".</span><span class="sxs-lookup"><span data-stu-id="60c83-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="60c83-115">تحديد نشاط وإضافة عنصر سابق</span><span class="sxs-lookup"><span data-stu-id="60c83-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="60c83-116">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="60c83-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="60c83-117">انقر فوق "إضافة عنصر سابق".</span><span class="sxs-lookup"><span data-stu-id="60c83-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="60c83-118">في حقل "النشاط"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="60c83-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="60c83-119">في الحقل "نسبة زمن الدورة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="60c83-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="60c83-120">نسبة زمن الدورة الافتراضية لعلاقة نشاط هي 1.</span><span class="sxs-lookup"><span data-stu-id="60c83-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="60c83-121">هذا يفترض أن تشغيل النشاطين يتم بنفس الوتيرة أو الوقت اللازم لإنتاج وحدة من المنتج.</span><span class="sxs-lookup"><span data-stu-id="60c83-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="60c83-122">إذا تم تنفيذ المهمة السابقة بوتيرة أسرع (مستوى أدنى للوقت اللازم لإنتاج وحدة من المنتج)، فيجب أن تكون النسبة أقل من 1، وإذا تم تنفيذ المهمة السابقة بوتيرة أبطأ (مستوى أعلى للوقت اللازم لإنتاج وحدة من المنتج)، فإن نسبة زمن الدورة ستكون أكبر من 1.</span><span class="sxs-lookup"><span data-stu-id="60c83-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="60c83-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="60c83-123">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]