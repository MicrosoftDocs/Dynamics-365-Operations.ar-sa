---
title: تمكين البحث عن البيانات الرئيسية لتكوين حساب الضريبة
description: توضح هذه المقالة كيفية إعداد وظيفة البحث عن البيانات الرئيسية لحساب الضريبة وتمكينها.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3642bb88d5b0570014513b64eef5fdab6d1ee9d3
ms.sourcegitcommit: 5b721f6fc1ba4350b5bd0eae457f71d80246db42
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/20/2022
ms.locfileid: "9181113"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>تمكين البحث عن البيانات الرئيسية لتكوين حساب الضريبة 

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية إعداد وظيفة البحث عن البيانات الرئيسية لحساب الضريبة وتمكينها. تتوفر قائمة منسدلة لتحديد القيم في تكوين حساب الضريبة لحقول مثل **كيان قانوني** و **حساب المورد** و **كود الصنف** و **مدة التسليم**. تأتي هذه القيم من بيئة Microsoft Dynamics 365 Finance المتصلة باستخدام مصدر بيانات Microsoft Dataverse.

> [!NOTE] 
> تُعد وظيفة البحث عن البيانات الرئيسية لحساب الضريبة وظيفة اختيارية. يمكنك تخطي الخطوات التالية إذا قمت بتعطيل الميزة **دعم مصدر البيانات Dataverse لخدمة الضرائب** في Regulatory Configuration Service (RCS). ومع ذلك، في هذه الحالة، لن تتوفر القائمة المنسدلة في تكوين حساب الضريبة.

لتمكين القائمة المنسدلة في تكوين إصدار الميزة الخاص بحساب الضريبة ، أكمل الخطوات التالية.

