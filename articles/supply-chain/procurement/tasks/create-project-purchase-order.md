---
title: إنشاء أمر شراء المشروع
description: يوضح هذا الإجراء كيفية إنشاء أمر شراء للمشروع.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, PurchCreateOrder, PurchTable, InventItemIdLookupPurchase
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 195fa23fc3d4f407ab82e1584fe870bfdd01c82a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838180"
---
# <a name="create-project-purchase-order"></a><span data-ttu-id="2bde3-103">إنشاء أمر شراء المشروع</span><span class="sxs-lookup"><span data-stu-id="2bde3-103">Create project purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2bde3-104">يوضح هذا الإجراء كيفية إنشاء أمر شراء للمشروع.</span><span class="sxs-lookup"><span data-stu-id="2bde3-104">This procedure shows you how to create a project purchase order.</span></span> <span data-ttu-id="2bde3-105">تستخدم هذه المهمة مجموعة بيانات USSI.</span><span class="sxs-lookup"><span data-stu-id="2bde3-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="2bde3-106">انتقل إلى إدارة المشاريع والمحاسبة > المشاريع > جميع المشاريع.</span><span class="sxs-lookup"><span data-stu-id="2bde3-106">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="2bde3-107">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2bde3-107">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="2bde3-108">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="2bde3-108">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="2bde3-109">انقر فوق مهمة الصنف.</span><span class="sxs-lookup"><span data-stu-id="2bde3-109">Click Item task.</span></span>
5. <span data-ttu-id="2bde3-110">انقر فوق "أمر الشراء".</span><span class="sxs-lookup"><span data-stu-id="2bde3-110">Click Purchase order.</span></span>
6. <span data-ttu-id="2bde3-111">في الحقل "حساب المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2bde3-111">In the Vendor account field, enter or select a value.</span></span>
7. <span data-ttu-id="2bde3-112">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2bde3-112">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="2bde3-113">هذه الخطوات ليست ضرورية، ولكنها تقوم بتبسيط أمر الشراء من خلال إعداد الموقع والمستودع الافتراضيين لبنود أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="2bde3-113">These steps aren't required, but they do simplify the purchase order by setting up a default site and warehouse for the purchase order lines.</span></span>  
8. <span data-ttu-id="2bde3-114">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2bde3-114">In the Warehouse field, enter or select a value.</span></span>
9. <span data-ttu-id="2bde3-115">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2bde3-115">Click OK.</span></span>
10. <span data-ttu-id="2bde3-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2bde3-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="2bde3-117">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2bde3-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2bde3-118">قد يكون هذا رقم صنف أو فئة تدبير.</span><span class="sxs-lookup"><span data-stu-id="2bde3-118">This can be the item number or a procurement category.</span></span>  
12. <span data-ttu-id="2bde3-119">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="2bde3-119">Expand the Line details section.</span></span>
13. <span data-ttu-id="2bde3-120">انقر فوق علامة التبويب "المشروع".</span><span class="sxs-lookup"><span data-stu-id="2bde3-120">Click the Project tab.</span></span>
    * <span data-ttu-id="2bde3-121">تحقق من توفر أسعار المبيعات والتكلفة.</span><span class="sxs-lookup"><span data-stu-id="2bde3-121">Verify that the sales and cost prices are available.</span></span> <span data-ttu-id="2bde3-122">إذا لم تكن متاحة ولكن مطلوبة، فأدخل المعلومات.</span><span class="sxs-lookup"><span data-stu-id="2bde3-122">If they are not available but needed, enter the information.</span></span>  
14. <span data-ttu-id="2bde3-123">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="2bde3-123">Click Save.</span></span>

