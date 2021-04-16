---
title: الموافقة على الموردين لفئات تدبير محددة
description: يوضح هذا الموضوع كيفية الموافقة على المورّدين لفئات تدبير معينة في Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 887905c35c684f2f60c3ce17eb652532831193cc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812436"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="bd61f-103">الموافقة على الموردين لفئات تدبير محددة</span><span class="sxs-lookup"><span data-stu-id="bd61f-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd61f-104">يوضح هذا الموضوع كيفية الموافقة على المورّدين لفئات تدبير معينة في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bd61f-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="bd61f-105">عندما يتم إنشاء طلب شراء، قد يكون من الضروري تحديد مورّد مفضل أو معتمد، بحسب الطريقة التي تم بها إعداد سياسات الشراء.</span><span class="sxs-lookup"><span data-stu-id="bd61f-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="bd61f-106">يوضح هذا الإجراء كيفية تحديد أحد المورّدين كمورّد مفضل أو معتمد لفئة تدبير معينة.</span><span class="sxs-lookup"><span data-stu-id="bd61f-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="bd61f-107">عادة ما يتم تنفيذ هذه المهمة بواسطة موظف تدبير محترف.</span><span class="sxs-lookup"><span data-stu-id="bd61f-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="bd61f-108">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="bd61f-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="bd61f-109">في جزء التنقل، انتقل إلى **الوحدات النمطية > التدبير والتوريد > المورّدون‬ > كافة المورّدين‬**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="bd61f-110">حدد المورّد الذي تريد تعيينه كمورّد مفضل أو معتمد لفئة ما.</span><span class="sxs-lookup"><span data-stu-id="bd61f-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="bd61f-111">في جزء الإجراءات، حدد **عام**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="bd61f-112">حدد **الفئات**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-112">Select **Categories**.</span></span>
5. <span data-ttu-id="bd61f-113">حدد **إضافة فئة**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-113">Select **Add category**.</span></span>
6. <span data-ttu-id="bd61f-114">في حقل **الفئة**، حدد **أكسسوارات المكتب" (أكسسوارات المكتب)**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="bd61f-115">في الحقل **حالة فئة المورّد**، حدد **مفضل**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="bd61f-116">من الممكن تعيين أكثر من مورّد مفضل لفئة ما.</span><span class="sxs-lookup"><span data-stu-id="bd61f-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="bd61f-117">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-117">Select **Save**.</span></span>
9. <span data-ttu-id="bd61f-118">في جزء التنقل، انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد‬ > فئات التدبير‬**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="bd61f-119">في الشجرة، حدد **فئات التدبير للشركة\أكسسوارات المكتب**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="bd61f-120">قم بتوسيع قسم **المورّدون**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="bd61f-121">تحقق من ظهور المورّد الذي قمت بتحديده كمورّد مفضل لفئة أكسسوارات المكتب.</span><span class="sxs-lookup"><span data-stu-id="bd61f-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="bd61f-122">إذا كنت تقوم بتشغيل هذا الإجراء كدليل مهمة، قد تضطر إلى تحديد الزر **إلغاء تأمين** لكي تتمكن من التمرير لأسفل إلى قائمة المورّدين.</span><span class="sxs-lookup"><span data-stu-id="bd61f-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="bd61f-123">من الممكن أيضًا إضافة مورّدين مفضلين ومورّدين معتمدين على هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bd61f-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="bd61f-124">في الشجرة، قم بتوسيع **أكسسوارات المكتب** وحدد **المقصات**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="bd61f-125">حدد **لا** في الحقل **توارث المورّدين من الفئة الرئيسية:**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="bd61f-126">حدد **نعم** في الحقل **توارث المورّدين من الفئة الرئيسية:**.</span><span class="sxs-lookup"><span data-stu-id="bd61f-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]