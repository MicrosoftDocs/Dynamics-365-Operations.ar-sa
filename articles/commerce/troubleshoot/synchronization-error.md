---
title: خطا مزامنة الأمر المرتبط بخدمة الدفع الافتراضية
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في إصلاح خطأ قد يحدث عند مزامنة أمر عبر الإنترنت.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021117"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="0727d-103">خطا مزامنة الأمر المرتبط بخدمة الدفع الافتراضية</span><span class="sxs-lookup"><span data-stu-id="0727d-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0727d-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في إصلاح خطأ قد يحدث عند مزامنة أمر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="0727d-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="0727d-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="0727d-105">Description</span></span>

<span data-ttu-id="0727d-106">عند مزامنة أحد الأوامر عبر الإنترنت، تتلقي رسالة الخطأ التالية: "يجب أن يكون هناك خدمة دفع افتراضية لمعالجة حركات بطاقات الائتمان."</span><span class="sxs-lookup"><span data-stu-id="0727d-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![خطأ خدمة الدفع الافتراضية مفقودة](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="0727d-108">الدقة</span><span class="sxs-lookup"><span data-stu-id="0727d-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="0727d-109">تأكيد خدمة الدفع الافتراضية في المركز الرئيسي لـ Commerce أو تعيينها</span><span class="sxs-lookup"><span data-stu-id="0727d-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="0727d-110">لتأكيد خدمة الدفع الافتراضية في المركز الرئيسي لـ Commerce أو تعيينها، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0727d-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0727d-111">انتقل إلى **الحسابات المدينة \> إعداد المدفوعات‬ \> ‏‫خدمات الدفع‬**.</span><span class="sxs-lookup"><span data-stu-id="0727d-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="0727d-112">تأكد من تعيين خيار **المعالج الافتراضي لبطاقات الائتمان الجديدة** على **نعم** لخدمة دفع واحدة.</span><span class="sxs-lookup"><span data-stu-id="0727d-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0727d-113">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0727d-113">Additional resources</span></span>

[<span data-ttu-id="0727d-114">إعداد بطاقة الائتمان وتفويضها والتقاطها</span><span class="sxs-lookup"><span data-stu-id="0727d-114">Credit card setup, authorization, and capture</span></span>](../../finance/accounts-receivable/credit-card-authorizations.md)