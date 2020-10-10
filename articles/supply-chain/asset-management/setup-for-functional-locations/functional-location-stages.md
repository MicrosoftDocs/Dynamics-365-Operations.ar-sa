---
title: حالات دورة حياة موقع العمل
description: يصف هذا الموضوع كيفية إعداد حالات موقع العمل ونماذج دورة الحياة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eedc21dde32671b4f5539ac4e798a8e1329c191
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/25/2020
ms.locfileid: "3890096"
---
# <a name="functional-location-lifecycle-states"></a><span data-ttu-id="ce374-103">حالات دورة حياة موقع العمل</span><span class="sxs-lookup"><span data-stu-id="ce374-103">Functional location lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ce374-104">يصف هذا الموضوع كيفية إعداد حالات دور حياة موقع العمل ونماذج دورة الحياة في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="ce374-104">This topic describes how to set up functional location lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="ce374-105">تحدد حالات دورة حياة موقع العمل الحالات التي يمكن أن يمر بها موقع العمل، على سبيل المثال، تم إنشاؤه ونشط ومنتهٍ.</span><span class="sxs-lookup"><span data-stu-id="ce374-105">Functional location lifecycle states define the states that a functional location can go through, for example, created, active, and ended.</span></span> <span data-ttu-id="ce374-106">يمكنك عرض كافة مواقع العمل، بغض النظر عن حالة دورة حياتها في صفحة قائمة **جميع مواقع العمل‬**.</span><span class="sxs-lookup"><span data-stu-id="ce374-106">You are able to view all functional locations, regardless of their lifecycle state, in the **All functional locations** list page.</span></span> <span data-ttu-id="ce374-107">يمكنك تغيير حالة موقع عمل عن طريق تحديده في صفحة قائمة **جميع مواقع العمل** وتحديد **تحديث حالة موقع العمل**.</span><span class="sxs-lookup"><span data-stu-id="ce374-107">You can change the state of a functional location by selecting it in the **All functional locations** list page and selecting **Update functional location state**.</span></span>

## <a name="set-up-functional-location-lifecycle-states"></a><span data-ttu-id="ce374-108">إعداد حالات دورة حياة مواقع العمل</span><span class="sxs-lookup"><span data-stu-id="ce374-108">Set up functional location lifecycle states</span></span>

