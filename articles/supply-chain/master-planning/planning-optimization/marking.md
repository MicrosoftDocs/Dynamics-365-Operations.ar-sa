---
title: علامات المخزون مع تحسين التخطيط
description: يوفر هذا الموضوع معلومات حول الخيارات المتاحة لتمييز المخزون في الأوامر المؤكدة عند استخدام تحسين التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7813f570afb0260e6740507c9504320c3e87be93
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263340"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="11a37-103">علامات المخزون مع تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="11a37-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11a37-104">يوفر هذا الموضوع معلومات حول الخيارات المتاحة لتمييز المخزون في الأوامر المؤكدة عند استخدام تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="11a37-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="11a37-105">تستخدم *العلامة* لربط التوريد والطلب.</span><span class="sxs-lookup"><span data-stu-id="11a37-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="11a37-106">وهو يمثل *تثبيت* السعر، والذي يشير إلى الطريقة التي يتوقع بها التخطيط الرئيسي تغطيه الطلب.</span><span class="sxs-lookup"><span data-stu-id="11a37-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="11a37-107">من وجهه لعرض التخطيط ، فان الفرق الأساسي هو ان وضع العلامة يعد أكثر نهائيه من تثبيت السعر.</span><span class="sxs-lookup"><span data-stu-id="11a37-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="11a37-108">وقد تم تقديم علامة لدعم سيناريوهات التكاليف الخاصة لأول مره داخل ، ما يرد أولا يصرف أولا وأخيرا ما يرد أخيرا يصرف أولا.</span><span class="sxs-lookup"><span data-stu-id="11a37-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="11a37-109">ومع ذلك ، فهي الآن تستخدم أيضا لبعض السيناريوهات غير الخاصة بالتكاليف.</span><span class="sxs-lookup"><span data-stu-id="11a37-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="11a37-110">وضع علامة علي التوريد والطلب يكون اختياريا ودائما في الغالب.</span><span class="sxs-lookup"><span data-stu-id="11a37-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="11a37-111">يمكن أزاله التمييز يدويا بواسطة مستخدم ، أو يمكن ازالته عن طريق تشغيل عمليه تحديد إجماليات بند أمر التوريد حيث يتم تحديد خيار **أزاله العلامات**.</span><span class="sxs-lookup"><span data-stu-id="11a37-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="11a37-112">يتم التحكم في تثبيت السعر بواسطة التخطيط الرئيسي اثناء التغطية لربط الطلب بالتوريد المطلوب.</span><span class="sxs-lookup"><span data-stu-id="11a37-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="11a37-113">يمكن تحديث تثبيت السعر لكل تشغيل تخطيط لتحسين التوريد المطلوب لتغطيه الطلب.</span><span class="sxs-lookup"><span data-stu-id="11a37-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="11a37-114">عندما يقوم التخطيط الرئيسي بتحديث معلومات التثبيت المسبق ، فانه يتقيد بآيه تعليمات موجودة.</span><span class="sxs-lookup"><span data-stu-id="11a37-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="11a37-115">ويبدا التثبيت من خلال تضمين العلامات ذات الصلة وعمليات الحجز الفعلية وعمليات الحجز علي الطلب ، بالتسلسل التالي:</span><span class="sxs-lookup"><span data-stu-id="11a37-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="11a37-116">وضع علامة علي الطلب والتوريد</span><span class="sxs-lookup"><span data-stu-id="11a37-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="11a37-117">عمليات الحجز الفعلية</span><span class="sxs-lookup"><span data-stu-id="11a37-117">On-hand reservations</span></span>
1. <span data-ttu-id="11a37-118">حجز الأمر</span><span class="sxs-lookup"><span data-stu-id="11a37-118">On-order reservations</span></span>

<span data-ttu-id="11a37-119">عند تاكيد أمر مخطط ، يوفر مربع الحوار **التاكيد** حقل **تحديث التعليم** الذي تستخدمه لتعيين خيارات وضع العلامات للأوامر التي تم إنشاؤها اثناء التاكيد.</span><span class="sxs-lookup"><span data-stu-id="11a37-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="11a37-120">حدد إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="11a37-120">Select one of the following values:</span></span>

- <span data-ttu-id="11a37-121">**لا** – لم يتم تطبيق إيه علامات مخزون.</span><span class="sxs-lookup"><span data-stu-id="11a37-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="11a37-122">‎**قياسي‎** - يتم تحديث علامات المخزون وفقًا لتثبيت السعر.</span><span class="sxs-lookup"><span data-stu-id="11a37-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="11a37-123">ويتم وضع علامة على أحد أوامر المتطلبات (الطلب) على أساس أمر استيفاء (العرض).</span><span class="sxs-lookup"><span data-stu-id="11a37-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="11a37-124">في حاله بقاء بعض الكمية علي أمر الاستيفاء ، فلن يتم تمييزها ، ويتم ترك المعلومات المرجعية فارغه.</span><span class="sxs-lookup"><span data-stu-id="11a37-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="11a37-125">علي سبيل المثال ، إذا كان أمر التوريد الخاص ب 100 ea بيجيد في مقابل أمر شراء ل 150 ea ، سيتم تعيين معلومات مرجعيه لأمر المبيعات فقط.</span><span class="sxs-lookup"><span data-stu-id="11a37-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="11a37-126">**مفصل** - يتم وضع علامة على كل من أمر المتطلب (الطلب) وأمر الاستيفاء (العرض)، بغض النظر عما إذا كانت هناك أية كمية متبقية في أمر الاستيفاء أم لا.</span><span class="sxs-lookup"><span data-stu-id="11a37-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="11a37-127">علي سبيل المثال ، إذا كان أمر التوريد الخاص ب 100 ea بيجيد في مقابل أمر شراء ل 150 ea ، سيتم تعيين معلومات مرجعيه لأمر المبيعات وأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="11a37-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]