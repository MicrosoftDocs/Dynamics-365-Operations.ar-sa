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
ms.openlocfilehash: 457be741dfd3b44cb963db37857d6a7bceecc14e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994655"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="8f344-103">إنشاء أنظمة استحقاق</span><span class="sxs-lookup"><span data-stu-id="8f344-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f344-104">يوضح هذا الموضوع كيفية إنشاء نظام استحقاق.</span><span class="sxs-lookup"><span data-stu-id="8f344-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="8f344-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="8f344-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="8f344-106">انتقل إلى **جزء التنقل > الوحدات النمطية > دفتر الأستاذ العام > إعداد دفتر اليومية > أنظمة الاستحقاق**.</span><span class="sxs-lookup"><span data-stu-id="8f344-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="8f344-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8f344-107">Select **New**.</span></span>
3. <span data-ttu-id="8f344-108">في الحقل **هوية الاستحقاق**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8f344-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="8f344-109">في الحقل **وصف نظام الاستحقاق**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8f344-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="8f344-110">في الحقل **المدين**، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="8f344-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="8f344-111">سيحل الحساب الرئيسي المحدد محل الحساب الرئيسي المدين في بند إيصال دفتر اليومية وسيُستخدم أيضًا لعكس التأجيل استناداً إلى حركات استحقاق دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="8f344-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="8f344-112">في الحقل **الدائن**، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="8f344-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="8f344-113">سيحل الحساب الرئيسي المحدد محل الحساب الرئيسي الدائن في بند إيصال دفتر اليومية وسيُستخدم أيضًا لعكس التأجيل استناداً إلى حركات استحقاق دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="8f344-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="8f344-114">في الحقل **الإيصال**، حدد الطريقة التي تريد من خلالها تحديد الإيصال عند ترحيل الحركات.</span><span class="sxs-lookup"><span data-stu-id="8f344-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="8f344-115">في الحقل **الوصف**، اكتب قيمة لوصف الحركات التي سيتم ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="8f344-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="8f344-116">في الحقل **تكرار الفترة**، حدد المعدل الذي يجب تكرار الحركات على أساسه.</span><span class="sxs-lookup"><span data-stu-id="8f344-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="8f344-117">في الحقل **عدد التكرارات حسب الفترة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="8f344-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="8f344-118">في الحقل **ترحيل الحركات**، حدد معدل الوقت الذي ينبغي ترحيل الحركات على أساسه، مثل **شهريًا**.</span><span class="sxs-lookup"><span data-stu-id="8f344-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

