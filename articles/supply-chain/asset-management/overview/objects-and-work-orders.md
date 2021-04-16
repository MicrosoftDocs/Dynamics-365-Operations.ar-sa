---
title: الأصول وأوامر العمل
description: يشرح هذا الموضوع الأصول وأوامر العمل في إدارة الأصول.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2fe5523edf46712b17aa7abcad50da44c3eaffd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816738"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="b8e97-103">الأصول وأوامر العمل</span><span class="sxs-lookup"><span data-stu-id="b8e97-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b8e97-104">يشرح هذا الموضوع الأصول وأوامر العمل في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="b8e97-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="b8e97-105">تعتبر الأصول وأوامر العمل الأجزاء الرئيسية من إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="b8e97-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="b8e97-106">*الأصل* هو جزء من جهاز أو جهاز يحتاج إلى الصيانة والخدمة بشكل مستمر.</span><span class="sxs-lookup"><span data-stu-id="b8e97-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="b8e97-107">يمكن إنشاء الأصول في بنية هرمية، ويمكن ربطها بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="b8e97-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="b8e97-108">يمكن التخطيط لمهام الصيانة على جميع المستويات في بنية الأصل.</span><span class="sxs-lookup"><span data-stu-id="b8e97-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="b8e97-109">يتم إعداد بيانات مختلفة، مثل معلومات المنتج ومواصفات الأصل وخطط الصيانة المطلوبة على كل أصل.</span><span class="sxs-lookup"><span data-stu-id="b8e97-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="b8e97-110">يتضمن الرسم التوضيحي التالي نظرة عامة على بيانات الأصول وارتباط الأصول بأنواع الوظائف.</span><span class="sxs-lookup"><span data-stu-id="b8e97-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="b8e97-111">يتم استخدام النص الأحمر للأمثلة التي تظهر التوارث والتبعيات.</span><span class="sxs-lookup"><span data-stu-id="b8e97-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![رسم تخطيطي يوضح بيانات الأصول المرتبطة بأنواع الوظائف](media/05-overview-image.png)

<span data-ttu-id="b8e97-113">كل أمر عمل له نوع أمر عمل، مثل الصيانة الوقائية، أو الصيانة التصحيحية، أو التفتيش.</span><span class="sxs-lookup"><span data-stu-id="b8e97-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="b8e97-114">يحتوي أمر العمل على وظيفة واحدة أو أكثر من وظائف أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="b8e97-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="b8e97-115">وتحدد كل وظيفة أمر عمل وظيفة يجب تنفيذها على أصل ونوع وظيفة ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="b8e97-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="b8e97-116">ومن الأمثلة على أنواع الوظائف ذات الصلة 000 10 كيلومتر، و000 50 كيلومتر، وإصلاح شامل لمدة سنة واحدة، وفحص للسلامة.</span><span class="sxs-lookup"><span data-stu-id="b8e97-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="b8e97-117">بإمكان أمر عمل واحد أن يرتبط بأصول متعددة.</span><span class="sxs-lookup"><span data-stu-id="b8e97-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="b8e97-118">يقدم الرسم التوضيحي التالي نظرة عامة على البيانات الرئيسية في أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="b8e97-118">The following illustration shows an overview of the key data in a work order.</span></span>

![رسم تخطيطي يوضح البيانات الأساسية في أمر عمل](media/06-overview-image.png)

<span data-ttu-id="b8e97-120">بإمكان أمر عمل أن يرتبط بأمر عمل آخر، وبإمكان أنواع الوظائف أن تحتوي على وظائف ناجحة تقوم بإنشاء أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="b8e97-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="b8e97-121">بشكل عام، لا توجد تبعيات بين أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="b8e97-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="b8e97-122">وبالتالي، يمكنها تغيير حالة دورة حياة أمر العمل، ويمكن جدولتها بشكل مستقل عن بعضها البعض.</span><span class="sxs-lookup"><span data-stu-id="b8e97-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="b8e97-123">يمكن إنشاء أوامر العمل بطرق مختلفة تتعلق بالصيانة التصحيحية أو الوقائية أو التفاعلية.</span><span class="sxs-lookup"><span data-stu-id="b8e97-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="b8e97-124">يمكنك أيضًا إنشاء أوامر العمل يدويًا.</span><span class="sxs-lookup"><span data-stu-id="b8e97-124">You can also create work orders manually.</span></span> <span data-ttu-id="b8e97-125">يقدم الرسم التوضيحي التالي نظرة عامة حول عملية الإنشاء التلقائي أو اليدوي لأوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="b8e97-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![رسم تخطيطي يوضح الإنشاء التلقائي أو اليدوي لأوامر العمل](media/07-overview-image.png)

<span data-ttu-id="b8e97-127">يجب إكمال عدة خطوات عندما تريد جدولة وتشغيل مهمة صيانة في أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="b8e97-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="b8e97-128">يقدم الرسم التوضيحي التالي نظرة عامة على معالجة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="b8e97-128">The following illustration shows an overview of the processing for a work order.</span></span>

![رسم تخطيطي يوضح نظرة عامة حول معالجة أمر عمل](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="b8e97-130">بشكل عام، عندما تعمل في Dynamics 365 Supply Chain Management والوحدة النمطية **إدارة الأصول**، تحدد **جديد** لإنشاء سجل جديد، وتحدد **تحرير** لتحديث سجل موجود ثم تحدد **حفظ** لحفظ بيانات جديدة أو محررة.</span><span class="sxs-lookup"><span data-stu-id="b8e97-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]