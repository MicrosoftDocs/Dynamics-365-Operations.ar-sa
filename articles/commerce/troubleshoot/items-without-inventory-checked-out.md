---
title: يمكن عمل سداد مع الخروج للأصناف التي ليس لها مخزون
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عندما يقوم أحد العملاء بإضافة أصناف خارج المخزون إلى سلة التسوق الخاصة بهم ومتابعة السداد مع الخروج.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018448"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="98713-103">يمكن عمل سداد مع الخروج للأصناف التي ليس لها مخزون</span><span class="sxs-lookup"><span data-stu-id="98713-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98713-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عندما يقوم أحد العملاء بإضافة أصناف خارج المخزون إلى سلة التسوق الخاصة بهم ومتابعة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="98713-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="98713-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="98713-105">Description</span></span>

<span data-ttu-id="98713-106">يمكن للمستخدمين إضافة أحد الأصناف إلى سلة التسوق الخاصة بهم، على الرغم من عدم وجود مخزون فعلي في المتجر، ثم الانتقال إلى صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="98713-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="98713-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="98713-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="98713-108">تمكين خاصية إظهار أخطاء نفاد المخزون في منشئ موقع Commerce</span><span class="sxs-lookup"><span data-stu-id="98713-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="98713-109">لتمكين خاصية **إظهار أخطاء نفاد المخزون** في منشئ موقع Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="98713-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="98713-110">حدد الموقع الذي تعمل عليه.</span><span class="sxs-lookup"><span data-stu-id="98713-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="98713-111">في جزء التنقل الأيسر، حدد **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="98713-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="98713-112">حدد **CartPage** لفتحه.</span><span class="sxs-lookup"><span data-stu-id="98713-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="98713-113">حدد فتحة **سلة التسوق 1**، وحدد **تحرير**، ثم في جزء الخصائص، حدد خانة الاختيار **إظهار أخطاء نفاد المخزون**.</span><span class="sxs-lookup"><span data-stu-id="98713-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="98713-114">احفظ الصفحة وقم بنشرها.</span><span class="sxs-lookup"><span data-stu-id="98713-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98713-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="98713-115">Additional resources</span></span>

[<span data-ttu-id="98713-116">تطبيق إعدادات المخزون</span><span class="sxs-lookup"><span data-stu-id="98713-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="98713-117">حساب توفر المخزون لقنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="98713-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="98713-118">تكوين المخازن المؤقتة للمخزون ومستويات المخزون</span><span class="sxs-lookup"><span data-stu-id="98713-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
