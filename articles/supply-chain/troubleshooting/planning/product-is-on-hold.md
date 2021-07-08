---
title: المنتج قيد الانتظار لحركات .
description: بعد تأكيد أوامر التخطيط، تظهر رسالة خطأ تنص على أن أحد الأصناف قيد الانتظار للحركات.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301269"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="a48f7-103">المنتج قيد الانتظار لحركات .</span><span class="sxs-lookup"><span data-stu-id="a48f7-103">Product is on hold for transactions</span></span>

<span data-ttu-id="a48f7-104">رمز الخطأ: SYS13295</span><span class="sxs-lookup"><span data-stu-id="a48f7-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="a48f7-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="a48f7-105">Symptoms</span></span>

<span data-ttu-id="a48f7-106">بعد تأكيد الأوامر المخططة، تظهر رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="a48f7-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="a48f7-107">الصنف %1 قيد الانتظار للحركة في %2.</span><span class="sxs-lookup"><span data-stu-id="a48f7-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="a48f7-108">السبب</span><span class="sxs-lookup"><span data-stu-id="a48f7-108">Cause</span></span>

<span data-ttu-id="a48f7-109">عند وصف الأصناف المحظورة، يستخدم النظام الشروط *محظور* و *متوقف* و *قيد الانتظار* بالتبادل.</span><span class="sxs-lookup"><span data-stu-id="a48f7-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="a48f7-110">يعني هذا الخطأ أنه قد تم تعيين العنصر كـ **متوقف** في إعدادات الأمر الافتراضية الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="a48f7-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="a48f7-111">في حالة حظر أحد الأصناف، وإضافته إلى أمر شراء أو بند أمر مبيعات، فإنك ستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="a48f7-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="a48f7-112">وفي حالة حظر الصنف، لا يمكن تعديل حركات المخزون المرتبطة بأمر الشراء أو بند أمر المبيعات، (على سبيل المثال، عند ترحيل إيصال تعبئة أو فاتورة).</span><span class="sxs-lookup"><span data-stu-id="a48f7-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="a48f7-113">ويمكنك حظر صنف مشترى وفي نفس الوقت بيعه.</span><span class="sxs-lookup"><span data-stu-id="a48f7-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="a48f7-114">وفي هذه الحالة، يتم تحديد مربع اختيار **متوقف** على أمر الشراء، لكن الصنف لا يتم حظره في المخزون أو أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a48f7-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="a48f7-115">فيما يلي بعض الشروط التي يمكن أن تؤدي إلى حظر رقم الصنف من البيع:</span><span class="sxs-lookup"><span data-stu-id="a48f7-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="a48f7-116">لا يزال الصنف تحت التطوير أو التصنيع.</span><span class="sxs-lookup"><span data-stu-id="a48f7-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="a48f7-117">ولذلك، فإنك لا ترغب في بيعه أو حجزه.</span><span class="sxs-lookup"><span data-stu-id="a48f7-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="a48f7-118">لقد استلمت العديد من الأصناف المعيبة، ويجب تصحيح العيوب قبل أن يتم بيع الصنف.</span><span class="sxs-lookup"><span data-stu-id="a48f7-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="a48f7-119">في حالات من هذا النوع، يمكنك حظر الصنف حتى يتم حل المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a48f7-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="a48f7-120">إذا تم حظر صنفًا محظورًا وتقوم بإنشاء بند أمر إرجاع، يتم استلام رسالة.</span><span class="sxs-lookup"><span data-stu-id="a48f7-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="a48f7-121">لا يمكنك تأمين سلسلة أو دفعة من الأصناف.</span><span class="sxs-lookup"><span data-stu-id="a48f7-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="a48f7-122">في حالة تأمين أجزاء من الصنف، يمكنك تأمينها عن طريق نقل المخزون أو تأمين مخزون الصنف بالكامل لتلك الفترة.</span><span class="sxs-lookup"><span data-stu-id="a48f7-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="a48f7-123">الحل</span><span class="sxs-lookup"><span data-stu-id="a48f7-123">Resolution</span></span>

- <span data-ttu-id="a48f7-124">افتح الصفحة **إعدادات الأمر الافتراضية**، وقم بإلغاء تحديد خانة الاختيار **متوقف**.</span><span class="sxs-lookup"><span data-stu-id="a48f7-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
