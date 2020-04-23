---
title: ترحيل دفتر يومية وصول المنتجات المرتجعة
description: ترحيل دفتر يومية وصول المنتجات المرتجعة.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c96f1499cf9ef93a56a636f990aa5d0d183f9627
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202113"
---
# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="df8c8-103">ترحيل دفتر يومية وصول المنتجات المرتجعة</span><span class="sxs-lookup"><span data-stu-id="df8c8-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="df8c8-104">لمعالجة إرجاع، يجب أولاً التحقق من كمية الإرجاع وتحديث حقل الكمية في دفتر يومية وصول الأصناف.</span><span class="sxs-lookup"><span data-stu-id="df8c8-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="df8c8-105">وبعد ذلك، حدد كود ترتيب أو قم بالإشارة إلى أنه يجب فحص أصناف الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="df8c8-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="df8c8-106">بعد استكمال هذه الخطوات، يمكنك ترحيل دفتر يومية وصول الصنف الخاص بأمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="df8c8-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="df8c8-107">انقر فوق **إدارة المخزون** \> **دوري** \> **نظرة عامة على الوصول**.</span><span class="sxs-lookup"><span data-stu-id="df8c8-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="df8c8-108">في عامل التصفية**اسم الإعداد**، حدد **أمر الإرجاع**.</span><span class="sxs-lookup"><span data-stu-id="df8c8-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="df8c8-109">إذا كانت قائمة عمليات الاستلام طويلة، فاستخدم الحقول الموجودة في المنطقة **النطاق** لتصغير القائمة.</span><span class="sxs-lookup"><span data-stu-id="df8c8-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="df8c8-110">حدد بند أمر الإرجاع المراد ترحيله، وحدد مربع **محدد للوصول‬** الخاص به، ثم انقر فوق **بدء الوصول**.</span><span class="sxs-lookup"><span data-stu-id="df8c8-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="df8c8-111">انقر فوق **دفاتر يومية** \> **إظهار عمليات الوصول من عمليات الاستلام** لفتح النموذج **دفتر يومية الموقع**.</span><span class="sxs-lookup"><span data-stu-id="df8c8-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="df8c8-112">لعرض معلومات مفصلة، حدد دفتر يومية، ثم انقر فوق <STRONG>البنود</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="df8c8-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="df8c8-113">قم بإجراء أية تحديثات ضرورية، ثم انقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="df8c8-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="df8c8-114">بعد ترحيل دفتر اليومية، يتم تسجيل الأصناف المرتجعة في المخزون، ويشير النموذج **أوامر الإرجاع** إلى وصول الأصناف إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="df8c8-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="df8c8-115">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="df8c8-115">See also</span></span>

<span data-ttu-id="df8c8-116">[دفتر يومية الموقع (نموذج)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="df8c8-116">[Location journal (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span></span>

  


