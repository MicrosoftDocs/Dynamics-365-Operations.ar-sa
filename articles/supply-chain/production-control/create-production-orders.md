---
title: نظرة عامة على إدارة دورة حياة أمر الإنتاج
description: عند إنشاء أمر إنتاج، يتم بدء طلب لبدء إنتاج صنف. يحتوي أمر الإنتاج على معلومات حول ما سيتم إنتاجه والكمية التي يجب إنتاجها وتاريخ الانتهاء المخطط. ويحتوي أيضًا على معلومات حول المواد التي يجب استهلاكها والعملية التي يجب اتباعها لإنتاج الصنف.
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80031737ab0d0c4ab1e4dbd5646ad91f1a010cd5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421513"
---
# <a name="production-order-lifecycle-overview"></a><span data-ttu-id="ccd17-105">نظرة عامة على إدارة دورة حياة أمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="ccd17-105">Production order lifecycle overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccd17-106">عند إنشاء أمر إنتاج، يتم بدء طلب لبدء إنتاج صنف.</span><span class="sxs-lookup"><span data-stu-id="ccd17-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="ccd17-107">يحتوي أمر الإنتاج على معلومات حول ما سيتم إنتاجه والكمية التي يجب إنتاجها وتاريخ الانتهاء المخطط.</span><span class="sxs-lookup"><span data-stu-id="ccd17-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="ccd17-108">ويحتوي أيضًا على معلومات حول المواد التي يجب استهلاكها والعملية التي يجب اتباعها لإنتاج الصنف.</span><span class="sxs-lookup"><span data-stu-id="ccd17-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="ccd17-109">يمر أمر الإنتاج بمراحل دورة حياة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ccd17-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="ccd17-110">وعند إنشاء أمر، فإنه يتم تعيين الحالة **تم إنشاؤه** له.</span><span class="sxs-lookup"><span data-stu-id="ccd17-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="ccd17-111">وعند الانتهاء من أمر، فإنه يتم تعيين الحالة **تم الانتهاء منه** له.</span><span class="sxs-lookup"><span data-stu-id="ccd17-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="ccd17-112">ويتيح إعداد المعلمة في كل مرحلة من المراحل للمستخدم بتكوين كل خطوة.</span><span class="sxs-lookup"><span data-stu-id="ccd17-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="ccd17-113">يمكن إعداد الإعداد لمستخدم واحد أو لكافة المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="ccd17-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="ccd17-114">قائمة مكونات صنف الإنتاج ومسار الإنتاج هي الكيانات الرئيسية لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ccd17-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="ccd17-115">ويتم نسخها لأمر الإنتاج استناداً إلى الصنف المحدد والكمية التي سيتم إنتاجها.</span><span class="sxs-lookup"><span data-stu-id="ccd17-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="ccd17-116">قبل بدء أمر الإنتاج، يمكن تحرير قائمة مكونات صنف الإنتاج والمسار.</span><span class="sxs-lookup"><span data-stu-id="ccd17-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="ccd17-117">ويمكن إنشاء أمر إنتاج في السيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="ccd17-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="ccd17-118">يتم إنشاؤه بواسطة تنفيذ التخطيط الرئيسي استنادًا إلى طلب المواد.</span><span class="sxs-lookup"><span data-stu-id="ccd17-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="ccd17-119">يتم إنشاؤه مباشرةً من بند أمر مبيعات أو عند إنشاء أمر إنتاج ذي مستوى عالي وتقديره (التوريد مثبت السعر).</span><span class="sxs-lookup"><span data-stu-id="ccd17-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="ccd17-120">يتم إنشاؤه يدوياً.</span><span class="sxs-lookup"><span data-stu-id="ccd17-120">Created manually.</span></span>




