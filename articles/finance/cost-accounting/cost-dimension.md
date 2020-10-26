---
title: إنشاء الأبعاد واستيراد أعضاء الأبعاد
description: تعتبر محاسبة التكاليف وحدة نمطية مستقلة تحتاج إلى بيانات رئيسية من الوحدات النمطية الأخرى.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d61358be79adc943572bb4a5d624cb7c80b52e6e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977661"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="5ec96-103">إنشاء الأبعاد واستيراد أعضاء الأبعاد</span><span class="sxs-lookup"><span data-stu-id="5ec96-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ec96-104">تعتبر محاسبة التكاليف وحدة نمطية مستقلة تحتاج إلى بيانات من الوحدات النمطية الأخرى.</span><span class="sxs-lookup"><span data-stu-id="5ec96-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="5ec96-105">تم تصنيف هذه البيانات على الشكل التالي:</span><span class="sxs-lookup"><span data-stu-id="5ec96-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="5ec96-106">عناصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="5ec96-106">Cost elements</span></span>
-  <span data-ttu-id="5ec96-107">كائنات التكلفة</span><span class="sxs-lookup"><span data-stu-id="5ec96-107">Cost objects</span></span>
-  <span data-ttu-id="5ec96-108">الأبعاد الإحصائية</span><span class="sxs-lookup"><span data-stu-id="5ec96-108">Statistical dimensions</span></span>

<span data-ttu-id="5ec96-109">يتطابق **عنصر التكلفة** مع عنصر ذي صلة بالتكلفة في دليل الحسابات.</span><span class="sxs-lookup"><span data-stu-id="5ec96-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="5ec96-110">يتطابق **كائن التكلفة** مع أي نوع من أنواع الأبعاد المالية، مثل المنتجات ومراكز التكلفة والمشاريع التي تريدها لتقدير التكاليف أو توزيها أو قياسها مباشرة.</span><span class="sxs-lookup"><span data-stu-id="5ec96-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="5ec96-111">يتم استخدام **البُعد الإحصائي** وأعضاء هذا البُعد لتسجيل الإدخالات غير النقدية.</span><span class="sxs-lookup"><span data-stu-id="5ec96-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="5ec96-112">يمكن استخدام أعضاء الأبعاد الإحصائية كأساس تخصيص في توزيع التكلفة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="5ec96-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="5ec96-113">يوضح المخطط التالي الأبعاد المستخدمة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="5ec96-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="5ec96-114">[![أبعاد محاسبة التكاليف](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="5ec96-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="5ec96-115">بعد استيراد البيانات إلى محاسبة التكاليف، يمكنك استخدامها لإنشاء منظورات مختلفة توفر معلومات دقيقة إلى المدراء على جميع مستويات المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="5ec96-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="5ec96-116">توفر الموضوعات التالية معلومات حول إنشاء الأبعاد واستيراد أعضاء الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="5ec96-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="5ec96-117">أبعاد عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="5ec96-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="5ec96-118">إنشاء عناصر تكلفة</span><span class="sxs-lookup"><span data-stu-id="5ec96-118">Create cost elements</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="5ec96-119">أبعاد كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="5ec96-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="5ec96-120">تعيين أعضاء أبعاد عنصر التكلفة لمجموعة شائعة من أعضاء الأبعاد</span><span class="sxs-lookup"><span data-stu-id="5ec96-120">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="5ec96-121">تعيين بُعد عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="5ec96-121">Map a cost element dimension</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="5ec96-122">أعضاء الأبعاد الإحصائية وقوالب موفري القياسات الإحصائية​</span><span class="sxs-lookup"><span data-stu-id="5ec96-122">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)






