---
title: تعرض صفحة إدخال بطاقة الائتمان خطأ عند السحب
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم تحميل قسم طريقة الدفع وظهور رسالة خطأ.
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
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018496"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="ac796-103">تعرض صفحة إدخال بطاقة الائتمان خطأ عند السحب</span><span class="sxs-lookup"><span data-stu-id="ac796-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac796-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم تحميل قسم **طريقة الدفع** وظهور رسالة خطأ.</span><span class="sxs-lookup"><span data-stu-id="ac796-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="ac796-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="ac796-105">Description</span></span>

<span data-ttu-id="ac796-106">عند فتح صفحة السداد مع الخروج من متجر على الإنترنت، لا يتم تحميل قسم **طريقة الدفع**، وتظهر رسالة الخطأ التالية: "حدث خطأ ما.</span><span class="sxs-lookup"><span data-stu-id="ac796-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="ac796-107">الرجاء المحاولة مره أخرى لاحقا."</span><span class="sxs-lookup"><span data-stu-id="ac796-107">Please try again later."</span></span>

![خطأ الوحدة النمطية للدفع](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="ac796-109">الدقة</span><span class="sxs-lookup"><span data-stu-id="ac796-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="ac796-110">انتظار انتهاء صلاحية ذاكره التخزين المؤقت لوحدة Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="ac796-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="ac796-111">يتم تخزين إعدادات خدمة الدفع في صفحة السداد مع الخروج لمتجر الإنترنت بشكل مؤقت في وحدة Commerce Scale Unit وقد تستغرق 15 دقيقه لتظهر في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ac796-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="ac796-112">تتضمن إعدادات خدمة الدفع هذه تغييرات في معرف حساب التاجر ومفتاح واجهة برمجة تطبيقات السحابة وإعدادات التكوين المتنوعة المرتبطة بطريقه الدفع.</span><span class="sxs-lookup"><span data-stu-id="ac796-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac796-113">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ac796-113">Additional resources</span></span>

[<span data-ttu-id="ac796-114">إعداد قناة على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="ac796-114">Set up an online channel</span></span>](../channel-setup-online.md)
