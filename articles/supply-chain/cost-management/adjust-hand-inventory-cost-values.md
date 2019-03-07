---
title: تعديل قيم تكلفة المخزون الفعلي
description: استخدم صفحة تسوية المخزون الفعلي لتسوية قيمة التكلفة لكميات المخزون الفعلي بعد إجراء عملية إغلاق المخزون.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2417a278e58f4309873ab4d33b0d1f1686081951
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "335153"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="75fe8-103">تعديل قيم تكلفة المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="75fe8-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75fe8-104">استخدم صفحة تسوية المخزون الفعلي لتسوية قيمة التكلفة لكميات المخزون الفعلي بعد إجراء عملية إغلاق المخزون.</span><span class="sxs-lookup"><span data-stu-id="75fe8-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="75fe8-105">يمكنك استخدام صفحة **تسوية المخزون الفعلي** لتسوية قيمة التكلفة لكميات المخزون الفعلي بعد إجراء عملية إقفال المخزون.</span><span class="sxs-lookup"><span data-stu-id="75fe8-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="75fe8-106">**ملاحظة:** لفتح صفحة **تسوية المخزون الفعلي**، في صفحة **الإقفال والتسوية**، حدد سجل عملية إقفال مخزون مكتملة، ثم انقر فوق **‎تسوية** &gt; **فعلي**.</span><span class="sxs-lookup"><span data-stu-id="75fe8-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="75fe8-107">**مثال:** لديك الحركات التالية في فبراير:</span><span class="sxs-lookup"><span data-stu-id="75fe8-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="75fe8-108">1 فبراير: الإيصال المالي للمخزون لكمية قيمتها 2 بتكلفة مقدارها 10.00 دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="75fe8-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="75fe8-109">5 فبراير: الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 13.00 دولارًا أمريكيًا</span><span class="sxs-lookup"><span data-stu-id="75fe8-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="75fe8-110">19 فبراير: الإصدار المالي للمخزون لكمية مقدارها 1 بتكلفة متوسط تشغيل قدرها 11 دولارًا أمريكيًا</span><span class="sxs-lookup"><span data-stu-id="75fe8-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="75fe8-111">تم إعداد هذا الصنف بنموذج مخزون ما يرد أولاً يصرف أولاً FIFO، وتم إجراء غلق المخزون اعتبارًا من 28 فبراير.</span><span class="sxs-lookup"><span data-stu-id="75fe8-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="75fe8-112">ستتم تسوية حركة الإصدار المالية بمقدار 11 ريالاً سعوديًا مقابل الإيصال المالي بتاريخ 1 فبراير وسيتم إجراء تسوية مقدارها 1 ريال سعودي.</span><span class="sxs-lookup"><span data-stu-id="75fe8-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="75fe8-113">عندئذ سوف تحتوي إيصالات المخزون التالية على كميات مخزون مفتوحة:</span><span class="sxs-lookup"><span data-stu-id="75fe8-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="75fe8-114">1 فبراير: كمية مقدارها 1 بتكلفة 10.00 دولارات أمريكية</span><span class="sxs-lookup"><span data-stu-id="75fe8-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="75fe8-115">5 فبراير: كمية مقدارها 1 بتكلفة 13.00 دولارات أمريكية</span><span class="sxs-lookup"><span data-stu-id="75fe8-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="75fe8-116">لتعيين تكلفة هذين الصنفين إلى 15 ريالاً سعوديًا، استخدم خيار التسوية الفعلي لتسوية الكميات الفعلية المفتوحة اعتبارًا من فترة إغلاق المخزون الأخير.</span><span class="sxs-lookup"><span data-stu-id="75fe8-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="75fe8-117">**ملاحظة:** سيكون تاريخ ترحيل حركة التسوية الفعلية هو تاريخ إغلاق المخزون الأخير.</span><span class="sxs-lookup"><span data-stu-id="75fe8-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="75fe8-118">لا يمكن تعديل هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="75fe8-118">This date can't be modified.</span></span>
