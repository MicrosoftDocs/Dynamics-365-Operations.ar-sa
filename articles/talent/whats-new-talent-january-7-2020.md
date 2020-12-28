---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (7‏ يناير 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460217"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="5a31c-103">ما الجديد أو المتغير في Dynamics 365 Talent‏ (7‏ يناير 2020)</span><span class="sxs-lookup"><span data-stu-id="5a31c-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="5a31c-104">تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="5a31c-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="5a31c-105">التغييرات في Attract</span><span class="sxs-lookup"><span data-stu-id="5a31c-105">Changes in Attract</span></span>

<span data-ttu-id="5a31c-106">يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="5a31c-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="5a31c-107">التغييرات في Onboard</span><span class="sxs-lookup"><span data-stu-id="5a31c-107">Changes in Onboard</span></span>

<span data-ttu-id="5a31c-108">يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="5a31c-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="5a31c-109">التغييرات في Core HR</span><span class="sxs-lookup"><span data-stu-id="5a31c-109">Changes in Core HR</span></span>

<span data-ttu-id="5a31c-110">تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2697.</span><span class="sxs-lookup"><span data-stu-id="5a31c-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="5a31c-111">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5a31c-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="5a31c-112">لا يمكن حذف العاملين الذين ليس لديهم سجلات توظيف - (386157)</span><span class="sxs-lookup"><span data-stu-id="5a31c-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="5a31c-113">يقوم هذا التغيير باضافه خيار حذف في نموذج **عمال بلا عمل**.</span><span class="sxs-lookup"><span data-stu-id="5a31c-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="5a31c-114">يظهر العاملون في هذا النموذج في حاله عدم وجود فرص توظيف مستقبليه أو نشطه أو تاريخيه للعامل.</span><span class="sxs-lookup"><span data-stu-id="5a31c-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="5a31c-115">في هذا الإصدار ، يتم تمكين الحذف فقط لمسؤولي النظام.</span><span class="sxs-lookup"><span data-stu-id="5a31c-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="5a31c-116">ومع ذلك ، في الأسبوع التالي ، سيتم تحديث الأمان للسماح لكافة المستخدمين الذين لديهم دور مساعد الموارد بازاله الموظفين دون امبلويمينتس.</span><span class="sxs-lookup"><span data-stu-id="5a31c-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="5a31c-117">يمكنك أيضا اجراء هذه التغييرات يدويا باتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5a31c-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="5a31c-118">انتقل إلى **تكوين الأمان**.</span><span class="sxs-lookup"><span data-stu-id="5a31c-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="5a31c-119">في علامة التبويب **الامتيازات**، قم بتصفية قائمة **الامتيازات** إلى  **الاحتفاظ بالعمال**.</span><span class="sxs-lookup"><span data-stu-id="5a31c-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="5a31c-120">في عمود **المراجع**، حدد **عرض عناصر القائمة**.</span><span class="sxs-lookup"><span data-stu-id="5a31c-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="5a31c-121">في **عرض عناصر القائمة**، حدد **HcmWOrkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="5a31c-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="5a31c-122">يمكنك تعيين إذن **الحذف** لمنحه.</span><span class="sxs-lookup"><span data-stu-id="5a31c-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="5a31c-123">حدد علامة التبويب **الكائنات غير المنشورة**.</span><span class="sxs-lookup"><span data-stu-id="5a31c-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="5a31c-124">حدد **نشر الكل**.</span><span class="sxs-lookup"><span data-stu-id="5a31c-124">Select **Publish all**.</span></span>