1. <span data-ttu-id="ce374-109">حدد **إدارة الأصول** > **الإعداد** > **مواقع العمل** > **حالات دورة الحياة.**.</span><span class="sxs-lookup"><span data-stu-id="ce374-109">Select **Asset management** > **Setup** > **Functional locations** > **Lifecycle states**.</span></span>
2. <span data-ttu-id="ce374-110">حدد **جديد** لإنشاء حالة موقع عمل جديدة.</span><span class="sxs-lookup"><span data-stu-id="ce374-110">Select **New** to create a new functional location state.</span></span>
3. <span data-ttu-id="ce374-111">أدخل معرف الحالة في حقل **حالة دورة الحياة**، وأدخل اسمًا لحالة موقع العمل في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="ce374-111">Insert the state ID in the **Lifecycle state** field and a name for the functional location state in the **Name** field.</span></span> <span data-ttu-id="ce374-112">في الحقل **نماذج دورة الحياة**، يمكنك رؤية عدد نماذج دورة حياة مواقع العمل التي تستخدم حالة موقع العمل.</span><span class="sxs-lookup"><span data-stu-id="ce374-112">In the **Lifecycle models** field, you can see the number of functional location lifecycle models that uses the functional location state.</span></span>
4. <span data-ttu-id="ce374-113">على علامة التبويب السريعة **عام**، حدد "نعم" على زر التبديل **نشط**، إذا كان يجب أن يكون موقع العمل نشطًا في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="ce374-113">On the **General** FastTab, select "Yes" on the **Active** toggle button if the functional location should be active at this state.</span></span>
5. <span data-ttu-id="ce374-114">حدد "نعم" على زر التبديل **إنشاء أصول** إذا كان من الممكن إنشاء أصل بنفس اسم موقع العمل بشكل تلقائي وتثبيته على موقع العمل في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="ce374-114">Select "Yes" on the **Create assets** toggle button if it should be possible to automatically create an asset with the same name as the functional location and install it on the functional location at this state.</span></span>  
>[!NOTE]
><span data-ttu-id="ce374-115">يرتبط زر التبديل هذا بالحقل **نوع الأصل** على علامة التبويب السريعة **عام** في النموذج **أنواع مواقع العمل** (**إدارة الأصول** > **الإعداد** > **مواقع العمل** > **أنواع مواقع العمل**).</span><span class="sxs-lookup"><span data-stu-id="ce374-115">This toggle button relates to the **Asset type** field on the **General** FastTab in the **Functional location types** form (**Asset management** > **Setup** > **Functional locations** > **Functional location types**).</span></span>
6. <span data-ttu-id="ce374-116">حدد "نعم" على زر التبديل **إعادة تسمية** إذا كان يجب أن يكون من الممكن تغيير اسم موقع العمل في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="ce374-116">Select "Yes" on the **Rename location** toggle button if it should be possible to change the name of the functional location at this state.</span></span>
7. <span data-ttu-id="ce374-117">حدد "نعم" على زر التبديل **مواقع فرعية جديدة** إذا كان يجب أن يكون من الممكن إضافة مواقع فرعية جديدة إلى موقع العمل في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="ce374-117">Select "Yes" on the **New sub locations** toggle button if it should be possible to add new sub locations to the functional location at this state.</span></span>
8. <span data-ttu-id="ce374-118">حدد "نعم" على زر التبديل **تثبيت الأصول** إذا كان يجب أن يكون من الممكن تثبيت أصول على موقع العمل في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="ce374-118">Select "Yes" on the **Install assets** toggle button if it should be possible to install assets on the functional location at this state.</span></span>
9. <span data-ttu-id="ce374-119">حدد "نعم" على زر التبديل **حذف موقع العمل** إذا كان يجب أن يكون من الممكن حذف موقع العمل في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="ce374-119">Select "Yes" on the **Delete functional location** toggle button if it should be possible to delete the functional location at this state.</span></span>
10. <span data-ttu-id="ce374-120">حدد حالة أصل في حقل **حالة دورة الحياة** إذا كنت تريد تحديث حالة دورة حياة الأصل لجميع الأصول المثبتة في موقع العمل بشكل تلقائي في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="ce374-120">Select an asset state in the **Lifecycle state** field if you want the asset lifecycle state for all assets installed on the functional location to be automatically updated at this state.</span></span> <span data-ttu-id="ce374-121">على سبيل المثال: إذا قمت بإغلاق موقع عمل، ثم قمت بتعيين حالة دورة حياة موقع العمل إلى "منتهٍ"، فقد تحتاج إلى تغيير حالة دورة حياة الأصول المثبتة في نوقع العمل هذا بشكل تلقائي إلى "غير مستخدم".</span><span class="sxs-lookup"><span data-stu-id="ce374-121">Example: If you close down a functional location, and set the functional location lifecycle state to "Ended", you may want to automatically change the lifecycle state of the assets installed on that functional location to "Not in use".</span></span>


>[!NOTE]
><span data-ttu-id="ce374-122">ترتبط حالات دورة حياة موقع العمل وأنواع ونماذج دورة الحياة ببعضها، ويتم استخدامها بالطريقة نفسها كحالات دورة حياة أمر عمل ونماذج حياة أمر العمل وأنواع أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="ce374-122">Functional location lifecycle states, lifecycle models, and types are related and used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 

## <a name="set-up-functional-location-lifecycle-models"></a><span data-ttu-id="ce374-123">إعداد نماذج دورة حياة مواقع العمل</span><span class="sxs-lookup"><span data-stu-id="ce374-123">Set up functional location lifecycle models</span></span>

<span data-ttu-id="ce374-124">عند إنشاء حالات دورة الحياة المطلوبة لمواقع العمل، يمكن تقسيمها إلى مجموعات.</span><span class="sxs-lookup"><span data-stu-id="ce374-124">When you have created the lifecycle states required for your functional locations, they can be divided into groups.</span></span> <span data-ttu-id="ce374-125">ويتم ذلك لإنشاء سير مهام نموذج دورة الحياة الذي يمكن استخداما لأنواع مختلفة من مواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="ce374-125">This is done to create the lifecycle model flow that may be used for different types of functional locations.</span></span> <span data-ttu-id="ce374-126">كحد أدنى، يجب إنشاء نموذج دورة حياة موقع عمل قياسي واحد.</span><span class="sxs-lookup"><span data-stu-id="ce374-126">As a minimum, one standard functional location lifecycle model should be created.</span></span>

