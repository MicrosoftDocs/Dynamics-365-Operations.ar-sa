---
title: البدء باستخدام إدارة خدمة الفوترة الإلكترونية
description: يوضح هذا الموضوع كيفية بدء استخدام الفوترة الإلكترونية.
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f77c8fd1696b74f852d04cc0a696d4816ef9af1f
ms.sourcegitcommit: 5033d42a2aac852916d726e40bd98a164d1a837d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/23/2022
ms.locfileid: "7984818"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>البدء باستخدام إدارة خدمة الفوترة الإلكترونية

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل أن تتمكن من استكمال الإجراءات في هذا الموضوع، يجب إتمام المهام المتطلبات التالية:

- يجب أن يكون لديك حق الوصول إلى حساب Microsoft Dynamics Lifecycle Services (LCS).
- يجب أن يكون لديك مشروع LCS يتضمن إصدار 10.0.17 أو إصدار أحدث من Microsoft Dynamics 365 Finance أو Dynamics 365 Supply Chain Management. بالإضافة إلى ذلك، يجب أن يتم نشر هذه التطبيقات في أحد مناطق Azure الجغرافية التالية:

    - الولايات المتحدة
    - أوروبا
    - المملكة المتحدة
    - آسيا

- يجب أن يكون لديك حق الوصول إلى حساب Dynamics 365 Regulatory Configuration Services (RCS)
- يجب تشغيل ميزة العولمة لحساب RCS في إدارة الميزات. لمزيد من المعلومات، راجع [Regulatory Configuration Services (RCS) - ميزات العولمة](rcs-globalization-feature.md).
- يجب إنشاء مخزن رئيسي وحساب تخزين في Azure. لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>تثبيت الوظيفة الإضافية للخدمات المصغرة في Lifecycle Services

1. قم بالتسجيل في حساب LCS، وعلى لوحة معلومات مشروع LCS، حدد مشروع LCS.
2. في المشروع، على لوحة معلومات **البيئة**، حدد البيئة المنشورة لك. يجب أن تكون البيئة التي تحددها قيد التشغيل.
3. في علامة التبويب تكامل **Power Platform**، في مجموعة الحقل **الوظائف الإضافبة للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.
4. حدد **الفوترة الإلكترونية**.
5. في حقل **معرف تطبيق AAD**، أدخل **091c98b0-a1c9-4b02-b62c-7753395ccabe**. هذه قيمة ثابتة.
6. في الحقل **معرف مستأجر AAD**، أدخل معرف المستأجر لحساب اشتراك Azure. يجب أن يكون مستأجر Azure Active Directory (Azure AD) الذي تحدده هو نفس المستأجر المستخدم لـ RCS.
7. راجع البنود والشروط، ثم حدد خانة الاختيار.
8. حدد **تثبيت**. قد تستغرق عملية التثبيت عدة دقائق.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>إعداد المعلمات لتكامل RCS باستخدام الفوترة الإلكترونية

1. سجل دخولك إلى حساب RCS.
2. في مساحة عمل **ميزات العولمة**، في قسم **الإعدادات ذات الصلة**، حدد **معلمات التقارير الإلكترونية**.
3. في علامة تبويب **الفوترة الإلكترونية**، في حقل **URI لنقطة نهاية الخدمة**، أدخل نقطة نهاية الخدمة المناسبة لمنطقة Azure الجغرافية الخاصة بك، كما هو موضح في الجدول التالي.

    | منطقة Azure الجغرافية لمركز البيانات | عنوان URI لنقطة نهاية الخدمة                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | الولايات المتحدة              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | أوروبا                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | المملكة المتحدة             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | آسيا                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. تأكد من أنه تم تعيين حقل **معرف التطبيق** إلى **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. هذه القيمة هي قيمة ثابتة.
5. في الحقل **معرف بيئة LCS**، أدخل معرف بيئة LCS الخاصة بك.
6. حدد **حفظ** ثم قم بإغلاق الصفحة.

## <a name="create-key-vault-references"></a>إنشاء مراجع المخزن الرئيسي

1. سجل دخولك إلى حساب RCS.
2. في مساحة عمل **ميزات العولمة**، في قسم **البيئة**، حدد الإطار المتجانب **الفوترة الإلكترونية**.
3. في صفحة **إعدادات البيئة**، في جزء الإجراء، حدد **بيئات الخدمة**، ثم حدد **معلمات المخزن الرئيسي**.
4. حدد **جديد** لإنشاء مرجع المخزن الرئيسي.
5. في حقل **الاسم**، أدخل اسم مرجع المخزن الرئيسي. في الحقل **الوصف**، أدخل وصفًا.
6. في حقل **URI للمخزن الرئيسي**، قم بلصق سر المخزن الرئيسي من مخزن Azure الرئيسي. لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).
7. حدد **حفظ**.

## <a name="create-storage-account-secret"></a>إنشاء سر حساب التخزين

1. في صفحة **إعدادات البيئة**، في جزء الإجراء، حدد **بيئة الخدمة** > **معلمات المخزن الرئيسي**.
2. حدد **مرجع المخزن الرئيسي** وفي قسم **الشهادات**، حدد **إضافة**.
3. في حقل **الاسم**، أدخل اسم سر حساب التخزين. لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).
4. في الحقل **الوصف**، أدخل وصفًا.
5. في حقل **النوع**، حدد **سر**.
6. حدد **حفظ** ثم قم بإغلاق الصفحة.

## <a name="create-a-digital-certificate-secret"></a>إنشاء كلمة سر لشهادة رقمية

