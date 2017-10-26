--- 
title: "إلغاء تنشيط إصدار تدفق الإنتاج"
description: "يمكنك إلغاء تنشيط إصدار تدفق الإنتاج عندما تنتفي الحاجة إليه."
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4a7eee6617e12d59a3d06207f5f6b58c93e28240
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="9bd3e-103">إلغاء تنشيط إصدار تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="9bd3e-103">Deactivate a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9bd3e-104">يمكنك إلغاء تنشيط إصدار تدفق الإنتاج عندما تنتفي الحاجة إليه.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="9bd3e-105">يجب استخدام هذا الخيار فقط إذا كانت كافة قواعد وأنشطة كانبان قد انتهت ولن يتم تنشيطها مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="9bd3e-106">لاحظ أنه سيتم تحديث تاريخ انتهاء صلاحية كافة قواعد كانبان المتعلقة بإصدار تدفق الإنتاج هذا بالتاريخ والوقت الحاليين.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="9bd3e-107">لتعديل إصدار تدفق إنتاج نشط، يمكنك تعيين تاريخ انتهاء صلاحية للإصدار النشط وإنشاء إصدار جديد.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="9bd3e-108">سيسمح لك هذا الأمر بمتابعة عمليات الإنتاج أثناء إعداد الإصدار الجديد وقواعد كانبان ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="9bd3e-109">لإنهاء صلاحية إصدار تدفق إنتاج نشط، تحتاج إلى تعيين تاريخ انتهاء صلاحية.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="9bd3e-110">وبهذا المعنى، يُعد إلغاء التنشيط بمثابة استثناء أكثر منه قاعدة.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="9bd3e-111">لتنفيذ هذا الإجراء تحتاج إلى تدفق إنتاج ذي إصدار يمكن إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="9bd3e-112">لا تحاول إجراء ذلك في بيئة إنتاج إلا إذا كنت متأكدًا 100% من أن هذا الإصدار قديم تمامًا.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="9bd3e-113">إلغاء تنشيط إصدار تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="9bd3e-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="9bd3e-114">انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="9bd3e-115">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9bd3e-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9bd3e-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9bd3e-118">انقر فوق "إلغاء تنشيط".</span><span class="sxs-lookup"><span data-stu-id="9bd3e-118">Click Deactivate.</span></span>
    * <span data-ttu-id="9bd3e-119">لا تتابع إذا لم تكن متأكدًا 100% من أن إصدار تدفق الإنتاج هذا عبارة عن إصدار مهمل.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="9bd3e-120">سيؤدي النقر فوق "موافق" إلى إنهاء صلاحية كافة قواعد كانبان النشطة وإيقاف كافة أنشطة الإنتاج والتزويد لإصدار تدفق الإنتاج هذا بشكل فوري.</span><span class="sxs-lookup"><span data-stu-id="9bd3e-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="9bd3e-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9bd3e-121">Click OK.</span></span>

