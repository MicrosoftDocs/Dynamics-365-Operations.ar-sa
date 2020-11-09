---
title: تكوين كيانات Common Data Service الظاهرية
description: يوضح هذا الموضوع كيفيه تكوين الكيانات الظاهرية لـ Dynamics 365 Human Resources. إنشاء كيانات ظاهريه موجودة وتحديثها، وتحليل الكيانات التي تم إنشاؤها والمتاحة.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058144"
---
# <a name="configure-common-data-service-virtual-entities"></a>تكوين كيانات Common Data Service الظاهرية

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources هو مصدر بيانات ظاهري في Common Data Service. وهو يوفر عمليات إنشاء وقراءه وتحديث وحذف (CRUD) كامله من Common Data Service وMicrosoft Power Platform لم يتم تخزين البيانات الخاصة بالكيانات الظاهرية في Common Data Service، ولكن في قاعده بيانات التطبيق. 

لتمكين عمليات CRUD علي كيانات الموارد البشرية من Common Data Service، يجب توفير الكيانات ككيانات ظاهريه في Common Data Service يتيح هذا امكانيه اجراء عمليات CRUD من Common Data Service وMicrosoft Power Platform علي البيانات الموجودة في الموارد البشرية. تدعم العمليات أيضا عمليات التحقق الكاملة من منطق العمل للموارد البشرية لضمان تكامل البيانات عند كتابه البيانات إلى الكيانات.

## <a name="available-virtual-entities-for-human-resources"></a>الكيانات الظاهرية المتاحة للموارد البشرية

تتوفر كافة كيانات بروتوكول البيانات المفتوحة (OData) في الموارد البشرية ككيانات ظاهريه في Common Data Service. وهي متوفرة أيضا في Power Platform. يمكنك الآن إنشاء التطبيقات والخبرة بالبيانات مباشره من الموارد البشرية التي لها قدره CRUD كامله، دون نسخ البيانات أو مزامنتها إلى Common Data Service. يمكنك استخدام مداخل Power Apps لإنشاء مواقع ويب خارجيه تمكن سيناريوهات التعاون للعمليات التجارية في الموارد البشرية.

