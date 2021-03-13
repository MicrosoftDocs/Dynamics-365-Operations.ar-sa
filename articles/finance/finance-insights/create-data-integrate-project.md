---
title: إنشاء مشروع موحد البيانات (معاينة)
description: يشرح هذا الموضوع كيفية إنشاء مشروع موحد البيانات.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0029e093f524c61ff17a480ee3b881b3994ba95a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009433"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="5256f-103">إنشاء مشروع موحد البيانات (معاينة)</span><span class="sxs-lookup"><span data-stu-id="5256f-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="5256f-104">يشرح هذا الموضوع كيفية إنشاء مشروع موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="5256f-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="5256f-105">تسجيل الدخول إلى Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="5256f-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="5256f-106">انتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد **كيانات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="5256f-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="5256f-107">انتظر حتى يتم تحديث كافة كيانات البيانات قبل الانتقال إلى الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="5256f-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="5256f-108">افتح مدخل [Power Apps ](https://make.powerapps.com/)، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5256f-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="5256f-109">حدد البيئة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="5256f-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="5256f-110">في جزء التنقل الأيسر، حدد **البيانات \> الاتصالات**.</span><span class="sxs-lookup"><span data-stu-id="5256f-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="5256f-111">الاتصال بالمثيلات المناسبة للعناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="5256f-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="5256f-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5256f-112">Dynamics 365</span></span>
        - <span data-ttu-id="5256f-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="5256f-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="5256f-114">افتح البيئات [Power Apps ](https://admin.powerapps.com/environments)، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5256f-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="5256f-115">حدد **موحد البيانات**.</span><span class="sxs-lookup"><span data-stu-id="5256f-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="5256f-116">حدد **مجموعات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="5256f-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="5256f-117">حدد **مجموعة اتصال جديدة**.</span><span class="sxs-lookup"><span data-stu-id="5256f-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="5256f-118">أدخل اسمًا للاتصال.</span><span class="sxs-lookup"><span data-stu-id="5256f-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="5256f-119">حدد الاتصالات المناسبة للأصناف التالية:</span><span class="sxs-lookup"><span data-stu-id="5256f-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="5256f-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5256f-120">Dynamics 365</span></span>
        - <span data-ttu-id="5256f-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="5256f-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="5256f-122">حدد تعيين المؤسسة المناسب.</span><span class="sxs-lookup"><span data-stu-id="5256f-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="5256f-123">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="5256f-123">Select **Create**.</span></span>

5. <span data-ttu-id="5256f-124">افتح البيئات [Power Apps ](https://admin.powerapps.com/environments)، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5256f-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="5256f-125">إنشاء مشاريع تكامل البيانات للقوالب التالية باستخدام مجموعة الاتصال التي قمت بإنشائها:</span><span class="sxs-lookup"><span data-stu-id="5256f-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="5256f-126">نتائج معلومات الدفع الخاصة بالعميل (CDS لـ Fin وOps)</span><span class="sxs-lookup"><span data-stu-id="5256f-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="5256f-127">نتائج السلسلة الزمنية للتدفق النقدي (CDS لـ Fin وOps)</span><span class="sxs-lookup"><span data-stu-id="5256f-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="5256f-128">نتائج السلسلة الزمنية للموازنة (CDS لـ Fin وOps)</span><span class="sxs-lookup"><span data-stu-id="5256f-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="5256f-129">قم بتعيين الجدولة المناسبة لكل مشروع.</span><span class="sxs-lookup"><span data-stu-id="5256f-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="5256f-130">في حالة عدم رؤية الكيانات المطلوبة في CDS، الرجاء الانتقال إلى **عمليات التحصيل والائتمان > الضبط > Finance Insights > معلمات Finance insights**، قم بتمكين ميزة توقعات دفع العميل وانقر فوق الزر **إنشاء نموذج توقع**.</span><span class="sxs-lookup"><span data-stu-id="5256f-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="5256f-131">عند اكتمال نشر نموذج AI (ناجح أو فاشل)، فإنه سيتم نشر كيانات CDS المطلوبة لإنشاء تكامل في CDS.</span><span class="sxs-lookup"><span data-stu-id="5256f-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="5256f-132">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="5256f-132">Privacy notice</span></span>

<span data-ttu-id="5256f-133">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="5256f-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
