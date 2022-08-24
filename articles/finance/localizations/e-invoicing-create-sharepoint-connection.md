---
title: تكوين اتصال SharePoint
description: توضح هذه المقالة كيفيه تكوين الاتصال بحيث يمكن للفوترة الإلكترونية الوصول إلى موقع SharePoint Microsoft.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: a2762178686d1f29c457b6de2a9b052fd048484b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283976"
---
# <a name="configure-a-sharepoint-connection"></a>تكوين اتصال SharePoint

[!include [banner](../includes/banner.md)]

يمكن لخدمه الفوترة الكترونيه قراءه ملفات من مجلدات Microsoft SharePoint وتحميل الملفات إلى SharePoint. لضمان امكانيه وصول الفوترة الكترونيه إلى موقع SharePoint محدد، يجب تقديم بيانات اعتماد الموقع إلى خدمه الفوترة الكترونيه. بالإضافة إلى ذلك، لضمان تخزين بيانات الاعتماد بشكل آمن، لا تزودها مباشرة. بدلاً من ذلك، قم بتخزينها في المخزن الرئيسي في Azure، وقم بتوفير سر المخزن الرئيسي في Azure.

## <a name="grant-access-to-a-sharepoint-folder"></a>منح الوصول إلى مجلد SharePoint

1. قم بإنشاء تسجيل تطبيق في المستأجر حيث تم تثبيت Regulatory Configuration Service (RCS).

    1. سجل الدخول إلى [مدخل Azure ](https://portal.azure.com/).
    2. انتقل إلى **عمليات تسجيل التطبيق**.
    3. حدد **تسجيل جديد**.
    4. ادخل اسمًا، مثل **تطبيق SharePoint للفوترة الإلكترونية**، وأكمل التسجيل
    5. حدد تسجيل التطبيق الجديد.
    6. في علامة التبويب **مصادقة**، قم بتكوين خيار **السماح بتدفقات العميل العامة**.
    4. في علامة التبويب **الشهادات والأسرار**، حدد **سر عميل جديد** لإنشاء سر عميل.
    5. انسخ قيمة السر الذي تم إنشاؤه.

    اتبع التوجيهات:

    - لا تستخدم تسجيل التطبيق نفسه لخدمات مختلفة.
    - اتبع [توصيات سياسة كلمة المرور](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - قم بإعداد تدوير كلمات المرور. أثناء الدوران، قم بإنشاء سر عميل جديد لتسجيل التطبيق، وقم بتحديث خزنة المفاتيح، ثم احذف السر القديم.

2. احفظ قيمتي **سر تسجيل التطبيق** و **معرف التطبيق (العميل)** كسرين جديدين في المخزن الرئيسي في إعداد بيئة الفوترة الإلكترونية.
3. أضف الأسرار التي قمت بإنشائها إلى معلمات المخزن الرئيسي في إعداد بيئة الفوترة الإلكترونية في RCS.
4. في مدخل Azure، امنح الوصول إلى SharePoint. يجب إكمال هذه الخطوة من قِبل مسؤول المستاجر.

    1. حدد تسجيل التطبيق الذي قمت بإنشائه.
    2. في علامة التبويب **أذونات API**، حدد **إضافة إذن**.
    3. حدد **رسم Microsoft (أذونات التطبيق)** \> **Sites.Selected**.
    4. حدد **منح موافقة المسؤول لـ \<user&nbsp;name\>**.
    5. راجع حقل **الحالة** للتأكد من منح الأذونات.

        ![الأذونات الممنوحة في علامة التبويب أذونات API.](media/configured-permissions.jpg)

    6. افتح [Graph Explorer - Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer)، وقم بتسجيل الدخول.
    7. في الجزء الأيسر، في علامة التبويب **عينة الاستعلامات**، ضمن **مواقع SharePoint**، حدد **الحصول على موقع SharePoint بناءً على المسار النسبي للموقع**.
    8. املأ معلمتي **\{host-name\}** و **\{server-relative-path\}**. على سبيل المثال، املأ `<domain>.sharepoint.com` لـ **\{host-name\}** و`sites/<siteName>` لـ **\{server-relative-path\}**.

        > [!NOTE]
        > بالنسبة لموقع الويب الافتراضي، اترك معلمة **\{server-relative-path\}** فارغة.

    9. حدد **تشغيل الاستعلام**، واحفظ النتيجة.
    10. قم بتكوين الاستعلام التالي.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        في هذا الاستعلام، **\{site-id\}** هو قيمة عقدة **المعرف** من استجابة الاستعلام السابق.

        فيما يلي نص الطلب الأساسي.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        في نص الطلب هذا، **\{app-id\}** هو قيمة **معرف التطبيق (العميل)**، و **\{app-name\}** هو قيمة **اسم التطبيق**.

        ![استعلام POST.](media/app-id-query.jpg)

    11. في علامة التبويب **تعديل الأذونات**، حدد **فتح لوحة الأذونات**، ثم حدد **المواقع** \> **Sites.FullControl.All** \> **الموافقة**.
    12. حدد **تشغيل الاستعلام**.

يمكن لخدمة الفواتير الإلكترونية الآن الوصول إلى موقع SharePoint الخاص بك.
