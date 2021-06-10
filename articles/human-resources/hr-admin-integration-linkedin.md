---
title: التكامل مع LinkedIn Talent Hub
description: يشرح هذا الموضوع كيفية إعداد التكامل بين Microsoft Dynamics 365 Human Resources وLinkedIn Talent Hub.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4b8c1467368cbcbed5049561b52b29388ec21a5f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055090"
---
# <a name="integrate-with-linkedin-talent-hub"></a>التكامل مع LinkedIn Talent Hub

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يُعد [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) هو النظام الأساسي لنظام تتبع مقدم التطبيق (ATS). يتيح لك إمكانية البحث عن المرشحين وإدارتهم وتوظيفهم في مكان واحد. ومن خلال تكامل Microsoft Dynamics 365 Human Resources مع LinkedIn Talent Hub، فإنه يمكنك بسهولة إنشاء سجلات الموظفين في Human Resources لمقدمي الطلبات الذين تم توظيفهم لأحد المناصب.

## <a name="setup"></a>الإعداد

يجب أن يقوم مسؤول النظام بإكمال مهام الإعداد لتمكين التكامل مع LinkedIn Talent Hub. أولاً، في البيئة Power Apps، فإنه يجب عليك إعداد مستخدم ودور أمان لمنح LinkedIn Talent Hub الأذونات المناسبة لكتابة البيانات في Human Resources.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>اربط بيئتك بـ LinkedIn Talent Hub

1. افتح [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).

2. في القائمة المنسدلة الخاصة بالمستخدم، حدد **إعدادات المنتج**.

3. في جزء التنقل الأيسر، في القسم **خيارات متقدمة**، حدد **عمليات التكامل**.

4. حدد **تخويل** لتكامل Microsoft Dynamics 365 Human Resources.

5. في الصفحة **Dynamics 365 Human Resources**، حدد البيئة لربط LinkedIn Talent Hub بها، ثم حدد **ربط**.

    ![إعداد LinkedIn Talent Hub](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > يمكنك الربط فقط بالبيئات التي يملك فيها حساب المستخدم الخاص بك حق الوصول كمسؤول إلى كل من بيئة Human Resources وبيئة Power Apps المقترنة منه. إذا لم يتم سرد أية بيئات في صفحة ارتباط Human Resources، فتأكد من أنك قد قمت بترخيص بيئات Human Resources على المستأجر، وأن المستخدم الذي قمت بتسجيل الدخول إلى صفحة الارتباط كما أن لديه أذونات مسؤول لكل من بيئة Human Resources وبيئة Power Apps.

### <a name="create-a-power-apps-security-role"></a>إنشاء دور أمان Power Apps

1. افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).

2. في القائمة **البيئات**، حدد البيئة المقترنة ببيئة Human Resources التي ترغب في ربط مثيل LinkedIn Talent Hub الخاص بك بها.

3. حدد **الإعدادات**.

4. قم بتوسيع العقدة **المستخدمون + الأذونات**، وحدد **أدوار الأمان**.

5. في الصفحة **أدوار الأمان**، من شريط الأدوات، حدد **دور جديد**.

6. في علامة التبويب **التفاصيل**، أدخل اسمًا للدور، مثل **LinkedIn Talent Hub HRIS Integration**.

7. في علامة التبويب **تخصيص**، حدد إذن **القراءة** على مستوى المؤسسة للكيانات التالية:

    - الكيان
    - الحقل
    - العلاقة

8. قم بحفظ دور الأمان وإغلاقه.

### <a name="create-a-power-apps-application-user"></a>إنشاء مستخدم تطبيق Power Apps

يجب إنشاء مستخدم التطبيق لمحول LinkedIn Talent Hub لمنح الأذونات إلى المحول لكتابة سجلات الترشيح في البيئة Power Apps.

1. افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).

2. في القائمة **البيئات**، حدد البيئة المقترنة ببيئة Human Resources التي ترغب في ربط مثيل LinkedIn Talent Hub الخاص بك بها.

3. حدد **الإعدادات**.

4. قم بتوسيع العقدة **المستخدمون + الأذونات**، وحدد **المستخدمين**.

5. حدد **إدارة المستخدمين في Dynamics 365**.

6. استخدم القائمة المنسدلة فوق القائمة لتغيير طريقة العرض من طريقة عرض **المستخدمين الممكنين** إلى **مستخدمي التطبيق**.

    ![طريقة عرض مستخدمي التطبيقات](./media/hr-admin-integration-power-apps-application-users.jpg)

7. من شريط الأدوات، حدد **جديد**.

8. في صفحة **المستخدم الجديد‬**، اتبع الخطوات التالية:

    1. قم بتغيير قيمة الحقل **نوع المستخدم** إلى **مستخدم التطبيق**.
    2. قم بتعيين الحقل **اسم المستخدم** إلى **تكامل Dynamics365 HR LinkedIn HRIS**.
    3. عيّن الحقل **معرف التطبيق** إلى **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    4. أدخل أية قيمة في الحقول **الاسم الأول** و **الاسم الأخير** و **البريد الإلكتروني الأساسي**.
    5. في شريط الأدوات، حدد **حفظ \& إغلاق**.

