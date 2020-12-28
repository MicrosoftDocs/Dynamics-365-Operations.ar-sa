---
title: إنشاء قالب إعداد باستخدام Dynamics 365 Talent - Onboard
description: يشرح هذا الموضوع كيفية استخدام تطبيق  Dynamics 365 Talent - Onboard لإنشاء قالب دليل إعداد الموظفين الجدد لديك. تعتبر هذه المهمة خطوة أولى أساسية في استراتيجية التوظيف إلى التقاعد في إدارة رؤوس الأموال البشرية‬.
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c322a0dd9a3c61a2d333fdc716acde88a2165f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460221"
---
# <a name="create-an-onboarding-template"></a><span data-ttu-id="3f160-104">إنشاء قالب إعداد</span><span class="sxs-lookup"><span data-stu-id="3f160-104">Create an onboarding template</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f160-105">يوفر Microsoft Dynamics 365 Talent: Onboard قوالب مختلفة يُمكنها أن تساعدك في إنشاء دليل إعداد في أسرع وقت ممكن.</span><span class="sxs-lookup"><span data-stu-id="3f160-105">Microsoft Dynamics 365 Talent: Onboard provides various templates that can help you create an onboarding guide as quickly as possible.</span></span> <span data-ttu-id="3f160-106">يمكنك استخدام قالب واحد أو أكثر من هذه القوالب، أو يمكنك إنشاء قوالب خاصة بك.</span><span class="sxs-lookup"><span data-stu-id="3f160-106">You can use one or more of these templates, or you can create your own templates.</span></span> <span data-ttu-id="3f160-107">يوفر Onboard نصًا نموذجيًا يمكنك استخدامه عند إنشاء قوالبك.</span><span class="sxs-lookup"><span data-stu-id="3f160-107">Onboard provides sample text that you can use when you create your own templates.</span></span> <span data-ttu-id="3f160-108">وبالتالي، فإن العملية سهلة حتى عندما تبدأ من الصفر.</span><span class="sxs-lookup"><span data-stu-id="3f160-108">Therefore, the process is easy even if you start from scratch.</span></span>

## <a name="create-an-onboarding-template-from-an-existing-template"></a><span data-ttu-id="3f160-109">إنشاء قالب إعداد من قالب موجود</span><span class="sxs-lookup"><span data-stu-id="3f160-109">Create an onboarding template from an existing template</span></span>

1. <span data-ttu-id="3f160-110">في القائمة اليمنى، حدد **القوالب**.</span><span class="sxs-lookup"><span data-stu-id="3f160-110">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="3f160-111">ضمن **القوالب الشائعة  من المعرض** أو **القوالب الخاصة بي**، حدد قالبًا.</span><span class="sxs-lookup"><span data-stu-id="3f160-111">Under **Popular templates from the gallery** or **My templates**, select a template.</span></span> <span data-ttu-id="3f160-112">لعرض المزيد من القوالب، حدد **المزيد في معرض القوالب**.</span><span class="sxs-lookup"><span data-stu-id="3f160-112">To view more templates, select **More in template gallery**.</span></span>
3. <span data-ttu-id="3f160-113">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="3f160-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="3f160-114">إذا كان القالب من المعرض، فحدد **حفظ كقالب خاص بي**، أدخل اسمًا جديدًا للقالب، وحدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3f160-114">If the template is from the gallery, select **Save as my template**, enter a new name for the template, and select **Save**.</span></span>
    - <span data-ttu-id="3f160-115">إذا كان القالب من **القوالب الخاصة بي**، فحدد **حفظ كقالب**، أدخل اسمًا جديدًا للقالب، وحدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3f160-115">If the template is from **My templates**, select **Save as template**, enter a new name for the template, and select **Save**.</span></span>

    <span data-ttu-id="3f160-116">[![إنشاء قالب من قالب موجود](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span><span class="sxs-lookup"><span data-stu-id="3f160-116">[![Creating a template from an existing template](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span></span>

## <a name="create-a-new-onboarding-template"></a><span data-ttu-id="3f160-117">إنشاء قالب إعداد جديد</span><span class="sxs-lookup"><span data-stu-id="3f160-117">Create a new onboarding template</span></span>

1. <span data-ttu-id="3f160-118">في القائمة اليمنى، حدد **القوالب**.</span><span class="sxs-lookup"><span data-stu-id="3f160-118">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="3f160-119">ضمن **القوالب الخاصة بي**، حدد لوحة **إضافة** (علامة الجميع \[**+**\]).</span><span class="sxs-lookup"><span data-stu-id="3f160-119">Under **My templates**, select the **Add** (plus sign \[**+**\]) tile.</span></span>

    <span data-ttu-id="3f160-120">[![إنشاء قالب جديد](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span><span class="sxs-lookup"><span data-stu-id="3f160-120">[![Creating a new template](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span></span>

3. <span data-ttu-id="3f160-121">في مربع الحوار **إنشاء قالب دليل**، أدخل اسمًا للقالب، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3f160-121">In the **Create a guide template** dialog box, enter a name for the template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3f160-122">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="3f160-122">Next steps</span></span>

- [<span data-ttu-id="3f160-123">تحرير أدلة وقوالب الإعداد</span><span class="sxs-lookup"><span data-stu-id="3f160-123">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="3f160-124">مشاركة المحتوى مع مساهمين آخرين</span><span class="sxs-lookup"><span data-stu-id="3f160-124">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="3f160-125">عرض حالة المهام وإعداد الموظفين</span><span class="sxs-lookup"><span data-stu-id="3f160-125">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="3f160-126">إنشاء فرق توظيف في Onboard‎</span><span class="sxs-lookup"><span data-stu-id="3f160-126">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="3f160-127">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="3f160-127">See also</span></span>

- [<span data-ttu-id="3f160-128">تجربة تطبيق Onboard أو شراؤه</span><span class="sxs-lookup"><span data-stu-id="3f160-128">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="3f160-129">ما الجديد أو المتغير‬ في Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="3f160-129">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="3f160-130">خطط الإصدارات</span><span class="sxs-lookup"><span data-stu-id="3f160-130">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="3f160-131">الحصول على دعم لـ Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="3f160-131">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
