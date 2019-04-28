---
title: ما الجديد أو المتغير في Dynamics 365 for Talent (27 فبراير 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
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
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d8e6a02b43ad60e3a0c4382f98cb808066587da7
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/12/2019
ms.locfileid: "949887"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-27-2019"></a>ما الجديد أو المتغير في Dynamics 365 for Talent (27 فبراير 2019)

[!include [banner](includes/banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2163

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>إضافة عنصر قائمة حقول مخصصة إلى إدارة النظام

تمت إضافة الانتقال إلى قائمة **الحقول المخصصة** إلى مساحة عمل **إدارة النظام**.

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>إخفاء عمليات الاستيراد والإنشاء لتطبيقات المحمول الجديدة

في الوقت الحالي، لا يمكن إنشاء تطبيقات محمول جديدة في Talent. وقد تمت إزالة الخيار المتعلق بإنشاء تجارب جديدة على المحمول من قائمة **تطبيق الجوال‬**.

### <a name="variable-compensation-award-dmf-entity"></a>مكافأة التعويض المتغير (كيان DMF)

في هذا الإصدار، يتوفر الآن كيان Data Management Framework (DMF) **مكافأة التعويض المتغير** للتصدير.

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>تظهر عناوين المملكة المتحدة في صفحة تحليلات إدارة الموظفين‬ كعناوين سويسرية

في هذا الإصدار، تظهر العناوين حسب المدينة. يصحح هذا الإصدار المشاكل حيث تمثل المرئيات موقع الموظف بشكل خاطئ.

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>يعرض تقرير "القوى العاملة‬" في Power BI خطأ عندما يكون تاريخ الأقدمية للعامل يومًا في سنة كبيسة

تم إجراء إصلاح في Microsoft Power BI لحساب تواريخ الأقدمية التي تقع في 29 فبراير.

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>تسمح خطط التعويض الثابت ومكافآت التعويض المتغير والتعويض المتغير للموظف (التسجيلات) بالحقول المخصصة

يمكن الآن إضافة الحقول المخصصة لخطط التعويض الثابت ومكافآت التعويض المتغير والتعويض المتغير للموظف (التسجيلات). يمكنك الآن تعقب مزيد من المعلومات حول خطط التعويض الثابت والتعويض المتغير‬ للموظفين، بالإضافة إلى المعلومات المتوفرة بشكل افتراضي. يمكن إدخال الحقول المخصصة وتحديثها من خلال واجهة المستخدم أو من الكيانات المتوفرة.

### <a name="other-miscellaneous-bug-fixes"></a>إصلاحات أخطاء متنوعة أخرى

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية إضافية أخرى:

## <a name="coming-soon"></a>قريبًا

### <a name="advanced-compensation-security-fixed-and-variable"></a>أمان التعويض المتقدم (التعويض الثابت والمتغير)

في الكثير من المؤسسات، قد يتوفر لدى مدراء التعويضات والمزايا حق الوصول إلى سجلات تعويض معينة فقط. وقد تكون هذه السجلات مخصصة للمدراء التنفيذيين أو الموظفين الإقليميين. سيسمح هذا التغيير لإدارة الموارد البشرية (HR) بإدارة خطط التعويض لمجموعات مختلفة من الموظفين في المؤسسة والمحافظة عليها. ستحدد أدوار الأمان التي يمكن تعيينها إلى خطط التعويض الثابت والمتغير حق الوصول إلى هذه الخطط وبيانات الموظفين ذات الصلة بها (على سبيل المثال، معلومات حول الرواتب وسجلات المكافآت). الأدوار التي ستتمكن من الوصول لمعالجة تعويضات هؤلاء الموظفين هي فقط الأدوار التي تملك حق الوصول المحدد.

### <a name="platform-update-24"></a>update 24 للنظام الأساسي

للحصول على مزيد من المعلومات حول Microsoft Dynamics 365 for Finance and Operations platform update 24 (مارس 2019)، راجع [ميزات المعاينة في Finance and Operations platform update 24 (مارس 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>جعل التعويض الثابت للموظف متوفرًا لتعيينات المناصب المستقبلية

من الطبيعي تحديد تاريخ بدء مستقبلي للموظفين الذين ينضمون إلى مؤسسة ما. سيسمح هذا التغيير بتحديد التعويض الثابت للموظفين الذين لديهم تعيينات مناصب مستقبلية.

## <a name="known-issues"></a>مشكلات معروفة​

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-to-finance-and-operations"></a>التغييرات في قالب تكامل Core HR (Talent Common Data Service إلى Finance and Operations)
تم تحديث قالب Core HR إلى "قالب استعلام متقدم". وبالتالي، سيكون الاستعلام المتقدم متوفرًا، بشكل افتراضي، للمشاريع التي يتم إنشاؤها باستخدام هذا القالب. بالإضافة إلى ذلك، ستكون أي وظائف تعيين افتراضية مرئية فقط في محرر الاستعلام. (تظهر وظائف التعيين الافتراضية على الشكل "FN" في التعيينات.)

للحصول على مزيد من المعلومات حول أخطاء التعيين، راجع [ما الجديد أو المتغير في Dynamics 365 for Talent Core HR (14 ديسمبر 2018)](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14).

لاستخدام القالب الجديد، أنشئ مشروعًا جديدًا، وحدد قالب تكامل Talent الجديد.

لتحديث قالب موجود، اتبع هذه الخطوات.

1. قم بتحديث التعيينات التالية:

    - **مناصب الوظيفة إلى الوظيفة:** أزل هذا التعيين.
    - **تعيين مناصب الوظيفة إلى الوظيفة الرئيسية للمناصب:** أزل هذا التعيين.
    - **مناصب الوظيفة إلى المنصب الأساسي:** أضف تعيينًا جديدًا من كيان **مناصب الوظيفة** إلى Common Data Service إلى كيان **المنصب الأساسي** في Finance and Operations. انقله إلى الموضع 7 في التسلسل.

        [![تعيين مناصب الوظيفة إلى المنصب الأساسي](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **مناصب الوظيفة إلى تفاصيل المنصب:** أضف تعيينًا جديدًا من كيان **مناصب الوظيفة** إلى Common Data Service إلى كيان **تفاصيل المنصب** في Finance and Operations. انقله إلى الموضع 8 في التسلسل.

        [![تعيين مناصب الوظيفة إلى تفاصيل المناصب](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **مناصب الوظيفة إلى مدد المنصب‬:** أضف تعيينًا جديدًا من كيان **مناصب الوظيفة** إلى Common Data Service إلى كيان **مدد المنصب‬** في Finance and Operations.

        [![تعيين مناصب الوظيفة إلى مدد المنصب‬](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **مناصب الوظيفة إلى التدرجات الهرمية للمناصب‬‬:** أضف تعيينًا جديدًا من كيان **مناصب الوظيفة** إلى Common Data Service إلى كيان **التدرجات الهرمية للمناصب‬‬** في Finance and Operations. حدد **استعلام متقدم** لجعل الاستعلام المتقدم متوفرًا لمشروعك.

       [![الزر "استعلام متقدم"](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. أضف التعيينات التالية.
    
    [![التعيين](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom = VALIDFROM cdm_validto cdm_validto = VALIDTO
       
    2. حدد الارتباط **الاستعلام المتقدم والتصفية** إلى جانب حقل **البحث**.  

    3. ابحث عن العمود **cdm_parentjobpositionid.cdm_jobpositionnumber**، وحدد زر السهم للأسفل إلى على جانبه الأيسر.

    4. في مربع الحوار الذي يظهر، حدد **إزالة الفارغ**.

    5. حدد **إضافة عمود \> إضافة عمود شرطي** لإضافة تحويل قيمة افتراضية للاسم HIERARCHYTYPENAME.

        [![الأمر "إضافة عمود شرطي"](./media/Add-column.png)](./media/Add-column.png)

    6. في مربع الحوار **إضافة عمود شرطي**، أدخل **HIERARCHYTYPENAME** كاسم للعمود الجديد.
    7. في الجزء **If** من الشرط، حدد أي حقل، واستخدم **equal to** كالعلاقة، وأدخل أي قيمة. في الجزأين الآخرين ***Then‎** و**Otherwise** من الشرط، حدد ما يجب أن تكون القيمة الافتراضية. في هذه الحالة، أدخل **Line** في الجزأين.

        [![مربع الحوار "إضافة عمود شرطي"](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. حدد **موافق** لإغلاق مربع الحوار **الاستعلام المتقدم والتصفية**.
    9. في صفحة **مهمة التعيين**، حدد العمود الجديد كمصدر لإنشاء تعيين آخر للاسم HIERARCHYTYPENAME.

        [![التعيين](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)
