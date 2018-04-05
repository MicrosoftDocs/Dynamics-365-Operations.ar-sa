---
title: "العميل المتوقع إلى النقدية"
description: "يوفر هذاالموضوع نظرة عامة حول العميل المتوقع إلى النقدية بين Microsoft Dynamics 365 for Finance and Operations وMicrosoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 025be8b44726194e6fc219816c40d2a15a7349df
ms.contentlocale: ar-sa
ms.lasthandoff: 03/26/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="42d7f-103">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="42d7f-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="42d7f-104">يوفر العميل المتوقع إلى النقدية مزامنة مباشرة بين Dynamics 365 for Finance and Operations وDynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="42d7f-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="42d7f-105">تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="42d7f-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="42d7f-106">بينما تتدفق البيانات بين Finance and Operations وSales، يمكنك تنفيذ أنشطة المبيعات والتسويق في Sales والتعامل مع تنفيذ الأوامر باستخدام إدارة المخزون في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42d7f-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="42d7f-107">لمزيد من المعلومات حول العميل المتوقع لتكامل النقدية، شاهد هذا الفيديو القصير على YouTube:</span><span class="sxs-lookup"><span data-stu-id="42d7f-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

<span data-ttu-id="42d7f-108">في الإصدار الحالي، يوفر العميل المتوقع للنقدية الأنواع التالية من المزامنة المباشرة:</span><span class="sxs-lookup"><span data-stu-id="42d7f-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="42d7f-109">المحافظة على الحسابات في Sales ومزامنتها مباشرة من Sales إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42d7f-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="42d7f-110">المحافظة على المنتجات في Finance and Operations ومزامنتها مباشرةً إلى Sales</span><span class="sxs-lookup"><span data-stu-id="42d7f-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="42d7f-111">‬‏‫المحافظة على جهات الاتصال في Sales ومزامنتها مباشرةً إلى جهات الاتصال أو العملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="42d7f-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="42d7f-112">مزامنة عرض أسعار المبيعات‬ مباشرةً من Sales إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="42d7f-112">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="42d7f-113">مزامنة عروض أسعار المبيعات‬ بين Sales وFinance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="42d7f-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="42d7f-114">مزامنة فاتورة المبيعات‬ مباشرةً من Finance and Operations إلى Sales‎</span><span class="sxs-lookup"><span data-stu-id="42d7f-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="42d7f-115">متطلبات النظام لـ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="42d7f-115">System requirements for Finance and Operations</span></span>

