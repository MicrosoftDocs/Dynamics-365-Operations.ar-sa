---
title: إدارة عمليات الفرز (نوفمبر 2016)
description: يوضح هذا الإجراء كيفية إنشاء ونشر فرز منتجات جديدة، وهو يستخدم شركة بيانات العرض التوضيحي USRT.‬
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailCategoryAndProductWorkspace, RetailCategoryAndProductAssortment, RetailAssortmentDetails, RetailOperatingUnitPicker, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f96c79558c3248406a1b5988f9c9dc9783db4406
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564329"
---
# <a name="manage-assortments-november-2016"></a><span data-ttu-id="d6289-103">إدارة عمليات الفرز (نوفمبر 2016)</span><span class="sxs-lookup"><span data-stu-id="d6289-103">Manage assortments (November 2016)</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d6289-104">يوضح هذا الإجراء كيفية إنشاء ونشر فرز منتجات جديدة، وهو يستخدم شركة بيانات العرض التوضيحي USRT.‬</span><span class="sxs-lookup"><span data-stu-id="d6289-104">This procedure demonstrates how to create and publish a new product assortment and uses the demo data company USRT.</span></span> <span data-ttu-id="d6289-105">يتطلب هذا الإجراء الإصدار 7.0.1 أو أحدث من تطبيق Dynamics AX والإصدار 7.1 من النظام الأساسي Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="d6289-105">This procedure requires Dynamics AX application 7.0.1 or later, and Dynamics AX platform 7.1.</span></span>  

1. <span data-ttu-id="d6289-106">انقر فوق "إدارة الفئات والمنتجات".</span><span class="sxs-lookup"><span data-stu-id="d6289-106">Click Category and product management.</span></span>

## <a name="create-an-assortment"></a><span data-ttu-id="d6289-107">إنشاء تصنيف</span><span class="sxs-lookup"><span data-stu-id="d6289-107">Create an assortment</span></span>
1. <span data-ttu-id="d6289-108">انقر فوق علامة التبويب "عمليات الفرز".</span><span class="sxs-lookup"><span data-stu-id="d6289-108">Click the Assortments tab.</span></span>
2. <span data-ttu-id="d6289-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d6289-109">Click New.</span></span>
3. <span data-ttu-id="d6289-110">انقر فوق "فرز".</span><span class="sxs-lookup"><span data-stu-id="d6289-110">Click Assortment.</span></span>
    * <span data-ttu-id="d6289-111">يُعد معرف التصنيف مطلوبًا ويجب أن يكون قيمة فريدة.</span><span class="sxs-lookup"><span data-stu-id="d6289-111">The Assortment ID is required and must be a unique value.</span></span>  
4. <span data-ttu-id="d6289-112">في الحقل "اسم التصنيف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d6289-112">In the Assortment name field, type a value.</span></span>
5. <span data-ttu-id="d6289-113">في الحقل "تاريخ السريان"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="d6289-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="d6289-114">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً.</span><span class="sxs-lookup"><span data-stu-id="d6289-114">In the Expiration date field, enter a date.</span></span>
7. <span data-ttu-id="d6289-115">قم بتوسيع قسم قنوات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="d6289-115">Expand the Retail channels section.</span></span>
8. <span data-ttu-id="d6289-116">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="d6289-116">Click Add line.</span></span>
9. <span data-ttu-id="d6289-117">في الشجرة، حدد 'Contoso Retail\Electronics\Boston'.</span><span class="sxs-lookup"><span data-stu-id="d6289-117">In the tree, select 'Contoso Retail\Electronics\Boston'.</span></span>
10. <span data-ttu-id="d6289-118">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="d6289-118">Click Add.</span></span>
11. <span data-ttu-id="d6289-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d6289-119">Click OK.</span></span>
12. <span data-ttu-id="d6289-120">قم بتوسيع قسم "المنتجات".</span><span class="sxs-lookup"><span data-stu-id="d6289-120">Expand the Products section.</span></span>
13. <span data-ttu-id="d6289-121">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="d6289-121">Click Add line.</span></span>
14. <span data-ttu-id="d6289-122">في حقل "الفئة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d6289-122">In the Category field, enter or select a value.</span></span>
15. <span data-ttu-id="d6289-123">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d6289-123">Click Save.</span></span>

## <a name="publish-an-assortment"></a><span data-ttu-id="d6289-124">نشر تصنيف</span><span class="sxs-lookup"><span data-stu-id="d6289-124">Publish an assortment</span></span>
1. <span data-ttu-id="d6289-125">انقر فوق "نشر".</span><span class="sxs-lookup"><span data-stu-id="d6289-125">Click Publish.</span></span>
2. <span data-ttu-id="d6289-126">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="d6289-126">Click Yes.</span></span>

