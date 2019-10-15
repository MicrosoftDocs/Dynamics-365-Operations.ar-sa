---
title: إرجاع أصناف عبر عدة فواتير وأوامر مبيعات للعملاء
description: يوضح هذا الموضوع الوظيفة التي تمكّن عمليات الإرجاع عبر العديد من الفواتير وأوامر العملاء في Dynamics 365 Retail.
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
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017979"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="840d9-103">إرجاع أصناف عبر عدة فواتير وأوامر مبيعات للعملاء</span><span class="sxs-lookup"><span data-stu-id="840d9-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="840d9-104">يمكن إجراء عمليات إرجاع عبر العديد من الفواتير والأوامر.</span><span class="sxs-lookup"><span data-stu-id="840d9-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="840d9-105">تكوين بيع بالتجزئة لدعم عمليات الإرجاع عبر العديد من الفواتير وأوامر العملاء</span><span class="sxs-lookup"><span data-stu-id="840d9-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="840d9-106">انتقل إلى **معلمات البيع بالتجزئة \> أوامر العميل‬**.</span><span class="sxs-lookup"><span data-stu-id="840d9-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="840d9-107">قم بتشغيل المعلمة **تمكين المرتجعات لأوامر متعددة‬**.</span><span class="sxs-lookup"><span data-stu-id="840d9-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="840d9-108">معالجة المرتجعات</span><span class="sxs-lookup"><span data-stu-id="840d9-108">Process returns</span></span>

<span data-ttu-id="840d9-109">بعد تشغيل المعلمة ومزامنة التغييرات مع المتاجر، بإمكان أمين الصندوق في المتجر تحديد أوامر مبيعات متعددة لعميل لمعالجة المرتجعات.</span><span class="sxs-lookup"><span data-stu-id="840d9-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="840d9-110">عند تحديد الأوامر، تظهر قائمة بكافة المنتجات القابلة للإرجاع عبر كافة الفواتير الخاصة بالأوامر.</span><span class="sxs-lookup"><span data-stu-id="840d9-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="840d9-111">بإمكان أمين الصندوق عندئذٍ تحديد المنتجات المطلوب إرجاعها.</span><span class="sxs-lookup"><span data-stu-id="840d9-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="840d9-112">سيتم إنشاء أمر إرجاع واحد لكافة المنتجات المحددة.</span><span class="sxs-lookup"><span data-stu-id="840d9-112">A single return order will be created for all the selected products.</span></span>
