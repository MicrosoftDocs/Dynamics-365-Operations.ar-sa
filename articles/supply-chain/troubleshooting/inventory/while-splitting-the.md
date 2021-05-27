---
title: عند تقسيم كمية وزن التعبئة، يتم استخدام الحد الأدنى للكمية بدلاً من الكمية الإسمية
description: عند تقسيم كمية التعبئة إلى مجموعات، فإن الحقل كمية الانتقاء يستخدم الحد الأدنى من الكمية المعينة للصنف، وليس الكمية الإسمية.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026244"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="a9f96-103">عند تقسيم كمية وزن التعبئة، يتم استخدام الحد الأدنى للكمية بدلاً من الكمية الإسمية</span><span class="sxs-lookup"><span data-stu-id="a9f96-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="a9f96-104">رقم KB: 4612073</span><span class="sxs-lookup"><span data-stu-id="a9f96-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="a9f96-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="a9f96-105">Symptoms</span></span>

<span data-ttu-id="a9f96-106">عند تقسيم كمية التعبئة إلى مجموعات، فإن الحقل **كمية الانتقاء** يستخدم الحد الأدنى من الكمية المعينة للصنف، وليس الكمية الإسمية.</span><span class="sxs-lookup"><span data-stu-id="a9f96-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="a9f96-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="a9f96-107">Resolution</span></span>

<span data-ttu-id="a9f96-108">يعمل النظام كما هو مصمم.</span><span class="sxs-lookup"><span data-stu-id="a9f96-108">The system is behaving as designed.</span></span> <span data-ttu-id="a9f96-109">يستخدم النظام إعداد الحد الأدنى لكمية كل صنف للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="a9f96-109">The system uses each item's minimum quantity setup for picking.</span></span>
