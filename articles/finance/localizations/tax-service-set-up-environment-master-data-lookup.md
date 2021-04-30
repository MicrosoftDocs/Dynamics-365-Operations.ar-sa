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
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="e4f8b-103">إعداد بيئة للبحث عن البيانات الرئيسية</span><span class="sxs-lookup"><span data-stu-id="e4f8b-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="e4f8b-104">يوضح هذا الموضوع كيفية إعداد بيئتك لاستخدام وظيفة البحث عن البيانات الرئيسية لحساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="e4f8b-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="e4f8b-105">إعداد تكامل Power Platform في Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e4f8b-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="e4f8b-106">لمزيد من المعلومات، راجع [تكامل Microsoft Power Platform - نظرة عامة على الوظائف الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e4f8b-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="e4f8b-107">إعداد Dynamics 365 Finance وMicrosoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e4f8b-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="e4f8b-108">لمزيد من المعلومات، راجع [الحصول على الحل](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) و[المصادقة والتخويل](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="e4f8b-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="e4f8b-109">استورد *حل الكيان الافتراضي لخدمة الضريبة للمتطلبات الأساسية* من [الكيان الافتراضي لخدمة الضريبة](https://go.microsoft.com/fwlink/?linkid=2158160).</span><span class="sxs-lookup"><span data-stu-id="e4f8b-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="e4f8b-110">قم بإعداد Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="e4f8b-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="e4f8b-111">أنشئ طلب خدمة من Microsoft لتمكين إصدار تقييم الميزات التالية:</span><span class="sxs-lookup"><span data-stu-id="e4f8b-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="e4f8b-112">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="e4f8b-112">ERCdsFeature</span></span>
      - <span data-ttu-id="e4f8b-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="e4f8b-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="e4f8b-114">في Finance، انتقل إلى مساحة عمل **إدارة الميزات**، ثم قم بتمكين الميزات التالية:</span><span class="sxs-lookup"><span data-stu-id="e4f8b-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="e4f8b-115">(إصدار أولي) دعم مصادر بيانات Dataverse لإعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e4f8b-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="e4f8b-116">(معاينة) دعم مصادر بيانات Dataverse لخدمة الضرائب</span><span class="sxs-lookup"><span data-stu-id="e4f8b-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="e4f8b-117">(معاينة) ميزات العولمة</span><span class="sxs-lookup"><span data-stu-id="e4f8b-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="e4f8b-118">سجل الدخول إلى RCS باستخدام حساب مسؤول مستأجر.</span><span class="sxs-lookup"><span data-stu-id="e4f8b-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="e4f8b-119">انتقل إلى **إعداد التقارير الإلكترونية** > **التطبيقات المتصلة**.</span><span class="sxs-lookup"><span data-stu-id="e4f8b-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="e4f8b-120">حدد **جديد** لإضافة سجل، وأدخل معلومات الحقل التالية.</span><span class="sxs-lookup"><span data-stu-id="e4f8b-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="e4f8b-121">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="e4f8b-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="e4f8b-122">في الحقل **النوع**، حدد **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="e4f8b-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="e4f8b-123">في حقل **التطبيق**، أدخل عنوان URL لـ Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e4f8b-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="e4f8b-124">في الحقل **المستأجر**، أدخل المستأجر.</span><span class="sxs-lookup"><span data-stu-id="e4f8b-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="e4f8b-125">في الحقل **عنوان URL‏‎ مخصص**، أدخل عنوان URL لـ Dataverse URL وألحقه بواسطة "/api/data/v9.1".</span><span class="sxs-lookup"><span data-stu-id="e4f8b-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="e4f8b-126">حدد **التحقق من الاتصال**، ثم أنجز عملية الاتصال.</span><span class="sxs-lookup"><span data-stu-id="e4f8b-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="e4f8b-127">[![زر التحقق من الاتصال](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="e4f8b-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="e4f8b-128">انتقل إلى **إعداد التقارير الإلكترونية** > **تكوينات الضرائب**، واستورد تكوينات الضرائب من [تكوينات الضرائب](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="e4f8b-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="e4f8b-129">[![صفحة تكوينات الضرائب، شجرة نموذج بيانات الضرائب](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="e4f8b-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="e4f8b-130">انتقل إلى **تعيين نموذج المستند الخاضع للضريبة** أو **تعيين نموذج Dataverse** إذا كنت تستخدم تكوين Microsoft، وفي حقل **التطبيق المتصل**، حدد السجل الذي أنشأته في الخطوة 7.</span><span class="sxs-lookup"><span data-stu-id="e4f8b-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="e4f8b-131">قم بتعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم.**</span><span class="sxs-lookup"><span data-stu-id="e4f8b-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="e4f8b-132">[![صفحة تعيين النموذج](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="e4f8b-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
