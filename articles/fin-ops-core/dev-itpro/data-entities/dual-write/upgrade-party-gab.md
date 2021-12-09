---
title: الترقية إلى الطرف ونموذج دفتر العناوين العمومي
description: يصف هذا الموضوع كيفية ترقية بيانات الكتابة المزدوجة إلى الطرف ونموذج دفتر العناوين العمومي‬.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 7434c2ed486fe0546a746afdd2c4c4aacdcc3d5c
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817278"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>الترقية إلى نموذج الطرف ودفتر العناوين العمومي

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

تساعدك قوالب [Microsoft Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) على ترقية البيانات الحالية في الكتابة المزدوجة إلى الحفلة ونموذج دفتر العناوين العمومي‬: البيانات في الجداول **حساب** و **جهة الاتصال** و **مورّد**، والعناوين البريدية والإلكترونية.

يتم توفير قوالب Data Factory الثلاثة التالية. إنها تساعد في تسوية البيانات من تطبيقات Finance and Operations وتطبيقات customer engagement.

- **[قالب الطرف](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (ترقية البيانات للكتابة المزدوجة Party-GAB schema/arm_template.json)** – هذا القالب يساعد في ترقية بيانات **الطرف** و **جهة الاتصال** المقترنة ببيانات **الحساب** و **جهة الاتصال** و **المورّد‬**.
- **[قالب العنوان البريدي للطرف](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (ترقية البيانات للكتابة المزدوجة للطرف-مخطط دفتر العناوين العمومي/ترقية العنوان البريدي للطرف - GAB/arm_template.json)** – يساعد هذا القالب في ترقية العناوين البريدية المقترنة ببيانات **الحساب** و **جهة اتصال** و **المورّد‬**.
- **[قالب العنوان الإلكتروني للطرف](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (ترقية البيانات للكتابة المزدوجة للطرف-مخطط دفتر العناوين العمومي/ترقية العنوان البريدي للطرف - GAB/arm_template.json)** – يساعد هذا القالب في ترقية العناوين الإلكترونية المقترنة ببيانات **الحساب** و **جهة الاتصال** و **المورّد‬**.

في نهاية العملية، يتم إنشاء ملفات القيم المفصولة بفاصله (.csv) التالية.

| اسم الملف | الاستخدام |
|---|---|
| FONewParty.csv | يساعد هذا الملف في إنشاء سجلات **الطرف** داخل تطبيق Finance and Operations. |
| ImportFONewPostalAddressLocation.csv | يساعد هذا الملف في إنشاء سجلات **موقع العنوان البريدي** في تطبيق Finance and Operations. |
| ImportFONewPartyPostalAddress.csv | يساعد هذا الملف في إنشاء سجلات **العنوان البريدي للطرف** في تطبيق Finance and Operations. |
| ImportFONewPostalAddress.csv | يساعد هذا الملف في إنشاء سجلات **العنوان البريدي** في تطبيق Finance and Operations. |
| ImportFONewElectronicAddress.csv | يساعد هذا الملف في إنشاء سجلات **العنوان الإلكتروني** في تطبيق Finance and Operations. |

يشرح هذا الموضوع كيفية استخدام قوالب Data Factory وترقية البيانات الخاصة بك. إذا لم يكن لديك أية تخصيصات، فيمكنك استخدام القوالب كما هي. على الرغم من ذلك، إذا كانت لديك تخصيصات لبيانات **الحساب** و **جهة الاتصال** و **المورّد**، فيجب عليك تعديل القوالب كما هو موضح في هذا الموضوع.

> [!IMPORTANT]
> توجد إرشادات خاصة إذا كنت ستقوم بتشغيل العنوان البريدي للطرف والقوالب الخاصة بالعنوان الإلكتروني للطرف. يجب عليك تشغيل قالب الطرف أولاً، ثم قالب العنوان البريدي للطرف، ثم قالب العنوان الإلكتروني للطرف.

## <a name="prerequisites"></a>المتطلبات الأساسية

يجب استيفاء المتطلبات الأساسية التالية قبل الترقية إلى الطرف ونموذج دفتر العناوين العمومي:

+ يجب أن يكون لديك [اشتراك Azure](https://portal.azure.com/).
+ يجب أن يكون لديك حق الوصول إلى [القوالب](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ يجب أن تكون عميل موجود للكتابة المزدوجة.

## <a name="prepare-for-the-upgrade"></a>التحضير للترقية

تتطلب الترقية التحضير على النحو التالي:

+ **المزامنة الكاملة:** كل من بيئة Finance and operations وبيئة customer engagement في حالة المزامنة الكاملة للجداول **الحساب (العميل)** و **الجهة الاتصال** و **المورّد‬**.
+ **مفاتيح التكامل**: تستخدم جداول **الحساب (العميل)** و **جهة الاتصال** و **المورّد** في تطبيقات customer engagement مفاتيح التكامل الجاهزة. إذا قمت بتخصيص مفاتيح التكامل، فيجب تخصيص القالب.
+ **رقم الطرف:** سيكون لجميع سجلات **الحساب (العميل)** و **جهة الاتصال** و **المورّد** التي ستتم ترقيتها رقم طرف. سيتم تجاهل السجلات التي ليس لها رقم طرف. إذا كنت ترغب في ترقية تلك السجلات، فيمكنك إضافة رقم طرف إليها قبل بدء عملية الترقية.
+ **انقطاع العمل في النظام:** أثناء عملية الترقية، يجب عليك وضع بيئة Finance and operations وبيئة customer engagement في وضع عدم الاتصال.
+ **لقطة:** خذ لقطات لتطبيقات Finance and Operations وتطبيقات customer engagement. ثم يمكنك استخدام اللقطات لاسترجاع الحالة السابقة إذا احتجت لذلك.

## <a name="deployment"></a>النشر

1. نزّل القوالب من [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. سجل الدخول إلى [مدخل Azure ](https://portal.azure.com/).
3. أنشئ [مجموعة موارد](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. أنشئ [حساب تخزين](/azure/storage/common/storage-account-create?tabs=azure-portal) في مجموعة الموارد التي أنشأتها.
5. أنشئ [مصنع بيانات](/azure/data-factory/quickstart-create-data-factory-portal) في مجموعة الموارد أعلاه التي أنشأتها.
6. افتح مصنع البيانات، وحدد اللوحة **التأليف والمراقبة**.
7. على علامة التبويب **إدارة**، حدد **قالب ARM**.
8. حدد **استيراد قالب ARM** لاستيراد قالب **الطرف‏‎**.
9. استورد القالب إلى مصنع البيانات. أدخل القيم التالية في **تفاصيل المشروع** و **تفاصيل المثيل**.

    | الحقل | قيمة |
    |---|---|
    | الاشتراك | اشتراك Azure |
    | مجموعة الموارد | قدم المورد نفسه الذي يتم إنشاء حساب التخزين ضمنه. |
    | المنطقة | المنطقة |
    | اسم المصنع | اسم المصنع |
    | FO Linked Service_service Principal Key | مفتاح التطبيق |
    | Azure Blob Storage_connection String | سلسلة اتصال مخزن Azure Blob |
    | Dynamics Crm Linked Service_password | كلمة المرور الخاصة بحساب المستخدم الذي تحدده كاسم المستخدم |
    | FO Linked Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO Linked Service_properties_type Properties_tenant | معلومات (اسم المجال أو معرف المستأجر) حول المستأجر الذي يوجد تطبيقك ضمنه |
    | FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO Linked Service_properties_type Properties_service Principal Id | معرف عميل التطبيق |
    | Dynamics Crm Linked Service_properties_type Properties_username | اسم المستخدم الذي يستخدم للاتصال بـ Dynamics 365 |

    لمزيد من المعلومات، راجع الموضوعات التالية:

    - [ترقية قالب Resource Manager يدويًا لكل بيئة](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [خصائص الخدمة المرتبطة](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [نسخ البيانات باستخدام Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. بعد عملية النشر، تحقق من صحة مجموعات البيانات وتدفق البيانات والخدمة المرتبطة لمصنع البيانات.

    ![مجموعات البيانات وتدفق البيانات والخدمة المرتبطة.](media/data-factory-validate.png)

11. انتقل إلى **إدارة**. ضمن **الاتصالات**، حدد **الخدمة المرتبطة**. ثم حدد **DynamicsCrmLinkedService**. في مربع الحوار **تحرير الخدمة المرتبطة (Dynamics CRM)**، أدخل القيم التالية.

    | الحقل | قيمة |
    |---|---|
    | Name | DynamicsCrmLinkedService |
    | الوصف | الخدمات المرتبطة للاتصال بمثيل CRM لإحضار بيانات الوحدات |
    | الاتصال عبر وقت تشغيل التكامل | AutoResolvelntegrationRuntime |
    | نوع النشر | عبر الإنترنت |
    | Uri الخاص بالخدمة | `https://<organization-name>.crm[x].dynamics.com` |
    | نوع المصادقة | Office365 |
    | اسم المستخدم | |
    | كلمة المرور أو Azure Key Vault | كلمة المرور |
    | كلمة المرور | |

## <a name="prepare-to-run-the-data-factory-templates"></a>الإعداد لتشغيل قوالب Data Factory

يصف هذا القسم الإعداد المطلوب قبل تشغيل العنوان البريدي للطرف وقوالب Data Factory للعنوان الإلكتروني للطرف.

### <a name="setup-to-run-the-party-postal-address-template"></a>إعداد تشغيل قالب العنوان البريدي للطرف

1. قم بتسجيل الدخول إلى تطبيقات customer engagement، وانتقل إلى **الإعدادات** \> **إعدادات إضفاء طابع شخصي**. ثم، في علامة التبويب **عام**، قم بتكوين إعداد المنطقة الزمنية لحساب مسؤول النظام. يجب أن تكون المنطقة الزمنية بالتوقيت العالمي المتفق عليه (UTC) لتحديث تواريخ العناوين البريدية "صالح من" و "صالح حتى" من تطبيقات Finance and Operations.

    ![إعداد المنطقة الزمنية لحساب مسؤول النظام.](media/ADF-1.png)

2. في Data Factory، وفي علامة التبويب **إدارة**، ضمن **معلمات عمومية**، قم بإنشاء المعلمة العمومية التالية.

    | الرقم | Name | النوع | قيمة |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | سلسلة | تلحق هذه المعلمة رقمًا تسلسليًا بالعناوين البريدية التي تم إنشاؤها حديثًا كبادئة. تأكد من توفير سلسلة لا تتعارض مع العناوين البريدية في تطبيقات Finance and Operations وتطبيقات customer engagement. على سبيل المثال، استخدم **ADF-PAD-**. |

    ![تم إنشاء المعلمة العمومية PostalAddressIdPrefix في علامة التبويب إدارة.](media/ADF-2.png)

3. عند الانتهاء، حدد **نشر الكل**.

    ![الزر "نشر الكل".](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>إعداد تشغيل قالب العنوان الإلكتروني للطرف

1. في Data Factory، وفي علامة التبويب **إدارة**، ضمن **معلمات عمومية**، قم بإنشاء المعلمات العمومية التالية.

    | الرقم | Name | النوع | قيمة |
    |---|---|---|---|
    | 1 | IsFOSource | قيمة منطقية | تحدد هذه المعلمة عناوين النظام الأساسية التي يتم استبدالها بحدث التعارضات. إذا كانت القيمة **صحيح**، ستقوم العناوين الرئيسية في تطبيقات Finance and Operations باستبدال العناوين الرئيسية في تطبيقات customer engagement. إذا كانت القيمة **خطأ**، ستقوم العناوين الرئيسية في تطبيقات customer engagement باستبدال العناوين الرئيسية في تطبيقات Finance and Operations. |
    | 2 | ElectronicAddressIdPrefix | سلسلة | تلحق هذه المعلمة رقمًا تسلسليًا بالعناوين الإلكترونية التي تم إنشاؤها حديثًا كبادئة. تأكد من توفير سلسلة لا تتعارض مع العناوين الإلكترونية في تطبيقات Finance and Operations وتطبيقات customer engagement. على سبيل المثال، استخدم **ADF-EAD-**. |

    ![تم إنشاء المعلمتين العموميتين IsFOSource وElectronicAddressIdPrefix في علامة التبويب إدارة.](media/ADF-4.png)

2. عند الانتهاء، حدد **نشر الكل**.

## <a name="run-the-templates"></a>تشغيل القوالب

1. أوقف الخرائط ثنائية الكتابة في **الحساب** و **جهة الاتصال** و **المورّد** التي تستخدم تطبيق Finance and Operations:

    + العملاء V3 (الحسابات)
    + العملاء V3 (جهات الاتصال)
    + جهات اتصال CDS‏ V2 (جهات الاتصال)
    + جهات اتصال CDS‏ V2 (جهات الاتصال)
    + المورّد V2 ‏(msdyn_vendor)

2. تأكد من إزالة الخرائط من الجدول **msdy_dualwriteruntimeconfig** في Dataverse.
3. ثبّت [حلول الكتابة المزدوجة للطرف ودفتر العناوين العمومي](https://aka.ms/dual-write-gab) من AppSource.
4. في تطبيق Finance and Operations، قم بتشغيل **المزامنة الأولية** للجداول التالية إذا كانت تحتوي على بيانات:

    + التحيات
    + أنواع الخصائص الشخصية
    + الختام الإطرائي
    + ألقاب جهات الاتصال
    + أدوار صنع القرار
    + مستويات الولاء

5. في تطبيق customer engagement، قم بتعطيل خطوات المكون الإضافي التالية:

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

    + Customeraddress

        + إنشاء

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: إنشاء customeraddress

        + تحديث

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: تحديث customeraddress

        + حذف

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: حذف customeraddress

    + msdyn_partypostaladdress

        + إنشاء

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: إنشاء msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: إنشاء msdyn_partypostaladdress

        + تحديث

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: تحديث msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: تحديث msdyn_partypostaladdress

    + msdyn_postaladdress

        + إنشاء

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: إنشاء msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: إنشاء msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: إنشاء msdyn_postaladdress

        + تحديث

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: تحديث msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: تحديث msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + إنشاء

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: إنشاء msdyn_partyelectronicaddress

        + تحديث

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: تحديث msdyn_partyelectronicaddress

        + حذف

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: تحديث msdyn_partyelectronicaddress

6. في تطبيق مشاركة العميل، قم بتعطيل عمليات سير العمل التالية.

    + إنشاء الموردين في جدول الحسابات
    + إنشاء الموردين في جدول الحسابات
    + إنشاء مورّدين من نوع الشخص في جدول جهات الاتصال
    + إنشاء الموردين من نوع الشخص في جدول الموردين
    + تحديث الموردين في جدول الحسابات
    + تحديث الموردين في جدول الموردين
    + تحديث الموردين من نوع الشخص في جدول جهات الاتصال
    + تحديث الموردين من نوع الشخص في جدول الموردين

7. في مصنع البيانات، قم بتشغيل القالب عن طريق تحديد **تشغيل الآن** كما هو موضح في الرسم التوضيحي التالي. قد تتطلب هذه العملية بضع ساعات لتكتمل، وفقًا لحجم البيانات.

    ![تشغيل القالب.](media/data-factory-trigger.png)

    > [!NOTE]
    > إذا كانت لديك تخصيصات لسجلات **الحساب** و **جهة الاتصال** و **المورّد**، فإنه يجب تعديل القالب.

8. قم باستيراد سجلات **الطرف** الجديدة في تطبيق Finance and Operations.

    1. نزّل الملف **FONewParty.csv** من محزن البيانات ثنائية الحجم لـ Azure. المسار هو **partybootstrapping/output/FONewParty.csv**.
    2. حوّل الملف **FONewParty.csv** إلى ملف Excel واستورد ملف Excel إلى تطبيق Finance and Operations. بدلاً من ذلك، إذا نجحت عملية استيراد CSV، فإنه يمكنك استيراد ملف csv مباشرةً. قد تتطلب هذه الخطوة بضع ساعات لتكتمل، وفقًا لحجم البيانات. لمزيد من المعلومات راجع [نظرة عامة حول وظائف استيراد البيانات وتصديرها](../data-import-export-job.md).

    ![استيراد سجلات طرف Dataverse.](media/data-factory-import-party.png)

9. في مصنع البيانات، قم بتشغيل قوالب العنوان البريدي للطرف والعنوان الإلكتروني للطرف، واحدًا تلو الآخر.

    + يعمل قالب العنوان البريدي للطرف على إدخال جميع سجلات العنوان البريدي في تطبيق customer engagement، ويعمل على إقرانها بسجلات **الحساب** و **جهة الاتصال** و **المورّد‬** المقابلة. كما إنه يعمل على إنشاء ملفات .csv: ImportFONewPostalAddressLocation.csv وImportFONewPartyPostalAddress.csv وImportFONewPostalAddress.csv.
    + يعمل قالب العنوان الإلكتروني للطرف على إدخال جميع العناوين الإلكترونية في تطبيق customer engagement، ويعمل على إقرانها بسجلات **الحساب** و **جهة الاتصال** و **المورّد‬** المقابلة. كما يعمل أيضًا على إنشاء ملف .csv واحد: ImportFONewElectronicAddress.csv.

    ![تشغيل العنوان البريدي للطرف وقوالب العنوان الإلكترونية للطرف.](media/ADF-7.png)

10. لتحديث تطبيق Finance and Operations بهذه البيانات، فإنه يجب عليك تحويل ملفات .csv إلى مصنف Excel [واستيراده في التطبيق Finance and Operations](/data-entities/data-import-export-job). بدلاً من ذلك، إذا نجحت عملية استيراد CSV، فإنه يمكنك استيراد ملفات csv مباشرةً. قد تتطلب هذه الخطوة بضع ساعات لتكتمل، وفقًا للحجم.

    ![استيراد ناجح.](media/ADF-8.png)

11. في تطبيق customer engagement، قم بتمكين خطوات المكون الإضافي التالية:

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

    + msdyn_partypostaladdress

        + إنشاء

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: إنشاء msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: إنشاء msdyn_partypostaladdress

        + تحديث

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: تحديث msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: تحديث msdyn_partypostaladdress

    + msdyn_postaladdress

        + إنشاء

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: إنشاء msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: إنشاء msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: إنشاء msdyn_postaladdress

        + تحديث

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: تحديث msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: تحديث msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + إنشاء

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: إنشاء msdyn_partyelectronicaddress

        + تحديث

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: تحديث msdyn_partyelectronicaddress

        + حذف

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: تحديث msdyn_partyelectronicaddress

12. في تطبيق customer engagement، قم بتنشيط عمليات سير العمل التالية إذا قمت بإلغاء تنشيطها مسبقًا:

    + إنشاء الموردين في جدول الحسابات
    + إنشاء الموردين في جدول الحسابات
    + إنشاء مورّدين من نوع الشخص في جدول جهات الاتصال
    + إنشاء الموردين من نوع الشخص في جدول الموردين
    + تحديث الموردين في جدول الحسابات
    + تحديث الموردين في جدول الموردين
    + تحديث الموردين من نوع الشخص في جدول جهات الاتصال
    + تحديث الموردين من نوع الشخص في جدول الموردين

13. شغّل الخرائط ذات الصلة **بالطرف** كما هو موضح في [الطرف ودفتر العناوين العمومي](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>توضيح قوالب Data Factory

يأخذك هذا القسم في الخطوات الواردة في كل قالب Data Factory.

### <a name="steps-in-the-party-template"></a>الخطوات الموجودة في قالب الطرف

1. تقوم الخطوات من 1 إلى 6 بتعريف الشركات التي يتم تمكينها للكتابة المزدوجة وعبارة عامل التصفية لها.
2. تقوم الخطوات 7-1 خلال 7-9 باسترداد البيانات من التطبيق Finance and Operations وتطبيق customer engagement، وتقوم بتجهيز تلك البيانات للترقية.
3. وتقوم الخطوات من 8 إلى 9 بمقارنة رقم الطرف لسجلات **الحساب** و **جهة الاتصال** و **المورّد‬** بين التطبيق Finance and Operations والتطبيق customer engagement. سيتم تخطي أية سجلات ليس لها رقم طرف.
4. تقوم الخطوة 10 بإنشاء ملفين .csv بالنسبة لسجلات الأطراف التي يجب إنشاؤها في تطبيق customer engagement وتطبيق Finance and Operations.

    - **FOCDSParty.csv** – يحتوي هذا الملف على جميع سجلات الطرف لكلا النظامين، بغض النظر عن تمكين الشركة للكتابة الثنائية.
    - **FONewParty.csv** – يحتوي هذا الملف على مجموعة فرعية من سجلات الطرف التي يكون Dataverse على دراية بها (على سبيل المثال، حسابات نوع **عميل متوقع**).

5. تعمل الخطوة 11 على إنشاء الأطراف في تطبيق customer engagement.
6. تقوم الخطوة 12 باسترداد المعرفات الفريدة العمومية (GUID) الخاصة بالأطراف من التطبيق customer engagement ومراحلها حتى يمكن إقرانها بالسجلات **الحساب** و **جهات الاتصال** و **المورّد‬** في الخطوات التالية.
7. الخطوة 13 لربط السجلات **الحساب** و **جهات الاتصال** و **المورّد‬** بالمعرفات الفريدة العمومية (GUID) الخاصة بالأطراف.
8. تعمل الخطوات من 14-1 إلى 14-3 على تحديث السجلات **الحساب** و **جهات الاتصال** و **المورّد‬** في تطبيق customer engagement بالمعرفات الفريدة العمومية (GUID) الخاصة بالأطراف.
9. تعمل الخطوات 15-1 إلى 15-3 على إعداد سجلات **جهة اتصال للطرف** للسجلات **الحساب** و **جهة الاتصال‬** و **المورّد**.
10. تعمل الخطوات 16-1 إلى 16-7 على استرداد البيانات المرجعية مثل التحيات وأنواع الأحرف الشخصية، وإقرانها بسجلات **جهة اتصال للطرف**.
11. تعمل الخطوة 17 على دمج سجلات **جهة اتصال للطرف** للسجلات **الحساب** و **جهة الاتصال‬** و **المورّد**.
12. تعمل الخطوة 18 على استيراد سجلات **جهة الاتصال** إلى تطبيق customer engagement.

### <a name="steps-in-the-party-postal-address-template"></a>الخطوات في قالب العنوان البريدي للطرف

1. تقوم الخطوات 1-1 خلال 1-10 باسترداد البيانات من التطبيق Finance and Operations وتطبيق customer engagement، وتقوم بتجهيز تلك البيانات للترقية.
2. تعمل الخطوة 2 على عدم توحيد بيانات العنوان البريدي في التطبيق Finance and Operations بالانضمام إلى العنوان البريدي والعنوان البريدي للطرف.
3. تعمل الخطوة 3 على عدم تكرار بيانات الحساب وجهة الاتصال والمورد ودمجها من تطبيق customer engagement.
4. تقوم الخطوة 4 بإنشاء ملفات .csv للتطبيق Finance and Operations لإنشاء بيانات العنوان الجديدة التي تستند إلى عناوين الحساب وجهات الاتصال والمورد.
5. تقوم الخطوة 5-1 بإنشاء ملفات .csv لتطبيق customer engagement لإنشاء كافة بيانات العناوين، استنادًا إلى التطبيق Finance and Operations وتطبيق customer engagement.
6. تعمل الخطوة 5-2 على تحويل ملفات .csv بتنسيق استيراد Finance and Operations للاستيراد اليدوي.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. تعمل الخطوة 6 على استيراد بيانات مجموعة العنوان البريدي إلى تطبيق customer engagement.
8. تعمل الخطوة 7 على استيراد بيانات مجموعة العنوان البريدي من تطبيق customer engagement.
9. تقوم الخطوة 8 بإنشاء بيانات عنوان العميل وربط مُعرف مجموعة العنوان البريدي.
10. تعمل الخطوات من 9-1 إلى 9-2 على إقران الطرف ومعرفات مجموعة العنوان البريدي بعناوين بريدية وعناوين بريدية للطرف.
11. تعمل الخطوات من 10-1 إلى 10-3 على استيراد عناوين العملاء والعناوين البريدية والعناوين البريدية للطرف إلى تطبيق customer engagement.

### <a name="steps-in-the-party-electronic-address-template"></a>الخطوات في قالب العنوان الإلكتروني للطرف

1. تقوم الخطوات 1-1 خلال 1-5 باسترداد البيانات من التطبيق Finance and Operations وتطبيق customer engagement، وتقوم بتجهيز تلك البيانات للترقية.
2. تعمل الخطوة 2 على دمج العناوين الإلكترونية في تطبيق customer engagement من كيانات الحساب وجهات الاتصال والمورد.
3. تعمل الخطوة 3 على دمج بيانات العنوان الإلكتروني الأساسيه من تطبيق customer engagement وتطبيق Finance and Operations.
4. تقوم الخطوة 4 بإنشاء ملفات .csv.

    - قم بإنشاء بيانات العنوان الإلكتروني للتطبيق Finance and Operations، استنادًا إلى عناوين الحساب وجهة الاتصال والمورد.
    - قم بإنشاء بيانات عنوان إلكتروني جديدة لتطبيق customer engagement، استنادًا إلى العنوان الإلكتروني وعناوين الحساب وجهات الاتصال والمورد في التطبيق Finance and Operations.

5. تعمل الخطوة 5-1 على استيراد العناوين الإلكترونية إلى تطبيق customer engagement.
6. تقوم الخطوة 5-2 على إنشاء ملفات .csv لتحديث العناوين الرئيسية للحسابات وجهات الاتصال في تطبيق customer engagement.
7. تعمل الخطوات 6-1 إلى 6-2 على استيراد الحسابات والعناوين الأساسية لجهات الاتصال بتطبيق customer engagement.

## <a name="troubleshooting"></a>استكشاف الأخطاء وإصلاحها

1. في حالة فشل العملية، قم بإعادة تشغيل مصنع البيانات. ابدأ من النشاط الفاشل.
2. يمكن استخدام بعض الملفات التي يتم إنشاؤها بواسطة مصنع البيانات بغرض التحقق من صحة البيانات.
3. يتم تشغيل مصنع البيانات استنادًا إلى ملفات csv. وبالتالي، إذا تم تضمين فاصلة في أي قيمة حقل، فقد تتداخل مع النتائج. يجب إزالة كافة الفواصل من قيم الحقول.
4. توفر علامة التبويب **المراقبة** معلومات حول كافة الخطوات والبيانات التي تمت معالجتها. حدد خطوة معينة لتصحيحها.

    ![علامة تبويب المراقبة.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>اعرف المزيد عن القالب

للحصول على معلومات إضافية حول القالب، راجع [التعليقات الخاصة بالأداة التمهيدية لقالب Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
