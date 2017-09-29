---
title: "تجميع النظام في قائمة عمل مفتوح‬"
description: "يصف هذا الموضوع كيفية تصفية قائمة العمل المفتوح‬ على جهاز محمول."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0c68d544fec985f325e6472203533f23948cc9b4
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="9882c-103">تجميع النظام في قائمة عمل مفتوح‬</span><span class="sxs-lookup"><span data-stu-id="9882c-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9882c-104">باستخدام حقل تجميع النظام، يمكنك تصفية قائمة عمل مفتوح دون الحاجة إلى تحرير عنصر قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="9882c-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="9882c-105">حيث ينطبق الأمر، يعمل تجميع نظام لتصفية قائمة عمل على حقل رأس عمل واحد.</span><span class="sxs-lookup"><span data-stu-id="9882c-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="9882c-106">لا يمكنك استخدام تجميع النظام للتصفية على حقول على مستوى البنود.</span><span class="sxs-lookup"><span data-stu-id="9882c-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="9882c-107">إعداد تجميع النظام في قائمة عمل مفتوح</span><span class="sxs-lookup"><span data-stu-id="9882c-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="9882c-108">استخدم هذه الخطوات لإعداد تجميع النظام في قائمة عمل مفتوح.</span><span class="sxs-lookup"><span data-stu-id="9882c-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="9882c-109">من عنصر قائمة جهاز محمول، حدد **وضع: غير مباشر** و**كود النشاط‬: عرض قائمة العمل المفتوح**.</span><span class="sxs-lookup"><span data-stu-id="9882c-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="9882c-110">يتوفر الخياران التاليان:</span><span class="sxs-lookup"><span data-stu-id="9882c-110">The following options become available.</span></span> <span data-ttu-id="9882c-111">هذان الخياران مطلوبان لتجميع النظام في قائمة عمل مفتوح.</span><span class="sxs-lookup"><span data-stu-id="9882c-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="9882c-112">الخيار</span><span class="sxs-lookup"><span data-stu-id="9882c-112">Option</span></span>        | <span data-ttu-id="9882c-113">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="9882c-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="9882c-114">السماح بتجميع النظام</span><span class="sxs-lookup"><span data-stu-id="9882c-114">Allow system grouping</span></span>   | <span data-ttu-id="9882c-115">لتمكين تجميع النظام لعنصر قائمة عمل محدد.</span><span class="sxs-lookup"><span data-stu-id="9882c-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="9882c-116">حقل تجميع النظام</span><span class="sxs-lookup"><span data-stu-id="9882c-116">System grouping field</span></span>   | <span data-ttu-id="9882c-117">يتوفر فقط عند تعيين **السماح بعمل النظام** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="9882c-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="9882c-118">حدد الحقل الذي يحدد كيفية تجميع عمل الانتقاء للعاملين.</span><span class="sxs-lookup"><span data-stu-id="9882c-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="9882c-119">على سبيل المثال، إذا قمت بتحديد حقل **‏‫معرف الشحنة‬**، سيقوم العامل بفحص معرف الشحنة لتجميع عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9882c-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="9882c-120">ثم يتم تعيين جميع الأعمال للشحنة للعامل.</span><span class="sxs-lookup"><span data-stu-id="9882c-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="9882c-121">ويتطلب هذا الحقل إنشاء صنف قائمة لاستخدام العمل الموجود الذي يتم تجميعه بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="9882c-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="9882c-122">استخدم الحقل **تسمية تجميع النظام** لإعلام العامل بما يجب عليه فحصه.</span><span class="sxs-lookup"><span data-stu-id="9882c-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="9882c-123">بطاقة تجميع النظام</span><span class="sxs-lookup"><span data-stu-id="9882c-123">System grouping label</span></span>   | <span data-ttu-id="9882c-124">يتوفر فقط عند تعيين **السماح بعمل النظام** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="9882c-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="9882c-125">أدخل معلومات للعامل عما يجب عليه فحصه عندما يتم تجميع عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9882c-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="9882c-126">على سبيل المثال، إذا كنت تستخدم حقل **معرف الشحنة** لتجميع عمل الانتقاء بالشحنة، يمكنك إدخال معرف الشحنة في الحقل.</span><span class="sxs-lookup"><span data-stu-id="9882c-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="9882c-127">ويتطلب هذا الحقل إنشاء صنف قائمة لاستخدام العمل الموجود الذي يتم تجميعه بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="9882c-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="9882c-128">يجب أيضًا تحديد الحقل للتجميع بحسب في حقل **تجميع النظام**.</span><span class="sxs-lookup"><span data-stu-id="9882c-128">You must also select the field to group by in the **System grouping** field.</span></span>|

