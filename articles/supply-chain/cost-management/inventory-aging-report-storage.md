---
title: تقرير تقادم المخزون
description: يصف هذا الموضوع الوظيفة التي تتيح لك امكانيه تشغيل تقرير فتره تاخر المخزون وجعل المخرجات متاحه كنموذج ومخطط.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
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
ms.openlocfilehash: 790c8fe3a52bce652227f1cef97eff6496476100
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201607"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="6cdc8-103">تقرير تقادم المخزون</span><span class="sxs-lookup"><span data-stu-id="6cdc8-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="6cdc8-104">في Microsoft Dynamics 365 Supply Chain Management، يمكنك تشغيل تقرير **فتره تقادم المخزون** وجعل المخرجات متاحه كنموذج ومخطط.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="6cdc8-105">في النموذج ، يتم تسويه الاعمده والارصده التجميعية بشكل حيوي ، وذلك وفقا للتخطيط الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="6cdc8-106">يوفر المخطط نظره عامه مرئية تدعم التصفية ويتيح لك التنقل لأسفل إلى التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="6cdc8-107">بالإضافة إلى ذلك، يتيح لك كيان البيانات المسمى **تقرير فترة تقادم المخزون** تصدير نتائج تشغيل تقرير **تقادم المخزون** إلى تنسيق مثل ملف Microsoft Excel أو ملف PDF.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="6cdc8-108">تفيد هذه الطريقة الخاصة بتشغيل تقرير **تقادم المخزون** في الحالات التي تحتوي فيها المخرجات علي العديد من البنود.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="6cdc8-109">على سبيل المثال ، سيحتوي الإخراج علي العديد من البنود إذا كان لديك 50,000 أصناف و 300 متجر يتم إنشاؤها كمستودعات ، وطلب فتره تاخر المخزون حسب الصنف والموقع والمستودع.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="6cdc8-110">تشغيل تقرير تقادم المخزون</span><span class="sxs-lookup"><span data-stu-id="6cdc8-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="6cdc8-111">انتقل إلى **إدارة التكاليف \> الاستعلامات والتقارير \> تخزين تقرير تقادم المخزون**.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="6cdc8-112">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-112">Select **New**.</span></span>
1. <span data-ttu-id="6cdc8-113">في حقل **معرف العملية - الاسم**، أدخل اسمًا فريدًا للتقرير.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="6cdc8-114">حدد تقرير **الهوية - المعرف**، وقم بتصفيته حسب الطلب.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="6cdc8-115">دائما ما تتم عمليه تنفيذ التقرير في وظيفة دفعة.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="6cdc8-116">بعد إكمال وظيفة الدفعة، يتم عرض الإخراج في صفحه **تخزين تقرير تقادم المخزون**.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="6cdc8-117">لعرض الإخراج كنموذج يحتوي علي تخطيط شبكه تقليدي، حدد **عرض التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="6cdc8-118">لعرض الإخراج كمخطط مجمع، حدد **عرض المخطط**.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6cdc8-119">لن يتضمن النموذج الإجماليات الفرعية التي تم تحديدها في تخطيط التقرير.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="6cdc8-120">ييح لك كيان بيانات **تقرير تقادم المخزون** استكشاف إخراج تقرير **تقادم المخزون** عن طريق تطبيق عامل تصفية لحقل **الاسم** إلى أي تنسيق تدعمه إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
