---
title: حفظ دلائل المهام في LCS وإعادة تشغيلها
description: يتناول هذا المقال كيفية حفظ أدلة المهام إلى Microsoft Dynamics Lifecycle Services (LCS) ثم إعادة تشغيلها.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c81c345932e0e3dce4b13104222ed9f668a3c460
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111402"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="6d722-103">حفظ دلائل المهام في LCS وإعادة تشغيلها</span><span class="sxs-lookup"><span data-stu-id="6d722-103">Save task guides to LCS and replay them</span></span>

<span data-ttu-id="6d722-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="6d722-104">**Environment details**</span></span> 

<span data-ttu-id="6d722-105">Microsoft Dynamics 365 Human Resources، الذي تم نشره عبر Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="6d722-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="6d722-106">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="6d722-106">**Issue**</span></span>

<span data-ttu-id="6d722-107">يرغب العميل في حفظ تسجيلات مهام جديدة لمشروع LCS الخاص به، ثم يُعيد تشغيل أدلة المهام المحفوظة.</span><span class="sxs-lookup"><span data-stu-id="6d722-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="6d722-108">**‏‏الدقة**</span><span class="sxs-lookup"><span data-stu-id="6d722-108">**Resolution**</span></span>

<span data-ttu-id="6d722-109">اتبع هذه الخطوات لحفظ تسجل المهام إلى LCS.</span><span class="sxs-lookup"><span data-stu-id="6d722-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="6d722-110">تسجيل الدخول إلى LCS، وتحديد المشروع.</span><span class="sxs-lookup"><span data-stu-id="6d722-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="6d722-111">حدد تجانب **أداة تكوين عمليات الأعمال**.</span><span class="sxs-lookup"><span data-stu-id="6d722-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="6d722-112">عرض الصفحة في "تجربة عارض العمليات التجارية (BPM) المُحدّثة."</span><span class="sxs-lookup"><span data-stu-id="6d722-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="6d722-113">حدد مكتبة، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="6d722-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="6d722-114">أدخل اسمًا لنموذج أداة تكوين عمليات الأعمال (BPM).</span><span class="sxs-lookup"><span data-stu-id="6d722-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="6d722-115">تسجيل الدخول إلى Human Resources من LCS.</span><span class="sxs-lookup"><span data-stu-id="6d722-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="6d722-116">في حقل **بحث**، أدخل **تعليمات**.</span><span class="sxs-lookup"><span data-stu-id="6d722-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="6d722-117">تم فتح تعليمات Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="6d722-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="6d722-118">حدد زر **تحديث** لتكوين تعليمات Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="6d722-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="6d722-119">يجب أن تظهر مكتبة عارض العمليات التجارية (BPM) الخاص بك، ويجب أن يكون نشطًا.</span><span class="sxs-lookup"><span data-stu-id="6d722-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="6d722-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6d722-120">Close the page.</span></span>
10. <span data-ttu-id="6d722-121">إنشاء تسجيل مهام.</span><span class="sxs-lookup"><span data-stu-id="6d722-121">Create a task recording.</span></span>
11. <span data-ttu-id="6d722-122">عند الانتهاء، حدد **حفظ إلى Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="6d722-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![حفظ إلى Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="6d722-124">حدد مكتبة عارض العمليات التجارية (BPM) وعقدة لحفظ تسجيل المهمة للعقدة.</span><span class="sxs-lookup"><span data-stu-id="6d722-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="6d722-125">اتبع هذه الخطوات لإعادة تشغيل دليل المهام من LCS.</span><span class="sxs-lookup"><span data-stu-id="6d722-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="6d722-126">بدء مسجل المهام.</span><span class="sxs-lookup"><span data-stu-id="6d722-126">Start Task recorder.</span></span>
2. <span data-ttu-id="6d722-127">حدد **فتح من LCS**.</span><span class="sxs-lookup"><span data-stu-id="6d722-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="6d722-128">حدد المكتبة وعقدة عارض العمليات التجارية التي تحتوي على دليل مهام محفوظ.</span><span class="sxs-lookup"><span data-stu-id="6d722-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="6d722-129">فتح دليل المهام.</span><span class="sxs-lookup"><span data-stu-id="6d722-129">Open the task guide.</span></span>
