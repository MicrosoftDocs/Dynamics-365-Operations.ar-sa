---
title: تكوين خدمات SQL Server Reporting Services لعمليات النشر المحلي
description: توفر هذه المقالة معلومات عن تكوين SQL Server Reporting Services‏ (SSRS‏) للنشر المحلي.
author: PeterRFriis
ms.date: 06/23/2017
ms.topic: article
ms.prod: dynamics-365
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.custom: 55651
ms.assetid: ''
ms.service: ''
ms.openlocfilehash: 9acb681ce07c3a7da82a630c7a87a4271a411b51
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275399"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>تكوين خدمات SQL Server Reporting Services لعمليات النشر المحلي

[!include [banner](../includes/banner.md)]

استخدم الخطوات الموجودة في هذا الموضوع لتكوين SQL Server Reporting Services‏ (SSRS) لنشر Microsoft Dynamics 365 Finance + Operations (on-premises) .

1. افتح تطبيق إدارة تكوين خدمات التقارير.
2. اترك **اسم الخادم** الافتراضي، الذي يجب أن يكون اسم الجهاز الحالي، و **مثيل خادم التقارير**، **MSSQLSERVER**.
3. انقر فوق **اتصال**.

    [![اتصال تكوين خدمات التقارير.](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. انقر فوق علامة التبويب **حساب الخدمة** وتأكد من تطابق الإعدادات مع الرسم التالي.

    [![علامة تبويب حساب الخدمة.](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. انقر فوق علامة التبويب **عنوان URL لخدمة الويب** وتأكد من تطابق الإعدادات مع الرسم التالي.

    [![علامة تبويب عنوان URL لخدمة الويب.](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. انقر فوق علامة تبويب **قاعدة البيانات** وتأكد من تطابق **اسم قاعدة البيانات** و **إعدادات بيانات الاعتماد** مع الصورة التالية.

    > [!NOTE]
    > ستحتاج إلى إنشاء قاعدة بيانات جديدة. للقيام بذلك، انقر فوق **تغيير قاعدة البيانات**، ثم تحقق من أن اسم قاعدة البيانات الجديدة هو: **DynamicsAxReportServer‎**.

    [![علامة تبويب قاعدة البيانات.](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. انقر فوق علامة التبويب **عنوان URL لمدخل الويب** وتأكد من تطابق الإعدادات مع الرسم التالي.

    > [!NOTE]
    > يجب عليك النقر فوق **تطبيق** لإنشاء وتكوين المدخل بشكل صحيح.

    [![علامة تبويب عنوان URL لمدخل الويب.](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    بعد تكوين المدخل، سوف تتطابق علامة تبويب **مدخل الويب** مع الرسم التالي.

    [![علامة تبويب مدخل الويب.](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. انقر فوق عنوان URL للتقارير لعرض مدخل ويب لخدمات SQL Server Reporting Services.
9. عندما تصبح في المدخل، أدخل مجلدًا جديدًا باسم **Dynamics**.

    [![مجلد dynamics.](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. في **إدارة تكوين خدمات التقارير**، انقر فوق علامة تبويب **إعدادات البريد الإلكتروني** وتأكد من تطابق الإعدادات مع الرسم التالي.‬

    [![علامة تبويب إعدادات البريد الإلكتروني.](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. انقر فوق علامة التبويب **حساب التنفيذ‬** وتأكد من تطابق الإعدادات مع الرسم التالي.

    [![علامة تبويب حساب التنفيذ‬.](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    لا تغيّر الإعدادات الافتراضية في علامة تبويب **مفاتيح التشفير**.

    [![علامة تبويب مفاتيح التشفير.](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. انقر فوق علامة التبويب **إعدادات الاشتراك‬** وتأكد من تطابق الإعدادات مع الرسم التالي.

    [![علامة تبويب إعدادات الاشتراك.](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    لا تغيّر الإعدادات الافتراضية في علامة تبويب **عمليات نشر لتوسيع الاستخدام**.

    [![علامة تبويب عمليات نشر لتوسيع الاستخدام.](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    لا تغيّر الإعدادات الافتراضية في علامة تبويب **تكامل Power BI**.

    [![علامة تبويب تكامل Power Bi.](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. انقر فوق **إنهاء** لإغلاق **إدارة تكوين خدمات التقارير**.

    [![إغلاق إدارة تكوين خدمات التقارير.](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
