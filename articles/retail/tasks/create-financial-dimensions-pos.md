--- 
title: " إنشاء الأبعاد المالية لسجلات نقاط البيع وتكوين قيم الأبعاد في السجلات"
description: "يتناول هذا الإجراء إنشاء أبعاد مالية لسجلات نقطة البيع، ويوضح كيفية تكوين قيم الأبعاد المالية في السجلات."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 33e0b1da5d16372b8a3c4cd153f451166af6003f
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="b962d-103"> إنشاء الأبعاد المالية لسجلات نقاط البيع وتكوين قيم الأبعاد في السجلات</span><span class="sxs-lookup"><span data-stu-id="b962d-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b962d-104">يتناول هذا الإجراء إنشاء أبعاد مالية لسجلات نقطة البيع، ويوضح كيفية تكوين قيم الأبعاد المالية في السجلات.</span><span class="sxs-lookup"><span data-stu-id="b962d-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="b962d-105">لا يتضمن هذا الإجراء خطوات أخرى ذات صلة، مثل إنشاء مجموعات الأبعاد وبُنى الحسابات.</span><span class="sxs-lookup"><span data-stu-id="b962d-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="b962d-106">يمكن العثور على هذه المهام في مواضيع أخرى.</span><span class="sxs-lookup"><span data-stu-id="b962d-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="b962d-107">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="b962d-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="b962d-108">انتقل إلى دفتر الأستاذ العام > دليل الحسابات > الأبعاد > الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="b962d-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="b962d-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b962d-109">Click New.</span></span>
3. <span data-ttu-id="b962d-110">في حقل "‏‫استخدام القيم من‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="b962d-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="b962d-111">في حقل "‏‫اسم البُعد‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b962d-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="b962d-112">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="b962d-112">Click Activate.</span></span>
6. <span data-ttu-id="b962d-113">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="b962d-113">Click Close.</span></span>
7. <span data-ttu-id="b962d-114">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="b962d-114">Click Activate.</span></span>
8. <span data-ttu-id="b962d-115">انقر فوق "قيم الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="b962d-115">Click Dimension values.</span></span>
9. <span data-ttu-id="b962d-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b962d-116">Close the page.</span></span>
10. <span data-ttu-id="b962d-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b962d-117">Click Save.</span></span>
11. <span data-ttu-id="b962d-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b962d-118">Close the page.</span></span>
12. <span data-ttu-id="b962d-119">في AX7، انتقل إلى البيع بالتجزئة والتجارة > إعداد القناة > إعداد نقطة البيع > السجلات.</span><span class="sxs-lookup"><span data-stu-id="b962d-119">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="b962d-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b962d-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b962d-121">بدّل توسيع المقطع "الأبعاد المالية‬".</span><span class="sxs-lookup"><span data-stu-id="b962d-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="b962d-122">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="b962d-122">Click Edit.</span></span>
16. <span data-ttu-id="b962d-123">في حقل "الوحدة الطرفية"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="b962d-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="b962d-124">في القائمة، ابحث عن قيمة البُعد وحددها للسجل الذي يتم تحديثه.</span><span class="sxs-lookup"><span data-stu-id="b962d-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="b962d-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b962d-125">Click Save.</span></span>


