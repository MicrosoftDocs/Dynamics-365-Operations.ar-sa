--- 
title: "تحويل أصل ثابت"
description: "سيقوم دليل المهمة هذا بتحويل المعلومات المالية لدفتر أصل ثابت من مجموعة أبعاد مالية إلى مجموعة أبعاد مالية جديدة."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ea0e54dad6d8a48d628fc831b3fdbe7c0f68e892
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="8fca6-103">تحويل أصل ثابت</span><span class="sxs-lookup"><span data-stu-id="8fca6-103">Transfer a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8fca6-104">سيقوم دليل المهمة هذا بتحويل المعلومات المالية لدفتر أصل ثابت من مجموعة أبعاد مالية إلى مجموعة أبعاد مالية جديدة.</span><span class="sxs-lookup"><span data-stu-id="8fca6-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="8fca6-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="8fca6-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="8fca6-106">انتقل إلى الأصول الثابتة > الأصول الثابتة > الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="8fca6-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="8fca6-107">في القائمة، ابحث عن الأصل الثابت المراد تحويله وحدده.</span><span class="sxs-lookup"><span data-stu-id="8fca6-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="8fca6-108">في جزء الإجراءات، انقر فوق "أصل ثابت".</span><span class="sxs-lookup"><span data-stu-id="8fca6-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="8fca6-109">انقر فوق "تحويل الأصول الثابتة‬".</span><span class="sxs-lookup"><span data-stu-id="8fca6-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="8fca6-110">في حقل "‏‫تاريخ التحويل‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="8fca6-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="8fca6-111">أدخل التعليقات لوصف عملية التحويل.</span><span class="sxs-lookup"><span data-stu-id="8fca6-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="8fca6-112">تعرض هذه القائمة كافة الدفاتر للأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="8fca6-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="8fca6-113">ضع علامة على الدفاتر التي تريد تحويلها إلى مجموعة أبعاد مالية جديدة.</span><span class="sxs-lookup"><span data-stu-id="8fca6-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="8fca6-114">تعرض هذه القائمة قيم الأبعاد المالية الموجودة للدفتر المحدد.</span><span class="sxs-lookup"><span data-stu-id="8fca6-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="8fca6-115">حدد البعد المالي الذي تريد تحديثه لدفتر الأصل الثابت المحدد.</span><span class="sxs-lookup"><span data-stu-id="8fca6-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="8fca6-116">في الحقل "البُعد المالي‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8fca6-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="8fca6-117">عيّن قيم الأبعاد المالية الأخرى حسب الاقتضاء.</span><span class="sxs-lookup"><span data-stu-id="8fca6-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="8fca6-118">تتغيّر كافة قيم البعد المالي عند حدوث عملية تحويل، سواء تم إدخال قيمة أو تم تركها فارغة.</span><span class="sxs-lookup"><span data-stu-id="8fca6-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="8fca6-119">على سبيل المثال، إذا قمت بإدخال قيمة لوحدة الاعمال BusinessUnit وتركت الأبعاد المالية لكل من مركز التكلفة CostCenter والقسم فارغين.</span><span class="sxs-lookup"><span data-stu-id="8fca6-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="8fca6-120">إذا كانت بنية حسابك تسمح بالقيم الفارغة لكل من مركز التكلفة CostCenter والقسم، فإن التحويل يؤدي إلى احتواء كل نموذج قيمة لديه قيمة جديدة لوحدة الأعمال BusinessUnit وقيمة فارغة لمركز التكلفة CostCenter والقسم.</span><span class="sxs-lookup"><span data-stu-id="8fca6-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="8fca6-121">انقر فوق تحديث.</span><span class="sxs-lookup"><span data-stu-id="8fca6-121">Click Update.</span></span>
    * <span data-ttu-id="8fca6-122">لديك الفرصة لمعاينة التغييرات قبل إتمام عملية التحويل.</span><span class="sxs-lookup"><span data-stu-id="8fca6-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="8fca6-123">راجع النتائج قبل نقل نماذج دفاتر الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="8fca6-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="8fca6-124">انقر فوق التحويل.</span><span class="sxs-lookup"><span data-stu-id="8fca6-124">Click Transfer.</span></span>


