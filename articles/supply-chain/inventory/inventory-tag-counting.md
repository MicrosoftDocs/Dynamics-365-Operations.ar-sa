---
title: جرد علامات المخزون
description: توفر هذا الموضوع معلومات حول جرد العلامات‬، الذي تستخدمه لمقارنة المحتويات الفعلية للمستودع بالمخزون الفعلي.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd10c24045fae5db00e88f3b84d4dea7b2c82c37
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571083"
---
# <a name="inventory-tag-counting"></a><span data-ttu-id="820e8-103">جرد علامات المخزون</span><span class="sxs-lookup"><span data-stu-id="820e8-103">Inventory tag counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="820e8-104">توفر هذا الموضوع معلومات حول جرد العلامات‬، الذي تستخدمه لمقارنة المحتويات الفعلية للمستودع بالمخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="820e8-104">This topic provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="820e8-105">‏‫عن طريق إنشاء بنود في صفحة **جرد العلامات**، ضع رقم علامة على كل صنف مخزون، مثل رقم من 1 إلى 500.</span><span class="sxs-lookup"><span data-stu-id="820e8-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="820e8-106">وأثناء الجرد، يمكنك إدخال رقم الصنف والكمية في علامة مناظرة.‬</span><span class="sxs-lookup"><span data-stu-id="820e8-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="820e8-107">ويمكن بعد ذلك استخدام هذه العلامة كأساس للإدخال في دفتر يومية جرد العلامات.</span><span class="sxs-lookup"><span data-stu-id="820e8-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="820e8-108">وبعد ترحيل دفتر يومية جرد العلامات، يتم إنشاء دفتر يومية جرد جديد في صفحة **الجرد**.</span><span class="sxs-lookup"><span data-stu-id="820e8-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="820e8-109">ويستند دفتر اليومية الجديد إلى بنود دفتر يومية جرد العلامات الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="820e8-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="820e8-110">ولجرد الأصناف بالعلامات بواسطة بُعد مخزون محدد، حدد البُعد في صفحة **بُعد العرض** التي يتم عرضها عند إنشاء دفتر يومية جرد العلامات.</span><span class="sxs-lookup"><span data-stu-id="820e8-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="820e8-111">على سبيل المثال، لحساب عدد الأصناف الموجودة في مستودع معين، حدد خانة الاختيار **مستودع**.</span><span class="sxs-lookup"><span data-stu-id="820e8-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="820e8-112">إذا تم تحديد شريط التمرير **تأمين الأصناف أثناء الجرد** في صفحة **معلمات إدارة المخزون والمستودعات**، لا يمكن تحديث الأصناف فعلياً أثناء الجرد.</span><span class="sxs-lookup"><span data-stu-id="820e8-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="820e8-113">ومع ذلك، لا يتم تأمين الأصناف في دفاتر يومية جرد العلامات خلال عملية الجرد.</span><span class="sxs-lookup"><span data-stu-id="820e8-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="820e8-114">ولا يتم إنشاء حركات المخزون حتى يتم ترحيل ونقل بنود جرد العلامات إلى دفتر يومية جرد.</span><span class="sxs-lookup"><span data-stu-id="820e8-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="820e8-115">في حالة إدخال العلامات عشوائيًا وكنت ترغب في تحديد العلامات المفقودة، فانقر فوق رأس عمود **العلامة** لفرز البنود حسب العلامة.</span><span class="sxs-lookup"><span data-stu-id="820e8-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="820e8-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="820e8-116">Additional resources</span></span>

[<span data-ttu-id="820e8-117">الجرد الدوري</span><span class="sxs-lookup"><span data-stu-id="820e8-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)
