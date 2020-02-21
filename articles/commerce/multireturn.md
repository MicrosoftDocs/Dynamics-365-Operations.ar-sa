---
title: إرجاع أصناف عبر عدة فواتير وأوامر مبيعات للعملاء
description: يوضح هذا الموضوع الوظيفة التي تمكّن عمليات الإرجاع عبر العديد من الفواتير وأوامر العملاء في Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004448"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="823b8-103">إرجاع أصناف عبر عدة فواتير وأوامر مبيعات للعملاء</span><span class="sxs-lookup"><span data-stu-id="823b8-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="823b8-104">يمكن إجراء عمليات إرجاع عبر العديد من الفواتير والأوامر.</span><span class="sxs-lookup"><span data-stu-id="823b8-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="823b8-105">تكوين Commerce لدعم عمليات الإرجاع عبر العديد من الفواتير وأوامر العملاء</span><span class="sxs-lookup"><span data-stu-id="823b8-105">Configure Commerce to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="823b8-106">انتقل إلى **معلمات Commerce \> أوامر العميل‬**.</span><span class="sxs-lookup"><span data-stu-id="823b8-106">Go to **Commerce parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="823b8-107">قم بتشغيل المعلمة **تمكين المرتجعات لأوامر متعددة‬**.</span><span class="sxs-lookup"><span data-stu-id="823b8-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="823b8-108">معالجة المرتجعات</span><span class="sxs-lookup"><span data-stu-id="823b8-108">Process returns</span></span>

<span data-ttu-id="823b8-109">بعد تشغيل المعلمة ومزامنة التغييرات مع المتاجر، بإمكان أمين الصندوق في المتجر تحديد أوامر مبيعات متعددة لعميل لمعالجة المرتجعات.</span><span class="sxs-lookup"><span data-stu-id="823b8-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="823b8-110">عند تحديد الأوامر، تظهر قائمة بكافة المنتجات القابلة للإرجاع عبر كافة الفواتير الخاصة بالأوامر.</span><span class="sxs-lookup"><span data-stu-id="823b8-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="823b8-111">بإمكان أمين الصندوق عندئذٍ تحديد المنتجات المطلوب إرجاعها.</span><span class="sxs-lookup"><span data-stu-id="823b8-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="823b8-112">سيتم إنشاء أمر إرجاع واحد لكافة المنتجات المحددة.</span><span class="sxs-lookup"><span data-stu-id="823b8-112">A single return order will be created for all the selected products.</span></span>