1. في صفحة **إعدادات البيئة**، في جزء الإجراء، حدد **بيئة الخدمة**، ثم حدد **معلمات المخزن الرئيسي**.
2. حدد **مرجع المخزن الرئيسي** ثم في قسم **الشهادات**، حدد **إضافة**.
3. في حقل **الاسم**، أدخل اسم سر الشهادة الرقمية. لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).
4. في الحقل **الوصف**، أدخل وصفًا.
5. في حقل **النوع**، حدد **الشهادة**.
6. حدد **حفظ** ثم قم بإغلاق الصفحة.

## <a name="create-a-service-environment"></a>إنشاء بيئة خدمة

1. سجل دخولك إلى حساب RCS.
2. في مساحة عمل **ميزات العولمة**، في قسم **البيئة**، حدد الإطار المتجانب **الفوترة الإلكترونية**.
3. في صفحة **إعدادات البيئة**، وفي جزء الإجراء، حدد **بيئة الخدمة**.
4. حدد **جديد** لإنشاء بيئة خدمة جديدة.
5. في حقل **الاسم**، أدخل اسم بيئة الفوترة الإلكترونية. في الحقل **الوصف**، أدخل وصفًا.
6. في حقل **سر رمز SAS المميز للتخزين**، حدد اسم حساب التخزين الذي يجب استخدامه لمصادقة الوصول إلى حساب التخزين.
7. في قسم **المستخدمون**، حدد **إضافة** لإضافة مستخدم يسمح له بإرسال الفواتير الإلكترونية من خلال البيئة والاتصال أيضًا بحساب التخزين.
8. في حقل **معرف المستخدم**، ادخل الاسم المستعار للمستخدم. ثم، في حقل **‏‫البريد الإلكتروني**، أدخل عنوان البريد الإلكتروني للمستخدم.
9. حدد **حفظ**.
10. إذا كانت الفواتير الخاصة ببلدك/منطقتك تتطلب سلسلة من الشهادات لتطبيق التوقيعات الرقمية، ففي جزء الإجراء، حدد **معلمات المخزن الرئيسي**، ثم حدد **تسلسل الشهادات** واتبع هذه الخطوات.

    1. حدد **جديد** لإنشاء سلسلة من الشهادات.
    2. في حقل **الاسم**، أدخل اسم تسلسل الشهادات. في الحقل **الوصف**، أدخل وصفًا.
    3. في قسم **الشهادات**، حدد **إضافة** لإضافة شهادة إلى السلسلة.
    4. استخدم الزر **لأعلى** أو **لأسفل** لتغيير موضع الشهادة في السلسلة.
    5. حدد **حفظ** ثم قم بإغلاق الصفحة.
    6. قم بإغلاق الصفحة.

11. في صفحة **بيئة الخدمة**، في جزء الإجراءات، حدد **نشر** لنشر البيئة إلى السحابة. تغيرت القيمة في حقل **الحالة** إلى **منشور**.

## <a name="create-a-connected-application"></a>إنشاء تطبيق متصل

1. في صفحة **إعداد البيئات**، في جزء الإجراء ، حدد **التطبيقات المتصلة**.
2. حدد **جديد** لإنشاء تطبيق متصل.
3. في حقل **الاسم**، أدخل اسم التطبيق المراد الاتصال به.
4. في حقل **التطبيق**، أدخل عنوان URL الخاص ببيئة Finance وSupply Chain Management المراد الاتصال بها.
4. في حقل **المستأجر**، أدخل المستأجر الخاص ببيئة Finance وSupply Chain Management.
5. حدد **حفظ**.
6. في جزء الإجراء ، حدد **فحص اتصال** لاختبار الاتصال مع البيئة. ثم أغلق الصفحة.

## <a name="link-connected-applications-to-environments"></a>ربط التطبيقات المتصلة بالبيئات

1. في صفحة **إعداد البيئات**، حدد **جديد** لتعيين تطبيق متصل لإحدى البيئات.
2. في حقل **التطبيق المتصل**، حدد أحد التطبيقات المتصلة.
3. في حقل **بيئة الخدمة**، حدد بيئة الخدمة.
4. حدد **حفظ** ثم قم بإغلاق الصفحة.

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>إعداد تكامل الفوترة الإلكترونية في Finance وSupply Chain Management

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>تشغيل ميزة تكامل الفوترة الإلكترونية

1. سجل دخولك إلى مثيل Finance أو Supply Chain Management.
2. في مساحة عمل **إدارة الميزات**، ابحث عن ميزة **تكامل الفوترة الإلكترونية**. إذا لم تظهر هذه الميزة على الصفحة ، فحدد **التحقق من وجود تحديثات**.
3. حدد الميزة، ثم حدد **تمكين الآن**.

### <a name="set-up-the-service-endpoint-url"></a>إعداد URL نقطة نهاية الخدمة

1. انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.
2. في علامة تبويب **الفوترة الإلكترونية**، في حقل **URL لنقطة نهاية الخدمة**، أدخل نقطة نهاية الخدمة المناسبة لمنطقة Azure الجغرافية الخاصة بك، كما هو موضح في الجدول التالي.

    | منطقة Azure الجغرافية لمركز البيانات | عنوان URI لنقطة نهاية الخدمة                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | الولايات المتحدة              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | أوروبا                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | المملكة المتحدة             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | آسيا                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. في حقل **البيئة**، أدخل اسم بيئة الخدمة المنشورة في الفوترة الإلكترونية.
4. حدد **حفظ** ثم قم بإغلاق الصفحة.

### <a name="enable-flighting-keys-for-finance-or-supply-chain-management-version-10017"></a>تمكين مفاتيح العرض للتقييم للإصدار 10.0.17 من Finance أو Supply Chain Management

1. قم بتنفيذ أمر SQL التالي:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. تنفيذ أمر IISreset لجميع خوادم كائنات التطبيقات.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
