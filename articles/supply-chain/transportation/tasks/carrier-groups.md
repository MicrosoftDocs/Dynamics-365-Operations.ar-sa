---
title: مجموعات شركات النقل
description: يصف هذا الموضوع كيفية إعداد بيانات مجموعات شركة الشحن.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 95517153dda06cecf8e57b1f9b080aa07966c111
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247252"
---
# <a name="carrier-groups"></a><span data-ttu-id="64cf8-103">مجموعات شركات النقل</span><span class="sxs-lookup"><span data-stu-id="64cf8-103">Carrier groups</span></span>

<span data-ttu-id="64cf8-104">مجموعه شركة الشحن هي مجموعه من شركات الشحن وخدمات الناقل.</span><span class="sxs-lookup"><span data-stu-id="64cf8-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="64cf8-105">تحدد كل مجموعه من مجموعات شركات النقل التسلسل المفضل لشركات الشحن وخدمات الناقل التي تنتمي اليها.</span><span class="sxs-lookup"><span data-stu-id="64cf8-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="64cf8-106">في حاله وجود شركات شحن وخدمات ناقل متعددة لنفس مقطع المسار ، يمكنك تحديد مجموعه شركات بدلا من شركه شحن وخدمه ناقل شحن محدده في خطه التوجيه أو دليل المسار.</span><span class="sxs-lookup"><span data-stu-id="64cf8-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="64cf8-107">إنشاء مجموعة شركة النقل</span><span class="sxs-lookup"><span data-stu-id="64cf8-107">Create a carrier group</span></span>

1. <span data-ttu-id="64cf8-108">انتقل إلى **إدارة النقل &gt; إعداد &gt; شركات النقل‬‬ &gt; مجموعة شركة النقل‬‬**.</span><span class="sxs-lookup"><span data-stu-id="64cf8-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="64cf8-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="64cf8-109">Select **New**.</span></span>
1. <span data-ttu-id="64cf8-110">في الحقل **مجموعة شركة النقل**، أدخل معرفًا فريدًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="64cf8-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="64cf8-111">في حقل **الاسم**، أدخل اسمًا وصفيًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="64cf8-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="64cf8-112">علي علامة التبويب السريعة **التفاصيل**، أضف صفا ، ثم حدد شركه شحن وخدمه ناقل لها.</span><span class="sxs-lookup"><span data-stu-id="64cf8-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="64cf8-113">كرر هذه الخطوة حتى تقوم باضافه العديد من الشركات التي تتطلبها للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="64cf8-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="64cf8-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="64cf8-114">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]