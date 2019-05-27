---
title: تعيين بُعد عنصر التكلفة
description: باستطاعة مراقب التكاليف استخدام هذا الإجراء لتعيين تكلفة بعد عنصر تكلفة إلى بعد عنصر تكلفة في الكيان القانوني MXMF.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52b9f6a5b71349d404fe9621b58f58aab843a71f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570683"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="22aec-103">تعيين بُعد عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="22aec-103">Map a cost element dimension</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22aec-104">باستطاعة مراقب التكاليف استخدام هذا الإجراء لتعيين تكلفة بعد عنصر تكلفة إلى بعد عنصر تكلفة في الكيان القانوني MXMF.</span><span class="sxs-lookup"><span data-stu-id="22aec-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="22aec-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="22aec-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="22aec-106">انتقل إلى محاسبة التكاليف > الأبعاد > أبعاد عنصر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="22aec-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="22aec-107">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="22aec-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="22aec-108">بالنسبة إلى هذا المثال، حدد "عناصر التكلفة".</span><span class="sxs-lookup"><span data-stu-id="22aec-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="22aec-109">انقر فوق "تعيينات الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="22aec-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="22aec-110">انقر فوق "تكوين التعيينات من هذا البُعد‬".</span><span class="sxs-lookup"><span data-stu-id="22aec-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="22aec-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="22aec-111">Click New.</span></span>
6. <span data-ttu-id="22aec-112">في الحقل "إلى البُعد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="22aec-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="22aec-113">بالنسبة إلى هذا المثال، حدد "عناصر التكلفة MXMF".</span><span class="sxs-lookup"><span data-stu-id="22aec-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="22aec-114">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="22aec-114">Click New.</span></span>
8. <span data-ttu-id="22aec-115">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="22aec-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="22aec-116">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="22aec-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="22aec-117">لهذا المثال، حدد عضو البعد 606400 مصروفات الهاتف والفاكس.</span><span class="sxs-lookup"><span data-stu-id="22aec-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="22aec-118">في الحقل "إلى عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="22aec-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="22aec-119">لهذا المثال، حدد عضو البعد 6001004 Telefono.</span><span class="sxs-lookup"><span data-stu-id="22aec-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="22aec-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="22aec-120">Click Save.</span></span>

