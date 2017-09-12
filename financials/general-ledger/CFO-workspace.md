---
title: "إضافة الأبعاد المالية إلى مساحة عمل المدير المالي‬"
description: "يشرح هذا المقال كيفية إضافة الأبعاد المالية إلى مساحة عمل المدير المالي، بحيث يمكن استخدامها لتقارير دفتر الأستاذ والموازنة."
author: aolson
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
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: ar-sa
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="dc842-103">إضافة الأبعاد المالية إلى مساحة عمل المدير المالي‬</span><span class="sxs-lookup"><span data-stu-id="dc842-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dc842-104">يشرح هذا المقال كيفية إضافة الأبعاد المالية إلى مساحة عمل المدير المالي، بحيث يمكن استخدامها لتقارير دفتر الأستاذ والموازنة.</span><span class="sxs-lookup"><span data-stu-id="dc842-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="dc842-105">تتضمن مساحة عمل المدير المالي علامة التبويب **نظرة عامة** وعلامة التبويب **مالي**.</span><span class="sxs-lookup"><span data-stu-id="dc842-105">The CFO workspace has an **Overview** tab and a **Financial** tab.</span></span> <span data-ttu-id="dc842-106">يتم إجراء نسخ احتياطي للتقارير على علامتي التبويب باستخدام مقياسين: LedgerActivityMeasure وBudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="dc842-106">The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="dc842-107">في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition تحديث يوليو 2017، توجد علاقة بين هذين المقياسين والكيان DimensionCombinationEntity.</span><span class="sxs-lookup"><span data-stu-id="dc842-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="dc842-108">لذلك، يمكنك تحديد الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="dc842-108">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="dc842-109">في Finance and Operations، في صفحة **متجر الكيانات**، قم بتحديث المقياسين **LedgerActivityMeasure**و**BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="dc842-109">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="dc842-110">في Microsoft Visual Studio، افتح مستكشف التطبيق، وابحث عن **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="dc842-110">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="dc842-111">ضمن **الموارد**، افتح **LedgerCFOWorkspacePBIX‎**.</span><span class="sxs-lookup"><span data-stu-id="dc842-111">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="dc842-112">عندما يفتح المورد في Microsoft Power BI Desktop، حدد **الحصول على البيانات**، وحدد **قاعدة بيانات SQL Server**، ثم حدد **اتصال**.</span><span class="sxs-lookup"><span data-stu-id="dc842-112">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="dc842-113">أدخل اسم الخادم، ثم أدخل **AxDW** كقاعدة بيانات.</span><span class="sxs-lookup"><span data-stu-id="dc842-113">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="dc842-114">حدد **DirectQuery**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="dc842-114">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="dc842-115">ابحث عن **LedgerActivityMeasure\_DimensionCombination** وحدده، ثم حدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="dc842-115">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="dc842-116">في قائمة **الحقول**، أعد تسمية جدول **الأبعاد المالية**، لتسهيل التعرف عليه.</span><span class="sxs-lookup"><span data-stu-id="dc842-116">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="dc842-117">حدد **إدارة العلاقات**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="dc842-117">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="dc842-118">في الحقل الأول، حدد **أنشطة دفتر الأستاذ العام**، ثم حدد **LedgerDimension‎**.</span><span class="sxs-lookup"><span data-stu-id="dc842-118">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="dc842-119">في الحقل الثاني، حدد **LedgerActivityMeasure\_DimensionCombination** (أو **الأبعاد المالية** إذا أعدت تسمية الجدول).</span><span class="sxs-lookup"><span data-stu-id="dc842-119">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="dc842-120">حدد الرأس  **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="dc842-120">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="dc842-121">في حقل **العلاقة الأساسية‬**، حدد **من عديد إلى واحد**.</span><span class="sxs-lookup"><span data-stu-id="dc842-121">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="dc842-122">قم بتغيير قيمة **اتجاه التصفية المتقاطع** إلى **فردي**.</span><span class="sxs-lookup"><span data-stu-id="dc842-122">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="dc842-123">حدد الخيارين **تنشيط هذه العلاقة** و**افتراض التكامل المرجعي**، وحدد **OK**، ثم حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="dc842-123">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="dc842-124">[![إنشاء علاقة](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="dc842-124">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="dc842-125">في قائمة **الحقول**، من المفترض أن ترى الجدول والأبعاد المالية المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="dc842-125">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="dc842-126">اسحب الأبعاد المالية المطلوبة إلى عوامل التصفية على مستوى التقرير.</span><span class="sxs-lookup"><span data-stu-id="dc842-126">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="dc842-127">‏‏قم بحفظ التغييرات التي قمت بإجرائها.</span><span class="sxs-lookup"><span data-stu-id="dc842-127">Save your changes.</span></span>
15. <span data-ttu-id="dc842-128">في شجرة مكونات البرنامج (AOT)، انقر بزر الماوس الأيمن فوق المشروع، ثم حدد **مزامنة**.</span><span class="sxs-lookup"><span data-stu-id="dc842-128">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="dc842-129">أنشئ مشروعك، ثم افتح التطبيق لعرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="dc842-129">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="dc842-130">[![مساحة عمل مكتملة](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="dc842-130">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

