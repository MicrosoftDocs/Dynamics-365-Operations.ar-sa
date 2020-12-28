---
title: التكامل للمشاريع واتفاقيات الخدمات
description: عند التعامل مع اتفاقيات الخدمة وبنود اتفاقيات الخدمات، يتم استخدام البيانات التي تم إعدادها في المناطق في إدارة المشاريع ومحاسبتها.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 578e4b9fe5ef487e999fd0de28d7566bad21fd89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421587"
---
# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="11d38-103">التكامل للمشاريع واتفاقيات الخدمات</span><span class="sxs-lookup"><span data-stu-id="11d38-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="11d38-104">عند التعامل مع اتفاقيات الخدمة وبنود اتفاقيات الخدمات، يتم استخدام البيانات التي تم إعدادها في المناطق التالية في **إدارة المشاريع ومحاسبتها**.</span><span class="sxs-lookup"><span data-stu-id="11d38-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="11d38-105">أسعار المشاريع</span><span class="sxs-lookup"><span data-stu-id="11d38-105">Project prices</span></span>

<span data-ttu-id="11d38-106">يتم اشتقاق سعر التكلفة والمبيعات لحركة اتفاقية خدمة من إعداد سعر التكلفة الذي ينطبق على المشروع الذي تم إرفاقه باتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="11d38-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="11d38-107">ويمكن إعداد أسعار التكلفة والمبيعات حسب المشروع والموظف والفئة.</span><span class="sxs-lookup"><span data-stu-id="11d38-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="11d38-108">التحقق من صحة المشروع</span><span class="sxs-lookup"><span data-stu-id="11d38-108">Project validation</span></span>

<span data-ttu-id="11d38-109">يمكن تقييد المشاريع والموظفين والفئات التي تكون متاحة للتحديد في بند اتفاقية الخدمة عن طريق إعداد التحقق من الصحة في **إدارة المشاريع ومحاسبتها**.</span><span class="sxs-lookup"><span data-stu-id="11d38-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="11d38-110">ويمكن باستخدام إعداد التحقق من الصحة تجميع الموظفين والمشاريع والفئات لأجل التحكم بالوصول.</span><span class="sxs-lookup"><span data-stu-id="11d38-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="11d38-111">خصائص بند المشروع</span><span class="sxs-lookup"><span data-stu-id="11d38-111">Project line properties</span></span>

<span data-ttu-id="11d38-112">يتم إدخال خاصية بند لبند اتفاقية الخدمة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="11d38-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="11d38-113">يتم إنشاء خواص البنود في نموذج **خواص البنود** في **إدارة المشاريع والمحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="11d38-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="11d38-114">يتم إرفاق خاصية البند التي تم إدخالها في اتفاقية الخدمة بالمشروع الذي تم تحديده لاتفاقية الخدمة وبالتالي يتم استيراده عن طريق بند اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="11d38-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="11d38-115">حسابات مقابلة افتراضية</span><span class="sxs-lookup"><span data-stu-id="11d38-115">Default offset accounts</span></span>

<span data-ttu-id="11d38-116">إذا تم إدخال حركة مصروفات، فسيتم تلقائيًا تحديد حساب مقابل افتراضي للمصروفات للحركة.</span><span class="sxs-lookup"><span data-stu-id="11d38-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="11d38-117">ويتم إعداد حساب المصروفات الافتراضي للمشروع الذي تم إرفاقه باتفاقية الخدمة الحالية.</span><span class="sxs-lookup"><span data-stu-id="11d38-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="11d38-118">فئات المشروع</span><span class="sxs-lookup"><span data-stu-id="11d38-118">Project categories</span></span>

<span data-ttu-id="11d38-119">يتم إعداد الفئات المتاحة لبنود اتفاقية الخدمة في النموذج **فئات المشروع** في **إدارة المشاريع ومحاسبتها**.</span><span class="sxs-lookup"><span data-stu-id="11d38-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="11d38-120">تتوفر الفئات التي تم تحديد خانة اختيار <STRONG>نشط في دفاتر اليومية</STRONG> بالنسبة لها في علامة تبويب <STRONG>المشروع</STRONG> في نموذج <STRONG>فئات المشروع</STRONG> للتحديد.</span><span class="sxs-lookup"><span data-stu-id="11d38-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="11d38-121">ومع ذلك، إذا تم تحديد خانة اختيار <STRONG>فئات غير نشطة</STRONG> في علامة تبويب <STRONG>دفاتر يومية</STRONG> في نموذج <STRONG>محددات إدارة المشاريع والمحاسبة</STRONG>، فإن كل الفئات تصبح متوفرة للتحديد.</span><span class="sxs-lookup"><span data-stu-id="11d38-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="11d38-122">محددات المشروع</span><span class="sxs-lookup"><span data-stu-id="11d38-122">Project parameters</span></span>

<span data-ttu-id="11d38-123">إذا كان حقل **عاملون تم إنهاء خدمتهم** في علامة تبويب **دفاتر يومية** في نموذج **محددات إدارة المشاريع والمحاسبة** محدداً، فيمكنك تحديد الموظفين غير النشطين والموظفين النشطين في نماذج **اتفاقيات الخدمة** و **أوامر الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="11d38-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="11d38-124">أيضًا، يمكنك تمكين حقلي **وقت البدء** و **وقت الانتهاء** في علامة تبويب **المشروع** في نموذج **أوامر الخدمة** لإدخال أوقات البدء والانتهاء لبنود أوامر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="11d38-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="11d38-125">تمكين ميزة أوقات البدء والانتهاء لأوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="11d38-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="11d38-126">انقر فوق **إدارة المشاريع‬ والمحاسبة** \> **الإعدادات** \> **محددات إدارة المشاريع‬ والمحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="11d38-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="11d38-127">انقر فوق علامة تبويب **دفاتر يومية** ثم حدد خانة الاختيار **إظهار أوقات البدء/الانتهاء**.</span><span class="sxs-lookup"><span data-stu-id="11d38-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="11d38-128">‏‫انقر فوق **‏‫إدارة المشاريع والمحاسبة** \> **الإعداد** \> **دفاتر اليومية‬** \> **أسماء دفاتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="11d38-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="11d38-129">حدد اسم دفتر اليومية الذي تم إرفاقه بأمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="11d38-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="11d38-130">انقر فوق علامة تبويب **عام**، ثم حدد خانة الاختيار **إظهار أوقات البدء/الانتهاء**.</span><span class="sxs-lookup"><span data-stu-id="11d38-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="11d38-131">حدد اسم دفتر اليومية لأمر الخدمة في الحقل <STRONG>الساعة</STRONG> في علامة التبويب <STRONG>دفاتر اليومية</STRONG> في النموذج <STRONG>محددات إدارة الخدمة</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="11d38-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>





