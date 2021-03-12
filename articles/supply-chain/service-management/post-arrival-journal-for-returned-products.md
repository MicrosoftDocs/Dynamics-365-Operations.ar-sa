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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 184ce418ff2ec4b891a24b2b75d37b6b4f5d23f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006631"
---
# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="f6a41-103">ترحيل دفتر يومية وصول المنتجات المرتجعة</span><span class="sxs-lookup"><span data-stu-id="f6a41-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f6a41-104">لمعالجة إرجاع، يجب أولاً التحقق من كمية الإرجاع وتحديث حقل الكمية في دفتر يومية وصول الأصناف.</span><span class="sxs-lookup"><span data-stu-id="f6a41-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="f6a41-105">وبعد ذلك، حدد كود ترتيب أو قم بالإشارة إلى أنه يجب فحص أصناف الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="f6a41-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="f6a41-106">بعد استكمال هذه الخطوات، يمكنك ترحيل دفتر يومية وصول الصنف الخاص بأمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="f6a41-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="f6a41-107">انقر فوق **إدارة المخزون** \> **دوري** \> **نظرة عامة على الوصول**.</span><span class="sxs-lookup"><span data-stu-id="f6a41-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="f6a41-108">في عامل التصفية **اسم الإعداد**، حدد **أمر الإرجاع**.</span><span class="sxs-lookup"><span data-stu-id="f6a41-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="f6a41-109">إذا كانت قائمة عمليات الاستلام طويلة، فاستخدم الحقول الموجودة في المنطقة **النطاق** لتصغير القائمة.</span><span class="sxs-lookup"><span data-stu-id="f6a41-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="f6a41-110">حدد بند أمر الإرجاع المراد ترحيله، وحدد مربع **محدد للوصول‬** الخاص به، ثم انقر فوق **بدء الوصول**.</span><span class="sxs-lookup"><span data-stu-id="f6a41-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="f6a41-111">انقر فوق **دفاتر يومية** \> **إظهار عمليات الوصول من عمليات الاستلام** لفتح النموذج **دفتر يومية الموقع**.</span><span class="sxs-lookup"><span data-stu-id="f6a41-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="f6a41-112">لعرض معلومات مفصلة، حدد دفتر يومية، ثم انقر فوق <STRONG>البنود</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f6a41-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="f6a41-113">قم بإجراء أية تحديثات ضرورية، ثم انقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="f6a41-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="f6a41-114">بعد ترحيل دفتر اليومية، يتم تسجيل الأصناف المرتجعة في المخزون، ويشير النموذج **أوامر الإرجاع** إلى وصول الأصناف إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="f6a41-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6a41-115">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="f6a41-115">See also</span></span>

<span data-ttu-id="f6a41-116">[دفتر يومية الموقع (نموذج)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="f6a41-116">[Location journal (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span></span>

  


