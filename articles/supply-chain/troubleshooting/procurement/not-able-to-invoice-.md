---
title: لا يمكن فوترة أمر مبيعات مخصص للعملاء
description: لم يعد بإمكانك فوترة أمر المبيعات الأصلي وأمر الشراء للتسليم المباشر الأصلي بعد تمكين الخيار ترحيل الفاتورة تلقائيًا.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026231"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="86404-103">لا يمكن فوترة أمر مبيعات مخصص للعملاء</span><span class="sxs-lookup"><span data-stu-id="86404-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="86404-104">رقم KB: 4611793</span><span class="sxs-lookup"><span data-stu-id="86404-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="86404-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="86404-105">Symptoms</span></span>

<span data-ttu-id="86404-106">لم يعد بإمكانك فوترة أمر المبيعات الأصلي وأمر الشراء للتسليم المباشر الأصلي بعد تمكين الخيار **ترحيل الفاتورة تلقائيًا** على الصفحة **بين شركات شقيقة** لمورد.</span><span class="sxs-lookup"><span data-stu-id="86404-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="86404-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="86404-107">Resolution</span></span>

<span data-ttu-id="86404-108">يتم التحكم في سلوك المزامنة الخاص بفواتير أمر التسليم بين الشركات الشقيقة والتسليم المباشر وفرضه بواسطة المعلمات الموضحة في [إعداد المحددات لترحيل أمر بين الشركات الشقيقة](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span><span class="sxs-lookup"><span data-stu-id="86404-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="86404-109">بعد تعيين تلك المعلمات، يجب أن تقوم بفوترة أمر مبيعات بين الشركات الشقيقة أولاً.</span><span class="sxs-lookup"><span data-stu-id="86404-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="86404-110">سيتم بعد ذلك مزامنة أوامر المبيعات وأوامر الشراء الأصلية.</span><span class="sxs-lookup"><span data-stu-id="86404-110">The original sales orders and purchase orders will then be synchronized.</span></span>
