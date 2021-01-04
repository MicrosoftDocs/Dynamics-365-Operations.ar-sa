---
title: المواقع والمستودعات المتكاملة
description: يوضح هذا الموضوع تكامل بيانات الموقع والمستودع بين تطبيقات Finance and Operations وDataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679310"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="4fdaf-103">المواقع والمستودعات المتكاملة</span><span class="sxs-lookup"><span data-stu-id="4fdaf-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="4fdaf-104">يوضح هذا الموضوع تكامل بيانات الموقع والمستودع بين تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="4fdaf-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="4fdaf-105">تعتبر المواقع والمستودعات التشغيلية مفاهيم عامة في تطبيق Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4fdaf-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="4fdaf-106">وهي تستخدم لصياغة سلسلة التوريد الخاصة بشركك.</span><span class="sxs-lookup"><span data-stu-id="4fdaf-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="4fdaf-107">القوالب</span><span class="sxs-lookup"><span data-stu-id="4fdaf-107">Templates</span></span>

<span data-ttu-id="4fdaf-108">من خلال التكامل مع Dataverse، تتوفر هذه المفاهيم وكافة المعلومات المتعلقة بها في Dataverse باستخدام جداول بيانات المواقع والمستودعات في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="4fdaf-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="4fdaf-109">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4fdaf-109">Finance and Operations apps</span></span> | <span data-ttu-id="4fdaf-110">تطبيقات Dynamics 365 الأخرى</span><span class="sxs-lookup"><span data-stu-id="4fdaf-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="4fdaf-111">الوصف</span><span class="sxs-lookup"><span data-stu-id="4fdaf-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="4fdaf-112">المواقع</span><span class="sxs-lookup"><span data-stu-id="4fdaf-112">Sites</span></span> | <span data-ttu-id="4fdaf-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="4fdaf-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="4fdaf-114">المستودعات</span><span class="sxs-lookup"><span data-stu-id="4fdaf-114">Warehouses</span></span> | <span data-ttu-id="4fdaf-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="4fdaf-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

