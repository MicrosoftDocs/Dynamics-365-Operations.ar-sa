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
ms.openlocfilehash: 1b9181211bbb65cdfc46e63f3cee0e9f5bc9f6a4
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173052"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="4dd09-103">المواقع والمستودعات المتكاملة</span><span class="sxs-lookup"><span data-stu-id="4dd09-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="4dd09-104">يوضح هذا الموضوع تكامل بيانات الموقع والمستودع بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="4dd09-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="4dd09-105">تعتبر المواقع والمستودعات التشغيلية مفاهيم عامة في تطبيق Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4dd09-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="4dd09-106">وهي تستخدم لصياغة سلسلة التوريد الخاصة بشركك.</span><span class="sxs-lookup"><span data-stu-id="4dd09-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="4dd09-107">القوالب</span><span class="sxs-lookup"><span data-stu-id="4dd09-107">Templates</span></span>

<span data-ttu-id="4dd09-108">من خلال التكامل مع Common Data Service، تتوفر هذه المفاهيم وكافة المعلومات المتعلقة بها في Common Data Service باستخدام كيانات بيانات المواقع والمستودعات في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="4dd09-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="4dd09-109">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4dd09-109">Finance and Operations apps</span></span> | <span data-ttu-id="4dd09-110">تطبيقات Dynamics 365 الأخرى</span><span class="sxs-lookup"><span data-stu-id="4dd09-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="4dd09-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="4dd09-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="4dd09-112">المواقع</span><span class="sxs-lookup"><span data-stu-id="4dd09-112">Sites</span></span> | <span data-ttu-id="4dd09-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="4dd09-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="4dd09-114">المستودعات</span><span class="sxs-lookup"><span data-stu-id="4dd09-114">Warehouses</span></span> | <span data-ttu-id="4dd09-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="4dd09-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