1. <span data-ttu-id="ce374-127">حدد **إدارة الأصول** > **الإعداد** > **مواقع العمل** > **نماذج دورة الحياة.**.</span><span class="sxs-lookup"><span data-stu-id="ce374-127">Select **Asset management** > **Setup** > **Functional locations** > **Lifecycle models**.</span></span>
2. <span data-ttu-id="ce374-128">حدد **جديد** لإنشاء نموذج دورة حياة جديد.</span><span class="sxs-lookup"><span data-stu-id="ce374-128">Select **New** to create a new lifecycle model.</span></span>
3. <span data-ttu-id="ce374-129">أدخل معرف نموذج دورة الحياة في حقل **نموذج دورة الحياة**، وأدخل اسمًا لنموذج دورة الحياة في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="ce374-129">Insert the lifecycle model ID in the **Lifecycle model** field and a name for the lifecycle model in the **Name** field.</span></span> <span data-ttu-id="ce374-130">في الحقلين **أنواع مواقع العمل** و**حالات دورة الحياة**، يمكنك رؤية عدد أنواع مواقع العمل التي تستخدم نموذج دورة الحياة وعدد الحالات المحددة في نموذج دورة الحياة.</span><span class="sxs-lookup"><span data-stu-id="ce374-130">In the **Functional location types** and **Lifecycle states** fields, you can see the number of functional location types that uses the lifecycle model and the number of states selected in the lifecycle model.</span></span>
4. <span data-ttu-id="ce374-131">على علامة التبويب السريعة **حالات دورة الحياة**، حدد الحالات التي يجب تضمينها في النموذج.</span><span class="sxs-lookup"><span data-stu-id="ce374-131">On the **Lifecycle states** FastTab, select the states that should be included in the model.</span></span> <span data-ttu-id="ce374-132">ويتم ذلك بالنقر فوق حالة في القسم **دورة الحياة المتبقية** والنقر فوق زر ![السهم للأمام](media/02-setup-for-functional-locations.png).</span><span class="sxs-lookup"><span data-stu-id="ce374-132">This is done by clicking on a state in the **Lifecycle states remaining** section and clicking the ![forward arrow](media/02-setup-for-functional-locations.png) button.</span></span>
5. <span data-ttu-id="ce374-133">إذا كنت ترغب في تحديد كافة الحالات المتوفرة لنموذج، فانقر فوق الزر ![تحديد جميع المراحل المتوفرة](media/03-setup-for-functional-locations.png).</span><span class="sxs-lookup"><span data-stu-id="ce374-133">If you want to select all the available states for a model, click the ![select all available stages](media/03-setup-for-functional-locations.png) button.</span></span> <span data-ttu-id="ce374-134">يتم نقل جميع الحالات إلى القسم **حالات دورة الحياة المحددة**.</span><span class="sxs-lookup"><span data-stu-id="ce374-134">All states are transferred to the **Lifecycle states selected** section.</span></span>
6. <span data-ttu-id="ce374-135">إذا كنت ترغب في إزالة حالة محددة من النموذج، فحدد الحالة في القسم **حالات دورة الحياة المحددة** ثم حدد الزر ![سهم للخلف](media/04-setup-for-functional-locations.png).</span><span class="sxs-lookup"><span data-stu-id="ce374-135">If you want to remove a selected state from the model, select the state in the **Lifecycle states selected** section and then select the ![back arrow](media/04-setup-for-functional-locations.png) button.</span></span>
7. <span data-ttu-id="ce374-136">حدد **تحديثات حالة دورة الحياة** لتحديد حالات دورة الحياة التي يمكنها أن تتبع حالة محددة.</span><span class="sxs-lookup"><span data-stu-id="ce374-136">Select **Lifecycle state updates** to define which lifecycle states can follow a selected state.</span></span>
