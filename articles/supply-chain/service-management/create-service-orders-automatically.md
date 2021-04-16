---
title: إنشاء أوامر الخدمة تلقائيًا
description: يمكن إنشاء أوامر خدمة لاتفاقية خدمة واحدة أو للعديد من اتفاقيات الخدمات.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc06536827320a35a691330d852ba64532604935
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817595"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="5d1ea-103">إنشاء أوامر الخدمة تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="5d1ea-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5d1ea-104">يمكن إنشاء أوامر خدمة لاتفاقية خدمة واحدة أو للعديد من اتفاقيات الخدمات.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="5d1ea-105">وعند إنشائها، يمكن عرض أوامر الخدمة في النموذج **أوامر الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="5d1ea-106">يتم إنشاء أوامر الخدمة لفترة صلاحية اتفاقية الخدمات فقط.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="5d1ea-107">فإذا كان الفاصل الزمني الذي قمت بتحديده في النموذج **إنشاء أوامر الخدمة** يقع قبل تاريخ بدء أو بعد تاريخ انتهاء اتفاقية الخدمات، فيتم إنشاء أوامر الخدمة لجزء الفاصل الزمني الذي يقع داخل اتفاقية الخدمات فقط.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="5d1ea-108">عندما تقوم بإنشاء أوامر الخدمة يدويًا أو تلقائيًا من بند اتفاقية الخدمة، فلابد من وقوع أمر الخدمة في نطاق الفترة الزمنية التي تم تحديدها من خلال تاريخي البداية والانتهاء للبند إلا إذا لم تقم بتحديد تاريخ انتهاء للبند.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="5d1ea-109">إنشاء أوامر خدمة لاتفاقية خدمات تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="5d1ea-110">انقر فوق **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="5d1ea-111">حدد اتفاقية خدمات.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="5d1ea-112">انقر فوق علامة تبويب **تقديم**، ثم انقر فوق **أوامر الخدمة المخططة**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="5d1ea-113">حدد التواريخ في حقول **من تاريخ** و **إلى تاريخ** لتحديد فترة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="5d1ea-114">حدد خانة الاختيار **إظهار سجل المعلومات** لعرض قائمة بأوامر الخدمات التي يتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="5d1ea-115">حدد أنواع الحركات في مجموعة الحقول **تضمين أنواع الحركات**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="5d1ea-116">تمثل أنواع الحركات البنود التي يتم إنشاؤها في اتفاقية الخدمات، ويقوم كل نوع تختاره من أنواع الحركات بإنشاء العديد من أوامر الخدمة، بناءً على الفاصل الزمني للخدمة الذي يتم تحديده في بند اتفاقية الخدمات.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="5d1ea-117">لإنشاء أي أوامر خدمة مفقودة في السلاسل المتواصلة لأوامر الخدمة، حدد خانة الاختيار **مستمر**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="5d1ea-118">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="5d1ea-119">إنشاء أوامر خدمة للعديد من اتفاقيات الخدمات تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="5d1ea-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="5d1ea-120">انقر فوق **إدارة الخدمة** \> **دوري** \> **أوامر الخدمات** \> **إنشاء أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="5d1ea-121">انقر فوق **حدد** لعمل تحديدات لإضافة أو إزالة المعايير المستخدمة لإنشاء أوامر خدمة.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="5d1ea-122">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d1ea-123">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="5d1ea-123">See also</span></span>

[<span data-ttu-id="5d1ea-124">أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="5d1ea-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="5d1ea-125">إنشاء أوامر الخدمة تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="5d1ea-125">Automatically create service orders</span></span>](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]