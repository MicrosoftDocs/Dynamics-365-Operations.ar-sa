---
title: المواقع والمستودعات المتكاملة
description: يوضح هذا الموضوع تكامل بيانات الموقع والمستودع بين تطبيقات Finance and Operations وDataverse.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750656"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="334a8-103">المواقع والمستودعات المتكاملة</span><span class="sxs-lookup"><span data-stu-id="334a8-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="334a8-104">يوضح هذا الموضوع تكامل بيانات الموقع والمستودع بين تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="334a8-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="334a8-105">تعتبر المواقع والمستودعات التشغيلية مفاهيم عامة في تطبيق Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="334a8-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="334a8-106">وهي تستخدم لصياغة سلسلة التوريد الخاصة بشركك.</span><span class="sxs-lookup"><span data-stu-id="334a8-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="334a8-107">القوالب</span><span class="sxs-lookup"><span data-stu-id="334a8-107">Templates</span></span>

<span data-ttu-id="334a8-108">من خلال التكامل مع Dataverse، تتوفر هذه المفاهيم وكافة المعلومات المتعلقة بها في Dataverse باستخدام جداول بيانات المواقع والمستودعات في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="334a8-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="334a8-109">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="334a8-109">Finance and Operations apps</span></span> | <span data-ttu-id="334a8-110">تطبيقات Dynamics 365 الأخرى</span><span class="sxs-lookup"><span data-stu-id="334a8-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="334a8-111">الوصف</span><span class="sxs-lookup"><span data-stu-id="334a8-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="334a8-112">المواقع</span><span class="sxs-lookup"><span data-stu-id="334a8-112">Sites</span></span> | <span data-ttu-id="334a8-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="334a8-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="334a8-114">المستودعات</span><span class="sxs-lookup"><span data-stu-id="334a8-114">Warehouses</span></span> | <span data-ttu-id="334a8-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="334a8-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]