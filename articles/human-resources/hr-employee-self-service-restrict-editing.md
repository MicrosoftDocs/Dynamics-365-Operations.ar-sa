---
title: تقييد تحرير المعلومات الشخصية
description: تقييد الموظفين من تحرير تفاصيل جهة اتصال في Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c82114f6600345ee5e2eb9c1c0629ae6c8f0b9a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877674"
---
# <a name="restrict-editing-of-personal-information"></a>تقييد تحرير المعلومات الشخصية


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

توضح هذه المقالة كيفية تقييد الموظفين من تحرير تفاصيل جهات الاتصال في Dynamics 365 Human Resources. قد ترغب في منع الموظفين من تحرير تفاصيل جهات اتصال معينة، مثل موقع العمل أو عنوان البريد الكتروني الخاص بهم.

> [!NOTE]
> لاستخدام هذه الميزة ، يجب أولاً تمكين **(المعاينة) تقييد الموظفين من إضافة أو تحرير معلومات العنوان وجهة الاتصال لأغراض التحديد** في إدارة المزايا. لمزيد من المعلومات حول تمكين ميزات المعاينة، راجع [إدارة الميزات](hr-admin-manage-features.md).<br><br>![تمكين ميزة المعاينة.](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>اختيار المعلومات التي يمكن للموظف إضافتها أو تحريرها

1. في الموارد البشرية، حدد **إدارة العاملين**، وحدد **الارتباطات**، ثم حدد **معلمات الموارد البشرية**.

   ![انتقل إلى معلمات الموارد البشرية.](./media/hr-employee-self-service-human-resources-parameters.png)

2. في الصفحة **معلمات Human resources**، حدد علامة التبويب **الخدمة الذاتية للموظف**.

   ![حدد الخدمة الذاتية للموظف.](./media/hr-employee-self-service-tab.png)

3. في علامة التبويب **الخدمة الذاتية للموظف**، قم بإلغاء تحديد كافة المعلومات الواردة في القسم **معلومات العنوان وجهة الاتصال** التي لا تريد أن يقوم الموظفون بإضافتها أو تحريرها. في هذا المثال، قمنا بإلغاء تحديد معلومات جهة اتصال **العمل**.

   ![تقييد تحرير معلومات جهات اتصال العمل.](./media/hr-employee-self-service-restrict-business.png)

4. حدد **حفظ**.

   ![حفظ التغييرات.](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>خبرة الموظف

بعد قيامك بتقييد الموظفين من إضافة تفاصيل جهة الاتصال أو تحريرها، فإنه يمكنهم رؤية المعلومات، ولكن لا يمكنهم تغييرها.

في هذا المثال، يتم تقييد الموظفين من تحرير تفاصيل جهة اتصال **العمل**، ويمكنهم الاستمرار في رؤية المعلومات الموجودة في **الخدمة الذاتية للموظفين**:

![عرض تفاصيل جهات اتصال العمل.](./media/hr-employee-self-service-restrict-view.png)

ومع ذلك، عند تحديد التفاصيل الخاصة بجهة اتصال العمل، يظهر الجزء **تحرير العنوان** للقراءة فقط، ولا يمكنهم تغيير أي حقل من الحقول.

![عرض تفاصيل جهات اتصال العمل للقراءة فقط.](./media/hr-employee-self-service-restrict-read-only.png)

بالإضافة إلى ذلك، إذا قاموا بتحديد **إضافة** لإضافة عنوان جديد، فلن يتمكنوا من تحديد **العمل** مربع القائمة المنسدلة **الغرض**.

![يتعذر على الموظف إضافة عنوان عمل.](./media/hr-employee-self-service-restrict-add.png)

يخوض الموظفون التجربة نفسها عند تحديد **تفاصيل جهة الاتصال** على الصفحة **المعلومات الشخصية** ويضيف عنوانًا جديدًا. يعرض المربع المنسدل **الغرض** أنواع المعلومات التي يمكنهم إضافتها فقط. 

![لا يمكن للموظف تحديد العمل في المربع المنسدل الغرض.](./media/hr-employee-self-service-restrict-purpose.png)

تعرض الآن **تفاصيل جهة الاتصال** في الشبكة **الغرض**.

![يعرض الغرض في شبكة تفاصيل جهة الاتصال.](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>راجع أيضًا

[نظرة عامة على إعداد الخدمة الذاتية للموظف والمدير](hr-employee-manager-self-service-overview.md)<br>
[تكوين معلمات Human resources](hr-setup-parameters.md)<br>
[تحرير المعلومات الشخصية](hr-employee-manager-self-service-edit-personal-information.md)
