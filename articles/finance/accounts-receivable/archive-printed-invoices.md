---
title: أرشفة فواتير العملاء المطبوعة ذات أرقام التجزئة
description: يوضح هذا الموضوع كيفية تمكين الأرشفة من أجل تخزين فواتير العميل المطبوعة بأرقام التجزئة.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5b0305381ee709ce52b18d171a1ea274e2126cce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827688"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="90f48-103">أرشفة فواتير العملاء المطبوعة ذات أرقام التجزئة</span><span class="sxs-lookup"><span data-stu-id="90f48-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="90f48-104">في بعض البلدان، هناك متطلب قانوني لتخزين أرقام التجزئة المحسوبة في النظام مع النُسخ المطبوعة لبعض المستندات.</span><span class="sxs-lookup"><span data-stu-id="90f48-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="90f48-105">يمكن استخدام أرقام التجزئة لإعداد التقارير إلى السلطات وأثناء عمليات التدقيق.</span><span class="sxs-lookup"><span data-stu-id="90f48-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="90f48-106">يوضح هذا الموضوع كيفية تكوين الأرشفة من أجل تخزين فواتير العميل المطبوعة بأرقام التجزئة.</span><span class="sxs-lookup"><span data-stu-id="90f48-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="90f48-107">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="90f48-107">Prerequisites</span></span>

- <span data-ttu-id="90f48-108">في مساحة عمل **إدارة الميزات**، قم بتشغيل الميزة **أرشفة فواتير العملاء المطبوعة بأرقام التجزئة**.</span><span class="sxs-lookup"><span data-stu-id="90f48-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="90f48-109">لمزيد من المعلومات، راجع [‏‫نظرة عامة على إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="90f48-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="90f48-110">قم بتكوين التنسيقات القابلة للطباعة للمستندات المطلوبة في **إدارة الطباعة**.</span><span class="sxs-lookup"><span data-stu-id="90f48-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="90f48-111">تنطبق هذه الوظيفة على المستندات التالية.</span><span class="sxs-lookup"><span data-stu-id="90f48-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="90f48-112">**الحسابات المدينة**</span><span class="sxs-lookup"><span data-stu-id="90f48-112">**Accounts receivable**</span></span>
- <span data-ttu-id="90f48-113">فاتورة العميل</span><span class="sxs-lookup"><span data-stu-id="90f48-113">Customer invoice</span></span>
- <span data-ttu-id="90f48-114">اشعار ائتمان العميل</span><span class="sxs-lookup"><span data-stu-id="90f48-114">Customer credit note</span></span>
- <span data-ttu-id="90f48-115">فاتورة ذات نص حر</span><span class="sxs-lookup"><span data-stu-id="90f48-115">Free text invoice</span></span>
- <span data-ttu-id="90f48-116">إشعار دائن بنص حر</span><span class="sxs-lookup"><span data-stu-id="90f48-116">Free text credit note</span></span>

<span data-ttu-id="90f48-117">**إدارة المشاريع ومحاسبتها**</span><span class="sxs-lookup"><span data-stu-id="90f48-117">**Project management and accounting**</span></span>
- <span data-ttu-id="90f48-118">فاتورة المشروع</span><span class="sxs-lookup"><span data-stu-id="90f48-118">Project invoice</span></span>
- <span data-ttu-id="90f48-119">إشعار الدائن للمشروع</span><span class="sxs-lookup"><span data-stu-id="90f48-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="90f48-120">تكوين البيانات الرئيسية للعملاء</span><span class="sxs-lookup"><span data-stu-id="90f48-120">Configure customer master data</span></span>
<span data-ttu-id="90f48-121">أكمل الخطوات التالية لتكوين بيانات العميل ولتشغيل إمكانية حفظ الفواتير المطبوعة تلقائيًا كمرفقات.</span><span class="sxs-lookup"><span data-stu-id="90f48-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="90f48-122">انتقل إلى **الحسابات المدينة** > **كافة العملاء‬**.</span><span class="sxs-lookup"><span data-stu-id="90f48-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="90f48-123">حدد عميلاً، وفي علامة التبويب السريعة **الفاتورة والتسليم**، في قسم **الفاتورة الإلكترونية**، في حقل **مرفق الفاتورة الإلكترونية**، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="90f48-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="90f48-124">طباعة الفواتير</span><span class="sxs-lookup"><span data-stu-id="90f48-124">Print invoices</span></span>
<span data-ttu-id="90f48-125">يمكنك ترحيل وطباعة أي نص حر والعميل وفاتورة المشروع أو الإشعار الدائن الخاص بالعميل الذي تم تكوينة في الإجراء السابق.</span><span class="sxs-lookup"><span data-stu-id="90f48-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="90f48-126">افتح صفحة **المرفقات** للفاتورة المطبوعة.</span><span class="sxs-lookup"><span data-stu-id="90f48-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="90f48-127">في علامة التبويب السريعة **المرفق**، في مجموعة حقول **التفاصيل الإضافية**، في حقل **رقم تجزئة المستند**، قم بالبحث عن رقم التجزئة المخزن الذي تم حسابه للفاتورة المطبوعة.</span><span class="sxs-lookup"><span data-stu-id="90f48-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![رقم تجزئة المرفقات](media/attach-hash-num.jpg)

