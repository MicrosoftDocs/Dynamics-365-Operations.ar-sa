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
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed722ba0c79afa038f1af7b4491f3ff18b052067
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246371"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="074e1-103">الأوامر الدفعية المجمعة</span><span class="sxs-lookup"><span data-stu-id="074e1-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="074e1-104">تصف هذه المقالة مفهوم الأوامر الدُفعية المجمعة.</span><span class="sxs-lookup"><span data-stu-id="074e1-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="074e1-105">يعتبر الصنف المجمع الذي تم إنتاجه صنفًا رئيسيًا، حيث يُعد الصنف المعبأ صنفًا تابعًا.</span><span class="sxs-lookup"><span data-stu-id="074e1-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="074e1-106">ويتم التعبير عن العلاقة بين الصنف المجمع والصنف المعبأ في تحويل الصنف المجمع.</span><span class="sxs-lookup"><span data-stu-id="074e1-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="074e1-107">ويتم تحديد تحويل الصنف المجمع في الصنف المجمع نفسه.</span><span class="sxs-lookup"><span data-stu-id="074e1-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="074e1-108">ويمكن تعبئة الأصناف المعبأة في حاويات بحجم واحد أو بأحجام متعددة تعتبر وحدة واحدة.</span><span class="sxs-lookup"><span data-stu-id="074e1-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="074e1-109">ومن خلال تجميع الأوامر لعنصر مجمع، يمكنك مشاهدة جميع الأوامر الدُفعية ذات الصلة في طريقة عرض واحدة تساعدك في تحديد أي عمل متبقٍ يجب إكماله.</span><span class="sxs-lookup"><span data-stu-id="074e1-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="074e1-110">يمكن أن يحتوي الأمر الدفعي المجمع على أي مجموعة من الأوامر التالية:</span><span class="sxs-lookup"><span data-stu-id="074e1-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="074e1-111">أمر مجمع واحد وأوامر معبأة متعددة</span><span class="sxs-lookup"><span data-stu-id="074e1-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="074e1-112">أوامر مجمعة متعددة وأوامر معبأة متعددة</span><span class="sxs-lookup"><span data-stu-id="074e1-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="074e1-113">أوامر مجمعة متعددة وأمر معبأ واحد</span><span class="sxs-lookup"><span data-stu-id="074e1-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="074e1-114">الأوامر المعبأة فقط.</span><span class="sxs-lookup"><span data-stu-id="074e1-114">Only packed orders</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]