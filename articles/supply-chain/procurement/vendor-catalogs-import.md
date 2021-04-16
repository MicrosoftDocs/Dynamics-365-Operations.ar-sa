---
title: استيراد كتالوجات المورِّد
description: يصف هذا الموضوع عملية استيراد بيانات كتالوج المورد.
author: kamaybac
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: dabourq
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: ee709d72098b4304cf7748cae1a328736fa16188
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825220"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="8d965-103">استيراد كتالوجات المورِّد</span><span class="sxs-lookup"><span data-stu-id="8d965-103">Import vendor catalogs</span></span>

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="8d965-104">استيراد كتالوجات المورِّد</span><span class="sxs-lookup"><span data-stu-id="8d965-104">Vendor catalogs import</span></span>

<span data-ttu-id="8d965-105">في Dynamics 365 Supply Chain Management، بإمكان محترفي الشراء إنشاء وصيانة كتالوجات يمكن لموظفي الشركة استخدامها عندما يطلبون الأصناف والخدمات للاستخدام الداخلي.</span><span class="sxs-lookup"><span data-stu-id="8d965-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="8d965-106">لإنشاء كتالوج تدبير، يمكنك إضافة الأصناف والخدمات التي تريد توفيرها للموظفين، إما عن طريق استيراد بيانات كتالوج المنتج أو عن طريق إضافة بيانات كتالوج المنتج لأصل المنتج يدوياً.</span><span class="sxs-lookup"><span data-stu-id="8d965-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="8d965-107">يمكنك تحميل بيانات الكتالوج المرسلة من قِبل مورّد من عميل Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8d965-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="8d965-108">يجب أن تكون بيانات المنتج التي يرسلها مورد إليك، بصيغة ملف طلب كتالوج (CMR)، بتنسيق ملف XML.</span><span class="sxs-lookup"><span data-stu-id="8d965-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="8d965-109">يجب أن يحتوي ملف CMR على تفاصيل المنتجات التي يوفرها المورد لشركتك.</span><span class="sxs-lookup"><span data-stu-id="8d965-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="8d965-110">استيراد بيانات كتالوج المورِّد</span><span class="sxs-lookup"><span data-stu-id="8d965-110">Import vendor catalog data</span></span>

<span data-ttu-id="8d965-111">لاستيراد كتالوج المورّد، يجب أن تكمل المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="8d965-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1. <span data-ttu-id="8d965-112">إعداد مشروع في مساحة عمل إدارة البيانات حيث قمت بتحديد قواعد تعيين البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="8d965-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="8d965-113">حدد **إدارة البيانات**، ثم حدد **إعداد أدوار لمشاريع البيانات**.</span><span class="sxs-lookup"><span data-stu-id="8d965-113">Select **Data management** and then select **Set up roles for data projects**.</span></span>

