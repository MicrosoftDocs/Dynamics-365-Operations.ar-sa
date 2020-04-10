---
title: إنشاء حركات استحقاق دفتر الأستاذ
description: يوضح دليل المهام هذا خطوات إنشاء حركات استحقاق دفتر الأستاذ التي تعتمد على أنظمة الاستحقاق.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2112336045086d0eb3b2fb0018f33631528a05ec
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145089"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="3e97c-103">إنشاء حركات استحقاق دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="3e97c-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e97c-104">يوضح دليل المهام هذا خطوات إنشاء حركات استحقاق دفتر الأستاذ التي تعتمد على أنظمة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="3e97c-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="3e97c-105">انتقل إلى دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة‬.</span><span class="sxs-lookup"><span data-stu-id="3e97c-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="3e97c-106">في القائم، ابحث عن دفتر اليومية المطلوب وحدده أو قم بإنشاء دفتر يومية جديد مطلوب.</span><span class="sxs-lookup"><span data-stu-id="3e97c-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="3e97c-107">انقر لمتابعة الارتباط الوارد في الحقل "رقم دفعة دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="3e97c-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="3e97c-108">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3e97c-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="3e97c-109">في حقل "الحساب"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3e97c-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="3e97c-110">في هذا المثال، نعرف المصروفات للتأمين.</span><span class="sxs-lookup"><span data-stu-id="3e97c-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="3e97c-111">وستصبح هذه المصروفات مبلغًا دوريًا من المصروفات.</span><span class="sxs-lookup"><span data-stu-id="3e97c-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="3e97c-112">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3e97c-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="3e97c-113">في الحقل "مدين"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3e97c-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="3e97c-114">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3e97c-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="3e97c-115">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="3e97c-115">Click Functions.</span></span>
10. <span data-ttu-id="3e97c-116">انقر فوق "استحقاقات دفتر الأستاذ".</span><span class="sxs-lookup"><span data-stu-id="3e97c-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="3e97c-117">في الحقل "معرف الاستحقاق"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="3e97c-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="3e97c-118">في القائمة، ابحث عن نظام الاستحقاق الذي تريد تطبيقه وحدده.</span><span class="sxs-lookup"><span data-stu-id="3e97c-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="3e97c-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3e97c-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="3e97c-120">في الحقل "تاريخ البدء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="3e97c-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="3e97c-121">انقر فوق "الحركات".</span><span class="sxs-lookup"><span data-stu-id="3e97c-121">Click Transactions.</span></span>
16. <span data-ttu-id="3e97c-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3e97c-122">Close the page.</span></span>
17. <span data-ttu-id="3e97c-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3e97c-123">Click OK.</span></span>
18. <span data-ttu-id="3e97c-124">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="3e97c-124">Click Post.</span></span>

