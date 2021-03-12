---
title: تغيير ‏‫وضع التسليم‬ في نقطة البيع
description: يصف هذا الموضوع كيفية تكوين واستخدام عملية تغيير وضع التسليم في نقطة البيع.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 6bfe27a7b4a768da00c67e307a0bd7e57b333d11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965417"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="dd75f-103">تغيير ‏‫وضع التسليم‬ في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="dd75f-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dd75f-104">يصف هذا الموضوع كيفية إعداد وظيفة "تغيير وضع التسليم" واستخدامها في بيئة نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="dd75f-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="dd75f-105">في الإصدارات 10.0.10 والإصدارات الأحدث من Dynamics 365 Commerce، تتوفر عملية **تغيير وضع التسليم** (647) لإضافتها إلى تخطيطات شاشة نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="dd75f-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="dd75f-106">توفر لك ميزة تغيير وضع التسليم خيار تغيير وضع التسليم لبند أو أكثر من بنود المبيعات المكونة للشحن على حركة نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="dd75f-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="dd75f-107">في الإصدارات السابقة من Commerce، كان يتعين عليك التنقل عبر تدفقات تكوين **شحن الكل‬** أو **شحن المحدد** الكاملة لتغيير وضع التسليم على بند موجود تم تكوينه للشحن.</span><span class="sxs-lookup"><span data-stu-id="dd75f-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="dd75f-108">لقد كانت هذه العملية تستغرق وقتًا طويلاً، وكان ينتج عنها تغييرات غير مقصودة في أصل التسليم أو تواريخ التسليم الخاصة بالبند.</span><span class="sxs-lookup"><span data-stu-id="dd75f-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="dd75f-109">توفر الوظيفة الجديدة طريقة بديلة لتحديث وضع التسليم بكفاءة على بنود المبيعات هذه.</span><span class="sxs-lookup"><span data-stu-id="dd75f-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="dd75f-110">لمزيد من المعلومات حول كيفية إضافة عملية إلى زر على شبكة أزرار نقطة البيع، راجع [تخطيطات الشاشة لنقطة البيع](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span><span class="sxs-lookup"><span data-stu-id="dd75f-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="dd75f-111">بعد تكوين هذه الميزة في نقطة البيع، عندما تحدد **تغيير وضع التسليم**، ستظهر قائمة صفحات تسمح لك باختيار بنود الحركة التي تريد تغيير وضع التسليم لها.</span><span class="sxs-lookup"><span data-stu-id="dd75f-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="dd75f-112">يمكنك اختيار بعض البنود أو جميعها، أو الخروج من دون إجراء أي تغييرات.</span><span class="sxs-lookup"><span data-stu-id="dd75f-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="dd75f-113">تعتبر بنود المبيعات التي تم تكوينها في السابق للشحن هي البنود الوحيدة الموجودة في القائمة التي يمكنك تغييرها.</span><span class="sxs-lookup"><span data-stu-id="dd75f-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="dd75f-114">إذا كنت ترغب في تغيير بند مخصص لانتقائه أو نقله للشحن، فيجب استخدام العمليتين **شحن الكل** أو **شحن المحدد**.</span><span class="sxs-lookup"><span data-stu-id="dd75f-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="dd75f-115">وعلى العكس من ذلك، إذا أردت تغيير بند تم تعيينه كشحن للانتقاء أو النقل، فيحب استخدام العمليات  **انتقاء الكل** أو **انتقاء المحدد** أو **نقل الكل** أو **نقل المحدد**.</span><span class="sxs-lookup"><span data-stu-id="dd75f-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="dd75f-116">بعد تحديد البنود التي ترغب في تغييرها، انقر فوق **تغيير وضع التسليم** كي تتم مطالبتك بتحديد خيارات وضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="dd75f-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="dd75f-117">إذا قمت بتحديد بنود متعددة لتغييرها، فستعرض نقطة البيع فقط أوضاع التسليم التي تم تكوينها على أنها مسموح بها لجميع المنتجات المحددة.</span><span class="sxs-lookup"><span data-stu-id="dd75f-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="dd75f-118">يمكن تكوين أوضاع التسليم لدعم منتجات وعناوين تسليم معينة.</span><span class="sxs-lookup"><span data-stu-id="dd75f-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="dd75f-119">عند وجود وضع تسليم مقبول لمجموعة واحدة تتكون من منتجات وعناوين، ولكنه غير مقبول لمجموعة أخرى تتكون من منتجات وعناوين محددة، لن يكون وضع التسليم متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="dd75f-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="dd75f-120">قد تحتاج إلى تحديد البنود كل واحد على حدة وتغيير وضع التسليم لكل بند على حدة إذا أردت تحديد وضع تسليم لمنتج غير مدعوم من قبل منتج آخر.</span><span class="sxs-lookup"><span data-stu-id="dd75f-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="dd75f-121">بعد تحديد وضع التسليم الجديد، يتم عرض صفحة الحركة.</span><span class="sxs-lookup"><span data-stu-id="dd75f-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="dd75f-122">لمراجعه تحديدات وضع التسليم الجديدة، حدد علامة تبويب **التسليم** في قائمة الحركات.</span><span class="sxs-lookup"><span data-stu-id="dd75f-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd75f-123">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="dd75f-123">Additional resources</span></span>

[<span data-ttu-id="dd75f-124">إنشاء أوامر مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="dd75f-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="dd75f-125">تخصيص رسائل البريد الكتروني للمعاملات حسب وضع التسليم</span><span class="sxs-lookup"><span data-stu-id="dd75f-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)
