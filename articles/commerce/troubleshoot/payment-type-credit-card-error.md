---
title: خطأ نوع الدفع يجب أن يكون بطاقة ائتمان في صفحة أمر المبيعات
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة ظهور رسالة خطأ في صفحة أمر المبيعات بعد مزامنة أحد الأوامر.
author: Reza-Assadi
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
ms.openlocfilehash: eabc64acc74645c7e6c7c4ab5794ed9fdb9dc997
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801665"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="8439a-103">خطأ "نوع الدفع يجب أن يكون بطاقة ائتمان" في صفحة أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="8439a-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8439a-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة ظهور رسالة خطأ في صفحة أمر المبيعات بعد مزامنة أحد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="8439a-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="8439a-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="8439a-105">Description</span></span>

<span data-ttu-id="8439a-106">عند فتح صفحة أمر المبيعات بعد مزامنة أحد الأوامر، تتلقي رسالة الخطا التالية: "يجب أن يكون نوع الدفع بطاقة ائتمان، نظرًا لأنه تم تحديد رقم بطاقة الائتمان."</span><span class="sxs-lookup"><span data-stu-id="8439a-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![خطأ نوع الدفع يجب أن يكون بطاقة ائتمان](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="8439a-108">الدقة</span><span class="sxs-lookup"><span data-stu-id="8439a-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="8439a-109">تعيين نوع الدفع في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="8439a-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="8439a-110">انتقل إلى **الحسابات المدينة \> إعداد المدفوعات‬ \> شروط الدفع**.</span><span class="sxs-lookup"><span data-stu-id="8439a-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="8439a-111">فى جزء التنقل الأيمن، حدد شروط الدفع.</span><span class="sxs-lookup"><span data-stu-id="8439a-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="8439a-112">في حقل **نوع الدفع**، تأكد من تحديد **بطاقة ائتمان**.</span><span class="sxs-lookup"><span data-stu-id="8439a-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8439a-113">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8439a-113">Additional resources</span></span>

[<span data-ttu-id="8439a-114">ترحيل الدفعات والمبيعات على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="8439a-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