يمكنك عرض قائمه بالكيانات الظاهرية الممكنة في البيئة، وبدء العمل مع الكيانات في [Power Apps](https://make.powerapps.com) في حل **كيانات HR الظاهرية لـ Dynamics 365**.

![كيانات HR الظاهرية لـ Dynamics 365 في Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>الكيانات الظاهرية مقابل الكيانات الطبيعية

لا تكون الكيانات الظاهرية للموارد البشرية متماثلة مع كيانات Common Data Service الطبيعية التي تم إنشاؤها للموارد البشرية. يتم إنشاء الكيانات الطبيعية للموارد البشرية بشكل منفصل وصيانتها في الحل الشائع لـ HCM في Common Data Service. باستخدام الكيانات الطبيعية، يتم تخزين البيانات في Common Data Service وتتطلب مزامنة مع قاعده بيانات التطبيق الخاصة بالموارد البشرية.

> [!NOTE]
> للحصول علي قائمه بكيانات Common Data Service الطبيعية للموارد البشرية، راجع [كيانات Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>الإعداد

اتبع خطوات الاعداد هذه لتمكين الكيانات الظاهرية في البيئة الخاصة بك. 

### <a name="register-the-app-in-microsoft-azure"></a>قم بتسجيل التطبيق في Microsoft Azure

أولا، يجب تسجيل التطبيق في مدخل Azure حتى يتمكن النظام الأساسي لهويه Microsoft من توفير خدمات المصادقة والتخويل للتطبيق والمستخدمين. لمزيد من المعلومات حول تسجيل التطبيقات في Azure، راجع [التشغيل السريع: تسجيل تطبيق بواسطة النظام الأساسي لهويه Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. افتح [مدخل Microsoft Azure](https://portal.azure.com).

2. في قائمة خدمات Azure، حدد **عمليات تسجيل التطبيق**.

3. حدد **تسجيل جديد**.

4. في حقل **الاسم** ، أدخل اسمًا وصفيًا للتطبيق. علي سبيل المثال، **كيانات Dynamics 365 Human Resources الظاهرية**.

5. في الحقل **أعاده توجيه URI** ، ادخل URL الخاص بمساحة الاسم لمثيل الموارد البشرية.

6. حدد **السجل**.

7. عند اكتمال التسجيل، يعرض مدخل Azure جزء **النظرة العامة** لتسجيل التطبيق الذي يتضمن **معرف التطبيق (العميل)**. سجل **معرف التطبيق (العميل)** في هذا الوقت. ستقوم بإدخال هذه المعلومات عند [تكوين مصدر بيانات الوحدة الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. في جزء التنقل الأيمن، حدد **الشهادات والاسرار**.

9. في القسم **أسرار العميل** في الصفحة، حدد **سر عميل جديد**.

10. قم بتوفير وصف، وحدد مده، وحدد **أضافه**.

11. سجل قيمة السر. ستقوم بإدخال هذه المعلومات عند [تكوين مصدر بيانات الوحدة الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > تاكد من مراعاه قيمه السر في هذا الوقت. لا يتم عرض السر أبدا مره أخرى بعد مغادره هذه الصفحة.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>تثبيت تطبيق Dynamics 365 HR Virtual Entity

قم بتثبيت تطبيق Dynamics 365 HR Virtual Entity في البيئة Power Apps الخاصة بك لنشر حزمه حلول الكيان الظاهري إلى Common Data Service.

1. افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).

2. في قائمه **البيئات** ، حدد بيئة Power Apps المقترنة بمثيل الموارد البشرية الخاص بك.

3. في القسم **الموارد** في الصفحة، حدد **تطبيقات Dynamics 365**.

4. حدد اجراء **تثبيت التطبيق**.

5. حدد **Dynamics 365 HR Virtual Entity** ، ثم حدد **التالي**.

6. مراجعه ووضع علامة علي الموافقة علي شروط الخدمة.

7. حدد **تثبيت**.

يستغرق التثبيت بضع دقائق. وعند الانتهاء، انتقل إلى الخطوات التالية.

![تثبيت تطبيق Dynamics 365 HR Virtual Entity من مركز اداره Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>تكوين مصدر بيانات الكيان الظاهري 

الخطوة التالية هي تكوين مصدر البيانات الكيان الظاهري في بيئة Power Apps. 

1. افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).

2. في قائمه **البيئات** ، حدد بيئة Power Apps المقترنة بمثيل الموارد البشرية الخاص بك.

3. حدد **عنوان URL للبيئة** في قسم **التفاصيل** من الصفحة.

4. في **مركز حماية الحل** ، حدد الرمز **بحث متقدم** في الجزء العلوي الأيسر من صفحة التطبيق.

5. في صفحه **بحث متقدم** ، وفي القائمة المنسدلة **البحث عن** ، حدد **تكوينات مصدر البيانات الظاهري Finance and Operations**.

6. حدد **النتائج**.

7. حدد سجل **مصدر بيانات الموارد البشرية من Microsoft**.

8. ادخل المعلومات المطلوبة لتكوين مصدر البيانات.

   - **URL الهدف** : عنوان URL لمساحة اسم الموارد البشرية الخاصة بك.
   - **معرف المستاجر** : معرف المستاجر في Azure Active Directory ( Azure AD).
   - **معرف تطبيق AAD** : معرف التطبيق (العميل) الذي تم إنشاؤه للتطبيق المسجل في مدخل Microsoft Azure. لقد تلقيت هذه المعلومات مبكرا اثناء الخطوة [تسجيل التطبيق في Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).
   - **سر تطبيق AAD** : سر التطبيق الذي تم إنشاؤه للتطبيق المسجل في مدخل Microsoft Azure. لقد تلقيت هذه المعلومات مبكرا اثناء الخطوة [تسجيل التطبيق في Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

9. حدد **حفظ وإغلاق**.

   ![مصدر بيانات الموارد البشرية في Microsoft](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a>منح أذونات التطبيق في الموارد البشرية

امنح أذونات لتطبيقي Azure AD في الموارد البشرية:

- التطبيق الذي تم إنشاؤه للمستاجر في مدخل Microsoft Azure
- تطبيق Dynamics 365 HR Virtual Entity الذي تم تبثبيته في من بيئة Power Apps 

1. في الموارد البشرية، افتح صفحة **تطبيقات Azure Active Directory**.

2. حدد **جديد** لإنشاء سجل تطبيق جديد:

    - في الحقل **معرف العميل** ، ادخل معرف العميل الخاص بالتطبيق الذي قمت بتسجيله في مدخل Microsoft Azure.
    - في الحقل **معرف العميل** ، ادخل معرف العميل الخاص بالتطبيق الذي قمت بتسجيله في مدخل Microsoft Azure.
    - في الحقل **معرف المستخدم** ، حدد معرف المستخدم الخاص بمستخدم لديه أذونات المسؤول في الموارد البشرية وبيئة Power Apps.

3. حدد **جديد** لإنشاء سجل تطبيق ثانٍ:

    - **معرف العميل** : f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **الاسم** : Dynamics 365 HR Virtual Entity
    - في الحقل **معرف المستخدم** ، حدد معرف المستخدم الخاص بمستخدم لديه أذونات المسؤول في الموارد البشرية وبيئة Power Apps.

## <a name="generate-virtual-entities"></a>إنشاء كيانات ظاهرية

عند اكتمال الاعداد، يمكنك تحديد الكيانات الظاهرية التي ترغب في إنشائها وتمكينها في مثيل Common Data Service الخاص بك.

1. في Human Resources، افتح صفحة **تكامل Common Data Service (CDS)**.

2. حدد علامة التبويب **الكيانات الظاهرية**.

> [!NOTE]
> سيتم تعيين زر التبديل **تمكين الكيان الظاهري** إلى **نعم** تلقائيًا عندما تم إكمال كافة الإعدادات المطلوبة. إذا تم تعيين زر التبديل إلى **لا** ، فراجع الخطوات الموجودة في الأقسام السابقة من هذا المستند لضمان إكمال كافة إعدادات المتطلبات الأساسية.

3. حدد الكيان أو الكيانات التي ترغب في إنشائها في Common Data Service.

4. حدد **إنشاء/تحديث**.

![تكامل Common Data Service](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a>التحقق من حالة إنشاء الكيان

يتم إنشاء الكيانات الظاهرية في Common Data Service خلال عملية خلفية غير متزامنة. تعرض التحديثات على العملية في مركز الإجراء. تظهر التفاصيل الخاصة بالعملية، بما في ذلك سجلات الأخطاء، في الصفحة **التنفيذ التلقائي للعمليات**.

1. في Human Resources، افتح الصفحة **التنفيذ التلقائي للعمليات**.

2. حدد علامة التبويب **عمليات الخلفية**.

3. حدد **عملية خلفية للتشغيل غير المتزامن لاستقصاء الكيان الظاهري**.

4. حدد **عرض أحدث النتائج**.

يعرض الجزء المنبثق للخارج أحدث نتائج التنفيذ للعملية. يمكنك عرض السجل للعملية، بما في ذلك أية أخطاء تم إرجاعها من Common Data Service.

## <a name="see-also"></a>راجع أيضًا

[ما هو Common Data Service؟](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[نظرة عامة على الكيان](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[نظره عامه علي علاقات الكيانات](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[إنشاء كيانات ظاهريه تحتوي علي بيانات من مصدر بيانات خارجي وتحريرها](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[ما المقصود بمداخل Power Apps؟](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[نظره عامه حول إنشاء التطبيقات في Power Apps](https://docs.microsoft.com/powerapps/maker/)
