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
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="fa29d-103">إعداد بيئة للبحث عن البيانات الرئيسية</span><span class="sxs-lookup"><span data-stu-id="fa29d-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa29d-104">يوضح هذا الموضوع كيفية إعداد بيئتك لاستخدام وظيفة البحث عن البيانات الرئيسية لحساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="fa29d-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="fa29d-105">إعداد تكامل Power Platform في Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fa29d-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="fa29d-106">لمزيد من المعلومات، راجع [تكامل Microsoft Power Platform - نظرة عامة على الوظائف الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fa29d-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="fa29d-107">إعداد Dynamics 365 Finance وMicrosoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fa29d-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="fa29d-108">لمزيد من المعلومات، راجع [الحصول على الحل](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) و[المصادقة والتخويل](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="fa29d-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="fa29d-109">قم بإعداد الكيانات التالية:</span><span class="sxs-lookup"><span data-stu-id="fa29d-109">Set up the following entities.</span></span> <span data-ttu-id="fa29d-110">لمزيد من المعلومات، راجع [تمكين الكيانات الظاهرية](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="fa29d-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="fa29d-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="fa29d-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="fa29d-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="fa29d-112">CurrencyEntity</span></span>
      - <span data-ttu-id="fa29d-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="fa29d-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="fa29d-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="fa29d-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="fa29d-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="fa29d-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="fa29d-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="fa29d-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="fa29d-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="fa29d-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="fa29d-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="fa29d-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="fa29d-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="fa29d-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="fa29d-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="fa29d-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="fa29d-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="fa29d-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="fa29d-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="fa29d-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="fa29d-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="fa29d-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="fa29d-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="fa29d-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="fa29d-125">قم بإعداد Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="fa29d-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="fa29d-126">أنشئ طلب خدمة من Microsoft لتمكين إصدار تقييم الميزات التالية:</span><span class="sxs-lookup"><span data-stu-id="fa29d-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="fa29d-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="fa29d-127">ERCdsFeature</span></span>
      - <span data-ttu-id="fa29d-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="fa29d-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="fa29d-129">انتقل إلى مساحة عمل **إدارة الميزات**، ثم قم بتمكين الميزات التالية:</span><span class="sxs-lookup"><span data-stu-id="fa29d-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="fa29d-130">(إصدار أولي) دعم مصادر بيانات Dataverse لإعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fa29d-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="fa29d-131">(معاينة) دعم مصادر بيانات Dataverse لخدمة الضرائب</span><span class="sxs-lookup"><span data-stu-id="fa29d-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="fa29d-132">(معاينة) ميزات العولمة</span><span class="sxs-lookup"><span data-stu-id="fa29d-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="fa29d-133">سجل الدخول إلى RCS باستخدام حساب مسؤول مستأجر.</span><span class="sxs-lookup"><span data-stu-id="fa29d-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="fa29d-134">انتقل إلى **إعداد التقارير الإلكترونية** > **التطبيقات المتصلة**.</span><span class="sxs-lookup"><span data-stu-id="fa29d-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="fa29d-135">حدد **جديد** لإضافة سجل، وأدخل معلومات الحقل التالية.</span><span class="sxs-lookup"><span data-stu-id="fa29d-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="fa29d-136">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="fa29d-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="fa29d-137">في الحقل **النوع**، حدد **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="fa29d-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="fa29d-138">في حقل **التطبيق**، أدخل عنوان URL لـ Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fa29d-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="fa29d-139">في الحقل **المستأجر**، أدخل المستأجر.</span><span class="sxs-lookup"><span data-stu-id="fa29d-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="fa29d-140">في الحقل **عنوان URL‏‎ مخصص**، أدخل عنوان URL لـ Dataverse URL وألحقه بواسطة "/api/data/v9.1".</span><span class="sxs-lookup"><span data-stu-id="fa29d-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="fa29d-141">حدد **التحقق من الاتصال**، ثم أنجز عملية الاتصال.</span><span class="sxs-lookup"><span data-stu-id="fa29d-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="fa29d-142">[![زر التحقق من الاتصال](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="fa29d-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="fa29d-143">انتقل إلى **إعداد التقارير الإلكترونية** > **تكوينات الضرائب**، واستورد تكوينات الضرائب من [تكوينات الضرائب](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="fa29d-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="fa29d-144">[![صفحة تكوينات الضرائب، شجرة نموذج بيانات الضرائب](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="fa29d-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="fa29d-145">انتقل إلى **تعيين نموذج المستند الخاضع للضريبة** أو **تعيين نموذج Dataverse** إذا كنت تستخدم تكوين Microsoft، وفي حقل **التطبيق المتصل**، حدد السجل الذي أنشأته في الخطوة 7.</span><span class="sxs-lookup"><span data-stu-id="fa29d-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="fa29d-146">قم بتعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم.**</span><span class="sxs-lookup"><span data-stu-id="fa29d-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="fa29d-147">[![صفحة تعيين النموذج](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="fa29d-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
