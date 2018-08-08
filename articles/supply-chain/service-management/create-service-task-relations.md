---
title: "إنشاء علاقات مهام الخدمة"
description: "يمكنك إقران مهام الخدمة باتفاقيات الخدمة أو أوامر الخدمة لأجل وصف مهمة الخدمة التي سيتم إكمالها لاتفاقية أو أمر."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2aa0e5200ff2a6822e631c72124335e2dc556c14
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="create-service-task-relations"></a><span data-ttu-id="87fb7-103">إنشاء علاقات مهام الخدمة</span><span class="sxs-lookup"><span data-stu-id="87fb7-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87fb7-104">يمكنك إقران مهام الخدمة باتفاقيات الخدمة أو أوامر الخدمة لأجل وصف مهمة الخدمة التي سيتم إكمالها لاتفاقية أو أمر.</span><span class="sxs-lookup"><span data-stu-id="87fb7-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="87fb7-105">تتوفر هذه المعلومات لكل من فنيي الخدمة والعملاء.</span><span class="sxs-lookup"><span data-stu-id="87fb7-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="87fb7-106">إنشاء علاقة مع اتفاقية خدمات</span><span class="sxs-lookup"><span data-stu-id="87fb7-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="87fb7-107">انقر فوق **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="87fb7-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="87fb7-108">حدد اتفاقية خدمات موجودة، أو قم بإنشاء اتفاقية خدمات جديدة.</span><span class="sxs-lookup"><span data-stu-id="87fb7-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="87fb7-109">في جزء الإجراءات، انقر فوق زر **مهام الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="87fb7-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="87fb7-110">في نموذج **مهام الخدمة**، اضغط على CTRL + N لإنشاء بند جديد ومن ثم حدد مهمة خدمة من قائمة **مهمة الخدمة** لإرفاق مهمة الخدمة باتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="87fb7-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="87fb7-111">في علامة تبويب **الوصف**، أدخل أية أوصاف للإشعارات سواء كانت داخلية أو خارجية في حقول النص الخالية.</span><span class="sxs-lookup"><span data-stu-id="87fb7-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="87fb7-112">أغلق النموذج لحفظ السجل.</span><span class="sxs-lookup"><span data-stu-id="87fb7-112">Close the form to save the record.</span></span>

<span data-ttu-id="87fb7-113">كرر هذا الإجراء حتى تنتهي من إنشاء كافة علاقات مهام الخدمة اللازمة لاتفاقية الخدمات.</span><span class="sxs-lookup"><span data-stu-id="87fb7-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="87fb7-114">يمكنك الآن تحديد مهام الخدمة هذه لأي من بنود الاتفاقية المرفقة.</span><span class="sxs-lookup"><span data-stu-id="87fb7-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="87fb7-115">تكون علاقة مهام الخدمة التي تم إنشاؤها في اتفاقية خدمات متوفرة في كل أوامر الخدمة المرفقة باتفاقية الخدمات.</span><span class="sxs-lookup"><span data-stu-id="87fb7-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="87fb7-116">إنشاء علاقة مع أمر خدمة</span><span class="sxs-lookup"><span data-stu-id="87fb7-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="87fb7-117">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="87fb7-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="87fb7-118">حدد أمر خدمة موجود، أو قم بإنشاء أمر خدمة جديد.</span><span class="sxs-lookup"><span data-stu-id="87fb7-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="87fb7-119">في جزء الإجراءات، انقر فوق زر **مهام الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="87fb7-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="87fb7-120">من نموذج **مهام الخدمة**، اضغط على CTRL + N لإنشاء بند جديد ومن ثم حدد مهمة خدمة من قائمة **مهمة الخدمة** لإرفاق مهام خدمة بأمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="87fb7-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="87fb7-121">في علامة تبويب **الوصف**، أدخل أية أوصاف للإشعارات سواء كانت داخلية أو خارجية في حقول النص الخالية.</span><span class="sxs-lookup"><span data-stu-id="87fb7-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="87fb7-122">أغلق النموذج لحفظ السجل.</span><span class="sxs-lookup"><span data-stu-id="87fb7-122">Close the form to save the record.</span></span>

<span data-ttu-id="87fb7-123">كرر هذا الإجراء حتى تنتهي من إنشاء كافة علاقات مهام الخدمة اللازمة لأمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="87fb7-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="87fb7-124">يمكنك الآن تحديد مهمة الخدمة التي قمت بإنشاء العلاقة لها عند إنشاء بنود أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="87fb7-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="87fb7-125">تكون علاقات مهام الخدمة التي تم إنشاؤها في أمر خدمة متوفرة في أمر الخدمة المحدد.</span><span class="sxs-lookup"><span data-stu-id="87fb7-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="87fb7-126">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="87fb7-126">See also</span></span>

[<span data-ttu-id="87fb7-127">‏‏مهام الخدمة </span><span class="sxs-lookup"><span data-stu-id="87fb7-127">Service tasks</span></span>](service-tasks.md)


  



