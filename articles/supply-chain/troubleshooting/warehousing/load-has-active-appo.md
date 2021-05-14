---
title: لا يمكنك تأكيد شحنة بسبب مشكلة في التقويم
description: لا يمكنك تأكيد شحنة بسبب مشكلة في التقويم
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938415"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="c4785-103">لا يمكنك تأكيد شحنة بسبب مشكلة في التقويم</span><span class="sxs-lookup"><span data-stu-id="c4785-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="c4785-104">رمز الخطأ: TRX2716</span><span class="sxs-lookup"><span data-stu-id="c4785-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="c4785-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="c4785-105">Symptoms</span></span>

<span data-ttu-id="c4785-106">عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:</span><span class="sxs-lookup"><span data-stu-id="c4785-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="c4785-107">يتطلب نوع التقويم %1 أن يتم تسجيل الدخول والخروج للموعد %2.</span><span class="sxs-lookup"><span data-stu-id="c4785-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="c4785-108">وبالتالي، لا يمكنك تاكيد الشحن للتحميل.</span><span class="sxs-lookup"><span data-stu-id="c4785-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="c4785-109">السبب</span><span class="sxs-lookup"><span data-stu-id="c4785-109">Cause</span></span>

<span data-ttu-id="c4785-110">المواعيد النشطة للتحميل موجودة.</span><span class="sxs-lookup"><span data-stu-id="c4785-110">Active appointments for the load exist.</span></span> <span data-ttu-id="c4785-111">على سبيل المثال، هناك قاعدة تتطلب تسجيل وصول السائق.</span><span class="sxs-lookup"><span data-stu-id="c4785-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="c4785-112">لذلك، يكون الحمل حاليًا في حالة فشل فيها تأكيد الشحن.</span><span class="sxs-lookup"><span data-stu-id="c4785-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="c4785-113">الدقة</span><span class="sxs-lookup"><span data-stu-id="c4785-113">Resolution</span></span>

<span data-ttu-id="c4785-114">يجب عليك التحقيق وإصلاح أية مشكلات تتعلق بالمواعيد النشطة المرتبطة بالحمل.</span><span class="sxs-lookup"><span data-stu-id="c4785-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="c4785-115">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="c4785-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c4785-116">حدد الحمل الذي لا يمكن تأكيد الشحنة له.</span><span class="sxs-lookup"><span data-stu-id="c4785-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="c4785-117">في جزء الإجراء، في علامة تبويب **النقل**، في مجموعة **المواعيد**، حدد **جدولة المواعيد**.</span><span class="sxs-lookup"><span data-stu-id="c4785-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="c4785-118">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="c4785-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="c4785-119">تأكد من اكتمال تسجيل الوصول/المغادرة للسائق للموعد.</span><span class="sxs-lookup"><span data-stu-id="c4785-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="c4785-120">أكمل أو ألغِ الموعد.</span><span class="sxs-lookup"><span data-stu-id="c4785-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="c4785-121">قم بتعطيل خيار **مطلوب تسجيل وصول السائق** لقاعدة المواعيد ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="c4785-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
