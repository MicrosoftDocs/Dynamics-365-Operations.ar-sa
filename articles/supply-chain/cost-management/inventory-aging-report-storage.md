---
title: تخزين تقرير تقادم المخزون
description: يصف هذا الموضوع الوظيفة التي تتيح لك امكانيه تشغيل تقرير فتره تاخر المخزون وجعل المخرجات متاحه كنموذج ومخطط.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: c4a1480cf96a4ba753b436c04eb8f7b01379da48
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421345"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="3a004-103">تخزين تقرير تقادم المخزون</span><span class="sxs-lookup"><span data-stu-id="3a004-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a004-104">في Microsoft Dynamics 365 Supply Chain Management، يمكنك تشغيل تقرير **تخزين تقرير تقادم المخزون‬** وجعل المخرجات متاحة كنموذج ومخطط.</span><span class="sxs-lookup"><span data-stu-id="3a004-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="3a004-105">في النموذج ، يتم تسويه الاعمده والارصده التجميعية بشكل حيوي ، وذلك وفقا للتخطيط الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="3a004-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="3a004-106">يوفر المخطط نظره عامه مرئية تدعم التصفية ويتيح لك التنقل لأسفل إلى التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="3a004-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="3a004-107">بالإضافة إلى ذلك، يتيح لك كيان البيانات المسمى **تقرير تقادم المخزون** تصدير النتائج لتشغيل تقرير **تخزين تقرير تقادم المخزون‬** إلى تنسيق مثل ملف Microsoft Excel أو ملف PDF.</span><span class="sxs-lookup"><span data-stu-id="3a004-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="3a004-108">تفيد هذه الطريقة الخاصة بتشغيل تقرير **تخزين تقرير تقادم المخزون‬** في الحالات التي تحتوي فيها المخرجات على العديد من البنود.</span><span class="sxs-lookup"><span data-stu-id="3a004-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="3a004-109">على سبيل المثال ، سيحتوي الإخراج علي العديد من البنود إذا كان لديك 50,000 أصناف و 300 متجر يتم إنشاؤها كمستودعات ، وطلب فتره تاخر المخزون حسب الصنف والموقع والمستودع.</span><span class="sxs-lookup"><span data-stu-id="3a004-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="3a004-110">تمكين ميزة تقرير تخزين قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="3a004-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="3a004-111">قبل أن تتمكن من استخدام هذه الميزة، فإنه يجب عليك تمكينه على النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="3a004-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="3a004-112">يمكن للمسؤولين [استخدام إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) الإعدادات للتحقق من حالة الميزة وتمكينها إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="3a004-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="3a004-113">هنا، يتم إدراج الميزة كـ:</span><span class="sxs-lookup"><span data-stu-id="3a004-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="3a004-114">**الوحدة** - إدارة التكلفة</span><span class="sxs-lookup"><span data-stu-id="3a004-114">**Module** - Cost management</span></span>
- <span data-ttu-id="3a004-115">**اسم الميزة** - تخزين تقرير تقادم المخزون</span><span class="sxs-lookup"><span data-stu-id="3a004-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="3a004-116">تشغيل تخزين تقرير تقادم المخزون</span><span class="sxs-lookup"><span data-stu-id="3a004-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="3a004-117">انتقل إلى **إدارة التكاليف \> الاستعلامات والتقارير \> تخزين تقرير تقادم المخزون**.</span><span class="sxs-lookup"><span data-stu-id="3a004-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="3a004-118">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="3a004-118">Select **New**.</span></span>
1. <span data-ttu-id="3a004-119">في حقل **معرف العملية - الاسم**، أدخل اسمًا فريدًا للتقرير.</span><span class="sxs-lookup"><span data-stu-id="3a004-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="3a004-120">حدد تقرير **الهوية - المعرف**، وقم بتصفيته حسب الطلب.</span><span class="sxs-lookup"><span data-stu-id="3a004-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="3a004-121">دائما ما تتم عمليه تنفيذ التقرير في وظيفة دفعة.</span><span class="sxs-lookup"><span data-stu-id="3a004-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="3a004-122">بعد إكمال وظيفة الدفعة، يتم عرض الإخراج في صفحه **تخزين تقرير تقادم المخزون**.</span><span class="sxs-lookup"><span data-stu-id="3a004-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="3a004-123">لعرض الإخراج كنموذج يحتوي علي تخطيط شبكه تقليدي، حدد **عرض التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="3a004-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="3a004-124">لعرض الإخراج كمخطط مجمع، حدد **عرض المخطط**.</span><span class="sxs-lookup"><span data-stu-id="3a004-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a004-125">لن يتضمن النموذج الإجماليات الفرعية التي تم تحديدها في تخطيط التقرير.</span><span class="sxs-lookup"><span data-stu-id="3a004-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="3a004-126">يتيح لك كيان بيانات **تقرير تقادم المخزون** تصدير إخراج تقرير **تخزين تقرير تقادم المخزون‬** عن طريق تطبيق عامل تصفية لحقل **معرف العملية - الاسم** إلى أي تنسيق تدعمه إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="3a004-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
