---
title: ميزات Platform التي تمت إزالتها أو إهمالها
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها في تحديثات الأنظمة الأساسية لتطبيقات Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
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
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095764"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="f0165-103">ميزات Platform التي تمت إزالتها أو إهمالها</span><span class="sxs-lookup"><span data-stu-id="f0165-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0165-104">يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها في تحديثات الأنظمة الأساسية لتطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0165-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="f0165-105">لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.</span><span class="sxs-lookup"><span data-stu-id="f0165-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="f0165-106">لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.</span><span class="sxs-lookup"><span data-stu-id="f0165-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="f0165-107">تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="f0165-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="f0165-108">يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="f0165-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="f0165-109">يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0165-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="f0165-110">update 32 للنظام الأساسي</span><span class="sxs-lookup"><span data-stu-id="f0165-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="f0165-111">لم يعد مربع حوار تغيير طلب سير العمل يتضمن القائمة المنسدلة لتحديد المستخدم</span><span class="sxs-lookup"><span data-stu-id="f0165-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="f0165-112">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="f0165-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="f0165-113">كانت هذه مشكلة تتعلق بالأمان نظرا لأنه قد تم إرسال طلب التغيير إلى مستخدم غير مقصود.</span><span class="sxs-lookup"><span data-stu-id="f0165-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="f0165-114">وكانت كذلك مشكلة في الاستخدام لأنها أجبرت المستخدم على تحديد الشخص الذي أنشأ سير العمل ويقوم بتحديدها يدويا.</span><span class="sxs-lookup"><span data-stu-id="f0165-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="f0165-115">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="f0165-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="f0165-116">لا</span><span class="sxs-lookup"><span data-stu-id="f0165-116">No</span></span> |
| <span data-ttu-id="f0165-117">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="f0165-117">**Product areas affected**</span></span>         | <span data-ttu-id="f0165-118">سير العمل</span><span class="sxs-lookup"><span data-stu-id="f0165-118">Workflow</span></span> |
| <span data-ttu-id="f0165-119">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="f0165-119">**Deployment option**</span></span>              | <span data-ttu-id="f0165-120">الكل</span><span class="sxs-lookup"><span data-stu-id="f0165-120">All</span></span> |
| <span data-ttu-id="f0165-121">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="f0165-121">**Status**</span></span>                         | <span data-ttu-id="f0165-122">تمت إزالة القائمة المنسدلة لتحديد المستخدم من مربع حوار طلب التغيير في النظام الأساسي لتحديث النظام 32.</span><span class="sxs-lookup"><span data-stu-id="f0165-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="f0165-123">سيتم إرسال طلبات التغيير التي تم طلبها تلقائيا إلى المنشئ كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="f0165-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="f0165-124">لمزيد من المعلومات حول هذ الوظيفة، راجع [‏‫الإجراءات في عمليات الموافقة على سير العمل](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="f0165-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a><span data-ttu-id="f0165-125">لم تعد الارتباطات المستخدمة للتصفح مدعومة في المستندات ذات حدود فاصلة للصفحات التي تعرضها الخدمة المستضافة في السحابة</span><span class="sxs-lookup"><span data-stu-id="f0165-125">Embedded drill-through links are no longer supported in paginated documents rendered by the cloud-hosted service</span></span> 
|   |  |
|------------|--------------------|
| <span data-ttu-id="f0165-126">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="f0165-126">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="f0165-127">قد تحتوي عناوين URL المضمنة في المستندات التي تعرضها الخدمة على بيانات عمل حساسة.</span><span class="sxs-lookup"><span data-stu-id="f0165-127">Navigation URLs embedded in documents rendered by the service may contain sensitive business data.</span></span> <span data-ttu-id="f0165-128">نحن نعمل على إزالة دعم الارتباطات المستخدمة للتصفح في المستندات كتدبير وقائي لتوفير المزيد من الحماية لبيانات العميل.</span><span class="sxs-lookup"><span data-stu-id="f0165-128">We are removing support for embedded drill-through links in documents as a security precaution to further protect customer's data.</span></span> <span data-ttu-id="f0165-129">سيستفيد المستخدمون أيضًا من الأداء المحسن أثناء إنتاج المستندات بشكل تفاعلي كنتيجة لهذا التغيير.</span><span class="sxs-lookup"><span data-stu-id="f0165-129">Users will also benefit from improved performance while interactively producing documents as a result of this change.</span></span>  |
| <span data-ttu-id="f0165-130">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="f0165-130">**Replaced by another feature?**</span></span>   | <span data-ttu-id="f0165-131">لا</span><span class="sxs-lookup"><span data-stu-id="f0165-131">No</span></span> |
| <span data-ttu-id="f0165-132">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="f0165-132">**Product areas affected**</span></span>         | <span data-ttu-id="f0165-133">التقارير</span><span class="sxs-lookup"><span data-stu-id="f0165-133">Reporting</span></span> |
| <span data-ttu-id="f0165-134">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="f0165-134">**Deployment option**</span></span>              | <span data-ttu-id="f0165-135">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="f0165-135">All</span></span> |
| <span data-ttu-id="f0165-136">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="f0165-136">**Status**</span></span>                         | <span data-ttu-id="f0165-137">تمت إزالة هذه الميزة من الخدمة.</span><span class="sxs-lookup"><span data-stu-id="f0165-137">This feature is actively being removed from the service.</span></span><br><br><span data-ttu-id="f0165-138">يقدم العميل الحديث خيارات عديدة لإنتاج طرق العرض التي تتضمن ارتباطات يتم إنشاؤها تلقائيًا للمساعدة في التنقل في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="f0165-138">The modern client offers numerous options for producing views that include auto-generated links to assist in navigating the application.</span></span> <span data-ttu-id="f0165-139">ننصح بالمستندات ذات حدود فاصلة للصفحات التي تعرضها الخدمة للمراسلات الخارجية التي يتم إرسالها بالبريد الإلكتروني وأرشفتها وطباعتها للمستلمين.</span><span class="sxs-lookup"><span data-stu-id="f0165-139">Paginated documents rendered by the service are recommended for external communications that are emailed, archived, and printed for recipients.</span></span> <span data-ttu-id="f0165-140">لقد قمنا بتحسين تجربة معاينة المستندات مباشرة في المستعرض، مما يوفر الوصول المباشر إلى الطابعات المحلية.</span><span class="sxs-lookup"><span data-stu-id="f0165-140">We have improved the experience for previewing documents directly in the browser, which offers direct access to local printers.</span></span> <span data-ttu-id="f0165-141">لمزيد من المعلومات، راجع [معاينة مستندات PDF باستخدام عارض مضمن‬](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents).</span><span class="sxs-lookup"><span data-stu-id="f0165-141">For more information, see [Preview PDF documents with an embedded viewer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="f0165-142">الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها</span><span class="sxs-lookup"><span data-stu-id="f0165-142">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="f0165-143">لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="f0165-143">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

