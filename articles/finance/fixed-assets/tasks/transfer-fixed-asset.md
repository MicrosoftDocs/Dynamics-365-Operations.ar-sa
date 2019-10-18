---
title: تحويل أصل ثابت
description: سيقوم دليل المهمة هذا بتحويل المعلومات المالية لدفتر أصل ثابت من مجموعة أبعاد مالية إلى مجموعة أبعاد مالية جديدة.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 167591cf160916f256e2d10f122eca312ba07639
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186821"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="8c89f-103">تحويل أصل ثابت</span><span class="sxs-lookup"><span data-stu-id="8c89f-103">Transfer a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c89f-104">سيقوم دليل المهمة هذا بتحويل المعلومات المالية لدفتر أصل ثابت من مجموعة أبعاد مالية إلى مجموعة أبعاد مالية جديدة.</span><span class="sxs-lookup"><span data-stu-id="8c89f-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="8c89f-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="8c89f-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="8c89f-106">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > الأصول الثابتة > الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="8c89f-106">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="8c89f-107">في القائمة، ابحث عن الأصل الثابت المراد تحويله وحدده.</span><span class="sxs-lookup"><span data-stu-id="8c89f-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="8c89f-108">في جزء الإجراءات، انقر فوق **أصل ثابت**.</span><span class="sxs-lookup"><span data-stu-id="8c89f-108">On the Action Pane, click **Fixed asset**.</span></span>
4. <span data-ttu-id="8c89f-109">انقر فوق **تحويل الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="8c89f-109">Click **Transfer fixed assets**.</span></span>
5. <span data-ttu-id="8c89f-110">في حقل **‏‫تاريخ التحويل‬**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="8c89f-110">In the **Transfer date** field, enter a date.</span></span>
6. <span data-ttu-id="8c89f-111">أدخل التعليقات لوصف عملية التحويل.</span><span class="sxs-lookup"><span data-stu-id="8c89f-111">Enter comments to describe the transfer.</span></span>
    
    <span data-ttu-id="8c89f-112">تعرض هذه القائمة كافة الدفاتر للأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="8c89f-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="8c89f-113">ضع علامة على الدفاتر التي تريد تحويلها إلى مجموعة أبعاد مالية جديدة.</span><span class="sxs-lookup"><span data-stu-id="8c89f-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="8c89f-114">تعرض هذه القائمة قيم الأبعاد المالية الموجودة للدفتر المحدد.</span><span class="sxs-lookup"><span data-stu-id="8c89f-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="8c89f-115">حدد البعد المالي الذي تريد تحديثه لدفتر الأصل الثابت المحدد.</span><span class="sxs-lookup"><span data-stu-id="8c89f-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="8c89f-116">في الحقل **البُعد المالي‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8c89f-116">In the **Financial dimension** field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="8c89f-117">عيّن قيم الأبعاد المالية الأخرى حسب الاقتضاء.</span><span class="sxs-lookup"><span data-stu-id="8c89f-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="8c89f-118">تتغيّر كافة قيم البعد المالي عند حدوث عملية تحويل، سواء تم إدخال قيمة أو تم تركها فارغة.</span><span class="sxs-lookup"><span data-stu-id="8c89f-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="8c89f-119">على سبيل المثال، إذا قمت بإدخال قيمة لوحدة الاعمال BusinessUnit وتركت الأبعاد المالية لكل من مركز التكلفة CostCenter والقسم فارغين.</span><span class="sxs-lookup"><span data-stu-id="8c89f-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="8c89f-120">إذا كانت بنية حسابك تسمح بالقيم الفارغة لكل من مركز التكلفة CostCenter والقسم، فإن التحويل يؤدي إلى احتواء كل نموذج قيمة لديه قيمة جديدة لوحدة الأعمال BusinessUnit وقيمة فارغة لمركز التكلفة CostCenter والقسم.</span><span class="sxs-lookup"><span data-stu-id="8c89f-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="8c89f-121">انقر فوق **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="8c89f-121">Click **Update**.</span></span>
    * <span data-ttu-id="8c89f-122">لديك الفرصة لمعاينة التغييرات قبل إتمام عملية التحويل.</span><span class="sxs-lookup"><span data-stu-id="8c89f-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="8c89f-123">راجع النتائج قبل نقل نماذج دفاتر الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="8c89f-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="8c89f-124">انقر فوق **التحويل**.</span><span class="sxs-lookup"><span data-stu-id="8c89f-124">Click **Transfer**.</span></span>

