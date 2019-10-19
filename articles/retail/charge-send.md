---
title: شحن أوامر من متجر آخر باستخدام ميزة إرسال شحنة
description: يصف هذا الموضوع ميزة إرسال شحنة.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 088f55e5605c99f69852b4d6811b5c5504f267a2
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019452"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a><span data-ttu-id="4ab23-103">شحن أوامر من متجر آخر باستخدام ميزة إرسال شحنة</span><span class="sxs-lookup"><span data-stu-id="4ab23-103">Ship orders from another store by using the Charge send feature</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4ab23-104">باستخدام ميزة إرسال الشحنة في Retail، يمكن تقديم طلبات العملاء في متجر وشحنها من متجر العملاء.</span><span class="sxs-lookup"><span data-stu-id="4ab23-104">With the Charge send feature in Retail, customer orders can be placed in one store and shipped from another store.</span></span>

<span data-ttu-id="4ab23-105">فأوامر العميل في نقطة البيع (POS) تدعم العديد من خيارات التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="4ab23-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="4ab23-106">تتضمن بعض أمثلة خيارات التنفيذ ما يلي:</span><span class="sxs-lookup"><span data-stu-id="4ab23-106">Some examples of fulfillment options include:</span></span>

- <span data-ttu-id="4ab23-107">الاستلام من المتجر نفسه بتاريخ مختلف.</span><span class="sxs-lookup"><span data-stu-id="4ab23-107">Pick up from the same store on a different date.</span></span>
- <span data-ttu-id="4ab23-108">الاستلام من متجر آخر بنفس التاريخ أو بتاريخ مختلف.</span><span class="sxs-lookup"><span data-stu-id="4ab23-108">Pick up from a different store on the same date or a different date.</span></span>
- <span data-ttu-id="4ab23-109">الشحن من مستودع الشحن الافتراضي المُعين للمتجر والتسليم في تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="4ab23-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="4ab23-110">تستخدم ميزة إرسال الشحنة هذه عمليات نقاط البيع التالية: شحن جميع المنتجات وشحن المنتجات المحددة.</span><span class="sxs-lookup"><span data-stu-id="4ab23-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="4ab23-111">يسمح هذا لموظف المتجر بتحديد موقع "الشحن من" الذي يمكن تلبية الأمر أو سطر الأمر منه.</span><span class="sxs-lookup"><span data-stu-id="4ab23-111">This allows the store clerk to select the "ship from" location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="4ab23-112">بشكل افتراضي، موقع "الشحن من" هو مستودع الشحن المقترن بالمتجر.</span><span class="sxs-lookup"><span data-stu-id="4ab23-112">By default, the "ship from" location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="4ab23-113">ومع ذلك، يمكن لموظف المتجر تغيير هذا الموقع وتحديد أي متجر يكون محددًا في مجموعة محدد مواقع المتاجر المُعينة للمتجر.</span><span class="sxs-lookup"><span data-stu-id="4ab23-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span>

<span data-ttu-id="4ab23-114">وتبقى إمكانية تحديد عناوين "الشحن إلى" دون تغيير.</span><span class="sxs-lookup"><span data-stu-id="4ab23-114">The ability to select "ship to" addresses remains unchanged.</span></span>

<span data-ttu-id="4ab23-115">تستند طرق الشحن التي يمكن استخدامها لتنفيذ سطر الأمر إلى تكوين أوضاع التسليم الصالحة للمنتجات والعناوين.</span><span class="sxs-lookup"><span data-stu-id="4ab23-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="4ab23-116">ونظرًا لأن القواعد الخاصة بأوضاع التسليم الصالحة يتم الاحتفاظ بها في إدارة البيع بالتجزئة فقط، يقوم عميل نقطة البيع باتصال في الوقت الفعلي لمعرفة أوضاع التسليم الصالحة لبند شحن.</span><span class="sxs-lookup"><span data-stu-id="4ab23-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span>
