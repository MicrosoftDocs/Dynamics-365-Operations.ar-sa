---
title: إلغاء أوامر الخدمة
description: يمكن إلغاء أمر خدمة أو بند أمر خدمة من أمر الخدمة نفسه، أو يمكنك إلغاء أوامر خدمة متعددة من خلال تشغيل مهمة دورية.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: a253a9c9ae4d7c34403db9bb5f3d63bc77e11101
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259664"
---
# <a name="cancel-service-orders"></a><span data-ttu-id="a3aa1-103">إلغاء أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="a3aa1-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a3aa1-104">يمكن إلغاء أمر خدمة أو بند أمر خدمة من أمر الخدمة نفسه، أو يمكنك إلغاء أوامر خدمة متعددة من خلال تشغيل مهمة دورية.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a3aa1-105">لا يمكن إلغاء أوامر الخدمة إذا لم تكن مرحلة أمر الخدمة تسمح بالإلغاء، أو إذا كان أمر الخدمة يحتوي على متطلبات صنف، أو إذا كان قد تم ترحيل أمر الخدمة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="a3aa1-106">إلغاء أمر خدمة في نموذج أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="a3aa1-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="a3aa1-107">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="a3aa1-108">حدد أمر خدمة، وفي جزء الإجراءات، انقر فوق **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="a3aa1-109">إلغاء بند أمر خدمة</span><span class="sxs-lookup"><span data-stu-id="a3aa1-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="a3aa1-110">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="a3aa1-111">انقر نقراً مزدوجاً فوق أمر الخدمة الذي يحتوي على البند التي تريد إلغاؤه.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="a3aa1-112">حدد بند أمر الخدمة الذي تريد إلغاؤه، ثم انقر فوق **إلغاء بند أمر** لتغيير حالة البند إلى **تم الإلغاء**.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="a3aa1-113">للعدول عن قرار الإلغاء لأمر الخدمة وتغيير الحالة مرة أخرى إلى <STRONG>تم الإنشاء</STRONG>، انقر فوق <STRONG>إبطال الإلغاء</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="a3aa1-114">إلغاء أوامر خدمة متعددة</span><span class="sxs-lookup"><span data-stu-id="a3aa1-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="a3aa1-115">انقر فوق **إدارة الخدمة** \> **دوري** \> **أوامر الخدمات** \> **إلغاء أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="a3aa1-116">انقر فوق الزر **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="a3aa1-117">في نموذج **الاستعلام**، في عمود **المعايير** حدد أوامر الخدمة التي تريد إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="a3aa1-118">انقر فوق **موافق** لإغلاق نموذج **الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="a3aa1-119">حدد خانة الاختيار **إظهار سجل المعلومات** لإنشاء سجل معلومات يسرد أوامر الخدمة التي تم إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="a3aa1-120">حدد خانة الاختيار **‏‫إبطال الإلغاء** إذا كنت ترغب في إلغاء حالة **تم الإلغاء** لأمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="a3aa1-121">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-121">Click **OK**.</span></span>

<span data-ttu-id="a3aa1-122">يتم إلغاء أوامر الخدمة المحددة أو يتم عكس حالة تقدمها من **تم الإلغاء** إلى **قيد التقدم**.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a3aa1-123">إذا قمت بتحديد خانة الاختيار <STRONG>إبطال الإلغاء</STRONG>، يتم عكس أوامر الخدمة بحالة تقدم <STRONG>تم الإلغاء</STRONG> ولا يحدث إلغاء لأوامر الخدمة بحالة تقدم <STRONG>قيد التقدم</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a3aa1-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]