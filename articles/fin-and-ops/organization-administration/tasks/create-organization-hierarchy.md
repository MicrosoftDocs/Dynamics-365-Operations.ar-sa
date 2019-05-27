---
title: إنشاء تدرج هرمي للمؤسسات.
description: استخدم الإجراء التالي لإنشاء تدرج هرمي للمؤسسات.
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 203a586b06a13a7c67f246384152d17627e22041
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545532"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="58845-103">إنشاء تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="58845-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="58845-104">استخدم الإجراء التالي لإنشاء تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="58845-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="58845-105">يمكنك استخدام التدرجات الهرمية المؤسسية لعرض العمل الخاص بك وإنشاء التقارير الخاصة به من منظورات متعددة.</span><span class="sxs-lookup"><span data-stu-id="58845-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="58845-106">على سبيل المثال، يمكنك إعداد تدرج هرمي للتقارير الضريبية أو القانونية.</span><span class="sxs-lookup"><span data-stu-id="58845-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="58845-107">ثم يمكنك إعداد تدرج هرمي آخر لإنشاء تقارير خاصة بالمعلومات المالية غير المطلوبة قانونيًا، ولكنها مستخدمة من أجل الإنشاء الداخلي للتقارير.</span><span class="sxs-lookup"><span data-stu-id="58845-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="58845-108">حتى تتمكن من إنشاء تدرج هرمي مؤسسي، يتعين عليك إنشاء مؤسسات.</span><span class="sxs-lookup"><span data-stu-id="58845-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="58845-109">لمزيد من المعلومات، راجع المهمتين: "إنشاء كيان قانوني" أو "إنشاء وحدة تشغيل".</span><span class="sxs-lookup"><span data-stu-id="58845-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="58845-110">يمكنك أيضًا إنشاء الأقسام والفرق.</span><span class="sxs-lookup"><span data-stu-id="58845-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="58845-111">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="58845-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="58845-112">إنشاء تدرج هرمي</span><span class="sxs-lookup"><span data-stu-id="58845-112">Create a hierarchy</span></span>
1. <span data-ttu-id="58845-113">انتقل إلى إدارة المؤسسة > المؤسسات > التدرجات الهرمية للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="58845-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="58845-114">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="58845-114">Click New.</span></span>
3. <span data-ttu-id="58845-115">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="58845-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="58845-116">انقر فوق "تعيين غرض".</span><span class="sxs-lookup"><span data-stu-id="58845-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="58845-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="58845-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="58845-118">حدد غرضًا للتعيين إلى التدرج الهرمي للمؤسسات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="58845-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="58845-119">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="58845-119">Click Add.</span></span>
7. <span data-ttu-id="58845-120">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="58845-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="58845-121">ابحث عن التدرج الهرمي الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="58845-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="58845-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="58845-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="58845-123">إضافة مؤسسات إلى التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="58845-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="58845-124">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="58845-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="58845-125">قم بتحديد التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="58845-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="58845-126">انقر فوق "عرض التدرج الهرمي".</span><span class="sxs-lookup"><span data-stu-id="58845-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="58845-127">قم بإضافة المؤسسات، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="58845-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="58845-128">لإضافة مؤسسة ما، انقر فوق "تحرير" ثم "إدراج" لإضافة المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="58845-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="58845-129">عند الانتهاء من إجراء التغييرات، يمكنك حفظ مسودة و/أو نشر التغييرات.</span><span class="sxs-lookup"><span data-stu-id="58845-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  

