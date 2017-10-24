---
title: "العميل المتوقع إلى النقدية"
description: "يوفر الموضوع نظرة عامة حول العميل المتوقع إلى النقدية بين Dynamics 365 for Finance and Operations, Enterprise Edition وDynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="f2ece-103">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="f2ece-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f2ece-104">يستخدم حل العميل المتوقع إلى النقدية [تكامل البيانات](/common-data-service/entity-reference/dynamics-365-integration) لمزامنة البيانات عبر Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ومثيلات Dynamics 365 for Sales عبر Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="f2ece-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="f2ece-105">تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأومر المبيعات وفواتير المبيعات بين Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="f2ece-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="f2ece-106">بينما تتدفق البيانات بين Finance and Operations وSales، يمكنك تنفيذ أنشطة المبيعات والتسويق في Sales والتعامل مع تنفيذ الأوامر باستخدام إدارة المخزون في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2ece-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="f2ece-107">يوفر هذا الحل التكامل في النواحي التالية:</span><span class="sxs-lookup"><span data-stu-id="f2ece-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="f2ece-108">المحافظة على الحسابات في Sales ومزامنتها إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2ece-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="f2ece-109">المحافظة على جهات الاتصال في Sales ومزامنتها إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2ece-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="f2ece-110">المحافظة على المنتجات في Finance and Operations ومزامنتها إلى Sales‎.</span><span class="sxs-lookup"><span data-stu-id="f2ece-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="f2ece-111">إنشاء عروض أسعار المبيعات في Sales ومزامنتها إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f2ece-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="f2ece-112">إنشاء أوامر المبيعات في Finance and Operations ومزامنتها إلى Sales</span><span class="sxs-lookup"><span data-stu-id="f2ece-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="f2ece-113">إنشاء فواتير المبيعات في Finance and Operations ومزامنتها إلى Sales</span><span class="sxs-lookup"><span data-stu-id="f2ece-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="f2ece-114">متطلبات النظام لتطبيق Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="f2ece-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="f2ece-115">لاستخدام حل العميل المتوقع إلى النقدية، يجب تثبيت ما يلي:</span><span class="sxs-lookup"><span data-stu-id="f2ece-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="f2ece-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (يوليو 2017) مع تحديث النظام الأساسي 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="f2ece-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="f2ece-117">إصلاحين عاجلين لتطبيق Dynamics 365 for Finance and Operations, Enterprise Edition (July 2017).</span><span class="sxs-lookup"><span data-stu-id="f2ece-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="f2ece-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - يمكّن هذا الإصلاح العاجل مزامنة بنود أوامر المبيعات مع ميزة تكامل البيانات من Finance and Operations إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="f2ece-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="f2ece-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - يمكّن هذا الإصلاح العاجل مزامنة بنود أوامر المبيعات مع ميزة تكامل البيانات من Finance and Operations إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="f2ece-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="f2ece-120">**ملاحظة**: تحتاج فقط إلى تثبيت KB4036524 لأن التثبيت يتضمن التغييرات من KB4036461.</span><span class="sxs-lookup"><span data-stu-id="f2ece-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="f2ece-121">متطلبات النظام لتطبيق Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="f2ece-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="f2ece-122">لاستخدام حل العميل المتوقع إلى النقدية، يجب تثبيت ما يلي:</span><span class="sxs-lookup"><span data-stu-id="f2ece-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="f2ece-123">Dynamics 365 for Sales الإصدار 1612 (8.2.1.207) (DB 8.2.1.207) عبر الإنترنت أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="f2ece-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="f2ece-124">حل العميل المتوقع إلى النقدية لتطبيق Dynamics 365 for Sales، الإصدار 1.14.0.0 (v14) أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="f2ece-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f2ece-125">تثبيت حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="f2ece-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="f2ece-126">قم بتنزيل [الملف المضغوط لحزمة حل العميل المتوقع إلى النقدية لتطبيق Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="f2ece-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="f2ece-127">تأكد من أن الملف المضغوط غير محظور لكي لا تتلقى الرسالة "لم يتم العثور على حزم استيراد" عند تثبيت حزمة الحل.</span><span class="sxs-lookup"><span data-stu-id="f2ece-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="f2ece-128">لإلغاء حظر الملف، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="f2ece-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="f2ece-129">انقر بزر الماوس الأيمن فوق الملف المضغوط.</span><span class="sxs-lookup"><span data-stu-id="f2ece-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="f2ece-130">حدد **خصائص** ثم حدد **إلغاء الحظر**.</span><span class="sxs-lookup"><span data-stu-id="f2ece-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="f2ece-131">قم بإلغاء الضغط وتشغيل PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="f2ece-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="f2ece-132">قم بتثبيت حل العميل المتوقع إلى النقدية في مثيل Sales.</span><span class="sxs-lookup"><span data-stu-id="f2ece-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="f2ece-133">حدد نوع نشر **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="f2ece-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="f2ece-134">حدد **إظهار الخيارات المتقدمة**.</span><span class="sxs-lookup"><span data-stu-id="f2ece-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="f2ece-135">لإجراء تثبيت سريع، حدد **المنطقة**.</span><span class="sxs-lookup"><span data-stu-id="f2ece-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="f2ece-136">إذا حددت **لا أعرف**، فسيبحث النظام بالبحث عن كافة المناطق وبالتالي تستغرق عملية التثبيت وقتًا أطول.</span><span class="sxs-lookup"><span data-stu-id="f2ece-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="f2ece-137">أدخل **اسم المستخدم** و**كلمة المرور** لمستخدم مسؤول لديه حقوق المستخدم لإجراء عملية تثبيت.</span><span class="sxs-lookup"><span data-stu-id="f2ece-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

