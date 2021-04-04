---
title: إنشاء تدرج هرمي للمؤسسات.
description: استخدم الإجراء التالي لإنشاء تدرج هرمي للمؤسسات.
author: sericks007
manager: AnnBe
ms.date: 12/15/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d61d6eee3b55087d633a8416fbed3a6192e82b2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560569"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="b3ae7-103">إنشاء تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3ae7-104">استخدم الإجراء التالي لإنشاء تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="b3ae7-105">يمكنك استخدام التدرجات الهرمية المؤسسية لعرض العمل الخاص بك وإنشاء التقارير الخاصة به من منظورات متعددة.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="b3ae7-106">على سبيل المثال، يمكنك إعداد تدرج هرمي للتقارير الضريبية أو القانونية.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="b3ae7-107">ثم يمكنك إعداد تدرج هرمي آخر لإنشاء تقارير خاصة بالمعلومات المالية غير المطلوبة قانونيًا، ولكنها مستخدمة من أجل الإنشاء الداخلي للتقارير.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="b3ae7-108">حتى تتمكن من إنشاء تدرج هرمي مؤسسي، يتعين عليك إنشاء مؤسسات.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="b3ae7-109">لمزيد من المعلومات، راجع المهمتين: "إنشاء كيان قانوني" أو "إنشاء وحدة تشغيل".</span><span class="sxs-lookup"><span data-stu-id="b3ae7-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="b3ae7-110">يمكنك أيضًا إنشاء الأقسام والفرق.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="b3ae7-111">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="b3ae7-112">إنشاء تدرج هرمي</span><span class="sxs-lookup"><span data-stu-id="b3ae7-112">Create a hierarchy</span></span>
1. <span data-ttu-id="b3ae7-113">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المؤسسة > المؤسسات > التدرجات الهرمية للمؤسسات**.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="b3ae7-114">انقر فوق **جديد** في **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="b3ae7-115">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="b3ae7-116">في قسم **الغرض**، انقر فوق **تعيين غرض‬**.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="b3ae7-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="b3ae7-118">حدد غرضًا للتعيين إلى التدرج الهرمي للمؤسسات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="b3ae7-119">في قسم **التدرجات الهرمية المعينة‬**، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-119">In the **Assigned hierarchies** section, click **Add**.</span></span>
7. <span data-ttu-id="b3ae7-120">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-120">In the list, mark the selected row.</span></span> <span data-ttu-id="b3ae7-121">ابحث عن التدرج الهرمي الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="b3ae7-122">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="b3ae7-123">إضافة مؤسسات إلى التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="b3ae7-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="b3ae7-124">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="b3ae7-125">قم بتحديد التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="b3ae7-126">في قسم **التدرجات الهرمية المعينة**، انقر فوق **عرض التدرج الهرمي**.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="b3ae7-127">قم بإضافة المؤسسات، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="b3ae7-128">لإضافة مؤسسة، انقر فوق **تحرير** ثم فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="b3ae7-129">عند الانتهاء من إجراء التغييرات، يمكنك **حفظ** مسودة و/أو **نشر** التغييرات.</span><span class="sxs-lookup"><span data-stu-id="b3ae7-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]