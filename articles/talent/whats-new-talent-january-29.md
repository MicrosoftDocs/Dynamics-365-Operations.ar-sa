---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (31‏ يناير 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fbbecd4e0f205c2f09ec30548756ff1a43872644
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899095"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a><span data-ttu-id="c4a40-103">ما الجديد أو المتغير في Dynamics 365 Talent‏ (31‏ يناير 2019)</span><span class="sxs-lookup"><span data-stu-id="c4a40-103">What's new or changed in Dynamics 365 Talent (January 31, 2019)</span></span>

<span data-ttu-id="c4a40-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="c4a40-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

<span data-ttu-id="c4a40-105">**الإصدار 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="c4a40-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="c4a40-106">التغييرات الرئيسية Core HR</span><span class="sxs-lookup"><span data-stu-id="c4a40-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="c4a40-107">وقت الإجازة المأخوذ على بطاقة الأفراد لا يأخذ في الاعتبار تواريخ خطة الإجازة</span><span class="sxs-lookup"><span data-stu-id="c4a40-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="c4a40-108">بالنسبة إلى أولئك الأشخاص الذين ليس لديهم أي خطط للإجازة على سنة التقويم، تعرض الآن بطاقة **مأخوذ** الإجازات المأخوذة في سنة الإجازة المحددة بواسطة خطة.</span><span class="sxs-lookup"><span data-stu-id="c4a40-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="c4a40-109">على سبيل المثال، إذا كانت فترة سنة الإجازة في المؤسسة تمتد من 1 يونيو إلى 30 مايو، وأخذ أحد الموظفين إجازة لمدة ثلاثة أيام في شهر ديسمبر، فستعرض البطاقة **مأخوذ** ثلاثة أيام في 15 يناير.</span><span class="sxs-lookup"><span data-stu-id="c4a40-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="c4a40-110">مقادير الاستحقاق غير متطابقة مع أساس تاريخ المستوى</span><span class="sxs-lookup"><span data-stu-id="c4a40-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="c4a40-111">تمت إضافة خيارات جديدة إلى الإجازة أو الغياب (معلمات **الموارد البشرية**) لتمكين العملاء من تحديد الوقت الذي يكون فيه تاريخ أشهر خدمة الموظف ساري المفعول.</span><span class="sxs-lookup"><span data-stu-id="c4a40-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="c4a40-112">بالنسبة إلى بعض المؤسسات، التاريخ هو نهاية الشهر، وقد يكون بداية الشهر التالي بالنسبة إلى البعض الآخر.</span><span class="sxs-lookup"><span data-stu-id="c4a40-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="c4a40-113">على سبيل المثال، قد تمنح إحدى المؤسسات إجازة يوم 31 ديسمبر، في حين أن مؤسسة أخرى قد تمنح إجازة يوم 1 يناير.</span><span class="sxs-lookup"><span data-stu-id="c4a40-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="c4a40-114">سيسمح لك هذا الخيار بتحديد وقت منح هذه الإجازة.</span><span class="sxs-lookup"><span data-stu-id="c4a40-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="c4a40-115">إجراءات توظيف العاملين عالقة في الحالة "اكتمال سير العمل"</span><span class="sxs-lookup"><span data-stu-id="c4a40-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="c4a40-116">تم إدخال تغييرات لتصحيح مشكلة حيث انتهى عدد صغير من مهام سير العمل مع الحالة "اكتمال سير العمل".</span><span class="sxs-lookup"><span data-stu-id="c4a40-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="c4a40-117">يجب أن تنتقل الآن مهام سير العمل الجديدة إلى الحالة "مكتمل" عند انتهاء سير العمل.</span><span class="sxs-lookup"><span data-stu-id="c4a40-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="c4a40-118">وسيتم نقل مهام سير العمل في الحالة "اكتمال سير العمل" إلى الحالة "خطأ" للسماح بالتحديث أو الإزالة، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="c4a40-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
