---
title: الموافقة على الموردين لفئات تدبير معينة
description: عندما يتم إنشاء طلب شراء، قد يكون من الضروري تحديد مورّد مفضل أو معتمد، بحسب الطريقة التي تم بها إعداد سياسات الشراء.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b783d1ce8f02ad119dc6768e6d9cd3c61ae07e70
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566423"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="796ee-103">الموافقة على الموردين لفئات تدبير معينة</span><span class="sxs-lookup"><span data-stu-id="796ee-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="796ee-104">عندما يتم إنشاء طلب شراء، قد يكون من الضروري تحديد مورّد مفضل أو معتمد، بحسب الطريقة التي تم بها إعداد سياسات الشراء.</span><span class="sxs-lookup"><span data-stu-id="796ee-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="796ee-105">يوضح هذا الإجراء كيفية تحديد أحد المورّدين كمورّد مفضل أو معتمد لفئة تدبير معينة.</span><span class="sxs-lookup"><span data-stu-id="796ee-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="796ee-106">عادة ما يتم تنفيذ هذه المهمة بواسطة موظف تدبير محترف.</span><span class="sxs-lookup"><span data-stu-id="796ee-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="796ee-107">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="796ee-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="796ee-108">انتقل إلى ‏‫التدبير والتوريد > الموردون > جميع الموردين.</span><span class="sxs-lookup"><span data-stu-id="796ee-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="796ee-109">حدد المورّد الذي تريد تعيينه كمورّد مفضل أو معتمد لفئة ما.</span><span class="sxs-lookup"><span data-stu-id="796ee-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="796ee-110">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="796ee-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="796ee-111">انقر فوق "الفئات".</span><span class="sxs-lookup"><span data-stu-id="796ee-111">Click Categories.</span></span>
5. <span data-ttu-id="796ee-112">انقر فوق "إضافة فئة".</span><span class="sxs-lookup"><span data-stu-id="796ee-112">Click Add category.</span></span>
6. <span data-ttu-id="796ee-113">في حقل "الفئة"، حدد "أكسسوارات المكتب" (أكسسوارات المكتب).</span><span class="sxs-lookup"><span data-stu-id="796ee-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="796ee-114">في الحقل "حالة فئة المورد‬"، حدد "مفضل".</span><span class="sxs-lookup"><span data-stu-id="796ee-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="796ee-115">من الممكن تعيين أكثر من مورّد مفضل لفئة ما.</span><span class="sxs-lookup"><span data-stu-id="796ee-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="796ee-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="796ee-116">Click Save.</span></span>
9. <span data-ttu-id="796ee-117">انتقل إلى التدبير والتوريد > فئات التدبير.</span><span class="sxs-lookup"><span data-stu-id="796ee-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="796ee-118">في الشجرة، حدد "فئات التدبير للشركة/أكسسوارات المكتب".</span><span class="sxs-lookup"><span data-stu-id="796ee-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="796ee-119">قم بتوسيع مقطع "المورّدون".</span><span class="sxs-lookup"><span data-stu-id="796ee-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="796ee-120">تحقق من ظهور المورّد الذي قمت بتحديده كمورّد مفضل لفئة أكسسوارات المكتب.</span><span class="sxs-lookup"><span data-stu-id="796ee-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="796ee-121">إذا كنت تقوم بتشغيل هذا الإجراء كدليل مهمة، قد تضطر إلى النقر فوق الزر "إلغاء تأمين" لكي تتمكن من التمرير لأسفل إلى قائمة المورّدين.</span><span class="sxs-lookup"><span data-stu-id="796ee-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="796ee-122">من الممكن أيضًا إضافة مورّدين مفضلين ومورّدين معتمدين على هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="796ee-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="796ee-123">في الشجرة، قم بتوسيع "أكسسوارات المكتب".</span><span class="sxs-lookup"><span data-stu-id="796ee-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="796ee-124">في الشجرة ، حدد "المقصات".</span><span class="sxs-lookup"><span data-stu-id="796ee-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="796ee-125">حدد "لا" في الحقل "اكتساب المورّدين من الفئة الرئيسية:".</span><span class="sxs-lookup"><span data-stu-id="796ee-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="796ee-126">حدد "نعم" في الحقل "اكتساب المورّدين من الفئة الرئيسية:".</span><span class="sxs-lookup"><span data-stu-id="796ee-126">Select Yes in the Inherit vendors from parent category: field.</span></span>

