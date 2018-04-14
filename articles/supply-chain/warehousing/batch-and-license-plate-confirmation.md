---
title: "تأكيد لوحة الترخيص والدُفعة"
description: "يصف هذا الموضوع كيفية إعداد وتطبيق الدفعة وتأكيد لوحة الترخيص من جهاز محمول."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 90a45347cb5ed94259587024027eb8d1c4643fc6
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="47a2d-103">تأكيد لوحة الترخيص والدُفعة</span><span class="sxs-lookup"><span data-stu-id="47a2d-103">Batch and license plate confirmation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="47a2d-104">يسمح لك تأكيد الدفعة بالتأكيد على أن الدفعة الصحيحة تم انتقائها من الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="47a2d-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="47a2d-105">عند الانتقاء الأولي لعمل الدفعة أعلاه-الأصناف فقط، حيث تشير المجموعة أعلاه إلى أن نطاقات الدفعة أكبر من الموقع في التدرج الهرمي للبحث، فمن ثم يجب عليك التحقق من أن الدفعة التي يتم انتقاؤها تطابق الدفعة الموجودة في بند العمل.</span><span class="sxs-lookup"><span data-stu-id="47a2d-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="47a2d-106">يسمح لك تأكيد لوحة الترخيص بالتأكيد على أن لوحة الترخيص الصحيحة تم انتقائها من الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="47a2d-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="47a2d-107">عند اختيار العمل من موقع المرحلة، يجب عليك التحقق من أن لوحة الرخصة التي يتم انتقاؤها تطابق لوحة الترخيص المرتبطة بالعمل.</span><span class="sxs-lookup"><span data-stu-id="47a2d-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="47a2d-108">إذا تم بدء العمل من خلال المسح الضوئي للوحة الترخيص، فمن ثم يتم تخطي خطوة التأكيد هذه.</span><span class="sxs-lookup"><span data-stu-id="47a2d-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="47a2d-109">أين يتم التطبيق</span><span class="sxs-lookup"><span data-stu-id="47a2d-109">Where it applies</span></span>
<span data-ttu-id="47a2d-110">يتم تطبيق التأكيد في السيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="47a2d-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="47a2d-111">ينطبق تأكيد الدفعة على اختيارات العمل الأولية لأصناف الدفعة أعلاه.</span><span class="sxs-lookup"><span data-stu-id="47a2d-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="47a2d-112">ينطبق تأكيد لوحة الترخيص على عمليات الانتقاء من مواقع المرحلة.</span><span class="sxs-lookup"><span data-stu-id="47a2d-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="47a2d-113">إعداد الدفعة وتأكيد لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="47a2d-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="47a2d-114">يمكنك تكوين الدفعة وتأكيد لوحة الترخيص من عناصر قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="47a2d-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="47a2d-115">من عناصر قائمة الجهاز المحمول، قم بإدخال إعداد تأكيد العمل.</span><span class="sxs-lookup"><span data-stu-id="47a2d-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="47a2d-116">حدد الخيار إما للدفعة أو لتأكيد لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="47a2d-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="47a2d-117">يتوافر كل من الخيارين لعمليات انتقاء نوع العمل التي لم يتم تمكين التأكيد التلقائي لها.</span><span class="sxs-lookup"><span data-stu-id="47a2d-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  

