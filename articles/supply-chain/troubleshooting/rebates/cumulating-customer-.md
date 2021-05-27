---
title: يفشل تراكم خصومات العميل عند استخدام مجموعات الخصم للأصناف
description: عند استخدام اتفاقيات الخصم للعميل مع مجموعات خصم الصنف، يتم حساب الخصومات، ولكن يفشل التراكم.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026225"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="87fbe-103">يفشل تراكم خصومات العميل عند استخدام مجموعات الخصم للأصناف</span><span class="sxs-lookup"><span data-stu-id="87fbe-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="87fbe-104">رقم KB: 4611372</span><span class="sxs-lookup"><span data-stu-id="87fbe-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="87fbe-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="87fbe-105">Symptoms</span></span>

<span data-ttu-id="87fbe-106">عند استخدام اتفاقيات الخصم للعميل(لنوع *المبلغ*) مع مجموعات خصم الصنف، يتم حساب الخصومات، ولكن يفشل التراكم.</span><span class="sxs-lookup"><span data-stu-id="87fbe-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="87fbe-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="87fbe-107">Resolution</span></span>

<span data-ttu-id="87fbe-108">يعمل النظام كما هو مصمم.</span><span class="sxs-lookup"><span data-stu-id="87fbe-108">The system is behaving as designed.</span></span> <span data-ttu-id="87fbe-109">تقوم مجموعات الأصناف فقط بتجميع الأصناف التي لها نفس شرط الحد.</span><span class="sxs-lookup"><span data-stu-id="87fbe-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="87fbe-110">يتم تعيين شرط الخصم (الحد) مقابل المبلغ لكل صنف، وليس مقابل المبلغ المتراكم لأي صنف في مجموعة الصنف.</span><span class="sxs-lookup"><span data-stu-id="87fbe-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
