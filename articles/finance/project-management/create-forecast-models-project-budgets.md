---
title: إنشاء طرز تنبؤ لموازنات المشاريع
description: يوضح هذا الموضوع كيفيه إنشاء نموذج تنبؤ للموازنات المتبقية.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321769"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="2ed74-103">إنشاء طرز تنبؤ لموازنات المشاريع</span><span class="sxs-lookup"><span data-stu-id="2ed74-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ed74-104">يوضح هذا الموضوع كيفيه إنشاء نموذج تنبؤ للموازنات المتبقية.</span><span class="sxs-lookup"><span data-stu-id="2ed74-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="2ed74-105">يستخدم المشروع الخاضع لتحكم الموازنة نوعين من الموازنات: الموازنة الأصلية والموازنة المتبقية.</span><span class="sxs-lookup"><span data-stu-id="2ed74-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="2ed74-106">عندما تقوم بإنشاء موازنة المشروع، يجب عليك تحديد نماذج تنبؤ الموازنة الأصلية والمتبقية التي تم إنشاؤها في صفحة **‏‫نماذج التنبؤ‬**.</span><span class="sxs-lookup"><span data-stu-id="2ed74-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="2ed74-107">موازنات المشروع المستندة إلى النماذج المحددة يتم إنشاؤها عند تنفيذ موازنة المشروع.</span><span class="sxs-lookup"><span data-stu-id="2ed74-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="2ed74-108">لا يمكن أن يحتوي نموذج التنبؤ المستخدم لتحكم الموازنة على نموذج فرعي، ولا يمكن استخدامه كنموذج فرعي.</span><span class="sxs-lookup"><span data-stu-id="2ed74-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="2ed74-109">حدد **‫إدارة المشاريع ومحاسبتها‬** > **الإعداد** > **‏‫التنبؤات‬**  > **‏‫نماذج التنبؤ‬**.</span><span class="sxs-lookup"><span data-stu-id="2ed74-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="2ed74-110">حدد **جديد** لإنشاء نموذج تنبؤ جديد، ثم أدخل رقم معرف نموذج واسمًا للنموذج الجديد.</span><span class="sxs-lookup"><span data-stu-id="2ed74-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="2ed74-111">قم بتعيين خيار **موقوف‬** إلى **نعم** لمنع إيه تغييرات في بنود التنبؤ الخاصة بنموذج التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="2ed74-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="2ed74-112">إذا كان ينبغي أن تقوم بنود التنبؤ المرتبطة بالنموذج بإنشاء تقديرات التدفقات النقدية في دفتر الأستاذ العام، فحدد **‏‫تضمين في تقديرات تدفق النقد‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="2ed74-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="2ed74-113">لاستخدام تاريخ المشروع كتاريخ فاتورة، قم بتعيين **تاريخ فاتورة التنبؤ** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="2ed74-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="2ed74-114">من الحقل **نوع الموازنة** حدد أحد أنواع النماذج التالية:</span><span class="sxs-lookup"><span data-stu-id="2ed74-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="2ed74-115">**الموازنة الأصلية**: استخدم نوع النموذج هذا لمبالغ الموازنة الأصلية التي يتم تنفيذها عند إنشاء الموازنة الأولية واعتمادها.</span><span class="sxs-lookup"><span data-stu-id="2ed74-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="2ed74-116">**الموازنة المتبقية**: استخدم نوع النموذج هذا لمبالغ الموازنة المتبقية أثناء مدة المشروع.</span><span class="sxs-lookup"><span data-stu-id="2ed74-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="2ed74-117">ويتم تقليل الارصدة الموجودة في نموذج التنبؤ هذا بواسطة الحركات الحقيقية، ويتم زيادتها أو تقليلها بواسطة مراجعات الموازنة.</span><span class="sxs-lookup"><span data-stu-id="2ed74-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="2ed74-118">**‏‫موازنة محولة‬**: استخدم نوع النموذج هذا لمبالغ الموازنة المحولة للمشروع.</span><span class="sxs-lookup"><span data-stu-id="2ed74-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="2ed74-119">التحويل هو علية اختيارية يمكن تشغيلها لنقل مبالغ الموازنة غير المستخدمة من سنة مالية إلى سنة مالية أخرى.</span><span class="sxs-lookup"><span data-stu-id="2ed74-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="2ed74-120">قم بضبط الخيارات التالية كما هو مطلوب:</span><span class="sxs-lookup"><span data-stu-id="2ed74-120">Set the following options as required:</span></span>

   - <span data-ttu-id="2ed74-121">قم بتمكين **تاريخ فاتورة التنبؤ** لاستخدام تاريخ المشروع كتاريخ فاتورة.</span><span class="sxs-lookup"><span data-stu-id="2ed74-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="2ed74-122">قم بتمكين **التنبؤ مع WIP** للتنبؤ استنادا إلى العمل الجاري (WIP) ، ثم تحديد نوع WIP.</span><span class="sxs-lookup"><span data-stu-id="2ed74-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="2ed74-123">يمكنك الاحتفاظ **بنوع الموازنة** الافتراضي على **بلا** أو إدخال نوع جديد.</span><span class="sxs-lookup"><span data-stu-id="2ed74-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="2ed74-124">لا يمكن تغيير نوع الموازنة بعد تغيير أحد السجلات.</span><span class="sxs-lookup"><span data-stu-id="2ed74-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="2ed74-125">إذا قمت بتغيير نوع الموازنة الافتراضي، لن تكون كافة الخيارات الأخرى متاحه للتحديثات، ولا يمكنك إعاده استخدام نموذج التنبؤ هذا.</span><span class="sxs-lookup"><span data-stu-id="2ed74-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

