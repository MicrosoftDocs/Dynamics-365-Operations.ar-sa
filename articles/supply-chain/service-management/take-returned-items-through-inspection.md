---
title: أخذ الأصناف المرتجعة عبر الفحص
description: أخذ الأصناف المرتجعة عبر الفحص.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f30937eb44893a3cb3587d072b685a855b0ecd3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224896"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="adcbe-103">أخذ الأصناف المرتجعة عبر الفحص</span><span class="sxs-lookup"><span data-stu-id="adcbe-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="adcbe-104">‏‫انقر فوق **‏‫إدارة المخزون‬** \> **دوري** \> **إدارة الجودة** \>‏‫ **أوامر إدخال مخزن الفحص**.</span><span class="sxs-lookup"><span data-stu-id="adcbe-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="adcbe-105">تحديد موقع بند الأمر المطابق للصنف المرجع الجاري فحصه.</span><span class="sxs-lookup"><span data-stu-id="adcbe-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="adcbe-106">يمكن أن يقترن أمر إدخال مخزن العزل برقم صنف وحيد فقط.</span><span class="sxs-lookup"><span data-stu-id="adcbe-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="adcbe-107">إذا تم إرجاع 10 أصناف لديها أرقام صنف مختلفة في شحنة واحدة وتم إرسالها إلى أمر إدخال مخزن العزل، سيتم إنشاء 10 أوامر فردية لإدخال مخزن العزل.</span><span class="sxs-lookup"><span data-stu-id="adcbe-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="adcbe-108">بعد إجراء فحص الصنف، قم بالتحديد في الحقل **رمز الإرجاع** للإشارة إلى ما يجب عمله مع الصنف وكيفية التعامل مع الحركات المالية المتصلة.</span><span class="sxs-lookup"><span data-stu-id="adcbe-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="adcbe-109">تشتمل الأمثلة على إرجاع الصنف إلى المخزن وإعادة تمويل العميل وتخريد الصنف وإرسال بديل إلى العميل أو إرجاع الصنف إلى العميل بدون ائتمان.</span><span class="sxs-lookup"><span data-stu-id="adcbe-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="adcbe-110">إذا تعذر تعيين رمز الإرجاع نفسه إلى عدة أصناف مرجعة في مجموعة أرقام صنف واحد، فسينبغي عليك تقسيم أمر إدخال مخزن الفحص‬ (<STRONG>الوظائف</STRONG> &gt; <STRONG>تقسيم</STRONG>) لتعيين رمز إرجاع مختلف لكل مجموعة فرعية.</span><span class="sxs-lookup"><span data-stu-id="adcbe-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="adcbe-111">عند الانتهاء من الفحص، انقر فوق **‏‫الإبلاغ كمنته‬** لإصدار الأصناف المرجعة وإنشاء دفتر يومية الوصول لصنف.</span><span class="sxs-lookup"><span data-stu-id="adcbe-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="adcbe-112">سيتولى الشخص أو القسم الذي يتسلم الأصناف معالجة دفتر اليومية للأصناف المراد إرجاعها إلى المخزن.</span><span class="sxs-lookup"><span data-stu-id="adcbe-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="adcbe-113">–أو –</span><span class="sxs-lookup"><span data-stu-id="adcbe-113">–or–</span></span>
    
    <span data-ttu-id="adcbe-114">قم بإنهاء أمر الإدخال ونقل الأصناف إلى المخزن مباشرةً باستخدام أحد وظائف **المخزون**.</span><span class="sxs-lookup"><span data-stu-id="adcbe-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="adcbe-115">أغلق النموذج لحفظ التغييرات.</span><span class="sxs-lookup"><span data-stu-id="adcbe-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="adcbe-116">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="adcbe-116">See also</span></span>

[<span data-ttu-id="adcbe-117">تحديد كيفية التخلص من الأصناف المرتجعة</span><span class="sxs-lookup"><span data-stu-id="adcbe-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]