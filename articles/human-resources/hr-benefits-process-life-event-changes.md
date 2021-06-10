---
title: معالجة تغييرات الأحداث الحياتية
description: معالجة تغييرات الأحداث الحياتية في Microsoft Dynamics 365 Human Resources للتغييرات الخاصة بالحدث الحياتي.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1bfbd7347581e57edcab39a675b17ef66e262582
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059006"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="af658-103">معالجة تغييرات الأحداث الحياتية</span><span class="sxs-lookup"><span data-stu-id="af658-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="af658-104">معالجة تغييرات الأحداث الحياتية في Microsoft Dynamics 365 Human Resources للتغييرين الخاصين بالحدث الحياتي.</span><span class="sxs-lookup"><span data-stu-id="af658-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="af658-105">تغييرات عيد الميلاد</span><span class="sxs-lookup"><span data-stu-id="af658-105">Birthday changes</span></span>
- <span data-ttu-id="af658-106">تتجاوز قاعدة الأهلية‬ تغييرات انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="af658-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="af658-107">في مساحة العمل **إدارة الميزات**، تحت **معالجة**، حدد **معالجة تغيير الحدث الحياتي**.</span><span class="sxs-lookup"><span data-stu-id="af658-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="af658-108">في مربع الحوار **تشغيل معالجة تغيير الحدث الحياتي**، حدد قيم الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="af658-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="af658-109">الحقل</span><span class="sxs-lookup"><span data-stu-id="af658-109">Field</span></span> | <span data-ttu-id="af658-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="af658-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="af658-111">فترة التسجيل</span><span class="sxs-lookup"><span data-stu-id="af658-111">Enrollment period</span></span> | <span data-ttu-id="af658-112">فترة التسجيل المراد تغيير معالجة الأحداث الحياتية بها.</span><span class="sxs-lookup"><span data-stu-id="af658-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="af658-113">كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="af658-113">Legal entity</span></span> | <span data-ttu-id="af658-114">الكيان القانوني المراد تغيير معالجة الأحداث الحياتية له.</span><span class="sxs-lookup"><span data-stu-id="af658-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="af658-115">إذا كنت ترغب في تشغيل العملية في الخلفية، حدد **تشغيل في الخلفية** وقم بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="af658-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="af658-116">إدخال المعلومات للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="af658-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="af658-117">لإعداد مهمة متكررة، حدد **التكرار**، وادخل معلومات التكرار، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="af658-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="af658-118">لإعداد تنبيه بالمهمة، حدد **التنبيهات**، وحدد التنبيهات المراد استلامها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="af658-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="af658-119">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="af658-119">Select **OK**.</span></span> <span data-ttu-id="af658-120">سيتم تشغيل العملية باستخدام المعلمات التي قمت بتعيينها.</span><span class="sxs-lookup"><span data-stu-id="af658-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="af658-121">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="af658-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]