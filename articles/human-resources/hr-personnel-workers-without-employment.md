---
title: العاملون بدون توظيف
description: يظهر العمال الذين ليس لديهم عمل مستقبلي أو نشط أو تاريخي مع مؤسستك في نموذج العمال بدون عمل.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6fbada6feb55b8627b1aa1ddfe367177edb7a0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051703"
---
# <a name="workers-without-employment"></a><span data-ttu-id="dce63-103">العاملون بدون توظيف</span><span class="sxs-lookup"><span data-stu-id="dce63-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dce63-104">يظهر العمال الذين ليس لديهم عمل مستقبلي أو نشط أو تاريخي مع مؤسستك في نموذج **العمال بدون عمل**.</span><span class="sxs-lookup"><span data-stu-id="dce63-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="dce63-105">يمكن أن يظهر العمال بهذه الحالة عند استيراد عمال ليس لديهم سجل توظيف ، أو عند حذف توظيف عامل من خلال **العمال > سجل التوظيف**.</span><span class="sxs-lookup"><span data-stu-id="dce63-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="dce63-106">بشكل افتراضي ، يتوفر نموذج **العمال بدون عمل** للأدوار التالية.</span><span class="sxs-lookup"><span data-stu-id="dce63-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="dce63-107">مساعد الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="dce63-107">Human Resources Assistant</span></span>
- <span data-ttu-id="dce63-108">مدير الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="dce63-108">Human Resources Manager</span></span>
- <span data-ttu-id="dce63-109">مسؤول التعيين</span><span class="sxs-lookup"><span data-stu-id="dce63-109">Recruiter</span></span>
- <span data-ttu-id="dce63-110">مدير التعويض والميزات</span><span class="sxs-lookup"><span data-stu-id="dce63-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="dce63-111">مسؤول المرتبات</span><span class="sxs-lookup"><span data-stu-id="dce63-111">Payroll Administrator</span></span>
- <span data-ttu-id="dce63-112">مدير المرتبات</span><span class="sxs-lookup"><span data-stu-id="dce63-112">Payroll Manager</span></span>
- <span data-ttu-id="dce63-113">مدير التدريب</span><span class="sxs-lookup"><span data-stu-id="dce63-113">Training Manager</span></span>

<span data-ttu-id="dce63-114">في قائمة **العمال بدون عمل**، يمكنك حذف الأفراد المدرجين.</span><span class="sxs-lookup"><span data-stu-id="dce63-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="dce63-115">بشكل افتراضي ، يتم منح هذا الامتياز لدور مساعد الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="dce63-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="dce63-116">يمكنك منح هذا الامتياز للأدوار الأخرى من خلال الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="dce63-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="dce63-117">حدد **إدارة النظام**، ثم حدد علامة التبويب **تكوين الأمان**.</span><span class="sxs-lookup"><span data-stu-id="dce63-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="dce63-118">في علامة التبويب **الامتيازات**، قم بتصفية قائمة **الامتيازات** إلى  **الاحتفاظ بالعمال**.</span><span class="sxs-lookup"><span data-stu-id="dce63-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="dce63-119">[![قائمة تصفية الامتيازات](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="dce63-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="dce63-120">في عمود **المراجع**، حدد **عرض عناصر القائمة**.</span><span class="sxs-lookup"><span data-stu-id="dce63-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="dce63-121">في **عرض عناصر القائمة**، حدد **HcmWorkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="dce63-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="dce63-122">[![تحديد نموذج](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="dce63-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="dce63-123">قم بتعيين إذن **حذف** إلى **منح**.</span><span class="sxs-lookup"><span data-stu-id="dce63-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="dce63-124">حدد علامة التبويب **الكائنات غير المنشورة**.</span><span class="sxs-lookup"><span data-stu-id="dce63-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="dce63-125">حدد **نشر الكل**.</span><span class="sxs-lookup"><span data-stu-id="dce63-125">Select **Publish all**.</span></span>

   <span data-ttu-id="dce63-126">[![نشر التغييرات](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="dce63-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]