<span data-ttu-id="42d7f-116">يتم دعم العميل المتوقع لتكامل النقدية في الإصدارات التالية:</span><span class="sxs-lookup"><span data-stu-id="42d7f-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="42d7f-117">Microsoft Dynamics 365 for Finance and Operations،‏ Enterprise edition 7.3 (ديسمبر 2017)</span><span class="sxs-lookup"><span data-stu-id="42d7f-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="42d7f-118">Dynamics 365 for Finance and Operations،‏ Enterprise edition (ديسمبر 2017) - إصدار التطبيق 7.3.11971.56116 مع تحديث النظام الأساسي 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="42d7f-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="42d7f-119">Dynamics 365 for Finance and Operations, Enterprise edition (يوليو 2017)</span><span class="sxs-lookup"><span data-stu-id="42d7f-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="42d7f-120">Dynamics 365 for Finance and Operations،‏ Enterprise Edition (يوليو 2017) - مع تحديث النظام الأساسي 8 (إصدار التطبيق 7.2.11792.56024 مع إصدار النظام الأساسي 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="42d7f-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="42d7f-121">الإصلاحات التالية مطلوبة:</span><span class="sxs-lookup"><span data-stu-id="42d7f-121">The following hotfixes are required:</span></span>

    - <span data-ttu-id="42d7f-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – يُمكّن هذا الإصلاح العاجل مزامنة أوامر المبيعات من Sales إلى Finance and Operations من خلال ميزة تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="42d7f-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="42d7f-123">كما يوفر العديد من التحسينات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="42d7f-123">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="42d7f-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – يُمكّن هذا الإصلاح العاجل مزامنة بنود أوامر المبيعات من Finance and Operations إلى Sales من خلال ميزة تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="42d7f-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="42d7f-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – يُمكّن هذا الإصلاح العاجل مزامنة أوامر المبيعات من Finance and Operations إلى Sales من خلال ميزة تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="42d7f-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="42d7f-126">تحتاج فقط إلى تثبيت KB4045570 لأن التثبيت يتضمن التغييرات من الإصلاحات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="42d7f-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="42d7f-127">Dynamics 365 for Finance and Operations إصدار 1611 (نوفمبر 2016)</span><span class="sxs-lookup"><span data-stu-id="42d7f-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="42d7f-128">Dynamics 365 for Finance and Operations، إصدار 1611 (نوفمبر 2016) مع تحديث النظام الأساسي 8 أو إصدار أحدث</span><span class="sxs-lookup"><span data-stu-id="42d7f-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="42d7f-129">الإصلاحات التالية مطلوبة:</span><span class="sxs-lookup"><span data-stu-id="42d7f-129">The following hotfixes are required:</span></span>

    - <span data-ttu-id="42d7f-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - تمكين مزامنة أوامر المبيعات باستخدام موحد البيانات من Finance and Operations لـ Sales</span><span class="sxs-lookup"><span data-stu-id="42d7f-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="42d7f-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - تمكين مزامنة عنوان أوامر التوريد باستخدام موحد البيانات من Finance and Operations لـ Sales</span><span class="sxs-lookup"><span data-stu-id="42d7f-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="42d7f-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - مطلوب دعم تكامل العميل المتوقع للنقدية من خلال كيانات بيانات.</span><span class="sxs-lookup"><span data-stu-id="42d7f-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="42d7f-133">بعد تثبيت الإصلاحات العاجلة، يجب عليك بدء تشغيل وظيفة الدُفعة التالية من نموذج **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="42d7f-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="42d7f-134">يتم إخفاء هذا النموذج لأنك لا تحتاج إليه إلا مرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="42d7f-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="42d7f-135">للوصول إلى النموذج، سجّل دخولك إلى البيئة وأضف التالي إلى URL في عنوان المستعرض: &mi=action:SalesPopulateProspectToCash, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="42d7f-135">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="42d7f-136">عند فتح النموذج، انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="42d7f-136">When the form opens, click OK.</span></span> <span data-ttu-id="42d7f-137">سوف يقوم هذا بتعبئة حقل **LineCreationSequnceNumber** في **SalesLine**، و **SalesQuotationLine**، وجداول **CustInvoiceTrans** بالقيم الفريدة، وسوف يتم تحديث قائمة المنتجات.</span><span class="sxs-lookup"><span data-stu-id="42d7f-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="42d7f-138">ويُعد هذا مطلوبًا للعميل المتوقع لتكامل النقدية للعمل.</span><span class="sxs-lookup"><span data-stu-id="42d7f-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="42d7f-139">متطلبات النظام لـ Sales</span><span class="sxs-lookup"><span data-stu-id="42d7f-139">System requirements for Sales</span></span>

<span data-ttu-id="42d7f-140">لاستخدام حل العميل المتوقع للنقدية، يجب تثبيت المكونات التالية:</span><span class="sxs-lookup"><span data-stu-id="42d7f-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="42d7f-141">Dynamics 365 for Sales الإصدار 1612 (8.2.1.207) (DB 8.2.1.207) عبر الإنترنت أو إصدار لاحق</span><span class="sxs-lookup"><span data-stu-id="42d7f-141">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="42d7f-142">حل العميل المتوقع للنقدية لتطبيق Dynamics 365 for Sales، الإصدار 1.15.0.0 (إصدار 15)</span><span class="sxs-lookup"><span data-stu-id="42d7f-142">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="42d7f-143">تثبيت حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="42d7f-143">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="42d7f-144">قم بتنزيل [الملف المضغوط لحزمة حل العميل المتوقع للنقدية لتطبيق Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) من CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="42d7f-144">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="42d7f-145">تأكد من أن الملف المضغوط غير محظور.</span><span class="sxs-lookup"><span data-stu-id="42d7f-145">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="42d7f-146">وبخلاف ذلك، عند محاولة تثبيت حزمة الحلول، قد تظهر لك رسالة الخطأ التالية، "لم يتم العثور على أي حزم استيراد".</span><span class="sxs-lookup"><span data-stu-id="42d7f-146">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="42d7f-147">لإلغاء حظر الملف المضغوط، انقر بزر الماوس فوقه، وحدد **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="42d7f-147">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="42d7f-148">حدد **إلغاء حظر**.</span><span class="sxs-lookup"><span data-stu-id="42d7f-148">Select **Unblock**.</span></span>
3. <span data-ttu-id="42d7f-149">قم بفك الضغط وتشغيل **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="42d7f-149">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="42d7f-150">قم بتثبيت حل العميل المتوقع للنقدية في مثيل Sales:</span><span class="sxs-lookup"><span data-stu-id="42d7f-150">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="42d7f-151">حدد **Office 365** كنوع نشر.</span><span class="sxs-lookup"><span data-stu-id="42d7f-151">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="42d7f-152">حدد **إظهار الخيارات المتقدمة**.</span><span class="sxs-lookup"><span data-stu-id="42d7f-152">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="42d7f-153">لإجراء تثبيت سريع، حدد منطقة.</span><span class="sxs-lookup"><span data-stu-id="42d7f-153">For a quick installation, select a region.</span></span> <span data-ttu-id="42d7f-154">إذا حددت **لا أعرف**، فسيبحث النظام عن جميع المناطقن وستستغرق عملية التثبيت وقتًا أطول.</span><span class="sxs-lookup"><span data-stu-id="42d7f-154">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="42d7f-155">أدخل اسم مستخدم وكلمة مرور مستخدم مسؤول لديه حقوق التثبيت.</span><span class="sxs-lookup"><span data-stu-id="42d7f-155">Enter the user name and password of an admin user who has installation rights.</span></span>



