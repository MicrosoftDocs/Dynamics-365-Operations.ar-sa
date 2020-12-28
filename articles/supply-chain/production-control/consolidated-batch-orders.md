---
title: الأوامر الدفعية المجمعة
description: تصف هذه المقالة مفهوم الأوامر الدُفعية المجمعة.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: faeb90aa3366a58b746c0b397dd950bfb8c9024f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421536"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="bec21-103">الأوامر الدفعية المجمعة</span><span class="sxs-lookup"><span data-stu-id="bec21-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bec21-104">تصف هذه المقالة مفهوم الأوامر الدُفعية المجمعة.</span><span class="sxs-lookup"><span data-stu-id="bec21-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="bec21-105">يعتبر الصنف المجمع الذي تم إنتاجه صنفًا رئيسيًا، حيث يُعد الصنف المعبأ صنفًا تابعًا.</span><span class="sxs-lookup"><span data-stu-id="bec21-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="bec21-106">ويتم التعبير عن العلاقة بين الصنف المجمع والصنف المعبأ في تحويل الصنف المجمع.</span><span class="sxs-lookup"><span data-stu-id="bec21-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="bec21-107">ويتم تحديد تحويل الصنف المجمع في الصنف المجمع نفسه.</span><span class="sxs-lookup"><span data-stu-id="bec21-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="bec21-108">ويمكن تعبئة الأصناف المعبأة في حاويات بحجم واحد أو بأحجام متعددة تعتبر وحدة واحدة.</span><span class="sxs-lookup"><span data-stu-id="bec21-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="bec21-109">ومن خلال تجميع الأوامر لعنصر مجمع، يمكنك مشاهدة جميع الأوامر الدُفعية ذات الصلة في طريقة عرض واحدة تساعدك في تحديد أي عمل متبقٍ يجب إكماله.</span><span class="sxs-lookup"><span data-stu-id="bec21-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="bec21-110">يمكن أن يحتوي الأمر الدفعي المجمع على أي مجموعة من الأوامر التالية:</span><span class="sxs-lookup"><span data-stu-id="bec21-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="bec21-111">أمر مجمع واحد وأوامر معبأة متعددة</span><span class="sxs-lookup"><span data-stu-id="bec21-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="bec21-112">أوامر مجمعة متعددة وأوامر معبأة متعددة</span><span class="sxs-lookup"><span data-stu-id="bec21-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="bec21-113">أوامر مجمعة متعددة وأمر معبأ واحد</span><span class="sxs-lookup"><span data-stu-id="bec21-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="bec21-114">الأوامر المعبأة فقط.</span><span class="sxs-lookup"><span data-stu-id="bec21-114">Only packed orders</span></span>




