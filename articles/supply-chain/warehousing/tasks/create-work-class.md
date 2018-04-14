--- 
title: "إنشاء درجة عمل"
description: "يوضح هذا الإجراء كيفية إعداد فئة عمل."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 11e506c41eb5e8d5bd28db8e6d5ca51ff9e72a62
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-work-class"></a><span data-ttu-id="60ddd-103">إنشاء درجة عمل</span><span class="sxs-lookup"><span data-stu-id="60ddd-103">Create a work class</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60ddd-104">يوضح هذا الإجراء كيفية إعداد فئة عمل.</span><span class="sxs-lookup"><span data-stu-id="60ddd-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="60ddd-105">تُستخدم فئات العمل لتوجيه و/أو الحد من نوع بنود أوامر العمل التي يستطيع عامل مستودع معالجتها على جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="60ddd-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="60ddd-106">وتُحدد البنود التي يستطيع عامل معالجتها من فئات العمل بعناصر قائمة الجهاز المحمول التي يحق لعامل المستودع الوصول إليها وفئة العمل المحددة ببنود العمل.</span><span class="sxs-lookup"><span data-stu-id="60ddd-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that’s specified on the work lines.</span></span> <span data-ttu-id="60ddd-107">ويمكن استخدام فئات العمل أيضًا للتحقق من صحة موقع وضع بند أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="60ddd-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="60ddd-108">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="60ddd-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="60ddd-109">هذا الإجراء مخصص لمدير المستودعات.</span><span class="sxs-lookup"><span data-stu-id="60ddd-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="60ddd-110">انتقل إلى إدارة المستودعات > الإعداد > العمل > فئات العمل.</span><span class="sxs-lookup"><span data-stu-id="60ddd-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="60ddd-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="60ddd-111">Click New.</span></span>
3. <span data-ttu-id="60ddd-112">في الحقل "معرف فئة العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="60ddd-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="60ddd-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="60ddd-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="60ddd-114">في الحقل "نوع أمر العمل‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="60ddd-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="60ddd-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="60ddd-115">Click New.</span></span>
7. <span data-ttu-id="60ddd-116">في الحقل "نوع الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="60ddd-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="60ddd-117">إذا قمت بتحديد نوع موقع، سيؤدي هذا إلى تعيين قيد على المواقع التي يمكن وضع العناصر بها بعد اختيارها.</span><span class="sxs-lookup"><span data-stu-id="60ddd-117">If you select a location type, this sets a restriction on where items can be put after they’ve been picked.</span></span> <span data-ttu-id="60ddd-118">يُستخدم هذا الإعداد عندما يحاول توجيه موقع حل الموقع أو عندما يوفر عامل مستودع الموقع لعنصر قائمة الجهاز المحمول يدوياً.</span><span class="sxs-lookup"><span data-stu-id="60ddd-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="60ddd-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="60ddd-119">Close the page.</span></span>


