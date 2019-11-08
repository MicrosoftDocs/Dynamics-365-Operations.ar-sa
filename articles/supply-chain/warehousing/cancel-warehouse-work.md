---
title: إلغاء عمل المستودع لمعالجه الاستثناء
description: يصف هذا الموضوع وظيفة إلغاء العمل التي تتيح لمشرفي المستودع معالجه العمل المحظور.
author: omulvad
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6aa073f72a3ece81d945f75b32f906d5846f7ce9
ms.sourcegitcommit: bc9b65b73bf6443581c2869a9ecfd0675f0be566
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/15/2019
ms.locfileid: "2625845"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="d04d3-103">إلغاء عمل المستودع لمعالجه الاستثناء</span><span class="sxs-lookup"><span data-stu-id="d04d3-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d04d3-104">تتيح وظيفة إلغاء العمل في Dynamics 365 Supply Chain Management Microsoft للمستخدم المسؤول إلغاء عمل مستودع مُعين قيد التقدم حاليًا، ولكن يتم حظره بواسطة النظام أو لا يمكن إكماله بسبب الظروف الاستثنائية.</span><span class="sxs-lookup"><span data-stu-id="d04d3-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="d04d3-105">وتعتبر هذه الوظيفة بديلاً مُغريًا وأمنًا للبرامج النصية التصحيحية في SQL التي تقوم بإصلاح البيانات غير المتناسقة.</span><span class="sxs-lookup"><span data-stu-id="d04d3-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="d04d3-106">ومع ذلك، بينما يتم طلب هذه البرامج النصية عادةً من متخصصي تكنولوجيا المعلومات، يمكن استخدام وظيفة إلغاء العمل من قبل المستخدمين الموجودين في الشركة والذين لديهم حقوق/صلاحيات المسؤول.</span><span class="sxs-lookup"><span data-stu-id="d04d3-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="d04d3-107">يمكنك الوصول إلى وظيفة إلغاء العمل في **إدارة المستودع** \> **المهام الدورية** \> **تنظيف \> إلغاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="d04d3-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="d04d3-108">في مربع الحوار **إلغاء العمل** ، حدد معرف العمل الخاص بالعمل المراد إلغاءه، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d04d3-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="d04d3-109">عمل المستودع الذي يمكن إلغاؤه</span><span class="sxs-lookup"><span data-stu-id="d04d3-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="d04d3-110">وأثناء عمليات انتقاء المستودع، قد يواجه العامل مواقف يتم فيها تسجيل كميات مسجلة علي أنها منتقية من موقع تخزين إلى موقع المستخدم الخاص بها، ولكن لا يمكنهم تسجيل عمليه الوضع.</span><span class="sxs-lookup"><span data-stu-id="d04d3-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="d04d3-111">وغالبًا وليس دائمًا ما تكون بيانات المستودع غير المتسقة هي السبب وراء حظر العمل.</span><span class="sxs-lookup"><span data-stu-id="d04d3-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="d04d3-112">علي عكس وظيفة الإلغاء العادية التي يمكن الوصول اليها باستخدام زر **إلغاء** في رأس العمل، لا تتطلب وظيفة إلغاء العمل ان يكون آخر بند عمل مكتمل هو بند عمل من النوع **وضع** .</span><span class="sxs-lookup"><span data-stu-id="d04d3-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="d04d3-113">بمعني آخر، بالنسبة لوظيفة إلغاء العمل، يمكن تشغيل منطق الإلغاء حتى إذا كانت كمية الصنف في بند العمل موجودة في موقع المستخدم.</span><span class="sxs-lookup"><span data-stu-id="d04d3-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="d04d3-114">بالنسبة للعمل الذي يجب إلغاؤه لأسباب تشغيلية، يجب أن يستمر مستخدمو المستودع في استخدام وظيفة الإلغاء العادية في صفحه العمل.</span><span class="sxs-lookup"><span data-stu-id="d04d3-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="d04d3-115">يمكن إلغاء عمل **المبيعات**، أو **إصدار تحويل‬**، أو **‏‫انتقاء المواد الخام‬**، أو نوع **التزويد** فقط من خلال استخدام وظيفة إلغاء العمل.</span><span class="sxs-lookup"><span data-stu-id="d04d3-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="d04d3-116">لن يتم تشغيل منطق الإلغاء لعمل الانتقاء للمواد الخام المجمدة أو العمل الذي يمكن إلغاؤه باستخدام وظيفة الإلغاء العادية (راجع الملاحظة السابقة).</span><span class="sxs-lookup"><span data-stu-id="d04d3-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="d04d3-117">لإلغاء حظر العمل، يُلغي النظام بنود العمل المتبقية ويُصلح بيانات المستودع المقترنة بمعرف العمل الذي حدده المستخدم.</span><span class="sxs-lookup"><span data-stu-id="d04d3-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="d04d3-118">ويمكن استئناف عمليات معالجة المستودع العادية التي تتضمن كمية الصنف المتأثرة.</span><span class="sxs-lookup"><span data-stu-id="d04d3-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="d04d3-119">لوضع الصنف المتأثر في موقع محدد بعد إلغاء العمل، يستخدم المستخدم حركة المخزون أو عملية تعديل الكمية علي جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="d04d3-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
