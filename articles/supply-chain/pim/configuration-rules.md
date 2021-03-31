---
title: قواعد التكوين
description: توفر هذه المقالة معلومات عامة حول قواعد التكوين. تعرّف قواعد التكوين العلاقات بين الأصناف الموجودة في قائمة مكونات الصنف (BOM) للمنتجات التي تستخدم تقنية التكوين المستنِد إلى بُعد.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac3515837df45b65121ebec72a32ac98d740796a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221861"
---
# <a name="configuration-rules"></a><span data-ttu-id="56345-104">قواعد التكوين</span><span class="sxs-lookup"><span data-stu-id="56345-104">Configuration rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56345-105">توفر هذه المقالة معلومات عامة حول قواعد التكوين.</span><span class="sxs-lookup"><span data-stu-id="56345-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="56345-106">تعرّف قواعد التكوين العلاقات بين الأصناف الموجودة في قائمة مكونات الصنف (BOM) للمنتجات التي تستخدم تقنية التكوين المستنِد إلى بُعد.</span><span class="sxs-lookup"><span data-stu-id="56345-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="56345-107">تتوفر قواعد التكوين عند قيامك بتحديد نماذج التكوين المستندة إلى بعد.</span><span class="sxs-lookup"><span data-stu-id="56345-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="56345-108">ويتم استخدام قواعد التكوين لفرض أو منع مجموعات الأصناف المحددة في قائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="56345-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="56345-109">وبعد إنشاء قائمة مكونات الصنف والأصناف ذات الصلة التي تم تعيينها إلى مجموعات التكوين الخاصة بها، يمكن تحديد واحد أو أكثر من قواعد التكوين.</span><span class="sxs-lookup"><span data-stu-id="56345-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="56345-110">وفي حالة انتماء الصنفين لبعضهما، يتم استخدام عامل **التحديد** لضمان الإدراج.</span><span class="sxs-lookup"><span data-stu-id="56345-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="56345-111">أما إذا كان يتم استثناء الصنفين بشكل متبادل، فإنه يتم استخدام عامل **إلغاء التحديد** لضمان الاستثناء.</span><span class="sxs-lookup"><span data-stu-id="56345-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="56345-112">**ملاحظة:** تنطبق هذه المعلومات فقط على أصول المنتجات التي تستخدم تقنية التكوين المستندة إلى بعد.</span><span class="sxs-lookup"><span data-stu-id="56345-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="56345-113">ولا تتأثر عمليات التكوين الحالية بالتغييرات المتتابعة على قواعد التكوين.</span><span class="sxs-lookup"><span data-stu-id="56345-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="56345-114">ومع ذلك، يُعد من المهم تعيين القواعد قبل تحديد تكوين جديد، أو فحص هذه القواعد إذا كنت تعتقد أنه قد تم تغيير القواعد.</span><span class="sxs-lookup"><span data-stu-id="56345-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="56345-115">**ملاحظة:** بالنسبة إلى طريقة **التحديد**، يتم تحديد مجموعة التكوين المشتق ورقم الصنف والتكوين تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="56345-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="56345-116">وفي طريقة **إلغاء التحديد** لا يمكن تحديد مجموعة التكوين المشتق ورقم الصنف بالإضافة إلى التكوين.</span><span class="sxs-lookup"><span data-stu-id="56345-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="additional-resources"></a><span data-ttu-id="56345-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="56345-117">Additional resources</span></span>
--------

[<span data-ttu-id="56345-118">نظرة عامة على تكوين المنتجات المستند إلى الأبعاد</span><span class="sxs-lookup"><span data-stu-id="56345-118">Dimension-based product configuration overview</span></span>](dimension-based-product-configuration.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]