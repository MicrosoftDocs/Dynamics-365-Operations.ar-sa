---
title: تجميع النظام في قائمة عمل مفتوح‬
description: يصف هذا الموضوع كيفية تصفية قائمة العمل المفتوح‬ على جهاز محمول.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73e1da37c354eecf1ef5d44e68d814664fe2be99
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564777"
---
# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="20389-103">تجميع النظام في قائمة عمل مفتوح‬</span><span class="sxs-lookup"><span data-stu-id="20389-103">System grouping on an open work list</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20389-104">باستخدام حقل تجميع النظام، يمكنك تصفية قائمة عمل مفتوح دون الحاجة إلى تحرير عنصر قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="20389-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="20389-105">حيث ينطبق الأمر، يعمل تجميع نظام لتصفية قائمة عمل على حقل رأس عمل واحد.</span><span class="sxs-lookup"><span data-stu-id="20389-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="20389-106">لا يمكنك استخدام تجميع النظام للتصفية على حقول على مستوى البنود.</span><span class="sxs-lookup"><span data-stu-id="20389-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="20389-107">إعداد تجميع النظام في قائمة عمل مفتوح</span><span class="sxs-lookup"><span data-stu-id="20389-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="20389-108">استخدم هذه الخطوات لإعداد تجميع النظام في قائمة عمل مفتوح.</span><span class="sxs-lookup"><span data-stu-id="20389-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="20389-109">من عنصر قائمة جهاز محمول، حدد **وضع: غير مباشر** و**كود النشاط‬: عرض قائمة العمل المفتوح**.</span><span class="sxs-lookup"><span data-stu-id="20389-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="20389-110">يتوفر الخياران التاليان:</span><span class="sxs-lookup"><span data-stu-id="20389-110">The following options become available.</span></span> <span data-ttu-id="20389-111">هذان الخياران مطلوبان لتجميع النظام في قائمة عمل مفتوح.</span><span class="sxs-lookup"><span data-stu-id="20389-111">These options are required for system grouping on an open work list.</span></span> 

|        <span data-ttu-id="20389-112">الخيار</span><span class="sxs-lookup"><span data-stu-id="20389-112">Option</span></span>         |                                                                                                                                                                                                                                                                         <span data-ttu-id="20389-113">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="20389-113">Description</span></span>                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20389-114">السماح بتجميع النظام</span><span class="sxs-lookup"><span data-stu-id="20389-114">Allow system grouping</span></span> |                                                                                                                                                                                                                                                 <span data-ttu-id="20389-115">لتمكين تجميع النظام لعنصر قائمة عمل محدد.</span><span class="sxs-lookup"><span data-stu-id="20389-115">Enables system groping for a selected work list menu item.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="20389-116">حقل تجميع النظام</span><span class="sxs-lookup"><span data-stu-id="20389-116">System grouping field</span></span> | <span data-ttu-id="20389-117">يتوفر فقط عند تعيين <strong>السماح بعمل النظام</strong> إلى <strong>نعم</strong>.</span><span class="sxs-lookup"><span data-stu-id="20389-117">Available only if <strong>Allow system work</strong> is set to <strong>Yes</strong>.</span></span> <span data-ttu-id="20389-118">حدد الحقل الذي يحدد كيفية تجميع عمل الانتقاء للعاملين.</span><span class="sxs-lookup"><span data-stu-id="20389-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="20389-119">على سبيل المثال، إذا قمت بتحديد حقل <strong>‏‫معرف الشحنة‬</strong>، سيقوم العامل بفحص معرف الشحنة لتجميع عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="20389-119">For example, if you select the <strong>ShipmentId</strong> field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="20389-120">ثم يتم تعيين جميع الأعمال للشحنة للعامل.</span><span class="sxs-lookup"><span data-stu-id="20389-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="20389-121">ويتطلب هذا الحقل إنشاء صنف قائمة لاستخدام العمل الموجود الذي يتم تجميعه بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="20389-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="20389-122">استخدم الحقل <strong>تسمية تجميع النظام</strong> لإعلام العامل بما يجب عليه فحصه.</span><span class="sxs-lookup"><span data-stu-id="20389-122">Use the <strong>System grouping label</strong> field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="20389-123">بطاقة تجميع النظام</span><span class="sxs-lookup"><span data-stu-id="20389-123">System grouping label</span></span> |                       <span data-ttu-id="20389-124">يتوفر فقط عند تعيين <strong>السماح بعمل النظام</strong> إلى <strong>نعم</strong>.</span><span class="sxs-lookup"><span data-stu-id="20389-124">Available only if <strong>Allow system work</strong> is set to <strong>Yes</strong>.</span></span> <span data-ttu-id="20389-125">أدخل معلومات للعامل عما يجب عليه فحصه عندما يتم تجميع عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="20389-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="20389-126">على سبيل المثال، إذا كنت تستخدم حقل <strong>معرف الشحنة</strong> لتجميع عمل الانتقاء بالشحنة، يمكنك إدخال معرف الشحنة في الحقل.</span><span class="sxs-lookup"><span data-stu-id="20389-126">For example, if you use the <strong>ShipmentId</strong> field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="20389-127">ويتطلب هذا الحقل إنشاء صنف قائمة لاستخدام العمل الموجود الذي يتم تجميعه بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="20389-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="20389-128">يجب أيضًا تحديد الحقل للتجميع بحسب في حقل <strong>تجميع النظام</strong>.</span><span class="sxs-lookup"><span data-stu-id="20389-128">You must also select the field to group by in the <strong>System grouping</strong> field.</span></span>                       |

