---
title: الأسئلة المتداولة حول سير العمل
description: يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/01/2019
ms.locfileid: "773193"
---
# <a name="workflow-system"></a><span data-ttu-id="a5dde-103">نظام سير العمل</span><span class="sxs-lookup"><span data-stu-id="a5dde-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5dde-104">يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a5dde-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="a5dde-105">الإخطارات</span><span class="sxs-lookup"><span data-stu-id="a5dde-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="a5dde-106">لماذا أتلقى إخطارات متعددة عند رفض عنصر عمل؟</span><span class="sxs-lookup"><span data-stu-id="a5dde-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="a5dde-107">عند رفض عنصر عمل، يتم إكمال هذا العنصر كعنصر مرفوض.</span><span class="sxs-lookup"><span data-stu-id="a5dde-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="a5dde-108">ويتم إنشاء عنصر عمل آخر وتعيينه إلى المنشئ.</span><span class="sxs-lookup"><span data-stu-id="a5dde-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="a5dde-109">وهذا يعني إرسال إخطار إلى المنشئ يتعلق بعنصر العمل المرفوض وإخطار منفصل إلى المستخدم المعيّن إلى عنصر العمل الجديد "التغيير المطلوب‬".</span><span class="sxs-lookup"><span data-stu-id="a5dde-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="a5dde-110">يتعلق كل إخطار بعنصر عمل مختلف، ولكن التشابه قد يسبب الإرباك.</span><span class="sxs-lookup"><span data-stu-id="a5dde-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="a5dde-111">نحن بصدد البحث عن طرق لتحسين هذا الأمر في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="a5dde-111">We are looking at ways to improve this in a future release.</span></span>
