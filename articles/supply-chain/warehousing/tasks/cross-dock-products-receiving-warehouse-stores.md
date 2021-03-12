---
title: توزيع المنتجات من المستودع المستلم حتى المتاجر
description: يتناول هذا الإجراء الخطوات اللازمة لإنشاء ومعالجة ‏‫توزيع البضائع‬ لتوزيع المنتجات من موقع استلام أمر الشراء إلى متجر واحد أو أكثر.
author: ShylaThompson
manager: tfehr
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac93806bc85be92840548e160ddf803e63adbbc4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977178"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="dfb12-103">توزيع المنتجات من المستودع المستلم حتى المتاجر</span><span class="sxs-lookup"><span data-stu-id="dfb12-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dfb12-104">يتناول هذا الإجراء الخطوات اللازمة لإنشاء ومعالجة ‏‫توزيع البضائع‬ لتوزيع المنتجات من موقع استلام أمر الشراء إلى متجر واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="dfb12-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="dfb12-105">يمكن للمستخدم تحديد تكوينات متعددة وامتلاك النظام الذي يقترح كيفية توزيع المنتجات أو إدخال مكان توزيع المنتجات يدويًا وكمية المنتجات التي يتم توزيعها على كل متجر.</span><span class="sxs-lookup"><span data-stu-id="dfb12-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="dfb12-106">لا يتضمن الإجراء عملية إعداد البيانات التي يمكن استخدامها في ‏‫توزيع البضائع‬، مثل قواعد التزويد والتدرجات الهرمية للمؤسسات وتخزين الأوزان.</span><span class="sxs-lookup"><span data-stu-id="dfb12-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="dfb12-107">ويستخدم هذا الإجراء شركة العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="dfb12-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="dfb12-108">انتقل إلى "كافة أوامر الشراء".</span><span class="sxs-lookup"><span data-stu-id="dfb12-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="dfb12-109">حدد أمر مبيعات في القائمة وانقر على الارتباط لفتح الأمر.</span><span class="sxs-lookup"><span data-stu-id="dfb12-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="dfb12-110">في جزء الإجراءات، انقر فوق "البيع بالتجزئة والتجارة".</span><span class="sxs-lookup"><span data-stu-id="dfb12-110">On the Action Pane, click Retail and Commerce.</span></span>
4. <span data-ttu-id="dfb12-111">انقر فوق توزيع البضائع.</span><span class="sxs-lookup"><span data-stu-id="dfb12-111">Click Cross docking.</span></span>
5. <span data-ttu-id="dfb12-112">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="dfb12-112">Click Edit.</span></span>
    * <span data-ttu-id="dfb12-113">يمكن استخدام الفئة لتصفية الأصناف الموجودة في قسم "البنود".</span><span class="sxs-lookup"><span data-stu-id="dfb12-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="dfb12-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="dfb12-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="dfb12-115">في حقل "‏‫كمية توزيع البضائع‬"، اكتب قيمة لتعيين مقدار الكمية المُشتراة من المنتج المحدد التي ينبغي توزيعها.</span><span class="sxs-lookup"><span data-stu-id="dfb12-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="dfb12-116">في حقل "‏‫الكمية الإضافية لتوزيع البضائع"، قم بإدخال قيمة لتحديد الكميات التي سيتم توزيعها للمنتجات المتوفرة المُشتراة</span><span class="sxs-lookup"><span data-stu-id="dfb12-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="dfb12-117">في حقل "التوزيع"، أدخل "‏‫وزن الموقع".</span><span class="sxs-lookup"><span data-stu-id="dfb12-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="dfb12-118">يمكنك تحديد أنواع أخرى لاستخدام قواعد مختلفة للتوزيع.</span><span class="sxs-lookup"><span data-stu-id="dfb12-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="dfb12-119">في حقل "‏‫التدرج الهرمي للتزويد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dfb12-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="dfb12-120">حدد "نعم" في حقل "‏‫مراعاة عمليات الفرز‬".</span><span class="sxs-lookup"><span data-stu-id="dfb12-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="dfb12-121">انقر فوق حساب الكميات.</span><span class="sxs-lookup"><span data-stu-id="dfb12-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="dfb12-122">انقر فوق إنشاء أمر.</span><span class="sxs-lookup"><span data-stu-id="dfb12-122">Click Create order.</span></span>
14. <span data-ttu-id="dfb12-123">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="dfb12-123">Click Yes.</span></span>
15. <span data-ttu-id="dfb12-124">في القائمة، ابحث عن المستودع الذي استلم المنتجات وحدده</span><span class="sxs-lookup"><span data-stu-id="dfb12-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="dfb12-125">انقر فوق الأمر لعرض الأوامر التي تم إنشاؤها للمستودع المحدد</span><span class="sxs-lookup"><span data-stu-id="dfb12-125">Click Order to view the orders that got created for the selected warehouse</span></span>

