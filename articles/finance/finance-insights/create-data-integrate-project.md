---
title: إنشاء مشروع موحد البيانات (معاينة)
description: يشرح هذا الموضوع كيفية إنشاء مشروع موحد البيانات.
author: ShivamPandey-msft
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9ecf6ef7b7f052ebbb1201dcd04a7431f5b72ce5
ms.sourcegitcommit: b64c52d85aa6f110f3b1959a5521637dd8631b5b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867437"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="34f98-103">إنشاء مشروع موحد البيانات (معاينة)</span><span class="sxs-lookup"><span data-stu-id="34f98-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="34f98-104">يشرح هذا الموضوع كيفية إنشاء مشروع موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="34f98-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="34f98-105">تسجيل الدخول إلى Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="34f98-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="34f98-106">انتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد **كيانات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="34f98-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="34f98-107">انتظر حتى يتم تحديث كافة كيانات البيانات قبل الانتقال إلى الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="34f98-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="34f98-108">افتح مدخل [Power Apps ](https://make.powerapps.com/)، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="34f98-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="34f98-109">حدد البيئة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="34f98-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="34f98-110">في جزء التنقل الأيسر، حدد **البيانات \> الاتصالات**.</span><span class="sxs-lookup"><span data-stu-id="34f98-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="34f98-111">الاتصال بالمثيلات المناسبة للعناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="34f98-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="34f98-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="34f98-112">Dynamics 365</span></span>
        - <span data-ttu-id="34f98-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="34f98-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="34f98-114">افتح البيئات [Power Apps ](https://admin.powerapps.com/environments)، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="34f98-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="34f98-115">حدد **موحد البيانات**.</span><span class="sxs-lookup"><span data-stu-id="34f98-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="34f98-116">حدد **مجموعات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="34f98-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="34f98-117">حدد **مجموعة اتصال جديدة**.</span><span class="sxs-lookup"><span data-stu-id="34f98-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="34f98-118">أدخل اسمًا للاتصال.</span><span class="sxs-lookup"><span data-stu-id="34f98-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="34f98-119">حدد الاتصالات المناسبة للأصناف التالية:</span><span class="sxs-lookup"><span data-stu-id="34f98-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="34f98-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="34f98-120">Dynamics 365</span></span>
        - <span data-ttu-id="34f98-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="34f98-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="34f98-122">حدد تعيين المؤسسة المناسب.</span><span class="sxs-lookup"><span data-stu-id="34f98-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="34f98-123">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="34f98-123">Select **Create**.</span></span>

5. <span data-ttu-id="34f98-124">افتح البيئات [Power Apps ](https://admin.powerapps.com/environments)، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="34f98-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="34f98-125">إنشاء مشاريع تكامل البيانات للقوالب التالية باستخدام مجموعة الاتصال التي قمت بإنشائها:</span><span class="sxs-lookup"><span data-stu-id="34f98-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="34f98-126">نتائج معلومات الدفع الخاصة بالعميل (CDS لـ Fin وOps)</span><span class="sxs-lookup"><span data-stu-id="34f98-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="34f98-127">إذا كنت تستخدم الإصدار 10.0.17 أو إصدار أحدث، ستحتاج إلى استخدام القالب المسمى، نتيجة الرؤى لمدفوعات العميل (CDS إلى Fin and Ops 10.0.17+).</span><span class="sxs-lookup"><span data-stu-id="34f98-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="34f98-128">نتائج السلسلة الزمنية للتدفق النقدي (CDS لـ Fin وOps)</span><span class="sxs-lookup"><span data-stu-id="34f98-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="34f98-129">نتائج السلسلة الزمنية للموازنة (CDS لـ Fin وOps)</span><span class="sxs-lookup"><span data-stu-id="34f98-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="34f98-130">قم بتعيين الجدولة المناسبة لكل مشروع.</span><span class="sxs-lookup"><span data-stu-id="34f98-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="34f98-131">في حالة عدم رؤية الكيانات المطلوبة في CDS، الرجاء الانتقال إلى **عمليات التحصيل والائتمان > الضبط > Finance Insights > معلمات Finance insights**، قم بتمكين ميزة توقعات دفع العميل وانقر فوق الزر **إنشاء نموذج توقع**.</span><span class="sxs-lookup"><span data-stu-id="34f98-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="34f98-132">عند اكتمال نشر نموذج AI (ناجح أو فاشل)، فإنه سيتم نشر كيانات CDS المطلوبة لإنشاء تكامل في CDS.</span><span class="sxs-lookup"><span data-stu-id="34f98-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="34f98-133">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="34f98-133">Privacy notice</span></span>

<span data-ttu-id="34f98-134">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="34f98-134">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
