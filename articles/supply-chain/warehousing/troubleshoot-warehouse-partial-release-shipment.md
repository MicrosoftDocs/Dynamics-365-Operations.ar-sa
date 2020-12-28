---
title: استكشاف أخطاء الإصدار الجزئي والشحنات الجزئية وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات الإصدار الجزئية والشحنات الجزئية في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645938"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="b33ec-103">استكشاف أخطاء الإصدار الجزئي والشحنات الجزئية وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="b33ec-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b33ec-104">يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات الإصدار الجزئية والشحنات الجزئية في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b33ec-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="b33ec-105">وتظل حاله إصدار أمر المبيعات قد تم إصدارها جزئيا حتى بعد ان تتم فوتره أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b33ec-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b33ec-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="b33ec-106">Issue description</span></span>

<span data-ttu-id="b33ec-107">أمر المبيعات هو أمر تسليم ، ولكن صنف واحد أو أكثر له له وضع تسليم مختلف.</span><span class="sxs-lookup"><span data-stu-id="b33ec-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="b33ec-108">بعد فوتره الأمر ، يبقي له حاله إصدار تم *إصدارها جزئيا*.</span><span class="sxs-lookup"><span data-stu-id="b33ec-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="b33ec-109">علي سبيل المثال ، يكون لأمر التوريد صنفين: أحدهما بالنسبة للتسليم والاخر للالتقاط.</span><span class="sxs-lookup"><span data-stu-id="b33ec-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="b33ec-110">تم اجراء التسليم والتقاط.</span><span class="sxs-lookup"><span data-stu-id="b33ec-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="b33ec-111">ولذلك ، تمت فوتره كلا البندين.</span><span class="sxs-lookup"><span data-stu-id="b33ec-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="b33ec-112">ومع ذلك ، لا تزال حاله الإصدار ظاهره علي انها تم *إصدارها جزئيا*، وهي مضلله.</span><span class="sxs-lookup"><span data-stu-id="b33ec-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b33ec-113">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="b33ec-113">Issue resolution</span></span>

<span data-ttu-id="b33ec-114">تنطبق حاله الإصدار فقط علي بنود الأمر التي يتم فيها تمكين الأصناف لأداره المستودعات.</span><span class="sxs-lookup"><span data-stu-id="b33ec-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="b33ec-115">لذلك تبقي حاله الإصدار تم *إصدارها جزئيا* في هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="b33ec-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="b33ec-116">قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه.</span><span class="sxs-lookup"><span data-stu-id="b33ec-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="b33ec-117">ويمكن أضافه ملحق كجزء من كشف التعبئة وعمليه الفوترة لتحديث حاله الإصدار.</span><span class="sxs-lookup"><span data-stu-id="b33ec-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
