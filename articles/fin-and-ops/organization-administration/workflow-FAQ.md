---
title: الأسئلة المتداولة حول سير العمل
description: يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509281"
---
# <a name="workflow-system"></a><span data-ttu-id="62189-103">نظام سير العمل</span><span class="sxs-lookup"><span data-stu-id="62189-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62189-104">يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="62189-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="62189-105">الإخطارات</span><span class="sxs-lookup"><span data-stu-id="62189-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="62189-106">لماذا أتلقى إخطارات متعددة عند رفض عنصر عمل؟</span><span class="sxs-lookup"><span data-stu-id="62189-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="62189-107">عند رفض عنصر عمل، يتم إكمال هذا العنصر كعنصر مرفوض.</span><span class="sxs-lookup"><span data-stu-id="62189-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="62189-108">ويتم إنشاء عنصر عمل آخر وتعيينه إلى المنشئ.</span><span class="sxs-lookup"><span data-stu-id="62189-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="62189-109">وهذا يعني إرسال إخطار إلى المنشئ يتعلق بعنصر العمل المرفوض وإخطار منفصل إلى المستخدم المعيّن إلى عنصر العمل الجديد "التغيير المطلوب‬".</span><span class="sxs-lookup"><span data-stu-id="62189-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="62189-110">يتعلق كل إخطار بعنصر عمل مختلف، ولكن التشابه قد يسبب الإرباك.</span><span class="sxs-lookup"><span data-stu-id="62189-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="62189-111">نحن بصدد البحث عن طرق لتحسين هذا الأمر في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="62189-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="62189-112">لماذا يفشل تصدير عمليات سير العمل؟</span><span class="sxs-lookup"><span data-stu-id="62189-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="62189-113">يوجد حاليًا قيد في ميزة تصدير عمليات سير العمل يمنع تجاوز أسماء عمليات سير العمل 48 حرفًا.</span><span class="sxs-lookup"><span data-stu-id="62189-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="62189-114">قد يؤدي استخدام اسم أطول من 48 حرفًا إلى ظهور الخطأ "فشل الخادم في مصادقة الطلب" و/أو منع تصدير ملف بدون نوع ملف.</span><span class="sxs-lookup"><span data-stu-id="62189-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="62189-115">يوفر منشور المدونة التالي المزيد من التفاصيل [استكشاف أخطاء تصدير سير العمل وإصلاحها](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="62189-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
