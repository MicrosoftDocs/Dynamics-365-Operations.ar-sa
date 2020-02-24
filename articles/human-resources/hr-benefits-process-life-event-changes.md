---
title: معالجة تغييرات الأحداث الحياتية
description: معالجة تغييرات الأحداث الحياتية في Microsoft Dynamics 365 Human Resources للتغييرات الخاصة بالحدث الحياتي.
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
ms.openlocfilehash: f9bce9394a361bbecfcc0531c5d7ebe9302c8f11
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007971"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="dc623-103">معالجة تغييرات الأحداث الحياتية</span><span class="sxs-lookup"><span data-stu-id="dc623-103">Process life event changes</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="dc623-104">معالجة تغييرات الأحداث الحياتية في Microsoft Dynamics 365 Human Resources للتغييرين الخاصين بالحدث الحياتي.</span><span class="sxs-lookup"><span data-stu-id="dc623-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="dc623-105">تغييرات عيد الميلاد</span><span class="sxs-lookup"><span data-stu-id="dc623-105">Birthday changes</span></span>
- <span data-ttu-id="dc623-106">تتجاوز قاعدة الأهلية‬ تغييرات انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="dc623-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="dc623-107">في مساحة العمل **إدارة الميزات** ، تحت **معالجة**، حدد **معالجة تغيير الحدث الحياتي**.</span><span class="sxs-lookup"><span data-stu-id="dc623-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="dc623-108">في مربع الحوار **تشغيل معالجة تغيير الحدث الحياتي** ، حدد قيم الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="dc623-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="dc623-109">الحقل</span><span class="sxs-lookup"><span data-stu-id="dc623-109">Field</span></span> | <span data-ttu-id="dc623-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="dc623-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="dc623-111">فترة التسجيل</span><span class="sxs-lookup"><span data-stu-id="dc623-111">Enrollment period</span></span> | <span data-ttu-id="dc623-112">فترة التسجيل المراد تغيير معالجة الأحداث الحياتية بها.</span><span class="sxs-lookup"><span data-stu-id="dc623-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="dc623-113">كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="dc623-113">Legal entity</span></span> | <span data-ttu-id="dc623-114">الكيان القانوني المراد تغيير معالجة الأحداث الحياتية له.</span><span class="sxs-lookup"><span data-stu-id="dc623-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="dc623-115">إذا كنت ترغب في تشغيل العملية في الخلفية ، حدد **تشغيل في الخلفية** وقم بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="dc623-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="dc623-116">إدخال المعلومات للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="dc623-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="dc623-117">لإعداد مهمة متكررة، حدد **التكرار**، وادخل معلومات التكرار، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="dc623-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="dc623-118">لإعداد تنبيه بالمهمة، حدد **التنبيهات**، وحدد التنبيهات المراد استلامها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="dc623-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="dc623-119">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="dc623-119">Select **OK**.</span></span> <span data-ttu-id="dc623-120">سيتم تشغيل العملية باستخدام المعلمات التي قمت بتعيينها.</span><span class="sxs-lookup"><span data-stu-id="dc623-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="dc623-121">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="dc623-121">Select **OK**.</span></span>
