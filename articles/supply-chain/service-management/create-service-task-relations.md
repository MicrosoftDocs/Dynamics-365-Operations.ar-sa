---
title: إنشاء علاقات مهام الخدمة
description: يمكنك إقران مهام الخدمة باتفاقيات الخدمة أو أوامر الخدمة لأجل وصف مهمة الخدمة التي سيتم إكمالها لاتفاقية أو أمر.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea5952376fe30f489d385c8f8295fbf86f2af085
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470658"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="95bb1-103">إنشاء علاقات مهام الخدمة</span><span class="sxs-lookup"><span data-stu-id="95bb1-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95bb1-104">يمكنك إقران مهام الخدمة باتفاقيات الخدمة أو أوامر الخدمة لأجل وصف مهمة الخدمة التي سيتم إكمالها لاتفاقية أو أمر.</span><span class="sxs-lookup"><span data-stu-id="95bb1-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="95bb1-105">تتوفر هذه المعلومات لكل من فنيي الخدمة والعملاء.</span><span class="sxs-lookup"><span data-stu-id="95bb1-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="95bb1-106">إنشاء علاقة مع اتفاقية خدمات</span><span class="sxs-lookup"><span data-stu-id="95bb1-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="95bb1-107">انتقل إلى **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="95bb1-107">Go to **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="95bb1-108">حدد اتفاقية خدمات موجودة، أو قم بإنشاء اتفاقية خدمات جديدة.</span><span class="sxs-lookup"><span data-stu-id="95bb1-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="95bb1-109">في جزء الإجراءات، حدد الزر **مهام الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="95bb1-109">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="95bb1-110">في نموذج **مهام الخدمة** ، حدد **جديد** لإنشاء بند جديد ومن ثم حدد مهمة خدمة من قائمة **مهمة الخدمة** لإرفاق مهمة الخدمة باتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="95bb1-110">On the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="95bb1-111">في علامة تبويب **الوصف**، أدخل أية أوصاف للإشعارات سواء كانت داخلية أو خارجية في حقول النص الخالية.</span><span class="sxs-lookup"><span data-stu-id="95bb1-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="95bb1-112">أغلق النموذج لحفظ السجل.</span><span class="sxs-lookup"><span data-stu-id="95bb1-112">Close the form to save the record.</span></span>

<span data-ttu-id="95bb1-113">كرر هذا الإجراء حتى تنتهي من إنشاء كافة علاقات مهام الخدمة اللازمة لاتفاقية الخدمات.</span><span class="sxs-lookup"><span data-stu-id="95bb1-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="95bb1-114">يمكنك الآن تحديد مهام الخدمة هذه لأي من بنود الاتفاقية المرفقة.</span><span class="sxs-lookup"><span data-stu-id="95bb1-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="95bb1-115">تكون علاقة مهام الخدمة التي تم إنشاؤها في اتفاقية خدمات متوفرة في كل أوامر الخدمة المرفقة باتفاقية الخدمات.</span><span class="sxs-lookup"><span data-stu-id="95bb1-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="95bb1-116">إنشاء علاقة مع أمر خدمة</span><span class="sxs-lookup"><span data-stu-id="95bb1-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="95bb1-117">انتقل إلى **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="95bb1-117">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="95bb1-118">حدد أمر خدمة موجود، أو قم بإنشاء أمر خدمة جديد.</span><span class="sxs-lookup"><span data-stu-id="95bb1-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="95bb1-119">في جزء الإجراءات، حدد الزر **مهام الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="95bb1-119">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="95bb1-120">من نموذج **مهام الخدمة** ، حدد **جديد** لإنشاء بند جديد ومن ثم حدد مهمة خدمة من قائمة **مهمة الخدمة** لإرفاق مهام الخدمة بأمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="95bb1-120">From the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="95bb1-121">في علامة تبويب **الوصف**، أدخل أية أوصاف للإشعارات سواء كانت داخلية أو خارجية في حقول النص الخالية.</span><span class="sxs-lookup"><span data-stu-id="95bb1-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="95bb1-122">أغلق النموذج لحفظ السجل.</span><span class="sxs-lookup"><span data-stu-id="95bb1-122">Close the form to save the record.</span></span>

<span data-ttu-id="95bb1-123">كرر هذا الإجراء حتى تنتهي من إنشاء كافة علاقات مهام الخدمة اللازمة لأمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="95bb1-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="95bb1-124">يمكنك الآن تحديد مهمة الخدمة التي قمت بإنشاء العلاقة لها عند إنشاء بنود أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="95bb1-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="95bb1-125">تكون علاقات مهام الخدمة التي تم إنشاؤها في أمر خدمة متوفرة في أمر الخدمة المحدد.</span><span class="sxs-lookup"><span data-stu-id="95bb1-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="95bb1-126">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="95bb1-126">See also</span></span>

[<span data-ttu-id="95bb1-127">نظرة عامة على مهام الخدمة</span><span class="sxs-lookup"><span data-stu-id="95bb1-127">Service tasks overview</span></span>](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]