--- 
title: "إضافة نشاط موجود إلى إصدار تدفق الإنتاج"
description: "عند إنشاء إصدارات جديدة من تدفقات الإنتاج، يمكنك أن تختار إضافة أنشطة تم إنشاؤها للإصدارات القديمة إلى الإصدار الجديد."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a74fb34db71ba4b539c1b6ede361329aaeb94920
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="07297-103">إضافة نشاط موجود إلى إصدار تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="07297-103">Add an existing activity to a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07297-104">عند إنشاء إصدارات جديدة من تدفقات الإنتاج، يمكنك أن تختار إضافة أنشطة تم إنشاؤها للإصدارات القديمة إلى الإصدار الجديد.</span><span class="sxs-lookup"><span data-stu-id="07297-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="07297-105">يوضح هذا الإجراء كيفية إنشاء إصدار جديد لتدفق إنتاج موجود، دون نسخ الأنشطة.</span><span class="sxs-lookup"><span data-stu-id="07297-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="07297-106">في الخطوة التالية، يُضاف نشاط موجود إلى الإصدار الجديد.</span><span class="sxs-lookup"><span data-stu-id="07297-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="07297-107">تتطلب هذه المهمة تدفق الإنتاج مع الإصدار والأنشطة التي تم إنشاؤها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="07297-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="07297-108">إنشاء إصدار تدفق إنتاج جديد</span><span class="sxs-lookup"><span data-stu-id="07297-108">Create a new production flow version</span></span>
1. <span data-ttu-id="07297-109">انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="07297-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="07297-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="07297-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="07297-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="07297-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="07297-112">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="07297-112">Click Edit.</span></span>
5. <span data-ttu-id="07297-113">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="07297-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="07297-114">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="07297-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="07297-115">قبل إنشاء إصدار تدفق إنتاج جديد، تأكد من التحقق من تاريخ ووقت انتهاء صلاحية الإصدار النشط.</span><span class="sxs-lookup"><span data-stu-id="07297-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="07297-116">سيتم إنشاء الإصدار الجديد مع تاريخ بدء السريان، وهو يتصل بتاريخ انتهاء صلاحية الإصدار المحدد.</span><span class="sxs-lookup"><span data-stu-id="07297-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="07297-117">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="07297-117">Click Add.</span></span>
8. <span data-ttu-id="07297-118">حدد "لا" في الحقل "نسخة من الإصدار".</span><span class="sxs-lookup"><span data-stu-id="07297-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="07297-119">حدد "لا" للبدء بإصدار فارغ إذا كان سيتم استبدال معظم الأنشطة للإصدار المنسوخ بأنشطة جديدة.</span><span class="sxs-lookup"><span data-stu-id="07297-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="07297-120">أضف الأنشطة التي لم يطرأ عليها تغيير إلى الوظيفة "إضافة موجود‬" في نموذج النشاط يدويًا.</span><span class="sxs-lookup"><span data-stu-id="07297-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="07297-121">حدد "لا" في الحقل "تكرار قواعد كانبان‬".</span><span class="sxs-lookup"><span data-stu-id="07297-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="07297-122">عندما لا يتم نسخ الأنشطة إلى الإصدار الجديد، سيتعذر نسخ قواعد كانبان في وقت إنشاء الإصدار الجديد.</span><span class="sxs-lookup"><span data-stu-id="07297-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="07297-123">بدلاً من ذلك، ستستخدم وظيفة إنشاء كانبان بديل لاحقًا في نموذج قاعدة كانبان، لاستبدال قواعد كانبان لإصدار تدفق الإنتاج القديم بقواعد كانبان التي تستخدم أنشطة الإصدار الجديد.</span><span class="sxs-lookup"><span data-stu-id="07297-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="07297-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="07297-124">Click OK.</span></span>
11. <span data-ttu-id="07297-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="07297-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="07297-126">إضافة نشاط موجود</span><span class="sxs-lookup"><span data-stu-id="07297-126">Add an existing activity</span></span>
1. <span data-ttu-id="07297-127">انقر فوق "الأنشطة".</span><span class="sxs-lookup"><span data-stu-id="07297-127">Click Activities.</span></span>
2. <span data-ttu-id="07297-128">انقر فوق "إضافة موجود" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="07297-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="07297-129">ابحث عن نشاط موجود وحدده لإضافته إلى إصدار تدفق الإنتاج الجديد.</span><span class="sxs-lookup"><span data-stu-id="07297-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="07297-130">لاحظ أن القائمة تعرض كافة الأنشطة التي تم إنشاؤها لتدفق الإنتاج هذا لكافة الإصدارات السابقة من التدفق.</span><span class="sxs-lookup"><span data-stu-id="07297-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="07297-131">في حقل "النشاط"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="07297-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="07297-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="07297-132">Click OK.</span></span>

