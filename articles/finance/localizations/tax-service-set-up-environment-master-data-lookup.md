---
title: إعداد بيئة للبحث عن البيانات الرئيسية
description: يوضح هذا الموضوع كيفية إعداد بيئتك لاستخدام وظيفة البحث عن البيانات الرئيسية لحساب الضريبة.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e4aa941c57e8c31793d6db8ae87140cd1bb1a82b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021334"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>إعداد بيئة للبحث عن البيانات الرئيسية

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إعداد بيئتك لاستخدام وظيفة البحث عن البيانات الرئيسية لحساب الضريبة.

1. إعداد تكامل Power Platform في Lifecycle Services (LCS). لمزيد من المعلومات، راجع [تكامل Microsoft Power Platform - نظرة عامة على الوظائف الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. إعداد Dynamics 365 Finance وMicrosoft Dataverse. لمزيد من المعلومات، راجع [الحصول على الحل](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) و[المصادقة والتخويل](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. قم بإعداد الكيانات التالية: لمزيد من المعلومات، راجع [تمكين الكيانات الظاهرية](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).
      - CompanyInfoEntity
      - CurrencyEntity
      - CustCustomerV3Entity
      - DeliveryTermsEntity
      - EcoResProductCategoryEntity
      - EcoResReleasedProductV2Entity
      - LogisticsAddressCityEntity
      - LogisticsAddressCountryRegionTranslationEntity
      - LogisticsAddressStateEntity
      - PurchProcurementChargeCDSEntity
      - SalesChargeCDSEntity
      - TaxGroupEntity
      - TaxItemGroupHeadingEntity
      - VendVendorV2Entity
4. قم بإعداد Dynamics 365 Regulatory Configuration Service (RCS). 
5. أنشئ طلب خدمة من Microsoft لتمكين إصدار تقييم الميزات التالية:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. انتقل إلى مساحة عمل **إدارة الميزات**، ثم قم بتمكين الميزات التالية:

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
