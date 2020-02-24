---
title: تكوين مُحددات الإجازة والغياب
description: تتيح تحديد معلمات الموارد البشرية للإجازات والغياب في Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007941"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="9a8dc-103">تكوين مُحددات الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="9a8dc-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="9a8dc-104">قبل اعداد خطط الإجازات والإجازات في Dynamics 365 Human Resources، من الأفضل التحقق من الإعدادات لكافة المحددات المتعلقة بالموارد البشرية، بما في ذلك:</span><span class="sxs-lookup"><span data-stu-id="9a8dc-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="9a8dc-105">التسلسل الرقمي لطلبات الإجازات</span><span class="sxs-lookup"><span data-stu-id="9a8dc-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="9a8dc-106">إعدادات قانون الأسرة والإجازات الطبية (FMLA)</span><span class="sxs-lookup"><span data-stu-id="9a8dc-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="9a8dc-107">إعدادات الخدمة الذاتية للموظفين لطلبات الاجازه والغياب</span><span class="sxs-lookup"><span data-stu-id="9a8dc-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="9a8dc-108">معلمات الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="9a8dc-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="9a8dc-109">عرض محددات الموارد البشرية وتغييرها</span><span class="sxs-lookup"><span data-stu-id="9a8dc-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="9a8dc-110">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="9a8dc-111">ضمن **الإعداد**، حدد **محددات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="9a8dc-112">في علامة التبويب **التسلسلات الرقمية**، تحقق من **كود التسلسل الرقمي** لـ **معرف طلب الإجازة** وقم بالتغيير حسب الضرورة.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="9a8dc-113">يحدد هذا الاعداد التسلسل المستخدم لتعيين المعرفات تلقائيا لطلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="9a8dc-114">في علامة التبويب **FMLA**، تحقق من إعدادات FMLA وقم بتغييرها حسب الضرورة.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="9a8dc-115">في علامة التبويب **الخدمة الذاتية للموظفين**، حدد ما إذا كان بإمكان المديرين إدخال الإجازات وطلبات الغياب نيابة عن موظفيهم.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="9a8dc-116">في علامة التبويب **الإجازة والغياب**، تحقق من الإعدادات وقم بتغييرها حسب الضرورة.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="9a8dc-117">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="9a8dc-118">تكوين معلمات التقويم</span><span class="sxs-lookup"><span data-stu-id="9a8dc-118">Configure calendar parameters</span></span>

<span data-ttu-id="9a8dc-119">إذا قمت بتمكين ميزه معاينه تقويم الاجازه والغياب، ستحتاج إلى تكوين معلمات اضافيه.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="9a8dc-120">بالنسبة لإصدار المعاينة في 3 فبراير 2020، يتم تمكين **تعليق طلبات الإجازات** فقط.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="9a8dc-121">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="9a8dc-122">ضمن **الإعداد**، حدد **محددات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="9a8dc-123">في علامة التبويب **تقويم**، وقم بتغيير الإعدادات حسب الضرورة.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="9a8dc-124">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9a8dc-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a8dc-125">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="9a8dc-125">See also</span></span>

- [<span data-ttu-id="9a8dc-126">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="9a8dc-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
