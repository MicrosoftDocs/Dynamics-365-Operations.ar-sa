---
title: التحديث اليدوي لعدادات الأصول
description: يصف هذا الموضوع التحديث اليدوي لعدادات الأصول‬ في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875485"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="dd24e-103">التحديث اليدوي لعدادات الأصول</span><span class="sxs-lookup"><span data-stu-id="dd24e-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="dd24e-104">يتم استخدام العدادات لإنشاء تسجيلات على أحد الأصول تتعلق، على سبيل المثال، بعدد الساعات قيد التشغيل أو عدد الكميات التي تم إنتاجها.</span><span class="sxs-lookup"><span data-stu-id="dd24e-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="dd24e-105">إذا تم تعيين نوع العداد المحدد لعداد ما بحيث يتوارث قيم العداد (**إدارة الأصول** > **الإعداد** > **أنواع الأصول‏‎** > **العدادات** > علامة التبويب السريعة **عام** > زر التبديل **توارث قيم عداد الأصول** معين إلى "نعم")، فسيتم تحديث كل أصل تابع يستخدم نوع العداد نفسه بشكل تلقائي وذلك عندما تنشئ بند عداد جديدًا من هذا النوع.</span><span class="sxs-lookup"><span data-stu-id="dd24e-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="dd24e-106">في **كل الأصول**، يمكنك إنشاء تسجيلات العداد للساعات أو الكميات على أصل ما استنادًا إلى قراءاتك على الأصل.</span><span class="sxs-lookup"><span data-stu-id="dd24e-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="dd24e-107">انقر فوق **إدارة الأصول** > **عام** > **الأصول** > **كل الأصول**.</span><span class="sxs-lookup"><span data-stu-id="dd24e-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="dd24e-108">حدد الأصل في القائمة، ثم انقر فوق **العدادات**.</span><span class="sxs-lookup"><span data-stu-id="dd24e-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="dd24e-109">في نموذج **عدادات الأصول**، تظهر قائمة بجميع تسجيلات العدادات السابقة على الأصل المحدد.</span><span class="sxs-lookup"><span data-stu-id="dd24e-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="dd24e-110">انقر فوق **جديد** لإنشاء تسجيل جديد.</span><span class="sxs-lookup"><span data-stu-id="dd24e-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="dd24e-111">يتم إدراج معرف الأصل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="dd24e-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="dd24e-112">في حقل **العداد**، حدد العداد المناسب.</span><span class="sxs-lookup"><span data-stu-id="dd24e-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="dd24e-113">لا تتوفر سوى العدادات المرتبطة بنوع الأصل المحدد في الأصل.</span><span class="sxs-lookup"><span data-stu-id="dd24e-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="dd24e-114">يتم إدراج الوحدة ذات الصلة بشكل تلقائي في حقل **الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="dd24e-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="dd24e-115">حدد تاريخ ووقت تسجيل العداد.</span><span class="sxs-lookup"><span data-stu-id="dd24e-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="dd24e-116">في حقل **القيمة**، أدخل الرقم منذ آخر تسجيل للعداد أو في حقل **القيمة المجمعة**، أدخل رقم الجرد الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="dd24e-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="dd24e-117">إذا قمت بتثبيت عداد جديد بشكل فعلي على أصل ما، فستحتاج إلى تسجيل التغيير على الأصل في **عدادات‏‎ الأصول**.</span><span class="sxs-lookup"><span data-stu-id="dd24e-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="dd24e-118">بعد ذلك، يجب إنشاء بندي تسجيل مع طوابع زمنية مختلفة، وفي البند المتعلق بالعداد الجديد، حدد خانة الاختيار **إعادة تعيين العداد**.</span><span class="sxs-lookup"><span data-stu-id="dd24e-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="dd24e-119">عند إنشاء بندي تسجيل، يجب أن يكون البند الأول خاصًا بالعداد الذي تقوم باستبداله.</span><span class="sxs-lookup"><span data-stu-id="dd24e-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="dd24e-120">في حقل **الإجماليات**، يتطابق العدد الإجمالي مع مجموع إجمالي العدادات لكافة القيم المسجلة في نوع العداد هذا.</span><span class="sxs-lookup"><span data-stu-id="dd24e-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="dd24e-121">إذا تم تحديد خانة الاختيار **إعادة تعيين العداد** على أحد الأصول باستخدام نوع الفاصل الزمني "مرة واحدة من..." أو "عند الوصول..."، يبقى العداد نشطًا على بند العداد الجديد لأنك قمت بإنشاء بند عداد منفصل وبدأت من جديد باستخدام عداد جديد.</span><span class="sxs-lookup"><span data-stu-id="dd24e-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![الشكل 1](media/11-work-orders.png)


<span data-ttu-id="dd24e-123">إذا أردت إجراء تسجيلات العداد على أصول متعددة، فيمكنك القيام بذلك في **إدارة الأصول** > **استعلامات** > **الأصول‏‎** > **عدادات الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="dd24e-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="dd24e-124">يمكنك إعداد نطاق لتعريف الانحرافات في تسجيلات العدادات اليدوية، ونوع الرسالة التي يجب عرضها عندما تكون التسجيلات خارج النطاق المحدد.</span><span class="sxs-lookup"><span data-stu-id="dd24e-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="dd24e-125">فيما يتعلق بإعداد العدادات، راجع الموضوع [العدادات](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="dd24e-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
