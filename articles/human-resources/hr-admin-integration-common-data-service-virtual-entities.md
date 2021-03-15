---
title: تكوين جداول Dataverse الظاهرية
description: يوضح هذا الموضوع كيفيه تكوين الجداول الظاهرية لـ Dynamics 365 Human Resources. قم إنشاء جداول ظاهريه موجودة وتحديثها، وتحليل الجداول التي تم إنشاؤها والمتاحة.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: cd299b51e38cc30c3e18f3ef9de1f43fa817b840
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111383"
---
# <a name="configure-dataverse-virtual-tables"></a>تكوين جداول Dataverse الظاهرية

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources هو مصدر بيانات ظاهري في Microsoft Dataverse. وهو يوفر عمليات إنشاء وقراءه وتحديث وحذف (CRUD) كامله من Dataverse وMicrosoft Power Platform لا يتم تخزين البيانات الخاصة بالجداول الظاهرية في Dataverse، ولكن في قاعدة بيانات التطبيق.

لتمكين عمليات CRUD على كيانات الموارد البشرية من Dataverse، يجب توفير الكيانات كجداول ظاهرية في Dataverse يتيح هذا امكانيه اجراء عمليات CRUD من Dataverse وMicrosoft Power Platform علي البيانات الموجودة في الموارد البشرية. تدعم العمليات أيضا عمليات التحقق الكاملة من منطق العمل للموارد البشرية لضمان تكامل البيانات عند كتابه البيانات إلى الكيانات.

