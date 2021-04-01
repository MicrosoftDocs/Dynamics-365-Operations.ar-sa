---
title: إنشاء أنظمة استحقاق
description: يوضح هذا الموضوع كيفية إنشاء نظام استحقاق.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c021f71735e63c270e8f1998d77d4e4abcc5506
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236687"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="bd8ab-103">إنشاء أنظمة استحقاق</span><span class="sxs-lookup"><span data-stu-id="bd8ab-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd8ab-104">يوضح هذا الموضوع كيفية إنشاء نظام استحقاق.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="bd8ab-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="bd8ab-106">انتقل إلى **جزء التنقل > الوحدات النمطية > دفتر الأستاذ العام > إعداد دفتر اليومية > أنظمة الاستحقاق**.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="bd8ab-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-107">Select **New**.</span></span>
3. <span data-ttu-id="bd8ab-108">في الحقل **هوية الاستحقاق**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="bd8ab-109">في الحقل **وصف نظام الاستحقاق**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="bd8ab-110">في الحقل **المدين**، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="bd8ab-111">سيحل الحساب الرئيسي المحدد محل الحساب الرئيسي المدين في بند إيصال دفتر اليومية وسيُستخدم أيضًا لعكس التأجيل استناداً إلى حركات استحقاق دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="bd8ab-112">في الحقل **الدائن**، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="bd8ab-113">سيحل الحساب الرئيسي المحدد محل الحساب الرئيسي الدائن في بند إيصال دفتر اليومية وسيُستخدم أيضًا لعكس التأجيل استناداً إلى حركات استحقاق دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="bd8ab-114">في الحقل **الإيصال**، حدد الطريقة التي تريد من خلالها تحديد الإيصال عند ترحيل الحركات.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="bd8ab-115">في الحقل **الوصف**، اكتب قيمة لوصف الحركات التي سيتم ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="bd8ab-116">في الحقل **تكرار الفترة**، حدد المعدل الذي يجب تكرار الحركات على أساسه.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="bd8ab-117">في الحقل **عدد التكرارات حسب الفترة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="bd8ab-118">في الحقل **ترحيل الحركات**، حدد معدل الوقت الذي ينبغي ترحيل الحركات على أساسه، مثل **شهريًا**.</span><span class="sxs-lookup"><span data-stu-id="bd8ab-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]