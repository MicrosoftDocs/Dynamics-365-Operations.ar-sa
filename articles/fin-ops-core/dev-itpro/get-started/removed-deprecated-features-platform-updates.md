---
title: ميزات Platform التي تمت إزالتها أو إهمالها
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها في تحديثات الأنظمة الأساسية لتطبيقات Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087873"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="cf199-103">ميزات Platform التي تمت إزالتها أو إهمالها</span><span class="sxs-lookup"><span data-stu-id="cf199-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf199-104">يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها في تحديثات الأنظمة الأساسية لتطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cf199-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="cf199-105">لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.</span><span class="sxs-lookup"><span data-stu-id="cf199-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="cf199-106">لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.</span><span class="sxs-lookup"><span data-stu-id="cf199-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="cf199-107">تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="cf199-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="cf199-108">يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="cf199-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="cf199-109">يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cf199-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="cf199-110">update 32 للنظام الأساسي</span><span class="sxs-lookup"><span data-stu-id="cf199-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="cf199-111">لم يعد مربع حوار تغيير طلب سير العمل يتضمن القائمة المنسدلة لتحديد المستخدم</span><span class="sxs-lookup"><span data-stu-id="cf199-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="cf199-112">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="cf199-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf199-113">كانت هذه مشكلة تتعلق بالأمان نظرا لأنه قد تم إرسال طلب التغيير إلى مستخدم غير مقصود.</span><span class="sxs-lookup"><span data-stu-id="cf199-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="cf199-114">وكانت كذلك مشكلة في الاستخدام لأنها أجبرت المستخدم على تحديد الشخص الذي أنشأ سير العمل ويقوم بتحديدها يدويا.</span><span class="sxs-lookup"><span data-stu-id="cf199-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="cf199-115">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="cf199-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf199-116">لا</span><span class="sxs-lookup"><span data-stu-id="cf199-116">No</span></span> |
| <span data-ttu-id="cf199-117">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="cf199-117">**Product areas affected**</span></span>         | <span data-ttu-id="cf199-118">سير العمل</span><span class="sxs-lookup"><span data-stu-id="cf199-118">Workflow</span></span> |
| <span data-ttu-id="cf199-119">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="cf199-119">**Deployment option**</span></span>              | <span data-ttu-id="cf199-120">الكل</span><span class="sxs-lookup"><span data-stu-id="cf199-120">All</span></span> |
| <span data-ttu-id="cf199-121">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="cf199-121">**Status**</span></span>                         | <span data-ttu-id="cf199-122">تمت إزالة القائمة المنسدلة لتحديد المستخدم من مربع حوار طلب التغيير في النظام الأساسي لتحديث النظام 32.</span><span class="sxs-lookup"><span data-stu-id="cf199-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="cf199-123">سيتم إرسال طلبات التغيير التي تم طلبها تلقائيا إلى المنشئ كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="cf199-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="cf199-124">لمزيد من المعلومات حول هذ الوظيفة، راجع [‏‫الإجراءات في عمليات الموافقة على سير العمل](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="cf199-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="cf199-125">الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها</span><span class="sxs-lookup"><span data-stu-id="cf199-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="cf199-126">لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="cf199-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

