---
title: استيراد كتالوجات المورِّد
description: يصف هذا الموضوع عملية استيراد بيانات كتالوج المورد.
author: mkirknel
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: cf81823de46da9a834f0214896b9e634989cac0e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569766"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="89ac4-103">استيراد كتالوجات المورِّد</span><span class="sxs-lookup"><span data-stu-id="89ac4-103">Import vendor catalogs</span></span>
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="89ac4-104">استيراد كتالوجات المورِّد</span><span class="sxs-lookup"><span data-stu-id="89ac4-104">Vendor catalogs import</span></span>

<span data-ttu-id="89ac4-105">في Microsoft Dynamics 365 for Finance and Operations، بإمكان محترفي الشراء إنشاء وصيانة كتالوجات يمكن لموظفي الشركة استخدامها عندما يطلبون الأصناف والخدمات للاستخدام الداخلي.</span><span class="sxs-lookup"><span data-stu-id="89ac4-105">In Microsoft Dynamics 365 for Finance and Operations, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="89ac4-106">لإنشاء كتالوج تدبير، يمكنك إضافة الأصناف والخدمات التي تريد توفيرها للموظفين، إما عن طريق استيراد بيانات كتالوج المنتج أو عن طريق إضافة بيانات كتالوج المنتج لأصل المنتج يدوياً.</span><span class="sxs-lookup"><span data-stu-id="89ac4-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="89ac4-107">يمكنك تحميل بيانات الكتالوج المرسلة من قِبل مورّد من عميل Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="89ac4-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="89ac4-108">يجب أن تكون بيانات المنتج التي يرسلها مورد إليك، بصيغة ملف طلب كتالوج (CMR)، بتنسيق ملف XML.</span><span class="sxs-lookup"><span data-stu-id="89ac4-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="89ac4-109">يجب أن يحتوي ملف CMR على تفاصيل المنتجات التي يوفرها المورد لشركتك.</span><span class="sxs-lookup"><span data-stu-id="89ac4-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="89ac4-110">استيراد بيانات كتالوج المورِّد</span><span class="sxs-lookup"><span data-stu-id="89ac4-110">Import vendor catalog data</span></span>

<span data-ttu-id="89ac4-111">لاستيراد كتالوج المورّد، يجب أن تكمل المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="89ac4-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1.  <span data-ttu-id="89ac4-112">إعداد مشروع في مساحة عمل إدارة البيانات حيث قمت بتحديد قواعد تعيين البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="89ac4-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="89ac4-113">حدد **إدارة البيانات**، ثم حدد **إعداد أدوار لمشاريع البيانات**.</span><span class="sxs-lookup"><span data-stu-id="89ac4-113">Select **Data management** and then select **Set up roles for data projects**.</span></span> 

