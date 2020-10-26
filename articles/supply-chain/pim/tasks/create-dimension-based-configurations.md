---
title: إنشاء التكوينات المستندة إلى أبعاد
description: يوضح هذا الإجراء كيفية تعريف تكوين لمنتج يستند إلى البعد.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c3e5cd2677480b14739f963cf4a74efaa7f2bd2a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986229"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="21173-103">إنشاء التكوينات المستندة إلى أبعاد</span><span class="sxs-lookup"><span data-stu-id="21173-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21173-104">يوضح هذا الإجراء كيفية تعريف تكوين لمنتج يستند إلى البعد.</span><span class="sxs-lookup"><span data-stu-id="21173-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="21173-105">وهذا هو الإجراء الأخير في السلسلة التي توضح كيفية إنشاء مجموعات للتكوين المستند إلى بُعد.</span><span class="sxs-lookup"><span data-stu-id="21173-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="21173-106">ويعتمد تنفيذ هذا الإجراء على البيانات التي تم إنشاؤها في التسجيلات السبعة السابقة.</span><span class="sxs-lookup"><span data-stu-id="21173-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="21173-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="21173-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="21173-108">إيجاد أصل منتج يستند إلى البعد</span><span class="sxs-lookup"><span data-stu-id="21173-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="21173-109">انقر فوق "صيانة المنتج الذي تم إصداره".</span><span class="sxs-lookup"><span data-stu-id="21173-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="21173-110">انقر فوق "المنتجات التي تم إصدارها".</span><span class="sxs-lookup"><span data-stu-id="21173-110">Click Released products.</span></span>
3. <span data-ttu-id="21173-111">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="21173-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="21173-112">حدد أصل المنتج المستند إلى البعد الذي قمت بإنشائه في التسجيل الأول في هذه السلسلة من التسجيلات الثمانية.</span><span class="sxs-lookup"><span data-stu-id="21173-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="21173-113">إنشاء التكوينات</span><span class="sxs-lookup"><span data-stu-id="21173-113">Create configurations</span></span>
1. <span data-ttu-id="21173-114">في جزء "الإجراءات الهندسية"، انقر فوق "الحفاظ على التكوينات".</span><span class="sxs-lookup"><span data-stu-id="21173-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="21173-115">انقر فوق "تكوين".</span><span class="sxs-lookup"><span data-stu-id="21173-115">Click Configure.</span></span>
3. <span data-ttu-id="21173-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="21173-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="21173-117">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="21173-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="21173-118">حدد أي من الأصناف في مجموعة التكوين الأولى.</span><span class="sxs-lookup"><span data-stu-id="21173-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="21173-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="21173-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="21173-120">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="21173-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="21173-121">حدد أي صنف من مجموعة التكوين الثاني.</span><span class="sxs-lookup"><span data-stu-id="21173-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="21173-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="21173-122">Click OK.</span></span>
8. <span data-ttu-id="21173-123">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="21173-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="21173-124">في حقل "التكوين"، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="21173-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="21173-125">أدخل اسم تكوين الذي سيجعل تحديد التكوين أمرًا سهلاً.</span><span class="sxs-lookup"><span data-stu-id="21173-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="21173-126">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="21173-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="21173-127">أدخل وصف التكوين لشرح محتواه.</span><span class="sxs-lookup"><span data-stu-id="21173-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="21173-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="21173-128">Click OK.</span></span>

