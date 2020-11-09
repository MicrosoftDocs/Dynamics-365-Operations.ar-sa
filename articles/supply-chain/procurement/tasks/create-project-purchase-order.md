---
title: إنشاء أمر شراء المشروع
description: يوضح هذا الإجراء كيفية إنشاء أمر شراء للمشروع.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, PurchCreateOrder, PurchTable, PurchTablePart, InventItemIdLookupPurchase
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85079a843de02a8c8d5ae0ec291fa77464dd2dff
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018111"
---
# <a name="create-project-purchase-order"></a><span data-ttu-id="421af-103">إنشاء أمر شراء المشروع</span><span class="sxs-lookup"><span data-stu-id="421af-103">Create project purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="421af-104">يوضح هذا الإجراء كيفية إنشاء أمر شراء للمشروع.</span><span class="sxs-lookup"><span data-stu-id="421af-104">This procedure shows you how to create a project purchase order.</span></span> <span data-ttu-id="421af-105">تستخدم هذه المهمة مجموعة بيانات USSI.</span><span class="sxs-lookup"><span data-stu-id="421af-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="421af-106">انتقل إلى إدارة المشاريع والمحاسبة > المشاريع > جميع المشاريع.</span><span class="sxs-lookup"><span data-stu-id="421af-106">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="421af-107">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="421af-107">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="421af-108">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="421af-108">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="421af-109">انقر فوق مهمة الصنف.</span><span class="sxs-lookup"><span data-stu-id="421af-109">Click Item task.</span></span>
5. <span data-ttu-id="421af-110">انقر فوق "أمر الشراء".</span><span class="sxs-lookup"><span data-stu-id="421af-110">Click Purchase order.</span></span>
6. <span data-ttu-id="421af-111">في الحقل "حساب المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="421af-111">In the Vendor account field, enter or select a value.</span></span>
7. <span data-ttu-id="421af-112">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="421af-112">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="421af-113">هذه الخطوات ليست ضرورية، ولكنها تقوم بتبسيط أمر الشراء من خلال إعداد الموقع والمستودع الافتراضيين لبنود أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="421af-113">These steps aren't required, but they do simplify the purchase order by setting up a default site and warehouse for the purchase order lines.</span></span>  
8. <span data-ttu-id="421af-114">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="421af-114">In the Warehouse field, enter or select a value.</span></span>
9. <span data-ttu-id="421af-115">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="421af-115">Click OK.</span></span>
10. <span data-ttu-id="421af-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="421af-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="421af-117">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="421af-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="421af-118">قد يكون هذا رقم صنف أو فئة تدبير.</span><span class="sxs-lookup"><span data-stu-id="421af-118">This can be the item number or a procurement category.</span></span>  
12. <span data-ttu-id="421af-119">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="421af-119">Expand the Line details section.</span></span>
13. <span data-ttu-id="421af-120">انقر فوق علامة التبويب "المشروع".</span><span class="sxs-lookup"><span data-stu-id="421af-120">Click the Project tab.</span></span>
    * <span data-ttu-id="421af-121">تحقق من توفر أسعار المبيعات والتكلفة.</span><span class="sxs-lookup"><span data-stu-id="421af-121">Verify that the sales and cost prices are available.</span></span> <span data-ttu-id="421af-122">إذا لم تكن متاحة ولكن مطلوبة، فأدخل المعلومات.</span><span class="sxs-lookup"><span data-stu-id="421af-122">If they are not available but needed, enter the information.</span></span>  
14. <span data-ttu-id="421af-123">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="421af-123">Click Save.</span></span>

