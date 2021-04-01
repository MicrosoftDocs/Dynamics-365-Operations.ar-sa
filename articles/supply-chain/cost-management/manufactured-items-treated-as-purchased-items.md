---
title: إعداد المنتجات التي يمكن أن تكون منتجة أو مشتراة
description: 'يمكن توريد المنتجات بطرق مختلفة: يمكن إنتاجها (تصنيعها) أو تدبيرها (شراؤها). توضح هذه المقالة بعض النقاط النموذجية التي يجب أخذها في الاعتبار عند تكوين المنتجات لدعم استخدام مصادر متعددة.'
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58d89b18d32ac1fde047bcb02b4af68f07ff335a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243313"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="1283c-104">إعداد المنتجات التي يمكن أن تكون منتجة أو مشتراة</span><span class="sxs-lookup"><span data-stu-id="1283c-104">Set up products that can be produced or procured</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1283c-105">يمكن توريد المنتجات بطرق مختلفة: يمكن إنتاجها (تصنيعها) أو تدبيرها (شراؤها).</span><span class="sxs-lookup"><span data-stu-id="1283c-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="1283c-106">توضح هذه المقالة بعض النقاط النموذجية التي يجب أخذها في الاعتبار عند تكوين المنتجات لدعم استخدام مصادر متعددة.</span><span class="sxs-lookup"><span data-stu-id="1283c-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="1283c-107">يتم عادةً استخدام المصادر المتعددة لصنف مشتري تم تصنيعه أحياناً، أو عند تغيير صنف كان في الأساس صنفًا مصنعًا بحيث يصبح الآن صنفًا تم شراؤه في الأساس.</span><span class="sxs-lookup"><span data-stu-id="1283c-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="1283c-108">ويتم تصميمه أولاً كصنف مصنّع، بحيث يمكن تحديد قائمة مكونات الصنف (BOM) ومعلومات المسار، ودعم أوامر الإنتاج الخاصة بالصنف.</span><span class="sxs-lookup"><span data-stu-id="1283c-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="1283c-109">يجب تعيين نوع الإنتاج إلى **قائمة مكونات الصنف** (أو لعملية التصنيع أو **المعادلة** أو **المنتج المساعد**).</span><span class="sxs-lookup"><span data-stu-id="1283c-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="1283c-110">عند استخدام التكاليف القياسية، يمكن حساب سجل تكلفة الصنف للأصناف المصنعة.</span><span class="sxs-lookup"><span data-stu-id="1283c-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="1283c-111">ومع ذلك، قد لا يتطابق سجل تكلفة الصنف مع التكلفة القياسية التي تريدها لأغراض الشراء.</span><span class="sxs-lookup"><span data-stu-id="1283c-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="1283c-112">وفي هذه الحالة، يجب إدخال التكلفة القياسية وتنشيطها يدويًا لسجل تكلفة الصنف.</span><span class="sxs-lookup"><span data-stu-id="1283c-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="1283c-113">وفي حساب التكلفة، خذ في الاعتبار استخدام قائمة مكونات الصنف الخاصة والمسار اللذين يمثلان مزيج توريد المنتج على مدى فترة مالية لتقليل التباينات على مر الزمن.</span><span class="sxs-lookup"><span data-stu-id="1283c-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="1283c-114">بالإضافة إلى ذلك، يمكن نقل صنف مصنع في موقع واحد إلى موقع آخر.</span><span class="sxs-lookup"><span data-stu-id="1283c-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="1283c-115">ولذلك، يجب إدخال تكلفة الصنف وتنشيطها يدوياً للموقع الذي يتم نقل الصنف إليه.</span><span class="sxs-lookup"><span data-stu-id="1283c-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="1283c-116">عند استخدام الصنف المصنّع كمكون تم شراؤه، حيث يجب التعامل مع الصنف الذي تم شراؤه.</span><span class="sxs-lookup"><span data-stu-id="1283c-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="1283c-117">وينطبق هذا المبدأ التوجيهي، بغض النظر عن ما إذا تم حساب تكاليف المكون أو تتم إدخاله يدوياً.</span><span class="sxs-lookup"><span data-stu-id="1283c-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="1283c-118">وبتعبير آخر، يجب أن تعالج عملية حساب قائمة مكونات الصنف تكاليف الصنف كمكون تم شراؤه، بدلاً من استخدام معلومات مسار وقائمة مكونات الصنف للصنف لحساب التكاليف.</span><span class="sxs-lookup"><span data-stu-id="1283c-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="1283c-119">لمنع حدوث الحساب، حدد علامة **إيقاف عملية تحديد إجمالي المكونات** المضمنة في مجموعة حساب قائمة مكونات الصنف التي تم تعيينها للصنف.</span><span class="sxs-lookup"><span data-stu-id="1283c-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="1283c-120">ولمنع عمليات حساب الجدولة الرئيسية من تحديد المتطلبات من خلال الصنف، قم بتحديد الحد الزمني لعملية تحديد إجمالي المكونات المطلوبة‬إلى 0 (صفر) يوم في تغطية الصنف أو مجموعة التغطية.</span><span class="sxs-lookup"><span data-stu-id="1283c-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="1283c-121">وستتعامل عملية حساب الجدولة الرئيسية فيما بعد مع الصنف كصنف تم شراؤه ولن يتم تنفيذ عملية حساب أخرى لمعلومات مسار وقائمة مكونات الصنف للصنف.</span><span class="sxs-lookup"><span data-stu-id="1283c-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]