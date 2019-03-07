---
title: اقتراح عمليات الاستحواذ على الأصول الثابتة‬
description: يوضح هذا الإجراء كيفية الاستحواذ على أصل ثابت باستخدام مقترح الاستحواذ في دفتر يومية الأصول الثابتة.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1891206bb266b126eccfa789b8c8062c9bfa688b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "350632"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="3a39b-103">اقتراح عمليات الاستحواذ على الأصول الثابتة‬</span><span class="sxs-lookup"><span data-stu-id="3a39b-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a39b-104">يوضح هذا الإجراء كيفية الاستحواذ على أصل ثابت باستخدام مقترح الاستحواذ في دفتر يومية الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="3a39b-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="3a39b-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="3a39b-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="3a39b-106">انتقل إلى الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬.</span><span class="sxs-lookup"><span data-stu-id="3a39b-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="3a39b-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a39b-107">Click New.</span></span>
3. <span data-ttu-id="3a39b-108">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a39b-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="3a39b-109">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="3a39b-109">Click Lines.</span></span>
5. <span data-ttu-id="3a39b-110">انقر فوق "المقترحات".</span><span class="sxs-lookup"><span data-stu-id="3a39b-110">Click Proposals.</span></span>
6. <span data-ttu-id="3a39b-111">انقر فوق "مقترح الاستحواذ‬".</span><span class="sxs-lookup"><span data-stu-id="3a39b-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="3a39b-112">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="3a39b-112">Click Filter.</span></span>
8. <span data-ttu-id="3a39b-113">انقر فوق "إعادة تعيين‬" لمسح القيم السابقة.</span><span class="sxs-lookup"><span data-stu-id="3a39b-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="3a39b-114">حدد صف رقم الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="3a39b-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="3a39b-115">في الحقل "المعايير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a39b-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="3a39b-116">عيّن المعايير المتبقية للأصول الثابتة التي تريد الاستحواذ عليها بواسطة هذا المقترح.</span><span class="sxs-lookup"><span data-stu-id="3a39b-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="3a39b-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3a39b-117">Click OK.</span></span>
12. <span data-ttu-id="3a39b-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3a39b-118">Click OK.</span></span>
    * <span data-ttu-id="3a39b-119">تحقق من بنود الحركة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="3a39b-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="3a39b-120">سيتضمن مقترح الاستحواذ فقط الأصول الثابتة ذات تاريخ استحواذ وسعر استحواذ تم تعيينهما على الدفتر.</span><span class="sxs-lookup"><span data-stu-id="3a39b-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="3a39b-121">انقر فوق علامة التبويب "الدفاتر".</span><span class="sxs-lookup"><span data-stu-id="3a39b-121">Click the Books tab.</span></span>
14. <span data-ttu-id="3a39b-122">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="3a39b-122">Click Post.</span></span>

