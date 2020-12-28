---
title: حالات إدارة النقل
description: يوضح هذا الموضوع كيفيه إنشاء حاله نقل وتعيين هذه الحالة إلى حاله الناقل.
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
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3f7d471771ec2b4703d878fbf395cd90902b6669
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/29/2020
ms.locfileid: "4421831"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="c4451-103">حالات إدارة النقل</span><span class="sxs-lookup"><span data-stu-id="c4451-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4451-104">قم بإعداد أكواد السجل الرئيسي لحالات النقل لتفسير الأكواد المقدمة من شركات الشحن.</span><span class="sxs-lookup"><span data-stu-id="c4451-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="c4451-105">يتيح لك ذلك امكانيه التكامل مع شركات الشحن لتقديم حاله.</span><span class="sxs-lookup"><span data-stu-id="c4451-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="c4451-106">يمكن أن تساعدك حالة النقل التي تقدمها لرمز حالة رئيسية نقل على تعقب حالة التحميل أو شحن حاوية.</span><span class="sxs-lookup"><span data-stu-id="c4451-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="c4451-107">يمكن تحديث حاله النقل الخاصة بالتحميل أو الشحن أو الحاوية فقط من خلال تكامل البيانات وليس يدويا من خلال واجهه المستخدم.</span><span class="sxs-lookup"><span data-stu-id="c4451-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="c4451-108">إنشاء حالة نقل</span><span class="sxs-lookup"><span data-stu-id="c4451-108">Create a transportation status</span></span>

<span data-ttu-id="c4451-109">لإنشاء حال نقل، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="c4451-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="c4451-110">انتقل إلى **إدارة النقل \> إعداد \> السجلات الرئيسية لحالة النقل**.</span><span class="sxs-lookup"><span data-stu-id="c4451-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="c4451-111">حدد **جديد** لإنشاء السجل الرئيسي لحالة النقل.</span><span class="sxs-lookup"><span data-stu-id="c4451-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="c4451-112">في الحقل **السجل الرئيسي لحالة النقل**، أدخل كودًا فريدًا لحالة النقل.</span><span class="sxs-lookup"><span data-stu-id="c4451-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="c4451-113">في الحقل **نوع النقل**، حدد اما *شركه الشحن* أو *المركز* كنوع النقل.</span><span class="sxs-lookup"><span data-stu-id="c4451-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="c4451-114">ادخل الاسم وحاله النقل.</span><span class="sxs-lookup"><span data-stu-id="c4451-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="c4451-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c4451-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="c4451-116">تعيين حاله النقل إلى حاله شركة النقل</span><span class="sxs-lookup"><span data-stu-id="c4451-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="c4451-117">لتعيين حاله النقل إلى حاله شركة النقل، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="c4451-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="c4451-118">انتقل إلى **إدارة النقل \> إعداد \> شركات النقل \> حالة النقل لشركة النقل**.</span><span class="sxs-lookup"><span data-stu-id="c4451-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="c4451-119">حدد **جديد** لتعيين رمز من شركة شحن إلى رمز حالة نقل رئيسية.</span><span class="sxs-lookup"><span data-stu-id="c4451-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="c4451-120">حدد معرف فريد لشركة الشحن وخدمة شركة النقل.</span><span class="sxs-lookup"><span data-stu-id="c4451-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="c4451-121">حدد رمز الحالة النقل التي تريد تعيينها إلى كود شركة الشحن المحددة.</span><span class="sxs-lookup"><span data-stu-id="c4451-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="c4451-122">أدخل الكود الخارجي المستخدمة بواسطة شركة الشحن.</span><span class="sxs-lookup"><span data-stu-id="c4451-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="c4451-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c4451-123">Close the page.</span></span>