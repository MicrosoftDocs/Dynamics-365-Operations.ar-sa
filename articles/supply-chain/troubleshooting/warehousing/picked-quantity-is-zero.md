---
title: لا يمكنك التاكيد علي الشحنة بسبب وجود كميه تساوي صفرا
description: لا يمكنك التاكيد علي الشحنة بسبب وجود كميه تساوي صفرا
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938412"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="e24a4-103">لا يمكنك التاكيد علي الشحنة بسبب وجود كميه تساوي صفرا</span><span class="sxs-lookup"><span data-stu-id="e24a4-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="e24a4-104">رمز الخطأ: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="e24a4-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="e24a4-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="e24a4-105">Symptoms</span></span>

<span data-ttu-id="e24a4-106">عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:</span><span class="sxs-lookup"><span data-stu-id="e24a4-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="e24a4-107">تم تحديث بند حمل العمل للعنصر %1 والشحنة %2 للحصول على كمية صفرية بسبب إعداد التسليم الناقص مما يسمح بعدم شحن أي كميات لهذا العنصر.</span><span class="sxs-lookup"><span data-stu-id="e24a4-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="e24a4-108">وبالتالي، لا يمكنك تاكيد الشحن للتحميل.</span><span class="sxs-lookup"><span data-stu-id="e24a4-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="e24a4-109">السبب</span><span class="sxs-lookup"><span data-stu-id="e24a4-109">Cause</span></span>

<span data-ttu-id="e24a4-110">ويقوم النظام بتقييم ما إذا كانت الكمية المنتقية تقع داخل الحدود المتوقعة، استنادا إلى الكمية المنتقية وكميه البند التي تم انتقاؤها ونسبه التسليم بالنقص.</span><span class="sxs-lookup"><span data-stu-id="e24a4-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="e24a4-111">في حاله عثور النظام علي ان الكمية المنتقية في بند التحميل هي 0 (صفر)، لا يمكنك تاكيد الشحنة.</span><span class="sxs-lookup"><span data-stu-id="e24a4-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="e24a4-112">علي سبيل المثال، قد تحدث هذه المشكلة في حاله إلغاء العمل، وكانت النسبة المئوية للتسليم بالنقص لبند التحميل هي 100 بالمائة.</span><span class="sxs-lookup"><span data-stu-id="e24a4-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="e24a4-113">الدقة</span><span class="sxs-lookup"><span data-stu-id="e24a4-113">Resolution</span></span>

<span data-ttu-id="e24a4-114">تحقق من بنود الحمل للتاكد من ان النسبة المئوية للتسليم بالنقص والكميات تتم محاذاتها بالعمل المنتقي.</span><span class="sxs-lookup"><span data-stu-id="e24a4-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="e24a4-115">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="e24a4-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e24a4-116">حدد الحمل الذي لا يمكن تأكيد الشحنة له.</span><span class="sxs-lookup"><span data-stu-id="e24a4-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="e24a4-117">في علامة التبويب السريعة، **بنود الحمل**، حدد بند الحمل للعنصر الذي يتجاوز النسبة المئوية للتسليم الناقص.</span><span class="sxs-lookup"><span data-stu-id="e24a4-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="e24a4-118">قم بتعديل قيمة حقل **تسليم الناقص** أو حقل **الكمية** كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="e24a4-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="e24a4-119">في حاله استمرار عدم إصلاح المشكلة، قد يلزم إكمال المزيد من اعمال الانتقاء لأوامر التوريد أو أوامر التحويل ذات الصلة حتى تتم محاذاة الكمية المتوفرة مع الحمل أو الحمل.</span><span class="sxs-lookup"><span data-stu-id="e24a4-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
