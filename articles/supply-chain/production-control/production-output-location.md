---
title: "موقع إخراج الإنتاج"
description: "يصف هذا الموضوع التدرج الهرمي الذي يتم استخدامه لتحديد موقع إخراج الإنتاج."
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e53c8e96579dba3b47bef0c00e55b8fa786fc55c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="production-output-location"></a><span data-ttu-id="f0b2b-103">موقع إخراج الإنتاج</span><span class="sxs-lookup"><span data-stu-id="f0b2b-103">Production output location</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f0b2b-104">يصف هذا الموضوع التدرج الهرمي الذي يتم استخدامه لتحديد موقع إخراج الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="f0b2b-105">موقع إخراج الإنتاج هو الموقع حيث يتم تخزين البضائع المنتهية أولاً بعد إنتاجها.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="f0b2b-106">عادة، يكون هذا الموقع قريبًا من عملية الإنتاج التي تنتج البضائع المنتهية.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="f0b2b-107">يتم استخدام موقع إخراج الإنتاج كمكان تخزين وسيط للمواد قبل نقلها إلى منطقة الشحن أو موقع تخزين موقع إدخال الإنتاج لعملية إنتاج نهائية، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="f0b2b-108">يتم تعيين موقع إخراج الإنتاج الافتراضي عند الإبلاغ عن البضائع المنتهية في أمر إنتاج أو أمر دفعي.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="f0b2b-109">يتم استخدام التدرج الهرمي التالي لتحديد موقع الإخراج هذا:</span><span class="sxs-lookup"><span data-stu-id="f0b2b-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="f0b2b-110">استخدم موقع الإخراج الذي تم تحديده في رأس أمر الإنتاج أو الأمر الدفعي.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="f0b2b-111">إذا لم يتم العثور على موقع هناك، فاستخدم موقع الإخراج الذي تم تحديده على المورد الذي استخدمته العملية الأخيرة التي تم تعريفها في مسار الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="f0b2b-112">إذا لم يتم العثور على موقع هناك، فاستخدم موقع الإخراج الذي تم تحديده على مجموعة الموارد التي استخدمها المورد للعملية الأخيرة التي تم تعريفها في مسار الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="f0b2b-113">إذا لم يتم العثور على موقع هناك، فاستخدم موقع الإخراج الذي تم تحديده في المستودع الذي تم تحديده لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="f0b2b-114">يتم تعيين موقع إخراج إنتاج افتراضي فقط للمنتجات التي تم إعدادها باستخدام عمليات المستودع المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="f0b2b-115">عندما يتم الإبلاغ عن نوع الصنف هذا كمنتهٍ، يتم إنشاء عمل مستودع من النوع **تخزين البضائع المنتهية‬** أو **تخزين منتج مساعد ومنتج ثانوي‬**.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="f0b2b-116">يستخدم نوع العمل هذا موقع إخراج الإنتاج كموقع انتقاء.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="f0b2b-117">يتحدد موقع التخزين بواسطة توجيهات الموقع.</span><span class="sxs-lookup"><span data-stu-id="f0b2b-117">The put-away location is determined by the location directives.</span></span>