2. <span data-ttu-id="8d965-114">إعداد تدرج هرمي لفئات التدبير، وقم بتعيين الموردين لفئات التدبير.</span><span class="sxs-lookup"><span data-stu-id="8d965-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="8d965-115">إذا كنت تستخدم أكواد السلع، فقم بإضافة أكواد السلع إلى فئات التدبير.</span><span class="sxs-lookup"><span data-stu-id="8d965-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="8d965-116">لمزيد من المعلومات حول إعداد تدرج هرمي لفئات التدبير، راجع [إعداد تدرج هرمي لفئات التدبير](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="8d965-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3. <span data-ttu-id="8d965-117">تكوين بيانات المورّد لاستيراد الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="8d965-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="8d965-118">حدد موردًا، ثم حدد **التدبير** > **إعداد** > **تكوين المورد لاستيراد الكتالوج**.</span><span class="sxs-lookup"><span data-stu-id="8d965-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4. <span data-ttu-id="8d965-119">تكوين سير العمل لاستيراد الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="8d965-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="8d965-120">أنشئ قالب ملف CMR وشارك هذا مع المورد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8d965-120">Create a CMR file template and share this with your vendor.</span></span>

5. <span data-ttu-id="8d965-121">حدد **التدبير والتوريد**\>**الشائعة**\>**الكتالوجات**\>**كتالوجات الموردين** لإنشاء كتالوج مورد.</span><span class="sxs-lookup"><span data-stu-id="8d965-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="8d965-122">يتم تجميع ملفات طلب صيانة الكتالوج (CMR) التي تتلقاها من المورد الخاص بك في هذا الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="8d965-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6. <span data-ttu-id="8d965-123">تحميل ملف CMR.</span><span class="sxs-lookup"><span data-stu-id="8d965-123">Upload the CMR file.</span></span>

7. <span data-ttu-id="8d965-124">قم بمراجعة أو اعتماد أو رفض المنتجات في كتالوج المورد.</span><span class="sxs-lookup"><span data-stu-id="8d965-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="8d965-125">يتم تعيين المنتجات بشكل تلقائي إلى فئات التدبير.</span><span class="sxs-lookup"><span data-stu-id="8d965-125">The products are automatically mapped to the procurement categories.</span></span> 

<span data-ttu-id="8d965-126">وتتم إضافة المنتجات المعتمدة إلى أصول المنتجات ويتم إصدارها إلى الكيانات القانونية المحددة، أو يمكن استخدامها لإنشاء أوامر شراء.</span><span class="sxs-lookup"><span data-stu-id="8d965-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="8d965-127">يمكن إضافة المنتجات المدعومة فقط إلى كتالوج التدبير.</span><span class="sxs-lookup"><span data-stu-id="8d965-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="8d965-128">إنشاء قالب ملف استيراد كتالوج</span><span class="sxs-lookup"><span data-stu-id="8d965-128">Generate a catalog import file template</span></span>

<span data-ttu-id="8d965-129">يتألف قالب ملف استيراد الكتالوج من ملف XSD الذي تستخدمه لإنشاء ملف طلب صيانة الكتالوج لمنتجات المورّد.</span><span class="sxs-lookup"><span data-stu-id="8d965-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="8d965-130">يمكنك استخدام ملف طلب صيانة الكتالوج لإنشاء كتالوج جديد، أو استبدال كتالوج حالي، أو تعديل كتالوج حالي.</span><span class="sxs-lookup"><span data-stu-id="8d965-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1. <span data-ttu-id="8d965-131">حدد **التدبير والتوريد** \> **الكتالوجات** \> **كتالوجات الموردين** وانقر نقراً مزدوجاً فوق الكتالوج الذي تريد العمل فيه.</span><span class="sxs-lookup"><span data-stu-id="8d965-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor  catalogs** and double-click the catalog that you want  to work with.</span></span>

2. <span data-ttu-id="8d965-132">تنزيل قالب استيراد كتالوج حالي (ملف XSD).</span><span class="sxs-lookup"><span data-stu-id="8d965-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="8d965-133">في صفحة **تحديث الكتالوج**، في **جزء الإجراءات**، في علامة التبويب **الكتالوجات**، في مجموعة **المعلومات ذات الصلة**، انقر فوق **إنشاء قالب كتالوج**، ثم حدد **فئة التدبير**.</span><span class="sxs-lookup"><span data-stu-id="8d965-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    - <span data-ttu-id="8d965-134">باستخدام خيار **فئة التدبير**، يمكنك إنشاء قالب الكتالوج الذي يحتوي على فئات التدبير التي يتم فيها اعتماد المورد لتقديم المنتجات.</span><span class="sxs-lookup"><span data-stu-id="8d965-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="8d965-135">في مربع الحوار **حفظ باسم**، حدد الموقع الذي تريد تخزين قالب ملف الكتالوج، وحفظ الملف به.</span><span class="sxs-lookup"><span data-stu-id="8d965-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="8d965-136">لمزيد من المعلومات والأمثلة، ارجع إلى نشرة المدونة هذه: [كتالوجات الموردين في Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="8d965-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]