### <a name="assign-a-security-role-to-the-new-user"></a>تعيين دور أمان للمستخدم الجديد

بعد أن تقوم بحفظ مستخدم التطبيق الجديد وإغلاقه في القسم السابق، فإنه يتم إرجاعك إلى الصفحة **قائمة المستخدمين**.

1. في الصفحة **قائمة المستخدمين**، قم بتغيير طريقة العرض إلى **مستخدمي التطبيق**.

2. حدد مستخدم التطبيق الذي قمت بإنشاؤه في القسم السابق.

3. في شريط الأدوات ، حدد **إدارة الأدوار**.

4. حدد دور الأمان الذي قمت بإنشاؤه سابقًا للتكامل.

5. حدد **موافق**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>أضف تطبيق Azure Active Directory في Human Resources

1. في Dynamics 365 Human Resources، افتح صفحة **تطبيقات Azure Active Directory**.
2. أضف سجلاً جديدًا إلى القائمة، ثم قم بتعيين الحقول التالية:

    - **معرف العميل**: أدخل **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    - **الاسم**: أدخل اسم دور أمان Power Apps الذي قمت بإنشائه مسبقًا، مثل **تكامل LinkedIn Talent Hub HRIS**.
    - **معرف المستخدم**: حدد المستخدم الذي لديه الأذونات لكتابة البيانات في إدارة الموظفين.

### <a name="create-the-table-in-dataverse"></a>إنشاء جدول في Dataverse

> [!IMPORTANT]
> يعتمد التكامل مع LinkedIn Talent Hub على الجداول الظاهرية في Dataverse لـ Human Resources. وكمتطلب أساسي لهذه الخطوة في الإعداد، يجب تكوين الجداول الظاهرية. للحصول على معلومات عن كيفية تكوين الجداول الظاهرية، راجع [تكوين جداول Dataverse الظاهرية](./hr-admin-integration-common-data-service-virtual-entities.md).

1. في الموارد البشرية، افتح صفحة **تكامل Dataverse**.

2. حدد علامة التبويب **الجداول الظاهرية**.

3. قم بتصفية قائمة الكيانات حسب تسمية الكيان للعثور على **المرشح الذي تم تصديره من LinkedIn**.

4. حدد الكيان، ثم حدد **إنشاء/تحديث**.

## <a name="exporting-candidate-records"></a>تصدير سجلات المرشحين

بعد اكتمال الإعداد، يمكن لمسؤولي التعيين ومحترفي الموارد البشرية (HR) استخدام الوظيفة **تصدير إلى HRIS** في LinkedIn Talent Hub لتصدير سجلات المرشحين من تم توظيفها LinkedIn Talent Hub إلى Human Resources.

### <a name="export-records-from-linkedin-talent-hub"></a>تصدير السجلات من LinkedIn Talent Hub

بعد نقل المرشح خلال عملية التوظيف وتوظيفه، فإنه يمكنك تصدير سجل المرشح من LinkedIn Talent Hub إلى Human Resources.

1. في LinkedIn Talent Hub، افتح المشروع الذي قمت بتوظيف الموظف الجديد به.

2. حدد سجل مرشح.

3. حدد **تغيير المرحلة**، ثم حدد **تم التوظيف**.

4. في قائمة علامة القطع (**...**) لمرشح، حدد **تصدير إلى HRIS**.

5. في الجزء **تصدير إلى HRIS**، أدخل المعلومات التي يجب تصديرها:

    - في الحقل **موفر HRIS**، حدد **Microsoft Dynamics 365 Human Resources**.
    - في الحقل **تاريخ البدء**، حدد قيمة الموظف الجديد.
    - في الحقل **المسمى الوظيفي**، أدخل المسمى الوظيفي لوظيفة الموظف الجديد.
    - في الحقل **الموقع**، أدخل الموقع الذي سيتواجد به الموظف.
    - أدخل عنوان البريد الإلكتروني للموظف أو تحقق منه.

![التصدير إلى جزء HRIS في لوحة LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>إكمال الإعداد في Human Resources

تظهر سجلات المرشحين التي يتم تصديرها من LinkedIn Talent Hub إلى Human Resources في القسم **‬‏‫المرشحون المُراد توظيفهم** في الصفحة **إدارة العاملين**.

1. في Human Resources، افتح الصفحة **إدارة العاملين**.

2. في المقطع **المرشحين المُراد توظيفهم**، حدد **توظيف** للمرشح المحدد.

3. في مربع الحوار **توظيف عامل جديد**، راجع السجل وأضف أية معلومات مطلوبة. يمكنك أيضًا تحديد رقم المنصب الذي تم توظيف المرشح به.

بعد إدخال المعلومات المطلوبة، يمكنك متابعة العمليات القياسية لإنشاء سجلات الموظفين وإعداد الموظفين.

يتم استيراد التفاصيل التالية وتضمينها في سجل الموظف الجديد:

- الاسم الأول
- اسم العائلة
- تاريخ بداية التوظيف
- عنوان البريد الإلكتروني
- رقم الهاتف

## <a name="see-also"></a>راجع أيضًا

[تكوين جداول Dataverse الظاهرية](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[ما هو Microsoft Dataverse؟](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]