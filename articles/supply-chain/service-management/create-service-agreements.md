---
title: "إنشاء اتفاقيات خدمات"
description: "يوضح هذا الموضوع كيفية استخدام الميزات الموجودة في إدارة الخدمة وإدارة المشروع والوحدات النمطية المحاسبية لإنشاء اتفاقيات الخدمة."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2a46173a3566a56a21add9d42c111d456b1ae7c1
ms.openlocfilehash: 517bc1b9de9b2512f42e4f32b4a19e517e349e8e
ms.contentlocale: ar-sa
ms.lasthandoff: 02/19/2018

---

# <a name="create-service-agreements"></a><span data-ttu-id="8f426-103">إنشاء اتفاقيات خدمات</span><span class="sxs-lookup"><span data-stu-id="8f426-103">Create service agreements</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8f426-104">يوضح هذا الموضوع كيفية استخدام الميزات الموجودة في إدارة الخدمة وإدارة المشروع والوحدات النمطية المحاسبية لإنشاء اتفاقيات الخدمة.</span><span class="sxs-lookup"><span data-stu-id="8f426-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="8f426-105">إنشاء اتفاقية خدمة من إدارة الخدمة</span><span class="sxs-lookup"><span data-stu-id="8f426-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="8f426-106">انتقل إلى **إدارة الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="8f426-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="8f426-107">انقر فوق **اتفاقيات الخدمة** لإنشاء بند اتفاقية خدمة جديد في رأس الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8f426-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="8f426-108">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8f426-108">Click **New**.</span></span> <span data-ttu-id="8f426-109">أدخل وصفًا، ثم حدد مرجعًا للمشروع في الحقل **معرّف المشروع**، ثم قم بملء باقي الحقول والبنود الخاصة باتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="8f426-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="8f426-110">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8f426-110">Click **Save**.</span></span>
4. <span data-ttu-id="8f426-111">انقر فوق علامة التبويب **علاقات**، ثم حدد **كائنات الخدمة** أو **مهام الخدمة** لإنشاء علاقات كائنات الخدمة أو علاقات مهام الخدمة لاتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="8f426-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="8f426-112">يمكن إرفاق كائنات ومهام الخدمة التي قمت بإنشاء علاقات لها ببنود اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="8f426-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="8f426-113">في النصف السفلي من الصفحة، أنشئ بنود اتفاقية الخدمة عن طريق نسخ البنود من قالب الخدمة أو اتفاقية خدمة أخرى أو عن طريق إنشاء بنود اتفاقية الخدمة يدويًا.</span><span class="sxs-lookup"><span data-stu-id="8f426-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="8f426-114">إذا قمت بنسخ بنود في اتفاقية الخدمة من اتفاقية خدمة أخرى، فيمكنك الإشارة إلى ما إذا كنت ترغب أيضًا في نسخ علاقات كائنات الخدمة ومهام الخدمة.</span><span class="sxs-lookup"><span data-stu-id="8f426-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="8f426-115">وإذا قمت بنسخ هذه العلاقات، فستتم إضافتها إلى أية علاقات موجودة في اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="8f426-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="8f426-116">وإذا قمت بنسخ بنود اتفاقية الخدمة من قالب خدمة، فسيتم نسخ علاقات كائنات الخدمة ومهام الخدمة تلقائيًا كعلاقات كائنات خدمة وعلاقات مهام خدمة في بنود اتفاقية الخدمة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="8f426-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="8f426-117">إنشاء بنود اتفاقية خدمة يدويًا</span><span class="sxs-lookup"><span data-stu-id="8f426-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="8f426-118">من صفحة **اتفاقيات الخدمات**، قم بإضافة بند اتفاقية خدمة في شبكة البنود.</span><span class="sxs-lookup"><span data-stu-id="8f426-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="8f426-119">قم بإدخال المعلومات المناسبة لبند اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="8f426-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="8f426-120">اضغط على **CTRL+S** لحفظ البند ثم أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8f426-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="8f426-121">إنشاء اتفاقية خدمة من مشروع</span><span class="sxs-lookup"><span data-stu-id="8f426-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="8f426-122">انقر فوق **إدارة المشاريع ومحاسبتها**.</span><span class="sxs-lookup"><span data-stu-id="8f426-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="8f426-123">انقر فوق **جميع المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="8f426-123">Click **All projects**.</span></span>
3. <span data-ttu-id="8f426-124">حدد المشروع من القائمة.</span><span class="sxs-lookup"><span data-stu-id="8f426-124">Select the project from the list.</span></span>
4. <span data-ttu-id="8f426-125">في **جزء الإجراءات**، انقر فوق **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="8f426-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="8f426-126">في مجموعة الإجراءات **جديد**، انقر فوق **خدمة** وحدد **اتفاقية الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="8f426-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="8f426-127">اتبع الخطوات الموجودة في القسم المعنون **إنشاء اتفاقية خدمة** كما هو موضح سابقًا في هذا الموضوع لإدخال مرجع المشروع.</span><span class="sxs-lookup"><span data-stu-id="8f426-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="8f426-128">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="8f426-128">Related topics</span></span>

[<span data-ttu-id="8f426-129">اتفاقيات الخدمة</span><span class="sxs-lookup"><span data-stu-id="8f426-129">Service agreements</span></span>](service-agreements.md)


