---
title: توسيع Talent باستخدام Power Apps وPower Automate
description: يصف هذا المقال بعض الأمثلة عن سيناريوهات قابلية التوسعة في Microsoft Dynamics 365 Human Resources التي تستخدم Microsoft Power Apps وMicrosoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b28480ff584870e931fdc288a2652a5649268576
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893067"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="f4595-103">توسيع باستخدام Power Apps وPower Automate</span><span class="sxs-lookup"><span data-stu-id="f4595-103">Extend with Power Apps and Power Automate</span></span>

<span data-ttu-id="f4595-104">يصف هذا المقال بعض الأمثلة عن سيناريوهات قابلية التوسعة في Microsoft Dynamics 365 Human Resources التي تستخدم Microsoft Power Apps وMicrosoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="f4595-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="f4595-105">يمكنك استيراد حزمة الحل المقترنة بكل مثال إلى بيئتك في Power Apps.</span><span class="sxs-lookup"><span data-stu-id="f4595-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="f4595-106">بعد ذلك، يمكنك استخدام الحزم كنقاط إرشادية أو كنقاط بداية لتنفيذ السيناريوهات التي تنطبق على مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="f4595-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4595-107">إذا أردت استخدام القوالب والتطبيقات التي تم وصفها في الموضوع "كما هي"، فتأكد من اختبارها للتأكد من أنها تغطي كافة السيناريوهات المتعلقة بعملية التنفيذ التي تقوم بها.</span><span class="sxs-lookup"><span data-stu-id="f4595-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f4595-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="f4595-108">Prerequisites</span></span>

- <span data-ttu-id="f4595-109">لاستيراد الحزم، يجب أن يتوفر إذن **أداة إنشاء البيئة** لدى المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="f4595-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="f4595-110">لتصدير التطبيقات أو استيرادها، يجب أن يتوفر لدى المستخدمين ترخيص Power Apps Plan 2 أو ترخيص إصدار تجريبي Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="f4595-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="f4595-111">التكامل مع Microsoft 365، Power Automate</span><span class="sxs-lookup"><span data-stu-id="f4595-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="f4595-112">يمكن استخدام تطبيق **التكامل مع Microsoft 365** لاستخراج معلومات الفريق للمستخدمين الذين سجلوا دخولهم من Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4595-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="f4595-113">ويشير إلى العاملين في الموارد البشرية لاستخراج أنواع ‏‫معرفات الموظفين.</span><span class="sxs-lookup"><span data-stu-id="f4595-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="f4595-114">يمكن للمديرين فحص تواريخ انتهاء صلاحية أنواع معرفات الموظفين.</span><span class="sxs-lookup"><span data-stu-id="f4595-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="f4595-115">كما يمكنهم إرسال تذكير بالبريد الكتروني إذا انتهت صلاحية نوع معرف الموظف.</span><span class="sxs-lookup"><span data-stu-id="f4595-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="f4595-116">يتكامل Power Automate مع Power Apps لإرسال هذا التذكير.</span><span class="sxs-lookup"><span data-stu-id="f4595-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="f4595-117">سيتم إعادة إرسال التأكيد إلى Power Apps من Power Automate وقت إرسال التذكير.</span><span class="sxs-lookup"><span data-stu-id="f4595-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="f4595-118">تتضمن أنواع التعريف رخصة القيادة وجواز السفر والنماذج الأخرى المقبولة للمعرف.</span><span class="sxs-lookup"><span data-stu-id="f4595-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="f4595-119">يمكنك توسيع هذا التطبيق لسيناريوهات أخرى.</span><span class="sxs-lookup"><span data-stu-id="f4595-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="f4595-120">على سبيل المثال، يمكن استخدامه لإظهار معلومات العطلة الخاصة بالفريق بالإضافة إلى أحداث التقويم وأي أحداث خاصة بالفريق.</span><span class="sxs-lookup"><span data-stu-id="f4595-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="f4595-121">لتنزيل تطبيق **التكامل مع Microsoft 365، Power Automate**، انتقل إلى [التكامل مع Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) على مركز التنزيل لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f4595-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="f4595-122">Power Automate – توصيل وتنفيذ SQL</span><span class="sxs-lookup"><span data-stu-id="f4595-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="f4595-123">يقوم القالب **Power Automate – توصيل وتنفيذ SQL‬** بالتوصيل بخادم Microsoft SQL Server ويتيح تشغيل استعلامات SQL.</span><span class="sxs-lookup"><span data-stu-id="f4595-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="f4595-124">على الرغم من أن هذا القالب يقرأ جداول SQL ويقوم بتحديثه، إلا أنه يمكنك توسيعه واستخدامه في السيناريوهات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f4595-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="f4595-125">على سبيل المثال، يمكن استخدامه لتعبئة جدول مرحلي في Common Data Service بواسطة سجلات من SQL Server، ولمزامنة الجدول المرحلي بشكل دوري باستخدام توزيع تزايدي من SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f4595-125">For example, you can use it to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="f4595-126">الاستعلام المتقدم متكامل مع التدفق لتمكين تحويل البيانات والدفع المتزايد.</span><span class="sxs-lookup"><span data-stu-id="f4595-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="f4595-127">لتنزيل القالب **Power Automate – توصيل وتنفيذ SQL**، انتقل إلى [Power Automate – توصيل وتنفيذ SQL](https://go.microsoft.com/fwlink/?linkid=2081789) على مركز تنزيل Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f4595-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4595-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f4595-128">Additional resources</span></span>

[<span data-ttu-id="f4595-129">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="f4595-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>