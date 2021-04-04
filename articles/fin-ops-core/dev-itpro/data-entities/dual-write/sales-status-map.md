---
title: إعداد التعيين أعمدة حالة أمر المبيعات
description: يوضح هذا الموضوع كيفية إعداد أعمدة حالات أمر المبيعات للكتابة المزدوجة.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: ecf26a2a697fa4d0485c1904041692a6c10ce9c3
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560399"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>إعداد التعيين أعمدة حالة أمر المبيعات

[!include [banner](../../includes/banner.md)]

تحتوي الأعمدة التي تشير إلى حالة أمر المبيعات على قيم تعداد مختلفة في Microsoft Dynamics 365 Supply Chain Management وDynamics 365 Sales. هناك حاجة إلى إعداد إضافي لتعيين هذه الأعمدة في الكتابة المزدوجة.

## <a name="columns-in-supply-chain-management"></a>الأعمدة في Supply Chain Management

في Supply Chain Management، يعكس العمودان حالة أمر المبيعات. العمودان اللذان يجب عليكما تعيينهما هما **الحالة** و **حالة المستند**.

يحدد تعداد **الحالة** الحالة الإجمالية  للأمر. تظهر هذه الحالة على رأس الأمر.

يتضمن تعداد **الحالة** القيم التالية:

- أمر مفتوح
- تم التسليم
- مفوتر
- تم الإلغاء

يحدد تعداد **حالة المستند** أحدث مستند تم إنشاؤه للأمر. على سبيل المثال، إذا تم تأكيد الأمر، فإن هذا المستند هو تأكيد أمر المبيعات. إذا تمت فوترة أمر المبيعات بشكل جزئي، ثم تم تأكيد البند المتبقي، تبقى حالة المستند **فاتورة**، بسبب إنشاء الفاتورة لاحقًا في العملية.

يتضمن تعداد **حالة المستند** القيم التالية:

- التأكيد
- قائمة الانتقاء
- كشف التعبئة
- الفاتورة

## <a name="columns-in-sales"></a>أعمده في المبيعات

في Sales، يشير العمودان إلى حالة الأمر. العمودان اللذان يجب عليكما تعيينهما هما **الحالة** و **حالة المعالجة‬**.

يحدد تعداد **الحالة** الحالة الإجمالية  للأمر. لديه القيم التالية:

- نشط
- ‏‫مُرسل
- تم الاستيفاء
- مفوتر
- تم الإلغاء

تم تقديم تعداد **حالة المعالجة** بحيث يمكن تعيين الحالة بدقة أكبر مع Supply Chain Management.

يعرض الجدول التالي تعيين **حالة المعالجة** في Supply Chain Management.

| حالة المعالجة   | الحالة في Supply Chain Management | حالة المستند في Supply Chain Management |
|---------------------|-----------------------------------|--------------------------------------------|
| نشط              | أمر مفتوح                        | لا شيء                                       |
| تاريخ التأكيد           | أمر مفتوح                        | التأكيد                               |
| منتقي              | أمر مفتوح                        | قائمة الانتقاء                               |
| تم تسليمه بشكل جزئي | أمر مفتوح                        | كشف التعبئة                               |
| تم التسليم           | تم التسليم                         | كشف التعبئة                               |
| مفوتر جزئيًا  | تم التسليم                         | الفاتورة                                    |
| مفوتر            | مفوتر                          | الفاتورة                                    |
| تم الإلغاء           | تم الإلغاء                         | غير قابل للتطبيق                             |

يعرض الجدول التالي تعيين **حالة المعالجة** بين Sales وSupply Chain Management.

| حالة المعالجة   | الحالة في Sales | الحالة في Supply Chain Management |
|---------------------|-----------------|-----------------------------------|
| نشط              | نشط          | أمر مفتوح                        |
| تاريخ التأكيد           | ‏‫مُرسل       | أمر مفتوح                        |
| منتقي              | ‏‫مُرسل       | أمر مفتوح                        |
| تم تسليمه بشكل جزئي | نشط          | أمر مفتوح                        |
| مفوتر جزئيًا  | نشط          | أمر مفتوح                        |
| مفوتر جزئيًا  | تم الاستيفاء       | تم التسليم                         |
| مفوتر            | مفوتر        | مفوتر                          |
| تم الإلغاء           | تم الإلغاء       | مُلغاة                         |

## <a name="setup"></a>الإعداد

لإعداد التعيين لأعمدة حالات أمر المبيعات، يجب تمكين السمتين **IsSOPIntegrationEnabled** و **isIntegrationUser**.

لتمكين السمة **IsSOPIntegrationEnabled**‎، اتبع الخطوات التالية:

1. في المستعرض، انتقل إلى `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. استبدل **\<test-name\>** بارتباط شركتك إلى Sales.
2. في الصفحة المفتوحة، ابحث عن **organizationid**، ودوّن القيمة.

    ![البحث عن organizationid](media/sales-map-orgid.png)

3. في Sales، افتح وحدة تحكم المستعرض، وقم بتشغيل البرنامج النصي التالي. استخدم القيمة **organizationid** من الخطوة 2.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![التعليمات البرمجية JavaScript في وحدة تحكم المستعرض](media/sales-map-script.png)

4. تأكد من تعيين **IsSOPIntegrationEnabled** إلى **صواب**. استخدم عنوان URL من الخطوة 1 للتدقيق في القيمة.

    ![تعيين IsSOPIntegrationEnabled إلى صواب.](media/sales-map-integration-enabled.png)

لتمكين السمة **isIntegrationUser‎**‎، اتبع الخطوات التالية:

1. في Sales، انتقل إلى **إعداد \> التخصيص \> تخصيص النظام**، حدد **جدول المستخدم**، ثم افتح  **النموذج \> المستخدم**.

    ![فتح نموذج المستخدم](media/sales-map-user.png)

2. في "مستكشف الحقول"، ابحث عن **وضع مستخدم التكامل**، ثم انقر نقرًا مزدوجًا فوقه لإضافته إلى النموذج. احفظ التغيير.

    ![إضافة عمود وضع مستخدم التكامل إلى النموذج](media/sales-map-field-explorer.png)

3. في Sales، انتقل إلى **الإعداد \> الأمان \> المستخدمون**، وقم بتغيير طريقة العرض من **المستخدمون الممكّنون** إلى **مستخدمو التطبيق**.

    ![تغيير طريقة العرض من "المستخدمون الممكّنون" إلى "مستخدمو التطبيق"](media/sales-map-enabled-users.png)

4. حدد الإدخالين لـ **DualWrite IntegrationUser**.

    ![قائمة مستخدمي التطبيق](media/sales-map-user-mode.png)

5. قم بتغيير قيمة عمود **وضع مستخدم التكامل** إلى **نعم**.

    ![تغيير قيمة عمود وضع مستخدم التكامل](media/sales-map-user-mode-yes.png)

أصبحت الآن أوامر مبيعاتك معيّنة.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]