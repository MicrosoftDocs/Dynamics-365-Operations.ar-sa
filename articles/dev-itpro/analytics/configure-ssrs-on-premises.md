---
title: "تكوين خدمات SQL Server Reporting Services للنشر المحلي"
description: "يوفر هذا الموضوع معلومات حول تكوين SQL Server Reporting Services (SSRS) للنشر المحلي."
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: 2b5abc98f5788c5091e5be61688cfd0d4076a510
ms.contentlocale: ar-sa
ms.lasthandoff: 03/09/2018

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a><span data-ttu-id="c1095-103">تكوين خدمات SQL Server Reporting Services للنشر المحلي</span><span class="sxs-lookup"><span data-stu-id="c1095-103">Configure SQL Server Reporting Services for an on-premises deployment</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c1095-104">استخدم الخطوات الواردة في هذا الموضوع لتكوين SQL Server Reporting Services (SSRS) لعملية نشر Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (محلي).</span><span class="sxs-lookup"><span data-stu-id="c1095-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) deployment.</span></span>

1. <span data-ttu-id="c1095-105">افتح تطبيق إدارة تكوين خدمات التقارير.</span><span class="sxs-lookup"><span data-stu-id="c1095-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="c1095-106">اترك **اسم الخادم** الافتراضي، الذي يجب أن يكون اسم الجهاز الحالي، و**مثيل خادم التقارير**، **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="c1095-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span> 
3. <span data-ttu-id="c1095-107">انقر فوق **اتصال**.</span><span class="sxs-lookup"><span data-stu-id="c1095-107">Click **Connect**.</span></span>
   
   <span data-ttu-id="c1095-108">[![اتصال تكوين خدمات التقارير](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>
   
4. <span data-ttu-id="c1095-109">انقر فوق علامة التبويب **حساب الخدمة** وتأكد من تطابق الإعدادات مع الرسم التالي.</span><span class="sxs-lookup"><span data-stu-id="c1095-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c1095-110">[![علامة تبويب حساب الخدمة](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>
    
5. <span data-ttu-id="c1095-111">انقر فوق علامة التبويب **عنوان URL لخدمة الويب** وتأكد من تطابق الإعدادات مع الرسم التالي.</span><span class="sxs-lookup"><span data-stu-id="c1095-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span> 

    <span data-ttu-id="c1095-112">[![علامة تبويب عنوان URL لخدمة الويب](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span> 
    
6. <span data-ttu-id="c1095-113">انقر فوق علامة تبويب **قاعدة البيانات** وتأكد من تطابق **اسم قاعدة البيانات** و**إعدادات بيانات الاعتماد** مع الصورة التالية.</span><span class="sxs-lookup"><span data-stu-id="c1095-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span> <span data-ttu-id="c1095-114">**ملاحظة:** ستحتاج إلى إنشاء قاعدة بيانات جديدة.</span><span class="sxs-lookup"><span data-stu-id="c1095-114">**Note:** You will need to create a new database.</span></span> <span data-ttu-id="c1095-115">للقيام بذلك، انقر فوق **تغيير قاعدة البيانات**، ثم تحقق من أن اسم قاعدة البيانات الجديدة هو: **DynamicsAxReportServer‎**.</span><span class="sxs-lookup"><span data-stu-id="c1095-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="c1095-116">[![علامة تبويب قاعدة البيانات](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>
    
7. <span data-ttu-id="c1095-117">انقر فوق علامة التبويب **عنوان URL لمدخل الويب** وتأكد من تطابق الإعدادات مع الرسم التالي.</span><span class="sxs-lookup"><span data-stu-id="c1095-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span> <span data-ttu-id="c1095-118">**ملاحظة:** يجب عليك النقر فوق **تطبيق** لإنشاء وتكوين المدخل بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="c1095-118">**Note:** You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="c1095-119">[![علامة تبويب عنوان URL لمدخل الويب](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>
    
  <span data-ttu-id="c1095-120">بعد تكوين المدخل، سوف تتطابق علامة تبويب **مدخل الويب** مع الرسم التالي.</span><span class="sxs-lookup"><span data-stu-id="c1095-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>
    <span data-ttu-id="c1095-121">[![علامة تبويب مدخل الويب](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>
    
8. <span data-ttu-id="c1095-122">انقر فوق عنوان URL للتقارير لعرض مدخل ويب لخدمات SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="c1095-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span> 
9.  <span data-ttu-id="c1095-123">عندما تصبح في المدخل، أدخل مجلدًا جديدًا باسم **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="c1095-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="c1095-124">[![مجلد dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>
    
10. <span data-ttu-id="c1095-125">في **إدارة تكوين خدمات التقارير**، انقر فوق علامة تبويب **إعدادات البريد الإلكتروني** وتأكد من تطابق الإعدادات مع الرسم التالي.‬</span><span class="sxs-lookup"><span data-stu-id="c1095-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c1095-126">[![علامة تبويب إعدادات البريد الإلكتروني](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>
    
11. <span data-ttu-id="c1095-127">انقر فوق علامة التبويب **حساب التنفيذ‬** وتأكد من تطابق الإعدادات مع الرسم التالي.</span><span class="sxs-lookup"><span data-stu-id="c1095-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c1095-128">[![علامة تبويب حساب التنفيذ‬](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>
    
  <span data-ttu-id="c1095-129">لا تغيّر الإعدادات الافتراضية في علامة تبويب **مفاتيح التشفير**. [![علامة تبويب مفاتيح التشفير](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-129">Don’t change the default settings on the **Encryption Keys** tab. [![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>
    
12. <span data-ttu-id="c1095-130">انقر فوق علامة التبويب **إعدادات الاشتراك‬** وتأكد من تطابق الإعدادات مع الرسم التالي.</span><span class="sxs-lookup"><span data-stu-id="c1095-130">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c1095-131">[![علامة تبويب إعدادات الاشتراك](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-131">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>
    
  <span data-ttu-id="c1095-132">لا تغيّر الإعدادات الافتراضية في علامة تبويب **عمليات نشر لتوسيع الاستخدام**. [![علامة تبويب عمليات نشر لتوسيع الاستخدام](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-132">Don’t change the default settings on the **Scale-out Deployment** tab. [![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>
    
  <span data-ttu-id="c1095-133">لا تغيّر الإعدادات الافتراضية في علامة تبويب **تكامل Power BI**. [![علامة تبويب تكامل Power BI](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-133">Don’t change the default settings on the **Power BI Integration** tab. [![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span> 
    
13. <span data-ttu-id="c1095-134">انقر فوق **إنهاء** لإغلاق **إدارة تكوين خدمات التقارير**.</span><span class="sxs-lookup"><span data-stu-id="c1095-134">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="c1095-135">[![إغلاق إدارة تكوين خدمات التقارير](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="c1095-135">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
    


