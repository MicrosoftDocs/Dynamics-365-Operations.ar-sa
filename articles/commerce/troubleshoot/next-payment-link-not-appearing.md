---
title: عدم ظهور خيار الحفظ للدفع التالي
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خانة الاختيار الحفظ للدفع التالي تحت طريقه الدفع في صفحة السداد مع الخروج الخاصة بموقع التجارة الإلكترونية.
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
ms.openlocfilehash: 7e3156d1aa9a05dc5d159b6f9b33ae341de640bf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801689"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="5dc11-103">عدم ظهور خيار "الحفظ للدفع التالي"</span><span class="sxs-lookup"><span data-stu-id="5dc11-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5dc11-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خانة الاختيار **الحفظ للدفع التالي** تحت **طريقه الدفع** في صفحة السداد مع الخروج الخاصة بموقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5dc11-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="5dc11-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="5dc11-105">Description</span></span>

<span data-ttu-id="5dc11-106">لا تظهر خانة الاختيار **الحفظ للدفع التالي** في قسم **طريقة الدفع** في صفحة السداد مع الخروج لموقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5dc11-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="5dc11-107">يبين الرسم التوضيحي التالي مثالا لصفحة السداد مع الخروج التي تتضمن خانة الاختيار **الحفظ للدفع التالي**.</span><span class="sxs-lookup"><span data-stu-id="5dc11-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![خانة الاختيار الحفظ للدفع التالي في وحدة الدفع النمطية](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="5dc11-109">الدقة</span><span class="sxs-lookup"><span data-stu-id="5dc11-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="5dc11-110">التحقق من تكوين موصل الدفع Dynamics 365 لـ Adyen بشكل صحيح في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="5dc11-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="5dc11-111">للتحقق من تكوين موصل الدفع Dynamics 365 لـ Adyen بشكل صحيح في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5dc11-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5dc11-112">انتقل إلى **Retail وCommerce \> القنوات \> المتاجر على الإنترنت**.</span><span class="sxs-lookup"><span data-stu-id="5dc11-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="5dc11-113">حدد متجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="5dc11-113">Select the online store.</span></span>
1. <span data-ttu-id="5dc11-114">في علامة التبويب السريعة **حسابات الدفع**، تأكد من تعيين حقل **السماح بحفظ معلومات الدفع في التجارة الإلكترونية** على القيمة **True**.</span><span class="sxs-lookup"><span data-stu-id="5dc11-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![السماح بحفظ معلومات الدفع في حقل التجارة الإلكترونية في المركز الرئيسي لـ Commerce](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="5dc11-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5dc11-116">Additional resources</span></span>

[<span data-ttu-id="5dc11-117">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="5dc11-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="5dc11-118">حفظ وسائل الدفع عبر الإنترنت باستخدام موصل Adyen</span><span class="sxs-lookup"><span data-stu-id="5dc11-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)
