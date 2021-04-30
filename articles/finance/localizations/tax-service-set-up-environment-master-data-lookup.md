---
title: إعداد بيئة للبحث عن البيانات الرئيسية
description: يوضح هذا الموضوع كيفية إعداد بيئتك لاستخدام وظيفة البحث عن البيانات الرئيسية لحساب الضريبة.
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869040"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>إعداد بيئة للبحث عن البيانات الرئيسية

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

يوضح هذا الموضوع كيفية إعداد بيئتك لاستخدام وظيفة البحث عن البيانات الرئيسية لحساب الضريبة.

1. إعداد تكامل Power Platform في Lifecycle Services (LCS). لمزيد من المعلومات، راجع [تكامل Microsoft Power Platform - نظرة عامة على الوظائف الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. إعداد Dynamics 365 Finance وMicrosoft Dataverse. لمزيد من المعلومات، راجع [الحصول على الحل](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) و[المصادقة والتخويل](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. استورد *حل الكيان الافتراضي لخدمة الضريبة للمتطلبات الأساسية* من [الكيان الافتراضي لخدمة الضريبة](https://go.microsoft.com/fwlink/?linkid=2158160).
4. قم بإعداد Dynamics 365 Regulatory Configuration Service (RCS). 
5. أنشئ طلب خدمة من Microsoft لتمكين إصدار تقييم الميزات التالية:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. في Finance، انتقل إلى مساحة عمل **إدارة الميزات**، ثم قم بتمكين الميزات التالية:

      - (إصدار أولي) دعم مصادر بيانات Dataverse لإعداد التقارير الإلكترونية
      - (معاينة) دعم مصادر بيانات Dataverse لخدمة الضرائب
      - (معاينة) ميزات العولمة

5. سجل الدخول إلى RCS باستخدام حساب مسؤول مستأجر.
6. انتقل إلى **إعداد التقارير الإلكترونية** > **التطبيقات المتصلة**. 
7. حدد **جديد** لإضافة سجل، وأدخل معلومات الحقل التالية. 

   - في حقل **الاسم**، أدخل اسمًا.
   - في الحقل **النوع**، حدد **Dataverse**.
   - في حقل **التطبيق**، أدخل عنوان URL لـ Dataverse.
   - في الحقل **المستأجر**، أدخل المستأجر.
   - في الحقل **عنوان URL‏‎ مخصص**، أدخل عنوان URL لـ Dataverse URL وألحقه بواسطة "/api/data/v9.1".

8. حدد **التحقق من الاتصال**، ثم أنجز عملية الاتصال. 

   [![زر التحقق من الاتصال](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. انتقل إلى **إعداد التقارير الإلكترونية** > **تكوينات الضرائب**، واستورد تكوينات الضرائب من [تكوينات الضرائب](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![صفحة تكوينات الضرائب، شجرة نموذج بيانات الضرائب](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. انتقل إلى **تعيين نموذج المستند الخاضع للضريبة** أو **تعيين نموذج Dataverse** إذا كنت تستخدم تكوين Microsoft، وفي حقل **التطبيق المتصل**، حدد السجل الذي أنشأته في الخطوة 7.
11. قم بتعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم.**

   [![صفحة تعيين النموذج](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
