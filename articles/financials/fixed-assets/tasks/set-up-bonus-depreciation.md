---
title: إعداد إهلاك إضافي
description: يوضح هذا الإجراء كيفية إنشاء بدل إهلاك خاص وإقرانه بدفتر أصول ثابتة.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bbd6b78d05fcc9d95f6e6409db2619a210ad760
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "339201"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="1a045-103">إعداد إهلاك إضافي</span><span class="sxs-lookup"><span data-stu-id="1a045-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1a045-104">يوضح هذا الإجراء كيفية إنشاء بدل إهلاك خاص وإقرانه بدفتر أصول ثابتة.</span><span class="sxs-lookup"><span data-stu-id="1a045-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="1a045-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="1a045-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="1a045-106">إنشاء بدل إهلاك خاص</span><span class="sxs-lookup"><span data-stu-id="1a045-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="1a045-107">انتقل إلى الأصول الثابتة > إعداد > بدل الإهلاك الخاص.</span><span class="sxs-lookup"><span data-stu-id="1a045-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="1a045-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1a045-108">Click New.</span></span>
3. <span data-ttu-id="1a045-109">في الحقل "بدل الإهلاك الخاص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1a045-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="1a045-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1a045-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1a045-111">في الحقل "النسبة المئوية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1a045-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="1a045-112">إذا لم تتم الإشارة إلى نسبة مئوية، فعيّن مبلغًا.</span><span class="sxs-lookup"><span data-stu-id="1a045-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="1a045-113">إقران بدل إهلاك خاص بدفتر مجموعة الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="1a045-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="1a045-114">انتقل إلى الأصول الثابتة > إعداد > مجموعات الأصول الثابتة‬.</span><span class="sxs-lookup"><span data-stu-id="1a045-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="1a045-115">في القائمة، حدد مجموعة الأصول الثابتة المقترنة ببدل الإهلاك الخاص.</span><span class="sxs-lookup"><span data-stu-id="1a045-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="1a045-116">انقر فوق "الدفاتر".</span><span class="sxs-lookup"><span data-stu-id="1a045-116">Click Books.</span></span>
4. <span data-ttu-id="1a045-117">في القائمة، حدد الدفتر المقترن ببدل الإهلاك الخاص.</span><span class="sxs-lookup"><span data-stu-id="1a045-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="1a045-118">انقر فوق "بدل الإهلاك الخاص".</span><span class="sxs-lookup"><span data-stu-id="1a045-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="1a045-119">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1a045-119">Click New.</span></span>
7. <span data-ttu-id="1a045-120">في الحقل "بدل الإهلاك الخاص"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1a045-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="1a045-121">يأتي المبلغ الافتراضي لمبلغ النسبة المئوية من إعداد بدل الإهلاك الخاص.‬</span><span class="sxs-lookup"><span data-stu-id="1a045-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="1a045-122">في حقل "الأولوية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1a045-122">In the Priority field, enter a number.</span></span>

