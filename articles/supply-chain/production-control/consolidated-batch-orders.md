---
title: الأوامر الدفعية المجمعة
description: تصف هذه المقالة مفهوم الأوامر الدُفعية المجمعة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49c2df19168855e6e6ab9ff061bcdce698947b20
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569441"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="70859-103">الأوامر الدفعية المجمعة</span><span class="sxs-lookup"><span data-stu-id="70859-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70859-104">تصف هذه المقالة مفهوم الأوامر الدُفعية المجمعة.</span><span class="sxs-lookup"><span data-stu-id="70859-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="70859-105">يعتبر الصنف المجمع الذي تم إنتاجه صنفًا رئيسيًا، حيث يُعد الصنف المعبأ صنفًا تابعًا.</span><span class="sxs-lookup"><span data-stu-id="70859-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="70859-106">ويتم التعبير عن العلاقة بين الصنف المجمع والصنف المعبأ في تحويل الصنف المجمع.</span><span class="sxs-lookup"><span data-stu-id="70859-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="70859-107">ويتم تحديد تحويل الصنف المجمع في الصنف المجمع نفسه.</span><span class="sxs-lookup"><span data-stu-id="70859-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="70859-108">ويمكن تعبئة الأصناف المعبأة في حاويات بحجم واحد أو بأحجام متعددة تعتبر وحدة واحدة.</span><span class="sxs-lookup"><span data-stu-id="70859-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="70859-109">ومن خلال تجميع الأوامر لعنصر مجمع، يمكنك مشاهدة جميع الأوامر الدُفعية ذات الصلة في طريقة عرض واحدة تساعدك في تحديد أي عمل متبقٍ يجب إكماله.</span><span class="sxs-lookup"><span data-stu-id="70859-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="70859-110">يمكن أن يحتوي الأمر الدفعي المجمع على أي مجموعة من الأوامر التالية:</span><span class="sxs-lookup"><span data-stu-id="70859-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="70859-111">أمر مجمع واحد وأوامر معبأة متعددة</span><span class="sxs-lookup"><span data-stu-id="70859-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="70859-112">أوامر مجمعة متعددة وأوامر معبأة متعددة</span><span class="sxs-lookup"><span data-stu-id="70859-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="70859-113">أوامر مجمعة متعددة وأمر معبأ واحد</span><span class="sxs-lookup"><span data-stu-id="70859-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="70859-114">الأوامر المعبأة فقط.</span><span class="sxs-lookup"><span data-stu-id="70859-114">Only packed orders</span></span>




