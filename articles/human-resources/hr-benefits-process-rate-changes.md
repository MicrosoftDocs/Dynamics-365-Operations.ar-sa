---
title: معالجة تغييرات المعدل
description: قم بمعالجة تغييرات معدل الميزة في Microsoft Dynamics 365 Human Resources عندما تحتوي خطة ميزة جديدة أو حالية في إعدادات قاعدة الأهلية.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: da42ef6ea91b95903316e35b551b222b8ff3b946
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417084"
---
# <a name="process-rate-changes"></a><span data-ttu-id="0af44-103">معالجة تغييرات المعدل</span><span class="sxs-lookup"><span data-stu-id="0af44-103">Process rate changes</span></span>

<span data-ttu-id="0af44-104">قم بمعالجة تغييرات معدل الميزة في Microsoft Dynamics 365 Human Resources عندما تحتوي خطة ميزة جديدة أو حالية في إعدادات قاعدة الأهلية.</span><span class="sxs-lookup"><span data-stu-id="0af44-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="0af44-105">إذا تم إنشاء قاعدة أهلية جديدة وتعيينها إلى الخطة، فإن هذا سيطالب النظام بإعادة تشغيل أهلية العامل للتحقق مما إذا كان من الممكن تأهيل العاملين الآن للخطة بناءً على خيارات الأهلية الجديدة.</span><span class="sxs-lookup"><span data-stu-id="0af44-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="0af44-106">في مساحة العمل **إدارة الميزات**، ضمن **معالجة**، حدد **معالجة تحديث تغيير المعدل**.</span><span class="sxs-lookup"><span data-stu-id="0af44-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="0af44-107">في مربع الحوار **تشغيل معالجة معدل الميزة**، حدد قيم الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="0af44-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="0af44-108">الحقل</span><span class="sxs-lookup"><span data-stu-id="0af44-108">Field</span></span> | <span data-ttu-id="0af44-109">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="0af44-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="0af44-110">**فترة التسجيل**</span><span class="sxs-lookup"><span data-stu-id="0af44-110">**Enrollment period**</span></span> | <span data-ttu-id="0af44-111">تغييرات المعدل المراد معالجة الأحداث الحياتية خلالها.</span><span class="sxs-lookup"><span data-stu-id="0af44-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="0af44-112">إذا كنت ترغب في تشغيل العملية في الخلفية، حدد **تشغيل في الخلفية** وقم بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="0af44-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="0af44-113">إدخال المعلومات للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="0af44-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="0af44-114">لإعداد مهمة متكررة، حدد **التكرار**، وادخل معلومات التكرار، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0af44-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="0af44-115">لإعداد تنبيه بالمهمة، حدد **التنبيهات**، وحدد التنبيهات المراد استلامها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0af44-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="0af44-116">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0af44-116">Select **OK**.</span></span> <span data-ttu-id="0af44-117">سيتم تشغيل العملية باستخدام المعلمات التي قمت بتعيينها.</span><span class="sxs-lookup"><span data-stu-id="0af44-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="0af44-118">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0af44-118">Select **OK**.</span></span>
