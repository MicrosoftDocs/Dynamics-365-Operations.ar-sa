---
title: تحديث حالة كانبان
description: عندما يتم إفراغ كانبان عن طريق الخطأ أو يحتاج كانبان المستلم إلى الإفراغ، فإنك تحتاج إلى تحديث حالة كانبان.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a0e03da4671ffec4ecf4835b20a00ef87971c94
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831796"
---
# <a name="update-kanban-status"></a><span data-ttu-id="cbd84-103">تحديث حالة كانبان</span><span class="sxs-lookup"><span data-stu-id="cbd84-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cbd84-104">عندما يتم إفراغ كانبان عن طريق الخطأ أو يحتاج كانبان المستلم إلى الإفراغ، فإنك تحتاج إلى تحديث حالة كانبان.</span><span class="sxs-lookup"><span data-stu-id="cbd84-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="cbd84-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="cbd84-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cbd84-106">هذا الإجراء مخصص لمشرف المتجر.</span><span class="sxs-lookup"><span data-stu-id="cbd84-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="cbd84-107">قم بإيجاد الكانبان.</span><span class="sxs-lookup"><span data-stu-id="cbd84-107">Find the kanban.</span></span>
1. <span data-ttu-id="cbd84-108">انتقل إلى التحكم بالإنتاج > كانبان > عمليات كانبان.</span><span class="sxs-lookup"><span data-stu-id="cbd84-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="cbd84-109">افتح عامل تصفية عمود وحدة معالجة المواد.</span><span class="sxs-lookup"><span data-stu-id="cbd84-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="cbd84-110">انقر فوق "مسح".</span><span class="sxs-lookup"><span data-stu-id="cbd84-110">Click Clear.</span></span>
    * <span data-ttu-id="cbd84-111">هذا يعيد تعيين عوامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="cbd84-111">This resets the filters.</span></span>  
4. <span data-ttu-id="cbd84-112">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="cbd84-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="cbd84-113">على سبيل المثال، قم بإجراء التصفية بالحقل "رقم البطاقة" باستخدام القيمة "000149".</span><span class="sxs-lookup"><span data-stu-id="cbd84-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="cbd84-114">تغيير حالة "مفرغة" إلى حالة "مستلمة"</span><span class="sxs-lookup"><span data-stu-id="cbd84-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="cbd84-115">انقر فوق "عكس وحدة معالجة مواد فارغة".</span><span class="sxs-lookup"><span data-stu-id="cbd84-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="cbd84-116">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cbd84-116">Click OK.</span></span>
    * <span data-ttu-id="cbd84-117">لاحظ أن حالة وحدة معالجة المواد هي "مستلم".</span><span class="sxs-lookup"><span data-stu-id="cbd84-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="cbd84-118">تغيير حالة "مستلمة" إلى حالة "مفرغة"</span><span class="sxs-lookup"><span data-stu-id="cbd84-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="cbd84-119">انقر فوق "كانبان فارغة".</span><span class="sxs-lookup"><span data-stu-id="cbd84-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="cbd84-120">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cbd84-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cbd84-121">لاحظ أن حالة وحدة معالجة المواد هي "مفرغ".</span><span class="sxs-lookup"><span data-stu-id="cbd84-121">Notice that the Handling unit status is Emptied.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]