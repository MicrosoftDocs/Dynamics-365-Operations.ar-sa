---
title: إنشاء أمر شراء المشروع
description: يوضح هذا الإجراء كيفية إنشاء أمر شراء للمشروع.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, PurchCreateOrder, PurchTable, PurchTablePart, InventItemIdLookupPurchase
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 825e374e9d450ee187e7ddb1ce5925c3d7e15f25
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016417"
---
# <a name="create-project-purchase-order"></a><span data-ttu-id="37c32-103">إنشاء أمر شراء المشروع</span><span class="sxs-lookup"><span data-stu-id="37c32-103">Create project purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37c32-104">يوضح هذا الإجراء كيفية إنشاء أمر شراء للمشروع.</span><span class="sxs-lookup"><span data-stu-id="37c32-104">This procedure shows you how to create a project purchase order.</span></span> <span data-ttu-id="37c32-105">تستخدم هذه المهمة مجموعة بيانات USSI.</span><span class="sxs-lookup"><span data-stu-id="37c32-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="37c32-106">انتقل إلى إدارة المشاريع والمحاسبة > المشاريع > جميع المشاريع.</span><span class="sxs-lookup"><span data-stu-id="37c32-106">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="37c32-107">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="37c32-107">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="37c32-108">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="37c32-108">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="37c32-109">انقر فوق مهمة الصنف.</span><span class="sxs-lookup"><span data-stu-id="37c32-109">Click Item task.</span></span>
5. <span data-ttu-id="37c32-110">انقر فوق "أمر الشراء".</span><span class="sxs-lookup"><span data-stu-id="37c32-110">Click Purchase order.</span></span>
6. <span data-ttu-id="37c32-111">في الحقل "حساب المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37c32-111">In the Vendor account field, enter or select a value.</span></span>
7. <span data-ttu-id="37c32-112">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37c32-112">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="37c32-113">هذه الخطوات ليست ضرورية، ولكنها تقوم بتبسيط أمر الشراء من خلال إعداد الموقع والمستودع الافتراضيين لبنود أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="37c32-113">These steps aren't required, but they do simplify the purchase order by setting up a default site and warehouse for the purchase order lines.</span></span>  
8. <span data-ttu-id="37c32-114">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37c32-114">In the Warehouse field, enter or select a value.</span></span>
9. <span data-ttu-id="37c32-115">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="37c32-115">Click OK.</span></span>
10. <span data-ttu-id="37c32-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="37c32-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="37c32-117">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37c32-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="37c32-118">قد يكون هذا رقم صنف أو فئة تدبير.</span><span class="sxs-lookup"><span data-stu-id="37c32-118">This can be the item number or a procurement category.</span></span>  
12. <span data-ttu-id="37c32-119">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="37c32-119">Expand the Line details section.</span></span>
13. <span data-ttu-id="37c32-120">انقر فوق علامة التبويب "المشروع".</span><span class="sxs-lookup"><span data-stu-id="37c32-120">Click the Project tab.</span></span>
    * <span data-ttu-id="37c32-121">تحقق من توفر أسعار المبيعات والتكلفة.</span><span class="sxs-lookup"><span data-stu-id="37c32-121">Verify that the sales and cost prices are available.</span></span> <span data-ttu-id="37c32-122">إذا لم تكن متاحة ولكن مطلوبة، فأدخل المعلومات.</span><span class="sxs-lookup"><span data-stu-id="37c32-122">If they are not available but needed, enter the information.</span></span>  
14. <span data-ttu-id="37c32-123">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="37c32-123">Click Save.</span></span>

