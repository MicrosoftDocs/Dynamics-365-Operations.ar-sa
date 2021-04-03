---
title: تكوين المعلمات المشتركة
description: يجب إعداد محددات مشتركة للسجلات التي تتم مشاركتها عبر الشركات، مثل سجلات المناصب. توضح هذه المقالة كيفية إعداد محددات الموارد البشرية عبر الكيانات القانونية.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 297141ab17660533b441629ccdfc624bbcb9c82b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467279"
---
# <a name="configure-shared-parameters"></a><span data-ttu-id="7d1ef-104">تكوين المعلمات المشتركة</span><span class="sxs-lookup"><span data-stu-id="7d1ef-104">Configure shared parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7d1ef-105">يجب إعداد محددات مشتركة للسجلات التي تتم مشاركتها عبر الشركات، مثل سجلات المناصب.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="7d1ef-106">توضح هذه المقالة كيفية إعداد محددات الموارد البشرية عبر الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="7d1ef-107">تتم مشاركة بعض أنواع السجلات، مثل سجلات المناصب، عبر الشركات.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="7d1ef-108">وفي هذه السجلات، يجب إعداد المعلمات المشتركة.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="7d1ef-109">على سبيل المثال، يمكنك استخدام صفحة **المعلمات المشتركة للموارد البشرية** لإعداد معلمات الموارد البشرية عبر الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="7d1ef-110">وفي صفحة **المعلمات المشتركة للموارد البشرية**، يتم تجميع المعلمات في المجالات، استناداً إلى وظائفها.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="7d1ef-111">وظيفة تم إصدارها في وقت سابق</span><span class="sxs-lookup"><span data-stu-id="7d1ef-111">Previously released functionality</span></span>
<span data-ttu-id="7d1ef-112">وفي علامة التبويب **تعريف**، يجب عليك تحديد أنواع التعريف التي تمثل أرقام التعريف المذكورة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="7d1ef-113">يجب عليك إعداد أنواع التعريف قبل أن يمكنك إدخال معلومات التعريف للعاملين.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="7d1ef-114">ويتم الاحتفاظ بالمعلومات المتعلقة برقم الضمان الاجتماعي، ورقم المعرف القومي، ورقم المعرف الأجنبي، وكود معرف الشخصية في صفحة **نوع التعريف**.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="7d1ef-115">لتحديد نوع تعريف جديد أو مراجعة قائمة الأنواع الموجودة، انقر فوق **إدارة العاملين‬** &gt; **علامة تبويب الارتباطات** &gt; **لإعداد** &gt; **أنواع التعريف**.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="7d1ef-116">يمكنك إدخال وصف وكود بسيط.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-human-resources"></a><span data-ttu-id="7d1ef-117">إذا كنت تستخدم Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="7d1ef-117">If you're using Dynamics 365 Human Resources</span></span>
<span data-ttu-id="7d1ef-118">وفي علامة التبويب **تعريف**، يجب عليك تحديد أنواع التعريف التي تمثل أرقام التعريف المذكورة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="7d1ef-119">يجب عليك إعداد أنواع التعريف قبل أن يمكنك إدخال معلومات التعريف للعاملين.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="7d1ef-120">ويتم الاحتفاظ بالمعلومات المتعلقة برقم الضمان الاجتماعي، ورقم المعرف القومي، ورقم المعرف الأجنبي، وكود معرف الشخصية في صفحة **نوع التعريف**.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="7d1ef-121">ولتحديد نوع تعريف جديد أو مراجعة قائمة الأنواع الموجودة، انقر فوق **الموارد البشرية** &gt; **الإعداد** &gt; **أنواع التعريف**.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="7d1ef-122">يمكنك إدخال وصف وكود بسيط.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="7d1ef-123">وفي علامة التبويب **التسلسلات الرقمية**، يمكنك تحديد التسلسلات الرقمية التي يتم استخدامها للسجلات التالية: عدد العاملين، والمنصب، ومعرف طلب المستخدم، ومستند I-9، ومقدم الطلب، والمناقشة، ومعرف الميزة، وإجراء العاملين (إذا تم تمكين هذا النوع من السجلات).</span><span class="sxs-lookup"><span data-stu-id="7d1ef-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="7d1ef-124">وللاحتفاظ بأكواد ومراجع التسلسل الرقمي، استخدم صفحة قائمة **التسلسلات الرقمية**.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="7d1ef-125">وللعثور على هذه الصفحة، استخدم ميزة البحث عن الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="7d1ef-126">وفي علامة التبويب **مناصب**، أشر إلى ما إذا كانت الوظائف الجديدة متوفرة للتعيين بشكل افتراضي:</span><span class="sxs-lookup"><span data-stu-id="7d1ef-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="7d1ef-127">**دائمًا**– يمكنك تعيين عمال لمناصب جديدة عند إنشاء مناصب.‬</span><span class="sxs-lookup"><span data-stu-id="7d1ef-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="7d1ef-128">وعند إنشاء المناصب، يتم تعيين التاريخ والوقت **المتوفر للتعيين** في علامة التبويب **عام** من صفحة **المنصب** إلى تاريخ ووقت الإنشاء تلقائيًا.‬</span><span class="sxs-lookup"><span data-stu-id="7d1ef-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="7d1ef-129">**أبدًا**– لا يمكنك تعيين عمال لمناصب جديدة عند إنشاء مناصب.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="7d1ef-130">إذا قمت بتحديد هذا الخيار، فيجب عليك فتح صفحة **المنصب** لكل منصب جديد عند توفره، ثم في علامة التبويب **عام**، أدخل تاريخ **متوفر للتعيين** لتمكين تعيين العامل.</span><span class="sxs-lookup"><span data-stu-id="7d1ef-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]