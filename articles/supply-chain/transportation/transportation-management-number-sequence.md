---
title: تسلسل رقم إدارة النقل
description: يوضح هذا الموضوع كيفيه اعداد التسلسلات الرقمية لأداره النقل.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3da757cbf47e0e1af781b720d17a673e19aeb3b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807670"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="8a0f7-103">تسلسل رقم إدارة النقل</span><span class="sxs-lookup"><span data-stu-id="8a0f7-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a0f7-104">استخدم الصفحة **تسلسلات رقميه** في الوحدة النمطية لأداره النقل لاعداد مبدئية احترافية مختلفه.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="8a0f7-105">يتم استخدام أرقام مبدئية بواسطة شركات الشحن لتنظيم تقدم كل شحنه وتعقبها.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="8a0f7-106">قم بإنشاء تسلسل رقمي للإجراءات المتعلقة بالرقم المبدئي</span><span class="sxs-lookup"><span data-stu-id="8a0f7-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="8a0f7-107">لإنشاء تسلسل رقمي لرقم مبدئي ، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="8a0f7-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="8a0f7-108">انتقل إلى **إدارة النقل \> إعداد \> شركات النقل‬‬ \> التسلسلات الرقمية‬**.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="8a0f7-109">حدد **جديد** لإنشاء تسلسل رقمي جديد.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="8a0f7-110">أدخل هوية فريدة واسمًا وصفيًا للتسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="8a0f7-111">في الحقل **نوع التسلسل الرقمي**، يعد *رقم مبدئي* هو الخيار الوحيد.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="8a0f7-112">في الحقل **رقم الشيك**، يعتبر *رقم الفحص* هو الخيار الوحيد ويتم اعداده كمشغل عام.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="8a0f7-113">علي علامة التبويب السريعة **التسلسل**، قم بتوفير معلومات حول التسلسل.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="8a0f7-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="8a0f7-115">ربط تسلسل رقمي بشركه شحن</span><span class="sxs-lookup"><span data-stu-id="8a0f7-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="8a0f7-116">لربط تسلسل رقمي بشركة نقل، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="8a0f7-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="8a0f7-117">انتقل إلى **إدارة النقل \> إعداد \> شركات النقل‬‬ \> شركات الشحن‬‬**.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="8a0f7-118">حدد ناقل شحن.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="8a0f7-119">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-119">Select **Edit**.</span></span>
1. <span data-ttu-id="8a0f7-120">في علامة التبويب السريعة **النظرة العامة**، حدد خيارا في الحقل **التسلسل الرقمي المبدئي**.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="8a0f7-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]