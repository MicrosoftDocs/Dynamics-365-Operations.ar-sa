---
title: استلام عمليات تسليم جزئية من الأصناف المرتجعة
description: يتم تحديد عمليات التسليم الجزئية كبنود أمر إرجاع، وليس شحنات أمر إرجاع.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e33096abc8e4fd84f5c3c53ce4f62db9e4e0f03
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211757"
---
# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="92c09-103">استلام عمليات تسليم جزئية من الأصناف المرتجعة</span><span class="sxs-lookup"><span data-stu-id="92c09-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="92c09-104">يتم تحديد عمليات التسليم الجزئية كبنود أمر إرجاع، وليس شحنات أمر إرجاع.</span><span class="sxs-lookup"><span data-stu-id="92c09-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="92c09-105">وهذا يعني أنه إذا تم استلام الكمية الكاملة الواردة في أحد بنود أمر الإرجاع، ولكنك لم تستلم أي شيء من البنود الأخرى في أمر الإرجاع، فلا يعتبر هذا تسليمًا جزئيًا.</span><span class="sxs-lookup"><span data-stu-id="92c09-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="92c09-106">لكن إذا كان بند أمر إرجاع يتطلب إرجاع عشر وحدات من صنف بعينه، ولكنك استلمت فقط أربع وحدات، فيعتبر ذلك تسليمًا جزئيًا.</span><span class="sxs-lookup"><span data-stu-id="92c09-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="92c09-107">إذا كانت شحنة إرجاع تحتوي على أقل من الكمية الكاملة لأحد بنود أمر الإرجاع، فإنه يمكن وضع الشحنة جانبًا وانتظار وصول باقي الكمية المرتجعة، أو يمكن تسجيل الكمية الجزئية وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="92c09-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="92c09-108">تسجيل كمية جزئية وترحيلها</span><span class="sxs-lookup"><span data-stu-id="92c09-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="92c09-109">بعد أن تحدد أمر إرجاع للوصول في النموذج **نظرة عامة على الوصول - المستودع: %1، الرصيف: %2, اسم دفتر اليومية: %3**، انقر فوق **بدء الوصول** لإنشاء دفتر يومية الوصول، ثم انقر فوق **دفاتر يومية** \> **إظهار عمليات الوصول من عمليات الاستلام** لفتح النموذج **دفتر يومية الموقع**.</span><span class="sxs-lookup"><span data-stu-id="92c09-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="92c09-110">حدد بند دفتر اليومية المطلوب العمل عليه، ثم انقر فوق **البنود** لفتح النموذج **بنود دفتر اليومية، المواقع**.</span><span class="sxs-lookup"><span data-stu-id="92c09-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="92c09-111">حدد بند رقم الصنف التي وصلت منه كمية جزئية فقط، ثم انقر فوق **الوظائف** \> **تقسيم** لفتح النموذج **تقسيم**.</span><span class="sxs-lookup"><span data-stu-id="92c09-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="92c09-112">في الحقل **تقسيم الكمية**، أدخل الكمية للعدد الإجمالي للأصناف التي تم استلامها، ثم انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="92c09-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="92c09-113">من النموذج **بنود دفتر اليومية، المواقع**، حدد بند كمية الأصناف التي وصلت، ثم انقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="92c09-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="92c09-114">يمكن ترحيل بند الكمية الإضافية بعدما تصل الأصناف.</span><span class="sxs-lookup"><span data-stu-id="92c09-114">You can post the line for the additional quantity after the items have arrived.</span></span>




