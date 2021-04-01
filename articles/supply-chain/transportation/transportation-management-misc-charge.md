---
title: المصاريف المتنوعة لأداره النقل
description: يوضح هذا الموضوع كيفيه ربط تكلفة النقل التي تم إنشاؤها بكود التكلفة.
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
ms.openlocfilehash: 4f58db216176832d61bdafbe43831ededd3dd6dc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233405"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="71124-103">المصاريف المتنوعة لأداره النقل</span><span class="sxs-lookup"><span data-stu-id="71124-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71124-104">كما هو الحال مع جميع التكاليف المتنوعة، يجب ربط تكلفة النقل التي تم إنشاؤها بكود التكلفة.</span><span class="sxs-lookup"><span data-stu-id="71124-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="71124-105">والا ، فلن تتم اضافتها مره أخرى إلى الأمر كتكلفة متنوعة.</span><span class="sxs-lookup"><span data-stu-id="71124-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="71124-106">يحدد **كود التكلفة** كيفيه حساب المصاريف فيما يتعلق بالأمر وبند الأمر الذي تتم اضافته اليه.</span><span class="sxs-lookup"><span data-stu-id="71124-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="71124-107">انتقل إلى **أداره النقل > اعداد > التقييم > المصاريف المتنوعة** لتحديد معايير التاهيل التي تحدد متى يتم تطبيق **كود التكلفة** علي التكلفة.</span><span class="sxs-lookup"><span data-stu-id="71124-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="71124-108">يجب ان يكون لديك اعداد واحد علي الأقل لكل اعداد **وحده المصاريف المرتبطة** ( *العميل* و *المورد*) الذي يتم فيه تعيين **نوع المصاريف المتنوعة** علي *بلا*.</span><span class="sxs-lookup"><span data-stu-id="71124-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="71124-109">في حاله فقد هذا الأمر ، *لن* تتم أضافه المصاريف المتنوعة إلى الأمر.</span><span class="sxs-lookup"><span data-stu-id="71124-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]