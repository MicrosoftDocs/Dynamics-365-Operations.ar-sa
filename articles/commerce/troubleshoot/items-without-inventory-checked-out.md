---
title: يمكن عمل سداد مع الخروج للأصناف التي ليس لها مخزون
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عندما يقوم أحد العملاء بإضافة أصناف خارج المخزون إلى سلة التسوق الخاصة بهم ومتابعة السداد مع الخروج.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: af44def901d3aa7d4b24ab6abfac60d066a8d1a3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801737"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="9ebc8-103">يمكن عمل سداد مع الخروج للأصناف التي ليس لها مخزون</span><span class="sxs-lookup"><span data-stu-id="9ebc8-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ebc8-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عندما يقوم أحد العملاء بإضافة أصناف خارج المخزون إلى سلة التسوق الخاصة بهم ومتابعة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="9ebc8-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="9ebc8-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="9ebc8-105">Description</span></span>

<span data-ttu-id="9ebc8-106">يمكن للمستخدمين إضافة أحد الأصناف إلى سلة التسوق الخاصة بهم، على الرغم من عدم وجود مخزون فعلي في المتجر، ثم الانتقال إلى صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="9ebc8-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="9ebc8-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="9ebc8-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="9ebc8-108">تمكين خاصية إظهار أخطاء نفاد المخزون في منشئ موقع Commerce</span><span class="sxs-lookup"><span data-stu-id="9ebc8-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="9ebc8-109">لتمكين خاصية **إظهار أخطاء نفاد المخزون** في منشئ موقع Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="9ebc8-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9ebc8-110">حدد الموقع الذي تعمل عليه.</span><span class="sxs-lookup"><span data-stu-id="9ebc8-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="9ebc8-111">في جزء التنقل الأيسر، حدد **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="9ebc8-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="9ebc8-112">حدد **CartPage** لفتحه.</span><span class="sxs-lookup"><span data-stu-id="9ebc8-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="9ebc8-113">حدد فتحة **سلة التسوق 1**، وحدد **تحرير**، ثم في جزء الخصائص، حدد خانة الاختيار **إظهار أخطاء نفاد المخزون**.</span><span class="sxs-lookup"><span data-stu-id="9ebc8-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="9ebc8-114">احفظ الصفحة وقم بنشرها.</span><span class="sxs-lookup"><span data-stu-id="9ebc8-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9ebc8-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9ebc8-115">Additional resources</span></span>

[<span data-ttu-id="9ebc8-116">تطبيق إعدادات المخزون</span><span class="sxs-lookup"><span data-stu-id="9ebc8-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="9ebc8-117">حساب توفر المخزون لقنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="9ebc8-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="9ebc8-118">تكوين المخازن المؤقتة للمخزون ومستويات المخزون</span><span class="sxs-lookup"><span data-stu-id="9ebc8-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
