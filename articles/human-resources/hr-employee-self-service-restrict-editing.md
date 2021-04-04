---
title: تقييد تحرير المعلومات الشخصية
description: تقييد الموظفين من تحرير تفاصيل جهة اتصال في Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d4785232dbb21c5f8a800497fb0cfd3c64dea2d8
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/05/2021
ms.locfileid: "5503026"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="3b34f-103">تقييد تحرير المعلومات الشخصية</span><span class="sxs-lookup"><span data-stu-id="3b34f-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="3b34f-104">يوضح هذا الموضوع كيفية تقييد الموظفين من تحرير تفاصيل جهات الاتصال في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3b34f-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3b34f-105">قد ترغب في منع الموظفين من تحرير تفاصيل جهات اتصال معينة، مثل موقع العمل أو عنوان البريد الكتروني الخاص بهم.</span><span class="sxs-lookup"><span data-stu-id="3b34f-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="3b34f-106">لاستخدام هذه الميزة ، يجب أولاً تمكين **(المعاينة) تقييد الموظفين من إضافة أو تحرير معلومات العنوان وجهة الاتصال لأغراض التحديد** في إدارة المزايا.</span><span class="sxs-lookup"><span data-stu-id="3b34f-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="3b34f-107">لمزيد من المعلومات حول تمكين ميزات المعاينة، راجع [إدارة الميزات](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="3b34f-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="3b34f-108">![تمكين ميزة المعاينة](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="3b34f-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="3b34f-109">اختيار المعلومات التي يمكن للموظف إضافتها أو تحريرها</span><span class="sxs-lookup"><span data-stu-id="3b34f-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="3b34f-110">في الموارد البشرية، حدد **إدارة العاملين**، وحدد **الارتباطات**، ثم حدد **معلمات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="3b34f-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![انتقل إلى معلمات الموارد البشرية](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="3b34f-112">في الصفحة **معلمات Human resources**، حدد علامة التبويب **الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="3b34f-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![تحديد الخدمة الذاتية للموظف](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="3b34f-114">في علامة التبويب **الخدمة الذاتية للموظف**، قم بإلغاء تحديد كافة المعلومات الواردة في القسم **معلومات العنوان وجهة الاتصال** التي لا تريد أن يقوم الموظفون بإضافتها أو تحريرها.</span><span class="sxs-lookup"><span data-stu-id="3b34f-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="3b34f-115">في هذا المثال، قمنا بإلغاء تحديد معلومات جهة اتصال **العمل**.</span><span class="sxs-lookup"><span data-stu-id="3b34f-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![تقييد تحرير معلومات جهات اتصال العمل](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="3b34f-117">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3b34f-117">Select **Save**.</span></span>

   ![حفظ التغييرات](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="3b34f-119">خبرة الموظف</span><span class="sxs-lookup"><span data-stu-id="3b34f-119">Employee experience</span></span>

<span data-ttu-id="3b34f-120">بعد قيامك بتقييد الموظفين من إضافة تفاصيل جهة الاتصال أو تحريرها، فإنه يمكنهم رؤية المعلومات، ولكن لا يمكنهم تغييرها.</span><span class="sxs-lookup"><span data-stu-id="3b34f-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="3b34f-121">في هذا المثال، يتم تقييد الموظفين من تحرير تفاصيل جهة اتصال **العمل**، ويمكنهم الاستمرار في رؤية المعلومات الموجودة في الخدمة الذاتية للموظفين:</span><span class="sxs-lookup"><span data-stu-id="3b34f-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![عرض تفاصيل جهات اتصال العمل](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="3b34f-123">ومع ذلك، عند تحديد التفاصيل الخاصة بجهة اتصال العمل، يظهر الجزء **تحرير العنوان** للقراءة فقط، ولا يمكنهم تغيير أي حقل من الحقول.</span><span class="sxs-lookup"><span data-stu-id="3b34f-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![عرض تفاصيل جهات اتصال العمل للقراءة فقط](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="3b34f-125">بالإضافة إلى ذلك، إذا قاموا بتحديد **إضافة** لإضافة عنوان جديد، فلن يتمكنوا من تحديد **العمل** مربع القائمة المنسدلة **الغرض**.</span><span class="sxs-lookup"><span data-stu-id="3b34f-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![يتعذر على الموظف إضافة عنوان عمل](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="3b34f-127">يخوض الموظفون التجربة نفسها عند تحديد **تفاصيل جهة الاتصال** على الصفحة **المعلومات الشخصية** ويضيف عنوانًا جديدًا.</span><span class="sxs-lookup"><span data-stu-id="3b34f-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="3b34f-128">يعرض المربع المنسدل **الغرض** أنواع المعلومات التي يمكنهم إضافتها فقط.</span><span class="sxs-lookup"><span data-stu-id="3b34f-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![لا يمكن للموظف تحديد العمل في المربع المنسدل الغرض](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="3b34f-130">تعرض الآن **تفاصيل جهة الاتصال** في الشبكة **الغرض**.</span><span class="sxs-lookup"><span data-stu-id="3b34f-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![يعرض الغرض في شبكة تفاصيل جهة الاتصال](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="3b34f-132">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="3b34f-132">See also</span></span>

[<span data-ttu-id="3b34f-133">نظرة عامة على إعداد الخدمة الذاتية للموظف والمدير</span><span class="sxs-lookup"><span data-stu-id="3b34f-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="3b34f-134">تكوين معلمات Human resources</span><span class="sxs-lookup"><span data-stu-id="3b34f-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="3b34f-135">تحرير المعلومات الشخصية</span><span class="sxs-lookup"><span data-stu-id="3b34f-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)