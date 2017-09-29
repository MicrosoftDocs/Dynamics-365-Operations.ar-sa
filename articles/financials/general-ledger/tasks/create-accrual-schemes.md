--- 
title: "إنشاء أنظمة استحقاق"
description: "يوضح دليل المهام هذا خطوات إنشاء بنية نظام استحقاق."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 324be23a1e26de0d05c7cf6a61567f7260d0c390
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="bfa6b-103">إنشاء أنظمة استحقاق</span><span class="sxs-lookup"><span data-stu-id="bfa6b-103">Create accrual schemes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bfa6b-104">يوضح دليل المهام هذا خطوات إنشاء بنية نظام استحقاق.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="bfa6b-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="bfa6b-106">انتقل إلى دفتر الأستاذ العام > إعداد دفتر اليومية > أنظمة الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="bfa6b-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bfa6b-107">Click New.</span></span>
3. <span data-ttu-id="bfa6b-108">في الحقل "هوية الاستحقاق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="bfa6b-109">في الحقل "وصف نظام الاستحقاق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="bfa6b-110">في الحقل "المدين"، حدد القيم المرغوب فيها.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="bfa6b-111">سيحل الحساب الرئيسي المحدد محل الحساب الرئيسي المدين في بند إيصال دفتر اليومية وسيُستخدم أيضًا لعكس التأجيل استناداً إلى حركات استحقاق دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="bfa6b-112">في الحقل "الدائن"، حدد القيم المرغوب فيها.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="bfa6b-113">سيحل الحساب الرئيسي المحدد محل الحساب الرئيسي الدائن في بند إيصال دفتر اليومية وسيُستخدم أيضًا لعكس التأجيل استناداً إلى حركات استحقاق دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="bfa6b-114">في الحقل "الإيصال"، حدد الكيفية التي تريد تحديد الإيصال بها عند ترحيل الحركات.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="bfa6b-115">في الحقل "الوصف"، اكتب قيمة لوصف الحركات التي سيتم ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="bfa6b-116">في الحقل "تكرار الفترة"، حدد المعدل الذي يجب تكرار الحركات على أساسه.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="bfa6b-117">في الحقل "عدد التكرارات حسب الفترة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="bfa6b-118">في الحقل "ترحيل الحركات"، حدد معدل الوقت الذي ينبغي ترحيل الحركات على أساسه، مثل شهريًا.</span><span class="sxs-lookup"><span data-stu-id="bfa6b-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


