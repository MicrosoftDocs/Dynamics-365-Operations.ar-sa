---
title: "شحن أحد الأوامر من متجر آخر"
description: "يصف هذا الموضوع ميزة إرسال شحنة."
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail Version
ms.translationtype: HT
ms.sourcegitcommit: 986ec7835dac52c326085c47313205d08b1bafa8
ms.openlocfilehash: d217bc31ad9d93c5440e5329f7b7327d089137f4
ms.contentlocale: ar-sa
ms.lasthandoff: 10/10/2017

---

# <a name="ship-an-order-from-a-different-store"></a><span data-ttu-id="03cb9-103">شحن أحد الأوامر من متجر آخر</span><span class="sxs-lookup"><span data-stu-id="03cb9-103">Ship an order from a different store</span></span>

<span data-ttu-id="03cb9-104">مع ميزة إرسال شحنة في Dynamics 365 for Retail، يمكن إجراء أوامر العملاء من متجر وشحنها من متجر آخر.</span><span class="sxs-lookup"><span data-stu-id="03cb9-104">With the Charge send feature in Dynamics 365 for Retail, customer orders can be placed in one store and shipped from another store.</span></span> <span data-ttu-id="03cb9-105">فأوامر العميل في نقطة البيع (POS) تدعم العديد من خيارات التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="03cb9-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="03cb9-106">تتضمن بعض أمثلة خيارات التنفيذ ما يلي:</span><span class="sxs-lookup"><span data-stu-id="03cb9-106">Some examples of fulfillment options include:</span></span>
-   <span data-ttu-id="03cb9-107">الاستلام من المتجر نفسه بتاريخ مختلف.</span><span class="sxs-lookup"><span data-stu-id="03cb9-107">Pick up from the same store on a different date.</span></span>
-   <span data-ttu-id="03cb9-108">الاستلام من متجر آخر بنفس التاريخ أو بتاريخ مختلف.</span><span class="sxs-lookup"><span data-stu-id="03cb9-108">Pick up from a different store on the same date or a different date.</span></span>
-   <span data-ttu-id="03cb9-109">الشحن من مستودع الشحن الافتراضي المُعين للمتجر والتسليم في تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="03cb9-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="03cb9-110">تستخدم ميزة إرسال الشحنة هذه عمليات نقاط البيع التالية: شحن جميع المنتجات وشحن المنتجات المحددة.</span><span class="sxs-lookup"><span data-stu-id="03cb9-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="03cb9-111">يسمح هذا لموظف المتجر بتحديد موقع "الشحن من" الذي يمكن تلبية الأمر أو سطر الأمر منه.</span><span class="sxs-lookup"><span data-stu-id="03cb9-111">This allows the store clerk to select the “ship from” location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="03cb9-112">بشكل افتراضي، يكون موقع "الشحن من" هو مستودع الشحن المقترن بالمتجر.</span><span class="sxs-lookup"><span data-stu-id="03cb9-112">By default, the “ship from” location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="03cb9-113">ومع ذلك، يمكن لموظف المتجر تغيير هذا الموقع وتحديد أي متجر يكون محددًا في مجموعة محدد مواقع المتاجر المُعينة للمتجر.</span><span class="sxs-lookup"><span data-stu-id="03cb9-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span> 

<span data-ttu-id="03cb9-114">وتبقى إمكانية تحديد عناوين "الشحن إلى" دون تغيير.</span><span class="sxs-lookup"><span data-stu-id="03cb9-114">The ability to select “ship to” addresses remains unchanged.</span></span> 

<span data-ttu-id="03cb9-115">تستند طرق الشحن التي يمكن استخدامها لتنفيذ سطر الأمر إلى تكوين أوضاع التسليم الصالحة للمنتجات والعناوين.</span><span class="sxs-lookup"><span data-stu-id="03cb9-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="03cb9-116">ونظرًا لأن القواعد الخاصة بأوضاع التسليم الصالحة يتم الاحتفاظ بها في إدارة البيع بالتجزئة فقط، يقوم عميل نقطة البيع باتصال في الوقت الفعلي لمعرفة أوضاع التسليم الصالحة لبند شحن.</span><span class="sxs-lookup"><span data-stu-id="03cb9-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span> 

