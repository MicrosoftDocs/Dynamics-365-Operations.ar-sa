---
title: "إضافة الأبعاد المالية إلى مساحة عمل المدير المالي‬"
description: "يشرح هذا المقال كيفية إضافة الأبعاد المالية إلى مساحة عمل المدير المالي، بحيث يمكن استخدامها لتقارير دفتر الأستاذ والموازنة."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e674948f642ab7525f96092a9a1f3adaae66974
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="e8412-103">إضافة الأبعاد المالية إلى مساحة عمل المدير المالي‬</span><span class="sxs-lookup"><span data-stu-id="e8412-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e8412-104">يشرح هذا المقال كيفية إضافة الأبعاد المالية إلى مساحة عمل المدير المالي، بحيث يمكن استخدامها لتقارير دفتر الأستاذ والموازنة.</span><span class="sxs-lookup"><span data-stu-id="e8412-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="e8412-105">تتضمن مساحة عمل المدير المالي علامة التبويب **نظرة عامة** وعلامة التبويب **مالي**. هناك مقياسان لدعم التقارير على علامتي التبويب: LedgerActivityMeasure وBudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="e8412-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="e8412-106">في Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (يوليو 2017)، توجد علاقة بين هذين المقياسين والكيان DimensionCombinationEntity.</span><span class="sxs-lookup"><span data-stu-id="e8412-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="e8412-107">لذلك، يمكنك تحديد الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="e8412-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="e8412-108">في Finance and Operations، في صفحة **متجر الكيانات**، قم بتحديث المقياسين **LedgerActivityMeasure**و**BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="e8412-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="e8412-109">في Microsoft Visual Studio، افتح مستكشف التطبيق، وابحث عن **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="e8412-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="e8412-110">ضمن **الموارد**، افتح **LedgerCFOWorkspacePBIX‎**.</span><span class="sxs-lookup"><span data-stu-id="e8412-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="e8412-111">عندما يفتح المورد في Microsoft Power BI Desktop، حدد **الحصول على البيانات**، وحدد **قاعدة بيانات SQL Server**، ثم حدد **اتصال**.</span><span class="sxs-lookup"><span data-stu-id="e8412-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="e8412-112">أدخل اسم الخادم، ثم أدخل **AxDW** كقاعدة بيانات.</span><span class="sxs-lookup"><span data-stu-id="e8412-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="e8412-113">حدد **DirectQuery**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e8412-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="e8412-114">ابحث عن **LedgerActivityMeasure\_DimensionCombination** وحدده، ثم حدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="e8412-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="e8412-115">في قائمة **الحقول**، أعد تسمية جدول **الأبعاد المالية**، لتسهيل التعرف عليه.</span><span class="sxs-lookup"><span data-stu-id="e8412-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="e8412-116">حدد **إدارة العلاقات**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e8412-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="e8412-117">في الحقل الأول، حدد **أنشطة دفتر الأستاذ العام**، ثم حدد **LedgerDimension‎**.</span><span class="sxs-lookup"><span data-stu-id="e8412-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="e8412-118">في الحقل الثاني، حدد **LedgerActivityMeasure\_DimensionCombination** (أو **الأبعاد المالية** إذا أعدت تسمية الجدول).</span><span class="sxs-lookup"><span data-stu-id="e8412-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="e8412-119">حدد الرأس  **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="e8412-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="e8412-120">في حقل **العلاقة الأساسية‬**، حدد **من عديد إلى واحد**.</span><span class="sxs-lookup"><span data-stu-id="e8412-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="e8412-121">قم بتغيير قيمة **اتجاه التصفية المتقاطع** إلى **فردي**.</span><span class="sxs-lookup"><span data-stu-id="e8412-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="e8412-122">حدد الخيارين **تنشيط هذه العلاقة** و**افتراض التكامل المرجعي**، وحدد **OK**، ثم حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="e8412-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="e8412-123">[![إنشاء علاقة](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="e8412-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="e8412-124">في قائمة **الحقول**، من المفترض أن ترى الجدول والأبعاد المالية المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="e8412-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="e8412-125">اسحب الأبعاد المالية المطلوبة إلى عوامل التصفية على مستوى التقرير.</span><span class="sxs-lookup"><span data-stu-id="e8412-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="e8412-126">‏‏قم بحفظ التغييرات التي قمت بإجرائها.</span><span class="sxs-lookup"><span data-stu-id="e8412-126">Save your changes.</span></span>
15. <span data-ttu-id="e8412-127">في شجرة مكونات البرنامج (AOT)، انقر بزر الماوس الأيمن فوق المشروع، ثم حدد **مزامنة**.</span><span class="sxs-lookup"><span data-stu-id="e8412-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="e8412-128">أنشئ مشروعك، ثم افتح التطبيق لعرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="e8412-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="e8412-129">[![مساحة عمل مكتملة](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="e8412-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>
