---
title: المواقع والمستودعات المتكاملة
description: يوضح هذا الموضوع تكامل بيانات الموقع والمستودع بين تطبيقات Finance and Operations وCommon Data Service.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
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
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 0f5ed58ad50df49250aa4c001401ff52d460dfa6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019615"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="18baa-103">المواقع والمستودعات المتكاملة</span><span class="sxs-lookup"><span data-stu-id="18baa-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="18baa-104">يوضح هذا الموضوع تكامل بيانات الموقع والمستودع بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="18baa-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="18baa-105">تعتبر المواقع والمستودعات التشغيلية مفاهيم عامة في تطبيق Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="18baa-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="18baa-106">وهي تستخدم لصياغة سلسلة التوريد الخاصة بشركك.</span><span class="sxs-lookup"><span data-stu-id="18baa-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="18baa-107">القوالب</span><span class="sxs-lookup"><span data-stu-id="18baa-107">Templates</span></span>

<span data-ttu-id="18baa-108">من خلال التكامل مع Common Data Service، تتوفر هذه المفاهيم وكافة المعلومات المتعلقة بها في Common Data Service باستخدام كيانات بيانات المواقع والمستودعات في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="18baa-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="18baa-109">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18baa-109">Finance and Operations apps</span></span> | <span data-ttu-id="18baa-110">تطبيقات Dynamics 365 الأخرى</span><span class="sxs-lookup"><span data-stu-id="18baa-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="18baa-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="18baa-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="18baa-112">المواقع</span><span class="sxs-lookup"><span data-stu-id="18baa-112">Sites</span></span> | <span data-ttu-id="18baa-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="18baa-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="18baa-114">المستودعات</span><span class="sxs-lookup"><span data-stu-id="18baa-114">Warehouses</span></span> | <span data-ttu-id="18baa-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="18baa-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