> [!NOTE]
> تتوافق كيانات Human Resources مع جداول Dataverse. لمزيد من المعلومات حول Dataverse (المعروف في السابق باسم Common Data Service) وتحديثات المصطلحات، راجع [الجديد في Microsoft Dataverse؟](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>الجداول الظاهرية المتاحة للموارد البشرية

تتوفر كافة كيانات بروتوكول البيانات المفتوحة (OData) في الموارد البشرية كجداول ظاهرية في Dataverse. وهي متوفرة أيضا في Power Platform. يمكنك الآن إنشاء التطبيقات والخبرة بالبيانات مباشره من الموارد البشرية التي لها قدره CRUD كامله، دون نسخ البيانات أو مزامنتها إلى Dataverse. يمكنك استخدام مداخل Power Apps لإنشاء مواقع ويب خارجيه تمكن سيناريوهات التعاون للعمليات التجارية في الموارد البشرية.

يمكنك عرض قائمة بالجداول الظاهرية الممكنة في البيئة، وبدء العمل مع الجداول في [Power Apps](https://make.powerapps.com) في حل **جداول HR الظاهرية لـ Dynamics 365**.

![جداول HR الظاهرية لـ Dynamics 365 في Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>الجداول الظاهرية مقابل الجداول الأصلية

لا تكون الجداول الظاهرية للموارد البشرية متماثلة مع جداول Dataverse الأصلية التي تم إنشاؤها للموارد البشرية. 

يتم إنشاء الجداول الأصلية للموارد البشرية بشكل منفصل وصيانتها في الحل الشائع HCM في Dataverse. باستخدام الجداول الأصلية، يتم تخزين البيانات في Dataverse وتتطلب مزامنة مع قاعدة بيانات التطبيق الخاصة بالموارد البشرية.

> [!NOTE]
> للحصول على قائمة بجداول Dataverse الأصلية للموارد البشرية، راجع [جداول Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>الإعداد

اتبع خطوات الإعداد هذه لتمكين الجداول الظاهرية في البيئة الخاصة بك.

### <a name="enable-virtual-tables-in-human-resources"></a>تمكين الجداول الظاهرية في الموارد البشرية

أولاً، يجب عليك تمكين الجداول الظاهرية في مساحة عمل **إدارة الميزات**.

1. في Human Resources، حدد **إدارة النظام**.

2. حدد الإطار المتجانب **إدارة الميزات**.

3. حدد **دعم الجدول الظاهري للموارد البشرية في Dataverse**، ثم حدد **تمكين**.

لمزيد من المعلومات حول تمكين الميزات وتعطيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>قم بتسجيل التطبيق في Microsoft Azure

يجب عليك تسجيل مثيل Human Resources الخاص بك في مدخل Azure حتى يتمكن النظام الأساسي لهويه Microsoft من توفير خدمات المصادقة والتخويل للتطبيق والمستخدمين. لمزيد من المعلومات حول تسجيل التطبيقات في Azure، راجع [التشغيل السريع: تسجيل تطبيق بواسطة النظام الأساسي لهويه Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. افتح [مدخل Microsoft Azure](https://portal.azure.com).

2. في قائمة خدمات Azure، حدد **عمليات تسجيل التطبيق**.

3. حدد **تسجيل جديد**.

4. في حقل **الاسم**، أدخل اسمًا وصفيًا للتطبيق. علي سبيل المثال، **جداول Dynamics 365 Human Resources الظاهرية**.

5. في الحقل **أعاده توجيه URI**، ادخل URL الخاص بمساحة الاسم لمثيل الموارد البشرية.

6. حدد **السجل**.

7. عند اكتمال التسجيل، يعرض مدخل Azure جزء **النظرة العامة** لتسجيل التطبيق الذي يتضمن **معرف التطبيق (العميل)**. سجل **معرف التطبيق (العميل)** في هذا الوقت. ستقوم بإدخال هذه المعلومات عند [تكوين مصدر بيانات الجدول الظاهري](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

8. في جزء التنقل الأيمن، حدد **الشهادات والاسرار**.

9. في القسم **أسرار العميل** في الصفحة، حدد **سر عميل جديد**.

10. قم بتوفير وصف، وحدد مده، وحدد **أضافه**.

11. سجل قيمة السر. ستقوم بإدخال هذه المعلومات عند [تكوين مصدر بيانات الجدول الظاهري](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

    > [!IMPORTANT]
    > تاكد من مراعاه قيمه السر في هذا الوقت. لا يتم عرض السر أبدا مره أخرى بعد مغادره هذه الصفحة.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>تثبيت تطبيق الجدول الظاهري Dynamics 365 HR Virtual Table

قم بتثبيت تطبيق الجدول الظاهري Dynamics 365 HR Virtual Table في البيئة Power Apps الخاصة بك لنشر حزمة حل الجدول الظاهري إلى Dataverse.

1. افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).

2. في قائمه **البيئات**، حدد بيئة Power Apps المقترنة بمثيل الموارد البشرية الخاص بك.

3. في القسم **الموارد** في الصفحة، حدد **تطبيقات Dynamics 365**.

4. حدد اجراء **تثبيت التطبيق**.

5. حدد **Dynamics 365 HR Virtual Table**، ثم حدد **التالي**.

6. مراجعه ووضع علامة علي الموافقة علي شروط الخدمة.

7. حدد **تثبيت**.

يستغرق التثبيت بضع دقائق. وعند الانتهاء، انتقل إلى الخطوات التالية.

![تثبيت تطبيق Dynamics 365 HR Virtual Table من مركز إدارة Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a>تكوين مصدر بيانات الجدول الظاهري 

الخطوة التالية هي تكوين مصدر البيانات الجدول الظاهري في بيئة Power Apps. 

1. افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).

2. في قائمه **البيئات**، حدد بيئة Power Apps المقترنة بمثيل الموارد البشرية الخاص بك.

3. حدد **عنوان URL للبيئة** في قسم **التفاصيل** من الصفحة.

4. في **مركز حماية الحل**، حدد الرمز **بحث متقدم** في الجزء العلوي الأيسر من صفحة التطبيق.

5. في صفحه **بحث متقدم**، وفي القائمة المنسدلة **البحث عن**، حدد **تكوينات مصدر البيانات الظاهري Finance and Operations**.

6. حدد **النتائج**.

7. حدد سجل **مصدر بيانات الموارد البشرية من Microsoft**.

8. أدخل المعلومات المطلوبة لتكوين مصدر البيانات:

   - **URL الهدف**: عنوان URL لمساحة اسم الموارد البشرية الخاصة بك. تنسيق عنوان URL الهدف هو:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     على سبيل المثال:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >تأكد من تضمين الحرف "**/**" في نهاية عنوان URL لتجنب تلقي خطأ ما.

   - **معرف المستاجر**: معرف المستاجر في Azure Active Directory ( Azure AD).

   - **معرف تطبيق AAD**: معرف التطبيق (العميل) الذي تم إنشاؤه للتطبيق المسجل في مدخل Microsoft Azure. لقد تلقيت هذه المعلومات مبكرا اثناء الخطوة [تسجيل التطبيق في Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **سر تطبيق AAD**: سر التطبيق الذي تم إنشاؤه للتطبيق المسجل في مدخل Microsoft Azure. لقد تلقيت هذه المعلومات مبكرا اثناء الخطوة [تسجيل التطبيق في Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![مصدر بيانات الموارد البشرية في Microsoft](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. حدد **حفظ وإغلاق**.

### <a name="grant-app-permissions-in-human-resources"></a>منح أذونات التطبيق في الموارد البشرية

امنح أذونات لتطبيقي Azure AD في الموارد البشرية:

- التطبيق الذي تم إنشاؤه للمستاجر في مدخل Microsoft Azure
- تطبيق Dynamics 365 HR Virtual Table الذي تم تبثبيته في من بيئة Power Apps 

1. في الموارد البشرية، افتح صفحة **تطبيقات Azure Active Directory**.

2. حدد **جديد** لإنشاء سجل تطبيق جديد:

    - في الحقل **معرف العميل**، ادخل معرف العميل الخاص بالتطبيق الذي قمت بتسجيله في مدخل Microsoft Azure.
    - في الحقل **معرف العميل**، ادخل معرف العميل الخاص بالتطبيق الذي قمت بتسجيله في مدخل Microsoft Azure.
    - في الحقل **معرف المستخدم** ، حدد معرف المستخدم الخاص بمستخدم لديه أذونات المسؤول في الموارد البشرية وبيئة Power Apps.

3. حدد **جديد** لإنشاء سجل تطبيق ثانٍ:

    - **معرف العميل**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **الاسم**: Dynamics 365 HR Virtual Table
    - في الحقل **معرف المستخدم** ، حدد معرف المستخدم الخاص بمستخدم لديه أذونات المسؤول في الموارد البشرية وبيئة Power Apps.

## <a name="generate-virtual-tables"></a>إنشاء جداول ظاهرية

عند اكتمال الإعداد، يمكنك تحديد الجداول الظاهرية التي ترغب في إنشائها وتمكينها في مثيل Dataverse الخاص بك.

1. في الموارد البشرية، افتح صفحة **تكامل Dataverse**.

2. حدد علامة التبويب **الجداول الظاهرية**.

> [!NOTE]
> سيتم تعيين زر التبديل **تمكين الجداول الظاهرية** إلى **نعم** تلقائيًا عند اكتمال كافة الإعدادات المطلوبة. إذا تم تعيين زر التبديل إلى **لا**، فراجع الخطوات الموجودة في الأقسام السابقة من هذا المستند لضمان إكمال كافة إعدادات المتطلبات الأساسية.

3. حدد الجدول أو الجداول التي ترغب في إنشائها في Dataverse.

4. حدد **إنشاء/تحديث**.

![تكامل Dataverse](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a>التحقق من حالة إنشاء الجدول

يتم إنشاء الجداول الظاهرية في Dataverse خلال عملية خلفية غير متزامنة. تعرض التحديثات على العملية في مركز الإجراء. تظهر التفاصيل الخاصة بالعملية، بما في ذلك سجلات الأخطاء، في الصفحة **التنفيذ التلقائي للعمليات**.

1. في Human Resources، افتح الصفحة **التنفيذ التلقائي للعمليات**.

2. حدد علامة التبويب **عمليات الخلفية**.

3. حدد **عملية خلفية للتشغيل غير المتزامن لاستقصاء الجدول الظاهري**.

4. حدد **عرض أحدث النتائج**.

يعرض الجزء المنبثق للخارج أحدث نتائج التنفيذ للعملية. يمكنك عرض السجل للعملية، بما في ذلك أية أخطاء تم إرجاعها من Dataverse.

## <a name="see-also"></a>راجع أيضًا

[ما هو Dataverse؟](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[الجداول في Dataverse](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[نظرة عامة على علاقات الجداول](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[إنشاء جداول ظاهرية تحتوي على بيانات من مصدر بيانات خارجي وتحريرها](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[ما المقصود بمداخل Power Apps؟](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[نظره عامه حول إنشاء التطبيقات في Power Apps](https://docs.microsoft.com/powerapps/maker/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]