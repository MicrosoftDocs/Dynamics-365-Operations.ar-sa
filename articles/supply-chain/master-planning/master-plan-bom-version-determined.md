---
title: تحديد إصدار قائمة مكونات الصنف
description: أثناء تحديد إجمالي المكونات المطلوبة للطلب، إذا تم تعيين نوع الأمر الافتراضي لصنف على الإنتاج، فإن محرك التخطيط يقوم بإيجاد إصدار قائمة مكونات صنف صالح يستند إلى الموقع.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6f1f1656f0ef04799b1ce6b397dac0f829e41c9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251927"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="30913-103">تحديد إصدار قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="30913-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30913-104">أثناء تحديد إجمالي المكونات المطلوبة للطلب، إذا تم تعيين نوع الأمر الافتراضي لصنف على الإنتاج، فإن محرك التخطيط يقوم بإيجاد إصدار قائمة مكونات صنف صالح يستند إلى الموقع.</span><span class="sxs-lookup"><span data-stu-id="30913-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="30913-105">يكون بُعد الموقع معروفًا دائمًا ويتم تحديده في حركة الطلب.</span><span class="sxs-lookup"><span data-stu-id="30913-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="30913-106">ويتم استخدام العملية التالية تحديد إصدار قائمة مكونات الصنف المراد استخدامه:</span><span class="sxs-lookup"><span data-stu-id="30913-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="30913-107">إذا تم تحديد إصدار قائمة مكونات الصنف للصنف في موقع الطلب، فإنه يتم استخدام قائمة مكونات الصنف الخاصة بالموقع.</span><span class="sxs-lookup"><span data-stu-id="30913-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="30913-108">وإذا لم يتم تحديد أي إصدار لقائمة مكونات الصنف الخاصة بالموقع لأي صنف في موقع الطلب، فإنه يتم استخدام قائمة مكونات صنف عامة.</span><span class="sxs-lookup"><span data-stu-id="30913-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="30913-109">لا تحدد شجرة المواد العامة موقعًا، وهي صالحة للعديد من المواقع.</span><span class="sxs-lookup"><span data-stu-id="30913-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="30913-110">وإذا كانت هناك قائمة مكونات صنف عامة، فإنه يتم استخدامها.</span><span class="sxs-lookup"><span data-stu-id="30913-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="30913-111">في حالة عدم وجود إصدار شجرة مواد عامة لاستخدامها، فإن تحديد إجمالي المكونات المطلوبة للطلب يتوقف عند هذه النقطة.</span><span class="sxs-lookup"><span data-stu-id="30913-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="30913-112">يجب أن يتوافق إصدار شجرة المواد الصالح مع المعايير المطلوبة للتاريخ والكمية، سواءً كان لموقع بعينه أو عامًا.</span><span class="sxs-lookup"><span data-stu-id="30913-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]