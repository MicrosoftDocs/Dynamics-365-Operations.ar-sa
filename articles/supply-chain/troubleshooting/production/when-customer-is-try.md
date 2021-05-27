---
title: يتم مسح رقم الدفعة عند تحديد معرف شحنة جديد
description: عندما تقوم بمراجعة بند دفتر يومية قائمة الانتقاء، فإنه يتم مسح القيمة الموجودة في الحقل رقم الدفعة إذا قمت بتحديد قيمة جديدة في الحقل معرف الشحنة.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026220"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="b63d8-103">يتم مسح رقم الدفعة عند تحديد معرف شحنة جديد</span><span class="sxs-lookup"><span data-stu-id="b63d8-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="b63d8-104">رقم KB: 4613107</span><span class="sxs-lookup"><span data-stu-id="b63d8-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="b63d8-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="b63d8-105">Symptoms</span></span>

<span data-ttu-id="b63d8-106">عندما تقوم بمراجعة بند دفتر يومية قائمة الانتقاء، فإنه يتم مسح القيمة الموجودة في الحقل **رقد الدفعة** ذا قمت بتحديد قيمة جديدة في الحقل **معرف الشحنة**.</span><span class="sxs-lookup"><span data-stu-id="b63d8-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="b63d8-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="b63d8-107">Resolution</span></span>

<span data-ttu-id="b63d8-108">يعمل النظام كما هو مصمم.</span><span class="sxs-lookup"><span data-stu-id="b63d8-108">The system is behaving as designed.</span></span> <span data-ttu-id="b63d8-109">إذا قمت بتغيير معرف الشحنة، فإنك تقوم بتغيير سياق الصنف.</span><span class="sxs-lookup"><span data-stu-id="b63d8-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="b63d8-110">ولذلك، ييتم إعادة تعيين رقم الدفعة.</span><span class="sxs-lookup"><span data-stu-id="b63d8-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="b63d8-111">لربط رقم الدفعة بمعرف شحنة، يجب تعيين معرف الشحنة أولاً.</span><span class="sxs-lookup"><span data-stu-id="b63d8-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