1. [قم بتمكين Microsoft Power Platform التكامل وفتح البيئة Dataverse .](#enable)
2. [تثبيت الكيانات الافتراضية للتمويل والعمليات.](#install)
3. [تسجيل Azure Active Directory (Azure AD) تطبيق.](#register)
4. [منح أذونات التطبيق في العمليات المالية وتطبيقات العمليات.](#grant)
5. [تكوين مصدر بيانات الكيان الظاهري](#configure)
6. [تمكين Dataverse كيانات الظاهرية.](#virtual)
7. [يستخدم في اعداد التطبيق المتصل لحساب الضريبة.](#set-up)
8. [استيراد وإنشاء Dataverse تكوين رسم الخرائط النموذجية.](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a>قم بتمكين Microsoft Power Platform التكامل وفتح Dataverse البيئة

يمكن تمكين تكامل الخدمات المالية وتطبيقات Microsoft Power Platformالعمليات عند إنشاء بيئة جديده وتطبيقات عمليات للعمليات المالية في خدمات دوره الحياة Microsoft Dynamics (LCS). لمزيد من المعلومات، راجع [تكامل Microsoft Power Platform - نظرة عامة على الوظائف الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). بعد الانتهاء ، سيظهر اسم بيئة Microsoft Power Platform في قسم **التكامل Power Platform**.

1. في LCS ، في بيئة التمويل والعمليات الخاصة بك ، في **Power Platform التكامل** ، ابحث عن ملف **اسم البيئة** قيمة للبيئة المرتبطة.

    [![قيمة اسم البيئة.](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. In the [Power Platform مركز الإدارة](https://admin.powerplatform.microsoft.com/environments), on the **البيئة** علامة التبويب، حدد البيئة التي تتطابق مع **اسم البيئة** القيمة التي قمت بتدوينها.
3. في صفحه **التفاصيل** ، ابحث عن **قيمه عنوان URL** للبيئة الخاصة بالبيئة Dataverse. قم بتدوين هذه القيمة ، لأنك ستحتاج إليها [الخطوة 7. قم بإعداد التطبيق المتصل لحساب الضرائب](#set-up).
4. تاكد من انه يمكنك فتح البيئة Dataverse في المستعرض الخاص بك عن طريق تحديد قيمه عنوان URL **الخاص بالبيئة**.

    [![Dataverseصفحة البيئة في LCS](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > احتفظ  Dataverse بيئة مفتوحة في متصفحك.. ستحتاج اليها في الخطوة الخامسة [ . تكوين مصدر ](#configure)بيانات الوحدة الظاهرية.

وللحصول على المزيد من المعلومات، راجع [تمكين تكامل Microsoft Power Platform](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a>تثبيت الكيانات الافتراضية للتمويل والعمليات

يجب تثبيت الحل الخاص بالكيانات المالية والعمليات الظاهرية Dataverseمن Microsoft AppSourceحل الكيان الظاهري.

1. في AppSource، أعثر على [الكيان الافتراضي للتمويل والعمليات](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. حدد **احصل عليها الآن**.
3. في الحقل **حدد بيئة** ، ادخل **قيمه اسم** البيئة التي قمت بإنشاءها في وقت سابق.
4. حدد خانات الاختيار ، ثم حدد **تثبيت**.

عند اكتمال التثبيت ، يمكنك العثور على ملف **الكيان الافتراضي للتمويل والعمليات** التطبيق في [Power Platform مركز الإدارة](https://admin.powerplatform.microsoft.com/), under **الموارد** \> **تطبيقات Dynamics 365**.

لمزيد من المعلومات، راجع [تمكين الكيانات الظاهرية](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a>تسجيل Azure AD تطبيق

يجب تسجيل أحد Azure AD التطبيقات علي نفس المستأجر مثل المالية وتطبيقات العمليات ، بحيث يمكن استدعاؤها بواسطة Dataverse.

1. في [Azure portal](https://portal.azure.com)اذهب إلى، **Azure Active Directory \> تسجيل التطبيق**.
2. حدد **تسجيل تطبيق جديد**، ثم قم بإدخال المعلومات التالية:

    - **الاسم** ، أدخل اسمًا فريد.
    - **نوع** الحساب – ادخل **اي Azure AD دليل** (المستأجر الواحد أو المستأجر المتعدد).
    - **إعادة توجيه URI:** اترك هذا الحقل فارغًا.

3. حدد **السجل**.
4. قم بتدوين قيمة **رقم التطبيق (العميل)**، لأنك ستحتاج إليها لاحقًا.

    [![Azure AD قيمة معرف التطبيق (العميل)](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. إنشاء مفتاح متماثل للتطبيق.
6. في التطبيق الجديد ، حدد **الشهادات ال& اسرار**.
7. حدد **سر عميل جديد**.
8. ادخل وصفا ، ثم حدد تاريخ انتهاء الصلاحية ، ثم حدد **حفظ**. سيتم إنشاء مفتاح وإظهاره. يستخدم هذا الزر في نسخ القيمة لاستخدامها لاحقا.

لمزيد من المعلومات، راجع [تسجيل Azure AD التطبيق](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a>منح أذونات التطبيق في العمليات المالية وتطبيقات العمليات.

Dataverse استخدام التطبيق Azure AD الذي قمت بإنشاءه لاستدعاء العمليات المالية وتطبيقات العمليات. لذلك ، يجب ان يكون التطبيق موثوق به من قبل تطبيقات التمويل والعمليات والمقترن بحساب مستخدم لديه الحقوق المناسبة. في تطبيقات المعالجة المالية والعمليات ، يجب إنشاء مستخدم خدمه خاص يمتلك حقوقا **لوظيفة الكيان الظاهري فقط**. لا يجب ان يكون لمستخدم الخدمة هذا حقوق أخرى. بعد إكمال هذه الخطوة ، سيتمكن اي تطبيق لديه سر Azure AD التطبيق الذي قمت بإنشاءه من استدعاء بيئة تطبيقات العمليات المالية والعمليات والوصول إلى وظيفة الوحدة الظاهرية.

1. في بيئتك، انتقل إلى **‎إدارة النظام** \> **المستخدمون** \> **المستخدمون**.
2. حدد **جديد** لإضافة مستخدم جديد، وإدخال المعلومات التالية:.

    - **معرف** المستخدم – ادخل **‎dataverseintegration** أو قيمه أخرى.
    - **اسم المستخدم** – أدخل **dataverse integration** أو قيمه أخرى.
    - **المستخدم** – تعيين هذا الحقل إلى **NonAAD**.
    - **البريد الإلكتروني** – ادخل **dataverseintegration‎** أو قيمه أخرى. (لا يجب ان تكون القيمة حساب بريد الكتروني صالح.)

3. تعيين **تطبيق الكيان الظاهري CDS** دور الأمان للمستخدم.
4. قم بازالة كافة الأدوار الأخرى ، بما في ذلك **مستخدم** النظام.
5. انتقل إلى **إدارة النظام** \> **إعداد** \> **Azure Active Directory التطبيقات** للتسجيل Dataverse. 
6. قم باضافة صف ، ثم في الحقل معرف **العميل** ، ادخل **قيمه معرف** التطبيق (العميل) التي قمت بإنشاء ملاحظه لها في وقت سابق.
7. في حقل **الاسم**، أدخل اسمًا. على سبيل المثال، أدخل **Dataverse التكامل**.
8. في حقل **معرف المستخدم** ، أدخل معرف المستخدم الذي قمت بإنشائه مسبقًا.

لمزيد من المعلومات، راج [امنح أذونات التطبيق في تطبيقات التمويل والعمليات](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>تكوين مصدر بيانات الكيان الظاهري

يجب التزويد Dataverse بالتمويل ومثيل التطبيق الخاص بالعمليات المطلوب الاتصال به.

1. يجب Dataverse أن تظل البيئة مفتوحة في متصفحك من [الخطوة 1. تمكين Microsoft Power Platform التكامل وافتح Dataverse البيئة](#enable). حدد زر الإعدادات (رمز الترس) في الجزء العلوي الأيمن ، ثم حدد **الإعدادات المتقدمة**.

    [![فتح الإعدادات المتقدمة في ملف Dataverse البيئة.](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. في **الإعدادات** القائمة المنسدلة، حدد **الإدارة‏‎**.

    [![الإدارة.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. حدد **مصادر بيانات الكيان الافتراضي**.

    [![مصادر بيانات الكيان الافتراضي.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. حدد مصدر البيانات المسمى **Finance and Operations**.

    [![مصدر بيانات Finance and Operations.](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. أدخل المعلومات التالية من الخطوات السابقة:

    - **الرابط** – أدخل عنوان URL حيث يمكنك الوصول إلى تطبيقات المالية والعمليات.
    - **عنوان URL لـ OAuth** – أدخل `https://login.windows.net/`.
    - **معرف المستأجر** –حدد المستأجر الخاص بك. يمكن أن تكون هذه القيمة اسم المجال للبريد الإلكتروني لشركتك (مثل contoso.com).
    - **معرف تطبيق AAD** – أدخل **معرف التطبيق (العميل)** القيمة التي تم إنشاؤها مسبقًا.
    - **سر تطبيق AAD** – أدخل السر الذي تم إنشاؤه في وقت سابق.
    - **مورد AAD** – أدخل **00000015-0000-0000-c000-000000000000**. هذه القيمة هي Azure AD تطبيق يمثل تطبيقات المالية والعمليات. يجب دائما ان تكون بنفس القيمة.

6. ‏‏قم بحفظ التغييرات التي قمت بإجرائها.
7. أغلق الصفحة للعودة إلى ملف **الإدارة** الصفحة حيث ستبدأ [الخطوة 6. تمكين Dataverse الكيانات الافتراضية](#virtual).

    [![إغلاق الكيان للتحرير.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

لمزيد من المعلومات، راجع [تكوين مصدر بيانات الكيان الظاهري](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a>تمكين Dataverse كيانات  الظاهرية

يجب تعيين امكانيه رؤية الكيانات الظاهرية من التمويل وتطبيقات العمليات إلى **نعم** قبل ان يتم استهلاكها بواسطة تكوين حساب الضريبة.

> [!NOTE]
> يمكنك تجاوز هذه الخطوة عن طريق تمكين الكيانات الظاهرية المرتبطة بحساب الضريبة بنقره واحده فقط في الخطوة [رقم 8. يستخدم في اعداد التطبيق المتصل لحساب](#import)الضريبة. ومع ذلك ، نوصي بتمكين كيان ظاهري واحد علي الأقل يدويا للإشارة إلى ان الاتصال بين المالية وتطبيقات العمليات وتم Dataverse تأسيسه بشكل جيد.

1. في البيئة الخاصة بك Dataverse ، في **الصفحة أداره** ، حدد زر التصفية (رمز قمع) في الركن الأيمن العلوي.

    [![زر التصفية](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. في الإطار **بحث** متقدم ، في الحقل **البحث عن** ، حدد **كيانات** العمليات المالية والعمليات المتوفرة.
3. قم بإضافه القاعدة التالية: **الاسم** - **يحتوي** **CompanyInfoEntity‎**. ثم حدد **النتائج**.

    [![اطار البحث المتقدم.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. حدد **CompanyInfoEntity‎** في نتائج البحث ، وحدد خانه الاختيار **المرئية** ، ثم حدد **حفظ**.

    [![تعيين امكانيه رؤية الكيان.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. قم بتكرار الخطوات السابقة للكيانات التالية التي يتم الإشاره اليها في تكوين حساب الضريبة:

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > يمكن استرداد السجلات 5,000 الاولي فقط من الكيان بواسطة وتوفيرها Dataverse في القائمة المنسدلة لتكوين حساب الضريبة.

لمزيد من المعلومات، راجع [تمكين الكيانات الظاهرية Microsoft Dataverse](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a>يستخدم في اعداد التطبيق المتصل لحساب الضريبة.

1. في RCS ، افتح **إدارة الميزات** ، ثم قم بتمكين الميزات التالية:

    - دعم مصادر بيانات Dataverse لإعداد التقارير الإلكترونية
    - دعم مصادر بيانات Dataverse لخدمة الضرائب
    - ميزات العولمة

2. انتقل إلى **‎إعداد التقارير الإلكترونية** وفي **الارتباطات‬ ذات الصلة** حدد **التطبيقات المتصلة اتصال آمن**.

    [![التطبيقات المتصلة](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

3. حدد **جديد** لإضافة سجل ، وإدخال المعلومات التالية..

    - **الاسم** – أدخل اسمًا.
    - **تحديد** – النوع **Dataverse**.
    - **التطبيق** – ادخل قيمه URL Dataverse الخاصة ببيئة البيئة **الخاصة بك** ، والتي قد قمت بعمل ملاحظه لها في [الخطوة 1. قم بتمكين Microsoft Power Platform التكامل وافتح البيئة Dataverse الخاصة بك ](#enable).
    - **المستاجر** – إدخال المستأجر الخاص بك.
    - **‎عنوان URL‏‎ مخصص** – أدخل Dataverse URL، وإلحاق **/api/data/v9.1** له.

4. حدد **التحقق من الاتصال** ، ثم في مربع الحوار الذي يظهر ، حدد **انقر هنا للاتصال بالتطبيق** البعيد المحدد.

    [![فحص الإتصال.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
5. تأكد من ظهور الرسالة "نجاح!". الرسالة التي تشير إلى انه تم تأسيس الاتصال بنجاح.

    [![رسالة نجاح.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a>استيراد وإعداد Dataverse تكوين رسم الخرائط النموذجية

توفر Microsoft تكوينات تعيين النموذج الافتراضية للكيانات من تطبيقات العمليات المالية وتطبيقات العمليات إلى حساب الضريبة.

1. في RCS، انتقل إلى **إعداد التقارير الإلكترونية**.
2. في **موفرو التكوين** على البلاط من أجل **Microsoft** مزود، حدد **‎المستودعات**.

    [![المستودعات](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. حدد **مستودع التكوين العام** سجل، ثم حدد **فتح**.
4. ضمن **نموذج البيانات الضريبية** \> **نموذج بيانات حساب الضريبة**، حدد **Dataverse رسم الخرائط النموذجية** ترتيب.
5. في **الإصدارات FastTab** ، حدد إصدارا يتوافق مع التمويل وإصدار تطبيقات العمليات ، ثم حدد **استيراد**.

    [![استيراد Dataverse تعيين نموذج التقارير الإلكتروني.](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > يكون **Dataverse تكوين تعيين** النموذج فعالا فقط علي الإصدار الأعلى الذي تم استيراده. التالي ، يجب الا تقوم باستيراد إصدار من **Dataverseتكوين تعيين** النموذج الذي يكون اعلي من إصدار تكوين حساب الضريبة الذي تخطط لتنفيذه. على سبيل المثال ، إذا كنت تخطط لتنفيذ الإصدار 40.50.225 من تكوين حساب الضريبة ، فيجب عليك استيراد الإصدار 40.50.13 فقط من **Dataverse رسم الخرائط النموذجية** التكوين. يجب الا تقوم باستيراد 40.54.14 الإصدار. والا ، سيكون هناك عدم تطابق في نموذج البيانات في التكوين.

6. انتقل إلى مساحة عمل **إعداد التقارير الإلكترونية**، حدد **لوحة تكوينات الضرائب**.
7. حدد تكوين تخصيص **Dataverse النموذج الذي تم استيراده** ، ثم حدد **تحرير**.
8. قم بتعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم.**
9. في **التطبيق متصل** ، حدد التطبيق المتصل الذي قمت بإعداده فيه [الخطوة 7. قم بإعداد التطبيق المتصل لحساب الضرائب](#set-up).
10. قم بتعيين الخيار **تعيين رؤية** الجدول الظاهري إلى **نعم** لتعيين كافة الكيانات الظاهرية المتعلقة بحساب الضريبة إلى مرئية.

وقد أكملت الآن عمليه الاعداد الخاصة بوظيفة بحث البيانات الرئيسية. سيتم الآن تمكين قائمه منسدلة للحقول مثل الكيان **القانوني وحساب** **المورد وكود** **الصنف ومصطلح** التسليم **من المالية Dynamics 365 في** اعداد إصدار **خاصيه حساب الضريبة**.

[![القائمة المنسدلة للكيان القانوني.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
