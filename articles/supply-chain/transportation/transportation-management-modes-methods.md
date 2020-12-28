---
title: طرق وأوضاع أداره النقل
description: يوضح هذا الموضوع كيفيه اعداد أوضاع وأساليب أداره النقل.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: ceb3930cdb7764f846e88edfff6906b902a7f5fa
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/29/2020
ms.locfileid: "4421833"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="a3558-103">طرق وأوضاع أداره النقل</span><span class="sxs-lookup"><span data-stu-id="a3558-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3558-104">وضع النقل يمثل نموذج النقل الذي يستخدمه الناقل لعمليات تسليم الشحن، مثل أقل من حمولة شاحنة (LTL) أو حمولة شاحنة (TL) أو طرد.</span><span class="sxs-lookup"><span data-stu-id="a3558-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="a3558-105">وضع النقل يمثل أسلوب النقل الذي يستخدمه الناقل لعمليات تسليم الشحن، مثل الهواء أو الأرض والمحيط والسكة الحديد.</span><span class="sxs-lookup"><span data-stu-id="a3558-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="a3558-106">يتم استخدام طرق النقل والأوضاع في العديد من السياقات.</span><span class="sxs-lookup"><span data-stu-id="a3558-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="a3558-107">يتم استخدام الأوضاع فقط في خطط المسارات ، بينما يتم استخدام كل من الوضعين وأساليب النقل عند اعداد شركات الشحن وخدمات الناقل.</span><span class="sxs-lookup"><span data-stu-id="a3558-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="a3558-108">لا توجد علاقة صريحه أو تدرج هرمي بين أساليب الأوضاع ووسائل النقل.</span><span class="sxs-lookup"><span data-stu-id="a3558-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="a3558-109">إنشاء وضع</span><span class="sxs-lookup"><span data-stu-id="a3558-109">Create a mode</span></span>

<span data-ttu-id="a3558-110">لإنشاء وضع، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="a3558-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="a3558-111">انتقل إلى **إدارة النقل \> الإعداد \> شركات النقل \> الوضع**.</span><span class="sxs-lookup"><span data-stu-id="a3558-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="a3558-112">حدد **جديد** لإنشاء وضع جديد.</span><span class="sxs-lookup"><span data-stu-id="a3558-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="a3558-113">أدخل هوية فريدة واسمًا وصفيًا للوضع.</span><span class="sxs-lookup"><span data-stu-id="a3558-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="a3558-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a3558-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="a3558-115">إنشاء أسلوبالنقل</span><span class="sxs-lookup"><span data-stu-id="a3558-115">Create a transportation method</span></span>

<span data-ttu-id="a3558-116">لإنشاء أسلوب نقل، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="a3558-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="a3558-117">انتقل إلى **إدارة النقل \> إعداد \> شركات النقل \> طرق النقل**.</span><span class="sxs-lookup"><span data-stu-id="a3558-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="a3558-118">حدد **جديد** لإنشاء أسلوب نقل جديد.</span><span class="sxs-lookup"><span data-stu-id="a3558-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="a3558-119">أدخل هوية فريدة واسمًا وصفيًا لأسلوب النقل.</span><span class="sxs-lookup"><span data-stu-id="a3558-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="a3558-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a3558-120">Close the page.</span></span>
