---
title: لا يتم تحديث الكمية في أمر إدخال مخزن الفحص الذي تم بدؤه عند تقسيم الأمر
description: عند إنشاء أمر الفحص ومحاولة تقسيمه، لا يتم تحديث كمية الأمر إلى الكمية المتبقية التي يتم تقسيمها.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026248"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="4e8e1-103">لا يتم تحديث الكمية في أمر إدخال مخزن الفحص الذي تم بدؤه عند تقسيم الأمر</span><span class="sxs-lookup"><span data-stu-id="4e8e1-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="4e8e1-104">رقم KB: 4613113</span><span class="sxs-lookup"><span data-stu-id="4e8e1-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="4e8e1-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="4e8e1-105">Symptoms</span></span>

<span data-ttu-id="4e8e1-106">عند إنشاء أمر الفحص ومحاولة تقسيمه، لا يتم تحديث كمية الأمر إلى الكمية المتبقية بعد التقسيم.</span><span class="sxs-lookup"><span data-stu-id="4e8e1-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="4e8e1-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="4e8e1-107">Resolution</span></span>

<span data-ttu-id="4e8e1-108">لا يقوم النظام بتغيير الكمية الأصلية من أمر فحص لضمان أنه يمكنك تعقب الكمية الأصلية التي تم إنشاؤها لأمر الفحص هذا.</span><span class="sxs-lookup"><span data-stu-id="4e8e1-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="4e8e1-109">ومع ذلك، يقوم النظام بتعقب الكمية التي تم تقسيمها من أحد أوامر الفحص.</span><span class="sxs-lookup"><span data-stu-id="4e8e1-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="4e8e1-110">لتنفيذ عملية التعقب هذه، يتم استخدام حقل قاعدة البيانات يسمي `QuantityThatHasSplitIntoOtherQuarantineOrders`</span><span class="sxs-lookup"><span data-stu-id="4e8e1-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="4e8e1-111">ومع ذلك، هذا الحقل غير مرئي في واجهة المستخدم (UI).</span><span class="sxs-lookup"><span data-stu-id="4e8e1-111">However, this field isn't visible in the user interface (UI).</span></span>
