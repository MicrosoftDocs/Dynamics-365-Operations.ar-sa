---
title: إرجاع أصناف عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء
description: يصف هذا الموضوع الوظيفة التي تمكّن عمليات الإرجاع عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء في Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
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
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2019
ms.locfileid: "373058"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="ef311-103">إرجاع أصناف عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء</span><span class="sxs-lookup"><span data-stu-id="ef311-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="ef311-104">في الإصدار 10.0 من Dynamics 365 for Finance and Operations، يمكنك إجراء عمليات إرجاع عبر أوامر وفواتير متعددة، في حين أن معالجة عمليات الإرجاع في الإصدارات التي تسبق الإصدار 10.0 كانت تتم فقط بواسطة كل فاتورة على حدة.</span><span class="sxs-lookup"><span data-stu-id="ef311-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="ef311-105">تكوين Retail لدعم عمليات الإرجاع عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء</span><span class="sxs-lookup"><span data-stu-id="ef311-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="ef311-106">انتقل إلى **معلمات Retail \> أوامر العميل‬**.</span><span class="sxs-lookup"><span data-stu-id="ef311-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="ef311-107">قم بتشغيل المعلمة **تمكين المرتجعات لأوامر متعددة‬**.</span><span class="sxs-lookup"><span data-stu-id="ef311-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="ef311-108">معالجة المرتجعات</span><span class="sxs-lookup"><span data-stu-id="ef311-108">Process returns</span></span>

<span data-ttu-id="ef311-109">بعد تشغيل المعلمة ومزامنة التغييرات مع المتاجر، بإمكان أمين الصندوق في المتجر تحديد أوامر مبيعات متعددة لعميل لمعالجة المرتجعات.</span><span class="sxs-lookup"><span data-stu-id="ef311-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="ef311-110">عند تحديد الأوامر، تظهر قائمة بكافة المنتجات القابلة للإرجاع عبر كافة الفواتير الخاصة بالأوامر.</span><span class="sxs-lookup"><span data-stu-id="ef311-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="ef311-111">بإمكان أمين الصندوق عندئذٍ تحديد المنتجات المطلوب إرجاعها.</span><span class="sxs-lookup"><span data-stu-id="ef311-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="ef311-112">سيتم إنشاء أمر إرجاع واحد لكافة المنتجات المحددة.</span><span class="sxs-lookup"><span data-stu-id="ef311-112">A single return order will be created for all the selected products.</span></span>
