---
title: نسخ المنتجات المساعدة من إصدار معادلة موجودة
description: يوضح هذا الإجراء كيفية نسخ المنتجات المساعدة أو المنتجات الثانوية من إصدار معادلة حالية إلى إصدار معادلة مختلفة لمنتج صادر.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93742819f492c0c169a6ca8dc2d486fe35ec4a5c
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149333"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="8f892-103">نسخ المنتجات المساعدة من إصدار معادلة موجودة</span><span class="sxs-lookup"><span data-stu-id="8f892-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f892-104">يوضح هذا الإجراء كيفية نسخ المنتجات المساعدة أو المنتجات الثانوية من إصدار معادلة حالية إلى إصدار معادلة مختلفة لمنتج صادر.</span><span class="sxs-lookup"><span data-stu-id="8f892-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="8f892-105">إنه شرط مسبق أن يوجد إصدار معادلة واحدة على الأقل مقترنة بالمنتجات المساعدة.</span><span class="sxs-lookup"><span data-stu-id="8f892-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="8f892-106">يتم استخدام شركة بيانات العرض التوضيحي USP2 لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="8f892-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="8f892-107">البحث عن منتج صادر</span><span class="sxs-lookup"><span data-stu-id="8f892-107">Find a released product</span></span>
1. <span data-ttu-id="8f892-108">انتقل إلى "المنتجات الصادرة‬".</span><span class="sxs-lookup"><span data-stu-id="8f892-108">Go to Released products.</span></span>
2. <span data-ttu-id="8f892-109">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="8f892-109">Click Show filters.</span></span>
    * <span data-ttu-id="8f892-110">أنت على وشك إضافة نوع إنتاج الحقل في مربع حوار "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="8f892-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="8f892-111">انقر فوق حقل "إضافة عامل تصفية" لإضافة نوع إنتاج الحقل.</span><span class="sxs-lookup"><span data-stu-id="8f892-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="8f892-112">في الخطوة التالية، إنك بحاجة إلى إدخال معادلة في حقل نوع الإنتاج قبل تحديد "تطبيق" يدويًا.</span><span class="sxs-lookup"><span data-stu-id="8f892-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="8f892-113">وهذا يعمل على تعيين عامل التصفية على قائمة المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="8f892-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="8f892-114">أدخل المعادلة في حقل "نوع الإنتاج" يدويًا.</span><span class="sxs-lookup"><span data-stu-id="8f892-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="8f892-115">انقر فوق تطبيق.</span><span class="sxs-lookup"><span data-stu-id="8f892-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="8f892-116">حدد المنتج الصادر</span><span class="sxs-lookup"><span data-stu-id="8f892-116">Select a released product</span></span>
1. <span data-ttu-id="8f892-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="8f892-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="8f892-118">انقر على إصدارات المعادلة.</span><span class="sxs-lookup"><span data-stu-id="8f892-118">Click Formula versions.</span></span>
    * <span data-ttu-id="8f892-119">في جزء "الإجراءات الهندسية"، انقر فوق "إصدارات المعادلة".</span><span class="sxs-lookup"><span data-stu-id="8f892-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="8f892-120">نسخ منتجات مساعدة</span><span class="sxs-lookup"><span data-stu-id="8f892-120">Copy co-products</span></span>
1. <span data-ttu-id="8f892-121">في جزء "الإجراءات"، انقر فوق "إصدار المعادلة".</span><span class="sxs-lookup"><span data-stu-id="8f892-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="8f892-122">انقر فوق "‏‫المنتجات المساعدة‬".</span><span class="sxs-lookup"><span data-stu-id="8f892-122">Click Co-products.</span></span>
3. <span data-ttu-id="8f892-123">انقر فوق نسخ.</span><span class="sxs-lookup"><span data-stu-id="8f892-123">Click Copy.</span></span>
4. <span data-ttu-id="8f892-124">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f892-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="8f892-125">في حقل "إصدار المعادلة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8f892-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="8f892-126">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="8f892-126">Click OK.</span></span>
7. <span data-ttu-id="8f892-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8f892-127">Close the page.</span></span>

