---
title: تتم معالجة الأوامر المؤكدة المشتقة مباشرة بواسطة سير عمل قيد المراجعة
description: تتم معالجة الأوامر المؤكدة المشتقة مباشرة بواسطة سير عمل يحتوي على حالة قيد المراجعة.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026243"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="7119a-103">تتم معالجة الأوامر المؤكدة المشتقة مباشرة بواسطة سير عمل قيد المراجعة</span><span class="sxs-lookup"><span data-stu-id="7119a-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="7119a-104">رقم KB: 4612450</span><span class="sxs-lookup"><span data-stu-id="7119a-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="7119a-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="7119a-105">Symptoms</span></span>

<span data-ttu-id="7119a-106">تتم معالجة الأوامر المؤكدة المشتقة مباشرة بواسطة سير عمل يحتوي على حالة *قيد المراجعة*.</span><span class="sxs-lookup"><span data-stu-id="7119a-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="7119a-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="7119a-107">Resolution</span></span>

<span data-ttu-id="7119a-108">عندما يتم تمكين تعقب تغيير الحالة، فإنه يتم تعيين حالة *قيد المراجعة* للأوامر المؤكدة المشتقة (أوامر الشراء الخاصة بالعقود من الباطن).</span><span class="sxs-lookup"><span data-stu-id="7119a-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="7119a-109">وبالتالي، إذا تم اشتقاق أمر شراء (وامر الشراء الخاصة بالعقود من الباطن)، يتم تقديمه فقط إلى سير عمل.</span><span class="sxs-lookup"><span data-stu-id="7119a-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="7119a-110">إذا كان أمر الشراء مؤكد ومخطط، فإنه يتم اعتماده تلقائيًا لضمان أن محرك التخطيط لا يقوم بإنشاء أوامر مخططة جديدة بينما لا يزال أمر الشراء في حالة *المسودة*.</span><span class="sxs-lookup"><span data-stu-id="7119a-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
