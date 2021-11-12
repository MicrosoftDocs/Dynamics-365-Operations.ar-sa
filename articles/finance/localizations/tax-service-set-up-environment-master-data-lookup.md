---
title: إعداد بيئة للبحث عن البيانات الرئيسية
description: يوضح هذا الموضوع كيفية إعداد بيئتك لاستخدام وظيفة البحث عن البيانات الرئيسية لحساب الضريبة.
author: kai-cloud
ms.date: 10/26/2021
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
ms.openlocfilehash: 901f8bcb0220355866952b68e92bc2dd906bb430
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/27/2021
ms.locfileid: "7700393"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>إعداد بيئة للبحث عن البيانات الرئيسية

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إعداد بيئتك لاستخدام وظيفة البحث عن البيانات الرئيسية لحساب الضريبة.

1. إعداد تكامل Microsoft Power Platform في Microsoft Dynamics Lifecycle Services (LCS). لمزيد من المعلومات، راجع [تكامل Microsoft Power Platform - نظرة عامة على الوظائف الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). بعد الانتهاء من هذه الخطوة ، سيظهر اسم بيئة Microsoft Power Platform في قسم **التكامل Power Platform**.
2. انتقل إلى [مركز اداره Microsoft Power Platform](https://admin.powerplatform.microsoft.com/environments)، ثم حدد اسم البيئة. يتم توفير عنوان URL الخاص بالبيئة.
3. إعداد Dynamics 365 Finance وDataverse. لمزيد من المعلومات، راجع [الحصول على حل الكيان الافتراضي](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) و[المصادقة والتخويل](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. قم بإعداد الكيانات التالية: لمزيد من المعلومات، راجع [تمكين الكيانات الظاهرية Microsoft Dataverse](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

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

5. إعداد Regulatory configuration service (RCS). افتح مساحة عمل **إدارة الميزات**، ثم قم بتمكين الميزات التالية:

    - دعم مصادر بيانات Dataverse لإعداد التقارير الإلكترونية
    - دعم مصادر بيانات Dataverse لخدمة الضرائب
    - ميزات العولمة

6. سجل الدخول إلى RCS باستخدام حساب مسؤول مستأجر.
7. انتقل إلى **إعداد التقارير الإلكترونية** > **التطبيقات المتصلة**. 
8. حدد **جديد** لإضافة سجل، وأدخل معلومات الحقل التالية. 

    - في حقل **الاسم**، أدخل اسمًا.
    - في الحقل **النوع**، حدد **Dataverse**.
    - في حقل **التطبيق**، أدخل عنوان URL لـ Dataverse.
    - في الحقل **المستأجر**، أدخل المستأجر.
    - في الحقل **عنوان URL‏‎ مخصص**، أدخل عنوان URL لـ Dataverse URL وألحقه بواسطة "/api/data/v9.1".

9. حدد **التحقق من الاتصال**، ثم أنجز عملية الاتصال. 

    [![زر التحقق من الاتصال.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. انتقل إلى **إعداد التقارير الإلكترونية** > **تكوينات الضرائب**، واستورد تكوينات الضرائب من [تكوينات الضرائب](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![صفحة تكوينات الضرائب، شجرة نموذج بيانات الضرائب.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. انتقل إلى **تعيين نموذج المستند الخاضع للضريبة** أو **تعيين نموذج Dataverse** إذا كنت تستخدم تكوين Microsoft، وفي حقل **التطبيق المتصل**، حدد السجل الذي أنشأته في الخطوة 7.
12. قم بتعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم.**

    [![صفحة تعيين النموذج.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
