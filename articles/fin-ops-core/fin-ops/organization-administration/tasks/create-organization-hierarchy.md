---
title: إنشاء تدرج هرمي للمؤسسات.
description: استخدم الإجراء التالي لإنشاء تدرج هرمي للمؤسسات.
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: 48c8564694b22a5110341d853a79096fbe805c91
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176311"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="47eab-103">إنشاء تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="47eab-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47eab-104">استخدم الإجراء التالي لإنشاء تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="47eab-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="47eab-105">يمكنك استخدام التدرجات الهرمية المؤسسية لعرض العمل الخاص بك وإنشاء التقارير الخاصة به من منظورات متعددة.</span><span class="sxs-lookup"><span data-stu-id="47eab-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="47eab-106">على سبيل المثال، يمكنك إعداد تدرج هرمي للتقارير الضريبية أو القانونية.</span><span class="sxs-lookup"><span data-stu-id="47eab-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="47eab-107">ثم يمكنك إعداد تدرج هرمي آخر لإنشاء تقارير خاصة بالمعلومات المالية غير المطلوبة قانونيًا، ولكنها مستخدمة من أجل الإنشاء الداخلي للتقارير.</span><span class="sxs-lookup"><span data-stu-id="47eab-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="47eab-108">حتى تتمكن من إنشاء تدرج هرمي مؤسسي، يتعين عليك إنشاء مؤسسات.</span><span class="sxs-lookup"><span data-stu-id="47eab-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="47eab-109">لمزيد من المعلومات، راجع المهمتين: "إنشاء كيان قانوني" أو "إنشاء وحدة تشغيل".</span><span class="sxs-lookup"><span data-stu-id="47eab-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="47eab-110">يمكنك أيضًا إنشاء الأقسام والفرق.</span><span class="sxs-lookup"><span data-stu-id="47eab-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="47eab-111">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="47eab-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="47eab-112">إنشاء تدرج هرمي</span><span class="sxs-lookup"><span data-stu-id="47eab-112">Create a hierarchy</span></span>
1. <span data-ttu-id="47eab-113">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المؤسسة > المؤسسات > التدرجات الهرمية للمؤسسات**.</span><span class="sxs-lookup"><span data-stu-id="47eab-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="47eab-114">انقر فوق **جديد** في **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="47eab-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="47eab-115">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="47eab-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="47eab-116">في قسم **الغرض**، انقر فوق **تعيين غرض‬**.</span><span class="sxs-lookup"><span data-stu-id="47eab-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="47eab-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="47eab-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="47eab-118">حدد غرضًا للتعيين إلى التدرج الهرمي للمؤسسات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="47eab-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="47eab-119">في قسم **التدرجات الهرمية المعينة‬**، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="47eab-119">In the **Assigned hierarchies** sectiom, click **Add**.</span></span>
7. <span data-ttu-id="47eab-120">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="47eab-120">In the list, mark the selected row.</span></span> <span data-ttu-id="47eab-121">ابحث عن التدرج الهرمي الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="47eab-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="47eab-122">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="47eab-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="47eab-123">إضافة مؤسسات إلى التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="47eab-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="47eab-124">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="47eab-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="47eab-125">قم بتحديد التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="47eab-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="47eab-126">في قسم **التدرجات الهرمية المعينة**، انقر فوق **عرض التدرج الهرمي**.</span><span class="sxs-lookup"><span data-stu-id="47eab-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="47eab-127">قم بإضافة المؤسسات، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="47eab-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="47eab-128">لإضافة مؤسسة، انقر فوق **تحرير** ثم فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="47eab-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="47eab-129">عند الانتهاء من إجراء التغييرات، يمكنك **حفظ** مسودة و/أو **نشر** التغييرات.</span><span class="sxs-lookup"><span data-stu-id="47eab-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

