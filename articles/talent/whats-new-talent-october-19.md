---
title: ما الجديد أو المتغير في Dynamics 365 Talent - Core HR (16 اكتوبر ، 2018)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 13e89faa3f8470125010ccdb40a6f01c0a9c4fe7
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008767"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-19-2018"></a><span data-ttu-id="568a5-103">ما الجديد أو المتغير في Dynamics 365 Talent: Core HR‏ (19 أكتوبر 2018)</span><span class="sxs-lookup"><span data-stu-id="568a5-103">What's new or changed in Dynamics 365 Talent: Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="568a5-104">**الإصدار 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="568a5-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="568a5-105">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Core HR.</span><span class="sxs-lookup"><span data-stu-id="568a5-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="568a5-106">السماح للمدراء بتحديث طلبات زمن التوقف</span><span class="sxs-lookup"><span data-stu-id="568a5-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="568a5-107">قد يلزم تحديث طلبات زمن التوقف التي يقدمها الموظفون بعد حصولها على الموافقة من خلال سير العمل.</span><span class="sxs-lookup"><span data-stu-id="568a5-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="568a5-108">في كثير من الحالات، يجري المدير هذه التحديثات بالنيابة عن الموظف.</span><span class="sxs-lookup"><span data-stu-id="568a5-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="568a5-109">توفر هذه الميزة الجديدة للمدراء القدرة على تحديث طلبات زمن التوقف أو إلغاء هذه الطلبات بالنيابة عن الموظفين.</span><span class="sxs-lookup"><span data-stu-id="568a5-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="568a5-110">تتحكم المعلمة **العمل نيابة عن** بهذه القدرة، ويمكن تغييرها في صفحة **محددات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="568a5-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="568a5-111">السماح لقسم الموارد البشرية بتحديث طلبات زمن التوقف</span><span class="sxs-lookup"><span data-stu-id="568a5-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="568a5-112">وبشكل مشابه للميزة أعلاه، قد يلزم تحديث طلبات زمن التوقف التي يقدمها الموظفون بواسطة قسم الموارد البشرية بعد حصولها على الموافقة من خلال سير العمل.</span><span class="sxs-lookup"><span data-stu-id="568a5-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="568a5-113">تقدم هذه الميزة لمستخدمي قسم الموارد البشرية القدرة على تحديث طلبات زمن التوقف.</span><span class="sxs-lookup"><span data-stu-id="568a5-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="568a5-114">يتم تمكين الإمكانية في مساحة عمل **الأشخاص** وفي صفحة **العامل**، باستخدام خيار جديد يسمى **عرض زمن التوقف‬**.</span><span class="sxs-lookup"><span data-stu-id="568a5-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="568a5-115">في هذه الصفحات، يستطيع مستخدمو قسم الموارد البشرية عرض طلبات زمن التوقف وتحديثها، بطريقة مماثلة لقيام المدراء بتنفيذ هذه الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="568a5-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="568a5-116">واجب الأمان الذي يتحكم في الوصول إلى هذه الوظيفة هو:</span><span class="sxs-lookup"><span data-stu-id="568a5-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="568a5-117">الواجب: المحافظة على عمليات الإجازات والغياب الخاصة بالعاملين.</span><span class="sxs-lookup"><span data-stu-id="568a5-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="568a5-118">الامتياز: المحافظة على طلبات الإجازات والغياب لجميع العاملين.</span><span class="sxs-lookup"><span data-stu-id="568a5-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="568a5-119">التغييرات الأخرى</span><span class="sxs-lookup"><span data-stu-id="568a5-119">Other changes</span></span>
<span data-ttu-id="568a5-120">تم إجراء التحديثات التالية في هذا الإصدار:</span><span class="sxs-lookup"><span data-stu-id="568a5-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="568a5-121">تغييرات في إجراءات توظيف العاملين بحيث لا تعود "عالقة" في حالة **اكتمل سير العمل‬**.</span><span class="sxs-lookup"><span data-stu-id="568a5-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="568a5-122">يمكنك الآن إنشاء سجل التوظيف من دون تاريخ بدء التوظيف.</span><span class="sxs-lookup"><span data-stu-id="568a5-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="568a5-123">يطبق تاريخ التسجيل في Dynamics 365 Talent لدورة تدريبية تظهر في الخدمة الذاتية للموظف المنطقة الزمنية المقابلة للتاريخ.</span><span class="sxs-lookup"><span data-stu-id="568a5-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="568a5-124">يمكن استيراد ملفات Excel عدة مرات دون أية أخطاء باستخدام **كيان الموظف‬**.</span><span class="sxs-lookup"><span data-stu-id="568a5-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="568a5-125">مشكلات معروفة​</span><span class="sxs-lookup"><span data-stu-id="568a5-125">Known issue</span></span>

- <span data-ttu-id="568a5-126">**المشكلة**: عند إضافة مرفق جديد إلى عامل، يظهر الزران **جديد** و**تحرير** بلون رمادي.</span><span class="sxs-lookup"><span data-stu-id="568a5-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="568a5-127">**الحل البديل:** قبل فتح صفحة المرفق، تأكد من أن مربعات الحقائق في صفحة **العامل** مغلقة.</span><span class="sxs-lookup"><span data-stu-id="568a5-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="568a5-128">إذا كانت مربعات الحقائق مغلقة عند تحميل صفحة **العامل**، سيتم تمكين زر المرفقات</span><span class="sxs-lookup"><span data-stu-id="568a5-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="568a5-129">(سوف يتم إصلاح هذه المشكلة في التحديث التالي للنظام الأساسي.)</span><span class="sxs-lookup"><span data-stu-id="568a5-129">(This issue will be fixed in the next platform update.)</span></span>
