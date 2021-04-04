---
title: تسوية المدفوعات تلقائيا قبل فوترة الأوامر أو شحنها
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عند تسوية الدفع في مدخل Adyen مباشرة بعد تقديم أمر ما، حتى وإن لم يكن قد تمت فوترة أمر المبيعات أو شحنه.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585177"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="19dbb-103">تسوية المدفوعات تلقائيا قبل فوترة الأوامر أو شحنها</span><span class="sxs-lookup"><span data-stu-id="19dbb-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19dbb-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عند تسوية الدفع في مدخل Adyen مباشرة بعد تقديم أمر ما، حتى وإن لم يكن قد تمت فوترة أمر المبيعات أو شحنه.</span><span class="sxs-lookup"><span data-stu-id="19dbb-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="19dbb-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="19dbb-105">Description</span></span>

<span data-ttu-id="19dbb-106">بعد تقديم أحد الأوامر، تتم تسوية الدفع مباشرة في مدخل Adyen مباشرة، حتى وإن لم يكن قد تمت فوترة أمر المبيعات أو شحنه.</span><span class="sxs-lookup"><span data-stu-id="19dbb-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="19dbb-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="19dbb-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="19dbb-108">تكوين الالتقاط اليدوي لمدفوعات التجارة الإلكترونية في مدخل Adyen</span><span class="sxs-lookup"><span data-stu-id="19dbb-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="19dbb-109">لتكوين الالتقاط اليدوي لمدفوعات التجارة الإلكترونية في مدخل Adyen، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="19dbb-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="19dbb-110">سجل الدخول إلى مدخل Adyen.</span><span class="sxs-lookup"><span data-stu-id="19dbb-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="19dbb-111">في الركن الأيمن العلوي، حدد حساب التاجر الخاص بك لقناة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="19dbb-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="19dbb-112">في جزء التنقل العلوي، حدد **الحساب**، ثم حدد **الإعدادات**.</span><span class="sxs-lookup"><span data-stu-id="19dbb-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="19dbb-113">في حقل **تأخير الالتقاط**، حدد **يدوي**.</span><span class="sxs-lookup"><span data-stu-id="19dbb-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![إعداد تأخير الالتقاط في مدخل Adyen](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="19dbb-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="19dbb-115">Additional resources</span></span>

[<span data-ttu-id="19dbb-116">التقاط مدفوعات Adyen</span><span class="sxs-lookup"><span data-stu-id="19dbb-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="19dbb-117">موصل دفع Dynamics 365 لـ Adyen</span><span class="sxs-lookup"><span data-stu-id="19dbb-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="19dbb-118">إعداد موصل دفع Adyen لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="19dbb-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
