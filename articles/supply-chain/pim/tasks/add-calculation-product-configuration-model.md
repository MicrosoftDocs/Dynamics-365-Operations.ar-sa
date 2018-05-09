--- 
title: "إضافة عملية حسابية إلى نموذج تكوين منتج"
description: "يوضح هذا الإجراء كيفية إضافة عملية حساب جديدة إلى نموذج تكوين منتج."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 123ae1315c95693af09d7d7c96a071d606ac98f8
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="d52ed-103">إضافة عملية حسابية إلى نموذج تكوين منتج</span><span class="sxs-lookup"><span data-stu-id="d52ed-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d52ed-104">يوضح هذا الإجراء كيفية إضافة عملية حساب جديدة إلى نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="d52ed-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="d52ed-105">ويُظهر كيف يمكنك إنشاء تعبير منطقي باستخدام العامل "لو" لتعيين ارتفاع مكبر الصوت إلى 10 لمكبرات الصوت البيضاء و15 لألوان الكابينات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="d52ed-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="d52ed-106">يستخدم الإجراء المكون مكبر الصوت المتطور في شركة العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="d52ed-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="d52ed-107">إضافة عملية حساب</span><span class="sxs-lookup"><span data-stu-id="d52ed-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="d52ed-108">إنشاء عملية تعبير حساب</span><span class="sxs-lookup"><span data-stu-id="d52ed-108">Create calculation expression</span></span>
1. <span data-ttu-id="d52ed-109">انقر فوق "تحرير التعبير".</span><span class="sxs-lookup"><span data-stu-id="d52ed-109">Click Edit expression.</span></span>
2. <span data-ttu-id="d52ed-110">في الحقل "ConstraintBody"، أدخل "If[CabinetFinish=="White", 10, 15]".</span><span class="sxs-lookup"><span data-stu-id="d52ed-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="d52ed-111">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="d52ed-111">Click Validate.</span></span>
4. <span data-ttu-id="d52ed-112">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="d52ed-112">Click Close.</span></span>
5. <span data-ttu-id="d52ed-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d52ed-113">Click OK.</span></span>


