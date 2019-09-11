---
title: نظرة عامة على التخطيط الرئيسي ووظائف المواقع المتعددة
description: يأخذ التخطيط الرئيسي إعدادات أبعاد مخزون المستودع والموقع في الاعتبار.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f05e3efd1716a27a659ae40145f37bb0b3d977f
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865390"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="1cf5a-103">نظرة عامة على التخطيط الرئيسي ووظائف المواقع المتعددة</span><span class="sxs-lookup"><span data-stu-id="1cf5a-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cf5a-104">يأخذ التخطيط الرئيسي إعدادات أبعاد مخزون المستودع والموقع في الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="1cf5a-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="1cf5a-105">بُعد الموقع إلزامي ويمكنك تعيين بُعد المستودع بحيث يكون إلزاميًا.</span><span class="sxs-lookup"><span data-stu-id="1cf5a-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="1cf5a-106">وعندما يكون البعد إلزاميًا، يجب إدخال قيمة البعد على كافة حركات المخزون.</span><span class="sxs-lookup"><span data-stu-id="1cf5a-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="1cf5a-107">ولذلك، وخلال التخطيط الرئيسي، يكون الموقع والمستودع للطلب الأولي معروفين.</span><span class="sxs-lookup"><span data-stu-id="1cf5a-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="1cf5a-108">ويكون بعد الموقع كذلك متوافقًا حتى لا تتغير قيمة الموقع أثناء عملية تحديد إجمالي المكونات المطلوبة للطلب منخفض المستوى.</span><span class="sxs-lookup"><span data-stu-id="1cf5a-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="1cf5a-109">وعندما لا يتم تعيين المستودع ليكون إلزاميًا، قد لا يُعرف من الطلب الأولي.</span><span class="sxs-lookup"><span data-stu-id="1cf5a-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="1cf5a-110">ويجب أن يحدد محرك التخطيط المستودع الذي سيستخدمه بناءً على الإعدادات المحددة للصنف، والمستودعات الفردية، وكذلك تفاصيل بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="1cf5a-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="1cf5a-111">تصف المواضيع التالية كيفية عمل محرك التخطيط، عند تحديد إعدادات مختلفة، لتحديد المستودع الذي سيتم استخدامه.</span><span class="sxs-lookup"><span data-stu-id="1cf5a-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="1cf5a-112">التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="1cf5a-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="1cf5a-113">التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="1cf5a-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="1cf5a-114">التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع غير إلزامي</span><span class="sxs-lookup"><span data-stu-id="1cf5a-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="1cf5a-115">التخطيط الرئيسي - تغطية الموقع، المستودع غير إلزامي</span><span class="sxs-lookup"><span data-stu-id="1cf5a-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="1cf5a-116">التخطيط الرئيسي - كيفية تحديد إصدار قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="1cf5a-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