2.  <span data-ttu-id="89ac4-114">إعداد تدرج هرمي لفئات التدبير، وقم بتعيين الموردين لفئات التدبير.</span><span class="sxs-lookup"><span data-stu-id="89ac4-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="89ac4-115">إذا كنت تستخدم أكواد السلع، فقم بإضافة أكواد السلع إلى فئات التدبير.</span><span class="sxs-lookup"><span data-stu-id="89ac4-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="89ac4-116">لمزيد من المعلومات حول إعداد تدرج هرمي لفئات التدبير، راجع [إعداد تدرج هرمي لفئات التدبير](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="89ac4-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3.  <span data-ttu-id="89ac4-117">تكوين بيانات المورّد لاستيراد الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="89ac4-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="89ac4-118">حدد موردًا، ثم حدد **التدبير** > **إعداد** > **تكوين المورد لاستيراد الكتالوج**.</span><span class="sxs-lookup"><span data-stu-id="89ac4-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4.  <span data-ttu-id="89ac4-119">تكوين سير العمل لاستيراد الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="89ac4-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="89ac4-120">أنشئ قالب ملف CMR وشارك هذا مع المورد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="89ac4-120">Create a CMR file template and share this with your vendor.</span></span>

5.  <span data-ttu-id="89ac4-121">حدد **التدبير والتوريد**\>**الشائعة**\>**الكتالوجات**\>**كتالوجات الموردين** لإنشاء كتالوج مورد.</span><span class="sxs-lookup"><span data-stu-id="89ac4-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="89ac4-122">يتم تجميع ملفات طلب صيانة الكتالوج (CMR) التي تتلقاها من المورد الخاص بك في هذا الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="89ac4-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6.  <span data-ttu-id="89ac4-123">تحميل ملف CMR.</span><span class="sxs-lookup"><span data-stu-id="89ac4-123">Upload the CMR file.</span></span>

7.  <span data-ttu-id="89ac4-124">قم بمراجعة أو اعتماد أو رفض المنتجات في كتالوج المورد.</span><span class="sxs-lookup"><span data-stu-id="89ac4-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="89ac4-125">يتم تعيين المنتجات بشكل تلقائي إلى فئات التدبير في Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="89ac4-125">The products are automatically mapped to the procurement categories in Dynamics 365 for Finance and Operations.</span></span> 
    
<span data-ttu-id="89ac4-126">وتتم إضافة المنتجات المعتمدة إلى أصول المنتجات ويتم إصدارها إلى الكيانات القانونية المحددة، أو يمكن استخدامها لإنشاء أوامر شراء.</span><span class="sxs-lookup"><span data-stu-id="89ac4-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="89ac4-127">يمكن إضافة المنتجات المدعومة فقط إلى كتالوج التدبير.</span><span class="sxs-lookup"><span data-stu-id="89ac4-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="89ac4-128">إنشاء قالب ملف استيراد كتالوج</span><span class="sxs-lookup"><span data-stu-id="89ac4-128">Generate a catalog import file template</span></span>

<span data-ttu-id="89ac4-129">يتألف قالب ملف استيراد الكتالوج من ملف XSD والذي تستخدمه لإنشاء ملف طلب صيانة الكتالوج لمنتجات المورد.</span><span class="sxs-lookup"><span data-stu-id="89ac4-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor’s products.</span></span> <span data-ttu-id="89ac4-130">يمكنك استخدام ملف طلب صيانة الكتالوج لإنشاء كتالوج جديد، أو استبدال كتالوج حالي، أو تعديل كتالوج حالي.</span><span class="sxs-lookup"><span data-stu-id="89ac4-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1.  <span data-ttu-id="89ac4-131">حدد **التدبير والتوريد**\>**الكتالوجات**\>**كتالوجات الموردين** وانقر نقراً مزدوجاً فوق الكتالوج الذي تريد العمل فيه.</span><span class="sxs-lookup"><span data-stu-id="89ac4-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor catalogs** and double-click the catalog that you want to work with.</span></span>

2.  <span data-ttu-id="89ac4-132">تنزيل قالب استيراد كتالوج حالي (ملف XSD).</span><span class="sxs-lookup"><span data-stu-id="89ac4-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="89ac4-133">في صفحة **تحديث الكتالوج**، في **جزء الإجراءات**، في علامة التبويب **الكتالوجات**، في مجموعة **المعلومات ذات الصلة**، انقر فوق **إنشاء قالب كتالوج**، ثم حدد **فئة التدبير**.</span><span class="sxs-lookup"><span data-stu-id="89ac4-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    -   <span data-ttu-id="89ac4-134">باستخدام خيار **فئة التدبير**، يمكنك إنشاء قالب الكتالوج الذي يحتوي على فئات التدبير التي يتم فيها اعتماد المورد لتقديم المنتجات.</span><span class="sxs-lookup"><span data-stu-id="89ac4-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="89ac4-135">في مربع الحوار **حفظ باسم**، حدد الموقع الذي تريد تخزين قالب ملف الكتالوج، وحفظ الملف به.</span><span class="sxs-lookup"><span data-stu-id="89ac4-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="89ac4-136">لمزيد من المعلومات والأمثلة، ارجع إلى نشرة المدونة هذه: [كتالوجات الموردين في Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="89ac4-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>
