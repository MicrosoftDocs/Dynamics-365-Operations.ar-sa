---
title: الترقية إلى الطرف ونموذج دفتر العناوين العمومي
description: يصف هذا الموضوع كيفية ترقية بيانات الكتابة المزدوجة إلى الطرف ونموذج دفتر العناوين العمومي‬.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857360"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>الترقية إلى الطرف ونموذج دفتر العناوين العمومي

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يساعدك [قالب Azure Data Factory](https://aka.ms/dual-write-gab-adf) على ترقية بيانات جدول **حساب** و **جهة اتصال** و **مورّد** موجود في الكتابة المزدوجة إلى نموذج الطرف ودفتر العناوين العمول يقوم القالب بتسوية البيانات من تطبيقات Finance and Operations وتطبيقات مشاركة العميل. في نهاية العملية، سيتم إنشاء حقلي **الطرف** و **جهة الاتصال** لسجلات **الطرف** وربطها بسجلات **الحساب** و **جهة الاتصال** و **المورّد** في تطبيقات مشاركة العميل. يتم إنشاء ملف csv. (`FONewParty.csv`) لإنشاء سجلات **طرف** جديدة داخل تطبيق Finance and Operations. يوفر هذا الموضوع الإرشادات الخاصة باستخدام قالب Data Factory وترقية البيانات.

إذا لم يكن لديك أي تخصيصات، فيمكنك استخدام القالب كما هو. إذا كانت لديك تخصيصات لسجلات **الحساب** و **جهة الاتصال** و **المورّد**، فيجب تعديل القالب باستخدام الإرشادات التالية.

> [!Note]
> يساعدك القالب على ترقية بيانات **الطرف**. سيتم تضمين العناوين البريدية والإلكترونية في إصدار مستقبلي.

## <a name="prerequisites"></a>المتطلبات الأساسية

هذه المتطلبات الأساسية مطلوبة:

+ [اشتراك Azure](https://portal.azure.com/)
+ [الوصول إلى القالب](https://aka.ms/dual-write-gab-adf)
+ أنت عميل موجود للكتابة المزدوجة.

## <a name="prepare-for-the-upgrade"></a>التحضير للترقية

+ **متزامنة بالكامل**: البيئتان في حالة متزامنة بالكامل لسجلات **الحساب (العميل)** و **جهة الاتصال** و **المورّد**.
+ **مفاتيح التكامل**: تستخدم جداول **الحساب (العميل)** و **جهة الاتصال** و **المورّد** في تطبيقات مشاركة العميل مفاتيح التكامل المشحونة الجاهزة. إذا قمت بتخصيص مفاتيح التكامل، فيجب تخصيص القالب.
+ **رقم الطرف**: سيكون لجميع سجلات **الحساب (العميل)** و **جهة الاتصال** و **المورّد** التي سيتم ترقيتها رقم **طرف**. سيتم تجاهل السجلات التي لا تحتوي على رقم **طرف**. إذا كنت ترغب في ترقية تلك السجلات، فيمكنك إضافة رقم **طرف** إليها قبل بدء عملية الترقية.
+ **انقطاع العمل في النظام**: أثناء عملية الترقية، يجب عليك وضع بيئات Finance and Operations وبيئات مشاركة العميل في وضع عدم الاتصال.
+ **لقطة**: خذ لقطات لتطبيقات Finance and Operations وتطبيقات مشاركة العميل. استخدم اللقطات لاسترجاع الحالة السابقة إذا احتجت لذلك.

## <a name="deployment"></a>النشر

1. نزّل القالب من [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).

2. سجل دخولك إلى [Microsoft Azure](https://portal.azure.com/).

3. أنشئ [مجموعة موارد](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).

4. أنشئ [حساب تخزين](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) في مجموعة الموارد التي أنشأتها.

5. أنشئ [مصنع بيانات](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) في مجموعة الموارد أعلاه التي أنشأتها.

6. افتح مصنع البيانات وحدد اللوحة **التأليف والمراقبة**.

7. على علامة التبويب **إدارة**، حدد **قالب ARM**.

8. حدد **استيراد قالب ARM** لاستيراد قالب **الطرف‏‎**.

9. استورد القالب إلى مصنع البيانات. أدخل القيم التالية في **تفاصيل المشروع** و **تفاصيل المثيل**.

    الحقل | قيمة
    ---|---
    الاشتراك | اشتراك Azure
    مجموعة الموارد | قدم المورد نفسه الذي يتم إنشاء حساب التخزين ضمنه.
    المنطقة | حدد منطقة.
    اسم المصنع | حدد اسم المصنع.
    FO Linked Service_service Principal Key | حدد مفتاح التطبيق.
    Azure Blob Storage_connection String | سلسلة اتصال مخزن البيانات الثنائية كبيرة الحجم لـ Azure.‬
    Dynamics Crm Linked Service_password | كلمة المرور الخاصة بحساب المستخدم الذي حددته كاسم المستخدم.
    FO Linked Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO Linked Service_properties_type Properties_tenant | حدد معلومات المستأجر (اسم المجال أو معرف المستأجر) الذي يوجد تطبيقك ضمنه.
    FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO Linked Service_properties_type Properties_service Principal Id | حدد معرف عميل التطبيق.
    Dynamics Crm Linked Service_properties_type Properties_username | اسم المستخدم الذي سيتصل بـ Dynamics.

    لمزيد من المعلومات، راجع [ترقية قالب إدارة الموارد يدويًا لكل بيئة](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)، و[خصائص الخدمة المرتبطة](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties)، و[نسخ البيانات باستخدام Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. بعد عملية النشر، تحقق من صحة مجموعات البيانات وتدفق البيانات والخدمة المرتبطة لمصنع البيانات.

   ![مجموعات البيانات وتدفق البيانات والخدمة المرتبطة](media/data-factory-validate.png)

11. انتقل إلى **إدارة**. ضمن **الاتصالات**، حدد **الخدمة المرتبطة**. حدد **DynamicsCrmLinkedService**. في النموذج **تحرير الخدمة المرتبطة (Dynamics CRM)**، أدخل القيم التالية:

    الحقل | قيمة
    ---|---
    الاسم | DynamicsCrmLinkedService
    الوصف | الخدمات المرتبطة للاتصال بمثيل CRM لإحضار بيانات الوحدات
    الاتصال عبر وقت تشغيل التكامل | AutoResolvelntegrationRuntime
    نوع النشر | عبر الإنترنت
    Uri الخاص بالخدمة | `https://<organization-name>.crm[x].dynamics.com`
    نوع المصادقة | Office365
    اسم المستخدم |
    كلمة المرور أو Azure Key Vault | كلمة المرور
    كلمة المرور |

## <a name="run-the-template"></a>تشغيل القالب

1. أوقف الكتابة المزدوجة في **الحساب** و **جهة  الاتصال** و **المورّد** باستخدام تطبيق Finance and Operations.

    + العملاء V3 (الحسابات)
    + العملاء V3 (جهات الاتصال)
    + جهات اتصال CDS‏ V2 (جهات الاتصال)
    + جهات اتصال CDS‏ V2 (جهات الاتصال)
    + المورّد V2 ‏(msdyn_vendor)

2. تأكد من إزالة الخرائط من الجدول `msdy_dualwriteruntimeconfig` في Dataverse.

3. ثبّت [حلول الكتابة المزدوجة للطرف ودفتر العناوين العمومي](https://aka.ms/dual-write-gab) من AppSource.

4. في تطبيق Finance and Operations، إذا كانت الجداول التالية تحتوي على بيانات، فشغّل **المزامنة الأولية** لها.

    + التحيات
    + أنواع الخصائص الشخصية
    + الختام الإطرائي
    + ألقاب جهات الاتصال
    + أدوار صنع القرار
    + مستويات الولاء

5. في تطبيق مشاركة العميل، قم بتعطيل خطوات المكون الإضافي التالية.

    + تحديث الحساب
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: تحديث حساب
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: تحديث حساب
    + تحديث جهة الاتصال
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث جهة اتصال
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: تحديث جهة اتصال
    + msdyn_party Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث msdyn_party
    + msdyn_vendor Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: تحديث msdyn_vendor

6. في تطبيق مشاركة العميل، قم بتعطيل عمليات سير العمل التالية.

    + إنشاء الموردين في جدول الحسابات
    + إنشاء الموردين في جدول الحسابات
    + إنشاء مورّدين من نوع الشخص في جدول جهات الاتصال
    + إنشاء الموردين من نوع الشخص في جدول الموردين
    + تحديث الموردين في جدول الحسابات
    + تحديث الموردين في جدول الموردين
    + تحديث الموردين من نوع الشخص في جدول جهات الاتصال
    + تحديث الموردين من نوع الشخص في جدول الموردين

7. في مصنع البيانات، قم بتشغيل القالب عن طريق تحديد **تشغيل الآن** كما هو موضح في الصورة التالية. قد تتطلب هذه العملية بضع ساعات لتكتمل بالاستناد إلى حجم البيانات.

    ![تشغيل المشغل](media/data-factory-trigger.png)

    > [!NOTE]
    > إذا كانت لديك تخصيصات لسجلات **الحساب** و **جهة الاتصال** و **المورّد**، فيجب تعديل القالب.

8. استورد سجلات **الطرف** الجديد في تطبيق Finance and Operations.

    + نزّل الملف `FONewParty.csv` من مخزن البيانات الثنائية كبيرة الحجم لـ Azure. المسار هو `partybootstrapping/output/FONewParty.csv`.
    + حوّل الملف `FONewParty.csv` إلى ملف Excel واستورد ملف Excel إلى تطبيق Finance and Operations.  إذا نجحت عملية استيراد csv، فيمكنك استيراد ملف csv مباشرة. قد يستغرق تشغيل عملية الاستيراد بضع ساعات، بحسب حجم البيانات. لمزيد من المعلومات راجع [نظرة عامة حول وظائف استيراد البيانات وتصديرها](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).

    ![استيراد سجلات طرف Datavers](media/data-factory-import-party.png)

9. في تطبيقات مشاركة العميل، قم بتمكين خطوات المكون الإضافي التالية:

    + تحديث الحساب
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: تحديث حساب
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: تحديث حساب
    + تحديث جهة الاتصال
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث جهة اتصال
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: تحديث جهة اتصال
    + msdyn_party Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث msdyn_party
    + msdyn_vendor Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: تحديث msdyn_vendor

10. في تطبيقات مشاركة العميل، قم بتنشيط عمليات سير العمل التالية إذا قمت بإلغاء تنشيطها في الخطوات السابقة:

    + إنشاء الموردين في جدول الحسابات
    + إنشاء الموردين في جدول الحسابات
    + إنشاء مورّدين من نوع الشخص في جدول جهات الاتصال
    + إنشاء الموردين من نوع الشخص في جدول الموردين
    + تحديث الموردين في جدول الحسابات
    + تحديث الموردين في جدول الموردين
    + تحديث الموردين من نوع الشخص في جدول جهات الاتصال
    + تحديث الموردين من نوع الشخص في جدول الموردين

11. شغّل الخرائط ذات الصلة **بالطرف** كما هو موضح في [الطرف ودفتر العناوين العمومي](party-gab.md).

## <a name="troubleshooting"></a>استكشاف الأخطاء وإصلاحها

1. في حالة فشل العملية، أعد تشغيل مصنع البيانات بدءًا من النشاط الفاشل.
2. يتم إنشاء بعض الملفات بواسطة مصنع البيانات الذي يمكنك استخدامه لغرض التحقق من صحة البيانات.
3. يتم تشغيل مصنع البيانات استنادًا إلى ملفات csv المفصولة بفواصل. إذا كانت هناك قيمة حقل تتضمن فاصلة، فقد تتداخل مع النتائج. تحتاج إلى إزالة الفواصل.
4. توفر علامة التبويب **المراقبة** معلومات حول كافة الخطوات والبيانات التي تمت معالجتها. حدد خطوة معينة لتصحيحها.

    ![علامة تبويب المراقبة](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>اعرف المزيد عن القالب

يمكنك العثور علي تعليقات على القالب في ملف [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
