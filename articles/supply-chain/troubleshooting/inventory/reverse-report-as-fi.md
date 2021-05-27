---
title: يعمل إلغاء التقارير كمنته على إنشاء حركة مفتوحة غير متوقعة
description: يؤدي إلغاء الإبلاغ كمنته الذي يحتوي على علامة إلى إنشاء حركة مفتوحة حيث تكون الكمية المعكوسة هي نفس أبعاد المخزون الخاصة بالحركة المعكوسة.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026247"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="5db29-103">يعمل إلغاء التقارير كمنته على إنشاء حركة مفتوحة غير متوقعة</span><span class="sxs-lookup"><span data-stu-id="5db29-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="5db29-104">رقم KB: 4612469</span><span class="sxs-lookup"><span data-stu-id="5db29-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="5db29-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="5db29-105">Symptoms</span></span>

<span data-ttu-id="5db29-106">إذا قمت بعكس الإبلاغ كمنته الذي يحتوي على علامة، فإن النظام يعمل على إنشاء حركة مفتوحة حيث تكون الكمية المعكوسة هي نفس أبعاد المخزون الخاصة بالحركة المعكوسة.</span><span class="sxs-lookup"><span data-stu-id="5db29-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="5db29-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="5db29-107">Resolution</span></span>

<span data-ttu-id="5db29-108">عند عكس عملية تقرير كمنته، تتم تهيئة بُعد المخزون من دفتر يومية الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="5db29-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="5db29-109">ولذلك، يحصل على رقم الدفعة.</span><span class="sxs-lookup"><span data-stu-id="5db29-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="5db29-110">وبسبب التمييز، سترث حركات أمر المبيعات رقم الدفعة.</span><span class="sxs-lookup"><span data-stu-id="5db29-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="5db29-111">يمكن إعادة تعيين البُعد عند ترحيل الإبلاغ كمنته.</span><span class="sxs-lookup"><span data-stu-id="5db29-111">The dimension can be reset when the reporting as finished is posted.</span></span>
