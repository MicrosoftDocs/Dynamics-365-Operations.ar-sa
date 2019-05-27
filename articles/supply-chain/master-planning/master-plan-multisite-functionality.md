---
title: التخطيط الرئيسي ووظائف المواقع المتعددة
description: يأخذ التخطيط الرئيسي إعدادات أبعاد مخزون المستودع والموقع في الاعتبار.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: 10981e0fe201566c83fd28c792000865bc533cd3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573081"
---
# <a name="master-planning-and-multisite-functionality"></a><span data-ttu-id="d2ae0-103">التخطيط الرئيسي ووظائف المواقع المتعددة</span><span class="sxs-lookup"><span data-stu-id="d2ae0-103">Master planning and multisite functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2ae0-104">يأخذ التخطيط الرئيسي إعدادات أبعاد مخزون المستودع والموقع في الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="d2ae0-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="d2ae0-105">بُعد الموقع إلزامي ويمكنك تعيين بُعد المستودع بحيث يكون إلزاميًا.</span><span class="sxs-lookup"><span data-stu-id="d2ae0-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="d2ae0-106">وعندما يكون البعد إلزاميًا، يجب إدخال قيمة البعد على كافة حركات المخزون.</span><span class="sxs-lookup"><span data-stu-id="d2ae0-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="d2ae0-107">ولذلك، وخلال التخطيط الرئيسي، يكون الموقع والمستودع للطلب الأولي معروفين.</span><span class="sxs-lookup"><span data-stu-id="d2ae0-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="d2ae0-108">ويكون بعد الموقع كذلك متوافقًا حتى لا تتغير قيمة الموقع أثناء عملية تحديد إجمالي المكونات المطلوبة للطلب منخفض المستوى.</span><span class="sxs-lookup"><span data-stu-id="d2ae0-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="d2ae0-109">وعندما لا يتم تعيين المستودع ليكون إلزاميًا، قد لا يُعرف من الطلب الأولي.</span><span class="sxs-lookup"><span data-stu-id="d2ae0-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="d2ae0-110">ويجب أن يحدد محرك التخطيط المستودع الذي سيستخدمه بناءً على الإعدادات المحددة للصنف، والمستودعات الفردية، وكذلك تفاصيل بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="d2ae0-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="d2ae0-111">تصف المواضيع التالية كيفية عمل محرك التخطيط، عند تحديد إعدادات مختلفة، لتحديد المستودع الذي سيتم استخدامه.</span><span class="sxs-lookup"><span data-stu-id="d2ae0-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="d2ae0-112">التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="d2ae0-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d2ae0-113">التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي</span><span class="sxs-lookup"><span data-stu-id="d2ae0-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d2ae0-114">التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع غير إلزامي</span><span class="sxs-lookup"><span data-stu-id="d2ae0-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="d2ae0-115">التخطيط الرئيسي - تغطية الموقع، المستودع غير إلزامي</span><span class="sxs-lookup"><span data-stu-id="d2ae0-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="d2ae0-116">التخطيط الرئيسي - كيفية تحديد إصدار قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="d2ae0-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



