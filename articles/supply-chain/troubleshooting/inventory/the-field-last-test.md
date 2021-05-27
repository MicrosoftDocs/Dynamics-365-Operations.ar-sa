---
title: لم يتم تحديث حقل تاريخ الاختبار الأخير عند إنشاء أوامر الجودة المتعددة
description: لم يتم تحديث حقل تاريخ الاختبار الأخير عند إنشاء أوامر الجودة المتعددة.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026246"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="be125-103">لم يتم تحديث حقل تاريخ الاختبار الأخير عند إنشاء أوامر الجودة المتعددة</span><span class="sxs-lookup"><span data-stu-id="be125-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="be125-104">رقم KB: 4612803</span><span class="sxs-lookup"><span data-stu-id="be125-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="be125-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="be125-105">Symptoms</span></span>

<span data-ttu-id="be125-106">لم يتم تحديث حقل **تاريخ الاختبار الأخير** عند إنشاء أوامر الجودة المتعددة.</span><span class="sxs-lookup"><span data-stu-id="be125-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="be125-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="be125-107">Resolution</span></span>

<span data-ttu-id="be125-108">يعمل النظام كما هو مصمم.</span><span class="sxs-lookup"><span data-stu-id="be125-108">The system is behaving as designed.</span></span> <span data-ttu-id="be125-109">آخر تاريخ تم اختباره غير مرتبط بأوامر الجودة.</span><span class="sxs-lookup"><span data-stu-id="be125-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="be125-110">ويقوم بتخزين التاريخ الذي تم فيه شراء البضائع المنتهية لأول مرة أو تصنيعها.</span><span class="sxs-lookup"><span data-stu-id="be125-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="be125-111">يتم استخدام هذا التاريخ لحساب تاريخ إشعار الصلاحية لفترة الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="be125-111">This date is used to calculate the shelf life advice date.</span></span>
