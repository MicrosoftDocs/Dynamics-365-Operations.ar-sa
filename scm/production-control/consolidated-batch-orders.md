---
title: "الأوامر الدفعية المجمعة"
description: "تصف هذه المقالة مفهوم الأوامر الدُفعية المجمعة."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 3ca9c920ea333bd21defebc29b40243d3a618a3d
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="consolidated-batch-orders"></a><span data-ttu-id="f9fa4-103">الأوامر الدفعية المجمعة</span><span class="sxs-lookup"><span data-stu-id="f9fa4-103">Consolidated batch orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f9fa4-104">تصف هذه المقالة مفهوم الأوامر الدُفعية المجمعة.</span><span class="sxs-lookup"><span data-stu-id="f9fa4-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="f9fa4-105">يعتبر الصنف المجمع الذي تم إنتاجه صنفًا رئيسيًا، حيث يُعد الصنف المعبأ صنفًا تابعًا.</span><span class="sxs-lookup"><span data-stu-id="f9fa4-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="f9fa4-106">ويتم التعبير عن العلاقة بين الصنف المجمع والصنف المعبأ في تحويل الصنف المجمع.</span><span class="sxs-lookup"><span data-stu-id="f9fa4-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="f9fa4-107">ويتم تحديد تحويل الصنف المجمع في الصنف المجمع نفسه.</span><span class="sxs-lookup"><span data-stu-id="f9fa4-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="f9fa4-108">ويمكن تعبئة الأصناف المعبأة في حاويات بحجم واحد أو بأحجام متعددة تعتبر وحدة واحدة.</span><span class="sxs-lookup"><span data-stu-id="f9fa4-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="f9fa4-109">ومن خلال تجميع الأوامر لعنصر مجمع، يمكنك مشاهدة جميع الأوامر الدُفعية ذات الصلة في طريقة عرض واحدة تساعدك في تحديد أي عمل متبقٍ يجب إكماله.</span><span class="sxs-lookup"><span data-stu-id="f9fa4-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="f9fa4-110">يمكن أن يحتوي الأمر الدفعي المجمع على أي مجموعة من الأوامر التالية:</span><span class="sxs-lookup"><span data-stu-id="f9fa4-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="f9fa4-111">أمر مجمع واحد وأوامر معبأة متعددة</span><span class="sxs-lookup"><span data-stu-id="f9fa4-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="f9fa4-112">أوامر مجمعة متعددة وأوامر معبأة متعددة</span><span class="sxs-lookup"><span data-stu-id="f9fa4-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="f9fa4-113">أوامر مجمعة متعددة وأمر معبأ واحد</span><span class="sxs-lookup"><span data-stu-id="f9fa4-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="f9fa4-114">الأوامر المعبأة فقط.</span><span class="sxs-lookup"><span data-stu-id="f9fa4-114">Only packed orders</span></span>





