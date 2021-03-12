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
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b9b548212c6f1f3faac56cd7ca182d84cc339bd2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973900"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="889a1-103">طرق وأوضاع أداره النقل</span><span class="sxs-lookup"><span data-stu-id="889a1-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="889a1-104">وضع النقل يمثل نموذج النقل الذي يستخدمه الناقل لعمليات تسليم الشحن، مثل أقل من حمولة شاحنة (LTL) أو حمولة شاحنة (TL) أو طرد.</span><span class="sxs-lookup"><span data-stu-id="889a1-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="889a1-105">وضع النقل يمثل أسلوب النقل الذي يستخدمه الناقل لعمليات تسليم الشحن، مثل الهواء أو الأرض والمحيط والسكة الحديد.</span><span class="sxs-lookup"><span data-stu-id="889a1-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="889a1-106">يتم استخدام طرق النقل والأوضاع في العديد من السياقات.</span><span class="sxs-lookup"><span data-stu-id="889a1-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="889a1-107">يتم استخدام الأوضاع فقط في خطط المسارات ، بينما يتم استخدام كل من الوضعين وأساليب النقل عند اعداد شركات الشحن وخدمات الناقل.</span><span class="sxs-lookup"><span data-stu-id="889a1-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="889a1-108">لا توجد علاقة صريحه أو تدرج هرمي بين أساليب الأوضاع ووسائل النقل.</span><span class="sxs-lookup"><span data-stu-id="889a1-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="889a1-109">إنشاء وضع</span><span class="sxs-lookup"><span data-stu-id="889a1-109">Create a mode</span></span>

<span data-ttu-id="889a1-110">لإنشاء وضع، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="889a1-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="889a1-111">انتقل إلى **إدارة النقل \> الإعداد \> شركات النقل \> الوضع**.</span><span class="sxs-lookup"><span data-stu-id="889a1-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="889a1-112">حدد **جديد** لإنشاء وضع جديد.</span><span class="sxs-lookup"><span data-stu-id="889a1-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="889a1-113">أدخل هوية فريدة واسمًا وصفيًا للوضع.</span><span class="sxs-lookup"><span data-stu-id="889a1-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="889a1-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="889a1-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="889a1-115">إنشاء أسلوبالنقل</span><span class="sxs-lookup"><span data-stu-id="889a1-115">Create a transportation method</span></span>

<span data-ttu-id="889a1-116">لإنشاء أسلوب نقل، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="889a1-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="889a1-117">انتقل إلى **إدارة النقل \> إعداد \> شركات النقل \> طرق النقل**.</span><span class="sxs-lookup"><span data-stu-id="889a1-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="889a1-118">حدد **جديد** لإنشاء أسلوب نقل جديد.</span><span class="sxs-lookup"><span data-stu-id="889a1-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="889a1-119">أدخل هوية فريدة واسمًا وصفيًا لأسلوب النقل.</span><span class="sxs-lookup"><span data-stu-id="889a1-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="889a1-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="889a1-120">Close the page.</span></span>
