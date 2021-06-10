---
title: تحسين الأداء باستخدام مهام التنظيف التلقائية
description: يتناول هذا المقال كيفية حل بعض مشكلات الأداء باستخدام Microsoft Dynamics 365 Human Resources عن طريق تنظيف سجل الوظائف الدفعية.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6a9e94e282aa8f101b42c1378ef21c6c1fe0477e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053481"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="c5931-103">تحسين الأداء باستخدام تنظيف المهام تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="c5931-103">Optimize performance with auto cleanup tasks</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c5931-104">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="c5931-104">**Issue**</span></span>

<span data-ttu-id="c5931-105">يمكن أن يواجه Microsoft Dynamics 365 Human Resources مشكلات في الأداء إذا زاد حجم سجل الوظائف الدفعية بدرجة كبيرة.</span><span class="sxs-lookup"><span data-stu-id="c5931-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="c5931-106">**السبب**</span><span class="sxs-lookup"><span data-stu-id="c5931-106">**Cause**</span></span>

<span data-ttu-id="c5931-107">قد تؤدي المهام الدفعية التي تعمل بشكل متكرر إلى زيادة مستدامة في سجل الوظائف الدفعية.</span><span class="sxs-lookup"><span data-stu-id="c5931-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="c5931-108">يمكن أن يسبب هذا مشاكل في الأداء.</span><span class="sxs-lookup"><span data-stu-id="c5931-108">This can cause performance issues.</span></span> 

<span data-ttu-id="c5931-109">**الدقة**</span><span class="sxs-lookup"><span data-stu-id="c5931-109">**Resolution**</span></span>

<span data-ttu-id="c5931-110">قم بجدولة مهمة تلقائية لتنظيف سجل الوظائف الدفعيه الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c5931-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="c5931-111">نوصي بإعداد المهمة لتعمل أسبوعيًا، ولكن قد تحتاج إلى تشغيل التنظيف على نحو أكثر تكرارًا أو أقل تكرارًا، وفقًا للبيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c5931-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="c5931-112">يحتوي الإجراء التالي على الإعدادات المستحسنة الخاصة بنا، ولكن يمكنك تغيير هذه الإعدادات وفقًا لاحتياجاتك.</span><span class="sxs-lookup"><span data-stu-id="c5931-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="c5931-113">في Human Resources، حدد **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="c5931-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="c5931-114">في شريط **البحث**، أدخل **‏‫تنظيف محفوظات الوظيفة الدُفعية**.</span><span class="sxs-lookup"><span data-stu-id="c5931-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![بحث عن تنظيف سجل الوظائف الدفعية](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="c5931-116">في **حد السجل (أيام)**، أدخل **30**.</span><span class="sxs-lookup"><span data-stu-id="c5931-116">In **History limit (days)**, enter **30**.</span></span>

   ![قم بتعيين حد السجل إلى 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="c5931-118">حدد **تشغيل في الخلفية** ثم حدد **التكرار**.</span><span class="sxs-lookup"><span data-stu-id="c5931-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![تعيين التكرار](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="c5931-120">ضمن **تعريف التكرار**، قم بتعيين **تاريخ البدء** و **وقت البدء** بحيث يقعان خلال ساعات التوقف عن العمل أو عطلة نهاية الأسبوع، ثم حدد **بلا تاريخ انتهاء**.</span><span class="sxs-lookup"><span data-stu-id="c5931-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![تعيين تاريخ بدء التكرار ووقته](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="c5931-122">ضمن **نمط التكرار**، حدد **أيام** وقم بتعيين **‏‫تكرار بعد الفترة المحددة** إلى **7**.</span><span class="sxs-lookup"><span data-stu-id="c5931-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![تعيين التنظيف ليتكرر أسبوعيًا](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="c5931-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c5931-124">Select **OK**.</span></span>

8. <span data-ttu-id="c5931-125">قم بتغيير إية معلمات أخرى ضمن **تشغيل في الخلفية** عند الضرورة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c5931-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]