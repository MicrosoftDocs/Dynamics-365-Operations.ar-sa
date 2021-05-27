---
title: خطأ نوع الدفع يجب أن يكون بطاقة ائتمان في صفحة أمر المبيعات
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة ظهور رسالة خطأ في صفحة أمر المبيعات بعد مزامنة أحد الأوامر.
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
ms.openlocfilehash: 5be19949e9d1dbc43fdd3e6def119effa50a34d0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018400"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="6542b-103">خطأ "نوع الدفع يجب أن يكون بطاقة ائتمان" في صفحة أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="6542b-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6542b-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة ظهور رسالة خطأ في صفحة أمر المبيعات بعد مزامنة أحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="6542b-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="6542b-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="6542b-105">Description</span></span>

<span data-ttu-id="6542b-106">عند فتح صفحة أمر المبيعات بعد مزامنة أحد الأوامر، تتلقي رسالة الخطا التالية: "يجب أن يكون نوع الدفع بطاقة ائتمان، نظرًا لأنه تم تحديد رقم بطاقة الائتمان."</span><span class="sxs-lookup"><span data-stu-id="6542b-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![خطأ نوع الدفع يجب أن يكون بطاقة ائتمان](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="6542b-108">الدقة</span><span class="sxs-lookup"><span data-stu-id="6542b-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="6542b-109">تعيين نوع الدفع في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="6542b-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="6542b-110">انتقل إلى **الحسابات المدينة \> إعداد المدفوعات‬ \> شروط الدفع**.</span><span class="sxs-lookup"><span data-stu-id="6542b-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="6542b-111">فى جزء التنقل الأيمن، حدد شروط الدفع.</span><span class="sxs-lookup"><span data-stu-id="6542b-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="6542b-112">في حقل **نوع الدفع**، تأكد من تحديد **بطاقة ائتمان**.</span><span class="sxs-lookup"><span data-stu-id="6542b-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6542b-113">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6542b-113">Additional resources</span></span>

[<span data-ttu-id="6542b-114">ترحيل الدفعات والمبيعات على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="6542b-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
