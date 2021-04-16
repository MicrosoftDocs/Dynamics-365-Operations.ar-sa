---
title: رفض المبلغ المسترد في أمر الإرجاع
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة رفض المبلغ المسترد لأمر الإرجاع نظرا لأن بطاقة الائتمان المستخدمة للفوترة تختلف عن البطاقة التي تم استخدامها أثناء تفويض الدفع الأصلي.
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
ms.openlocfilehash: 5961e77de1de5dc23454fc1a6e16f8c0b4e7cc6a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801545"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="884bc-103">رفض المبلغ المسترد في أمر الإرجاع</span><span class="sxs-lookup"><span data-stu-id="884bc-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="884bc-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة رفض المبلغ المسترد لأمر الإرجاع نظرا لأن بطاقة الائتمان المستخدمة للفوترة تختلف عن البطاقة التي تم استخدامها أثناء تفويض الدفع الأصلي.</span><span class="sxs-lookup"><span data-stu-id="884bc-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="884bc-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="884bc-105">Description</span></span>

<span data-ttu-id="884bc-106">يتم رفض المبلغ المسترد عندما تختلف بطاقة الائتمان المستخدمة لفوترة أمر الإرجاع عن البطاقة التي تم استخدامها أثناء تفويض الدفع الأصلي.</span><span class="sxs-lookup"><span data-stu-id="884bc-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="884bc-107">تظهر رسالة الخطا التالية: بعض المدفوعات ليست بالحالة الصحيحة للترحيل.</span><span class="sxs-lookup"><span data-stu-id="884bc-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="884bc-108">الرجاء إعادة التحقق من صحة حالة كافة المدفوعات السابقة للفوترة."</span><span class="sxs-lookup"><span data-stu-id="884bc-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="884bc-109">ستتضمن تفاصيل تخويل الدفع رسالة الخطا التالية: "فشل SendRequest() في بوابة Adyen بالحالة'InternalServerError'.22144; تم إرجاع استجابة فارغة من Adyen.(22001);"</span><span class="sxs-lookup"><span data-stu-id="884bc-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![خطأ رفض المبلغ المسترد في أمر الإرجاع](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="884bc-111">الدقة</span><span class="sxs-lookup"><span data-stu-id="884bc-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="884bc-112">تمكين المرتجعات المخفيه في Adyen</span><span class="sxs-lookup"><span data-stu-id="884bc-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="884bc-113">لتمكين المرتجعات المخفية، اتبع الخطوات الموجودة في [استكشاف الأخطاء وإصلاح مشكلات موصل الدفع Dynamics 365 لـ Adyen](adyen-support.md) للاتصال بفريق دعم Adyen وطلب أن يتم تمكين المرتجعات المخفية في حساب تاجر Adyen الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="884bc-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="884bc-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="884bc-114">Additional resources</span></span>

[<span data-ttu-id="884bc-115">موصل دفع Dynamics 365 لـ Adyen</span><span class="sxs-lookup"><span data-stu-id="884bc-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="884bc-116">إعداد موصل دفع Adyen لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="884bc-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
