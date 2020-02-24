---
title: معالجة أهلية التسجيل‬
description: يوضح هذا المقال كيفية تشغيل معالجة أهلية التسجيل.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007905"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="64f22-103">معالجة أهلية التسجيل‬</span><span class="sxs-lookup"><span data-stu-id="64f22-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="64f22-104">يوضح هذا المقال كيفية تشغيل معالجة أهلية التسجيل.</span><span class="sxs-lookup"><span data-stu-id="64f22-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="64f22-105">في مساحة العمل **إدارة المزايا** ، ضمن **معالجة**، حدد **معالجة أهلية التسجيل**.</span><span class="sxs-lookup"><span data-stu-id="64f22-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="64f22-106">في مربع الحوار **تشغيل معالجة أهلية التسجيل** ، حدد قيم الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="64f22-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="64f22-107">الحقل</span><span class="sxs-lookup"><span data-stu-id="64f22-107">Field</span></span> | <span data-ttu-id="64f22-108">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="64f22-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="64f22-109">فترة التسجيل</span><span class="sxs-lookup"><span data-stu-id="64f22-109">Enrollment period</span></span> | <span data-ttu-id="64f22-110">فترة التسجيل المراد معالجة أهلية التسجيل لها.</span><span class="sxs-lookup"><span data-stu-id="64f22-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="64f22-111">كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="64f22-111">Legal entity</span></span> | <span data-ttu-id="64f22-112">الكيان القانوني المراد معالجة أهلية التسجيل له.</span><span class="sxs-lookup"><span data-stu-id="64f22-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="64f22-113">العامل</span><span class="sxs-lookup"><span data-stu-id="64f22-113">Worker</span></span> | <span data-ttu-id="64f22-114">العامل المراد معالجة أهلية التسجيل له.</span><span class="sxs-lookup"><span data-stu-id="64f22-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="64f22-115">في حالة ترك هذا الحقل فارغًا، فإنه ستتم معالجة أهلية التسجيل لكافة العاملين.</span><span class="sxs-lookup"><span data-stu-id="64f22-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="64f22-116">خطة الميزة</span><span class="sxs-lookup"><span data-stu-id="64f22-116">Benefit plan</span></span> | <span data-ttu-id="64f22-117">خطة الميزة المراد معالجة أهلية التسجيل لها.</span><span class="sxs-lookup"><span data-stu-id="64f22-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="64f22-118">إذا كنت ترغب في تشغيل العملية في الخلفية ، حدد **تشغيل في الخلفية** وقم بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="64f22-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="64f22-119">إدخال المعلومات للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="64f22-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="64f22-120">لإعداد مهمة متكررة، حدد **التكرار**، وادخل معلومات التكرار، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="64f22-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="64f22-121">لإعداد تنبيه بالمهمة، حدد **التنبيهات**، وحدد التنبيهات المراد استلامها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="64f22-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="64f22-122">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="64f22-122">Select **OK**.</span></span> <span data-ttu-id="64f22-123">سيتم تشغيل العملية باستخدام المعلمات التي قمت بتعيينها.</span><span class="sxs-lookup"><span data-stu-id="64f22-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="64f22-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="64f22-124">Select **OK**.</span></span>
