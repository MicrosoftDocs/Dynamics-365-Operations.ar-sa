---
title: "استلام لوحة ترخيص مختلطة"
description: "يصف هذا الموضوع كيفية استخدام استلام لوحة ترخيص مختلطة‬ لتسجيل وانشاء عمل لأصناف متعددة بواسطة جهاز محمول."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ec3fdff6e1118f4a4ef4146d315fe8c58664f453
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="2c3a6-103">استلام لوحة ترخيص مختلطة</span><span class="sxs-lookup"><span data-stu-id="2c3a6-103">Mixed license plate receiving</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2c3a6-104">يسمح لك استلام لوحة ترخيص مختلطة بإنشاء لوحة ترخيص تتكون من العديد من الأصناف قبل أن تقوم بالتسجيل وإنشاء عمل تخزين.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="2c3a6-105">لا تحتاج لوحة الترخيص المكونة من عدة أصناف إلى تقسيمها في رصيف الاستلام لكي تتمكن من تسجيل كل صنف.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="2c3a6-106">عند استخدام تدفق ذي صلة بالأصناف لتحديد بنود المستند المصدر، يمكنك فحص الأكواد الشريطية في عنصر تحكم الصنف.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="2c3a6-107">إذا تضمن الكود الشريطي كمية ووحدة قياس تم تكوينهما عليه، فسيضاف الصنف والكمية تلقائيًا إلى لوحة الترخيص المختلطة، وسيعاد توجيهك إلى الشاشة لمسح صنف آخر.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="2c3a6-108">سيسمح لك ذلك بفحص كافة الأصناف من دون الحاجة إلى إجراء تأكيد في كل خطوة.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="2c3a6-109">في التدفق الخاص باستلام لوحة الترخيص المختلطة، يمكنك عرض قائمة بالأصناف التي تم فحصها على لوحة الترخيص، ومن هنا يمكنك تعديل أو تصحيح كمية أحد الأصناف.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="2c3a6-110">أين يتم التطبيق</span><span class="sxs-lookup"><span data-stu-id="2c3a6-110">Where it applies</span></span>

<span data-ttu-id="2c3a6-111">إن استلام لوحة الترخيص المختلطة‬ عبارة عن تدفق استلام على جهاز محمول لتسجيل وانشاء عمل لأصناف/بنود متعددة في الوقت نفسه.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="2c3a6-112">يعتبر هذا الأمر مفيدًا إذا كنت تتلقى لوحات ترخيص واردة ذات أصناف متعددة.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="2c3a6-113">كيفية إعداد استلام ‏‫لوحة الترخيص‬ المختلطة</span><span class="sxs-lookup"><span data-stu-id="2c3a6-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="2c3a6-114">يتم إعداد استلام ‏‫لوحة الترخيص‬ المختلطة وتخزينها كعنصر قائمة جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="2c3a6-115">تحتاج إلى إنشاء عنصر قائمة جديد باستخدام وضع العمل الذي لا يستخدم العمل الموجود واستخدام إحدى الطريقتين التاليتين:</span><span class="sxs-lookup"><span data-stu-id="2c3a6-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="2c3a6-116">استلام لوحة ترخيص مختلطة</span><span class="sxs-lookup"><span data-stu-id="2c3a6-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="2c3a6-117">استلام ‏‫لوحة الترخيص‬ المختلطة وتخزينها</span><span class="sxs-lookup"><span data-stu-id="2c3a6-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="2c3a6-118">هناك خيارات للتعرف على بنود المستند المصدر وهي صنف أمر الشراء وبند أمر الشراء وأمر الإرجاع‬ وصنف أمر التحويل‬ وبند أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="2c3a6-119">باستطاعة هذه الخيارات تغيير أمر الاستلام على لوحة ترخيص واحدة.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="2c3a6-120">الخيار الأخير يتعلق بصنف حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-120">The last option is by load item.</span></span> <span data-ttu-id="2c3a6-121">يمكنك إضافة عدة عناصر إلى لوحة الترخيص، ولكن لا يمكنك التبديل بين أحمال عمل متعددة.</span><span class="sxs-lookup"><span data-stu-id="2c3a6-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>

