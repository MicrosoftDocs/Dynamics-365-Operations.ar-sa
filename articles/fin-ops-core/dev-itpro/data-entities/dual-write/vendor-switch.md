---
title: التبديل بين تصميمات المورّدين
description: يصف هذا الموضوع كيفية التبديل بين تكامل بيانات البائع وبين تطبيقات Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 587a9b98f28b11e303aff4b59e9726f220d956eb
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019613"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="8cfb4-103">التبديل بين تصميمات المورّدين</span><span class="sxs-lookup"><span data-stu-id="8cfb4-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="8cfb4-104">تدفق بيانات المورّد</span><span class="sxs-lookup"><span data-stu-id="8cfb4-104">Vendor data flow</span></span> 

<span data-ttu-id="8cfb4-105">إذا كنت تستخدم تطبيقات Dynamics 365 الأخرى لإدارة المورّدين، وأردت عزل معلومات المورّد عن العملاء، فاستخدم تصميم المورّد الأساسي هذا.</span><span class="sxs-lookup"><span data-stu-id="8cfb4-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![تدفق المورد الأساسي](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="8cfb4-107">إذا كنت تستخدم تطبيقات Dynamics 365 الأخرى لإدارة المورّدين، وأردت متابعة استخدام كيان **الحساب** لتخزين معلومات المورّدين، فاستخدم تصميم المورّد الموسع هذا.</span><span class="sxs-lookup"><span data-stu-id="8cfb4-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="8cfb4-108">في هذا التصميم، يتم تخزين معلومات المورد الموسعة مثل حالة انتظار المورد وملف تعريف المورد في كيان **الموردين** في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8cfb4-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![تدفق المورّد الموسّع](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="8cfb4-110">اتبع الخطوات المذكورة أدناه لاستخدام تصميم المورد الموسع:</span><span class="sxs-lookup"><span data-stu-id="8cfb4-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="8cfb4-111">تحتوي حزمة حل **SupplyChainCommon** على قوالب عملية سير العمل كما هو موضح في الصورة التالية.</span><span class="sxs-lookup"><span data-stu-id="8cfb4-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8cfb4-112">![قوالب عمليات سير العمل](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="8cfb4-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="8cfb4-113">أنشئ عمليات سير عمل جديدة باستخدام قوالب عملية سير العمل:</span><span class="sxs-lookup"><span data-stu-id="8cfb4-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="8cfb4-114">أنشئ عملية سير عمل جديدة لكيان **المورد** باستخدام قالب عملية سير عمل **إنشاء الموردين في كيان الحساب** وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8cfb4-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="8cfb4-115">يعالج سير العمل هذا سيناريو إنشاء المورد لكيان **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="8cfb4-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="8cfb4-116">![إنشاء موردين في كيان الحساب](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="8cfb4-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="8cfb4-117">أنشئ عملية سير عمل جديدة لكيان **المورد** باستخدام قالب عملية سير عمل **تحديث كيان الحسابات** وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8cfb4-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="8cfb4-118">يعالج سير العمل هذا سيناريو تحديث المورد لكيان **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="8cfb4-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="8cfb4-119">![تحديث كيان الحسابات](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="8cfb4-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="8cfb4-120">أنشئ عمليات سير عمل جديدة من القوالب التي تم إنشاؤها في كيان **الحسابات**.</span><span class="sxs-lookup"><span data-stu-id="8cfb4-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="8cfb4-121">![إنشاء موردين في كيان الموردين](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="8cfb4-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="8cfb4-122">![تحديث كيان الموردين](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="8cfb4-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="8cfb4-123">يمكنك تكوين مهام سير العمل بمثابه الوقت الحقيقي أو مهام سير العمل الخلفية وفقًا لمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="8cfb4-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="8cfb4-124">![التحويل إلى سير عمل في الخلفية](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="8cfb4-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="8cfb4-125">قم بتنشيط عمليات سير العمل التي قمت بإنشائها في كياني **الحساب** و **المورد** لبدء استخدام كيان **الحساب** لتخزين معلومات المورد.</span><span class="sxs-lookup"><span data-stu-id="8cfb4-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
