---
title: الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها في Dynamics 365 Supply Chain Management.
author: kamaybac
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7502cd16129431d41d152508fb3b49ff85a5a9f8
ms.sourcegitcommit: f1db998ecfccca660eb15cc2739b12c8463fa54d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331238"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="42ed5-103">الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="42ed5-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42ed5-104">سيتم تحديث هذا الموضوع عند توثيق الميزات الجديدة أو التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="42ed5-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="42ed5-105">لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.</span><span class="sxs-lookup"><span data-stu-id="42ed5-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="42ed5-106">لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.</span><span class="sxs-lookup"><span data-stu-id="42ed5-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="42ed5-107">تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="42ed5-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="42ed5-108">يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="42ed5-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="42ed5-109">يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42ed5-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="42ed5-110">ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.11 من Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="42ed5-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="42ed5-111">استخدام محرك التخطيط الرئيسي لـ Supply Chain Management لسيناريوهات التوزيع</span><span class="sxs-lookup"><span data-stu-id="42ed5-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="42ed5-112">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="42ed5-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="42ed5-113">لتحسين الأداء وتصغير حمل قاعده بيانات SQL أثناء تشغيل التخطيط الرئيسي، يتم استبدال محرك التخطيط الرئيسي لـ Supply Chain Management بواسطة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="42ed5-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="42ed5-114">يسمح تحسين التخطيط بتشغيل التخطيط السريع الذي يمكن تنفيذه حتى أثناء ساعات العمل.</span><span class="sxs-lookup"><span data-stu-id="42ed5-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="42ed5-115">ويعمل ذلك علي المخططين من التفاعل علي الفور للتغييرات في محددات الطلب أو التخطيط.</span><span class="sxs-lookup"><span data-stu-id="42ed5-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="42ed5-116">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="42ed5-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="42ed5-117">نعم، سيحل تحسين التخطيط محل محرك التخطيط الرئيسي الحالي لـ Supply Chain Management المضمن.</span><span class="sxs-lookup"><span data-stu-id="42ed5-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="42ed5-118">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="42ed5-118">**Product areas affected**</span></span>         | <span data-ttu-id="42ed5-119">Supply Chain Management - التخطيط الرئيسي</span><span class="sxs-lookup"><span data-stu-id="42ed5-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="42ed5-120">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="42ed5-120">**Deployment option**</span></span>              | <span data-ttu-id="42ed5-121">السحابة فقط.</span><span class="sxs-lookup"><span data-stu-id="42ed5-121">Cloud only.</span></span> <span data-ttu-id="42ed5-122">تحسين التخطيط غير مدعوم بعمليات النشر المحلية.</span><span class="sxs-lookup"><span data-stu-id="42ed5-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="42ed5-123">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="42ed5-123">**Status**</span></span>                         | <span data-ttu-id="42ed5-124">مهملة.</span><span class="sxs-lookup"><span data-stu-id="42ed5-124">Deprecated.</span></span> <span data-ttu-id="42ed5-125">في إبريل 2021، لن يتم دعم سيناريوهات التوزيع بعد ذلك مع محرك التخطيط الرئيسي المضمّن لـ Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="42ed5-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="42ed5-126">بالنسبة لسيناريوهات التوزيع، يجب أن يستخدم العملاء تحسين التخطيط لعمليات حساب التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="42ed5-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="42ed5-127">لمزيد من المعلومات، راجع [مستندات تحسين التخطيط](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="42ed5-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="42ed5-128">وقد يستمر العملاء الذين لديهم عمليات نشر محلية لـ Dynamics 365 Supply Chain Management في استخدام محرك التخطيط الرئيسي لـ Supply Chain Management بعد أبريل 2021.</span><span class="sxs-lookup"><span data-stu-id="42ed5-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="42ed5-129">ومع ذلك، لن يتم توفير المزيد من تحسينات الميزات.</span><span class="sxs-lookup"><span data-stu-id="42ed5-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="42ed5-130">الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها</span><span class="sxs-lookup"><span data-stu-id="42ed5-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="42ed5-131">لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="42ed5-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
