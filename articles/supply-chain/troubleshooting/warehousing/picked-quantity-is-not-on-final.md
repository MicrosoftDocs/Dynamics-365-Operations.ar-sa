---
title: لا يمكنك تاكيد شحنه نظرا لأنه لم يتم انتقاء الأصناف
description: لا يمكنك تاكيد شحنه نظرا لأنه لم يتم انتقاء الأصناف
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938413"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="da6b4-103">لا يمكنك تاكيد شحنه نظرا لأنه لم يتم انتقاء الأصناف</span><span class="sxs-lookup"><span data-stu-id="da6b4-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="da6b4-104">رمز الخطأ: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="da6b4-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="da6b4-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="da6b4-105">Symptoms</span></span>

<span data-ttu-id="da6b4-106">عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:</span><span class="sxs-lookup"><span data-stu-id="da6b4-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="da6b4-107">لم يتم انتقاء بعض الأصناف اللازمة لحمل العمل %1 ولا نقلها إلى موقع الشحن النهائي.</span><span class="sxs-lookup"><span data-stu-id="da6b4-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="da6b4-108">وبالتالي، لا يمكنك تاكيد الشحن للتحميل.</span><span class="sxs-lookup"><span data-stu-id="da6b4-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="da6b4-109">السبب</span><span class="sxs-lookup"><span data-stu-id="da6b4-109">Cause</span></span>

<span data-ttu-id="da6b4-110">لا يمكن تاكيد التحميل أو الشحن في حالته الحالية لان أحدي الحالات التالية قد تكون موجودة:</span><span class="sxs-lookup"><span data-stu-id="da6b4-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="da6b4-111">لم يتم بعد انتقاء العمل ذي الصلة ونقله إلى موقع الشحن النهائي.</span><span class="sxs-lookup"><span data-stu-id="da6b4-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="da6b4-112">لا تتطابق كميه العمل المنتقية مع كميه العمل التي تم إنشاؤها في بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="da6b4-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="da6b4-113">الدقة</span><span class="sxs-lookup"><span data-stu-id="da6b4-113">Resolution</span></span>

<span data-ttu-id="da6b4-114">تحقق من أوامر التوريد أو أوامر التحويل ذات الصلة الخاصة بالحمل أو الشحن.</span><span class="sxs-lookup"><span data-stu-id="da6b4-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="da6b4-115">تاكد من اكتمال كافة الاعمال ذات الصلة في موقع الشحن النهائي، وان الكميات متطابقة.</span><span class="sxs-lookup"><span data-stu-id="da6b4-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="da6b4-116">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="da6b4-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="da6b4-117">حدد الحمل الذي لا يمكن تأكيد الشحنة له.</span><span class="sxs-lookup"><span data-stu-id="da6b4-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="da6b4-118">في علامة التبويب السريعة **بنود الحمل**، حدد بند الحمل.</span><span class="sxs-lookup"><span data-stu-id="da6b4-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="da6b4-119">دون ملاحظه قيمة حقل **الكمية التي أنشاهأ العمل**.</span><span class="sxs-lookup"><span data-stu-id="da6b4-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="da6b4-120">في جزء الإجراءات، في علامة التبويب **الأحمال**، في مجموعة **المعلومات ذات الصلة**، حدد **العمل**.</span><span class="sxs-lookup"><span data-stu-id="da6b4-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="da6b4-121">تحقق من اكتمال العمل في موقع الشحن النهائي، وان كميه العمل المنتقية تطابق كميه العمل التي تم إنشاؤها في بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="da6b4-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="da6b4-122">قم بتكرار هذا الاجراء لكافة بنود التحميل للتاكد من استيفاء كافة المعايير.</span><span class="sxs-lookup"><span data-stu-id="da6b4-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
