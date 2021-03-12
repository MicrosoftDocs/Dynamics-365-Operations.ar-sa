---
title: إعداد أكواد الترتيب
description: يمكنك إعداد رموز إرجاع لتحديد كيفية معالجة صنف مرتجع من عميل.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnDispositionCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 518b70223b2f6bf86809ccce77a2cf67c30e4168
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977528"
---
# <a name="set-up-disposition-codes"></a><span data-ttu-id="e09f5-103">إعداد أكواد الترتيب</span><span class="sxs-lookup"><span data-stu-id="e09f5-103">Set up disposition codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e09f5-104">يمكنك إعداد رموز إرجاع لتحديد كيفية معالجة صنف مرتجع من عميل.</span><span class="sxs-lookup"><span data-stu-id="e09f5-104">You can set up disposition codes to specify how to process an item that is returned by a customer.</span></span> <span data-ttu-id="e09f5-105">على سبيل المثال، قم بإنشاء كود ترتيب باسم **إصلاح وإرجاع** للإشارة إلى أن الصنف المرتجع سيتم إصلاحه وإرجاعه إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="e09f5-105">For example, create a disposition code named **Repair and return** to indicate that the returned item will be repaired and then returned to the customer.</span></span> <span data-ttu-id="e09f5-106">لمعرفة أمثلة حول أكواد الإرجاع التي تُستخدم عادةً للأصناف المرتجعة من العملاء، راجع [‏‫تحديد كيفية التخلص من الأصناف المرتجعة‬](specify-how-to-dispose-of-returned-items.md).</span><span class="sxs-lookup"><span data-stu-id="e09f5-106">For more examples of disposition codes that are typically used for items that are returned by customers, see [Specify how to dispose of returned items](specify-how-to-dispose-of-returned-items.md).</span></span>

<span data-ttu-id="e09f5-107">كما يمكنك إعداد كود سبب للمساعدة في تفسير سبب إرجاع صنف ما.</span><span class="sxs-lookup"><span data-stu-id="e09f5-107">You can also set up a reason code to help explain why an item was returned.</span></span> <span data-ttu-id="e09f5-108">للحصول على مزيد من المعلومات حول أكواد الأسباب، راجع [إعداد أكواد سبب الإرجاع](set-up-return-reason-code.md).</span><span class="sxs-lookup"><span data-stu-id="e09f5-108">For more information about reason codes, see [Set up return reason codes](set-up-return-reason-code.md).</span></span>

1.  <span data-ttu-id="e09f5-109">انقر فوق **‏‫المبيعات والتسويق‬** \> **إعداد** \> **‏‫‏‫أوامر المبيعات**‬ \> **المرتجعات** \> **رموز الإرجاع**.</span><span class="sxs-lookup"><span data-stu-id="e09f5-109">Click **Sales and marketing** \> **Setup** \> **Sales orders** \> **Returns** \> **Disposition codes**.</span></span>

2.  <span data-ttu-id="e09f5-110">انقر فوق **جديد** أو اضغط على CTRL+N لإنشاء كود ترتيب جديد.</span><span class="sxs-lookup"><span data-stu-id="e09f5-110">Click **New** or press CTRL+N to create a new disposition code.</span></span>

3.  <span data-ttu-id="e09f5-111">أدخل اسمًا وصفيًا فريدًا، وحدد إجراءً، ثم أدخل وصفًا لكود الترتيب.</span><span class="sxs-lookup"><span data-stu-id="e09f5-111">Enter a unique, descriptive name, select an action, and enter a description for the disposition code.</span></span>

4.  <span data-ttu-id="e09f5-112">إذا كنت ترغب في ربط أية مصاريف عميل برمز الإرجاع هذا، فانقر فوق الزر **المصاريف** لفتح النموذج **إعداد المصاريف**.</span><span class="sxs-lookup"><span data-stu-id="e09f5-112">If you want to associate any customer charges with this disposition code, click the **Charges** button to open the **Set up charges** form.</span></span>

5.  <span data-ttu-id="e09f5-113">إذا كنت ترغب في تحديد أي رموز خارجية لمطابقتها برموز الإرجاع الخاصة بالشركة، فانقر فوق الزر **أكواد خارجية** لفتح النموذج **أكواد خارجية**.</span><span class="sxs-lookup"><span data-stu-id="e09f5-113">If you want to define any external codes to match with the company's own disposition codes, click the **External codes** button to open the **External codes** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="e09f5-114">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="e09f5-114">See also</span></span>

[<span data-ttu-id="e09f5-115">نظرة عامة على مرتجعات العميل</span><span class="sxs-lookup"><span data-stu-id="e09f5-115">Customer returns overview</span></span>](disposition-and-return-reason-codes.md)

<span data-ttu-id="e09f5-116">[أكواد الترتيب (نموذج)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="e09f5-116">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

<span data-ttu-id="e09f5-117">[المصاريف التلقائية (نموذج)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="e09f5-117">[Auto charges (form)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span></span>

<span data-ttu-id="e09f5-118">[الأكواد الخارجية (نموذج)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="e09f5-118">[External codes (form)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span></span>

  


