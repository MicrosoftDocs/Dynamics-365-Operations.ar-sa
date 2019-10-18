---
title: تكوين خدمات SQL Server Reporting Services لعمليات النشر المحلي
description: يوفر هذا الموضوع معلومات حول تكوين SQL Server Reporting Services (SSRS) للنشر المحلي.
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: bb6e8a55c9bee4e60c3a627409d2fbe3b8915196
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174226"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>تكوين خدمات SQL Server Reporting Services لعمليات النشر المحلي

[!include [banner](../includes/banner.md)]

استخدم الخطوات في هذا الموضوع لتكوين SQL Server Reporting Services (SSRS) لعملية نشر Microsoft Dynamics 365 Finance + Operations (محلي).

1. افتح تطبيق إدارة تكوين خدمات التقارير.
2. اترك **اسم الخادم** الافتراضي، الذي يجب أن يكون اسم الجهاز الحالي، و**مثيل خادم التقارير**، **MSSQLSERVER**.
3. انقر فوق **اتصال**.

    [![اتصال تكوين خدمات التقارير](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. انقر فوق علامة التبويب **حساب الخدمة** وتأكد من تطابق الإعدادات مع الرسم التالي.

    [![علامة تبويب حساب الخدمة](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. انقر فوق علامة التبويب **عنوان URL لخدمة الويب** وتأكد من تطابق الإعدادات مع الرسم التالي.

    [![علامة تبويب عنوان URL لخدمة الويب](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. انقر فوق علامة تبويب **قاعدة البيانات** وتأكد من تطابق **اسم قاعدة البيانات** و**إعدادات بيانات الاعتماد** مع الصورة التالية.

    > [!NOTE]
    > ستحتاج إلى إنشاء قاعدة بيانات جديدة. للقيام بذلك، انقر فوق **تغيير قاعدة البيانات**، ثم تحقق من أن اسم قاعدة البيانات الجديدة هو: **DynamicsAxReportServer‎**.

    [![علامة تبويب قاعدة البيانات](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. انقر فوق علامة التبويب **عنوان URL لمدخل الويب** وتأكد من تطابق الإعدادات مع الرسم التالي.

    > [!NOTE]
    > يجب عليك النقر فوق **تطبيق** لإنشاء وتكوين المدخل بشكل صحيح.

    [![علامة تبويب عنوان URL لمدخل الويب](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    بعد تكوين المدخل، سوف تتطابق علامة تبويب **مدخل الويب** مع الرسم التالي.

    [![علامة تبويب مدخل الويب](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. انقر فوق عنوان URL للتقارير لعرض مدخل ويب لخدمات SQL Server Reporting Services.
9. عندما تصبح في المدخل، أدخل مجلدًا جديدًا باسم **Dynamics**.

    [![مجلد dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. في **إدارة تكوين خدمات التقارير**، انقر فوق علامة تبويب **إعدادات البريد الإلكتروني** وتأكد من تطابق الإعدادات مع الرسم التالي.‬

    [![علامة تبويب إعدادات البريد الإلكتروني](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. انقر فوق علامة التبويب **حساب التنفيذ‬** وتأكد من تطابق الإعدادات مع الرسم التالي.

    [![علامة تبويب حساب التنفيذ‬](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    لا تغيّر الإعدادات الافتراضية في علامة تبويب **مفاتيح التشفير**.

    [![علامة تبويب مفاتيح التشفير](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. انقر فوق علامة التبويب **إعدادات الاشتراك‬** وتأكد من تطابق الإعدادات مع الرسم التالي.

    [![علامة تبويب إعدادات الاشتراك](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    لا تغيّر الإعدادات الافتراضية في علامة تبويب **عمليات نشر لتوسيع الاستخدام**.

    [![علامة تبويب عمليات نشر لتوسيع الاستخدام](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    لا تغيّر الإعدادات الافتراضية في علامة تبويب **تكامل Power BI**.

    [![علامة تبويب تكامل Power Bi](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. انقر فوق **إنهاء** لإغلاق **إدارة تكوين خدمات التقارير**.

    [![إغلاق إدارة تكوين خدمات التقارير](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
