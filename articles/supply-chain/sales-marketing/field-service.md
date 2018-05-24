---
title: "التكامل مع Microsoft Dynamics 365 for Field Service"
description: "يوفر هذا الموضوع نظرة عامة على التكامل مع Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
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
ms.sourcegitcommit: 03a932652cdd93b2a5917d0fca72809d1648b678
ms.openlocfilehash: b1acf0b64914a3199fcf44f8377e32b26f0af99e
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="7ecf4-103">التكامل مع Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="7ecf4-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7ecf4-104">يعمل Microsoft Dynamics 365 for Field Service على تمكين مزامنة عمليات الأعمال بين Finance and Operations وMicrosoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="7ecf4-105">يتم تكوين سيناريوهات التكامل باستخدام قوالب مطور البيانات القابلة للتوسيع وCommon Data Service (CDS) لتمكين مزامنة عمليات الأعمال.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="7ecf4-106">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="7ecf4-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="7ecf4-107">تنصب المرحلة الأولى من التكامل بين Field Service وFinance and Operations على تمكين أوامر العمل والاتفاقيات في Field Service لفوترتها في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="7ecf4-108">يبدأ التدفق المدعوم في Field Service، حيث تتم مزامنة المعلومات من أوامر العمل لـ Finance and Operations كأوامر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="7ecf4-109">في Finance and Operations، تتم فوترة أوامر المبيعات لإنشاء مستندات الفواتير.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="7ecf4-110">بالإضافة إلى ذلك، تتم مزامنة المعلومات من فواتير اتفاقيات Field Service لـ Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="7ecf4-111">يقوم مطور بيانات Microsoft Dynamics 365 بمزامنة البيانات من خلال استخدام المشاريع القابلة للتخصيص.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="7ecf4-112">يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة حيث يمكن تعيين الحقول المخصصة والقياسية الإضافية، وكذلك الكيانات، لتعديل التكامل والوفاء بالمتطلبات المحددة.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="7ecf4-113">تعمل المرحلة الأولى من التكامل بين Field Service وFinance and Operations على تمكين مزامنة العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="7ecf4-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="7ecf4-114">المنتجات في Finance and Operations للمنتجات في Field Service التي تشمل معلومات نوع المنتج</span><span class="sxs-lookup"><span data-stu-id="7ecf4-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="7ecf4-115">أوامر العمل في Field Service لأوامر المبيعات في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7ecf4-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="7ecf4-116">الفواتير في Field Service لفواتير النص الحر في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7ecf4-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="7ecf4-117">لمشاهدة مثال عن كيف يمكن مزامنة أمر عمل بين Field Service وFinance and Operations، شاهد فيديو YouTube القصير:</span><span class="sxs-lookup"><span data-stu-id="7ecf4-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/hAB4TDVMjxU]

[<span data-ttu-id="7ecf4-118">مزامنة أمر عمل بين Field Service and Finance وOperations (فيديو YouTube)</span><span class="sxs-lookup"><span data-stu-id="7ecf4-118">Synchronize a work order between Field Service and Finance and Operations (YouTube video)</span></span>](https://youtu.be/hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="7ecf4-119">متطلبات النظام لـ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7ecf4-119">System requirements for Finance and Operations</span></span>
<span data-ttu-id="7ecf4-120">يدعم تكامل Field Service الإصدارات التالية:</span><span class="sxs-lookup"><span data-stu-id="7ecf4-120">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="7ecf4-121">Dynamics 365 for Finance and Operations، إصدار 8.0 (إبريل 2018) أو إصدار أحدث</span><span class="sxs-lookup"><span data-stu-id="7ecf4-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="7ecf4-122">تم إصدار Dynamics 365 for Finance and Operations، إصدار 8.0 في أبريل 2018 ويشتمل على رقم إصدار تطبيق 8.0.30.8020 مع تحديث النظام الأساسي 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="7ecf4-122">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="7ecf4-123">متطلبات النظام لـ Field Service</span><span class="sxs-lookup"><span data-stu-id="7ecf4-123">System requirements for Field Service</span></span>
<span data-ttu-id="7ecf4-124">لاستخدام حل تكامل Field Service، يجب عليك تثبيت المكونات التالية:</span><span class="sxs-lookup"><span data-stu-id="7ecf4-124">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="7ecf4-125">الإصدار 9.0 من Microsoft Dynamics 365 for Field Service أو إصدار أحدث</span><span class="sxs-lookup"><span data-stu-id="7ecf4-125">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="7ecf4-126">Dynamics 365 for Field Service، الإصدار 1612 (9.0.1.733) (DB 9.0.1.733) عبر الإنترنت أو إصدار أحدث.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-126">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="7ecf4-127">حل العميل المتوقع إلى النقدية (P2C) لتطبيق Dynamics 365، الإصدار 1.15.0.1 أو إصدار أحدث.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-127">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="7ecf4-128">الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="7ecf4-128">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="7ecf4-129">حل تكامل Field Service، إصدار 1.0.0.0 أو إصدار أحدث.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-129">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="7ecf4-130">الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span><span class="sxs-lookup"><span data-stu-id="7ecf4-130">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

