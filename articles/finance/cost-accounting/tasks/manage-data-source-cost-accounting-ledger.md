---
title: إدارة مصدر بيانات لدفتر أستاذ محاسبة التكاليف
description: استخدم هذا الإجراء لإدارة مصدر بيانات دفتر الأستاذ العام لدفتر أستاذ محاسبة التكاليف.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7246d42b42404f0f1215bbf14b8ad168fe12691c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990707"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="b4984-103">إدارة مصدر بيانات لدفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="b4984-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4984-104">استخدم هذا الإجراء لإدارة مصدر بيانات دفتر الأستاذ العام لدفتر أستاذ محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="b4984-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="b4984-105">قبل إتمام هذه المهمة، احرص على تشغيل دلائل المهام "إنشاء دفتر أستاذ محاسبة التكاليف" و"تحديد وحدات التحكم بالتكاليف".</span><span class="sxs-lookup"><span data-stu-id="b4984-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="b4984-106">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="b4984-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="b4984-107">انتقل إلى محاسبة التكاليف > إعداد دفتر الأستاذ > دفاتر أستاذ محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="b4984-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="b4984-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b4984-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b4984-109">انقر فوق "الإصدارات الفعلية".</span><span class="sxs-lookup"><span data-stu-id="b4984-109">Click Actual versions.</span></span>
4. <span data-ttu-id="b4984-110">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="b4984-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="b4984-111">انقر فوق "دفتر الأستاذ العام".</span><span class="sxs-lookup"><span data-stu-id="b4984-111">Click General ledger.</span></span>
6. <span data-ttu-id="b4984-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b4984-112">Click New.</span></span>
7. <span data-ttu-id="b4984-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4984-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="b4984-114">في الحقل "موفر البيانات"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4984-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="b4984-115">لهذا المثال، حدد Dynamics 365 Finance - إدخالات دفتر الأستاذ العام .</span><span class="sxs-lookup"><span data-stu-id="b4984-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="b4984-116">في الحقل "بُعد عنصر التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b4984-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="b4984-117">بالنسبة إلى هذا المثال، حدد "عناصر التكلفة".</span><span class="sxs-lookup"><span data-stu-id="b4984-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="b4984-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b4984-118">Click Save.</span></span>
11. <span data-ttu-id="b4984-119">انقر فوق "تكوين موفر البيانات".</span><span class="sxs-lookup"><span data-stu-id="b4984-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="b4984-120">في الحقل "الكيان القانوني"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="b4984-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="b4984-121">في هذا المثال، حدد USP2.</span><span class="sxs-lookup"><span data-stu-id="b4984-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="b4984-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b4984-122">Click New.</span></span>
14. <span data-ttu-id="b4984-123">في حقل "طبقة الترحيل"، حدد "حالي".</span><span class="sxs-lookup"><span data-stu-id="b4984-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="b4984-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b4984-124">Click OK.</span></span>

