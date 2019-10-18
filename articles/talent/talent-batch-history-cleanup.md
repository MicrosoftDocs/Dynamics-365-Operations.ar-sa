---
title: تحسين الأداء باستخدام تنظيف المهام تلقائيًا
description: يوضح هذا الموضوع كيفية حل بعض مشكلات الأداء باستخدام Dynamics 365 Talent عن طريق تنظيف سجل الوظائف الدفعية.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 1e9d237817024800ad9880ec58db3505ac1c493f
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2027074"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="5be82-103">تحسين الأداء باستخدام تنظيف المهام تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="5be82-103">Optimize performance with auto cleanup tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5be82-104">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="5be82-104">**Issue**</span></span>

<span data-ttu-id="5be82-105">يمكن أن يواجه Microsoft Dynamics 365 Talent مشكلات في الأداء إذا زاد حجم سجل الوظائف الدفعية بدرجة كبيرة.</span><span class="sxs-lookup"><span data-stu-id="5be82-105">Microsoft Dynamics 365 Talent can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="5be82-106">**السبب**</span><span class="sxs-lookup"><span data-stu-id="5be82-106">**Cause**</span></span>

<span data-ttu-id="5be82-107">قد تؤدي المهام الدفعية التي تعمل بشكل متكرر إلى زيادة مستدامة في سجل الوظائف الدفعية.</span><span class="sxs-lookup"><span data-stu-id="5be82-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="5be82-108">يمكن أن يسبب هذا مشاكل في الأداء.</span><span class="sxs-lookup"><span data-stu-id="5be82-108">This can cause performance issues.</span></span> 

<span data-ttu-id="5be82-109">**الدقة**</span><span class="sxs-lookup"><span data-stu-id="5be82-109">**Resolution**</span></span>

<span data-ttu-id="5be82-110">قم بجدولة مهمة تلقائية لتنظيف سجل الوظائف الدفعيه الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="5be82-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="5be82-111">نوصي بإعداد المهمة لتعمل أسبوعيًا، ولكن قد تحتاج إلى تشغيل التنظيف على نحو أكثر تكرارًا أو أقل تكرارًا، وفقًا للبيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="5be82-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="5be82-112">يحتوي الإجراء التالي على الإعدادات المستحسنة الخاصة بنا، ولكن يمكنك تغيير هذه الإعدادات وفقًا لاحتياجاتك.</span><span class="sxs-lookup"><span data-stu-id="5be82-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="5be82-113">في Talent، حدد **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="5be82-113">In Talent, select **System administration**.</span></span>

2. <span data-ttu-id="5be82-114">في شريط **البحث**، أدخل **‏‫تنظيف محفوظات الوظيفة الدُفعية**.</span><span class="sxs-lookup"><span data-stu-id="5be82-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![بحث عن تنظيف سجل الوظائف الدفعية](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="5be82-116">في **حد السجل (أيام)**، أدخل **30**.</span><span class="sxs-lookup"><span data-stu-id="5be82-116">In **History limit (days)**, enter **30**.</span></span>

   ![قم بتعيين حد السجل إلى 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="5be82-118">حدد **تشغيل في الخلفية** ثم حدد **التكرار**.</span><span class="sxs-lookup"><span data-stu-id="5be82-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![تعيين التكرار](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="5be82-120">ضمن **تعريف التكرار**، قم بتعيين **تاريخ البدء** و**وقت البدء** بحيث يقعان خلال ساعات التوقف عن العمل أو عطلة نهاية الأسبوع، ثم حدد **بلا تاريخ انتهاء**.</span><span class="sxs-lookup"><span data-stu-id="5be82-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![تعيين تاريخ بدء التكرار ووقته](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="5be82-122">ضمن **نمط التكرار**، حدد **أيام** وقم بتعيين **‏‫تكرار بعد الفترة المحددة** إلى **7**.</span><span class="sxs-lookup"><span data-stu-id="5be82-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![تعيين التنظيف ليتكرر أسبوعيًا](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="5be82-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5be82-124">Select **OK**.</span></span>

8. <span data-ttu-id="5be82-125">قم بتغيير إية معلمات أخرى ضمن **تشغيل في الخلفية** عند الضرورة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5be82-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>

