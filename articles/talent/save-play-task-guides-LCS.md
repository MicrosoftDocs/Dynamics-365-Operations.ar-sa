---
title: "حفظ دلائل المهام في LCS وإعادة تشغيلها"
description: "يتناول هذا الموضوع كيفية حفظ أدلة المهام إلى Microsoft Dynamics Lifecycle Services (LCS) وإعادة تشغيلهم."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.contentlocale: ar-sa
ms.lasthandoff: 12/04/2018

---

# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="3581f-103">حفظ دلائل المهام في LCS وإعادة تشغيلها</span><span class="sxs-lookup"><span data-stu-id="3581f-103">Save task guides to LCS and replay them</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3581f-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="3581f-104">**Environment details**</span></span> 

<span data-ttu-id="3581f-105">Microsoft Dynamics 365 for Talent، الذي تم نشره من خلال Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="3581f-105">Microsoft Dynamics 365 for Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="3581f-106">**المشكلة**</span><span class="sxs-lookup"><span data-stu-id="3581f-106">**Issue**</span></span>

<span data-ttu-id="3581f-107">يرغب العميل في حفظ تسجيلات مهام جديدة لمشروع LCS الخاص به، ثم يُعيد تشغيل أدلة المهام المحفوظة.</span><span class="sxs-lookup"><span data-stu-id="3581f-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="3581f-108">**‏‏الدقة**</span><span class="sxs-lookup"><span data-stu-id="3581f-108">**Resolution**</span></span>

<span data-ttu-id="3581f-109">اتبع هذه الخطوات لحفظ تسجل المهام إلى LCS.</span><span class="sxs-lookup"><span data-stu-id="3581f-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="3581f-110">تسجيل الدخول إلى LCS، وتحديد المشروع.</span><span class="sxs-lookup"><span data-stu-id="3581f-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="3581f-111">حدد تجانب **أداة تكوين عمليات الأعمال**.</span><span class="sxs-lookup"><span data-stu-id="3581f-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="3581f-112">عرض الصفحة في "تجربة عارض العمليات التجارية (BPM) المُحدّثة."</span><span class="sxs-lookup"><span data-stu-id="3581f-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="3581f-113">حدد مكتبة، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="3581f-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="3581f-114">أدخل اسمًا لنموذج أداة تكوين عمليات الأعمال (BPM).</span><span class="sxs-lookup"><span data-stu-id="3581f-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="3581f-115">سجل الدخول إلى Talent من LCS.</span><span class="sxs-lookup"><span data-stu-id="3581f-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="3581f-116">في حقل **بحث**، أدخل **تعليمات**.</span><span class="sxs-lookup"><span data-stu-id="3581f-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="3581f-117">تم فتح تعليمات Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="3581f-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="3581f-118">حدد زر **تحديث** لتكوين تعليمات Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="3581f-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="3581f-119">يجب أن تظهر مكتبة عارض العمليات التجارية (BPM) الخاص بك، ويجب أن يكون نشطًا.</span><span class="sxs-lookup"><span data-stu-id="3581f-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="3581f-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3581f-120">Close the page.</span></span>
10. <span data-ttu-id="3581f-121">إنشاء تسجيل مهام.</span><span class="sxs-lookup"><span data-stu-id="3581f-121">Create a task recording.</span></span>
11. <span data-ttu-id="3581f-122">عند الانتهاء، حدد **حفظ إلى Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="3581f-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![حفظ إلى Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="3581f-124">حدد مكتبة عارض العمليات التجارية (BPM) وعقدة لحفظ تسجيل المهمة للعقدة.</span><span class="sxs-lookup"><span data-stu-id="3581f-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="3581f-125">اتبع هذه الخطوات لإعادة تشغيل دليل المهام من LCS.</span><span class="sxs-lookup"><span data-stu-id="3581f-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="3581f-126">بدء مسجل المهام.</span><span class="sxs-lookup"><span data-stu-id="3581f-126">Start Task recorder.</span></span>
2. <span data-ttu-id="3581f-127">حدد **فتح من LCS**.</span><span class="sxs-lookup"><span data-stu-id="3581f-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="3581f-128">حدد المكتبة وعقدة عارض العمليات التجارية التي تحتوي على دليل مهام محفوظ.</span><span class="sxs-lookup"><span data-stu-id="3581f-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="3581f-129">فتح دليل المهام.</span><span class="sxs-lookup"><span data-stu-id="3581f-129">Open the task guide.</span></span>

