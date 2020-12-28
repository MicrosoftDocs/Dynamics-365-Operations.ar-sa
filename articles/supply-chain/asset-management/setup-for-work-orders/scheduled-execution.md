---
title: التنفيذ المجدول
description: يشرح هذا الموضوع التنفيذ المجدول في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 976155b685498456952f7d715779d20191712103
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421398"
---
# <a name="scheduled-execution"></a><span data-ttu-id="55426-103">التنفيذ المجدول</span><span class="sxs-lookup"><span data-stu-id="55426-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="55426-104">يمكنك استخدام مستويات خدمة أمر العمل لإعداد التنفيذ المجدول.</span><span class="sxs-lookup"><span data-stu-id="55426-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="55426-105">(لمزيد من المعلومات حول مستويات خدمة أمر العمل، راجع [مستوى الخدمة ووصفها‬](service-level-and-description.md).) يوفر التنفيذ المجدول مرونة في تخطيط العمل لعاملي الصيانة، لأنه يمكنك إعداد متطلبات أكثر تفصيلاً أو أقل تفصيلاً للفترة التي يجب أن يتم إكمال أمر العمل خلالها.</span><span class="sxs-lookup"><span data-stu-id="55426-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="55426-106">على سبيل المثال، بإمكان عامل الصيانة الذي يكمل إحدى المهام خلال وقت أسرع من المتوقع في مرفق إنتاج الانتقال إلى مهمة قريبة تم التخطيط لتنفيذها في الأسبوع الحالي ولكن ليس بالضرورة في اليوم الحالي.</span><span class="sxs-lookup"><span data-stu-id="55426-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="55426-107">تتيح هذه الطريقة تحسين تخطيط العامل واكتمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="55426-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="55426-108">بإمكان إعداد التنفيذ المجدول، المرتبط بأوامر العمل، أن يكون عامًا أو محددًا.</span><span class="sxs-lookup"><span data-stu-id="55426-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="55426-109">يمكن إعداد بنود عامة غير مقيدة بأنواع أوامر عامل أو أنواع أصول معينة، وما إلى ذلك.</span><span class="sxs-lookup"><span data-stu-id="55426-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="55426-110">أو يمكنك إنشاء بنود تنفيذ مجدولة تنطبق على أنواع معينة من أوامر العمل والأصول ومهام الصيانة، وغير ذلك.</span><span class="sxs-lookup"><span data-stu-id="55426-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="55426-111">حدد **إدارة الأصول** \> **الإعداد** \> **أوامر العمل** \> **التنفيذ المجدول**.</span><span class="sxs-lookup"><span data-stu-id="55426-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="55426-112">حدد **جديد**" لإنشاء بند تنفيذ مجدول جديد.</span><span class="sxs-lookup"><span data-stu-id="55426-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="55426-113">في الحقول **موقع العمل** و **نوع أمر العمل** و **نوع الأصل** و **الشركة المصنعة** و **النموذج** و **فئة نوع مهمة الصيانة** و **نوع مهمة الصيانة** و **متغير نوع مهمة الصيانة** و **المعاملات**، حدد القيم كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="55426-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="55426-114">حدد مستوى خدمه أمر عمل في حقل **مستوى الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="55426-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="55426-115">إذا تركت هذا الحقل فارغًا، فأنت تنشئ نوع بند التنفيذ المجدولة الأكثر عمومية.</span><span class="sxs-lookup"><span data-stu-id="55426-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="55426-116">للحصول على مثال عن بند عام، راجع السجل الأول في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="55426-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="55426-117">ويتيح ذلك البند إمكانية جدولة جميع أوامر العمل التي ليس لها مستوى خدمة أمر عمل لتاريخ ووقت محددين.</span><span class="sxs-lookup"><span data-stu-id="55426-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="55426-118">في الحقل **التنفيذ المجدول**، حدد الفترة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="55426-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="55426-119">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="55426-119">Select **Save**.</span></span>

![التنفيذ المجدول](media/20-setup-for-work-orders.png)
