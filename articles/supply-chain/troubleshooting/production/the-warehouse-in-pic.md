---
title: لا يتم تحديث المستودع الموجود في دفتر يومية قائمة الانتقاء في بند قائمة مكونات الصنف.
description: لا يتم تحديث المستودع الموجود في دفتر يومية قائمة الانتقاء في بند قائمة مكونات الصنف (BOM).
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026226"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a><span data-ttu-id="6f93f-103">لا يتم تحديث المستودع الموجود في دفتر يومية قائمة الانتقاء في بند قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="6f93f-103">The warehouse in the picking list journal isn't updated on a BOM line</span></span>

<span data-ttu-id="6f93f-104">رقم KB: 4614848</span><span class="sxs-lookup"><span data-stu-id="6f93f-104">KB number: 4614848</span></span>

## <a name="symptoms"></a><span data-ttu-id="6f93f-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="6f93f-105">Symptoms</span></span>

<span data-ttu-id="6f93f-106">لا يتم تحديث المستودع الموجود في دفتر يومية قائمة الانتقاء في بند قائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="6f93f-106">The warehouse in the picking list journal isn't updated on a bill of materials (BOM) line.</span></span>

## <a name="resolution"></a><span data-ttu-id="6f93f-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="6f93f-107">Resolution</span></span>

<span data-ttu-id="6f93f-108">يعمل النظام كما هو مصمم.</span><span class="sxs-lookup"><span data-stu-id="6f93f-108">The system is behaving as designed.</span></span> <span data-ttu-id="6f93f-109">في حالة إنشاء بند دفتر يومية قائمة الانتقاء الذي يحتوي على مرجع (بواسطة معرف الدفعة) إلى بند قائمة مكونات الصنف‬، لن يتم تحديث المستودع الموجود في بند قائمة مكونات الصنف‬ إذا تم تغيير بعد المستودع الموجود في بند دفتر يومية قائمة انتقاء الإنتاج في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="6f93f-109">If a picking list journal line is created that has a reference (via the lot ID) to a production BOM line, the warehouse on the production BOM line won't be updated if the warehouse dimension on the production picking list journal line is changed later.</span></span>
