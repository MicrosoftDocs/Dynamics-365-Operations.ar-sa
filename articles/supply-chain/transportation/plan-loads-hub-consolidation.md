---
title: "تخطيط الأحمال باستخدام توحيد الموزِّعين"
description: "تصف هذه المقالة ميزة توحيد الشحنات في الموزّع عند تسليم بضائع من مستودعات مختلفة إلى العميل نفسه، أو عند استلام بضائع من مورّدين متعددين في المستودع نفسه."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 159410e7c1f04ee9a057c7d9dc9a2527c522b85b
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="plan-loads-using-hub-consolidation"></a><span data-ttu-id="6d1f5-103">تخطيط الأحمال باستخدام توحيد الموزِّعين</span><span class="sxs-lookup"><span data-stu-id="6d1f5-103">Plan loads using hub consolidation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="6d1f5-104">تصف هذه المقالة ميزة توحيد الشحنات في الموزّع عند تسليم بضائع من مستودعات مختلفة إلى العميل نفسه، أو عند استلام بضائع من مورّدين متعددين في المستودع نفسه.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="6d1f5-105">قد يكون من المفيد توحيد الشحنات في الموزّع عند تسليم بضائع من مستودعات مختلفة إلى العميل نفسه، أو عند تسليم بضائع من مورّدين متعددين إلى المستودع نفسه.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="6d1f5-106">إنشاء الأحمال</span><span class="sxs-lookup"><span data-stu-id="6d1f5-106">Building loads</span></span>
<span data-ttu-id="6d1f5-107">قبل استخدام خيار توحيد الموزِّعين، يجب تمكين الخيار **تخطيط الشحن بالطريق‬**في صفحة **محددات إدارة النقل**.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="6d1f5-108">ويجب أيضا إنشاء الموزِّعين في مكان حدوث التوحيد.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="6d1f5-109">يوضح الرسم التخطيطي التالي مثالاً لتوحيد الموزّعين.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="6d1f5-110">في هذه الحالة، ستنتقل أوامر المبيعات من مستودعات مختلفة إلى العميل نفسه.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="6d1f5-111">يتم إنشاء الأحمال الأساسية بالاستناد إلى أوامر المبيعات بالطريقة المعتادة، باستخدام صفحة **منضدة عمل تخطيط الحِمل‬**.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="6d1f5-112">لتوحيد حملين في الموزّع قبل أن يتم تسليمهما إلى العميل، في صفحة **منضدة عمل تخطيط الحِمل‬** في حقل **النقل**، حدد **توحيد الموزِّعين‬**.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="6d1f5-113">عند تحديد الموزّع الصحيح لكل حمل، سيكون الموزّع وجهة "تسليم" الأحمال.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="6d1f5-114">وسيتضمن أيضًا مقطع **العرض والطلب** في صفحة **منضدة عمل تخطيط الحمل** "بندي طلب نقل".</span><span class="sxs-lookup"><span data-stu-id="6d1f5-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="6d1f5-115">ويمكنك إضافة هذين البندين إلى حمل جديد.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="6d1f5-116">سيتضمن الحمل الجديد هذا بنود أمري المبيعات، وسيكون الموزّع عنوان "الالتقاط" والعميل A وجهة "التسليم".</span><span class="sxs-lookup"><span data-stu-id="6d1f5-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="6d1f5-117">وستكون الأحمال الثلاثة جاهزة عندئذٍ لتصنيفها وتوجيهها كأي حمل آخر.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="6d1f5-118">يمكنك تحديد أي من شركات الشحن التي يقترحها النظام لكل حمل.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="6d1f5-119">[![‏‫توحيد الموزِّعين](./media/hubconsol.jpg)](./media/hubconsol.jpg) يمكنك أيضًا استخدام نفس الأسلوب لتوحيد الأحمال لعدة أوامر نقل.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="6d1f5-120">في هذه الحالة، سيكون العميل ِA في الرسم التخطيطي السابق عبارة عن مستودع.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="6d1f5-121">أو، يمكنك توحيد الأحمال الخاصة بأوامر شراء متعددة، حيث يتم تسليم الأحمال من مورّدين مختلفين إلى المستودع نفسه.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="6d1f5-122">يمكن إنشاء أكثر من موزّع توحيد، ويمكنك إجراء التوحيد في عدة موزّعين لأحمال إضافية تأتي من مستودعات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="6d1f5-123">بعد إنشاء الأحمال الأساسية واستخدم خيار توحيد الموزّعين، يمكنك إنشاء أحمال جديدة باستخدام بنود طلب النقل الموحد.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="6d1f5-124">بعد ذلك، يمكنك تصنيف الأحمال وتوجيهها.</span><span class="sxs-lookup"><span data-stu-id="6d1f5-124">You then rate and route your loads.</span></span>




