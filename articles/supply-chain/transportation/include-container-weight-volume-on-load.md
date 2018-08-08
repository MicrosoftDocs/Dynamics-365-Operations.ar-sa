---
title: "تضمين وزن وحجم الحاوية على الحمولة"
description: "يصف هذا الموضوع كيفية إعداد وتطبيق وظيفة تضمين وزن وحجم الحاوية على الحمولات‬."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: adbaa379889d373d597b2f6882b78f82bd71ae57
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="c494b-103">تضمين وزن وحجم الحاوية على الحمولة</span><span class="sxs-lookup"><span data-stu-id="c494b-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c494b-104">توفر وظيفة تضمين وزن وحجم الحاوية على الحمولة تمثيلًا واضحًا لإجمالي وزن وحجم الحاويات التي سيتم تحميلها.</span><span class="sxs-lookup"><span data-stu-id="c494b-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="c494b-105">تحتوي الحمولة على شحنة واحدة أو شحنات متعددة، وتحتوي هذه الشحنات على أصناف مميزة تنتمي إلى أمر مبيعات واحد أو أوامر مبيعات متعددة.</span><span class="sxs-lookup"><span data-stu-id="c494b-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="c494b-106">يتم تخزين الأصناف داخل حاوية، ويتم تحميل الحاويات على حمولة.</span><span class="sxs-lookup"><span data-stu-id="c494b-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="c494b-107">وباستطاعة الأصناف الموجودة خارج الحاوية أن تكون هي أيضًا جزءًا من الحمولة.</span><span class="sxs-lookup"><span data-stu-id="c494b-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="c494b-108">استنادًا إلى هذه الشروط، يقوم النظام بحساب قيم الوزن والحجم على الحمولة من خلال أخذ حجم ووزن الحاويات والأصناف في الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="c494b-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="c494b-109">إذا لم تكن القيم المحسوبة دقيقة، فيمكنك ضبطها عن طريق إدخال القيم الفعلية للوزن والحجم على الحمولة.</span><span class="sxs-lookup"><span data-stu-id="c494b-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="c494b-110">يتم استخدام قيم الوزن والحجم في عمليات إدارة النقل.</span><span class="sxs-lookup"><span data-stu-id="c494b-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="c494b-111">على سبيل المثال، يتم استخدام القيم الموجودة في لوحة عمل مسار الأسعار‬، حيث تساعد في تحديد سعر ومسار الحمولات، ويتم استخدامها أيضًا لطرق دفع النقل وتسجيل دخول السائق.</span><span class="sxs-lookup"><span data-stu-id="c494b-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="c494b-112">أين يتم التطبيق</span><span class="sxs-lookup"><span data-stu-id="c494b-112">Where it applies</span></span>

<span data-ttu-id="c494b-113">تنطبق وظيفة تضمين وزن وحجم الحاوية على حمولة في عمليات إدارة النقل، مثل لوحة عمل مسار الأسعار‬ وطرق دفع النقل وتسجيل دخول السائق.‬</span><span class="sxs-lookup"><span data-stu-id="c494b-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="c494b-114">كيف يتم إعدادها</span><span class="sxs-lookup"><span data-stu-id="c494b-114">How it is set up</span></span>

<span data-ttu-id="c494b-115">يتم حساب عدد الحاويات التي يجب اخذها في الاعتبار لحمولة ما استنادًا إلى وزن وحجم الحاوية وإلى النسبة المئوية المستخدمة من الحاوية.</span><span class="sxs-lookup"><span data-stu-id="c494b-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="c494b-116">لتعيين الوزن والحجم لحاوية، انقر فوق **إدارة المستودعات** \> **الإعداد** \> **الحاويات** \> **أنواع الحاويات**.</span><span class="sxs-lookup"><span data-stu-id="c494b-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="c494b-117">لتعيين النسبة المئوية لاستخدام الحاوية، انقر فوق **إدارة المستودعات** \> **الإعداد** \> **الحاويات‏‎** \> **مجموعات الحاويات**، ثم أدخل قيمة في حقل **النسبة المئوية لاستخدام الحاوية‬**.</span><span class="sxs-lookup"><span data-stu-id="c494b-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>

